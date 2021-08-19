---
description: Возвращает или задает значение, представляющее компонент секунд значения DateTime.
ms.assetid: 194d4309-6abf-4c5f-99f8-60d2c835af6c
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. Seconds (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Seconds
- ISWbemDateTime.Seconds
- ISWbemDateTime.get_Seconds
- ISWbemDateTime.put_Seconds
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4d30095e5464736b3db984b71f94a216c29f4327227a5e5b99becfbcae5e1a58
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816193"
---
# <a name="swbemdatetimeseconds-property"></a>SWbemDateTime. Seconds, свойство

Свойство **Seconds** объекта [**SWbemDateTime**](swbemdatetime.md) Возвращает или задает значение, представляющее компонент секунд значения DateTime.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
SWbemDateTime.Seconds As Long
```



## <a name="property-value"></a>Значение свойства

## <a name="error-codes"></a>Коды ошибок

После получения или задания свойства **Seconds** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать приведенный ниже код ошибки.

<dl> <dt>

**вбемеррвалуеаутофранже** -2147749931 (0x8004102B)
</dt> <dd>

Значение не находится в диапазоне от 0 до 59.

</dd> </dl>

## <a name="remarks"></a>Remarks

Свойство **SWbemDateTime. Seconds** может содержать неверное значение, если свойство [**SWbemDateTime. minutes**](swbemdatetime-minutes.md) установлено в значение 1. Он содержит значение, которое смещается на одну секунду из-за ошибки округления, возникающей при преобразовании значения [**DateTime**](datetime.md) CIM в значение **\_ даты VT** . Если вместо значения свойства **minutes** задано значение 0 (ноль), то свойство **Seconds** будет возвращать правильную величину.

## <a name="examples"></a>Примеры

Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md). Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMDATETIME CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемдатетиме<br/>                                                          |



## <a name="see-also"></a>См. также

<dl> <dt>

[**SWbemDateTime. СекондсспеЦифиед**](swbemdatetime-secondsspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

