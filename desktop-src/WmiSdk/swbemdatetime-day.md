---
description: Возвращает или задает значение, представляющее компонент дня значения DateTime.
ms.assetid: 60da99bc-560c-45bc-b787-f4bef8e5a509
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. Day (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Day
- ISWbemDateTime.Day
- ISWbemDateTime.get_Day
- ISWbemDateTime.put_Day
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 1de77a8e5d616284c3dc13a19bce2526db371c20
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999371"
---
# <a name="swbemdatetimeday-property"></a>SWbemDateTime. Day, свойство

Свойство **Day** объекта [**SWbemDateTime**](swbemdatetime.md) Возвращает или задает значение, представляющее компонент дня значения DateTime. Значение должно находиться в диапазоне от 1 до 31 [**, если**](swbemdatetime-isinterval.md) параметру IsFalse задано **значение false**. Однако проверка ошибок не зависит от значения месяца. Таким словами, значение 31 в диапазоне не будет возвращать ошибку в случаях, когда значение [**SWbemDateTime. month**](swbemdatetime-month.md) составляет месяц менее 31 дня (Февраль, Апрель, Июнь, Сентябрь ноября).

Значение **дня** по умолчанию — 01.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
SWbemDateTime.Day As Long
```



## <a name="property-value"></a>Значение свойства

## <a name="error-codes"></a>Коды ошибок

После получения или задания свойства **Day** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать приведенный ниже код ошибки.

<dl> <dt>

**вбемеррвалуеаутофранже** -2147749931 (0x8004102B)
</dt> <dd>

Если [**параметр**](swbemdatetime-isinterval.md) IsTrue имеет **значение true** , а диапазон правильных значений превышает 0 – 99999999.

</dd> </dl>

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

[**SWbemDateTime. ДайспеЦифиед**](swbemdatetime-dayspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[DATETIME](datetime.md)
</dt> </dl>

 

