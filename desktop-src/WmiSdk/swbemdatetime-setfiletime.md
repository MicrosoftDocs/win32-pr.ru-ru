---
description: Преобразует дату в строковом формате FILETIME в формат даты и времени CIM.
ms.assetid: e375afda-5e94-46d6-b1ac-e801e0f4a620
ms.tgt_platform: multiple
title: SWbemDateTime. Сетфилетиме, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
- ISWbemDateTime.SetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: ca3e36a284e3700e166e86f6786218bada8f369e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155839"
---
# <a name="swbemdatetimesetfiletime-method"></a>SWbemDateTime. Сетфилетиме, метод

Метод **сетфилетиме** объекта [**SWbemDateTime**](swbemdatetime.md) преобразует дату в строковом формате **fileTime** в формат [даты и времени CIM](date-and-time-format.md) .

Формат **fileTime** — это 64-разрядная структура DateTime, представляющая число единиц с 100 до 1 января 1601 г. Инструментарий управления Windows (WMI) (WMI) рассматривает значения **fileTime** как строковые представления беззнаковых 64-разрядных чисел.

Описание синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
SWbemDateTime.SetFileTime( _
  ByVal strFileTime, _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*стрфилетиме* \[ окне\]
</dt> <dd>

Значение **fileTime** , используемое для задания объекта.

</dd> <dt>

*бислокал* \[ в необязательное\]
</dt> <dd>

Если **значение равно true**, *стрфилетиме* интерпретируется как местное время. Свойство времени в формате UTC содержит местное время, преобразованное в правильное смещение в формате UTC. Если *бислокал* имеет **значение false**, то *стрфилетиме* преобразуется непосредственно в значение UTC со смещением 0 (нулем).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод не возвращает значение.

## <a name="error-codes"></a>Коды ошибок

После завершения метода **сетфилетиме** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать код ошибки из следующего списка.

<dl> <dt>

**вбемерринвалидсинтакс** -2147749921 (0x80041021)
</dt> <dd>

Недопустимый формат *стрфилетиме* .

</dd> </dl>

## <a name="remarks"></a>Комментарии

После успешного вызова **сетфилетиме** значение [**DateTime**](datetime.md) всегда интерпретируется как абсолютное значение (**DateTime**) [**, а**](swbemdatetime-isinterval.md) параметру IsFalse — значение **false**.

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

[**SWbemDateTime. Сетвардате**](swbemdatetime-setvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

