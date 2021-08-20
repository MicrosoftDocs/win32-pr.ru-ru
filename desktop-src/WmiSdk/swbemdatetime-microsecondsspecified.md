---
description: Логическое значение, указывающее, содержит ли компонент микросекунды в значении DateTime CIM интервал или значение с подстановочным знаком.
ms.assetid: 65244ece-2326-4edc-b982-57e2046ec33e
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. МикросекондсспеЦифиед (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.MicrosecondsSpecified
- ISWbemDateTime.get_MicrosecondsSpecified
- ISWbemDateTime.put_MicrosecondsSpecified
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1b516b5fbe98c8bf481eaeed5b01c11f2dde6697a5832afc9d505d49254db2a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118816382"
---
# <a name="swbemdatetimemicrosecondsspecified-property"></a>SWbemDateTime. МикросекондсспеЦифиед, свойство

Свойство **микросекондсспеЦифиед** объекта [**SWbemDateTime**](swbemdatetime.md) является логическим значением, указывающим, содержит ли компонент микросекунды в значении типа данных CIM интервал или значение с подстановочным знаком. Если **микросекондсспеЦифиед** имеет значение true [**, а параметр**](swbemdatetime-isinterval.md) **IsTrue** имеет значение **false**, то [**SWbemDateTime. в микросекундах**](swbemdatetime-microseconds.md) содержит значение DateTime. Значение DateTime, содержащее интервал, не может быть преобразовано в формат **\_ даты VT** или **fileTime** . Если [**хаурсспеЦифиед**](swbemdatetime-hoursspecified.md) имеет **значение false** **, а** параметр **IsTrue имеет значение true**, то **SWbemDateTime. МКС** содержит интервал.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
SWbemDateTime.MicrosecondsSpecified As Boolean
```



## <a name="property-value"></a>Значение свойства

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

[**SWbemDateTime. микросекунды**](swbemdatetime-microseconds.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[DATETIME](datetime.md)
</dt> </dl>

 

 




