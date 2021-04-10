---
description: В инструментарии WMI можно определять статистические данные производительности на основе данных в отформатированных классах производительности, производных от Win32 \_ перфформаттеддата. Доступной статистикой являются средние, минимальные, максимальные значения, диапазон и дисперсия, как определено в типах статистических счетчиков.
ms.assetid: 5552d5fc-df8c-4353-8593-c106ee19dc84
ms.tgt_platform: multiple
title: Получение статистических данных о производительности
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 65892608e642b675440d81127ef9afa0badd1d36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104143390"
---
# <a name="obtaining-statistical-performance-data"></a>Получение статистических данных о производительности

В инструментарии WMI можно определять статистические данные производительности на основе данных в отформатированных классах производительности, производных от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata). Доступной статистикой являются средние, минимальные, максимальные значения, диапазон и дисперсия, как определено в [типах статистических счетчиков](statistical-counter-types.md).

Следующий список включает специальные типы статистических счетчиков:

-   [Среднее время от острова \_](cooker-average.md)
-   [мин. \_](cooker-min.md)
-   [максимум острова Кука \_](cooker-max.md)
-   [диапазон острова Кука \_](cooker-range.md)
-   [\_отклонение от острова](cooker-variance.md)

В следующих примерах показано, как:

-   Создайте MOF-файл, определяющий класс вычисляемых данных.
-   Напишите скрипт, создающий экземпляр класса, и периодически обновляет данные в экземпляре с помощью пересчитанных статистических значений.

## <a name="mof-file"></a>MOF-файл

В следующем примере кода MOF создается новый класс вычисляемых данных с именем **Win32 \_ перфформаттеддата \_ аваилаблембитес**. Этот класс содержит данные из свойства **аваилаблембитес** необработанного класса [**Win32 \_ перфравдата \_ перфос \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data). Класс **Win32 \_ перфформаттеддата \_ Аваилаблебитес** определяет свойства **СРЗНАЧ**, **min**, **Max**, **Range** и **вариативность**.

MOF-файл использует [**Квалификаторы свойств для форматированных классов счетчиков производительности**](property-qualifiers-for-performance-counter-classes.md) , чтобы определить источник данных свойства и формулу вычисления.

-   Свойство **Average** получает необработанные данные из [**памяти Win32 \_ перфравдата \_ перфос \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**Свойство Аваилаблембитес** .
-   **Квалификатор** счетчика для свойства **Average** указывает источник необработанных данных.
-   Квалификатор **кукингтипе** задает [ \_ минимальное](cooker-min.md) значение для вычисления данных в формуле.
-   Квалификатор **самплевиндов** указывает, сколько выборок следует предпринять перед выполнением вычисления.


```mof
// Store the new Win32_PerfFormattedData_MemoryStatistics
//     class in the Root\Cimv2 namespace
#pragma autorecover
#pragma namespace("\\\\.\\Root\\CimV2")

qualifier vendor:ToInstance;
qualifier guid:ToInstance;
qualifier displayname:ToInstance;
qualifier perfindex:ToInstance;
qualifier helpindex:ToInstance;
qualifier perfdetail:ToInstance;
qualifier countertype:ToInstance;
qualifier perfdefault:ToInstance;
qualifier defaultscale:ToInstance;

qualifier dynamic:ToInstance;
qualifier hiperf:ToInstance;
qualifier AutoCook:ToInstance;
qualifier AutoCook_RawClass:ToInstance;
qualifier CookingType:ToInstance;
qualifier Counter:ToInstance;


// Define the Win32_PerFormattedData_MemoryStatistics
//     class, derived from Win32_PerfFormattedData
[
  dynamic,
  // Name of formatted data provider: "WMIPerfInst" for Vista 
  //   and later
  provider("HiPerfCooker_v1"), 
  // Text that will identify new counter in Perfmon
  displayname("My Calculated Counter"),                            
  // A high performance class     
  Hiperf,
  // Contains calculated data 
  Cooked, 
  // Value must be 1 
  AutoCook(1), 
  // Raw performance class to get data for calculations
  AutoCook_RawClass("Win32_PerfRawData_PerfOS_Memory"),
  // Value must be 1        
  AutoCook_RawDefault(1),
  // Name of raw class property to use for timestamp in formulas 
  PerfSysTimeStamp("Timestamp_PerfTime"), 
  // Name of raw class property to use for frequency in formulas
  PerfSysTimeFreq("Frequency_PerfTime"), 
  // Name of raw class property to use for timestamp in formulas
  Perf100NSTimeStamp("Timestamp_Sys100NS"),
  // Name of raw class property to use for frequency in formulas
  Perf100NSTimeFreq("Frequency_Sys100NS"),
  // Name of raw class property to use for timestamp in formulas
  PerfObjTimeStamp("Timestamp_Object"),
  // Name of raw class property to use for frequency in formulas 
  PerfObjTimeFreq("Frequency_Object"),
  // Only one instance of class allowed in namespace
  singleton                                                   
]

class Win32_PerfFormattedData_MemoryStatistics
          : Win32_PerfFormattedData
{

// Define the properties for the class. 
// All the properties perform different
//     statistical operations on the same
//     property, AvailableMBytes, in the raw class

// Define the Average property,
//     which uses the "COOKER_AVERAGE" counter type and 
//     gets its data from the AvailableMBytes 
//     property in the raw class

    [
     CookingType("COOKER_AVERAGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Average = 0;

// Define the Min property, which uses
//     the "COOKER_MIN" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_MIN"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Min = 0;

// Define the Max property, which uses
//     the "COOKER_MAX" counter type and 
//     gets its data from the
//     AvailableMBytes property in the raw class

    [
     CookingType("COOKER_MAX"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Max = 0;

// Define the Range property, which uses
//     the "COOKER_RANGE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_RANGE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Range = 0;

// Define the Variance property, which uses
//     the "COOKER_VARIANCE" counter type and 
//     gets its data from the AvailableMBytes
//     property in the raw class

    [
     CookingType("COOKER_VARIANCE"),
     Counter("AvailableMBytes"),
     SampleWindow(10)
    ]
    uint64 Variance = 0;
};
```



## <a name="script"></a>Скрипт

Следующий пример кода скрипта получает статистику о доступной памяти в мегабайтах с помощью созданного ранее MOF. Скрипт использует объект скрипта [**свбемрефрешер**](swbemrefresher.md) для создания обновления, содержащего один экземпляр класса Statistics, создаваемого MOF-файлом, то есть **Win32 \_ перфформаттеддата \_ MemoryStatistics**. Дополнительные сведения об использовании скриптов см. [в разделе Обновление данных WMI в скриптах](refreshing-wmi-data-in-scripts.md). При работе в C++ см. раздел [доступ к данным производительности в c++](accessing-performance-data-in-c--.md).

> [!Note]  
> [**Свбемрефрешаблеитем. Object**](swbemrefreshableitem-object.md) должен вызываться после получения элемента из вызова [**свбемрефрешер. Add**](swbemrefresher-add.md) или скрипт завершится ошибкой. [**Свбемрефрешер. Refresh**](swbemrefresher-refresh.md) должен вызываться перед входом в цикл для получения базовых значений, или статистические свойства равны нулю (0) при первом прохождении.

 


```VB
' Connect to the Root\Cimv2 namespace
strComputer = "."
Set objService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate}!\\" _
    & strComputer & "\root\cimv2")

' Create a refresher
Set Refresher = CreateObject("WbemScripting.SWbemRefresher")
If Err <> 0 Then
WScript.Echo Err
WScript.Quit
End If

' Add the single instance of the statistics
'    class to the refresher
Set obMemoryStatistics = Refresher.Add(objService, _
    "Win32_PerfFormattedData_MemoryStatistics=@").Object

' Refresh once to obtain base values for cooking calculations
Refresher.Refresh

Const REFRESH_INTERVAL = 10

' Refresh every REFRESH_INTERVAL seconds 
For I=1 to 3
  WScript.Sleep REFRESH_INTERVAL * 1000
  Refresher.Refresh

  WScript.Echo "System memory statistics" _
      & "(Available Megabytes) " _
      & "for the past 100 seconds - pass " & i 
  WScript.Echo "Average = " _
     & obMemoryStatistics.Average & VBNewLine & "Max = " _
     & obMemoryStatistics.Max & VBNewLine & "Min = " _
     & obMemoryStatistics.Min & VBNewLine & "Range = " _ 
     & obMemoryStatistics.Range & VBNewLine & "Variance = " _
     & obMemoryStatistics.Variance 
Next
```



## <a name="running-the-script"></a>Выполнение скрипта

В следующей процедуре описывается, как выполнить пример.

**Выполнение примера скрипта**

1.  Скопируйте код MOF и сценарий в файлы на компьютере.
2.  Присвойте MOF-файлу расширение. mof и описание файла скрипта a. vbs.
3.  В командной строке перейдите в каталог, где хранятся файлы, и запустите [**mofcomp**](mofcomp.md) в MOF-файле. Например, если вы назначите имя файла *калкулатеддата. mof*, то команда будет иметь название **mofcomp** *калкулатеддата. mof*
4.  Выполните скрипт.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Мониторинг данных производительности](monitoring-performance-data.md)
</dt> <dt>

[Доступ к предустановленным классам производительности WMI](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[**Квалификаторы свойств для отформатированных классов счетчиков производительности**](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[Типы статистических счетчиков](statistical-counter-types.md)
</dt> </dl>

 

 
