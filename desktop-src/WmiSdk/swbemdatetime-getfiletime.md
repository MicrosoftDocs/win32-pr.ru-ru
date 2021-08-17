---
description: Преобразует значение даты и времени в формате DATETIME CIM в формат FILETIME.
ms.assetid: 08e0761d-e735-454a-8429-2bd1eb331123
ms.tgt_platform: multiple
title: SWbemDateTime. функции getFileTime, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
- ISWbemDateTime.GetFileTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 8c35daf5b6e986b2519f127969edc5bbcf05a260bd23e8aa1168b1a7c20a5372
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117739442"
---
# <a name="swbemdatetimegetfiletime-method"></a>SWbemDateTime. функции getFileTime, метод

Метод **функции getFileTime** объекта [**SWbemDateTime**](swbemdatetime.md) преобразует значение даты и времени в формате [DateTime](datetime.md) CIM в формат FILETIME.

Если для параметра задано значение **true**, то возвращаемое значение представляет местное время клиента. В противном случае возвращаемое значение — это время в формате UTC. Структура  [даты и времени](datetime.md) FILETIME — это 64-разрядное значение, представляющее число единиц в 100-наносекундных с начала 1 января 1601 г. Windows Инструментарий управления (WMI) рассматривает значения **fileTime** как строковые представления беззнаковых 64-разрядных чисел.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
vDate = .GetFileTime( _
  [ ByVal bIsLocaL ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бислокал* \[ в необязательное\]
</dt> <dd>

Указывает, интерпретируется ли возвращаемое значение как местное время. Свойство UTC содержит местное время, преобразованное в правильное смещение в формате UTC. Если значение равно **false**, то значение интерпретируется как время в формате UTC с нулевым смещением (0).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Дата и время в формате **fileTime** .

## <a name="error-codes"></a>Коды ошибок

После завершения метода **функции getFileTime** объект [Err](/previous-versions//sbf5ze0e(v=vs.85)) может содержать код ошибки из следующего списка.

<dl> <dt>

**вбемеррфаилед** -2147749889 (0x80041001)
</dt> <dd>

Вызов не выполнен.

</dd> </dl>

## <a name="remarks"></a>Remarks

**VT \_ Значения DATE** и **fileTime** не могут содержать подстановочные поля.

Метод **функции getFileTime** завершается ошибкой (вбемеррфаилед), если любое из следующих свойств имеет **значение false**:

-   [**еарспеЦифиед**](swbemdatetime-yearspecified.md)
-   [**монсспеЦифиед**](swbemdatetime-monthspecified.md)
-   [**дайспеЦифиед**](swbemdatetime-dayspecified.md)
-   [**хаурсспеЦифиед**](swbemdatetime-hoursspecified.md)
-   [**минутесспеЦифиед**](swbemdatetime-minutesspecified.md)
-   [**секондсспеЦифиед**](swbemdatetime-secondsspecified.md)
-   [**микросекондсспеЦифиед**](swbemdatetime-microsecondsspecified.md)
-   [**уткспеЦифиед**](swbemdatetime-utcspecified.md)

При успешном возврате из [**сетфилетиме**](swbemdatetime-setfiletime.md)всем этим свойствам присваивается **значение true**.

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

[**SWbemDateTime. GetVarDate**](swbemdatetime-getvardate.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[**DATETIME**](datetime.md)
</dt> </dl>

 

