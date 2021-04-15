---
title: Объект LogFiles (Isysmon.h)
description: Этот класс используется для управления коллекцией из одного или нескольких файлов журнала, содержащих данные счетчика производительности. Чтобы получить этот объект, вызовите Системмонитор. файл_журнала.
ms.assetid: 1af475c5-ed0c-49b4-a558-13eb8758a986
keywords:
- Файл журнала Сисмон
- Сисмон объект LogFile, описание
topic_type:
- apiref
api_name:
- LogFiles
api_location:
- Sysmon.ocx
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab30de5c371c012e1320950e4a491021bb0b15c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488943"
---
# <a name="logfiles-object"></a><span data-ttu-id="c46df-105">Объект файл_журнала</span><span class="sxs-lookup"><span data-stu-id="c46df-105">LogFiles object</span></span>

<span data-ttu-id="c46df-106">Этот класс используется для управления коллекцией из одного или нескольких файлов журнала, содержащих данные счетчика производительности.</span><span class="sxs-lookup"><span data-stu-id="c46df-106">Use this class to manage a collection of one or more log files that contain performance counter data.</span></span>

<span data-ttu-id="c46df-107">Чтобы получить этот объект, вызовите [**системмонитор. файл_журнала**](systemmonitor-logfiles.md).</span><span class="sxs-lookup"><span data-stu-id="c46df-107">To retrieve this object, call [**SystemMonitor.LogFiles**](systemmonitor-logfiles.md).</span></span>

## <a name="members"></a><span data-ttu-id="c46df-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="c46df-108">Members</span></span>

<span data-ttu-id="c46df-109">Объект **файл_журнала** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="c46df-109">The **LogFiles** object has these types of members:</span></span>

-   [<span data-ttu-id="c46df-110">Методы</span><span class="sxs-lookup"><span data-stu-id="c46df-110">Methods</span></span>](#methods)
-   [<span data-ttu-id="c46df-111">Свойства</span><span class="sxs-lookup"><span data-stu-id="c46df-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="c46df-112">Методы</span><span class="sxs-lookup"><span data-stu-id="c46df-112">Methods</span></span>

<span data-ttu-id="c46df-113">Объект **файл_журнала** содержит эти методы.</span><span class="sxs-lookup"><span data-stu-id="c46df-113">The **LogFiles** object has these methods.</span></span>



| <span data-ttu-id="c46df-114">Метод</span><span class="sxs-lookup"><span data-stu-id="c46df-114">Method</span></span>                                          | <span data-ttu-id="c46df-115">Описание</span><span class="sxs-lookup"><span data-stu-id="c46df-115">Description</span></span>                                                                           |
|:------------------------------------------------|:--------------------------------------------------------------------------------------|
| [<span data-ttu-id="c46df-116">**Включить**</span><span class="sxs-lookup"><span data-stu-id="c46df-116">**Add**</span></span>](systemmonitor-logfiles-add.md)       | <span data-ttu-id="c46df-117">Добавляет экземпляр [**логфилеитем**](logfileitem.md) в коллекцию.</span><span class="sxs-lookup"><span data-stu-id="c46df-117">Adds a [**LogFileItem**](logfileitem.md) instance to the collection.</span></span><br/>      |
| [<span data-ttu-id="c46df-118">**Отменит**</span><span class="sxs-lookup"><span data-stu-id="c46df-118">**Remove**</span></span>](systemmonitor-logfiles-remove.md) | <span data-ttu-id="c46df-119">Удаляет экземпляр [**логфилеитем**](logfileitem.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="c46df-119">Removes a [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="c46df-120">Свойства</span><span class="sxs-lookup"><span data-stu-id="c46df-120">Properties</span></span>

<span data-ttu-id="c46df-121">Объект **файл_журнала** имеет следующие свойства.</span><span class="sxs-lookup"><span data-stu-id="c46df-121">The **LogFiles** object has these properties.</span></span>



| <span data-ttu-id="c46df-122">Свойство</span><span class="sxs-lookup"><span data-stu-id="c46df-122">Property</span></span>                                                 | <span data-ttu-id="c46df-123">Описание</span><span class="sxs-lookup"><span data-stu-id="c46df-123">Description</span></span>                                                                                         |
|:---------------------------------------------------------|:----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c46df-124">**Расчета**</span><span class="sxs-lookup"><span data-stu-id="c46df-124">**Count**</span></span>](systemmonitor-logfiles-count.md)<br/> | <span data-ttu-id="c46df-125">Возвращает количество экземпляров [**логфилеитем**](logfileitem.md) в коллекции.</span><span class="sxs-lookup"><span data-stu-id="c46df-125">Retrieves the number of [**LogFileItem**](logfileitem.md) instances in the collection.</span></span><br/>  |
| [<span data-ttu-id="c46df-126">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="c46df-126">**Item**</span></span>](systemmonitor-logfiles-item.md)<br/>   | <span data-ttu-id="c46df-127">Извлекает указанный экземпляр [**логфилеитем**](logfileitem.md) из коллекции.</span><span class="sxs-lookup"><span data-stu-id="c46df-127">Retrieves the specified [**LogFileItem**](logfileitem.md) instance from the collection.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c46df-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="c46df-128">Remarks</span></span>

<span data-ttu-id="c46df-129">Чтобы СИСМОН отобразить счетчики производительности из файла журнала, задайте для [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) значение [**DataSourceTypeConstants.sysмонлогфилес**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="c46df-129">To have SYSMON display performance counters from a log file, set [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="c46df-130">После добавления файлов журнала в коллекцию используйте коллекцию [**счетчиков**](counters.md) , чтобы указать данные счетчиков, которые необходимо считать из файлов журнала.</span><span class="sxs-lookup"><span data-stu-id="c46df-130">After adding the log files to the collection, use the [**Counters**](counters.md) collection to specify the counters data that you want to read from the log files.</span></span> <span data-ttu-id="c46df-131">Обратите внимание, что если **системмонитор. DataSourceType** имеет значение **DataSourceTypeConstants.sysмонлогфилес**, сисмон будет выполнять повторную выборку файлов журнала каждый раз при добавлении файла журнала или счетчика в соответствующие коллекции.</span><span class="sxs-lookup"><span data-stu-id="c46df-131">Note that if **SystemMonitor.DataSourceType** is set to **DataSourceTypeConstants.sysmonLogFiles**, SYSMON will resample the log files each time you add a log file or counter to their respective collections.</span></span>

<span data-ttu-id="c46df-132">**До Windows Vista:** Невозможно добавить файлы журнала в [**коллекцию файлов журнала**](systemmonitor-logfiles.md) , если для [**системмонитор. DataSourceType**](systemmonitor-datasourcetype.md) задано значение [**DataSourceTypeConstants.sysмонлогфилес**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span><span class="sxs-lookup"><span data-stu-id="c46df-132">**Prior to Windows Vista:** You cannot add log files to the [**log file collection**](systemmonitor-logfiles.md) if the value of [**SystemMonitor.DataSourceType**](systemmonitor-datasourcetype.md) is set to [**DataSourceTypeConstants.sysmonLogFiles**](/windows/desktop/api/ISysmon/ne-isysmon-datasourcetypeconstants).</span></span> <span data-ttu-id="c46df-133">Сначала задайте **системмонитор. DataSourceType** для **DataSourceTypeConstants.sysмоннуллдатасаурце**, добавьте файлы журнала и счетчики, а затем установите **Системмонитор. DataSourceType** в **DataSourceTypeConstants.sysмонлогфилес**.</span><span class="sxs-lookup"><span data-stu-id="c46df-133">First, set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonNullDataSource**, add your log files and counters, and then set **SystemMonitor.DataSourceType** to **DataSourceTypeConstants.sysmonLogFiles**.</span></span>

<span data-ttu-id="c46df-134">Свойства [**системмонитор. логвиевстарт**](systemmonitor-logviewstart.md) и [**системмонитор. логвиевстоп**](systemmonitor-logviewstop.md) определяют диапазон значений выборки из файлов журнала в графе.</span><span class="sxs-lookup"><span data-stu-id="c46df-134">The [**SystemMonitor.LogViewStart**](systemmonitor-logviewstart.md) and [**SystemMonitor.LogViewStop**](systemmonitor-logviewstop.md) properties specify the range of sampled values from the log files to graph.</span></span> <span data-ttu-id="c46df-135">СИСМОН Graphs только по одному представлению данных из файла журнала (представление Graph не прокручивается, как это делается при построении диаграммы текущей активности компьютера).</span><span class="sxs-lookup"><span data-stu-id="c46df-135">SYSMON graphs only one view worth of data from the log file (the graph view does not scroll as it does when graphing the current activity of the computer).</span></span> <span data-ttu-id="c46df-136">Если выборка данных превышает то, что может быть отображено в одном представлении графика, СИСМОН сжимает данные выборки (Каждая диаграмма представляет среднее значение нескольких выборок), чтобы вместить все данные выборки из файлов журнала на диаграмме.</span><span class="sxs-lookup"><span data-stu-id="c46df-136">If the sampled data exceeds what can be shown on a single graph view, SYSMON compresses the sampled data (each graphed point represents the average of multiple sampled values) to fit all the sampled data from the log files on the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="c46df-137">Требования</span><span class="sxs-lookup"><span data-stu-id="c46df-137">Requirements</span></span>



| <span data-ttu-id="c46df-138">Требование</span><span class="sxs-lookup"><span data-stu-id="c46df-138">Requirement</span></span> | <span data-ttu-id="c46df-139">Значение</span><span class="sxs-lookup"><span data-stu-id="c46df-139">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c46df-140">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c46df-140">Minimum supported client</span></span><br/> | <span data-ttu-id="c46df-141">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c46df-141">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="c46df-142">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c46df-142">Minimum supported server</span></span><br/> | <span data-ttu-id="c46df-143">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="c46df-143">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c46df-144">Заголовок</span><span class="sxs-lookup"><span data-stu-id="c46df-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="c46df-145"><dt>Исисмон. h</dt></span><span class="sxs-lookup"><span data-stu-id="c46df-145"><dt>Isysmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="c46df-146">DLL</span><span class="sxs-lookup"><span data-stu-id="c46df-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c46df-147"><dt>Сисмон. ocx</dt></span><span class="sxs-lookup"><span data-stu-id="c46df-147"><dt>Sysmon.ocx</dt></span></span> </dl> |



 

 





