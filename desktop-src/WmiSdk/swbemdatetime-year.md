---
description: Возвращает или задает значение, представляющее компонент года значения DATETIME.
ms.assetid: eab3738a-c92a-4602-b1ee-e2547da88308
ms.tgt_platform: multiple
title: Свойство SWbemDateTime. Year (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.Year
- ISWbemDateTime.Year
- ISWbemDateTime.get_Year
- ISWbemDateTime.put_Year
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 5fe8988b3772f0f5d976c38eb5e9cc44fb9c4ede
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702746"
---
# <a name="swbemdatetimeyear-property"></a>SWbemDateTime. year, свойство

Свойство **year** объекта [**SWbemDateTime**](swbemdatetime.md) Возвращает или задает значение, представляющее компонент года для значения [**DateTime**](datetime.md) . Значение должно быть в диапазоне от 0000-9999 или возвращена ошибка Вбемеррвалуеаутофранже.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

Это свойство доступно для чтения и записи.

## <a name="syntax"></a>Синтаксис


```VB
SWbemDateTime.Year As Long
```



## <a name="property-value"></a>Значение свойства

## <a name="error-codes"></a>Коды ошибок

После получения или задания свойства **year** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать приведенный ниже код ошибки.

<dl> <dt>

**вбемеррвалуеаутофранже** -2147749931 (0x8004102B)
</dt> <dd>

Значение не находится в диапазоне от 0000 до 9999.

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

[**SWbemDateTime. ЕарспеЦифиед**](swbemdatetime-yearspecified.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

