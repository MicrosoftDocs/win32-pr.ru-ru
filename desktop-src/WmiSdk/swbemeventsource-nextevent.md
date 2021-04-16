---
description: Если событие доступно, метод Некстевент объекта Свбемевентсаурце извлекает событие из запроса события.
ms.assetid: ff2d54d4-b8ee-4bb8-b6f7-081a1ca20489
ms.tgt_platform: multiple
title: Свбемевентсаурце. Некстевент, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
- ISWbemEventSource.NextEvent
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 02fbc32557ab29c66849a4249d26cc2ca41564e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105703173"
---
# <a name="swbemeventsourcenextevent-method"></a>Свбемевентсаурце. Некстевент, метод

Если событие доступно, метод **некстевент** объекта [**свбемевентсаурце**](swbemeventsource.md) извлекает событие из запроса события.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
objWbemObject = .NextEvent( _
  [ ByVal iTimeoutMs ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*итимеаутмс* \[ в необязательное\]
</dt> <dd>

Число миллисекунд, в течение которых вызов ожидает события, прежде чем возвращать ошибку времени ожидания. Значение по умолчанию для этого параметра — **вбемтимеаутинфините** (-1), которое направляет вызов на неограниченное время ожидания.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Если метод **некстевент** успешно выполнен, он возвращает объект [**SWbemObject**](swbemobject.md) , содержащий запрошенное событие. Если время ожидания вызова истекло, возвращаемый объект имеет **значение NULL** и возникает ошибка.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **некстевент** объект **Err** может содержать код ошибки из следующего списка.

<dl> <dt>

**вбемерртимедаут** — 0x80043001
</dt> <dd>

Запрошенное событие не поступало в течение времени, указанного в *итимеаутмс.*

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_СВБЕМЕВЕНТСАУРЦЕ CLSID<br/>                                                      |
| IID<br/>                      | IID \_ исвбемевентсаурце<br/>                                                       |



 

 




