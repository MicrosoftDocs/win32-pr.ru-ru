---
description: '\_Константы побитового флага линекаллселект описывают, какие вызовы должны быть выбраны.'
ms.assetid: f19a41bc-403a-4d4b-ab85-240a73514ebb
title: Константы LINECALLSELECT_ (TAPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: feaa76ea5b421b8090f9289431bfee65be61a6b47abd170569beff73a9846533
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003152"
---
# <a name="linecallselect_-constants"></a>\_Константы линекаллселект

Константы побитового флага **линекаллселект \_** описывают, какие вызовы должны быть выбраны.

<dl> <dt>

<span id="LINECALLSELECT_ADDRESS"></span><span id="linecallselect_address"></span>**ЛИНЕКАЛЛСЕЛЕКТ \_ адрес**
</dt> <dd> <dl> <dt>



Выбирает вызов по указанному адресу.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALL"></span><span id="linecallselect_call"></span>**\_вызов линекаллселект**
</dt> <dd> <dl> <dt>



Выбирает связанные вызовы для указанного вызова. Например, участники конференц-связи.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_CALLID"></span><span id="linecallselect_callid"></span>**ЛИНЕКАЛЛСЕЛЕКТ \_ каллид**
</dt> <dd> <dl> <dt>



Выбирает связанные вызовы к указанному идентификатору вызова. Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 3,0 или более позднюю.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_DEVICEID"></span><span id="linecallselect_deviceid"></span>**DEVICEID для ЛИНЕКАЛЛСЕЛЕКТ \_**
</dt> <dd> <dl> <dt>



Выбирает вызовы по указанному идентификатору устройства. Этот флаг предоставляется только приложениям, которые согласовывают версию TAPI 2,1 или более позднюю. В приложениях следует использовать \_ константу строки линекаллселект, а не ее.


</dt> </dl> </dd> <dt>

<span id="LINECALLSELECT_LINE"></span><span id="linecallselect_line"></span>**ЛИНЕКАЛЛСЕЛЕКТ \_ строка**
</dt> <dd> <dl> <dt>



Выбирает вызовы на указанном устройстве линии.


</dt> </dl> </dd> </dl>

## <a name="remarks"></a>Remarks

Без расширяемости. Все 32 бит зарезервированы.

Эта константа используется в [**линежетневкаллс**](/windows/desktop/api/Tapi/nf-tapi-linegetnewcalls) и для указания выбора (области) запрашиваемых вызовов.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------|-----------------------------------------------------------------------------------|
| Версия TAPI<br/> | Требуется TAPI 2,0 или более поздней версии<br/>                                             |
| Заголовок<br/>       | <dl> <dt>TAPI. h</dt> </dl> |



 

 




