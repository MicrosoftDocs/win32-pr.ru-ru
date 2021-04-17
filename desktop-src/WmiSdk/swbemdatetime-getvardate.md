---
description: Преобразует значение даты и времени в формате DATETIME CIM в \_ Формат даты VT.
ms.assetid: e63e7acc-89d4-458a-a1ab-4d4a65cf7f8b
ms.tgt_platform: multiple
title: SWbemDateTime. GetVarDate, метод (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
- ISWbemDateTime.GetVarDate
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: b4d0c71e4748774eacab4b234092178179a4a774
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105711652"
---
# <a name="swbemdatetimegetvardate-method"></a>SWbemDateTime. GetVarDate, метод

Метод **GetVarDate** объекта [**SWbemDateTime**](swbemdatetime.md) преобразует значение даты и времени в формате [**DateTime**](datetime.md) CIM в формат **\_ даты VT** .

Формат **\_ даты VT** — это значение даты и [**времени**](datetime.md) автоматизации типа Variant, которое Visual Basic и использование ActiveX.

Описание этого синтаксиса см. в разделе [соглашения о документе для API скриптов](document-conventions-for-the-scripting-api.md).

## <a name="syntax"></a>Синтаксис


```VB
vdate = .GetVarDate( _
  [ ByVal bIsLocal ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*бислокал* \[ в необязательное\]
</dt> <dd>

Указывает, интерпретируется ли возвращаемое значение как местное время. Свойство времени в формате UTC содержит местное время, преобразованное в правильное смещение в формате UTC. Если значение равно **false**, то значение интерпретируется как время в формате UTC с нулевым смещением (0).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Значение даты и времени в формате **\_ даты VT** .

## <a name="remarks"></a>Комментарии

**VT \_ Значения DATE** и **fileTime** не могут содержать подстановочные поля.

Метод **GetVarDate** завершается ошибкой (**вбемеррфаилед**), если любое из следующих свойств имеет **значение false**:

-   [**еарспеЦифиед**](swbemdatetime-yearspecified.md)
-   [**монсспеЦифиед**](swbemdatetime-monthspecified.md)
-   [**дайспеЦифиед**](swbemdatetime-dayspecified.md)
-   [**хаурсспеЦифиед**](swbemdatetime-hoursspecified.md)
-   [**минутесспеЦифиед**](swbemdatetime-minutesspecified.md)
-   [**секондсспеЦифиед**](swbemdatetime-secondsspecified.md)
-   [**микросекондсспеЦифиед**](swbemdatetime-microsecondsspecified.md)
-   [**уткспеЦифиед**](swbemdatetime-utcspecified.md)

При успешном возврате из [**сетвардате**](swbemdatetime-setvardate.md)всем этим свойствам присваивается **значение true**.

После успешного вызова [**сетвардате**](swbemdatetime-setvardate.md)значение [**DateTime**](datetime.md) всегда интерпретируется как абсолютное значение **DateTime** вместо интервала, а для параметра IsFalse [**устанавливается значение**](swbemdatetime-isinterval.md) **false**.

Если параметру IsTrue [**присвоено**](swbemdatetime-isinterval.md) значение **true**, вызов **GetVarDate** приводит к ошибке **вбемеррфаилед** .

При вызове **GetVarDate** происходит некоторое снижение точности, поскольку значения [DateTime](datetime.md) имеют одно разрешение в микросекундах, а значения **\_ даты VT** имеют разрешение 500 миллисекунд.

## <a name="examples"></a>Примеры

Примеры использования объекта [**SWbemDateTime**](swbemdatetime.md) для преобразования значений [**DateTime**](datetime.md) CIM в и из параметра **fileTime** или формата **\_ даты VT** см. в разделе [задачи WMI: даты и время](wmi-tasks--dates-and-times.md). Описание формата **DateTime** в CIM см. в разделе [Формат даты и времени](date-and-time-format.md).

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

[**SWbemDateTime. функции getFileTime**](swbemdatetime-getfiletime.md)
</dt> <dt>

[**SWbemDateTime**](swbemdatetime.md)
</dt> <dt>

[DATETIME](datetime.md)
</dt> </dl>

 

 




