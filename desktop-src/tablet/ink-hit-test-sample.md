---
description: В этом примере показаны два метода поиска рукописного ввода по заданному положению экрана.
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: Пример проверки нажатия рукописного ввода
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d25e6cbc0ed471384bea0cc1977dd38d3ae4830
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710990"
---
# <a name="ink-hit-test-sample"></a><span data-ttu-id="63239-103">Пример проверки нажатия рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="63239-103">Ink Hit Test Sample</span></span>

<span data-ttu-id="63239-104">В этом примере показаны два метода поиска рукописного ввода по заданному положению экрана.</span><span class="sxs-lookup"><span data-stu-id="63239-104">This sample illustrates two methods to find ink, given a screen location.</span></span>

<span data-ttu-id="63239-105">В этом примере используются следующие функции.</span><span class="sxs-lookup"><span data-stu-id="63239-105">The following features are used in this sample:</span></span>

-   <span data-ttu-id="63239-106">Использование сборщика рукописных данных</span><span class="sxs-lookup"><span data-stu-id="63239-106">Using an ink collector</span></span>
-   <span data-ttu-id="63239-107">Выполнение проверки нажатия</span><span class="sxs-lookup"><span data-stu-id="63239-107">Performing a hit test</span></span>
-   <span data-ttu-id="63239-108">Поиск ближайшей точки</span><span class="sxs-lookup"><span data-stu-id="63239-108">Locating the nearest point</span></span>

## <a name="accessing-the-ink-api"></a><span data-ttu-id="63239-109">Доступ к API рукописного ввода</span><span class="sxs-lookup"><span data-stu-id="63239-109">Accessing the Ink API</span></span>

<span data-ttu-id="63239-110">Во-первых, сослаться на классы планшетных ПК, которые находятся в пакете SDK для Windows Vista или Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="63239-110">First, reference the Tablet PC classes, located in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a><span data-ttu-id="63239-111">Обработка событий загрузки и рисования форм</span><span class="sxs-lookup"><span data-stu-id="63239-111">Handling Form Load and Paint Events</span></span>

<span data-ttu-id="63239-112">Обработчик событий загрузки формы:</span><span class="sxs-lookup"><span data-stu-id="63239-112">The form's Load event handler:</span></span>

-   <span data-ttu-id="63239-113">Создает объект [InkCollector](/previous-versions/ms583683(v=vs.100)) (IC) для формы.</span><span class="sxs-lookup"><span data-stu-id="63239-113">Creates an [InkCollector](/previous-versions/ms583683(v=vs.100)) object, ic, for the form.</span></span>
-   <span data-ttu-id="63239-114">Задает для свойства [режиме CollectionMode](/previous-versions/ms836497(v=msdn.10)) объекта [InkCollector](/previous-versions/ms583683(v=vs.100)) игнорирование жестов.</span><span class="sxs-lookup"><span data-stu-id="63239-114">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [CollectionMode](/previous-versions/ms836497(v=msdn.10)) property to ignore gestures.</span></span>
-   <span data-ttu-id="63239-115">Включает объект [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="63239-115">Enables the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span>
-   <span data-ttu-id="63239-116">Задает для свойства [ауторедрав](/previous-versions/ms836495(v=msdn.10)) объекта [InkCollector](/previous-versions/ms583683(v=vs.100)) **значение true**.</span><span class="sxs-lookup"><span data-stu-id="63239-116">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property to **TRUE**.</span></span>


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



<span data-ttu-id="63239-117">Обработчик событий Paint формы проверяет режим приложения:</span><span class="sxs-lookup"><span data-stu-id="63239-117">The form's Paint event handler checks the application mode:</span></span>

-   <span data-ttu-id="63239-118">В режиме HitTest он рисует окружность вокруг курсора.</span><span class="sxs-lookup"><span data-stu-id="63239-118">In the HitTest mode, it paints a circle around the cursor.</span></span> <span data-ttu-id="63239-119">Активное перо задается в методе Хандлехиттест приложения.</span><span class="sxs-lookup"><span data-stu-id="63239-119">The active pen is set in the application's handleHitTest method.</span></span>
-   <span data-ttu-id="63239-120">В режиме Неарестпоинт он рисует красную линию между курсором и точкой, ближайшей к курсору.</span><span class="sxs-lookup"><span data-stu-id="63239-120">In the NearestPoint mode, it paints a red line between the cursor and the point nearest the cursor.</span></span> <span data-ttu-id="63239-121">Ближайшая точка вычисляется в методе Хандленеарестпоинт приложения.</span><span class="sxs-lookup"><span data-stu-id="63239-121">The nearest point is calculated in the application's handleNearestPoint method.</span></span>


```C++
if( mode == ApplicationMode.HitTest)
{
    e.Graphics.DrawEllipse(activepen, penPt.X - HitSize/2, penPt.Y - HitSize/2, HitSize, HitSize);
}
else if( mode == ApplicationMode.NearestPoint )
{
    e.Graphics.DrawLine(redPen, penPt, nearestPt);
}
```



<span data-ttu-id="63239-122">Этот пример имеет очень простой алгоритм перерисовки.</span><span class="sxs-lookup"><span data-stu-id="63239-122">This sample has a very straightforward repaint algorithm.</span></span> <span data-ttu-id="63239-123">Если свойство [ауторедрав](/previous-versions/ms836495(v=msdn.10)) имеет значение **true**, сборщик рукописного ввода перерисовывается при перерисовке формы.</span><span class="sxs-lookup"><span data-stu-id="63239-123">With its [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property set to **TRUE**, the ink collector repaints itself when the form is redrawn.</span></span> <span data-ttu-id="63239-124">Чтобы упростить перерисовку формы, приложение отслеживает ограничивающий прямоугольник, переменную-член Инвалидатерект, для области, в которую добавляется Paint, которая становится недействительной при каждом перерисовке формы.</span><span class="sxs-lookup"><span data-stu-id="63239-124">To simplify redrawing the form, the application tracks a bounding box, the invalidateRect member variable, for the area where paint is added, which is invalidated each time the form is redrawn.</span></span>

## <a name="handling-menu-events"></a><span data-ttu-id="63239-125">Обработка событий меню</span><span class="sxs-lookup"><span data-stu-id="63239-125">Handling Menu Events</span></span>

<span data-ttu-id="63239-126">Команда exit отключает объект [InkCollector](/previous-versions/ms583683(v=vs.100)) перед выходом из приложения.</span><span class="sxs-lookup"><span data-stu-id="63239-126">The Exit command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) before exiting the application.</span></span>

<span data-ttu-id="63239-127">Команда рукописного ввода обновляет состояние режима приложения и меню, включает сборщик рукописных данных и делает недействительным закрашиваемую область формы.</span><span class="sxs-lookup"><span data-stu-id="63239-127">The Ink command updates the application mode and menu status, enables the ink collector, and invalidates the previously painted region of the form.</span></span>

<span data-ttu-id="63239-128">Команды проверки попадания и ближайших точек изменяют курсор, обновляют режим приложения и состояние меню, отключают сборщик рукописных данных и делают недействительными ранее закрашиваемую область формы.</span><span class="sxs-lookup"><span data-stu-id="63239-128">Both the Hit Test and Nearest Point commands change the cursor, update the application mode and menu status, disable the ink collector, and invalidate the previously painted region of the form.</span></span>

<span data-ttu-id="63239-129">Очистка!</span><span class="sxs-lookup"><span data-stu-id="63239-129">The Clear!</span></span> <span data-ttu-id="63239-130">команда отключает [InkCollector](/previous-versions/ms583683(v=vs.100)) , заменяя свойство [рукописного ввода](/previous-versions/ms836505(v=msdn.10)) объекта InkCollector новым объектом [рукописного ввода](/previous-versions/ms571716(v=vs.100)) , создает событие команды рукописного ввода и принудительно выполняет обновление элемента управления.</span><span class="sxs-lookup"><span data-stu-id="63239-130">command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) while replacing InkCollector object's [Ink](/previous-versions/ms836505(v=msdn.10)) property with a new [Ink](/previous-versions/ms571716(v=vs.100)) object, generates an Ink command event, and forces a refresh on the control.</span></span>

## <a name="handling-mouse-events"></a><span data-ttu-id="63239-131">Обработка событий мыши</span><span class="sxs-lookup"><span data-stu-id="63239-131">Handling Mouse Events</span></span>

<span data-ttu-id="63239-132">Обработчик событий [MouseMove](/previous-versions/ms567617(v=vs.100)) проверяет режим приложения:</span><span class="sxs-lookup"><span data-stu-id="63239-132">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode:</span></span>

-   <span data-ttu-id="63239-133">В режиме рукописного ввода ничего не делает, позволяя обычным образом собирать рукописные данные с помощью сборщика рукописных данных.</span><span class="sxs-lookup"><span data-stu-id="63239-133">In Ink mode, it does nothing, allowing ink to be collected normally by the ink collector.</span></span>
-   <span data-ttu-id="63239-134">В режиме HitTest он отправляет аргументы события в метод Хандлехиттест приложения.</span><span class="sxs-lookup"><span data-stu-id="63239-134">In HitTest mode, it sends the event arguments to the application's handleHitTest method.</span></span>
-   <span data-ttu-id="63239-135">В режиме Неарестпоинт он отправляет аргументы события в метод Хандленеарестпоинт приложения.</span><span class="sxs-lookup"><span data-stu-id="63239-135">In NearestPoint mode, it sends the event arguments to the application's handleNearestPoint method.</span></span>

## <a name="performing-a-hit-test"></a><span data-ttu-id="63239-136">Выполнение проверки нажатия</span><span class="sxs-lookup"><span data-stu-id="63239-136">Performing a Hit Test</span></span>

<span data-ttu-id="63239-137">Метод Хандлехиттест приложения создает две точки: положение курсора и точку Хитсизе Пиксели, удаленные от курсора, а затем преобразует эти две точки из пикселов в координаты рукописного пространства.</span><span class="sxs-lookup"><span data-stu-id="63239-137">The application's handleHitTest method creates two points, the cursor location and a point HitSize pixels distant from the cursor, and then converts these two points from pixels to ink space coordinates.</span></span>


```C++
penPt = new Point(e.X, e.Y);
Point pt2 = new Point(e.X, e.Y);
Point pt3 = new Point(e.X + HitSize/2, e.Y);

using (Graphics g = CreateGraphics())
{
    ic.Renderer.PixelToInkSpace(g, ref pt1);
    ic.Renderer.PixelToInkSpace(g, ref pt2);
}
```



<span data-ttu-id="63239-138">Затем объект [InkCollector](/previous-versions/ms583683(v=vs.100)) использует метод [Microsoft. Ink. Ink. HitTest ()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) для поиска штрихов, находящихся в PT3. X-PT2. Единицы измерения позиции курсора по оси X, PT2.</span><span class="sxs-lookup"><span data-stu-id="63239-138">Then, the [InkCollector](/previous-versions/ms583683(v=vs.100)) object uses the [Microsoft.Ink.Ink.HitTest()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to find any strokes that are within pt3.X - pt2.X ink space units of the cursor, pt2.</span></span>


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



<span data-ttu-id="63239-139">Затем метод Хандлехиттест задает цвет пера на основе того, были ли обнаружены штрихи, делает недействительным Инвалидатерект область, вычисляет новый регион, в котором рисуется окружность проверки нажатия, а затем делает недействительным новый регион.</span><span class="sxs-lookup"><span data-stu-id="63239-139">The handleHitTest method then sets the pen color based on whether strokes were found, invalidates the invalidateRect region, calculates a new region that the hit test circle is drawn in, and then invalidates the new region.</span></span>

## <a name="locating-the-nearest-point"></a><span data-ttu-id="63239-140">Поиск ближайшей точки</span><span class="sxs-lookup"><span data-stu-id="63239-140">Locating the Nearest Point</span></span>

<span data-ttu-id="63239-141">Метод Хандленеарестпоинт приложения создает две точки, равные положению курсора, одна из этих точек, пт, преобразуется в пространство рукописного ввода и используется в вызове метода Неарестпоинт объекта [рукописного ввода](/previous-versions/ms836505(v=msdn.10)) [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="63239-141">The application's handleNearestPoint method creates two points both equal to the cursor's location, one of these points, pt, is converted to ink space and used in the call to the NearestPoint method of the [InkCollector](/previous-versions/ms583683(v=vs.100))'s [Ink](/previous-versions/ms836505(v=msdn.10)) object.</span></span> <span data-ttu-id="63239-142">Метод Неарестпоинт возвращает объект [Stroke](/previous-versions/ms827842(v=msdn.10)) , ближайший к точке, и задает выходной параметр индекса с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="63239-142">The NearestPoint method returns the [Stroke](/previous-versions/ms827842(v=msdn.10)) object closest to the point, and sets the floating point index output parameter.</span></span>


```C++
using (Graphics g = CreateGraphics())
{

   // Remeber pen location
    Point inkPenPt = new Point(e.X, e.Y);

    // Convert the pen location into a location in ink space
    ic.Renderer.PixelToInkSpace(g, ref inkPenPt);

    // ...

    float fIndex;
    Stroke stroke = ic.Ink.NearestPoint(inkPenPt, out fIndex);
```



<span data-ttu-id="63239-143">Если штрихи отсутствуют, метод Неарестпоинт возвращает **значение NULL**, а положение курсора используется в качестве ближайшей точки.</span><span class="sxs-lookup"><span data-stu-id="63239-143">If no strokes are present, the NearestPoint method returns **NULL**, and the cursor location is used as the nearest point.</span></span> <span data-ttu-id="63239-144">В противном случае вычисляется положение в штрихе, соответствующем индексу с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="63239-144">Otherwise, the location on the stroke that corresponds to the floating point index is calculated.</span></span>

<span data-ttu-id="63239-145">Затем координаты ближайших точек преобразуются в пиксели из пространства рукописного ввода, метод Хандленеарестпоинт делает недействительным Инвалидатерект область, вычисляет новый регион, в котором рисуется линия до ближайшей точки, и делает новую область недействительной.</span><span class="sxs-lookup"><span data-stu-id="63239-145">The nearest point coordinates are then converted to pixels from ink space, The handleNearestPoint method then invalidates the invalidateRect region, calculates a new region the line to the nearest point is drawn in, and invalidates the new region, too.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="63239-146">Закрытие формы</span><span class="sxs-lookup"><span data-stu-id="63239-146">Closing the Form</span></span>

<span data-ttu-id="63239-147">Метод Dispose удаляет объект [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="63239-147">The form's Dispose method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
