---
description: Файлы журналов WMI больше не поддерживаются.
ms.assetid: 4ba80063-7aa6-42df-a620-1b366b795034
ms.tgt_platform: multiple
title: Ведение журнала действий WMI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6ced8645eb7ad9005e6ba751d011ae7f0ccb3dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693273"
---
# <a name="logging-wmi-activity"></a><span data-ttu-id="57ee4-103">Ведение журнала действий WMI</span><span class="sxs-lookup"><span data-stu-id="57ee4-103">Logging WMI Activity</span></span>

<span data-ttu-id="57ee4-104">Файлы журналов WMI больше не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="57ee4-104">The WMI log files are no longer supported.</span></span> <span data-ttu-id="57ee4-105">Начиная с Windows Vista, Инструментарий WMI использует средство [трассировки событий для Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) и события, доступные через пользовательский интерфейс **Просмотр событий** или программу командной строки wevtutil.</span><span class="sxs-lookup"><span data-stu-id="57ee4-105">Starting with Windows Vista, WMI uses [Event Tracing for Windows (ETW](/windows/desktop/ETW/event-tracing-portal)) and events that are available through the **Event Viewer** UI or the Wevtutil command line tool.</span></span> <span data-ttu-id="57ee4-106">Дополнительные сведения см. в разделе Поставщик ETW и документация по командной строке [вевутил](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) .</span><span class="sxs-lookup"><span data-stu-id="57ee4-106">For more information, see the ETW provider and the [Wevutil](/previous-versions/windows/it-pro/windows-server-2012-R2-and-2012/cc732848(v=ws.11)) command-line documentation.</span></span>

<span data-ttu-id="57ee4-107">В этом разделе обсуждаются следующие разделы:</span><span class="sxs-lookup"><span data-stu-id="57ee4-107">The following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="57ee4-108">Файлы журналов WMI до Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57ee4-108">WMI Log Files Before Windows Vista</span></span>](#wmi-log-files-before-windows-vista)
-   [<span data-ttu-id="57ee4-109">Действия записи в журнал для компонентов WMI Core до Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57ee4-109">Logging Activities for WMI Core Components Before Windows Vista</span></span>](#logging-activities-for-wmi-core-components-before-windows-vista)
-   [<span data-ttu-id="57ee4-110">Действия ведения журнала для компонентов поставщика WMI до Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57ee4-110">Logging Activities for WMI Provider Components Before Windows Vista</span></span>](#logging-activities-for-wmi-provider-components-before-windows-vista)
-   [<span data-ttu-id="57ee4-111">См. также</span><span class="sxs-lookup"><span data-stu-id="57ee4-111">Related topics</span></span>](#related-topics)

## <a name="wmi-log-files-before-windows-vista"></a><span data-ttu-id="57ee4-112">Файлы журналов WMI до Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57ee4-112">WMI Log Files Before Windows Vista</span></span>

<span data-ttu-id="57ee4-113">Файлы журналов, созданные WMI и различными поставщиками, регистрируются в записях: события, трассировка или диагностические данные, ошибки и различные действия.</span><span class="sxs-lookup"><span data-stu-id="57ee4-113">The log files created by WMI and various providers record: events, trace or diagnostic data, errors, and various activities.</span></span> <span data-ttu-id="57ee4-114">Только администраторы имеют доступ на чтение к папке журнала WMI, найденной в журналах% WINDIR% \\ system32 \\ WBEM \\ .</span><span class="sxs-lookup"><span data-stu-id="57ee4-114">Only administrators have read access to the WMI log folder found at %windir%\\system32\\wbem\\logs.</span></span>

<span data-ttu-id="57ee4-115">В файлы журнала записываются только компоненты ядра WMI или поставщики WMI.</span><span class="sxs-lookup"><span data-stu-id="57ee4-115">Only WMI core components or WMI providers write to log files.</span></span> <span data-ttu-id="57ee4-116">Данные в этих журналах можно читать и просматривать только в целях диагностики.</span><span class="sxs-lookup"><span data-stu-id="57ee4-116">You can only read or view the data in these logs for diagnostic purposes.</span></span> <span data-ttu-id="57ee4-117">Вы можете создавать и хранить собственные файлы журнала в каталоге журнала WMI.</span><span class="sxs-lookup"><span data-stu-id="57ee4-117">You can create and store your own log files in the WMI log directory.</span></span>

## <a name="logging-activities-for-wmi-core-components-before-windows-vista"></a><span data-ttu-id="57ee4-118">Действия записи в журнал для компонентов WMI Core до Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57ee4-118">Logging Activities for WMI Core Components Before Windows Vista</span></span>

<span data-ttu-id="57ee4-119">Эти файлы не содержат единообразный формат, подходящий для программного чтения.</span><span class="sxs-lookup"><span data-stu-id="57ee4-119">These files do not contain a consistent format that is suitable for reading programmatically.</span></span> <span data-ttu-id="57ee4-120">Дополнительные сведения о конкретных журналах см. в разделе [файлы журналов WMI](wmi-log-files.md).</span><span class="sxs-lookup"><span data-stu-id="57ee4-120">For more information about specific logs, see [WMI Log Files](wmi-log-files.md).</span></span>

<span data-ttu-id="57ee4-121">Действия по ведению журнала для компонентов WMI Core возникают при установке следующих разделов реестра:</span><span class="sxs-lookup"><span data-stu-id="57ee4-121">Logging activities for WMI core components occurs when the following registry keys are set:</span></span>

-   <span data-ttu-id="57ee4-122">Уровень ведения журнала</span><span class="sxs-lookup"><span data-stu-id="57ee4-122">Logging level</span></span>

    <span data-ttu-id="57ee4-123">Изменения в значении реестра уровня ведения журнала вступают в силу немедленно.</span><span class="sxs-lookup"><span data-stu-id="57ee4-123">Changes to the logging level registry value take effect immediately.</span></span> <span data-ttu-id="57ee4-124">Перезапуск службы WMI не требуется.</span><span class="sxs-lookup"><span data-stu-id="57ee4-124">No restart of the WMI service is necessary.</span></span>

    <span data-ttu-id="57ee4-125">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера, \\  \\  \\  \\ **ведение журнала** Microsoft WBEM CIMOM = 2</span><span class="sxs-lookup"><span data-stu-id="57ee4-125">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging** = 2</span></span>

    <span data-ttu-id="57ee4-126">В следующем списке перечислены уровни ведения журнала, которые могут быть определены в реестре.</span><span class="sxs-lookup"><span data-stu-id="57ee4-126">The following list lists the logging levels that can be defined in the registry.</span></span>

    

    | <span data-ttu-id="57ee4-127">Уровень ведения журнала</span><span class="sxs-lookup"><span data-stu-id="57ee4-127">Logging level</span></span> | <span data-ttu-id="57ee4-128">Описание</span><span class="sxs-lookup"><span data-stu-id="57ee4-128">Description</span></span>               |
    |---------------|---------------------------|
    | <span data-ttu-id="57ee4-129">0</span><span class="sxs-lookup"><span data-stu-id="57ee4-129">0</span></span>             | <span data-ttu-id="57ee4-130">Без ведения журнала</span><span class="sxs-lookup"><span data-stu-id="57ee4-130">No Logging</span></span>                |
    | <span data-ttu-id="57ee4-131">1</span><span class="sxs-lookup"><span data-stu-id="57ee4-131">1</span></span>             | <span data-ttu-id="57ee4-132">Записывать только ошибки</span><span class="sxs-lookup"><span data-stu-id="57ee4-132">Log only errors</span></span>           |
    | <span data-ttu-id="57ee4-133">2</span><span class="sxs-lookup"><span data-stu-id="57ee4-133">2</span></span>             | <span data-ttu-id="57ee4-134">Подробное ведение журнала (по умолчанию)</span><span class="sxs-lookup"><span data-stu-id="57ee4-134">Verbose Logging (default)</span></span> |

    

     

-   <span data-ttu-id="57ee4-135">Расположение файла журнала</span><span class="sxs-lookup"><span data-stu-id="57ee4-135">Log file location</span></span>

    <span data-ttu-id="57ee4-136">Чтобы изменения в расположении файла журнала вступили в силу, перезапустите службу WMI.</span><span class="sxs-lookup"><span data-stu-id="57ee4-136">For changes to log file location to take effect, restart the WMI service.</span></span>

    <span data-ttu-id="57ee4-137">**HKey \_ По локального \_ компьютера** \\ **программное обеспечение** \\ **Microsoft** \\ **WBEM** \\ **CIMOM** \\ **Каталог журнала** =% WINDIR% \\ system32 \\ WBEM \\ журналы</span><span class="sxs-lookup"><span data-stu-id="57ee4-137">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Logging Directory** = %windir%\\system32\\wbem\\logs</span></span>

-   <span data-ttu-id="57ee4-138">Максимальный размер файла журнала, в байтах</span><span class="sxs-lookup"><span data-stu-id="57ee4-138">Maximum log file size, in bytes</span></span>

    <span data-ttu-id="57ee4-139">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера. \\  \\ файл журнала Microsoft **WBEM** \\ **CIMOM** \\ **максимальный размер** = 65536</span><span class="sxs-lookup"><span data-stu-id="57ee4-139">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM**\\**Log File Max Size** = 65536</span></span>

<span data-ttu-id="57ee4-140">Эти значения разделов реестра можно изменить с помощью редактора реестра или оснастки WMI для консоли управления (MMC).</span><span class="sxs-lookup"><span data-stu-id="57ee4-140">You can change these registry key values through the Registry Editor or through the WMI snap-in for the Microsoft Management Console.</span></span>

<span data-ttu-id="57ee4-141">**Установка уровня ведения журнала для инструментария WMI до Windows Vista**</span><span class="sxs-lookup"><span data-stu-id="57ee4-141">**To set the logging level for WMI before Windows Vista**</span></span>

1.  <span data-ttu-id="57ee4-142">Нажмите кнопку **Пуск**, затем щелкните **Выполнить**.</span><span class="sxs-lookup"><span data-stu-id="57ee4-142">Click **Start**, and then click **Run**.</span></span>
2.  <span data-ttu-id="57ee4-143">Введите **wmimgmt. msc**</span><span class="sxs-lookup"><span data-stu-id="57ee4-143">Type **wmimgmt.msc**</span></span>
3.  <span data-ttu-id="57ee4-144">В меню **Действие** выберите пункт **Свойства**.</span><span class="sxs-lookup"><span data-stu-id="57ee4-144">On the **Action** menu, click **Properties**.</span></span>
4.  <span data-ttu-id="57ee4-145">На вкладке **ведение журнала** задайте для параметра уровень ведения журнала значение **отключено**, **включено** или **подробный**.</span><span class="sxs-lookup"><span data-stu-id="57ee4-145">On the **Logging** tab, set the logging level to **Disabled**, **Enabled**, or **Verbose**.</span></span>
5.  <span data-ttu-id="57ee4-146">В поле **Расположение:** введите путь к папке файла журнала и **максимальный размер (в байтах):**, установите максимальный размер файла журнала (в байтах).</span><span class="sxs-lookup"><span data-stu-id="57ee4-146">In **Location:**, type the path to the log file folder and in **Maximum size (bytes):**, set the maximum size, in bytes, of the log file.</span></span>

<span data-ttu-id="57ee4-147">Дополнительные сведения о настройке свойств файла журнала см. в интерактивной справке для управляющего приложения WMI.</span><span class="sxs-lookup"><span data-stu-id="57ee4-147">For more information about setting the log file properties, see the online Help for the WMI Control application.</span></span>

## <a name="logging-activities-for-wmi-provider-components-before-windows-vista"></a><span data-ttu-id="57ee4-148">Действия ведения журнала для компонентов поставщика WMI до Windows Vista</span><span class="sxs-lookup"><span data-stu-id="57ee4-148">Logging Activities for WMI Provider Components Before Windows Vista</span></span>

<span data-ttu-id="57ee4-149">Если включено ведение журнала для компонентов ядра WMI, ведение журнала также включено для любого поставщика с возможностями ведения журнала.</span><span class="sxs-lookup"><span data-stu-id="57ee4-149">When logging for WMI core components is enabled, logging is also enabled for any provider with logging capabilities.</span></span>

<span data-ttu-id="57ee4-150">В следующем списке перечислены необходимые значения.</span><span class="sxs-lookup"><span data-stu-id="57ee4-150">The following list lists the required values.</span></span>

<dl> <dt>

<span data-ttu-id="57ee4-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**File**</span><span class="sxs-lookup"><span data-stu-id="57ee4-151"><span id="File"></span><span id="file"></span><span id="FILE"></span>**File**</span></span>
</dt> <dd>

<span data-ttu-id="57ee4-152">Полный путь и имя файла журнала.</span><span class="sxs-lookup"><span data-stu-id="57ee4-152">Full path and file name of the log file.</span></span> <span data-ttu-id="57ee4-153">По умолчанию используется значение% WINDIR% \\ system32 \\ WBEM \\ logs.</span><span class="sxs-lookup"><span data-stu-id="57ee4-153">The default value is %windir%\\system32\\wbem\\logs.</span></span> <span data-ttu-id="57ee4-154">Для использования этого именованного значения **тип** с именем value должен быть установлен в значение = File.</span><span class="sxs-lookup"><span data-stu-id="57ee4-154">The **Type** named value must be set to = File for this named value to be used.</span></span>

</dd> <dt>

<span data-ttu-id="57ee4-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Уровню**</span><span class="sxs-lookup"><span data-stu-id="57ee4-155"><span id="Level"></span><span id="level"></span><span id="LEVEL"></span>**Level**</span></span>
</dt> <dd>

<span data-ttu-id="57ee4-156">32-разрядная логическая маска, определяющая тип выходных данных отладки, создаваемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="57ee4-156">A 32-bit logical mask that defines the type of debugging output generated by the provider.</span></span> <span data-ttu-id="57ee4-157">Это значение зависит от поставщика.</span><span class="sxs-lookup"><span data-stu-id="57ee4-157">This value is provider-dependent.</span></span> <span data-ttu-id="57ee4-158">Значение по умолчанию — 0 (нуль).</span><span class="sxs-lookup"><span data-stu-id="57ee4-158">The default value is 0 (zero).</span></span>

</dd> <dt>

<span data-ttu-id="57ee4-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**</span><span class="sxs-lookup"><span data-stu-id="57ee4-159"><span id="MaxFileSize"></span><span id="maxfilesize"></span><span id="MAXFILESIZE"></span>**MaxFileSize**</span></span>
</dt> <dd>

<span data-ttu-id="57ee4-160">Максимальный размер файла журнала в байтах.</span><span class="sxs-lookup"><span data-stu-id="57ee4-160">Maximum file size, in bytes, of the log file.</span></span> <span data-ttu-id="57ee4-161">Это целое значение должно находиться в диапазоне от 1024 до 2 ^ 32-1.</span><span class="sxs-lookup"><span data-stu-id="57ee4-161">This integer value must be in the range 1024 to 2^32-1.</span></span> <span data-ttu-id="57ee4-162">Если размер файла превышает это значение, файл переименовывается в **~ filename** и создается новый пустой файл журнала.</span><span class="sxs-lookup"><span data-stu-id="57ee4-162">When the file size exceeds this value, the file is renamed to **~filename** and a new, empty log file is created.</span></span> <span data-ttu-id="57ee4-163">Место на диске, необходимое для файла журнала, вдвое больше значения **MaxFileSize**.</span><span class="sxs-lookup"><span data-stu-id="57ee4-163">The disk space required for the log file is twice the value of **MaxFileSize**.</span></span> <span data-ttu-id="57ee4-164">Значение по умолчанию — 65 535.</span><span class="sxs-lookup"><span data-stu-id="57ee4-164">The default value is 65,535.</span></span>

</dd> <dt>

<span data-ttu-id="57ee4-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Тип**</span><span class="sxs-lookup"><span data-stu-id="57ee4-165"><span id="Type"></span><span id="type"></span><span id="TYPE"></span>**Type**</span></span>
</dt> <dd>

<span data-ttu-id="57ee4-166">Можно задать значение = File или = Debugger.</span><span class="sxs-lookup"><span data-stu-id="57ee4-166">Can be set to = File or = Debugger.</span></span> <span data-ttu-id="57ee4-167">Если задано значение = File, данные трассировки записываются в файл журнала, указанный в **файле** с именем value.</span><span class="sxs-lookup"><span data-stu-id="57ee4-167">If set to = File, the trace information is written to the log file specified in the **File** named value.</span></span> <span data-ttu-id="57ee4-168">Значение по умолчанию — = File.</span><span class="sxs-lookup"><span data-stu-id="57ee4-168">The default value is = File.</span></span>

</dd> </dl>

<span data-ttu-id="57ee4-169">Например, чтобы вести журнал запросов и получать вызовы экземпляров от поставщика представления, используйте следующие значения раздела реестра.</span><span class="sxs-lookup"><span data-stu-id="57ee4-169">For example, to log query and get instance calls from the View Provider, use the following registry key values.</span></span> <span data-ttu-id="57ee4-170">Журнал будет находиться в папке Log и будет иметь размер файла по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="57ee4-170">The log will be located in the log folder and will be the default file size.</span></span>

<span data-ttu-id="57ee4-171">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **поставщики Microsoft** \\ **WBEM** \\  \\ **ведение журнала** \\ **виевпровидер** \\ **файл** = C: \\ Windows \\ system32 \\ WBEM \\ журналы \\ виевпровидер. log</span><span class="sxs-lookup"><span data-stu-id="57ee4-171">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**File** = C:\\Windows\\system32\\WBEM\\Logs\\ViewProvider.log</span></span>

<span data-ttu-id="57ee4-172">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **поставщики Microsoft** \\ **WBEM** \\  \\ **ведение журнала** \\ **виевпровидер** \\ **уровень** = 2</span><span class="sxs-lookup"><span data-stu-id="57ee4-172">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Level** = 2</span></span>

<span data-ttu-id="57ee4-173">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **поставщики Microsoft** \\ **WBEM** \\  \\ **ведение журнала** \\ **виевпровидер** \\ **MaxFileSize** = 65535</span><span class="sxs-lookup"><span data-stu-id="57ee4-173">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**MaxFileSize** = 65535</span></span>

<span data-ttu-id="57ee4-174">**HKey \_ \_** \\ **Программное обеспечение** локального компьютера \\ **поставщики Microsoft** \\ **WBEM** \\  \\ **ведение журнала** \\ **виевпровидер** \\ **тип** = файл</span><span class="sxs-lookup"><span data-stu-id="57ee4-174">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**PROVIDERS**\\**Logging**\\**ViewProvider**\\**Type** = File</span></span>

> [!Note]  
> <span data-ttu-id="57ee4-175">Для собственных поставщиков с возможностями ведения журнала необходимо записать необходимые разделы и значения реестра, чтобы включить ведение журнала.</span><span class="sxs-lookup"><span data-stu-id="57ee4-175">For your own providers with logging capabilities, you need to write the necessary registry keys and values to enable logging.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="57ee4-176">См. также</span><span class="sxs-lookup"><span data-stu-id="57ee4-176">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="57ee4-177">[Устранение неполадок WMI](wmi-troubleshooting.md).</span><span class="sxs-lookup"><span data-stu-id="57ee4-177">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> <dt>

[<span data-ttu-id="57ee4-178">Файлы журналов WMI</span><span class="sxs-lookup"><span data-stu-id="57ee4-178">WMI Log Files</span></span>](wmi-log-files.md)
</dt> <dt>

[<span data-ttu-id="57ee4-179">Классы устранения неполадок WMI</span><span class="sxs-lookup"><span data-stu-id="57ee4-179">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> <dt>

[<span data-ttu-id="57ee4-180">Трассировка действий WMI</span><span class="sxs-lookup"><span data-stu-id="57ee4-180">Tracing WMI Activity</span></span>](tracing-wmi-activity.md)
</dt> </dl>

 

 
