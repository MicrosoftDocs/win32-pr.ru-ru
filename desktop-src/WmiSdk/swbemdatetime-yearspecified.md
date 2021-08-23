---
description: Логическое значение, указывающее, содержит ли компонент year в значении DateTime CIM интервал или значение с подстановочным знаком.
ms.assetid: afac0a08-7bd0-42f1-b5a7-8664f9db8615
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. ЕарспеЦифиед (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.YearSpecified
- ISWbemDateTime.YearSpecified
- ISWbemDateTime.get_YearSpecified
- ISWbemDateTime.put_YearSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 2cb8a3733d6aaf5679c47d0cf61ca05b2154b57edfd64e5152c0da1f8c822dd5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118815966"
---
# <a name="swbemdatetimeyearspecified-property"></a>SWbemDateTime. ЕарспеЦифиед, свойство

Свойство **еарспеЦифиед** объекта [**SWbemDateTime**](swbemdatetime.md) является логическим значением, указывающим, содержит ли компонент year в значении DateTime CIM интервал или значение с подстановочным знаком. Если **еарспеЦифиед** имеет значение true [**, а параметр**](swbemdatetime-isinterval.md) **IsTrue** имеет значение **false**, то [**SWbemDateTime. Year**](swbemdatetime-year.md) содержит значение DateTime. Значение DateTime, содержащее интервал, не может быть преобразовано в формат **\_ даты VT** или **fileTime** . Если **еарспеЦифиед** имеет **значение false** **, а** параметр **IsTrue имеет значение true**, то **SWbemDateTime. Year** содержит интервал.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
SWbemDateTime.YearSpecified As Boolean
```



## <a name="property-value"></a>Значение свойства

## <a name="examples"></a>Примеры

Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md). Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Заголовок<br/>                   | <dl> <dt>Wbemdisp. h</dt> </dl>   |
| Библиотека типов<br/>             | <dl> <dt>Wbemdisp. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wbemdisp.dll</dt> </dl> |
| CLSID<br/>                    | \_SWBEMDATETIME CLSID<br/>                                                         |
| IID<br/>                      | IID \_ исвбемдатетиме<br/>                                                          |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**SWbemDateTime. год**](swbemdatetime-year.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[DATETIME](datetime.md)
</dt> </dl>

 

 




