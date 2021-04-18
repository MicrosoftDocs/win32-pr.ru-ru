---
description: '\_Константы линекаллоригин описывают происхождение вызова.'
ms.assetid: b830a40e-62d9-4a6c-b43f-8318f30a7cd4
title: Константы LINECALLORIGIN_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f00495d67dcff56ef7ee34cd85600a281e006ec3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105675245"
---
# <a name="linecallorigin_-constants"></a>\_Константы линекаллоригин

Константы **линекаллоригин \_** описывают происхождение вызова.

<dl> <dt>

<span id="LINECALLORIGIN_CONFERENCE"></span><span id="linecallorigin_conference"></span>**\_Конференция линекаллоригин**
</dt> <dd> <dl> <dt>



Обработчик вызова предназначен для вызова конференции, т. е. это подключение приложения к мосту конференции в коммутаторе.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_EXTERNAL"></span><span id="linecallorigin_external"></span>**ЛИНЕКАЛЛОРИГИН \_ внешний**
</dt> <dd> <dl> <dt>



Вызов создан как входящий вызов на внешней строке.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INBOUND"></span><span id="linecallorigin_inbound"></span>**ЛИНЕКАЛЛОРИГИН \_ входящий трафик**
</dt> <dd> <dl> <dt>



Вызов создан как входящий вызов, но поставщик услуг не может определить, поступил ли он с другой станции на том же коммутаторе или на внешней строке. Поставщики услуг могут использовать эту константу только при согласовании TAPI версии 1,4 или более поздней. В противном случае поставщик услуг может заменить ЛИНЕКАЛЛОРИГИН \_ .


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_INTERNAL"></span><span id="linecallorigin_internal"></span>**\_Внутренняя линекаллоригин**
</dt> <dd> <dl> <dt>



Вызов создан как входящий вызов на станции, внутренней для той же среды коммутации.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_OUTBOUND"></span><span id="linecallorigin_outbound"></span>**ЛИНЕКАЛЛОРИГИН \_ исходящий трафик**
</dt> <dd> <dl> <dt>



Вызов был получен от станции как исходящий вызов.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNAVAIL"></span><span id="linecallorigin_unavail"></span>**ЛИНЕКАЛЛОРИГИН \_ НЕсвободно**
</dt> <dd> <dl> <dt>



Источник вызова недоступен и никогда не будет известен для этого вызова.


</dt> </dl> </dd> <dt>

<span id="LINECALLORIGIN_UNKNOWN"></span><span id="linecallorigin_unknown"></span>**ЛИНЕКАЛЛОРИГИН \_ неизвестный**
</dt> <dd> <dl> <dt>



Источник вызова сейчас неизвестен, но может быть известен позже.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Комментарии

Без расширяемости. Все 32 бит зарезервированы.

Источник вызова хранится в элементе **dwOrigin** структуры [**линекаллинфо**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) вызова.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Header<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




