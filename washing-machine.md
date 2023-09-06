# Washing machine state

## START
topic:v1cdti/app/get/6310301020/model-01/sn-01
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
    "serial"    :   "sn-01",
    "name"      :   "STATUS",
    "value"     :   "READY"
}

## FILLWATER
topic:v1cdti/app/get/6310301020/model-01/sn-01
payload: {
    "action"    :   "get",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "sn-01",
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
    "serial"    :   "sn-01",
    "name"      :   "STATUS",
    "value"     :   "WaterFullLevel"
}

## TEMPERATUREREACHED
topic:v1cdti/app/set/6310301020/model-01/sn-01
payload: {
    "action"    :   "set",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "sn-01",
    "name"      :   "STATUS",
    "value"     :   "TEMPERATUREREACHED"
}


# FAULT state

## TIMEOUT
topic:v1cdti/app/get/6310301020/model-01/sn-01
payload: {
    "action"    :   "get",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "sn-01",
    "name"      :   "STATUS",
    "value"     :   "TimeOut"
}

## OUTOFBALANCE
topic:v1cdti/app/set/6310301020/model-01/sn-01
payload: {
    "action"    :   "set",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "sn-01",
    "name"      :   "STATUS",
    "value"     :   "TimeOut"
}


## MOTORFAILURE
topic:v1cdti/app/set/6310301020/model-01/sn-01
payload: {
    "action"    :   "set",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "sn-01",
    "name"      :   "STATUS",
    "value"     :   "TimeOut"
}


## FAULTCLEARED
topic:v1cdti/app/set/6310301020/model-01/sn-01
payload: {
    "action"    :   "set",
    "project"   :   "6310301020",
    "model"     :   "model-01",
    "serial"    :   "sn-01",
    "name"      :   "STATUS",
    "value"     :   "FAULTCLEARED"
}
