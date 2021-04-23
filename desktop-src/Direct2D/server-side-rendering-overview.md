---
title: Использование Direct2D для подготовки к просмотру Server-Side
description: Описывает использование Direct2D для отрисовки на стороне сервера.
ms.assetid: 12bf4f14-d86f-40ff-b3d3-15ffb3bd7300
keywords:
- Direct2D, отрисовка на стороне сервера
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a35c9df619ee43d11c90c171598c87b6e447dd5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104413083"
---
# <a name="using-direct2d-for-server-side-rendering"></a><span data-ttu-id="36a8d-104">Использование Direct2D для подготовки к просмотру Server-Side</span><span class="sxs-lookup"><span data-stu-id="36a8d-104">Using Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="36a8d-105">Direct2D хорошо подходит для графических приложений, требующих отрисовку на стороне сервера в Windows Server.</span><span class="sxs-lookup"><span data-stu-id="36a8d-105">Direct2D is well-suited for graphics applications that require server-side rendering on Windows Server.</span></span> <span data-ttu-id="36a8d-106">В этом обзоре описываются основные принципы использования Direct2D для отрисовки на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="36a8d-106">This overview describes the basics of using Direct2D for server-side rendering.</span></span> <span data-ttu-id="36a8d-107">Он содержит следующие подразделы:</span><span class="sxs-lookup"><span data-stu-id="36a8d-107">It contains the following sections:</span></span>

-   [<span data-ttu-id="36a8d-108">Требования к отрисовке Server-Side</span><span class="sxs-lookup"><span data-stu-id="36a8d-108">Requirements for Server-Side Rendering</span></span>](#requirements-for-server-side-rendering)
-   [<span data-ttu-id="36a8d-109">Параметры доступных интерфейсов API</span><span class="sxs-lookup"><span data-stu-id="36a8d-109">Options for Available APIs</span></span>](#options-for-available-apis)
    -   [<span data-ttu-id="36a8d-110">ИСПОЛЬЗОВАНИЕМ</span><span class="sxs-lookup"><span data-stu-id="36a8d-110">GDI</span></span>](#gdi)
    -   [<span data-ttu-id="36a8d-111">GDI+</span><span class="sxs-lookup"><span data-stu-id="36a8d-111">GDI+</span></span>](#gdi)
    -   [<span data-ttu-id="36a8d-112">Direct2D</span><span class="sxs-lookup"><span data-stu-id="36a8d-112">Direct2D</span></span>](#using-direct2d-for-server-side-rendering)
-   [<span data-ttu-id="36a8d-113">Использование Direct2D для подготовки к просмотру Server-Side</span><span class="sxs-lookup"><span data-stu-id="36a8d-113">How to Use Direct2D for Server-Side Rendering</span></span>](#how-to-use-direct2d-for-server-side-rendering)
    -   [<span data-ttu-id="36a8d-114">Программная отрисовка</span><span class="sxs-lookup"><span data-stu-id="36a8d-114">Software Rendering</span></span>](#software-rendering)
    -   [<span data-ttu-id="36a8d-115">Многопоточность</span><span class="sxs-lookup"><span data-stu-id="36a8d-115">Multithreading</span></span>](#multithreading)
    -   [<span data-ttu-id="36a8d-116">Создание файла точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="36a8d-116">Generating a Bitmap File</span></span>](#generating-a-bitmap-file)
-   [<span data-ttu-id="36a8d-117">Заключение</span><span class="sxs-lookup"><span data-stu-id="36a8d-117">Conclusion</span></span>](#conclusion)
-   [<span data-ttu-id="36a8d-118">См. также</span><span class="sxs-lookup"><span data-stu-id="36a8d-118">Related topics</span></span>](#related-topics)

## <a name="requirements-for-server-side-rendering"></a><span data-ttu-id="36a8d-119">Требования к отрисовке Server-Side</span><span class="sxs-lookup"><span data-stu-id="36a8d-119">Requirements for Server-Side Rendering</span></span>

<span data-ttu-id="36a8d-120">Ниже приведен типичный сценарий для сервера диаграммы: диаграммы и графики подготавливаются к просмотру на сервере и доставляются в виде растровых изображений в ответ на веб-запросы.</span><span class="sxs-lookup"><span data-stu-id="36a8d-120">The following is a typical scenario for a chart server: charts and graphics are rendered on a server and delivered as bitmaps in response to Web requests.</span></span> <span data-ttu-id="36a8d-121">Сервер может быть оснащен высокопроизводительной графической картой или вообще без графической карты.</span><span class="sxs-lookup"><span data-stu-id="36a8d-121">The server might be equipped with a low-end graphics card or no graphics card at all.</span></span>

<span data-ttu-id="36a8d-122">Этот сценарий раскрывает три требования к приложениям.</span><span class="sxs-lookup"><span data-stu-id="36a8d-122">This scenario reveals three application requirements.</span></span> <span data-ttu-id="36a8d-123">Во первых, приложение должно эффективно обслуживать несколько параллельных запросов, особенно на многоядерных серверах.</span><span class="sxs-lookup"><span data-stu-id="36a8d-123">First, the application must handle multiple concurrent requests efficiently, especially on multicore servers.</span></span> <span data-ttu-id="36a8d-124">Во-вторых, приложение должно использовать программную отрисовку при работе на серверах с высокопроизводительной графической картой или без графической карты.</span><span class="sxs-lookup"><span data-stu-id="36a8d-124">Second, the application must use software rendering when running on servers with a low-end graphics card or no graphics card.</span></span> <span data-ttu-id="36a8d-125">Наконец, приложение должно быть запущено в качестве службы в сеансе 0, чтобы не требовать входа пользователя в систему.</span><span class="sxs-lookup"><span data-stu-id="36a8d-125">Finally, the application must run as a service in Session 0 so that it does not require a user to be logged in.</span></span> <span data-ttu-id="36a8d-126">Дополнительные сведения о сеансе 0 см. в разделе [влияние изоляции сеанса 0 на службы и драйверы в Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).</span><span class="sxs-lookup"><span data-stu-id="36a8d-126">For more information about Session 0, see [Impact of Session 0 Isolation on Services and Drivers in Windows](https://www.microsoft.com/whdc/system/sysinternals/Session0Changes.mspx).</span></span>

## <a name="options-for-available-apis"></a><span data-ttu-id="36a8d-127">Параметры доступных интерфейсов API</span><span class="sxs-lookup"><span data-stu-id="36a8d-127">Options for Available APIs</span></span>

<span data-ttu-id="36a8d-128">Существует три варианта отрисовки на стороне сервера: GDI, GDI+ и Direct2D.</span><span class="sxs-lookup"><span data-stu-id="36a8d-128">There are three options for server-side rendering: GDI, GDI+ and Direct2D.</span></span> <span data-ttu-id="36a8d-129">Как и GDI и GDI+, Direct2D — это собственный API двухмерной отрисовки, который предоставляет приложениям больший контроль над использованием графических устройств.</span><span class="sxs-lookup"><span data-stu-id="36a8d-129">Like GDI and GDI+, Direct2D is a native 2D rendering API that gives applications more control over the use of graphics devices.</span></span> <span data-ttu-id="36a8d-130">Кроме того, Direct2D уникально поддерживает многопоточные и многопоточные фабрики.</span><span class="sxs-lookup"><span data-stu-id="36a8d-130">In addition, Direct2D uniquely supports a single-threaded and a multithreaded factory.</span></span> <span data-ttu-id="36a8d-131">В следующих разделах сравнивается каждый API с точки зрения качества рисования и многопоточной отрисовки на стороне сервера.</span><span class="sxs-lookup"><span data-stu-id="36a8d-131">The following sections compare each API in terms of drawing qualities and multithreaded server-side rendering.</span></span>

### <a name="gdi"></a><span data-ttu-id="36a8d-132">GDI</span><span class="sxs-lookup"><span data-stu-id="36a8d-132">GDI</span></span>

<span data-ttu-id="36a8d-133">В отличие от Direct2D и GDI+, GDI не поддерживает функции рисования высокого качества.</span><span class="sxs-lookup"><span data-stu-id="36a8d-133">Unlike Direct2D and GDI+, GDI does not support high-quality drawing features.</span></span> <span data-ttu-id="36a8d-134">Например, GDI не поддерживает сглаживание для создания гладких линий и имеет ограниченную поддержку прозрачности.</span><span class="sxs-lookup"><span data-stu-id="36a8d-134">For instance, GDI does not support antialiasing for creating smooth lines and has only limited support for transparency.</span></span> <span data-ttu-id="36a8d-135">На основе результатов тестирования производительности графики в Windows 7 и Windows Server 2008 R2 Direct2D масштабируется более эффективно, чем GDI, несмотря на переработку блокировок в GDI.</span><span class="sxs-lookup"><span data-stu-id="36a8d-135">Based on the graphics performance test results on Windows 7 and Windows Server 2008 R2, Direct2D scales more efficiently than GDI, despite the redesign of locks in GDI.</span></span> <span data-ttu-id="36a8d-136">Дополнительные сведения об этих результатах тестирования см. в разделе [проектирование производительности графики в Windows 7](/archive/blogs/e7/engineering-windows-7-graphics-performance).</span><span class="sxs-lookup"><span data-stu-id="36a8d-136">For more information about these test results, see [Engineering Windows 7 Graphics Performance](/archive/blogs/e7/engineering-windows-7-graphics-performance).</span></span>

<span data-ttu-id="36a8d-137">Кроме того, приложения, использующие GDI, ограничены до 10240 дескрипторов GDI на процесс и 65536 дескрипторов GDI на сеанс.</span><span class="sxs-lookup"><span data-stu-id="36a8d-137">In addition, applications using GDI are limited to 10240 GDI handles per process and 65536 GDI handles per session.</span></span> <span data-ttu-id="36a8d-138">Причина заключается в том, что внутренние окна используют 16-разрядное слово для хранения индекса дескрипторов для каждого сеанса.</span><span class="sxs-lookup"><span data-stu-id="36a8d-138">The reason is that internally Windows uses a 16-bit WORD to store the index of handles for each session.</span></span>

### <a name="gdi"></a><span data-ttu-id="36a8d-139">GDI+</span><span class="sxs-lookup"><span data-stu-id="36a8d-139">GDI+</span></span>

<span data-ttu-id="36a8d-140">Хотя GDI+ поддерживает сглаживание и альфа-смешение для высококачественного рисования, основная проблема с GDI+ для серверных сценариев заключается в том, что она не поддерживает выполнение в сеансе 0.</span><span class="sxs-lookup"><span data-stu-id="36a8d-140">While GDI+ supports antialiasing and alpha blending for high-quality drawing, the main problem with GDI+ for server-scenarios is that it does not support running in Session 0.</span></span> <span data-ttu-id="36a8d-141">Так как сеанс 0 поддерживает только неинтерактивные функции, функции, непосредственно или косвенно взаимодействующие с устройствами вывода, получают ошибки.</span><span class="sxs-lookup"><span data-stu-id="36a8d-141">Since Session 0 only supports non-interactive functionality, functions that directly or indirectly interact with display devices will therefore receive errors.</span></span> <span data-ttu-id="36a8d-142">Конкретные примеры функций включают не только те, которые относятся к устройствам вывода, но и те, которые косвенно работают с драйверами устройств.</span><span class="sxs-lookup"><span data-stu-id="36a8d-142">Specific examples of functions include not only those dealing with display devices, but also those indirectly dealing with device drivers.</span></span>

<span data-ttu-id="36a8d-143">Подобно GDI, GDI+ ограничен механизмом блокировки.</span><span class="sxs-lookup"><span data-stu-id="36a8d-143">Similar to GDI, GDI+ is limited by its locking mechanism.</span></span> <span data-ttu-id="36a8d-144">Механизмы блокировки в GDI+ одинаковы в Windows 7 и Windows Server 2008 R2, как в предыдущих версиях.</span><span class="sxs-lookup"><span data-stu-id="36a8d-144">The locking mechanisms in GDI+ are the same in Windows 7 and Windows Server 2008 R2 as in previous versions.</span></span>

### <a name="direct2d"></a><span data-ttu-id="36a8d-145">Direct2D</span><span class="sxs-lookup"><span data-stu-id="36a8d-145">Direct2D</span></span>

<span data-ttu-id="36a8d-146">Direct2D — это высокопроизводительный, высококачественный графический API, обеспечивающий высокую производительность и качественную визуализацию с аппаратным ускорением.</span><span class="sxs-lookup"><span data-stu-id="36a8d-146">Direct2D is a hardware-accelerated, immediate-mode, 2-D graphics API that provides high performance and high-quality rendering.</span></span> <span data-ttu-id="36a8d-147">Она предлагает однопотоковую и многопоточной фабрику, а также линейное масштабирование программной отрисовки с детализацией.</span><span class="sxs-lookup"><span data-stu-id="36a8d-147">It offers a single-threaded and a multithreaded factory and the linear scaling of course-grained software rendering.</span></span>

<span data-ttu-id="36a8d-148">Для этого Direct2D определяет корневой интерфейс фабрики.</span><span class="sxs-lookup"><span data-stu-id="36a8d-148">To do this, Direct2D defines a root factory interface.</span></span> <span data-ttu-id="36a8d-149">Как правило, объект, созданный в фабрике, может использоваться только с другими объектами, созданными из той же фабрики.</span><span class="sxs-lookup"><span data-stu-id="36a8d-149">As a rule, an object created on a factory can only be used with other objects created from the same factory.</span></span> <span data-ttu-id="36a8d-150">Вызывающий объект может запросить однопотоковое или многопоточное фабрику при ее создании.</span><span class="sxs-lookup"><span data-stu-id="36a8d-150">The caller can request either a single-threaded or a multithreaded factory when it is created.</span></span> <span data-ttu-id="36a8d-151">При запросе однопотоковой фабрики не выполняется блокировка потоков.</span><span class="sxs-lookup"><span data-stu-id="36a8d-151">If a single-threaded factory is requested, then no locking of threads is performed.</span></span> <span data-ttu-id="36a8d-152">Если вызывающий объект запрашивает многопоточную фабрику, то при каждом вызове в Direct2D будет получено блокирование потока на уровне фабрики.</span><span class="sxs-lookup"><span data-stu-id="36a8d-152">If the caller requests a multithreaded factory, then, a factory-wide thread lock is acquired whenever a call is made into Direct2D.</span></span>

<span data-ttu-id="36a8d-153">Кроме того, блокировка потоков в Direct2D более детализирована, чем в GDI и GDI+, поэтому увеличение числа потоков оказывает минимальное влияние на производительность.</span><span class="sxs-lookup"><span data-stu-id="36a8d-153">In addition, the locking of threads in Direct2D is more granular than in GDI and GDI+, so that the increase of the number of threads has minimal impact on the performance.</span></span>

## <a name="how-to-use-direct2d-for-server-side-rendering"></a><span data-ttu-id="36a8d-154">Использование Direct2D для подготовки к просмотру Server-Side</span><span class="sxs-lookup"><span data-stu-id="36a8d-154">How to Use Direct2D for Server-Side Rendering</span></span>

<span data-ttu-id="36a8d-155">В следующих разделах описывается использование программной отрисовки, оптимальное использование однопотоковых и многопоточных фабрик, а также рисование и сохранение сложного рисунка в файл.</span><span class="sxs-lookup"><span data-stu-id="36a8d-155">The following sections describe how to use software rendering, how to optimally use a single-threaded and a multithreaded factory, and how to draw and save a complex drawing to a file.</span></span>

### <a name="software-rendering"></a><span data-ttu-id="36a8d-156">Программная отрисовка</span><span class="sxs-lookup"><span data-stu-id="36a8d-156">Software Rendering</span></span>

<span data-ttu-id="36a8d-157">Серверные приложения используют отрисовку программного обеспечения путем создания целевого объекта рендеринга [ивикбитмап](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) , при этом для типа целевого объекта прорисовки задано значение D2D1 для \_ \_ целевого типа прорисовки \_ \_ программного обеспечения или D2D1 \_ \_ тип целевого объекта визуализации \_ \_ по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36a8d-157">Server-side applications use software rendering by creating [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target, with the render target type set to either D2D1\_RENDER\_TARGET\_TYPE\_SOFTWARE or D2D1\_RENDER\_TARGET\_TYPE\_DEFAULT.</span></span> <span data-ttu-id="36a8d-158">Дополнительные сведения о целевых объектах рендеринга [ивикбитмап](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) см. в разделе метод [**ID2D1Factory:: креатевикбитмапрендертаржет**](id2d1factory-createwicbitmaprendertarget.md) . Дополнительные сведения о типах целевых объектов отрисовки см. в разделе [**D2D1 \_ Render \_ Target \_ Type**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).</span><span class="sxs-lookup"><span data-stu-id="36a8d-158">For more information about [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render targets, see the [**ID2D1Factory::CreateWicBitmapRenderTarget**](id2d1factory-createwicbitmaprendertarget.md) method; for more information about the render target types, see [**D2D1\_RENDER\_TARGET\_TYPE**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_render_target_type).</span></span>

### <a name="multithreading"></a><span data-ttu-id="36a8d-159">Многопоточность</span><span class="sxs-lookup"><span data-stu-id="36a8d-159">Multithreading</span></span>

<span data-ttu-id="36a8d-160">Знание создания и совместного использования фабрик и целевых объектов рендеринга в разных потоках может значительно повлиять на производительность приложения.</span><span class="sxs-lookup"><span data-stu-id="36a8d-160">Knowing how to create and share factories and render targets across threads can significantly impact the performance of an application.</span></span> <span data-ttu-id="36a8d-161">На следующих трех рисунках показаны три различных подхода.</span><span class="sxs-lookup"><span data-stu-id="36a8d-161">The following three figures show three varied approaches.</span></span> <span data-ttu-id="36a8d-162">Оптимальный подход показан на рис. 3.</span><span class="sxs-lookup"><span data-stu-id="36a8d-162">The optimal approach is shown in figure 3.</span></span>

![Direct2D схема многопоточности с одним целевым объектом рендеринга.](images/server-side-rendering-1.png)

<span data-ttu-id="36a8d-164">На рис. 1 разные потоки совместно используют одну и ту же фабрику и один и тот же целевой объект рендеринга.</span><span class="sxs-lookup"><span data-stu-id="36a8d-164">In figure 1, different threads share the same factory and the same render target.</span></span> <span data-ttu-id="36a8d-165">Такой подход может привести к непредсказуемым результатам в случаях, когда несколько потоков одновременно изменяют состояние общей цели рендеринга, например, одновременно устанавливая матрицу преобразования.</span><span class="sxs-lookup"><span data-stu-id="36a8d-165">This approach can lead to unpredictable results in cases when multiple threads simultaneously change the state of the shared render target, such as simultaneously setting the transformation matrix.</span></span> <span data-ttu-id="36a8d-166">Так как внутренняя блокировка в Direct2D не синхронизирует общий ресурс, например целевые объекты рендеринга, этот подход может вызвать сбой вызова [**бегиндрав**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) в потоке 1, так как в потоке 2 вызов **бегиндрав** уже использует общий целевой объект отрисовки.</span><span class="sxs-lookup"><span data-stu-id="36a8d-166">As the internal locking in Direct2D does not synchronize a shared resource such as render targets, this approach can cause the [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) call to fail in thread 1, because in thread 2, the **BeginDraw** call is already using the shared render target.</span></span>

![Direct2D Многопотоковая диаграмма с несколькими целевыми объектами отрисовки.](images/server-side-rendering-2.png)

<span data-ttu-id="36a8d-168">Чтобы избежать непредсказуемых результатов, возникших на рис. 1, на рис. 2 показана многопоточная фабрика с каждым потоком, имеющим собственный целевой объект рендеринга.</span><span class="sxs-lookup"><span data-stu-id="36a8d-168">To avoid the unpredictable results encountered in figure 1, figure 2 shows a multithreaded factory with each thread having its own render target.</span></span> <span data-ttu-id="36a8d-169">Этот подход работает, но фактически функционирует как приложение с одним потоком.</span><span class="sxs-lookup"><span data-stu-id="36a8d-169">This approach works but it effectively functions as a single-threaded application.</span></span> <span data-ttu-id="36a8d-170">Причина заключается в том, что блокировка на уровне фабрики применяется только к уровню операции рисования, и все вызовы рисования в той же фабрике сериализуются.</span><span class="sxs-lookup"><span data-stu-id="36a8d-170">The reason is that the factory-wide lock applies only to the drawing-operation level and all the drawing calls in the same factory consequently are serialized.</span></span> <span data-ttu-id="36a8d-171">В результате поток 1 блокируется при попытке ввести вызов рисования, а поток 2 — в середине выполнения другого вызова рисования.</span><span class="sxs-lookup"><span data-stu-id="36a8d-171">As a result, thread 1 becomes blocked when trying to enter a drawing call, while thread 2 is in the middle of executing another drawing call.</span></span>

![Direct2D Многопотоковая диаграмма с несколькими фабриками и несколькими целевыми объектами рендеринга.](images/server-side-rendering-3.png)

<span data-ttu-id="36a8d-173">На рис. 3 показан оптимальный подход, в котором используются однопотоковые фабрики и однопотоковый целевой объект отрисовки.</span><span class="sxs-lookup"><span data-stu-id="36a8d-173">Figure 3 shows the optimal approach, where a single-threaded factory and a single-threaded render target are used.</span></span> <span data-ttu-id="36a8d-174">Поскольку при использовании однопотоковой фабрики не выполняется блокировка, операции рисования в каждом потоке могут выполняться параллельно для достижения оптимальной производительности.</span><span class="sxs-lookup"><span data-stu-id="36a8d-174">Since no locking is performed when using a single-threaded factory, drawing operations in each thread can run concurrently to achieve optimal performance.</span></span>

### <a name="generating-a-bitmap-file"></a><span data-ttu-id="36a8d-175">Создание файла точечного рисунка</span><span class="sxs-lookup"><span data-stu-id="36a8d-175">Generating a Bitmap File</span></span>

<span data-ttu-id="36a8d-176">Чтобы создать файл точечного рисунка с помощью отрисовки программного обеспечения, используйте целевой объект рендеринга [ивикбитмап](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="36a8d-176">To generate a bitmap file using software rendering, use an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="36a8d-177">Используйте [ивикстреам](/windows/win32/api/wincodec/nn-wincodec-iwicstream) для записи точечного рисунка в файл.</span><span class="sxs-lookup"><span data-stu-id="36a8d-177">Use an [IWICStream](/windows/win32/api/wincodec/nn-wincodec-iwicstream) to write the bitmap to a file.</span></span> <span data-ttu-id="36a8d-178">Используйте [ивикбитмапфраминкоде](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) для кодирования точечного рисунка в указанный формат изображения.</span><span class="sxs-lookup"><span data-stu-id="36a8d-178">Use [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap into a specified image format.</span></span> <span data-ttu-id="36a8d-179">В следующем примере кода показано, как выполнить прорисовку и сохранение следующего изображения в файл.</span><span class="sxs-lookup"><span data-stu-id="36a8d-179">The following code example shows how to draw and save the following image to a file.</span></span>

![пример выходного изображения.](images/saveasimagefile-sample.png)

<span data-ttu-id="36a8d-181">В этом примере кода сначала создается [ивикбитмап](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) и целевой объект отрисовки [ивикбитмап](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) .</span><span class="sxs-lookup"><span data-stu-id="36a8d-181">This code example first creates an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) and an [IWICBitmap](/windows/win32/api/wincodec/nn-wincodec-iwicbitmap) render target.</span></span> <span data-ttu-id="36a8d-182">Затем он визуализирует изображение с текстом, геометрическим контуром, представляющим почасовое стекло, а также преобразованное почасовое стекло в растровое изображение WIC.</span><span class="sxs-lookup"><span data-stu-id="36a8d-182">It then renders a drawing with some text, a path geometry representing an hour glass, and a transformed hour glass into a WIC bitmap.</span></span> <span data-ttu-id="36a8d-183">Затем он использует [ивикстреам:: инитиализефромфиленаме](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) для сохранения растрового изображения в файл.</span><span class="sxs-lookup"><span data-stu-id="36a8d-183">It then uses [IWICStream::InitializeFromFilename](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefromfilename) to save the bitmap to a file.</span></span> <span data-ttu-id="36a8d-184">Если приложению необходимо сохранить точечный рисунок в памяти, используйте вместо него [ивикстреам:: инитиализефроммемори](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) .</span><span class="sxs-lookup"><span data-stu-id="36a8d-184">If your application needs to save the bitmap in memory, use [IWICStream::InitializeFromMemory](/windows/win32/api/wincodec/nf-wincodec-iwicstream-initializefrommemory) instead.</span></span> <span data-ttu-id="36a8d-185">Наконец, он использует [ивикбитмапфраминкоде](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) для кодирования точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="36a8d-185">Finally, it uses [IWICBitmapFrameEncode](/windows/win32/api/wincodec/nn-wincodec-iwicbitmapframeencode) to encode the bitmap.</span></span>


```C++
// Create an IWICBitmap and RT
static const UINT sc_bitmapWidth = 640;
static const UINT sc_bitmapHeight = 480;
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateBitmap(
        sc_bitmapWidth,
        sc_bitmapHeight,
        GUID_WICPixelFormat32bppBGR,
        WICBitmapCacheOnLoad,
        &pWICBitmap
        );
}

// Set the render target type to D2D1_RENDER_TARGET_TYPE_DEFAULT to use software rendering.
if (SUCCEEDED(hr))
{
    hr = pD2DFactory->CreateWicBitmapRenderTarget(
        pWICBitmap,
        D2D1::RenderTargetProperties(),
        &pRT
        );
}

// Create text format and a path geometry representing an hour glass. 
if (SUCCEEDED(hr))
{
    static const WCHAR sc_fontName[] = L"Calibri";
    static const FLOAT sc_fontSize = 50;

    hr = pDWriteFactory->CreateTextFormat(
        sc_fontName,
        NULL,
        DWRITE_FONT_WEIGHT_NORMAL,
        DWRITE_FONT_STYLE_NORMAL,
        DWRITE_FONT_STRETCH_NORMAL,
        sc_fontSize,
        L"", //locale
        &pTextFormat
        );
}
if (SUCCEEDED(hr))
{
    pTextFormat->SetTextAlignment(DWRITE_TEXT_ALIGNMENT_CENTER);
    pTextFormat->SetParagraphAlignment(DWRITE_PARAGRAPH_ALIGNMENT_CENTER);
    hr = pD2DFactory->CreatePathGeometry(&pPathGeometry);
}
if (SUCCEEDED(hr))
{
    hr = pPathGeometry->Open(&pSink);
}
if (SUCCEEDED(hr))
{
    pSink->SetFillMode(D2D1_FILL_MODE_ALTERNATE);

    pSink->BeginFigure(
        D2D1::Point2F(0, 0),
        D2D1_FIGURE_BEGIN_FILLED
        );

    pSink->AddLine(D2D1::Point2F(200, 0));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(150, 50),
            D2D1::Point2F(150, 150),
            D2D1::Point2F(200, 200))
        );

    pSink->AddLine(D2D1::Point2F(0, 200));

    pSink->AddBezier(
        D2D1::BezierSegment(
            D2D1::Point2F(50, 150),
            D2D1::Point2F(50, 50),
            D2D1::Point2F(0, 0))
        );

    pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

    hr = pSink->Close();
}
if (SUCCEEDED(hr))
{
    static const D2D1_GRADIENT_STOP stops[] =
    {
        {   0.f,  { 0.f, 1.f, 1.f, 1.f }  },
        {   1.f,  { 0.f, 0.f, 1.f, 1.f }  },
    };

    hr = pRT->CreateGradientStopCollection(
        stops,
        ARRAYSIZE(stops),
        &pGradientStops
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateLinearGradientBrush(
        D2D1::LinearGradientBrushProperties(
            D2D1::Point2F(100, 0),
            D2D1::Point2F(100, 200)),
        D2D1::BrushProperties(),
        pGradientStops,
        &pLGBrush
        );
}
if (SUCCEEDED(hr))
{
    hr = pRT->CreateSolidColorBrush(
        D2D1::ColorF(D2D1::ColorF::Black),
        &pBlackBrush
        );
}
if (SUCCEEDED(hr))
{
    // Render into the bitmap.
    pRT->BeginDraw();
    pRT->Clear(D2D1::ColorF(D2D1::ColorF::White));
    D2D1_SIZE_F rtSize = pRT->GetSize();

    // Set the world transform to a 45 degree rotation at the center of the render target
    // and write "Hello, World".
    pRT->SetTransform(
        D2D1::Matrix3x2F::Rotation(
            45,
            D2D1::Point2F(
                rtSize.width / 2,
                rtSize.height / 2))
            );

    static const WCHAR sc_helloWorld[] = L"Hello, World!";
    pRT->DrawText(
        sc_helloWorld,
        ARRAYSIZE(sc_helloWorld) - 1,
        pTextFormat,
        D2D1::RectF(0, 0, rtSize.width, rtSize.height),
        pBlackBrush);

    // Reset back to the identity transform.
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(0, rtSize.height - 200));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    pRT->SetTransform(D2D1::Matrix3x2F::Translation(rtSize.width - 200, 0));
    pRT->FillGeometry(pPathGeometry, pLGBrush);
    hr = pRT->EndDraw();
}

if (SUCCEEDED(hr))
{
    // Save the image to a file.
    hr = pWICFactory->CreateStream(&pStream);
}

WICPixelFormatGUID format = GUID_WICPixelFormatDontCare;

// Use InitializeFromFilename to write to a file. If there is need to write inside the memory, use InitializeFromMemory. 
if (SUCCEEDED(hr))
{
    static const WCHAR filename[] = L"output.png";
    hr = pStream->InitializeFromFilename(filename, GENERIC_WRITE);
}
if (SUCCEEDED(hr))
{
    hr = pWICFactory->CreateEncoder(GUID_ContainerFormatPng, NULL, &pEncoder);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Initialize(pStream, WICBitmapEncoderNoCache);
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->CreateNewFrame(&pFrameEncode, NULL);
}
// Use IWICBitmapFrameEncode to encode the bitmap into the picture format you want.
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Initialize(NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetSize(sc_bitmapWidth, sc_bitmapHeight);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->SetPixelFormat(&format);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->WriteSource(pWICBitmap, NULL);
}
if (SUCCEEDED(hr))
{
    hr = pFrameEncode->Commit();
}
if (SUCCEEDED(hr))
{
    hr = pEncoder->Commit();
}

```



## <a name="conclusion"></a><span data-ttu-id="36a8d-186">Заключение</span><span class="sxs-lookup"><span data-stu-id="36a8d-186">Conclusion</span></span>

<span data-ttu-id="36a8d-187">Как видно из приведенного выше, использование Direct2D для отрисовки на стороне сервера является простым и простым.</span><span class="sxs-lookup"><span data-stu-id="36a8d-187">As seen from the above, using Direct2D for server-side rendering is simple and straightforward.</span></span> <span data-ttu-id="36a8d-188">Кроме того, он обеспечивает высококачественную и высокопараллелизуемыеную отрисовку, которая может выполняться в средах сервера с низким уровнем прав.</span><span class="sxs-lookup"><span data-stu-id="36a8d-188">In addition, it provides high quality and highly parallelizable rendering that can run in low-privilege environments of the server.</span></span>

## <a name="related-topics"></a><span data-ttu-id="36a8d-189">См. также</span><span class="sxs-lookup"><span data-stu-id="36a8d-189">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36a8d-190">Справочник по Direct2D</span><span class="sxs-lookup"><span data-stu-id="36a8d-190">Direct2D Reference</span></span>](reference.md)
</dt> </dl>

 

 