---
description: '\_Константы побитового флага линедиалтонемоде описывают различные типы тонов набора. Специальный гудок обычно несет специальное значение (как в ожидании сообщения).'
ms.assetid: 0b040482-35cf-42e8-84bc-33002635b591
title: Константы LINEDIALTONEMODE_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5128f2a176f3aeaf92bc3487b131b7720568085e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105685156"
---
# <a name="linedialtonemode_-constants"></a>\_Константы линедиалтонемоде

Константы побитового флага **линедиалтонемоде \_** описывают различные типы тонов набора. Специальный гудок обычно несет специальное значение (как в ожидании сообщения).

<dl> <dt>

<span id="LINEDIALTONEMODE_EXTERNAL"></span><span id="linedialtonemode_external"></span>**ЛИНЕДИАЛТОНЕМОДЕ \_ внешний**
</dt> <dd> <dl> <dt>



Это внешний гудок (в общедоступной сети).


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_INTERNAL"></span><span id="linedialtonemode_internal"></span>**\_Внутренняя линедиалтонемоде**
</dt> <dd> <dl> <dt>



Это внутренний гудок, как в УАТС.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_NORMAL"></span><span id="linedialtonemode_normal"></span>**ЛИНЕДИАЛТОНЕМОДЕ, \_ Обычная**
</dt> <dd> <dl> <dt>



Это стандартный гудок, который обычно является непрерывным.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_SPECIAL"></span><span id="linedialtonemode_special"></span>**\_специальное линедиалтонемоде**
</dt> <dd> <dl> <dt>



Это специальный гудок, указывающий на то, что в настоящее время действует определенное условие (известное коммутатору или сети). Специальные звуки обычно используют Прерванный тон. Как и при нормальном тоновом наборе, это означает, что коммутатор готов к получению номера для набора.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNAVAIL"></span><span id="linedialtonemode_unavail"></span>**ЛИНЕДИАЛТОНЕМОДЕ \_ НЕсвободно**
</dt> <dd> <dl> <dt>



Режим «гудок» недоступен и не будет известен.


</dt> </dl> </dd> <dt>

<span id="LINEDIALTONEMODE_UNKNOWN"></span><span id="linedialtonemode_unknown"></span>**ЛИНЕДИАЛТОНЕМОДЕ \_ неизвестный**
</dt> <dd> <dl> <dt>



Режим «гудок» в настоящее время не известен, но может быть известен позже.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Старшие 16 бит можно назначить для расширений для конкретных устройств. 16 младших разрядов зарезервированы.

**\_ Константы линедиалтонемоде** используются в структуре данных [**линекаллстатус**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) для вызова в состоянии диалтоне.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




