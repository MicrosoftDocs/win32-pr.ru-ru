---
description: Логическое значение, указывающее, содержит ли компонент дня в значении DATETIME CIM интервал или значение с подстановочным знаком.
ms.assetid: a713378b-3953-49d8-9c6a-44aa9337eae2
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. ДайспеЦифиед (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.DaySpecified
- ISWbemDateTime.DaySpecified
- ISWbemDateTime.get_DaySpecified
- ISWbemDateTime.put_DaySpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: effa3bcb68351aa754006c143e738443efdb7238129f30847876ad17527ca279
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118992254"
---
# <a name="swbemdatetimedayspecified-property"></a>SWbemDateTime. ДайспеЦифиед, свойство

Свойство **дайспеЦифиед** объекта [**SWbemDateTime**](swbemdatetime.md) является логическим значением, указывающим, содержит ли компонент дня в значении [**DateTime**](datetime.md) CIM интервал или значение с подстановочным знаком. Если **дайспеЦифиед** имеет значение true [**, а параметр**](swbemdatetime-isinterval.md) **IsTrue** имеет значение **false**, то [**SWbemDateTime. Day**](swbemdatetime-day.md) содержит значение DateTime. Значение [**DateTime**](datetime.md) , содержащее интервал, не может быть преобразовано в формат **\_ даты VT** или **fileTime** . Если **дайспеЦифиед** имеет **значение false** **, а** параметр **IsTrue имеет значение true**, то **SWbemDateTime. Day** содержит интервал.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
SWbemDateTime.DaySpecified As BOOLEAN
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

[**SWbemDateTime. Day**](swbemdatetime-day.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

 




