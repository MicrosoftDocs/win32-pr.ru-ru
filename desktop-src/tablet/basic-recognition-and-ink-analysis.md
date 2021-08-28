---
description: В этом разделе представлены API-интерфейсы анализа рукописного текста.
ms.assetid: a3126930-2802-43c7-9e98-3a73498ac3f5
title: Базовый анализ и распознавание рукописного текста
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c4bdfa0d93c25e397caf0f116f0f47b303e9571d342825673572011534404de
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111336"
---
# <a name="basic-recognition-and-ink-analysis"></a>Базовый анализ и распознавание рукописного текста

В этом разделе представлены API-интерфейсы анализа рукописного текста.

## <a name="simple-recognition"></a>Простое распознавание

Базовые функциональные возможности, предоставляемые API анализа рукописного ввода, — это доступ к результатам распознавания для определенного фрагмента рукописного ввода. Это просто и просто, как показано в следующем примере кода.


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



Результаты операции распознавания — это просто строковое значение, представляющее распознанное значение рукописного ввода. API анализа рукописного ввода предоставляет гораздо больше функций распознавания, чем просто распознанная строка, но это наиболее распространенная операция.

## <a name="incremental-recognition"></a>Добавочное распознавание

Процесс распознавания занимает некоторое время, блокируя доступ к приложению, блокируя поток пользовательского интерфейса приложения. Следовательно, это может быть дорогостоящим и неприятной для конечного пользователя для синхронного ожидания результатов. Многие приложения для планшетных ПК используют распознавание более чем нескольких строк рукописного ввода, а добавочный подход к распознаванию штрихов в фоновом потоке является оптимальной стратегией. Преимущество инкрементного подхода вместо выполнения групповой операции заключается в том, что он позволяет распознавание штрихов в течение определенного периода времени, распределять работу в фоновом потоке, а не синхронно в потоке переднего плана. Для поддержки добавочного анализа объект [**InkAnalyzer**](inkanalyzer.md) имеет метод [**баккграунданализе**](iinkanalyzer-backgroundanalyze.md) , который управляет созданием и управлением фонового потока для приложения. **InkAnalyzer** также автоматически отвечает за управление тем, что необходимо распознать и что уже было распознано.

Таким образом, существует два механизма для достижения результатов распознавания:

-   Метод [**Analyze**](iinkanalyzer-analyze.md) (синхронный анализ), который лучше подходит для:

    -   Небольшие объемы рукописного ввода.
    -   Если результаты необходимы перед переходом к следующей операции в приложении, например при отображении пользовательского интерфейса исправления.

-   Метод [**баккграунданализе**](iinkanalyzer-backgroundanalyze.md) (асинхронный анализ), который лучше подходит для:

    -   Любой объем рукописного ввода.
    -   При использовании с таймером пулсинг примерно каждые 600 миллисекунд.

> [!Note]  
> 600 миллисекунд — это текущая рекомендация, но эта продолжительность может быть изменена в ожидании дополнительного тестирования.

 

чтобы использовать операцию [**баккграунданализе**](iinkanalyzer-backgroundanalyze.md) , объект [**InkCollector**](inkcollector-class.md) (или аналогичные объекты или элементы управления, такие как [**RealTimeStylus**](realtimestylus-class.md) (RTS), [**InkOverlay**](inkoverlay-class.md)или [InkCanvas](/dotnet/api/system.windows.controls.inkcanvas?view=netcore-3.1) в Windows Presentation Foundation) управляет сбором и отрисовкой рукописных штрихов. Если объект **InkCollector** связан с API-интерфейсами анализа рукописного ввода, приложения могут обновлять результаты распознавания, [**InkAnalyzer**](inkanalyzer.md) о каждом новом штрихе, добавленном в приложение. Это позволяет **InkAnalyzer** распознавать штрихи постепенно и в фоновом потоке.

Для выполнения добавочного фонового анализа в приложениях необходимо выполнить три шага (показаны для управляемого кода):

1. При каждом вызове события [**Stroke**](inkoverlay-stroke.md) объекта [**InkOverlay**](inkoverlay-class.md) добавьте этот росчерк в [**InkAnalyzer**](inkanalyzer.md) :


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



2. Вызов операций [**баккграунданализе**](iinkanalyzer-backgroundanalyze.md) с заданным интервалом.


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
> Обратите внимание, что приложения не должны просто вызывать операцию фонового анализа после каждого нового штриха. Это приведет к сбою (возврат значения **false**), если фоновая операция уже выполняется. Причина такого поведения заключается в ограничении числа требуемых фоновых потоков и операций сверки.

 

3. Прослушивать событие [ресултсупдатед](/previous-versions/ms567607(v=vs.100)) (управляемый код) или [**результаты**](-ianalysisevents-results.md) (код C++), чтобы определить завершение фонового процесса:


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



Теперь, когда обработка рукописного ввода выполняется в фоновом потоке, приложение может принимать изменения рукописного ввода во время работы фоновой операции. Если мы используем синхронный поток, это невозможно. Работа выполняется в потоке пользовательского интерфейса и блокируется возможность внесения изменений. Изменения включают добавление в документ дополнительных рукописных данных, удаление рукописного ввода или преобразование расположения или внешнего вида существующего рукописного ввода. Изменения, происходящие во время фоновой операции, могут привести к недействительности результатов. Например, при удалении штриха из слова изменяется значение распознавания этого слова. В API [**InkAnalyzer**](inkanalyzer.md) есть встроенный процесс сверки, который автоматически определяет, какие части фоновой операции становятся недопустимыми в результате изменения рукописного ввода во время анализа.

Процесс автоматической сверки достигается из-за трех факторов:

1.  Свойство [**диртирегион**](iinkanalyzer-getdirtyregion.md) .

    -   Каждый раз, когда приложение добавляет (метод [**аддстроке**](iinkanalyzer-addstroke.md) ) или удаляет (метод [**ремовестроке**](iinkanalyzer-removestroke.md) ) штрих к [**InkAnalyzer**](inkanalyzer.md), физическое местоположение штриха захватывается и при следующем вызове операции анализа **InkAnalyzer** гарантирует, что Обводка или область, занятая этим обводкой, будет проанализирована.
    -   Когда приложение изменяет существующий рукописный ввод, изменяет расположение или изменяет другие атрибуты рисования рукописного ввода, расположение изменения (границы рукописного ввода) можно добавить в свойство [**диртирегион**](iinkanalyzer-getdirtyregion.md) объекта [**InkAnalyzer**](inkanalyzer.md). Это гарантирует, что при следующем запуске приложением операции анализа эти области проверяются на правильность результатов.
    -   Таким словами, свойство [**диртирегион**](iinkanalyzer-getdirtyregion.md) отслеживает, какие области документа и, в свою очередь, должны проверяться на предмет правильного анализа рукописного ввода и результатов распознавания, между выполнением анализа.

2.  Ограниченный анализ.

    -   Каждый раз, когда приложение вызывает операцию анализа, свойство [**диртирегион**](iinkanalyzer-getdirtyregion.md) определяет, какие штрихи необходимо проанализировать. Это позволяет операции анализа ограничить операцию только недействительными областями и игнорировать все остальные регионы, оптимизируя время, затрачиваемое на повторный анализ рукописного ввода.
    -   [**InkAnalyzer**](inkanalyzer.md) не полностью игнорирует все остальные регионы на странице, а вместо этого может проверить соседние области, чтобы определить, влияют ли изменения, внесенные в "грязном" регионе, на соседние регионы. Например, анализатор классифицирует "имеет" в следующем примере рукописного ввода как один тип **инкворд** класса [**контекстноде**](icontextnode.md) :

![рукописный текст "является"](images/b0e45d31-a0e5-4157-a345-a3a32de2566e.jpg)

Удаление "s" приводит к изменению области (отмеченной красным полем).

![рукописный ввод "i"](images/272a25a7-c730-40e6-b7d8-214ccbb85569.jpg)

После анализа анализатор изменяет классификацию "I" на тип **инкдравинг** , несмотря на то, что он находится за пределами "грязного" региона, поскольку без поддержки обводки "s" анализатор рукописного ввода имеет 50/50 вероятность того, что рукописный ввод классифицируется как рисунок или слово.

-   Внутреннее кэшированное состояние.

    -   Когда приложение вызывает операцию фонового анализа, [**InkAnalyzer**](inkanalyzer.md) кэширует моментальный снимок очистки данных. Используя моментальный снимок, **InkAnalyzer** может работать над анализом данных независимо от данных, используемых приложением, или использовать моментальный снимок в качестве точки сравнения для определения того, какие изменения были сделаны приложением во время анализа в фоновом режиме.
    -   Кэширование состояния и Сравнение изменений лучше, чем хранить список всех изменений, произошедших по одной из основных причин: прокси-сервер данных. Это расширенный сценарий, описанный далее в этом документе, но в нем предполагается, что приложение обновляет [**InkAnalyzer**](inkanalyzer.md) только с текущими рукописными и нерукописными данными перед вызываемой операцией анализа и до обработки результатов операции анализа.

## <a name="simple-ink-analysis"></a>Простой анализ рукописного ввода

В двух предыдущих сценариях (простое распознавание и последовательное распознавание) показано, как получить доступ к значениям распознавания, но не говоря о том, как получить доступ к анализу рукописного ввода или результатам классификации. Конфигурация по умолчанию для [**InkAnalyzer**](inkanalyzer.md)выполняет как алгоритмы анализа рукописного текста, так и алгоритмы распознавания. Эта конфигурация дает наиболее точные результаты, так как две технологии работают совместно для повышения точности. Это значит, что механизмы анализа рукописного ввода помогают отделить рисование от написания и нормализации повернутого текста к горизонтальной плоскости, которая является оптимальной входной плоскостью для механизмов распознавания.

Чтобы получить доступ к результатам анализа рукописного ввода, приложение использует методы [**Analyze**](iinkanalyzer-analyze.md) или [**баккграунданализе**](iinkanalyzer-backgroundanalyze.md) точно так же, как описано в двух предыдущих сценариях распознавания. Ничего не меняется, так как анализ рукописного ввода и алгоритмы распознавания уже выполняются при вызове этих методов. Однако доступ к результатам является более сложным, чем считывание значения строки. Например, в следующем образце кода показано группирование и расположение всех сегментов **инкворд** и **инкдравинг** , выполнив отрисовку прямоугольника вокруг группы штрихов, составляющих классификацию.

в этом примере просто используется событие **Paint** формы для отрисовки цветных прямоугольников вокруг слов или рисунков. Метод [**финднодесофтипе**](iinkanalyzer-findnodesoftype.md) Возвращает коллекцию объектов, которые существуют, только если была выполнена операция анализа, а результаты содержат классификации с указанным типом [**контекстноде**](icontextnode.md) . Если в документе нет **контекстноде** требуемого типа, шаги для рисования прямоугольников пропускаются.

Каждый объект, возвращаемый методом [**финднодесофтипе**](iinkanalyzer-findnodesoftype.md) , будет иметь свойства, связанные с этим типом классификации. Например, **инквордноде** ссылается на все штрихи, которые составляют одно слово в документе, и ссылаются на распознанную строку для этого слова. **Инкдравингноде** ссылается на все штрихи, составляющие один рисунок в документе, и указывает имя фигуры для этого рисунка.

Метод [**финднодесофтипе**](iinkanalyzer-findnodesoftype.md) очень похож на метод [**Дивисионресулт:: ресултбитипе**](/windows/desktop/api/msinkaut15/nf-msinkaut15-iinkdivisionresult-resultbytype) , который возвращает коллекции [**дивисионунитс**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionunits) типов для записи или рисования.


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



Чтобы перевести предыдущий пример кода в перспективу, рассмотрим следующий образец рукописного ввода:

![образец рукописного ввода "это рукописный ввод". с кругом под ним](images/f11cc578-d2eb-4246-af77-6bc768b0b91c.jpg)

При вызове метода [**финднодесофтипе**](iinkanalyzer-findnodesoftype.md) и передаче статического поля для **инкворд** анализатор Возвращает коллекцию из четырех объектов **инквордноде** :

![выходные данные анализатора «это рукописный ввод»](images/16ae768a-d97c-494e-9e3d-16bce1bcb432.jpg)

При вызове метода [**финднодесофтипе**](iinkanalyzer-findnodesoftype.md) и передаче статического поля для **инкдравинг** анализатор Возвращает коллекцию из одного объекта **инкдравингноде** :

![изображение, показывающее «овал», результат из анализатора инкдравинг](images/624b6a53-b6b9-4ccf-9bb8-c4c5629b88cf.jpg)

после запуска события **Paint** пример кода выводит прямоугольники вокруг каждого объекта:

![исходный рисунок с прямоугольниками, визуализированными вокруг объекта и слов](images/7fd9bcc3-8d7c-4cab-aa36-ba5ed78a25c0.jpg)

В этом примере используется только метод [**финднодесофтипе**](iinkanalyzer-findnodesoftype.md) , но поскольку механизмы анализа рукописного ввода могут обнаруживать более широкий набор типов рукописного ввода, метод также соответствует всем типам узлов, обнаруживаемым механизмами анализа рукописного ввода (например, строками, абзацами и другими структурами).

## <a name="using-ink-analysis-with-point-erase"></a>Использование анализа рукописного ввода с точкой стирания

Приложению необходимо внести изменения в способ обновления штрихов при выполнении пункта стирания, чтобы обеспечить хорошую производительность. Сначала на уровне приложения замените точку пера существующего штриха на точку пера нового штриха, затем вызовите [**клеарстрокедата**](iinkanalyzer-clearstrokedata.md) для этого росчерка и обновите «грязную» область с границами штриха. Это приведет к тому, что [**InkAnalyzer**](inkanalyzer.md) будет получать обновленные данные о штрихах при начале следующего цикла фонового анализа. Этот метод показан в следующем примере.


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



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Обзор анализа рукописного ввода](ink-analysis-overview.md)
</dt> <dt>

[Использование API анализа рукописного ввода](ink-analysis-api-usage.md)
</dt> </dl>

 

 
