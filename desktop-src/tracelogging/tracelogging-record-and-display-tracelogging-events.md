---
title: Запись и Просмотр событий Трацелоггинг
description: Записывайте события Трацелоггинг с помощью средства записи производительности Windows (ЗВЧ) и просматривайте их с помощью анализатора производительности Windows (WPA).
ms.assetid: 906589FA-F48D-4105-9E56-1EC8B86542FB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09be054d274fc2c2c62635cc7bf12e8cf8acdef3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103891036"
---
# <a name="record-and-view-tracelogging-events"></a><span data-ttu-id="feb16-103">Запись и Просмотр событий Трацелоггинг</span><span class="sxs-lookup"><span data-stu-id="feb16-103">Record and View TraceLogging Events</span></span>

<span data-ttu-id="feb16-104">Записывайте события Трацелоггинг с помощью средства записи производительности Windows (ЗВЧ) и просматривайте их с помощью анализатора производительности Windows (WPA).</span><span class="sxs-lookup"><span data-stu-id="feb16-104">Record TraceLogging events with the Windows Performance Recorder (WPR) and view them with the Windows Performance Analyzer (WPA).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="feb16-105">Предварительные условия</span><span class="sxs-lookup"><span data-stu-id="feb16-105">Prerequisites</span></span>

-   <span data-ttu-id="feb16-106">Windows 10</span><span class="sxs-lookup"><span data-stu-id="feb16-106">Windows 10</span></span>
-   <span data-ttu-id="feb16-107">Windows 10 с версией средства записи производительности Windows (ЗВЧ) и Windows 10 анализатора производительности Windows (WPA), которая является частью комплекта средств для развертывания и оценки Windows® (Windows ADK).</span><span class="sxs-lookup"><span data-stu-id="feb16-107">The Windows 10 version of Windows Performance Recorder (WPR), and the Windows 10 version of Windows Performance Analyzer (WPA) which is part of the Windows® Assessment and Deployment Kit (Windows ADK).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="feb16-108">Трассировки, захваченные с помощью Трацелоггинг, должны быть записаны в версии Windows 10 средства записи производительности Windows и просмотрены с помощью Windows 10 Performance Analyzer.</span><span class="sxs-lookup"><span data-stu-id="feb16-108">Traces captured with TraceLogging must be captured with the Windows 10 version of Windows Performance Recorder and viewed with the Windows 10 version of Windows Performance Analyzer.</span></span> <span data-ttu-id="feb16-109">Если вы не можете записать или декодировать события, убедитесь, что используете версию средств Windows 10.</span><span class="sxs-lookup"><span data-stu-id="feb16-109">If you are unable to capture or decode your events, verify that you are using the Windows 10 version of the tools.</span></span>

 

### <a name="1-capture-trace-data-with-wpr"></a><span data-ttu-id="feb16-110">1. запись данных трассировки с помощью ЗВЧ</span><span class="sxs-lookup"><span data-stu-id="feb16-110">1. Capture trace data with WPR</span></span>

<span data-ttu-id="feb16-111">Чтобы записать трассировку Windows Phone, см. раздел Capture Трацелоггинг Events On Windows Phone ниже.</span><span class="sxs-lookup"><span data-stu-id="feb16-111">To capture a trace on Windows Phone, see Capture TraceLogging events on Windows Phone below.</span></span>

<span data-ttu-id="feb16-112">Создайте профиль средства записи производительности Windows (. впрп), чтобы можно было использовать ЗВЧ для захвата событий Трацелоггинг.</span><span class="sxs-lookup"><span data-stu-id="feb16-112">Create a Windows Performance Recorder profile (.wprp) so that you can use WPR to capture your Tracelogging events.</span></span>

<span data-ttu-id="feb16-113">**Создайте. Файл ВПРП**</span><span class="sxs-lookup"><span data-stu-id="feb16-113">**Create a .WPRP file**</span></span>

1.  <span data-ttu-id="feb16-114">Используйте следующий пример ВПРП с примером машинного кода в [Трацелоггинг C/C++ быстрое начало](tracelogging-native-quick-start.md) или управляемом примере в [управляемом быстрое начало трацелоггинг](tracelogging-managed-quick-start.md).</span><span class="sxs-lookup"><span data-stu-id="feb16-114">Use the following WPRP example with the native code example in the [TraceLogging C/C++ Quick Start](tracelogging-native-quick-start.md) or the managed example in the [TraceLogging Managed Quick Start](tracelogging-managed-quick-start.md).</span></span> <span data-ttu-id="feb16-115">Если вы регистрируете события из собственного поставщика, замените `TODO` разделы соответствующими значениями для поставщика.</span><span class="sxs-lookup"><span data-stu-id="feb16-115">If you are logging events from your own provider, replace the `TODO` sections with the appropriate values for your provider.</span></span>

    > <span data-ttu-id="feb16-116">\[! Существенно\]</span><span class="sxs-lookup"><span data-stu-id="feb16-116">\[!Important\]</span></span>  

     

    <span data-ttu-id="feb16-117">Если вы используете быстрый запуск Трацелоггинг C/C++, укажите идентификатор GUID поставщика в `Name` атрибуте `<EventProvider>` элемента.</span><span class="sxs-lookup"><span data-stu-id="feb16-117">If you are using the TraceLogging C/C++ quick start, specify the provider GUID in the `Name` attribute of the `<EventProvider>` element.</span></span> <span data-ttu-id="feb16-118">Например: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`.</span><span class="sxs-lookup"><span data-stu-id="feb16-118">For example: `<EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833" />`.</span></span> <span data-ttu-id="feb16-119">Если вы используете быстрое начало работы с управляемыми Трацелоггинг, укажите имя поставщика, которое предшествует " \* " в `Name` атрибуте `<EventProvider />` элемента.</span><span class="sxs-lookup"><span data-stu-id="feb16-119">If you are using the managed TraceLogging quick start, specify the provider name prefaced by '\*' in the `Name` attribute of the `<EventProvider />` element.</span></span> <span data-ttu-id="feb16-120">Например, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.</span><span class="sxs-lookup"><span data-stu-id="feb16-120">For example, `<EventProvider Name="*SimpleTraceLoggingProvider" />`.</span></span>

    <span data-ttu-id="feb16-121">Пример файла ВПРП.</span><span class="sxs-lookup"><span data-stu-id="feb16-121">Sample WPRP file.</span></span>

    ```XML
    <?xml version="1.0" encoding="utf-8"?>
    <!-- TODO: 
    1. Find and replace "SimpleTraceLoggingProvider" with the name of your provider.
    2. See TODO below to update GUID for your event provider
    -->
    <WindowsPerformanceRecorder Version="1.0" Author="Microsoft Corporation" Copyright="Microsoft Corporation" Company="Microsoft Corporation">
      <Profiles>
        <EventCollector Id="EventCollector_SimpleTraceLoggingProvider" Name="SimpleTraceLoggingProvider">
          <BufferSize Value="64" />
          <Buffers Value="4" />
        </EventCollector>

        <!-- TODO: 
     1. Update Name attribute in EventProvider xml element with your provider GUID, eg: Name="3970F9cf-2c0c-4f11-b1cc-e3a1e9958833". Or
        if you specify an EventSource C# provider or call TraceLoggingRegister(...) without a GUID, use star (*) before your provider
        name, eg: Name="*MyEventSourceProvider" which will enable your provider appropriately.  
     2. This sample lists one EventProvider xml element and references it in a Profile with EventProviderId xml element. 
        For your component wprp, enable the required number of providers and fix the Profile xml element appropriately
    -->
        <EventProvider Id="EventProvider_SimpleTraceLoggingProvider" Name="*SimpleTraceLoggingProvider" />
        
        <Profile Id="SimpleTraceLoggingProvider.Verbose.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" LoggingMode="File" DetailLevel="Verbose">
          <Collectors>
            <EventCollectorId Value="EventCollector_SimpleTraceLoggingProvider">
              <EventProviders>
                <!-- TODO:
     1. Fix your EventProviderId with Value same as the Id attribute on EventProvider xml element above
    -->
                <EventProviderId Value="EventProvider_SimpleTraceLoggingProvider" />
              </EventProviders>
            </EventCollectorId>
          </Collectors>
        </Profile>

        <Profile Id="SimpleTraceLoggingProvider.Light.File" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="File" DetailLevel="Light" />
        <Profile Id="SimpleTraceLoggingProvider.Verbose.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Verbose" />
        <Profile Id="SimpleTraceLoggingProvider.Light.Memory" Name="SimpleTraceLoggingProvider" Description="SimpleTraceLoggingProvider" Base="SimpleTraceLoggingProvider.Verbose.File" LoggingMode="Memory" DetailLevel="Light" />

      </Profiles>
    </WindowsPerformanceRecorder>
    
    ```

    

2.  <span data-ttu-id="feb16-122">Сохраните файл с расширением. Расширение имени файла ВПРП.</span><span class="sxs-lookup"><span data-stu-id="feb16-122">Save the file with a .WPRP file name extension.</span></span>
3.  <span data-ttu-id="feb16-123">Запустите запись с помощью инструкции ЗВЧ в окне командной строки с повышенными привилегиями (Запуск от имени администратора).</span><span class="sxs-lookup"><span data-stu-id="feb16-123">Start the capture using WPR from an elevated (run as Administrator) Command Prompt window.</span></span>

    <span data-ttu-id="feb16-124">**<path to wpr>\\wpr.exe Женералпрофиле-Start Трацелоггингпровидер. впрп**</span><span class="sxs-lookup"><span data-stu-id="feb16-124">**<path to wpr>\\wpr.exe -start GeneralProfile -start TraceLoggingProvider.wprp**</span></span>

    > <span data-ttu-id="feb16-125">\[! Советы\]</span><span class="sxs-lookup"><span data-stu-id="feb16-125">\[!Tip\]</span></span>  
    > <span data-ttu-id="feb16-126">В общих целях профилирования можно также добавить **– Start женералпрофиле** в командную строку wpr.exe для записи системных событий вместе с событиями от поставщика.</span><span class="sxs-lookup"><span data-stu-id="feb16-126">For general profiling purposes, you can also add **–start GeneralProfile** to the wpr.exe command line to capture system events along with the events from your provider.</span></span> <span data-ttu-id="feb16-127">Если вы хотите собрать только события, пропустите параметр **-Start женералпрофиле**.</span><span class="sxs-lookup"><span data-stu-id="feb16-127">If you only want to gather your events, omit **-start GeneralProfile**.</span></span>

     

4.  <span data-ttu-id="feb16-128">Запустите приложение, содержащее события.</span><span class="sxs-lookup"><span data-stu-id="feb16-128">Run the application that contains your events.</span></span>
5.  <span data-ttu-id="feb16-129">Останавливает запись трассировки.</span><span class="sxs-lookup"><span data-stu-id="feb16-129">Stop the trace capture.</span></span>

    <span data-ttu-id="feb16-130">**<path to wpr>\\wpr.exe — описание Трацекаптурефиле. ETL**</span><span class="sxs-lookup"><span data-stu-id="feb16-130">**<path to wpr>\\wpr.exe -stop TraceCaptureFile.etl description**</span></span>

    > <span data-ttu-id="feb16-131">\[! Советы\]</span><span class="sxs-lookup"><span data-stu-id="feb16-131">\[!Tip\]</span></span>  
    > <span data-ttu-id="feb16-132">Если вы добавили- **Start женералпрофиле** для сбора системных событий, добавьте **wpr.exe** **женералпрофиле** в командную строку выше.</span><span class="sxs-lookup"><span data-stu-id="feb16-132">If you added **–start GeneralProfile** to gather system events, add **-stop GeneralProfile** to the **wpr.exe** command line above.</span></span>

     

### <a name="2-capture-tracelogging-events-on-windows-phone"></a><span data-ttu-id="feb16-133">2. запись событий Трацелоггинг в Windows Phone</span><span class="sxs-lookup"><span data-stu-id="feb16-133">2. Capture TraceLogging events on Windows Phone</span></span>

<span id="capturephone"></span><span id="CAPTUREPHONE"></span>

1.  <span data-ttu-id="feb16-134">Запустите tracelog, чтобы записать события от поставщика.</span><span class="sxs-lookup"><span data-stu-id="feb16-134">Start tracelog to capture events from your provider.</span></span>

    <span data-ttu-id="feb16-135">**кмдд tracelog — запустить тест-f c: \\ Test. ETL-GUID \# провидергуид**</span><span class="sxs-lookup"><span data-stu-id="feb16-135">**cmdd tracelog -start test -f c:\\test.etl -guid \#providerguid**</span></span>

2.  <span data-ttu-id="feb16-136">Запустите сценарий тестирования для записи событий в журнал.</span><span class="sxs-lookup"><span data-stu-id="feb16-136">Run your test scenario to log events.</span></span>
3.  <span data-ttu-id="feb16-137">Останавливает запись трассировки.</span><span class="sxs-lookup"><span data-stu-id="feb16-137">Stop trace capture.</span></span>

    <span data-ttu-id="feb16-138">**кмдд tracelog — завершение теста**</span><span class="sxs-lookup"><span data-stu-id="feb16-138">**cmdd tracelog -stop test**</span></span>

4.  <span data-ttu-id="feb16-139">Объедините результаты трассировки системы с результатами трассировки.</span><span class="sxs-lookup"><span data-stu-id="feb16-139">Merge the system trace results with your trace results.</span></span>

    <span data-ttu-id="feb16-140">**кмдд XPerf — слияние c: \\ Test. ETL c: \\ тестмержед. ETL**</span><span class="sxs-lookup"><span data-stu-id="feb16-140">**cmdd xperf -merge c:\\test.etl c:\\testmerged.etl**</span></span>

5.  <span data-ttu-id="feb16-141">Получите объединенный файл журнала.</span><span class="sxs-lookup"><span data-stu-id="feb16-141">Retrieve the merged log file.</span></span>

    <span data-ttu-id="feb16-142">**жетд c: \\ тестмержед. ETL**</span><span class="sxs-lookup"><span data-stu-id="feb16-142">**getd c:\\testmerged.etl**</span></span>

### <a name="3-view-tracelogging-data-using-windows-performance-analyzer"></a><span data-ttu-id="feb16-143">3. Просмотр данных Трацелоггинг с помощью анализатора производительности Windows.</span><span class="sxs-lookup"><span data-stu-id="feb16-143">3. View TraceLogging data using Windows Performance Analyzer.</span></span>

<span data-ttu-id="feb16-144">В настоящее время WPA является единственным средством просмотра, которое можно использовать для просмотра файлов трассировки Трацелоггинг (ETL).</span><span class="sxs-lookup"><span data-stu-id="feb16-144">WPA is currently the only viewer you can use to view TraceLogging trace (.etl) files.</span></span>

1.  <span data-ttu-id="feb16-145">Запустите WPA.</span><span class="sxs-lookup"><span data-stu-id="feb16-145">Start WPA.</span></span>

    <span data-ttu-id="feb16-146">**<path to wpr>\\wpa.exe Трацелоггингресултс. ETL**</span><span class="sxs-lookup"><span data-stu-id="feb16-146">**<path to wpr>\\wpa.exe traceLoggingResults.etl**</span></span>

2.  <span data-ttu-id="feb16-147">Загрузите файл трассировки (ETL), указанный в приведенной выше команде wpa.exe, например Трацелоггингресултс. ETL.</span><span class="sxs-lookup"><span data-stu-id="feb16-147">Load the trace (.etl) file that you specified in the wpa.exe command above, e.g. traceLoggingResults.etl.</span></span>
3.  <span data-ttu-id="feb16-148">Просмотр событий поставщика.</span><span class="sxs-lookup"><span data-stu-id="feb16-148">View your provider events.</span></span> <span data-ttu-id="feb16-149">В обозревателе WPA Graph разверните узел **активность системы**.</span><span class="sxs-lookup"><span data-stu-id="feb16-149">In the WPA Graph Explorer, expand **System Activity**.</span></span>
4.  <span data-ttu-id="feb16-150">Дважды щелкните на панели **Общие события** , чтобы просмотреть события на панели **анализ** .</span><span class="sxs-lookup"><span data-stu-id="feb16-150">Double-click in the **Generic Events** pane to view the events in the **Analysis** pane.</span></span>

    ![развернуть общие события](images/expandsystemactivity.png)

5.  <span data-ttu-id="feb16-152">В области анализ найдите события от поставщика, чтобы убедиться, что Трацелоггинг работает.</span><span class="sxs-lookup"><span data-stu-id="feb16-152">In the Analysis pane, locate the events from your provider to verify that TraceLogging is working.</span></span>

    <span data-ttu-id="feb16-153">В столбце **имя поставщика** таблицы **Универсальные события** найдите и выберите строку с именем поставщика.</span><span class="sxs-lookup"><span data-stu-id="feb16-153">In the **Provider Name** column of the **Generic Events** table, find and select the row with your provider name.</span></span>

    <span data-ttu-id="feb16-154">Если у вас есть несколько поставщиков для сортировки, щелкните заголовок столбца, чтобы выполнить сортировку по имени столбца, что может облегчить поиск поставщика.</span><span class="sxs-lookup"><span data-stu-id="feb16-154">If you have multiple providers to sort through, click the column header to sort by column name which may make it easier to find your provider.</span></span>

    <span data-ttu-id="feb16-155">При обнаружении поставщика щелкните правой кнопкой мыши имя и выберите пункт **Фильтр для выбора**.</span><span class="sxs-lookup"><span data-stu-id="feb16-155">When you find your provider, right click on the name and select **Filter to Selection**.</span></span>

    ![Фильтр выбора для поставщика](images/filtertoselection.png)

    <span data-ttu-id="feb16-157">Событие для Симплетрацелоггингпровидер и его значение появится в нижней области окна анализ.</span><span class="sxs-lookup"><span data-stu-id="feb16-157">The event for the SimpleTraceLoggingProvider and its value will appear in the bottom pane of the Analysis window.</span></span> <span data-ttu-id="feb16-158">Разверните имя поставщика, чтобы просмотреть события.</span><span class="sxs-lookup"><span data-stu-id="feb16-158">Expand the provider name to see the events.</span></span>

    ![Просмотр события из симплетрацелоггингпровидер](images/eventview.png)

    <span data-ttu-id="feb16-160">Дополнительные сведения об использовании WPA см. в разделе [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).</span><span class="sxs-lookup"><span data-stu-id="feb16-160">For more information about using WPA, see [Windows Performance Analyzer](/previous-versions/windows/it-pro/windows-8.1-and-8/hh448170(v=win.10)).</span></span>

## <a name="summary-and-next-steps"></a><span data-ttu-id="feb16-161">Сводка и дальнейшие действия</span><span class="sxs-lookup"><span data-stu-id="feb16-161">Summary and next steps</span></span>

<span data-ttu-id="feb16-162">Процесс записи и просмотра событий ETW с использованием ЗВЧ и WPA применяется одинаково хорошо для Трацелоггинг событий.</span><span class="sxs-lookup"><span data-stu-id="feb16-162">The process for recording and viewing ETW events using WPR and WPA apply equally well to TraceLogging events.</span></span>

<span data-ttu-id="feb16-163">Дополнительные примеры Трацелоггинг см. [в статье примеры в C/C++ трацелоггинг](tracelogging-c-cpp-tracelogging-examples.md) .</span><span class="sxs-lookup"><span data-stu-id="feb16-163">See [C/C++ Tracelogging Examples](tracelogging-c-cpp-tracelogging-examples.md) for additional TraceLogging examples.</span></span>

 

 