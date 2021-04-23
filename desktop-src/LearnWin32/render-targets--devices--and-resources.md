---
title: Отрисовка целевых объектов, устройств и ресурсов
description: Отрисовка целевых объектов, устройств и ресурсов
ms.assetid: cf48c2ce-16ad-4e61-8900-501c7c27da23
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eeddd84e12c52e0fd0ae82dab8b5e8741a2e0891
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2020
ms.locfileid: "104337201"
---
# <a name="render-targets-devices-and-resources"></a><span data-ttu-id="fc77d-103">Отрисовка целевых объектов, устройств и ресурсов</span><span class="sxs-lookup"><span data-stu-id="fc77d-103">Render Targets, Devices, and Resources</span></span>

<span data-ttu-id="fc77d-104">*Цель рендеринга* — это просто расположение, в котором программа будет рисовать.</span><span class="sxs-lookup"><span data-stu-id="fc77d-104">A *render target* is simply the location where your program will draw.</span></span> <span data-ttu-id="fc77d-105">Как правило, целью рендеринга является окно (в частности, клиентская область окна).</span><span class="sxs-lookup"><span data-stu-id="fc77d-105">Typically, the render target is a window (specifically, the client area of the window).</span></span> <span data-ttu-id="fc77d-106">Он также может быть точечным рисунком в памяти, который не отображается.</span><span class="sxs-lookup"><span data-stu-id="fc77d-106">It could also be a bitmap in memory that is not displayed.</span></span> <span data-ttu-id="fc77d-107">Целевой объект прорисовки представлен интерфейсом [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) .</span><span class="sxs-lookup"><span data-stu-id="fc77d-107">A render target is represented by the [**ID2D1RenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1rendertarget) interface.</span></span>

<span data-ttu-id="fc77d-108">*Устройство* — это абстракция, представляющая все фактически рисуемые Пиксели.</span><span class="sxs-lookup"><span data-stu-id="fc77d-108">A *device* is an abstraction that represents whatever actually draws the pixels.</span></span> <span data-ttu-id="fc77d-109">Аппаратное устройство использует GPU для повышения производительности, в то время как программное устройство использует процессор.</span><span class="sxs-lookup"><span data-stu-id="fc77d-109">A hardware device uses the GPU for faster performance, whereas a software device uses the CPU.</span></span> <span data-ttu-id="fc77d-110">Приложение не создает устройство.</span><span class="sxs-lookup"><span data-stu-id="fc77d-110">The application does not create the device.</span></span> <span data-ttu-id="fc77d-111">Вместо этого устройство создается неявно, когда приложение создает целевой объект отрисовки.</span><span class="sxs-lookup"><span data-stu-id="fc77d-111">Instead, the device is created implicitly when the application creates the render target.</span></span> <span data-ttu-id="fc77d-112">Каждый целевой объект прорисовки связан с конкретным устройством, оборудованием или программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="fc77d-112">Each render target is associated with a particular device, either hardware or software.</span></span>

![Схема, показывающая отношение между целевым объектом отрисовки и устройством.](images/graphics09.png)

<span data-ttu-id="fc77d-114">*Ресурс* — это объект, используемый программой для рисования.</span><span class="sxs-lookup"><span data-stu-id="fc77d-114">A *resource* is an object that the program uses for drawing.</span></span> <span data-ttu-id="fc77d-115">Ниже приведены некоторые примеры ресурсов, определенных в Direct2D.</span><span class="sxs-lookup"><span data-stu-id="fc77d-115">Here are some examples of resources that are defined in Direct2D:</span></span>

-   <span data-ttu-id="fc77d-116">**Кисть**.</span><span class="sxs-lookup"><span data-stu-id="fc77d-116">**Brush**.</span></span> <span data-ttu-id="fc77d-117">Определяет, как рисуются линии и регионы.</span><span class="sxs-lookup"><span data-stu-id="fc77d-117">Controls how lines and regions are painted.</span></span> <span data-ttu-id="fc77d-118">К типам кистей относятся кисти с сплошным цветом и градиентные кисти.</span><span class="sxs-lookup"><span data-stu-id="fc77d-118">Brush types include solid-color brushes and gradient brushes.</span></span>
-   <span data-ttu-id="fc77d-119">**Стиль обводки**.</span><span class="sxs-lookup"><span data-stu-id="fc77d-119">**Stroke style**.</span></span> <span data-ttu-id="fc77d-120">Управляет внешним видом линии, например штриховой или сплошной.</span><span class="sxs-lookup"><span data-stu-id="fc77d-120">Controls the appearance of a line—for example, dashed or solid.</span></span>
-   <span data-ttu-id="fc77d-121">**Геометрия**.</span><span class="sxs-lookup"><span data-stu-id="fc77d-121">**Geometry**.</span></span> <span data-ttu-id="fc77d-122">Представляет коллекцию линий и кривых.</span><span class="sxs-lookup"><span data-stu-id="fc77d-122">Represents a collection of lines and curves.</span></span>
-   <span data-ttu-id="fc77d-123">**Сетка**.</span><span class="sxs-lookup"><span data-stu-id="fc77d-123">**Mesh**.</span></span> <span data-ttu-id="fc77d-124">Фигура, образованная из треугольников.</span><span class="sxs-lookup"><span data-stu-id="fc77d-124">A shape formed out of triangles.</span></span> <span data-ttu-id="fc77d-125">Данные сетки могут быть использованы непосредственно графическим процессором, в отличие от данных geometry, которые необходимо преобразовать перед отрисовкой.</span><span class="sxs-lookup"><span data-stu-id="fc77d-125">Mesh data can be consumed directly by the GPU, unlike geometry data, which must be converted before rendering.</span></span>

<span data-ttu-id="fc77d-126">Целевые объекты рендеринга также считаются типами ресурсов.</span><span class="sxs-lookup"><span data-stu-id="fc77d-126">Render targets are also considered a type of resource.</span></span>

<span data-ttu-id="fc77d-127">Некоторые ресурсы имеют преимущество аппаратного ускорения.</span><span class="sxs-lookup"><span data-stu-id="fc77d-127">Some resources benefit from hardware acceleration.</span></span> <span data-ttu-id="fc77d-128">Ресурс этого типа всегда связан с конкретным устройством (GPU) или программным обеспечением (ЦП).</span><span class="sxs-lookup"><span data-stu-id="fc77d-128">A resource of this type is always associated with a particular device, either hardware (GPU) or software (CPU).</span></span> <span data-ttu-id="fc77d-129">Этот тип ресурса называется аппаратно *-зависимым*.</span><span class="sxs-lookup"><span data-stu-id="fc77d-129">This type of resource is called *device-dependent*.</span></span> <span data-ttu-id="fc77d-130">Примерами ресурсов, зависящих от устройства, являются кисти и сетки.</span><span class="sxs-lookup"><span data-stu-id="fc77d-130">Brushes and meshes are examples of device-dependent resources.</span></span> <span data-ttu-id="fc77d-131">Если устройство становится недоступным, ресурс необходимо создать заново для нового устройства.</span><span class="sxs-lookup"><span data-stu-id="fc77d-131">If the device becomes unavailable, the resource must be re-created for a new device.</span></span>

<span data-ttu-id="fc77d-132">Другие ресурсы хранятся в памяти ЦП независимо от используемого устройства.</span><span class="sxs-lookup"><span data-stu-id="fc77d-132">Other resources are kept in CPU memory, regardless of what device is used.</span></span> <span data-ttu-id="fc77d-133">Эти ресурсы не *зависят от устройства*, так как они не связаны с конкретным устройством.</span><span class="sxs-lookup"><span data-stu-id="fc77d-133">These resources are *device-independent*, because they are not associated with a particular device.</span></span> <span data-ttu-id="fc77d-134">При изменении устройства не требуется повторно создавать ресурсы, независимые от устройства.</span><span class="sxs-lookup"><span data-stu-id="fc77d-134">It is not necessary to re-create device-independent resources when the device changes.</span></span> <span data-ttu-id="fc77d-135">Стили и геометрические штрихи являются независимыми от устройства ресурсами.</span><span class="sxs-lookup"><span data-stu-id="fc77d-135">Stroke styles and geometries are device-independent resources.</span></span>

<span data-ttu-id="fc77d-136">В документации MSDN по каждому ресурсу указывается, зависит ли ресурс от устройства или от устройства.</span><span class="sxs-lookup"><span data-stu-id="fc77d-136">The MSDN documentation for each resource states whether the resource is device-dependent or device-independent.</span></span> <span data-ttu-id="fc77d-137">Каждый тип ресурса представлен интерфейсом, производным от [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource).</span><span class="sxs-lookup"><span data-stu-id="fc77d-137">Every resource type is represented by an interface that derives from [**ID2D1Resource**](/windows/desktop/api/d2d1/nn-d2d1-id2d1resource).</span></span> <span data-ttu-id="fc77d-138">Например, кисти представлены интерфейсом [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) .</span><span class="sxs-lookup"><span data-stu-id="fc77d-138">For example, brushes are represented by the [**ID2D1Brush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1brush) interface.</span></span>

## <a name="the-direct2d-factory-object"></a><span data-ttu-id="fc77d-139">Объект фабрики Direct2D</span><span class="sxs-lookup"><span data-stu-id="fc77d-139">The Direct2D Factory Object</span></span>

<span data-ttu-id="fc77d-140">Первым шагом при использовании Direct2D является создание экземпляра объекта фабрики Direct2D.</span><span class="sxs-lookup"><span data-stu-id="fc77d-140">The first step when using Direct2D is to create an instance of the Direct2D factory object.</span></span> <span data-ttu-id="fc77d-141">В компьютерных программах *фабрика* — это объект, который создает другие объекты.</span><span class="sxs-lookup"><span data-stu-id="fc77d-141">In computer programming, a *factory* is an object that creates other objects.</span></span> <span data-ttu-id="fc77d-142">Фабрика Direct2D создает следующие типы объектов:</span><span class="sxs-lookup"><span data-stu-id="fc77d-142">The Direct2D factory creates the following types of objects:</span></span>

-   <span data-ttu-id="fc77d-143">Целевые объекты отрисовки.</span><span class="sxs-lookup"><span data-stu-id="fc77d-143">Render targets.</span></span>
-   <span data-ttu-id="fc77d-144">Независимые от устройства ресурсы, такие как стили и геометрические штрихи.</span><span class="sxs-lookup"><span data-stu-id="fc77d-144">Device-independent resources, such as stroke styles and geometries.</span></span>

<span data-ttu-id="fc77d-145">Ресурсы, зависящие от устройства, такие как кисти и точечные рисунки, создаются целевым объектом прорисовки.</span><span class="sxs-lookup"><span data-stu-id="fc77d-145">Device-dependent resources, such as brushes and bitmaps, are created by the render target object.</span></span>

![Схема, на которой показана фабрика Direct2D.](images/graphics10.png)

<span data-ttu-id="fc77d-147">Чтобы создать объект фабрики Direct2D, вызовите функцию [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) .</span><span class="sxs-lookup"><span data-stu-id="fc77d-147">To create the Direct2D factory object, call the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function.</span></span>


```C++
ID2D1Factory *pFactory = NULL;

HRESULT hr = D2D1CreateFactory(D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory);
```



<span data-ttu-id="fc77d-148">Первый параметр — это флаг, указывающий параметры создания.</span><span class="sxs-lookup"><span data-stu-id="fc77d-148">The first parameter is a flag that specifies creation options.</span></span> <span data-ttu-id="fc77d-149">**\_ \_ Однопотоковый флаг \_ типа \_ фабрики D2D1** означает, что вы не будете вызывать Direct2D из нескольких потоков.</span><span class="sxs-lookup"><span data-stu-id="fc77d-149">The **D2D1\_FACTORY\_TYPE\_SINGLE\_THREADED** flag means that you will not call Direct2D from multiple threads.</span></span> <span data-ttu-id="fc77d-150">Для поддержки вызовов из нескольких потоков укажите **\_ Тип фабрики D2D1 с \_ \_ несколькими \_ потоками**.</span><span class="sxs-lookup"><span data-stu-id="fc77d-150">To support calls from multiple threads, specify **D2D1\_FACTORY\_TYPE\_MULTI\_THREADED**.</span></span> <span data-ttu-id="fc77d-151">Если программа использует один поток для вызова Direct2D, то однопотоковый вариант является более эффективным.</span><span class="sxs-lookup"><span data-stu-id="fc77d-151">If your program uses a single thread to call into Direct2D, the single-threaded option is more efficient.</span></span>

<span data-ttu-id="fc77d-152">Второй параметр функции [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) получает указатель на интерфейс [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) .</span><span class="sxs-lookup"><span data-stu-id="fc77d-152">The second parameter to the [**D2D1CreateFactory**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) function receives a pointer to the [**ID2D1Factory**](/windows/desktop/api/d2d1/nn-d2d1-id2d1factory) interface.</span></span>

<span data-ttu-id="fc77d-153">Перед первым сообщением [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) необходимо создать объект фабрики Direct2D.</span><span class="sxs-lookup"><span data-stu-id="fc77d-153">You should create the Direct2D factory object before the first [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message.</span></span> <span data-ttu-id="fc77d-154">Для создания фабрики лучше всего создать обработчик сообщений [**WM \_ CREATE**](/windows/desktop/winmsg/wm-create) .</span><span class="sxs-lookup"><span data-stu-id="fc77d-154">The [**WM\_CREATE**](/windows/desktop/winmsg/wm-create) message handler is a good place to create the factory:</span></span>


```C++
    case WM_CREATE:
        if (FAILED(D2D1CreateFactory(
                D2D1_FACTORY_TYPE_SINGLE_THREADED, &pFactory)))
        {
            return -1;  // Fail CreateWindowEx.
        }
        return 0;
```



## <a name="creating-direct2d-resources"></a><span data-ttu-id="fc77d-155">Создание ресурсов Direct2D</span><span class="sxs-lookup"><span data-stu-id="fc77d-155">Creating Direct2D Resources</span></span>

<span data-ttu-id="fc77d-156">Программа Circle использует следующие ресурсы, зависящие от устройства:</span><span class="sxs-lookup"><span data-stu-id="fc77d-156">The Circle program uses the following device-dependent resources:</span></span>

-   <span data-ttu-id="fc77d-157">Целевой объект отрисовки, связанный с окном приложения.</span><span class="sxs-lookup"><span data-stu-id="fc77d-157">A render target that is associated with the application window.</span></span>
-   <span data-ttu-id="fc77d-158">Кисть с сплошным цветом для рисования окружности.</span><span class="sxs-lookup"><span data-stu-id="fc77d-158">A solid-color brush to paint the circle.</span></span>

<span data-ttu-id="fc77d-159">Каждый из этих ресурсов представлен интерфейсом COM:</span><span class="sxs-lookup"><span data-stu-id="fc77d-159">Each of these resources is represented by a COM interface:</span></span>

-   <span data-ttu-id="fc77d-160">Интерфейс [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) представляет целевой объект отрисовки.</span><span class="sxs-lookup"><span data-stu-id="fc77d-160">The [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) interface represents the render target.</span></span>
-   <span data-ttu-id="fc77d-161">Интерфейс [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) представляет кисть.</span><span class="sxs-lookup"><span data-stu-id="fc77d-161">The [**ID2D1SolidColorBrush**](/windows/desktop/api/d2d1/nn-d2d1-id2d1solidcolorbrush) interface represents the brush.</span></span>

<span data-ttu-id="fc77d-162">Программа Circle сохраняет указатели на эти интерфейсы как переменные члена `MainWindow` класса:</span><span class="sxs-lookup"><span data-stu-id="fc77d-162">The Circle program stores pointers to these interfaces as member variables of the `MainWindow` class:</span></span>


```C++
ID2D1HwndRenderTarget   *pRenderTarget;
ID2D1SolidColorBrush    *pBrush;
```



<span data-ttu-id="fc77d-163">Следующий код создает эти два ресурса.</span><span class="sxs-lookup"><span data-stu-id="fc77d-163">The following code creates these two resources.</span></span>


```C++
HRESULT MainWindow::CreateGraphicsResources()
{
    HRESULT hr = S_OK;
    if (pRenderTarget == NULL)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        D2D1_SIZE_U size = D2D1::SizeU(rc.right, rc.bottom);

        hr = pFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &pRenderTarget);

        if (SUCCEEDED(hr))
        {
            const D2D1_COLOR_F color = D2D1::ColorF(1.0f, 1.0f, 0);
            hr = pRenderTarget->CreateSolidColorBrush(color, &pBrush);

            if (SUCCEEDED(hr))
            {
                CalculateLayout();
            }
        }
    }
    return hr;
}
```



<span data-ttu-id="fc77d-164">Чтобы создать целевой объект отрисовки для окна, вызовите метод [**ID2D1Factory:: креатехвндрендертаржет**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) в фабрике Direct2D.</span><span class="sxs-lookup"><span data-stu-id="fc77d-164">To create a render target for a window, call the [**ID2D1Factory::CreateHwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) method on the Direct2D factory.</span></span>

-   <span data-ttu-id="fc77d-165">Первый параметр задает параметры, которые являются общими для любого типа целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="fc77d-165">The first parameter specifies options that are common to any type of render target.</span></span> <span data-ttu-id="fc77d-166">Здесь мы передаем параметры по умолчанию, вызывая вспомогательную функцию [**D2D1:: рендертаржетпропертиес**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).</span><span class="sxs-lookup"><span data-stu-id="fc77d-166">Here, we pass in default options by calling the helper function [**D2D1::RenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-rendertargetproperties).</span></span>
-   <span data-ttu-id="fc77d-167">Второй параметр задает маркер окна и размер целевого объекта отрисовки в пикселях.</span><span class="sxs-lookup"><span data-stu-id="fc77d-167">The second parameter specifies the handle to the window plus the size of the render target, in pixels.</span></span>
-   <span data-ttu-id="fc77d-168">Третий параметр получает указатель [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) .</span><span class="sxs-lookup"><span data-stu-id="fc77d-168">The third parameter receives an [**ID2D1HwndRenderTarget**](/windows/desktop/api/d2d1/nn-d2d1-id2d1hwndrendertarget) pointer.</span></span>

<span data-ttu-id="fc77d-169">Чтобы создать кисть с сплошным цветом, вызовите метод [**ID2D1RenderTarget:: креатесолидколорбруш**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) для целевого объекта прорисовки.</span><span class="sxs-lookup"><span data-stu-id="fc77d-169">To create the solid-color brush, call the [**ID2D1RenderTarget::CreateSolidColorBrush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-createsolidcolorbrush(constd2d1_color_f__id2d1solidcolorbrush)) method on the render target.</span></span> <span data-ttu-id="fc77d-170">Цвет задается как значение [**D2D1 \_ Color \_ F**](/windows/desktop/Direct2D/d2d1-color-f) .</span><span class="sxs-lookup"><span data-stu-id="fc77d-170">The color is given as a [**D2D1\_COLOR\_F**](/windows/desktop/Direct2D/d2d1-color-f) value.</span></span> <span data-ttu-id="fc77d-171">Дополнительные сведения о цветах в Direct2D см. в разделе [Использование цвета в Direct2D](using-color-in-direct2d.md).</span><span class="sxs-lookup"><span data-stu-id="fc77d-171">For more information about colors in Direct2D, see [Using Color in Direct2D](using-color-in-direct2d.md).</span></span>

<span data-ttu-id="fc77d-172">Кроме того, обратите внимание, что если целевой объект прорисовки уже существует, `CreateGraphicsResources` метод возвращает значение **S \_ ОК** без выполнения каких-либо действий.</span><span class="sxs-lookup"><span data-stu-id="fc77d-172">Also, notice that if the render target already exists, the `CreateGraphicsResources` method returns **S\_OK** without doing anything.</span></span> <span data-ttu-id="fc77d-173">Причина этого проекта станет очевидной в следующем разделе.</span><span class="sxs-lookup"><span data-stu-id="fc77d-173">The reason for this design will become clear in the next topic.</span></span>

## <a name="next"></a><span data-ttu-id="fc77d-174">Следующая</span><span class="sxs-lookup"><span data-stu-id="fc77d-174">Next</span></span>

[<span data-ttu-id="fc77d-175">Рисование с использованием Direct2D</span><span class="sxs-lookup"><span data-stu-id="fc77d-175">Drawing with Direct2D</span></span>](drawing-with-direct2d.md)

 

 