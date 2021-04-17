---
description: В этом разделе представлены API-интерфейсы анализа рукописного текста.
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: Базовый анализ и распознавание рукописного текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9858ceedba245a733d4dc0055dd0747507654f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423509"
---
# <a name="basic-recognition-and-ink-analysis"></a><span data-ttu-id="fdcf7-103">Базовый анализ и распознавание рукописного текста</span><span class="sxs-lookup"><span data-stu-id="fdcf7-103">Basic Recognition and Ink Analysis</span></span>

<span data-ttu-id="fdcf7-104">В этом разделе представлены API-интерфейсы анализа рукописного текста.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-104">This topic introduces the Ink Analysis APIs.</span></span>

## <a name="simple-recognition"></a><span data-ttu-id="fdcf7-105">Простое распознавание</span><span class="sxs-lookup"><span data-stu-id="fdcf7-105">Simple Recognition</span></span>

<span data-ttu-id="fdcf7-106">Базовые функциональные возможности, предоставляемые API анализа рукописного ввода, — это доступ к результатам распознавания для определенного фрагмента рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-106">The basic functionality exposed by the ink analysis API is access to the recognition results for a given piece of ink.</span></span> <span data-ttu-id="fdcf7-107">Это просто и просто, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-107">This is straightforward and simple to do, as shown in the following example code.</span></span>


```C++
// Instantiate a new InkAnalyzer object, passing in an Ink object and
// the synchronizing object.
InkAnalyzer ia = new InkAnalyzer(myInkOverlay.Ink, this);

// Associate the Strokes to be recognized with the InkAnalyzer.
ia.AddStrokes(myInkOverlay.Ink.Strokes);

// Synchronously recognize the Strokes.
ia.Analyze();

// Access the results and display.
string myResults = ia.GetRecognizedString();
MessageBox.Show(myResults);
```



<span data-ttu-id="fdcf7-108">Результаты операции распознавания — это просто строковое значение, представляющее распознанное значение рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-108">The results of the recognition operation are simply a string value representing the recognized value of the handwritten ink.</span></span> <span data-ttu-id="fdcf7-109">API анализа рукописного ввода предоставляет гораздо больше функций распознавания, чем просто распознанная строка, но это наиболее распространенная операция.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-109">The ink analysis API exposes much more recognition functionality than just the recognized string, but that is the most common operation.</span></span>

## <a name="incremental-recognition"></a><span data-ttu-id="fdcf7-110">Добавочное распознавание</span><span class="sxs-lookup"><span data-stu-id="fdcf7-110">Incremental Recognition</span></span>

<span data-ttu-id="fdcf7-111">Процесс распознавания занимает некоторое время, блокируя доступ к приложению, блокируя поток пользовательского интерфейса приложения.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-111">The recognition process takes time to complete, blocking access to the application by blocking the application's UI thread.</span></span> <span data-ttu-id="fdcf7-112">Следовательно, это может быть дорогостоящим и неприятной для конечного пользователя для синхронного ожидания результатов.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-112">It can therefore be costly and frustrating to the end-user to wait synchronously for results.</span></span> <span data-ttu-id="fdcf7-113">Многие приложения для планшетных ПК используют распознавание более чем нескольких строк рукописного ввода, а добавочный подход к распознаванию штрихов в фоновом потоке является оптимальной стратегией.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-113">Many Tablet PC applications require the recognition of more than a few lines of ink, and an incremental approach to recognizing strokes on a background thread is the optimal strategy.</span></span> <span data-ttu-id="fdcf7-114">Преимущество инкрементного подхода вместо выполнения групповой операции заключается в том, что он позволяет распознавание штрихов в течение определенного периода времени, распределять работу в фоновом потоке, а не синхронно в потоке переднего плана.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-114">The advantage of an incremental approach instead of a bulk operation is that it allows the recognition of the strokes to happen over a period of time, spreading out the work on the background thread instead of synchronously on the foreground thread.</span></span> <span data-ttu-id="fdcf7-115">Для поддержки добавочного анализа объект [**InkAnalyzer**](inkanalyzer.md) имеет метод [**баккграунданализе**](iinkanalyzer-backgroundanalyze.md) , который управляет созданием и управлением фонового потока для приложения.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-115">To support incremental analysis, the [**InkAnalyzer**](inkanalyzer.md) object has a [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method, which handles the creation and management of a background thread for the application.</span></span> <span data-ttu-id="fdcf7-116">**InkAnalyzer** также автоматически отвечает за управление тем, что необходимо распознать и что уже было распознано.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-116">The **InkAnalyzer** also automatically takes care of managing what needs to be recognized and what has already been recognized.</span></span>

<span data-ttu-id="fdcf7-117">Таким образом, существует два механизма для достижения результатов распознавания:</span><span class="sxs-lookup"><span data-stu-id="fdcf7-117">Thus, there are two mechanisms for attaining recognition results:</span></span>

-   <span data-ttu-id="fdcf7-118">Метод [**Analyze**](iinkanalyzer-analyze.md) (синхронный анализ), который лучше подходит для:</span><span class="sxs-lookup"><span data-stu-id="fdcf7-118">The [**Analyze**](iinkanalyzer-analyze.md) method (synchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="fdcf7-119">Небольшие объемы рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-119">Small amounts of ink.</span></span>
    -   <span data-ttu-id="fdcf7-120">Если результаты необходимы перед переходом к следующей операции в приложении, например при отображении пользовательского интерфейса исправления.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-120">When results are required before proceeding to the next operation in the application, such as when displaying a correction user interface.</span></span>

-   <span data-ttu-id="fdcf7-121">Метод [**баккграунданализе**](iinkanalyzer-backgroundanalyze.md) (асинхронный анализ), который лучше подходит для:</span><span class="sxs-lookup"><span data-stu-id="fdcf7-121">The [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) method (asynchronous analysis), which works best for:</span></span>

    -   <span data-ttu-id="fdcf7-122">Любой объем рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-122">Any amount of ink.</span></span>
    -   <span data-ttu-id="fdcf7-123">При использовании с таймером пулсинг примерно каждые 600 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-123">When utilized with a timer pulsing approximately every 600 milliseconds.</span></span>

> [!Note]  
> <span data-ttu-id="fdcf7-124">600 миллисекунд — это текущая рекомендация, но эта продолжительность может быть изменена в ожидании дополнительного тестирования.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-124">600 milliseconds is the current recommendation, but this timing is subject to change pending further testing.</span></span>

 

<span data-ttu-id="fdcf7-125">Чтобы использовать операцию [**баккграунданализе**](iinkanalyzer-backgroundanalyze.md) , объект [**InkCollector**](inkcollector-class.md) (или аналогичные объекты или элементы управления, такие как [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md)или [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) в Windows Presentation Foundation) управляет сбором и отрисовкой рукописных штрихов.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-125">To use the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operation, the [**InkCollector**](inkcollector-class.md) object (or similar objects or controls such as the [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md), or [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) in Windows Presentation Foundation) manages the collection and rendering of the ink strokes.</span></span> <span data-ttu-id="fdcf7-126">Если объект **InkCollector** связан с API-интерфейсами анализа рукописного ввода, приложения могут обновлять результаты распознавания, [**InkAnalyzer**](inkanalyzer.md) о каждом новом штрихе, добавленном в приложение.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-126">If the **InkCollector** is paired with the ink analysis APIs, applications can keep the recognition results updated by informing the [**InkAnalyzer**](inkanalyzer.md) about each new stroke added to the application.</span></span> <span data-ttu-id="fdcf7-127">Это позволяет **InkAnalyzer** распознавать штрихи постепенно и в фоновом потоке.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-127">This allows for the **InkAnalyzer** to recognize the strokes incrementally and on a background thread.</span></span>

<span data-ttu-id="fdcf7-128">Для выполнения добавочного фонового анализа в приложениях необходимо выполнить три шага (показаны для управляемого кода):</span><span class="sxs-lookup"><span data-stu-id="fdcf7-128">To accomplish incremental background analysis, applications need to implement three steps (shown for managed code):</span></span>

1. <span data-ttu-id="fdcf7-129">При каждом вызове события [**Stroke**](inkoverlay-stroke.md) объекта [**InkOverlay**](inkoverlay-class.md) добавьте этот росчерк в [**InkAnalyzer**](inkanalyzer.md) :</span><span class="sxs-lookup"><span data-stu-id="fdcf7-129">Add the stroke to the [**InkAnalyzer**](inkanalyzer.md) whenever the [**InkOverlay**](inkoverlay-class.md) object's [**Stroke**](inkoverlay-stroke.md) event is raised:</span></span>


```C++
/// Event Handler from InkOverlay's Stroke event
/// This event is fired when a new stroke is drawn. 
/// In this case, it is necessary to update the ink analyzer's 
/// Strokes collection. The event is fired even when the eraser 
/// stroke is created.
/// The event handler must filter out the eraser strokes.
/// <param name="sender">The control that raised the event.</param>
/// <param name="e">The event arguments.</param>
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
{
        // Add the new stroke to the InkAnalyzer's stroke collection
        theInkAnalyzer.AddStroke(e.Stroke);
        this.Refresh();
}
```



2. <span data-ttu-id="fdcf7-130">Вызов операций [**баккграунданализе**](iinkanalyzer-backgroundanalyze.md) с заданным интервалом.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-130">Invoke the [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) operations at a set interval.</span></span>


```C++
//Setup a timer tick handler
private System.Windows.Forms.Timer analysisTimer;
analysisTimer = new Timer();
analysisTimer.Tick += new System.EventHandler(this.analysisTimer_Tick);

// The timer is enabled and set to tick every 600 milliseconds.
analysisTimer.Enabled = true;
analysisTimer.Interval = 600;
// ...
//The background analysis operation is invoked with every tick
private void analysisTimer_Tick(object sender, System.EventArgs e)
{
    theInkAnalyzer.BackgroundAnalyze();
}
```



> [!Note]  
> <span data-ttu-id="fdcf7-131">Обратите внимание, что приложения не должны просто вызывать операцию фонового анализа после каждого нового штриха.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-131">Note Applications should not simply invoke the background analysis operation after every new stroke.</span></span> <span data-ttu-id="fdcf7-132">Это приведет к сбою (возврат значения **false**), если фоновая операция уже выполняется.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-132">This will fail (returning a value of **false**) if a background operation is already running.</span></span> <span data-ttu-id="fdcf7-133">Причина такого поведения заключается в ограничении числа требуемых фоновых потоков и операций сверки.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-133">The reason for this behavior is to limit the number of background threads and reconciliation operations required.</span></span>

 

3. <span data-ttu-id="fdcf7-134">Прослушивать событие [ресултсупдатед](/previous-versions/ms567607(v=vs.100)) (управляемый код) или [**результаты**](-ianalysisevents-results.md) (код C++), чтобы определить завершение фонового процесса:</span><span class="sxs-lookup"><span data-stu-id="fdcf7-134">Listen for the [ResultsUpdated](/previous-versions/ms567607(v=vs.100)) event (managed code) or [**Results**](-ianalysisevents-results.md) event (C++ code) to determine when the background process has finished:</span></span>


```C++
// ...
theInkAnalyzer.Results += new ResultsEventHandler(ia_Results);
// ...

private void ia_Results(object sender, ResultsEventArgs e)
{
    String myResults = e.InkAnalyzer.GetRecognizedString();
    MessageBox.Show(myResults);
}
```



<span data-ttu-id="fdcf7-135">Теперь, когда обработка рукописного ввода выполняется в фоновом потоке, приложение может принимать изменения рукописного ввода во время работы фоновой операции.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-135">Now that the processing of the ink is being done on a background thread, the application has the ability to accept changes to the ink while the background operation is working.</span></span> <span data-ttu-id="fdcf7-136">Если мы используем синхронный поток, это невозможно.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-136">If we use a synchronous thread this is not possible.</span></span> <span data-ttu-id="fdcf7-137">Работа выполняется в потоке пользовательского интерфейса и блокируется возможность внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-137">The work executes on the UI thread, blocking the ability to make changes.</span></span> <span data-ttu-id="fdcf7-138">Изменения включают добавление в документ дополнительных рукописных данных, удаление рукописного ввода или преобразование расположения или внешнего вида существующего рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-138">Changes include adding more ink to the document, deleting ink, or transforming the location or appearance of the existing ink.</span></span> <span data-ttu-id="fdcf7-139">Изменения, происходящие во время фоновой операции, могут привести к недействительности результатов.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-139">Changes that occur during the background operation may in fact invalidate the results.</span></span> <span data-ttu-id="fdcf7-140">Например, при удалении штриха из слова изменяется значение распознавания этого слова.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-140">For example, deleting a stroke from a word changes the recognition value of that word.</span></span> <span data-ttu-id="fdcf7-141">В API [**InkAnalyzer**](inkanalyzer.md) есть встроенный процесс сверки, который автоматически определяет, какие части фоновой операции становятся недопустимыми в результате изменения рукописного ввода во время анализа.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-141">The [**InkAnalyzer**](inkanalyzer.md) API has a built-in reconciliation process that automatically determines what parts of the background operation become invalid as the result of the ink changing while analyzing.</span></span>

<span data-ttu-id="fdcf7-142">Процесс автоматической сверки достигается из-за трех факторов:</span><span class="sxs-lookup"><span data-stu-id="fdcf7-142">The automatic reconciliation process is accomplished because of three factors:</span></span>

1.  <span data-ttu-id="fdcf7-143">Свойство [**диртирегион**](iinkanalyzer-getdirtyregion.md) .</span><span class="sxs-lookup"><span data-stu-id="fdcf7-143">The [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property.</span></span>

    -   <span data-ttu-id="fdcf7-144">Каждый раз, когда приложение добавляет (метод [**аддстроке**](iinkanalyzer-addstroke.md) ) или удаляет (метод [**ремовестроке**](iinkanalyzer-removestroke.md) ) штрих к [**InkAnalyzer**](inkanalyzer.md), физическое местоположение штриха захватывается и при следующем вызове операции анализа **InkAnalyzer** гарантирует, что Обводка или область, занятая этим обводкой, будет проанализирована.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-144">Each time the application adds ([**AddStroke**](iinkanalyzer-addstroke.md) method) or removes ([**RemoveStroke**](iinkanalyzer-removestroke.md) method) a stroke to or from the [**InkAnalyzer**](inkanalyzer.md), the physical location of the stroke is captured and the next time an analysis operation is invoked, the **InkAnalyzer** ensures that stroke, or the area occupied by that stroke, is analyzed.</span></span>
    -   <span data-ttu-id="fdcf7-145">Когда приложение изменяет существующий рукописный ввод, изменяет расположение или изменяет другие атрибуты рисования рукописного ввода, расположение изменения (границы рукописного ввода) можно добавить в свойство [**диртирегион**](iinkanalyzer-getdirtyregion.md) объекта [**InkAnalyzer**](inkanalyzer.md).</span><span class="sxs-lookup"><span data-stu-id="fdcf7-145">Whenever the application modifies existing ink, changes the location, or changes other drawing attributes of the ink, the location of the change (the bounds of the ink) can be added to the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property of the [**InkAnalyzer**](inkanalyzer.md).</span></span> <span data-ttu-id="fdcf7-146">Это гарантирует, что при следующем запуске приложением операции анализа эти области проверяются на правильность результатов.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-146">This ensures that the next time the application starts the analysis operation those areas are checked for correct results.</span></span>
    -   <span data-ttu-id="fdcf7-147">Таким словами, свойство [**диртирегион**](iinkanalyzer-getdirtyregion.md) отслеживает, какие области документа и, в свою очередь, должны проверяться на предмет правильного анализа рукописного ввода и результатов распознавания, между выполнением анализа.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-147">Thus, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property keeps track, between analysis runs, of what areas of the document and-in turn-which strokes need to be checked for correct ink analysis and recognition results.</span></span>

2.  <span data-ttu-id="fdcf7-148">Ограниченный анализ.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-148">Limited analysis.</span></span>

    -   <span data-ttu-id="fdcf7-149">Каждый раз, когда приложение вызывает операцию анализа, свойство [**диртирегион**](iinkanalyzer-getdirtyregion.md) определяет, какие штрихи необходимо проанализировать.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-149">Each time the application invokes the analysis operation, the [**DirtyRegion**](iinkanalyzer-getdirtyregion.md) property identifies which strokes need to be analyzed.</span></span> <span data-ttu-id="fdcf7-150">Это позволяет операции анализа ограничить операцию только недействительными областями и игнорировать все остальные регионы, оптимизируя время, затрачиваемое на повторный анализ рукописного ввода.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-150">This allows the analysis operation to limit the operation to only the dirty regions and ignore all other regions, optimizing the amount of time spent re-analyzing ink.</span></span>
    -   <span data-ttu-id="fdcf7-151">[**InkAnalyzer**](inkanalyzer.md) не полностью игнорирует все остальные регионы на странице, а вместо этого может проверить соседние области, чтобы определить, влияют ли изменения, внесенные в "грязном" регионе, на соседние регионы.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-151">The [**InkAnalyzer**](inkanalyzer.md) does not completely ignore all other regions on the page, but instead may examine neighboring areas to determine if the changes made in the dirty region affect those neighboring regions.</span></span> <span data-ttu-id="fdcf7-152">Например, анализатор классифицирует "имеет" в следующем примере рукописного ввода как один тип **инкворд** класса [**контекстноде**](icontextnode.md) :</span><span class="sxs-lookup"><span data-stu-id="fdcf7-152">For example, the analyzer classifies "Is", in the following ink sample, as a single **InkWord** type of the [**ContextNode**](icontextnode.md) class:</span></span>

![рукописный текст "является"](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

<span data-ttu-id="fdcf7-154">Удаление "s" приводит к изменению области (отмеченной красным полем).</span><span class="sxs-lookup"><span data-stu-id="fdcf7-154">Deleting the "s" results in a dirty region (marked with a red box).</span></span>

![рукописный ввод "i"](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

<span data-ttu-id="fdcf7-156">После анализа анализатор изменяет классификацию "I" на тип **инкдравинг** , несмотря на то, что он находится за пределами "грязного" региона, поскольку без поддержки обводки "s" анализатор рукописного ввода имеет 50/50 вероятность того, что рукописный ввод классифицируется как рисунок или слово.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-156">After analysis, the analyzer changes the classification for the "I" to an **InkDrawing** type, even though it is outside of the dirty region, because without the supporting "s" stroke the ink analyzer has a 50/50 chance of the ink being classified as a drawing or a word.</span></span>

-   <span data-ttu-id="fdcf7-157">Внутреннее кэшированное состояние.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-157">Internally cached state.</span></span>

    -   <span data-ttu-id="fdcf7-158">Когда приложение вызывает операцию фонового анализа, [**InkAnalyzer**](inkanalyzer.md) кэширует моментальный снимок очистки данных.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-158">When an application invokes a background analysis operation the [**InkAnalyzer**](inkanalyzer.md) caches a snapshot of the pruned data.</span></span> <span data-ttu-id="fdcf7-159">Используя моментальный снимок, **InkAnalyzer** может работать над анализом данных независимо от данных, используемых приложением, или использовать моментальный снимок в качестве точки сравнения для определения того, какие изменения были сделаны приложением во время анализа в фоновом режиме.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-159">By taking a snapshot the **InkAnalyzer** can either work on analyzing the data independently of the data being used by the application, or use the snapshot as the comparison point to determine what changes were made by the application while background analyzing.</span></span>
    -   <span data-ttu-id="fdcf7-160">Кэширование состояния и Сравнение изменений лучше, чем хранить список всех изменений, произошедших по одной из основных причин: прокси-сервер данных.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-160">Caching the state and comparing changes is better than keeping a list of all changes that occurred for one primary reason: data proxy.</span></span> <span data-ttu-id="fdcf7-161">Это расширенный сценарий, описанный далее в этом документе, но в нем предполагается, что приложение обновляет [**InkAnalyzer**](inkanalyzer.md) только с текущими рукописными и нерукописными данными перед вызываемой операцией анализа и до обработки результатов операции анализа.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-161">This is an advanced scenario described later in this document, but it involves the application updating the [**InkAnalyzer**](inkanalyzer.md) with only the current ink and non-ink data prior to the invoked analysis operation and prior to processing the results of an analysis operation.</span></span>

## <a name="simple-ink-analysis"></a><span data-ttu-id="fdcf7-162">Простой анализ рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="fdcf7-162">Simple Ink Analysis</span></span>

<span data-ttu-id="fdcf7-163">В двух предыдущих сценариях (простое распознавание и последовательное распознавание) показано, как получить доступ к значениям распознавания, но не говоря о том, как получить доступ к анализу рукописного ввода или результатам классификации.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-163">The previous two scenarios (simple recognition and incremental recognition) outline how to access recognition values but do not mention how to access the ink analysis or classification results.</span></span> <span data-ttu-id="fdcf7-164">Конфигурация по умолчанию для [**InkAnalyzer**](inkanalyzer.md)выполняет как алгоритмы анализа рукописного текста, так и алгоритмы распознавания.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-164">The default configuration of the [**InkAnalyzer**](inkanalyzer.md), runs both ink analysis algorithms and recognition algorithms.</span></span> <span data-ttu-id="fdcf7-165">Эта конфигурация дает наиболее точные результаты, так как две технологии работают совместно для повышения точности.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-165">This configuration yields the most accurate results, because the two technologies work together to increase accuracy.</span></span> <span data-ttu-id="fdcf7-166">Это значит, что механизмы анализа рукописного ввода помогают отделить рисование от написания и нормализации повернутого текста к горизонтальной плоскости, которая является оптимальной входной плоскостью для механизмов распознавания.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-166">That is, the ink analysis engines help to separate the drawing from the writing and normalize angled writing into a horizontal plane, which is the optimum input plane for the recognition engines.</span></span>

<span data-ttu-id="fdcf7-167">Чтобы получить доступ к результатам анализа рукописного ввода, приложение использует методы [**Analyze**](iinkanalyzer-analyze.md) или [**баккграунданализе**](iinkanalyzer-backgroundanalyze.md) точно так же, как описано в двух предыдущих сценариях распознавания.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-167">To access the ink analysis results, your application uses the [**Analyze**](iinkanalyzer-analyze.md) or [**BackgroundAnalyze**](iinkanalyzer-backgroundanalyze.md) methods exactly as described in the previous two recognition scenarios.</span></span> <span data-ttu-id="fdcf7-168">Ничего не меняется, так как анализ рукописного ввода и алгоритмы распознавания уже выполняются при вызове этих методов.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-168">Nothing changes because the ink analysis and recognition algorithms are already being run when those methods are called.</span></span> <span data-ttu-id="fdcf7-169">Однако доступ к результатам является более сложным, чем считывание значения строки.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-169">However, accessing the results is more complicated than reading the value of a string.</span></span> <span data-ttu-id="fdcf7-170">Например, в следующем образце кода показано группирование и расположение всех сегментов **инкворд** и **инкдравинг** , выполнив отрисовку прямоугольника вокруг группы штрихов, составляющих классификацию.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-170">As an example, the following code sample shows the grouping and locations of all the **InkWord** segments and **InkDrawing** segments by rendering a rectangle around the group of strokes that make up the classification.</span></span>

<span data-ttu-id="fdcf7-171">В этом примере просто используется событие **рисования** формы для отрисовки цветных прямоугольников вокруг слов или рисунков.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-171">This example simply uses the form's **Paint** event to render colored rectangles around the words or drawings.</span></span> <span data-ttu-id="fdcf7-172">Метод [**финднодесофтипе**](iinkanalyzer-findnodesoftype.md) Возвращает коллекцию объектов, которые существуют, только если была выполнена операция анализа, а результаты содержат классификации с указанным типом [**контекстноде**](icontextnode.md) .</span><span class="sxs-lookup"><span data-stu-id="fdcf7-172">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method returns a collection of objects that exists only if the analysis operation has been executed and the results contain classifications with the specified [**ContextNode**](icontextnode.md) type.</span></span> <span data-ttu-id="fdcf7-173">Если в документе нет **контекстноде** требуемого типа, шаги для рисования прямоугольников пропускаются.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-173">If no **ContextNode** of the desired type exists in the document, the steps to draw the rectangles are skipped.</span></span>

<span data-ttu-id="fdcf7-174">Каждый объект, возвращаемый методом [**финднодесофтипе**](iinkanalyzer-findnodesoftype.md) , будет иметь свойства, связанные с этим типом классификации.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-174">Each object returned from the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method will have properties that relate to that kind of classification.</span></span> <span data-ttu-id="fdcf7-175">Например, **инквордноде** ссылается на все штрихи, которые составляют одно слово в документе, и ссылаются на распознанную строку для этого слова.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-175">For example the **InkWordNode** references all the strokes that make up a single word in the document and reference the recognized string for that word.</span></span> <span data-ttu-id="fdcf7-176">**Инкдравингноде** ссылается на все штрихи, составляющие один рисунок в документе, и указывает имя фигуры для этого рисунка.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-176">The **InkDrawingNode** references all the strokes that make up the single drawing in the document and reference the shape name for that drawing.</span></span>

<span data-ttu-id="fdcf7-177">Метод [**финднодесофтипе**](iinkanalyzer-findnodesoftype.md) очень похож на метод [**Дивисионресулт:: ресултбитипе**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) , который возвращает коллекции [**дивисионунитс**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) типов для записи или рисования.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-177">The [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method is very similar to the [**DivisionResult::ResultByType**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) method that returned collections of [**DivisionUnits**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) of either writing or drawing types.</span></span>


```C++
private void Form1_Paint(object sender, PaintEventArgs e)
{
    //Setup the pen to draw
    using(Pen penBox = new Pen(Color.Red, 1))
    {
        // Find all the InkWord ContextNodes in the results
        ContextNodeCollection InkWordNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkWord);
        // For each InkWord node found, cast the ContextNode to a type specific
        // "InkWordNode" to easily access the rotated bounding box property.
        foreach (ContextNode InkWord in InkWordNodes)
        {
            //Draw the rotated bounding box.
            e.Graphics.DrawPolygon(penBox,
                    ((InkWordNode)InkWord).GetRotatedBoundingBox());
        }

        // Find all the InkDrawing ContextNodes in the results
        ContextNodeBaseCollection InkDrawingNodes = theInkAnalyzer.FindNodesOfType(ContextNodeType.InkDrawing);

        penBox.Color = Color.Green;

        // For each InkDrawing node found, access the node's location property to
        // draw a rectangle around the drawing.
        foreach (ContextNode InkDrawing in InkDrawingNodes)
        {
            e.Graphics.DrawRectangle(penBox, InkDrawing.Location.GetBounds());
        }
    }
}
```



<span data-ttu-id="fdcf7-178">Чтобы перевести предыдущий пример кода в перспективу, рассмотрим следующий образец рукописного ввода:</span><span class="sxs-lookup"><span data-stu-id="fdcf7-178">To put the previous code example into perspective, consider the following ink sample:</span></span>

![образец рукописного ввода "это рукописный ввод".](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

<span data-ttu-id="fdcf7-181">При вызове метода [**финднодесофтипе**](iinkanalyzer-findnodesoftype.md) и передаче статического поля для **инкворд** анализатор Возвращает коллекцию из четырех объектов **инквордноде** :</span><span class="sxs-lookup"><span data-stu-id="fdcf7-181">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkWord**, the analyzer returns a collection of four **InkWordNode** objects:</span></span>

![выходные данные анализатора «это рукописный ввод»](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

<span data-ttu-id="fdcf7-183">При вызове метода [**финднодесофтипе**](iinkanalyzer-findnodesoftype.md) и передаче статического поля для **инкдравинг** анализатор Возвращает коллекцию из одного объекта **инкдравингноде** :</span><span class="sxs-lookup"><span data-stu-id="fdcf7-183">If you call the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method and pass in the static field for **InkDrawing**, the analyzer returns a collection of one **InkDrawingNode** object:</span></span>

![изображение, показывающее «овал», результат из анализатора инкдравинг](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

<span data-ttu-id="fdcf7-185">После запуска события **Paint** образец кода выводит прямоугольники вокруг каждого объекта:</span><span class="sxs-lookup"><span data-stu-id="fdcf7-185">After the **Paint** event has fired, the sample code renders rectangles around each of the objects:</span></span>

![исходный рисунок с прямоугольниками, визуализированными вокруг объекта и слов](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

<span data-ttu-id="fdcf7-187">В этом примере используется только метод [**финднодесофтипе**](iinkanalyzer-findnodesoftype.md) , но поскольку механизмы анализа рукописного ввода могут обнаруживать более широкий набор типов рукописного ввода, метод также соответствует всем типам узлов, обнаруживаемым механизмами анализа рукописного ввода (например, строками, абзацами и другими структурами).</span><span class="sxs-lookup"><span data-stu-id="fdcf7-187">This example only touches on the [**FindNodesOfType**](iinkanalyzer-findnodesoftype.md) method, but because the ink analysis engines can detect a richer set of ink types, the method also correspond to all types of nodes detectable by the ink analysis engines (such as lines, paragraphs, and other structures).</span></span>

## <a name="using-ink-analysis-with-point-erase"></a><span data-ttu-id="fdcf7-188">Использование анализа рукописного ввода с точкой стирания</span><span class="sxs-lookup"><span data-stu-id="fdcf7-188">Using Ink Analysis with Point Erase</span></span>

<span data-ttu-id="fdcf7-189">Приложению необходимо внести изменения в способ обновления штрихов при выполнении пункта стирания, чтобы обеспечить хорошую производительность.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-189">Your application needs to make adjustments in the way it updates strokes when performing point erase to ensure good performance.</span></span> <span data-ttu-id="fdcf7-190">Сначала на уровне приложения замените точку пера существующего штриха на точку пера нового штриха, затем вызовите [**клеарстрокедата**](iinkanalyzer-clearstrokedata.md) для этого росчерка и обновите «грязную» область с границами штриха.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-190">Firstly, at the application layer, replace the stylus point of the existing Stroke with the stylus point of the new stroke, then call [**ClearStrokeData**](iinkanalyzer-clearstrokedata.md) on that stroke and update the dirty region with the stroke's bounds.</span></span> <span data-ttu-id="fdcf7-191">Это приведет к тому, что [**InkAnalyzer**](inkanalyzer.md) будет получать обновленные данные о штрихах при начале следующего цикла фонового анализа.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-191">This will cause the [**InkAnalyzer**](inkanalyzer.md) to fetch the updated stroke data when the next round of background analysis starts.</span></span> <span data-ttu-id="fdcf7-192">Этот метод показан в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="fdcf7-192">This technique is demonstrated in the following example.</span></span>


```C++
using System;
using System.Diagnostics;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;

class PointEraseAnalysisSample : Application
{
  InkAnalyzer _analyzer;
  InkCanvas _canvas;
  bool _isPointErasing = false;
  bool _strokesManipulated = false;

  protected override void OnStartup(StartupEventArgs e)
  {
      base.OnStartup(e);
      Window win = new Window();

      _canvas = new InkCanvas();
      _canvas.Background = new LinearGradientBrush(Colors.Yellow, Colors.LightYellow, 60d);
      _canvas.EditingModeInverted = InkCanvasEditingMode.EraseByPoint;
      _canvas.Strokes.StrokesChanged += new StrokeCollectionChangedEventHandler(Strokes_StrokesChanged);
      _canvas.AddHandler(InkCanvas.MouseUpEvent, new MouseButtonEventHandler(_canvas_MouseUp), true);

      _analyzer = new InkAnalyzer(this.Dispatcher);
      _analyzer.ResultsUpdated += new ResultsUpdatedEventHandler(_analyzer_ResultsUpdated);

      win.Content = _canvas;
      win.Show();
  }

  void _analyzer_ResultsUpdated(object sender, ResultsUpdatedEventArgs e)
  {
      if (!_analyzer.DirtyRegion.IsEmpty)
      {
          _analyzer.BackgroundAnalyze();
          return;
      }

      Console.WriteLine(_analyzer.GetRecognizedString());
  }

  void _canvas_MouseUp(object sender, MouseButtonEventArgs e)
  {
      if (_isPointErasing)
      {
          _isPointErasing = false;
          _analyzer.BackgroundAnalyze();
      }
  }

  void Strokes_StrokesChanged(object sender, StrokeCollectionChangedEventArgs e)
  {
      if (_strokesManipulated)
      {
          // ignore StrokesChanged if we changed them ourselves
          _strokesManipulated = false;
          return;
      }

      if (_canvas.ActiveEditingMode == InkCanvasEditingMode.EraseByPoint &&
          e.Added.Count == 1 && e.Removed.Count == 1)
      {
          // set flag so we call BackgroundAnalyze in MouseUp
          _isPointErasing = true;

          // set flag so we ignore the next StrokesChanged
          _strokesManipulated = true;

          // replace the stylus points on the removed stroke with the added stroke
          e.Removed[0].StylusPoints = e.Added[0].StylusPoints;
          
          // force IA to update the stroke data for the removed stroke
          _analyzer.ClearStrokeData(e.Removed[0]);

          // replace the added stroke with the updated removed stroke back into InkCanvas
          _canvas.Strokes.Replace(e.Added[0], new StrokeCollection(new Stroke[] {e.Removed[0]})); 
          
          return;
      }

      if (e.Added.Count > 0)
      {
          _analyzer.AddStrokes(e.Added);
      }

      if (e.Removed.Count > 0)
      {
          _analyzer.RemoveStrokes(e.Removed);
      }

      _analyzer.BackgroundAnalyze();
  }

  [STAThread]
  static void Main(string[] args)
  {
      new PointEraseAnalysisSample().Run();
  }
}
```



## <a name="related-topics"></a><span data-ttu-id="fdcf7-193">См. также</span><span class="sxs-lookup"><span data-stu-id="fdcf7-193">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdcf7-194">Обзор анализа рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="fdcf7-194">Ink Analysis Overview</span></span>](ink-analysis-overview.md)
</dt> <dt>

[<span data-ttu-id="fdcf7-195">Использование API анализа рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="fdcf7-195">Ink Analysis API Usage</span></span>](ink-analysis-api-usage.md)
</dt> </dl>

 

 
