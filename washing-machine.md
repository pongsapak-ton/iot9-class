# Washing machine state

## START
topic:v1cdti/app/get/6310301020/model-01/SN-001
payload: {
    "action"    :   "get",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "sn-01",
    "name"      :   "STATUS",
    "value"     :   "START"
}

## READY
topic:v1cdti/app/get/6310301020/model-01/sn-01
payload: {
    "action"    :   "get",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "SN-001",
    "name"      :   "STATUS",
    "value"     :   "READY"
}

## FILLWATER
topic:v1cdti/app/get/6310301020/model-01/sn-01
payload: {
    "action"    :   "get",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "SN-001",
    "name"      :   "STATUS",
    "value"     :   "FillWater"
}

## HEATWATER
topic:v1cdti/app/get/6310301020/model-01/sn-01
payload: {
    "action"    :   "get",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "sn-01",
    "name"      :   "STATUS",
    "value"     :   "HeatWater"
}

## WASH
topic:v1cdti/app/get/6310301020/model-01/sn-01
payload: {
    "action"    :   "get",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "sn-01",
    "name"      :   "STATUS",
    "value"     :   "WASH"
}

## RINSE
topic:v1cdti/app/get/6310301020/model-01/sn-01
payload: {
    "action"    :   "get",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "sn-01",
    "name"      :   "STATUS",
    "value"     :   "RINSE"
}
## SPIN
topic:v1cdti/app/get/6310301020/model-01/sn-01
payload: {
    "action"    :   "get",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "sn-01",
    "name"      :   "STATUS",
    "value"     :   "SPIN"
}

# Operation state

## DOORCLOSE
topic:v1cdti/app/set/6310301020/model-01/sn-01
payload: {
    "action"    :   "set",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "sn-01",
    "name"      :   "STATUS",
    "value"     :   "DoorClose"
}

## WATERFULLLEVEL
topic:v1cdti/app/set/6310301020/model-01/sn-01
payload: {
    "action"    :   "set",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "SN-001",
    "name"      :   "WaterLevel",
    "value"     :   "WaterFull"
}

## TEMPERATUREREACHED
topic:v1cdti/app/set/6310301020/model-01/sn-01
payload: {
    "action"    :   "set",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "SN-001",
    "name"      :   "Temperature",
    "value"     :   "REACHED"
}


# FAULT state

## TIMEOUT
topic:v1cdti/app/get/6310301020/model-01/sn-01
payload: {
    "action"    :   "get",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "SN-001",
    "name"      :   "FAULT-state",
    "value"     :   "TimeOut"
}

## OUTOFBALANCE
topic:v1cdti/app/set/6310301020/model-01/sn-01
payload: {
    "action"    :   "set",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "SN-001",
    "name"      :   "FAULT-state",
    "value"     :   "OutofBalance"
}


## MOTORFAILURE
topic:v1cdti/app/set/6310301020/model-01/sn-01
payload: {
    "action"    :   "set",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "SN-001",
    "name"      :   "FAULT-state",
    "value"     :   "MOTORFAILURE"
}


## FAULTCLEARED
topic:v1cdti/app/set/6310301020/model-01/sn-01
payload: {
    "action"    :   "set",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "SN-001",
    "name"      :   "FAULT-state",
    "value"     :   "Clear"
}


  if w.MACHINE_STATUS == 'WaterHeat':
                wait = w.waiting_task()
                await wait
                while w.MACHINE_STATUS == 'WaterHeat':
                    await asyncio.sleep(2)
        
        if w.MACHINE_STATUS == 'FAULT':
            await publish_message(w, client, 'app', 'get', 'FAULT', w.FAULT_TYPE)
            while w.MACHINE_STATUS == 'FAULT':
                print(f"{time.ctime()} - [{w.SERIAL}] Waiting to clear fault...")
                await asyncio.sleep(1)

        if w.MACHINE_STATUS == 'WASHING':
            continue
                