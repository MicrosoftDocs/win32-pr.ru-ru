---
description: Преобразует дату в формате VT в \_ Формат даты и времени CIM.
ms.assetid: 24c39d44-22ac-44ac-9e05-72a5b666ab19
ms.tgt_platform: multiple
title: SWbemDateTime. Сетвардате, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetVarDate
- ISWbemDateTime.SetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 56d193bd2faffd51507ec4a913c7ee068b055dcf45ca756e801431659768c47d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050102"
---
# <a name="swbemdatetimesetvardate-method"></a>SWbemDateTime. Сетвардате, метод

Метод **сетвардате** объекта [**SWbemDateTime**](swbemdatetime.md) преобразует дату в формате VT в формат **\_ даты** [и времени CIM](date-and-time-format.md) .

значение **\_ даты VT** — это значение типа datetime, которое Visual Basic и ActiveX использования.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemDateTime.SetVarDate( _
  ByVal vdate, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*вдате* \[ окне\]
</dt> <dd>

Значение варианта даты для задания объекта. Этот параметр должен быть в формате **\_ даты VT** .

</dd> <dt>

*бислокал* \[ в необязательное\]
</dt> <dd>

Если **значение равно true**, *вдате* интерпретируется как местное время, а свойство координированного скоординированного времени (UTC) содержит местное время, которое преобразуется в правильное смещение в формате UTC. Если *бислокал* имеет **значение false**, то *вдате* преобразуется непосредственно в значение времени в формате UTC с нулевым смещением (0).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **сетвардате** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать код ошибки из следующего списка.

<dl> <dt>

**вбемерринвалидсинтакс** -2147749921 (0x80041021)
</dt> <dd>

Недопустимый формат *вдате* .

</dd> </dl>

## <a name="remarks"></a>Remarks

После успешного вызова **сетвардате** значение [**DateTime**](datetime.md) интерпретируется как абсолютное значение DateTime, а не как интервал, а свойство " [**интервал**](swbemdatetime-isinterval.md) " — в значение **false**.

встроенная функция [CDate](/previous-versions//2dt118h2(v=vs.85)) Visual Basic или VBScript предоставляет значение [**datetime**](datetime.md) в формате **\_ даты VT** для входных данных в **сетвардате**.

## <a name="examples"></a>Примеры

Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в формат **fileTime** или в формат **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md). Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).

Пример кода VBScript [Date to WMI Date-Time Format](https://Gallery.TechNet.Microsoft.Com/33beff76-1b5f-4ba1-a8ea-5e124eb74306) в коллекции TechNet использует сетвардате для преобразования регулярного значения даты и времени в формат даты и времени в формате UTC.

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

[**SWbemDateTime. Сетфилетиме**](swbemdatetime-setfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

