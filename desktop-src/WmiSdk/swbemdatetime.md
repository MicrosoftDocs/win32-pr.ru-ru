---
description: Объект SWbemDateTime — это вспомогательный объект для синтаксического анализа и установки значений DateTime модель CIM (CIM).
ms.assetid: 3dd34c73-3c2b-4d59-827b-169cf8020213
ms.tgt_platform: multiple
title: Объект SWbemDateTime (Wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemDateTime
- ISWbemDateTime
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 25f8b04aa8c581d8d7e40ab1d52162d305c97d0d8ce3f7d626cb3d29e7262666
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119050092"
---
# <a name="swbemdatetime-object"></a>Объект SWbemDateTime

Объект **SWbemDateTime** — это вспомогательный объект для синтаксического анализа и установки значений [DateTime](datetime.md) модель CIM (CIM). Он играет роль, аналогичную [**свбемобжектпас**](swbemobjectpath.md), которая обеспечивает поддержку форматирования и интерпретации путей к объектам. Для создания объекта **SWbemDateTime** можно использовать вызов функции [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) VBScript.

Объект **SWbemDateTime** можно инициализировать из и отформатировать в значениях **VT \_** или **fileTime** с помощью методов объекта. С помощью свойств объекта значение может быть проанализировано в год, месяц, день, час, минуты, секунды или микросекунды. Объект **SWbemDateTime** можно отформатировать как локальное значение, так и в формате UTC. Дополнительные сведения см. в разделе [Формат даты и времени](date-and-time-format.md).

**SWbemDateTime** — это единственный объект скрипта инструментарий управления Windows (WMI) (WMI), помеченный как надежный для инициализации и скриптов, выполняющихся на HTML-страницах в Internet Explorer.

## <a name="members"></a>Элементы

Объект **SWbemDateTime** имеет следующие типы членов:

-   [Методы](#methods)
-   [Свойства](#properties)

### <a name="methods"></a>Методы

Объект **SWbemDateTime** содержит эти методы.



| Метод                                           | Описание                                                                                                          |
|:-------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [**Функции getFileTime**](swbemdatetime-getfiletime.md) | Преобразует дату и время **fileTime** , выраженные в виде **BSTR**, в формат [DateTime](datetime.md) WMI.<br/> |
| [**GetVarDate**](swbemdatetime-getvardate.md)   | Преобразует значение даты и времени в формате WMI [DateTime](datetime.md) в **\_ дату VT**.<br/>                  |
| [**сетфилетиме**](swbemdatetime-setfiletime.md) | Преобразует формат [DateTime](datetime.md) WMI в значение даты и времени **fileTime** , выраженное в виде **BSTR**.<br/>  |
| [**сетвардате**](swbemdatetime-setvardate.md)   | Преобразует дату и время в формате **\_ VT** в [значение DateTime](datetime.md)WMI.<br/>                        |



 

### <a name="properties"></a>Свойства

Объект **SWbemDateTime** имеет следующие свойства.



| Свойство                                                                        | Тип доступа           | Описание                                                                                                                     |
|:--------------------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**День**](swbemdatetime-day.md)<br/>                                     | Чтение/запись<br/> | Компонент дня для значения [DateTime](datetime.md) CIM.<br/>                                                           |
| [**дайспеЦифиед**](swbemdatetime-dayspecified.md)<br/>                   | Чтение/запись<br/> | Указывает, указан ли день в качестве подстановочного знака.<br/>                                                        |
| [**Hours**](swbemdatetime-hours.md)<br/>                                 | Чтение/запись<br/> | Часы компонента дня в значении [даты и времени](datetime.md) CIM.<br/>                                              |
| [**хаурсспеЦифиед**](swbemdatetime-hoursspecified.md)<br/>               | Чтение/запись<br/> | Указывает, указан ли час или оставлен в качестве подстановочного знака.<br/>                                                       |
| [**Параметр "интервал"**](swbemdatetime-isinterval.md)<br/>                       | Чтение/запись<br/> | Указывает, что хотя бы один компонент [даты и времени](datetime.md) CIM представляет интервал, а не дату.<br/> |
| [**Микросекунды**](swbemdatetime-microseconds.md)<br/>                   | Чтение/запись<br/> | Компонент микросекунд для значения [DateTime](datetime.md) CIM.<br/>                                                  |
| [**микросекондсспеЦифиед**](swbemdatetime-microsecondsspecified.md)<br/> | Чтение/запись<br/> | Указывает, указан ли компонент микросекунд в качестве подстановочного знака.<br/>                                     |
| [**Минуты**](swbemdatetime-minutes.md)<br/>                             | Чтение/запись<br/> | Компонент минут для значения [DateTime](datetime.md) CIM.<br/>                                                       |
| [**минутесспеЦифиед**](swbemdatetime-minutesspecified.md)<br/>           | Чтение/запись<br/> | Указывает, указан ли компонент минут или оставлен в качестве подстановочного знака.<br/>                                          |
| [**Месяц**](swbemdatetime-month.md)<br/>                                 | Чтение/запись<br/> | Компонент месяца для значения [DateTime](datetime.md) CIM.<br/>                                                         |
| [**монсспеЦифиед**](swbemdatetime-monthspecified.md)<br/>               | Чтение/запись<br/> | Указывает, указан ли месяц или Left в качестве подстановочного знака.<br/>                                                      |
| [**Секунды**](swbemdatetime-seconds.md)<br/>                             | Чтение/запись<br/> | Компонент секунд для значения [DateTime](datetime.md) CIM.<br/>                                                       |
| [**секондсспеЦифиед**](swbemdatetime-secondsspecified.md)<br/>           | Чтение/запись<br/> | Указывает, указан ли компонент секунд или является его левым в качестве подстановочного знака.<br/>                                          |
| [**ФОРМАТА**](swbemdatetime-utc.md)<br/>                                     | Чтение/запись<br/> | Компонент времени в формате UTC значения [DateTime](datetime.md) CIM.<br/>                                                           |
| [**уткспеЦифиед**](swbemdatetime-utcspecified.md)<br/>                   | Чтение/запись<br/> | Указывает, указан ли компонент времени в формате UTC или является его левым в качестве подстановочного знака.<br/>                                              |
| [**Значение**](swbemdatetime-value.md)<br/>                                 | Чтение/запись<br/> | Полное значение [даты и времени](datetime.md) CIM.<br/>                                                                         |
| [**Год**](swbemdatetime-year.md)<br/>                                   | Чтение/запись<br/> | Компонент года для значения [DateTime](datetime.md) CIM.<br/>                                                          |
| [**еарспеЦифиед**](swbemdatetime-yearspecified.md)<br/>                 | Чтение/запись<br/> | Указывает, указан ли год или нет в качестве подстановочного знака.<br/>                                                |



 

## <a name="remarks"></a>Remarks

WMI записывает отметки времени в формате UTC. Время в формате UTC не используется большинство разработчиков и ИТ-администраторов. Поэтому распространенной проблемой является определение способа перевода времени в формате UTC в более удобочитаемый формат. Дополнительные сведения о работе со временем в формате UTC см. в разделе [задачи WMI: даты и времени](wmi-tasks--dates-and-times.md) и [Работа с датами и временем с помощью WMI](/previous-versions/tn-archive/ee198928(v=technet.10)). Кроме того, можно прочитать [сведения о времени (и о датах)](/previous-versions/technet-magazine/cc160973(v=msdn.10)) , а также о том, [как вычесть указанное число дней из значения времени в формате UTC?](https://blogs.technet.com/b/heyscriptingguy/archive/2006/07/21/how-can-i-subtract-a-specified-number-of-days-from-a-utc-value.aspx) записи блога для получения дополнительных сведений.

Любое числовое поле может иметь подстановочное значение, [**Если свойство ISNUMERIC**](swbemdatetime-isinterval.md) имеет значение **false**. Поля с подстановочными значениями содержат звездочки во всем поле.

Каждое свойство, например [**Day**](swbemdatetime-day.md), имеет соответствующее заданное логическое значение, например [**дайспеЦифиед**](swbemdatetime-dayspecified.md). Если **дайспеЦифиед** имеет значение **false**, то значение интерпретируется как интервал, а не число от 01 до 31. Если интервал используется в любом месте в значении [даты и времени](datetime.md) CIM [**, то параметру IsTrue также присваивается**](swbemdatetime-isinterval.md) **значение true**. По умолчанию значение DateTime в CIM должно содержать дату, а не один или несколько интервалов.

Например, если [**SWbemDateTime. дайспеЦифиед**](swbemdatetime-dayspecified.md) имеет **значение true**, то [**SWbemDateTime. Value**](swbemdatetime-value.md) включает текущее значение [**SWbemDateTime. Day**](swbemdatetime-day.md), в противном случае это значение с подстановочным знаком. В [**любом случае свойство**](swbemdatetime-isinterval.md) **IsFalse имеет значение false** .

## <a name="examples"></a>Примеры

В следующем примере кода скрипта показано, как использовать объект **SWbemDateTime** для анализа значения свойства DateTime, считанного из репозитория WMI, свойства **инсталлдате** в [**Win32 \_**](/windows/desktop/CIMWin32Prov/win32-operatingsystem).


```VB
' Create a new datetime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")

' Retrieve a WMI object that contains a datetime value.
for each os in GetObject( _
    "winmgmts:").InstancesOf ("Win32_OperatingSystem")

    ' The InstallDate property is a CIM_DATETIME. 
    MsgBox os.InstallDate
    dateTime.Value = os.InstallDate

    ' Display the year of installation.
    MsgBox "This OS was installed in the year " & dateTime.Year

    ' Display the installation date using the VT_DATE format.
    MsgBox "Full installation date (VT_DATE format) is " _
    & dateTime.GetVarDate

    ' Display the installation date using the FILETIME format.
    MsgBox "Full installation date (FILETIME format) is " _
    & dateTime.GetFileTime 
next
Set datetime = Nothing
```



В следующем примере показано, как создать объект **SWbemDateTime** , сохранить значение даты в объекте, отобразить дату в виде местного времени (UTC) и сохранить значение во вновь созданном классе и свойстве. Дополнительные сведения о константной **вбемЦимтипедатетиме** см. в разделе [вбемЦимтипинум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum).


```VB
' Create an SWbemDateTime object.
Set dateTime = CreateObject("WbemScripting.SWbemDateTime")
' Set the value 
Const wbemCimTypeDatetime = 101

' Construct a datetime value using the intrinsic VBScript CDate
' function interpreting this as a local date/time in
' the Pacific time zone (-8 hrs GMT). Convert to CIM datetime
' using SetVarDate method. The year defaults to current year.
dateTime.SetVarDate (CDate ("January 20 11:56:32"))

' The value in dateTime displays as 
' 20000120195632.000000-480. This is the equivalent time
' in GMT with the specified offset for PST of -8 hrs.
MsgBox "CIM datetime " & dateTime

' The value now displays as B=0/2000 11:56:32 AM because the
' parameter contains the default TRUE value causing the value to be
' interpreted as a local time.
MsgBox "Local datetime " & dateTime.GetVarDate ()

' The value now displays as B=0/2000 7:56:32 PM because the
' parameter value is FALSE, which indicates a GMT time.
' non-local time.
MsgBox "Datetime in GMT " & dateTime.GetVarDate (false)

' Create a new class and add a DateTime property value.
' SWbemServices.Get returns an empty SWbemObject
' which can become a new class. SWbemObject.Path_ returns an
' SWbemObjectPath object. 
set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "NewClass"

' Add a new property named "InterestingDate" to the NewObject class
' and define its datatype as a CIM datetime value.
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value of the SWbemDateTime object in the InterestingDate
' property.
NewObject.InterestingDate = dateTime.Value
MsgBox "Datetime in new object " & NewObject.InterestingDate

' Write the new class (named "NewClass") containing
' the SWbemDateTime object to the repository.
NewObject.Put_
WScript.Echo "NewClass is now in WMI repository"

' Clean up the example by deleting the new class from the repository
NewObject.Delete_
```



В следующем примере кода скрипта показано, как использовать объект **SWbemDateTime** для изменения значения интервала в свойстве, которое считывается из репозитория WMI.


```VB
' Construct an interval value of 100 days, 1 hour, and 3 seconds.
dateTime.IsInterval = true 
dateTime.Day = 100
dateTime.Hours = 1
dateTime.Seconds = 3

' The datetime displays as 00000100010003.000000:000.
MsgBox "Constructed interval value " & datetime

' Retrieve an empty WMI object and add a datetime property. 
Const wbemCimTypeDatetime = 101
Set NewObject = GetObject("winmgmts:root\default").Get
NewObject.Path_.Class = "Empty"
NewObject.Properties_.Add "InterestingDate", wbemCimtypeDatetime

' Set the new value in the property and update. 
NewObject.InterestingDate = dateTime.Value
MsgBox "NewObject.InterestingDate = " & NewObject.InterestingDate

' Write the new SWbemDateTime object to the repository.
NewObject.Put_

' Delete the object.
NewObject.Delete_
```



В следующем примере кода скрипта показано, как использовать объект **свбемдате** для считывания значения **fileTime** .


```VB
' Create a new datetime object.
Set datetime = CreateObject("WbemScripting.SWbemDateTime")

' Set from a FILETIME value (non-local).
' Assume a timezone -7 hrs. GMT.
MsgBox "FILETIME value " & "126036951652030000"
datetime.SetFileTime "126036951652030000", false

' Displays as 5/24/2000 7:26:05 PM.
MsgBox "GMT time " & dateTime.GetVarDate   

' Set from a FILETIME value (local).
datetime.SetFileTime "126036951652030000"

' Displays as 5/25/2000 2:26:05 AM.
MsgBox "Same value in local time " & dateTime.GetVarDate
Set datetime = Nothing
```



Следующий код PowerShell создает экземпляр объекта SWbemDateTime, получает дату установки ОС и преобразует дату в другой формат.


```PowerShell
# Create swbemdatetime object
$datetime = New-Object -ComObject WbemScripting.SWbemDateTime

#  Get OS installation time and assign to datetime object
$os = Get-WmiObject -Class Win32_OperatingSystem
$dateTime.Value = $os.InstallDate

# Now display the time
"This OS was installed in the year {0}"           -f $dateTime.Year
"Full installation date (VT_DATE format) is {0}"  -f $dateTime.GetVarDate()
"Full installation date (FILETIME format) is {0}" -f $dateTime.GetFileTime() 
```



Следующий код PowerShell преобразует код в формат, готовый для использования поставщиком CIM.


```PowerShell
 $time = (Get-Date)
 $objScriptTime = New-Object -ComObject WbemScripting.SWbemDateTime
 $objScriptTime.SetVarDate($time)
 $cimTime = $objScriptTime.Value
```



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

[вбемЦимтипинум](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemcimtypeenum)
</dt> <dt>

[DATETIME](datetime.md)
</dt> <dt>

[Создание скриптов для объектов API](scripting-api-objects.md)
</dt> </dl>

 

