---
description: Указывает, содержит ли компонент минут в значении DateTime CIM интервал или значение с подстановочным знаком.
ms.assetid: de15f87e-0092-467e-b0d7-42ef447fa00a
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. МинутесспеЦифиед (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MinutesSpecified
- ISWbemDateTime.MinutesSpecified
- ISWbemDateTime.get_MinutesSpecified
- ISWbemDateTime.put_MinutesSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 62f64ad749ee020093008a308a3244e045f9995d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155842"
---
# <a name="swbemdatetimeminutesspecified-property"></a>SWbemDateTime. МинутесспеЦифиед, свойство

Свойство **минутесспеЦифиед** объекта [**SWbemDateTime**](swbemdatetime.md) является логическим значением, указывающим, содержит ли компонент минут в значении DateTime CIM интервал или значение с подстановочным знаком. Если **минутесспеЦифиед** имеет **значение true** [**, а параметр**](swbemdatetime-isinterval.md) ISDATE имеет значение **false** (что означает, что значение DateTime в CIM не содержит подстановочных знаков), то [**SWbemDateTime. minutes**](swbemdatetime-minutes.md) содержит значение даты. Значение DateTime, содержащее интервал, не может быть преобразовано в формат **\_ даты VT** или **fileTime** . Если [**хаурсспеЦифиед**](swbemdatetime-hoursspecified.md) имеет **значение false** **, а** параметр **IsTrue имеет значение true**, то **SWbemDateTime. minutes** содержит интервал.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
SWbemDateTime.MinutesSpecified As boolean
```



## <a name="property-value"></a>Значение свойства

## <a name="examples"></a>Примеры

Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md). Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Header<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMDATETIME CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемдатетиме<br/>                                                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SWbemDateTime. минут**](swbemdatetime-minutes.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[DATETIME](datetime.md)
</dt> </dl>

 

 




