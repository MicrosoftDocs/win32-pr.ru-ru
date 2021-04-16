---
description: '\_Константы линеажентстатикс описывают состояние агента по адресу.'
ms.assetid: d49025c5-f1db-4b71-a2d5-1cf3df66f3e5
title: Константы LINEAGENTSTATEEX_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 214b816a35e3fdb420a9d95772c466791c6d2f2c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689395"
---
# <a name="lineagentstateex_-constants"></a>\_Константы линеажентстатикс

**\_ Константы линеажентстатикс** описывают состояние агента по адресу.

<dl> <dt>

<span id="LINEAGENTSTATEEX_BUSYACD"></span><span id="lineagentstateex_busyacd"></span>**ЛИНЕАЖЕНТСТАТИКС \_ бусякд**
</dt> <dd> <dl> <dt>



Агент занят обработкой вызова, направляемого из очереди ACD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYINCOMING"></span><span id="lineagentstateex_busyincoming"></span>**ЛИНЕАЖЕНТСТАТИКС \_ бусинкоминг**
</dt> <dd> <dl> <dt>



Агент занят обработкой входящего вызова, который не был передан агенту из очереди ACD, в которой вошел агент.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_BUSYOUTGOING"></span><span id="lineagentstateex_busyoutgoing"></span>**ЛИНЕАЖЕНТСТАТИКС \_ бусйоутгоинг**
</dt> <dd> <dl> <dt>



Агент занят обработкой исходящего вызова, например одного маршрута из очереди прогнозируемого набора.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_NOTREADY"></span><span id="lineagentstateex_notready"></span>**ЛИНЕАЖЕНТСТАТИКС \_ NOTREADY**
</dt> <dd> <dl> <dt>



Агент вошел в систему, но занят задачей, отличной от обслуживания вызова (например, при прерывании). Никакие дополнительные вызовы не должны маршрутизироваться агенту.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_READY"></span><span id="lineagentstateex_ready"></span>**ЛИНЕАЖЕНТСТАТИКС \_ Готово**
</dt> <dd> <dl> <dt>



Агент готов принять вызовы.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_RELEASED"></span><span id="lineagentstateex_released"></span>**ЛИНЕАЖЕНТСТАТИКС \_ выпущен**
</dt> <dd> <dl> <dt>



Агент был выпущен, возможно, из-за того, что он вышел из системы.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATEEX_UNKNOWN"></span><span id="lineagentstateex_unknown"></span>**ЛИНЕАЖЕНТСТАТИКС \_ неизвестный**
</dt> <dd> <dl> <dt>



Состояние агента неизвестно, но может быть известно позже. Это может быть переходное состояние при первом открытии строки или адреса.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




