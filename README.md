## 最新更新记录

### 2.2.1

- 新增法定节假日判断，调休日判断
- 法定节假日新增 `isSwap` 字段，用于判断该假期是否有调休日
- 法定节假日新增 `swapDate` 字段，如果 `isSwap` 为 `true`，则该字段展示本法定节假日的调休日数组
- 新增 `type` 字段 1/正常日，2/法定节假日，3/调休日

## NPM
> npm i festival_chn

## USE
> import festival from "@/utils/festival.js";

## PARMAES
> date 需要符合 "yyyy-mm-dd" 格式
> const date = "2022-01-01"
> const res = festival(date);

## RETURN

|字段名称|字段类型|返回状态|说明|
|----|----|----|----|
|name|String|必返|节假日名称/调休/正常|
|type|Number|必返|1/正常 2/节假日 3/调休日|
|isSwap|Boolean|法定节假日必返|true/有调休 false/无调休|
|swapDate|Array|法定节假日有调休日必返|调休日组成的数组|