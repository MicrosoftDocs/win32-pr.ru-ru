---
description: Возвращает или задает представление значения даты и времени в формате UTC.
ms.assetid: 43d9d0c8-5521-410f-825b-6b00c3dd0039
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. UTC (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.UTC
- ISWbemDateTime.UTC
- ISWbemDateTime.get_UTC
- ISWbemDateTime.put_UTC
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 4c1bb3307116042a61aae06489bec7d8eabbf7859f3e8770811b50680dcfe5cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118314697"
---
# <a name="swbemdatetimeutc-property"></a>SWbemDateTime. UTC, свойство

Свойство **UTC** объекта [**SWbemDateTime**](swbemdatetime.md) Возвращает или задает представление значения **DateTime** в формате UTC. UTC — это время, заданное стандартом мирового времени. Время в формате UTC заменяется средним временем по Гринвичу (GMT). Значение UTC с нулевым смещением равно значению GMT с нулевым смещением. Число со знаком должно быть в диапазоне от-720 до 720 или возвращена ошибка **вбемеррвалуеаутофранже** .

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
SWbemDateTime.UTC As Long
```



## <a name="property-value"></a>Значение свойства

## <a name="error-codes"></a>Коды ошибок

После получения или задания свойства **UTC** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать приведенный ниже код ошибки.

<dl> <dt>

**вбемеррвалуеаутофранже** -2147749931 (0x8004102B)
</dt> <dd>

Значение не находится в диапазоне от-720 до 720.

</dd> </dl>

## <a name="examples"></a>Примеры

Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md). Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).

## <a name="requirements"></a>Requirements (Требования)



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

[**SWbemDateTime. УткспеЦифиед**](swbemdatetime-utcspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

