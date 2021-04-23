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
# <a name="obtaining-statistical-performance-data"></a><span data-ttu-id="4b199-104">Получение статистических данных о производительности</span><span class="sxs-lookup"><span data-stu-id="4b199-104">Obtaining Statistical Performance Data</span></span>

<span data-ttu-id="4b199-105">В инструментарии WMI можно определять статистические данные производительности на основе данных в отформатированных классах производительности, производных от [**Win32 \_ перфформаттеддата**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span><span class="sxs-lookup"><span data-stu-id="4b199-105">In WMI, you can define statistical performance data based on data in formatted performance classes derived from [**Win32\_PerfFormattedData**](/windows/desktop/CIMWin32Prov/win32-perfformatteddata).</span></span> <span data-ttu-id="4b199-106">Доступной статистикой являются средние, минимальные, максимальные значения, диапазон и дисперсия, как определено в [типах статистических счетчиков](statistical-counter-types.md).</span><span class="sxs-lookup"><span data-stu-id="4b199-106">The available statistics are average, minimum, maximum, range, and variance, as defined in [Statistical Counter Types](statistical-counter-types.md).</span></span>

<span data-ttu-id="4b199-107">Следующий список включает специальные типы статистических счетчиков:</span><span class="sxs-lookup"><span data-stu-id="4b199-107">The following list includes the special statistical counter types:</span></span>

-   [<span data-ttu-id="4b199-108">Среднее время от острова \_</span><span class="sxs-lookup"><span data-stu-id="4b199-108">COOKER\_AVERAGE</span></span>](cooker-average.md)
-   [<span data-ttu-id="4b199-109">мин. \_</span><span class="sxs-lookup"><span data-stu-id="4b199-109">COOKER\_MIN</span></span>](cooker-min.md)
-   [<span data-ttu-id="4b199-110">максимум острова Кука \_</span><span class="sxs-lookup"><span data-stu-id="4b199-110">COOKER\_MAX</span></span>](cooker-max.md)
-   [<span data-ttu-id="4b199-111">диапазон острова Кука \_</span><span class="sxs-lookup"><span data-stu-id="4b199-111">COOKER\_RANGE</span></span>](cooker-range.md)
-   [<span data-ttu-id="4b199-112">\_отклонение от острова</span><span class="sxs-lookup"><span data-stu-id="4b199-112">COOKER\_VARIANCE</span></span>](cooker-variance.md)

<span data-ttu-id="4b199-113">В следующих примерах показано, как:</span><span class="sxs-lookup"><span data-stu-id="4b199-113">The following examples show how to:</span></span>

-   <span data-ttu-id="4b199-114">Создайте MOF-файл, определяющий класс вычисляемых данных.</span><span class="sxs-lookup"><span data-stu-id="4b199-114">Create a MOF file that defines a class of calculated data.</span></span>
-   <span data-ttu-id="4b199-115">Напишите скрипт, создающий экземпляр класса, и периодически обновляет данные в экземпляре с помощью пересчитанных статистических значений.</span><span class="sxs-lookup"><span data-stu-id="4b199-115">Write a script that creates an instance of the class, and periodically refreshes the data in the instance with the recalculated statistical values.</span></span>

## <a name="mof-file"></a><span data-ttu-id="4b199-116">MOF-файл</span><span class="sxs-lookup"><span data-stu-id="4b199-116">MOF File</span></span>

<span data-ttu-id="4b199-117">В следующем примере кода MOF создается новый класс вычисляемых данных с именем **Win32 \_ перфформаттеддата \_ аваилаблембитес**.</span><span class="sxs-lookup"><span data-stu-id="4b199-117">The following MOF code example creates a new calculated data class named **Win32\_PerfFormattedData\_AvailableMBytes**.</span></span> <span data-ttu-id="4b199-118">Этот класс содержит данные из свойства **аваилаблембитес** необработанного класса [**Win32 \_ перфравдата \_ перфос \_ Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).</span><span class="sxs-lookup"><span data-stu-id="4b199-118">This class contains data from the **AvailableMBytes** property of the raw class [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).</span></span> <span data-ttu-id="4b199-119">Класс **Win32 \_ перфформаттеддата \_ Аваилаблебитес** определяет свойства **СРЗНАЧ**, **min**, **Max**, **Range** и **вариативность**.</span><span class="sxs-lookup"><span data-stu-id="4b199-119">The **Win32\_PerfFormattedData\_AvailableBytes** class defines the properties **Average**, **Min**, **Max**, **Range**, and **Variance**.</span></span>

<span data-ttu-id="4b199-120">MOF-файл использует [**Квалификаторы свойств для форматированных классов счетчиков производительности**](property-qualifiers-for-performance-counter-classes.md) , чтобы определить источник данных свойства и формулу вычисления.</span><span class="sxs-lookup"><span data-stu-id="4b199-120">The MOF file uses the [**Property Qualifiers for Formatted Performance Counter Classes**](property-qualifiers-for-performance-counter-classes.md) to define the property data source and the calculation formula.</span></span>

-   <span data-ttu-id="4b199-121">Свойство **Average** получает необработанные данные из [**памяти Win32 \_ перфравдата \_ перфос \_**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**Свойство Аваилаблембитес** .</span><span class="sxs-lookup"><span data-stu-id="4b199-121">The **Average** property obtains raw data from the [**Win32\_PerfRawData\_PerfOS\_Memory**](/windows/desktop/WmiSdk/retrieving-raw-and-formatted-performance-data).**AvailableMBytes** property.</span></span>
-   <span data-ttu-id="4b199-122">**Квалификатор** счетчика для свойства **Average** указывает источник необработанных данных.</span><span class="sxs-lookup"><span data-stu-id="4b199-122">The Counter **qualifier** for the **Average** property specifies the raw data source.</span></span>
-   <span data-ttu-id="4b199-123">Квалификатор **кукингтипе** задает [ \_ минимальное](cooker-min.md) значение для вычисления данных в формуле.</span><span class="sxs-lookup"><span data-stu-id="4b199-123">The **CookingType** qualifier specifies the formula [COOKER\_MIN](cooker-min.md) for calculating the data.</span></span>
-   <span data-ttu-id="4b199-124">Квалификатор **самплевиндов** указывает, сколько выборок следует предпринять перед выполнением вычисления.</span><span class="sxs-lookup"><span data-stu-id="4b199-124">The **SampleWindow** qualifier specifies how many samples to take before performing the calculation.</span></span>


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



## <a name="script"></a><span data-ttu-id="4b199-125">Скрипт</span><span class="sxs-lookup"><span data-stu-id="4b199-125">Script</span></span>

<span data-ttu-id="4b199-126">Следующий пример кода скрипта получает статистику о доступной памяти в мегабайтах с помощью созданного ранее MOF.</span><span class="sxs-lookup"><span data-stu-id="4b199-126">The following script code example obtains statistics about available memory, in megabytes, using the MOF created previously.</span></span> <span data-ttu-id="4b199-127">Скрипт использует объект скрипта [**свбемрефрешер**](swbemrefresher.md) для создания обновления, содержащего один экземпляр класса Statistics, создаваемого MOF-файлом, то есть **Win32 \_ перфформаттеддата \_ MemoryStatistics**.</span><span class="sxs-lookup"><span data-stu-id="4b199-127">The script uses the [**SWbemRefresher**](swbemrefresher.md) scripting object to create a refresher that contains one instance of the statistics class that the MOF file creates, which is **Win32\_PerfFormattedData\_MemoryStatistics**.</span></span> <span data-ttu-id="4b199-128">Дополнительные сведения об использовании скриптов см. [в разделе Обновление данных WMI в скриптах](refreshing-wmi-data-in-scripts.md).</span><span class="sxs-lookup"><span data-stu-id="4b199-128">For more information about using scripts, see [Refreshing WMI Data in Scripts](refreshing-wmi-data-in-scripts.md).</span></span> <span data-ttu-id="4b199-129">При работе в C++ см. раздел [доступ к данным производительности в c++](accessing-performance-data-in-c--.md).</span><span class="sxs-lookup"><span data-stu-id="4b199-129">If working in C++, see [Accessing Performance Data in C++](accessing-performance-data-in-c--.md).</span></span>

> [!Note]  
> <span data-ttu-id="4b199-130">[**Свбемрефрешаблеитем. Object**](swbemrefreshableitem-object.md) должен вызываться после получения элемента из вызова [**свбемрефрешер. Add**](swbemrefresher-add.md) или скрипт завершится ошибкой.</span><span class="sxs-lookup"><span data-stu-id="4b199-130">[**SWbemRefreshableItem.Object**](swbemrefreshableitem-object.md) must be called after obtaining the item from the call to [**SWbemRefresher.Add**](swbemrefresher-add.md) or the script will fail.</span></span> <span data-ttu-id="4b199-131">[**Свбемрефрешер. Refresh**](swbemrefresher-refresh.md) должен вызываться перед входом в цикл для получения базовых значений, или статистические свойства равны нулю (0) при первом прохождении.</span><span class="sxs-lookup"><span data-stu-id="4b199-131">[**SWbemRefresher.Refresh**](swbemrefresher-refresh.md) must be called before entering the loop to obtain baseline values, or the statistical properties is zero (0) on the first pass.</span></span>

 


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



## <a name="running-the-script"></a><span data-ttu-id="4b199-132">Выполнение скрипта</span><span class="sxs-lookup"><span data-stu-id="4b199-132">Running the Script</span></span>

<span data-ttu-id="4b199-133">В следующей процедуре описывается, как выполнить пример.</span><span class="sxs-lookup"><span data-stu-id="4b199-133">The following procedure describes how to run the example.</span></span>

<span data-ttu-id="4b199-134">**Выполнение примера скрипта**</span><span class="sxs-lookup"><span data-stu-id="4b199-134">**To run the example script**</span></span>

1.  <span data-ttu-id="4b199-135">Скопируйте код MOF и сценарий в файлы на компьютере.</span><span class="sxs-lookup"><span data-stu-id="4b199-135">Copy both the MOF code and script to files on your computer.</span></span>
2.  <span data-ttu-id="4b199-136">Присвойте MOF-файлу расширение. mof и описание файла скрипта a. vbs.</span><span class="sxs-lookup"><span data-stu-id="4b199-136">Give the MOF file a .mof extension and the script file a .vbs description.</span></span>
3.  <span data-ttu-id="4b199-137">В командной строке перейдите в каталог, где хранятся файлы, и запустите [**mofcomp**](mofcomp.md) в MOF-файле.</span><span class="sxs-lookup"><span data-stu-id="4b199-137">On the command line, change to the directory where the files are stored, and run [**Mofcomp**](mofcomp.md) on the MOF file.</span></span> <span data-ttu-id="4b199-138">Например, если вы назначите имя файла *калкулатеддата. mof*, то команда будет иметь название **mofcomp** *калкулатеддата. mof*</span><span class="sxs-lookup"><span data-stu-id="4b199-138">For example, if you name the file *CalculatedData.mof*, then the command is **Mofcomp** *CalculatedData.mof*</span></span>
4.  <span data-ttu-id="4b199-139">Выполните скрипт.</span><span class="sxs-lookup"><span data-stu-id="4b199-139">Run the script.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b199-140">См. также</span><span class="sxs-lookup"><span data-stu-id="4b199-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b199-141">Мониторинг данных производительности</span><span class="sxs-lookup"><span data-stu-id="4b199-141">Monitoring Performance Data</span></span>](monitoring-performance-data.md)
</dt> <dt>

[<span data-ttu-id="4b199-142">Доступ к предустановленным классам производительности WMI</span><span class="sxs-lookup"><span data-stu-id="4b199-142">Accessing WMI Preinstalled Performance Classes</span></span>](accessing-wmi-preinstalled-performance-classes.md)
</dt> <dt>

[<span data-ttu-id="4b199-143">**Квалификаторы свойств для отформатированных классов счетчиков производительности**</span><span class="sxs-lookup"><span data-stu-id="4b199-143">**Property Qualifiers for Formatted Performance Counter Classes**</span></span>](property-qualifiers-for-performance-counter-classes.md)
</dt> <dt>

[<span data-ttu-id="4b199-144">Типы статистических счетчиков</span><span class="sxs-lookup"><span data-stu-id="4b199-144">Statistical Counter Types</span></span>](statistical-counter-types.md)
</dt> </dl>

 

 
