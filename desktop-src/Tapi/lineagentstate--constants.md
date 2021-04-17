---
description: '\_Константы линеажентстате описывают состояние агента по адресу.'
ms.assetid: 1dbc33e7-05cc-4cb9-8904-f495b884b8db
title: Константы LINEAGENTSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 90b5afa8f93cfde5529f8f57fd8e48d37ecd415b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679913"
---
# <a name="lineagentstate_-constants"></a>\_Константы линеажентстате

**\_ Константы линеажентстате** описывают состояние агента по адресу.

<dl> <dt>

<span id="LINEAGENTSTATE_BUSYACD"></span><span id="lineagentstate_busyacd"></span>**ЛИНЕАЖЕНТСТАТЕ \_ бусякд**
</dt> <dd> <dl> <dt>



Агент занят обработкой вызова, направляемого из очереди ACD.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYINCOMING"></span><span id="lineagentstate_busyincoming"></span>**ЛИНЕАЖЕНТСТАТЕ \_ бусинкоминг**
</dt> <dd> <dl> <dt>



Агент занят обработкой входящего вызова, который не был передан агенту из очереди ACD, в которой вошел агент.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOTHER"></span><span id="lineagentstate_busyother"></span>**ЛИНЕАЖЕНТСТАТЕ \_ бусйосер**
</dt> <dd> <dl> <dt>



Агент занят обработкой другого типа вызова, например, исходящего личного звонка, не переданного агенту с помощью прогнозирующего набора. Это значение можно также использовать, когда агент может быть занят при вызове, но тип вызова неизвестен.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_BUSYOUTBOUND"></span><span id="lineagentstate_busyoutbound"></span>**ЛИНЕАЖЕНТСТАТЕ \_ бусйоутбаунд**
</dt> <dd> <dl> <dt>



Агент занят обработкой исходящего вызова, например одного маршрута из очереди прогнозируемого набора.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_LOGGEDOFF"></span><span id="lineagentstate_loggedoff"></span>**ЛИНЕАЖЕНТСТАТЕ \_ логжедофф**
</dt> <dd> <dl> <dt>



В адресе не вошел агент.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_NOTREADY"></span><span id="lineagentstate_notready"></span>**ЛИНЕАЖЕНТСТАТЕ \_ NOTREADY**
</dt> <dd> <dl> <dt>



Агент вошел в систему, но занят задачей, отличной от обслуживания вызова (например, при прерывании). Никакие дополнительные вызовы не должны маршрутизироваться агенту.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_READY"></span><span id="lineagentstate_ready"></span>**ЛИНЕАЖЕНТСТАТЕ \_ Готово**
</dt> <dd> <dl> <dt>



Агент готов принять вызовы.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNAVAIL"></span><span id="lineagentstate_unavail"></span>**ЛИНЕАЖЕНТСТАТЕ \_ НЕсвободно**
</dt> <dd> <dl> <dt>



Состояние агента неизвестно и никогда не станет известным. В [**линеаддрессстатус**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)это условие также может быть представлено членом **дважентстате** , для которого задано значение 0.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_UNKNOWN"></span><span id="lineagentstate_unknown"></span>**ЛИНЕАЖЕНТСТАТЕ \_ неизвестный**
</dt> <dd> <dl> <dt>



Состояние агента неизвестно, но может быть известно позже. Это может быть переходное состояние при первом открытии строки или адреса.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSTATE_WORKINGAFTERCALL"></span><span id="lineagentstate_workingaftercall"></span>**ЛИНЕАЖЕНТСТАТЕ \_ воркингафтеркалл**
</dt> <dd> <dl> <dt>



Агент завершил предыдущий вызов, но по-прежнему занят работой, связанным с этим вызовом. Агент не должен принимать дополнительные вызовы.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Верхние 16 разрядов этого набора констант зарезервированы для расширений для конкретных устройств.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




