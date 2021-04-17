---
description: '\_Константы линеажентсессионстате описывают различные состояния сеанса агента.'
ms.assetid: 8a0d06bb-51ba-4eaf-8719-120aed817f63
title: Константы LINEAGENTSESSIONSTATE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdfd1be8cf846d0e23828f0a3540960a86a83ef1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675421"
---
# <a name="lineagentsessionstate_-constants"></a>\_Константы линеажентсессионстате

**\_ Константы линеажентсессионстате** описывают различные состояния сеанса агента.

<dl> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYONCALL"></span><span id="lineagentsessionstate_busyoncall"></span>**ЛИНЕАЖЕНТСЕССИОНСТАТЕ \_ бусйонкалл**
</dt> <dd> <dl> <dt>



Агент занят обработкой вызова.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_BUSYWRAPUP"></span><span id="lineagentsessionstate_busywrapup"></span>**ЛИНЕАЖЕНТСЕССИОНСТАТЕ \_ бусиврапуп**
</dt> <dd> <dl> <dt>



Агент занят обработкой оболочки вызова.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_ENDED"></span><span id="lineagentsessionstate_ended"></span>**ЛИНЕАЖЕНТСЕССИОНСТАТЕ \_ завершено**
</dt> <dd> <dl> <dt>



Сеанс агента завершен.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_NOTREADY"></span><span id="lineagentsessionstate_notready"></span>**ЛИНЕАЖЕНТСЕССИОНСТАТЕ \_ NOTREADY**
</dt> <dd> <dl> <dt>



Агент вошел в систему, но занят задачей, отличной от обслуживания вызова (например, при прерывании). Никакие дополнительные вызовы не должны маршрутизироваться агенту.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_READY"></span><span id="lineagentsessionstate_ready"></span>**ЛИНЕАЖЕНТСЕССИОНСТАТЕ \_ Готово**
</dt> <dd> <dl> <dt>



Агент готов принять вызовы.


</dt> </dl> </dd> <dt>

<span id="LINEAGENTSESSIONSTATE_RELEASED"></span><span id="lineagentsessionstate_released"></span>**ЛИНЕАЖЕНТСЕССИОНСТАТЕ \_ выпущен**
</dt> <dd> <dl> <dt>



Сеанс агента был выпущен.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,2<br/>                                                      |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




