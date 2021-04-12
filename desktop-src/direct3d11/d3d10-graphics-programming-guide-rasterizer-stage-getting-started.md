---
title: начало работы с этапом средства прорисовки
description: В этом разделе описывается настройка окна просмотра, прямоугольника ножниц, состояния средства прорисовки и множественная выборка.
ms.assetid: d78c3845-76fd-4bd7-a603-bb1d8c66ac49
keywords:
- многовыборка, состояние средства отображения программной прорисовки (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ac95a15221f6fd4bd422e96c0686816afb35d4e8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104337580"
---
# <a name="getting-started-with-the-rasterizer-stage"></a><span data-ttu-id="2f2cb-104">начало работы с этапом средства прорисовки</span><span class="sxs-lookup"><span data-stu-id="2f2cb-104">Getting Started with the Rasterizer Stage</span></span>

<span data-ttu-id="2f2cb-105">В этом разделе описывается настройка окна просмотра, прямоугольника ножниц, состояния средства прорисовки и множественная выборка.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-105">This section describes setting the viewport, the scissors rectangle, the rasterizer state, and multi-sampling.</span></span>

## <a name="set-the-viewport"></a><span data-ttu-id="2f2cb-106">Задание окна просмотра</span><span class="sxs-lookup"><span data-stu-id="2f2cb-106">Set the Viewport</span></span>

<span data-ttu-id="2f2cb-107">Окно просмотра сопоставляет позиции вершины (в пространстве обрезки) с положениями целевого объекта отрисовки.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-107">A viewport maps vertex positions (in clip space) into render target positions.</span></span> <span data-ttu-id="2f2cb-108">На этом шаге трехмерные позиции масштабируются в двухмерном пространстве.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-108">This step scales the 3D positions into 2D space.</span></span> <span data-ttu-id="2f2cb-109">Цель прорисовки ориентирована на оси Y, указывающие вниз. для этого необходимо, чтобы координаты Y были отражены в масштабе окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-109">A render target is oriented with the Y axes pointing down; this requires that the Y coordinates get flipped during the viewport scale.</span></span> <span data-ttu-id="2f2cb-110">Кроме того, экстенты x и y (диапазон значений x и y) масштабируются в соответствии с размером окна просмотра согласно следующим формулам:</span><span class="sxs-lookup"><span data-stu-id="2f2cb-110">In addition, the x and y extents (range of the x and y values) are scaled to fit the viewport size according to the following formulas:</span></span>


```
X = (X + 1) * Viewport.Width * 0.5 + Viewport.TopLeftX
Y = (1 - Y) * Viewport.Height * 0.5 + Viewport.TopLeftY
Z = Viewport.MinDepth + Z * (Viewport.MaxDepth - Viewport.MinDepth) 
```



<span data-ttu-id="2f2cb-111">В этом руководстве 1 создается окно просмотра 640 × 480 с помощью [**\_ окна просмотра D3D11**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) и вызывается [**ссылку ID3D11DeviceContext:: рссетвиевпортс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).</span><span class="sxs-lookup"><span data-stu-id="2f2cb-111">Tutorial 1 creates a 640 × 480 viewport using [**D3D11\_VIEWPORT**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_viewport) and by calling [**ID3D11DeviceContext::RSSetViewports**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetviewports).</span></span>


```
    D3D11_VIEWPORT vp[1];
    vp[0].Width = 640.0f;
    vp[0].Height = 480.0f;
    vp[0].MinDepth = 0;
    vp[0].MaxDepth = 1;
    vp[0].TopLeftX = 0;
    vp[0].TopLeftY = 0;
    g_pd3dDevice->RSSetViewports( 1, vp );
```



<span data-ttu-id="2f2cb-112">В описании окна просмотра указывается размер окна просмотра, диапазон для отображения глубины (с помощью *миндепс* и *MaxDepth*) и расположение верхнего левого края окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-112">The viewport description specifies the size of the viewport, the range to map depth to (using *MinDepth* and *MaxDepth*), and the placement of the top left of the viewport.</span></span> <span data-ttu-id="2f2cb-113">*Миндепс* должно быть меньше или равно *MaxDepth*; диапазоны для *миндепс* и *MaxDepth* находятся в диапазоне от 0,0 до 1,0 включительно.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-113">*MinDepth* must be less than or equal to *MaxDepth*; the range for both *MinDepth* and *MaxDepth* is between 0.0 and 1.0, inclusive.</span></span> <span data-ttu-id="2f2cb-114">Обычно окно просмотра сопоставляется с целевым объектом отрисовки, но не является обязательным. Кроме того, окно просмотра не обязательно должно иметь тот же размер или расположение, что и целевой объект рендеринга.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-114">It is common for the viewport to map to a render target but it is not necessary; additionally, the viewport does not have to have the same size or position as the render target.</span></span>

<span data-ttu-id="2f2cb-115">Можно создать массив окна просмотра, но только один из них можно применить к примитивным выходным данным из шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-115">You can create an array of viewports, but only one can be applied to a primitive output from the geometry shader.</span></span> <span data-ttu-id="2f2cb-116">Одновременно можно задать только одно окно просмотра.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-116">Only one viewport can be set active at a time.</span></span> <span data-ttu-id="2f2cb-117">В процессе растрирования конвейер использует окно просмотра по умолчанию (и прямоугольный прямоугольник, который обсуждается в следующем разделе).</span><span class="sxs-lookup"><span data-stu-id="2f2cb-117">The pipeline uses a default viewport (and scissor rectangle, discussed in the next section) during rasterization.</span></span> <span data-ttu-id="2f2cb-118">Значение по умолчанию всегда является первым окном просмотра (или прямоугольным прямоугольником) в массиве.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-118">The default is always the first viewport (or scissor rectangle) in the array.</span></span> <span data-ttu-id="2f2cb-119">Для выполнения примитивного выбора окна просмотра в шейдере Geometry укажите семантику Виевпортаррайиндекс для соответствующего компонента вывода GS в объявлении выходной подписи GS.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-119">To perform a per-primitive selection of the viewport in the geometry shader, specify the ViewportArrayIndex semantic on the appropriate GS output component in the GS output signature declaration.</span></span>

<span data-ttu-id="2f2cb-120">Максимальное количество окна просмотра (и прямоугольных прямоугольников), которое может быть привязано к этапу средства прорисовки в любой момент времени, равно 16 (задается в окне **\_ просмотра D3D11 \_ и \_ \_ число объектов сЦиссоррект \_ \_ на \_ конвейер**).</span><span class="sxs-lookup"><span data-stu-id="2f2cb-120">The maximum number of viewports (and scissor rectangles) that can be bound to the rasterizer stage at any one time is 16 (specified by **D3D11\_VIEWPORT\_AND\_SCISSORRECT\_OBJECT\_COUNT\_PER\_PIPELINE**).</span></span>

## <a name="set-the-scissor-rectangle"></a><span data-ttu-id="2f2cb-121">Задать прямоугольный прямоугольник</span><span class="sxs-lookup"><span data-stu-id="2f2cb-121">Set the Scissor Rectangle</span></span>

<span data-ttu-id="2f2cb-122">Прямоугольный прямоугольник дает еще одну возможность уменьшить количество пикселей, которые будут отправлены на этап слияния выходных данных.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-122">A scissor rectangle gives you another opportunity to reduce the number of pixels that will be sent to the output merger stage.</span></span> <span data-ttu-id="2f2cb-123">Пиксели за пределами прямоугольной прямоугольной области отбрасываются.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-123">Pixels outside of the scissor rectangle are discarded.</span></span> <span data-ttu-id="2f2cb-124">Размер прямоугольной прямоугольной области задается в целых числах.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-124">The size of the scissor rectangle is specified in integers.</span></span> <span data-ttu-id="2f2cb-125">Только один прямоугольный прямоугольник (на основе *виевпортаррайиндекс* в [семантике системных значений](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) можно применить к треугольнику во время растрирования.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-125">Only one scissor rectangle (based on *ViewportArrayIndex* in [system value semantics](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)) can be applied to a triangle during rasterization.</span></span>

<span data-ttu-id="2f2cb-126">Чтобы включить прямоугольный прямоугольник, используйте элемент *сЦиссоренабле* (в [**D3D11 \_ растеризации \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span><span class="sxs-lookup"><span data-stu-id="2f2cb-126">To enable the scissor rectangle, use the *ScissorEnable* member (in [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span> <span data-ttu-id="2f2cb-127">Прямоугольный прямоугольник по умолчанию является пустым прямоугольником; то есть все значения Rect равны 0.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-127">The default scissor rectangle is an empty rectangle; that is, all rect values are 0.</span></span> <span data-ttu-id="2f2cb-128">Иными словами, если не настроить прямоугольный прямоугольник и ножницы включены, вы не будете пересылать Пиксели на этап слияния вывода.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-128">In other words, if you do not set up the scissor rectangle and scissor is enabled, you will not send any pixels to the output-merger stage.</span></span> <span data-ttu-id="2f2cb-129">Наиболее распространенной установкой является инициализация прямоугольного прямоугольника до размера окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-129">The most common setup is to initialize the scissor rectangle to the size of the viewport.</span></span>

<span data-ttu-id="2f2cb-130">Чтобы задать для устройства массив прямоугольных прямоугольников, вызовите [**ссылку ID3D11DeviceContext:: рссетсЦиссорректс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) с [**D3D11 \_ Rect**](d3d11-rect.md).</span><span class="sxs-lookup"><span data-stu-id="2f2cb-130">To set an array of scissor rectangles to the device, call [**ID3D11DeviceContext::RSSetScissorRects**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-rssetscissorrects) with [**D3D11\_RECT**](d3d11-rect.md).</span></span>


```
D3D11_RECT rects[1];
  rects[0].left = 0;
  rects[0].right = 640;
  rects[0].top = 0;
  rects[0].bottom = 480;

  D3DDevice->RSSetScissorRects( 1, rects );
```



<span data-ttu-id="2f2cb-131">Этот метод принимает два параметра: (1) число прямоугольников в массиве и (2) массив прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-131">This method takes two parameters: (1) the number of rectangles in the array and (2) an array of rectangles.</span></span>

<span data-ttu-id="2f2cb-132">Конвейер использует индекс прямоугольной области по умолчанию во время растрирования (по умолчанию это прямоугольник нулевого размера с отключенной обрезками).</span><span class="sxs-lookup"><span data-stu-id="2f2cb-132">The pipeline uses a default scissor rectangle index during rasterization (the default is a zero-size rectangle with clipping disabled).</span></span> <span data-ttu-id="2f2cb-133">Чтобы переопределить это, укажите в \_ объявлении выходной сигнатуры GS семантику SV виевпортаррайиндекс для выходного компонента GS.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-133">To override this, specify the SV\_ViewportArrayIndex semantic to a GS output component in the GS output signature declaration.</span></span> <span data-ttu-id="2f2cb-134">Это приведет к тому, что этап GS пометит этот компонент вывода GS в качестве компонента, созданного системой, с этой семантикой.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-134">This will cause the GS stage to mark this GS output component as a system-generated component with this semantic.</span></span> <span data-ttu-id="2f2cb-135">Этап средства развертки распознает эту семантику и будет использовать параметр, к которому он присоединен, в качестве индекса прямоугольной прямоугольной области для доступа к массиву прямоугольных прямоугольников.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-135">The rasterizer stage recognizes this semantic and will use the parameter it is attached to as the scissor rectangle index to access the array of scissor rectangles.</span></span> <span data-ttu-id="2f2cb-136">Не забудьте сообщить этапу средства создания программной прорисовки, что вы определили, какой прямоугольный прямоугольник задаете, включив значение *сЦиссоренабле* в описании средства программной прорисовки перед созданием объекта средства программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-136">Don't forget to tell the rasterizer stage to use the scissor rectangle that you define by enabling the *ScissorEnable* value in the rasterizer description before creating the rasterizer object.</span></span>

## <a name="set-rasterizer-state"></a><span data-ttu-id="2f2cb-137">Задать состояние средства отображения программной прорисовки</span><span class="sxs-lookup"><span data-stu-id="2f2cb-137">Set Rasterizer State</span></span>

<span data-ttu-id="2f2cb-138">Начиная с Direct3D 10, состояние средства программной прорисовки инкапсулируется в объекте состояния средства программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-138">Beginning with Direct3D 10, rasterizer state is encapsulated in a rasterizer state object.</span></span> <span data-ttu-id="2f2cb-139">Можно создать до 4096 объектов состояния средства прорисовки, которые затем можно задать для устройства, передав обработчик в объект State.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-139">You may create up to 4096 rasterizer state objects which can then be set to the device by passing a handle to the state object.</span></span>

<span data-ttu-id="2f2cb-140">Используйте [**ID3D11Device1:: CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) для создания объекта состояния средства программной прорисовки из описания средства создания программной прорисовки (см. раздел [**D3D11 \_ растеризации \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span><span class="sxs-lookup"><span data-stu-id="2f2cb-140">Use [**ID3D11Device1::CreateRasterizerState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createrasterizerstate1) to create a rasterizer state object from a rasterizer description (see [**D3D11\_RASTERIZER\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1)).</span></span>


```
    ID3D11RasterizerState1 * g_pRasterState;

    D3D11_RASTERIZER_DESC1 rasterizerState;
    rasterizerState.FillMode = D3D11_FILL_SOLID;
    rasterizerState.CullMode = D3D11_CULL_FRONT;
    rasterizerState.FrontCounterClockwise = true;
    rasterizerState.DepthBias = false;
    rasterizerState.DepthBiasClamp = 0;
    rasterizerState.SlopeScaledDepthBias = 0;
    rasterizerState.DepthClipEnable = true;
    rasterizerState.ScissorEnable = true;
    rasterizerState.MultisampleEnable = false;
    rasterizerState.AntialiasedLineEnable = false;
    rasterizerState.ForcedSampleCount = 0;
    pd3dDevice->CreateRasterizerState1( &rasterizerState, &g_pRasterState );
```



<span data-ttu-id="2f2cb-141">В этом примере набора состояний может быть, возможно, самая базовая настройка средства программной прорисовки:</span><span class="sxs-lookup"><span data-stu-id="2f2cb-141">This example set of state accomplishes perhaps the most basic rasterizer setup:</span></span>

-   <span data-ttu-id="2f2cb-142">Режим сплошной заливки</span><span class="sxs-lookup"><span data-stu-id="2f2cb-142">Solid fill mode</span></span>
-   <span data-ttu-id="2f2cb-143">Изъятие или удаление задних граней; Предполагаемый порядок поворота по часовой стрелке для примитивов</span><span class="sxs-lookup"><span data-stu-id="2f2cb-143">Cull out or remove back faces; assume counter-clockwise winding order for primitives</span></span>
-   <span data-ttu-id="2f2cb-144">Отключить смещение глубины, но включить буферизацию глубины и включить прямоугольный прямоугольник</span><span class="sxs-lookup"><span data-stu-id="2f2cb-144">Turn off depth bias but enable depth buffering and enable the scissor rectangle</span></span>
-   <span data-ttu-id="2f2cb-145">Отключение многовыборочной и многострочного сглаживания</span><span class="sxs-lookup"><span data-stu-id="2f2cb-145">Turn off multisampling and line anti-aliasing</span></span>

<span data-ttu-id="2f2cb-146">Кроме того, базовые операции программной прорисовки всегда включают следующее: обрезка (в представлении фрустум), деление перспективы и масштаб окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-146">In addition, basic rasterizer operations, always include the following: clipping (to the view frustum), perspective divide, and the viewport scale.</span></span> <span data-ttu-id="2f2cb-147">После успешного создания объекта состояния средства программной прорисовки задайте устройство следующим образом:</span><span class="sxs-lookup"><span data-stu-id="2f2cb-147">After successfully creating the rasterizer state object, set it to the device like this:</span></span>


```
    pd3dDevice->RSSetState(g_pRasterState);
```



### <a name="multisampling"></a><span data-ttu-id="2f2cb-148">Множественная дискретизация</span><span class="sxs-lookup"><span data-stu-id="2f2cb-148">Multisampling</span></span>

<span data-ttu-id="2f2cb-149">Множественная выборка демонстрирует некоторые или все компоненты изображения с более высоким разрешением (за которым следует понижение до исходного разрешения), чтобы уменьшить наиболее видимую форму псевдонимов, вызванную рисованием краев многоугольников.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-149">Multisampling samples some or all of the components of an image at a higher resolution (followed by downsampling to the original resolution) to reduce the most visible form of aliasing caused by drawing polygon edges.</span></span> <span data-ttu-id="2f2cb-150">Несмотря на то, что для множественной выборки требуются образцы в виде фрагментов, в современных GPU реализуется многовыборка, чтобы построитель текстуры выполнялся один раз на пиксель.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-150">Even though multisampling requires sub-pixel samples, modern GPU's implement multisampling so that a pixel shader runs once per pixel.</span></span> <span data-ttu-id="2f2cb-151">Это обеспечивает приемлемый компромисс между производительностью (особенно в приложении, привязанном к GPU) и сглаживанием окончательного образа.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-151">This provides an acceptable tradeoff between performance (especially in a GPU bound application) and anti-aliasing the final image.</span></span>

<span data-ttu-id="2f2cb-152">Чтобы использовать многофакторную выборку, задайте поле Enable в [**описании растрирования**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), создайте целевой объект рендеринга с множественной выборкой и либо прочтите целевой объект отрисовки с помощью шейдера, чтобы разрешить выборку в один цвет пикселя, либо вызовите [**ссылку ID3D11DeviceContext:: ресолвесубресаурце**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) для разрешения образцов с помощью видеоадаптера.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-152">To use multisampling, set the enable field in the [**rasterization description**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_rasterizer_desc1), create a multisampled render target, and either read the render target with a shader to resolve the samples into a single pixel color or call [**ID3D11DeviceContext::ResolveSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-resolvesubresource) to resolve the samples using the video card.</span></span> <span data-ttu-id="2f2cb-153">Наиболее распространенным сценарием является прорисовка в один или несколько целевых объектов рендеринга с несколькими примерами.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-153">The most common scenario is to draw to one or more multisampled render targets.</span></span>

<span data-ttu-id="2f2cb-154">Многовыборочная выборка не зависит от того, используется ли образец маски, включено [альфа-покрытие](d3d10-graphics-programming-guide-blend-state.md) или операции с наборами элементов (которые всегда выполняются по образцу).</span><span class="sxs-lookup"><span data-stu-id="2f2cb-154">Multisampling is independent of whether or not a sample mask is used, [alpha-to-coverage](d3d10-graphics-programming-guide-blend-state.md) is enabled, or stencil operations (which are always performed per-sample).</span></span>

<span data-ttu-id="2f2cb-155">На тестирование глубины влияет множественная выборка:</span><span class="sxs-lookup"><span data-stu-id="2f2cb-155">Depth testing is affected by multisampling:</span></span>

-   <span data-ttu-id="2f2cb-156">Если включена многовыборочная выборка, для выборки глубины используется интерполяция, а для каждого образца выполняется проверка глубины и трафарета. выходной цвет шейдера пикселей дублируется для всех передаваемых образцов.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-156">When multisampling is enabled, depth is interpolated per sample and the depth/stencil test is done per sample; the pixel shader output color is duplicated for all passing samples.</span></span> <span data-ttu-id="2f2cb-157">Если глубина выходных данных шейдера пикселей превышает глубину, значение глубины дублируется для всех выборок (хотя этот сценарий теряет преимущество многовыборки).</span><span class="sxs-lookup"><span data-stu-id="2f2cb-157">If the pixel shader outputs depth, the depth value is duplicated for all samples (although this scenario loses the benefit of multisampling).</span></span>
-   <span data-ttu-id="2f2cb-158">Если множественная выборка отключена, тестирование глубины и набора элементов по-прежнему выполняется для каждого образца, но глубина не поддается интерполяции по образцу.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-158">When multisampling is disabled, depth/stencil testing is still done per-sample, but depth is not interpolated per-sample.</span></span>

<span data-ttu-id="2f2cb-159">Не существует ограничений на смешивание многовыборочной и многовыборочной отрисовки в пределах одного целевого объекта рендеринга.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-159">There are no restrictions for mixing multisampled and non-multisampled rendering within a single render target.</span></span> <span data-ttu-id="2f2cb-160">Если включить многофакторную выборку и нарисовать на целевой объект рендеринга, не являющийся множественной выборкой, то результат будет таким же, как если бы многовыборочная выборка не была включена. выборка выполняется с одним примером на пиксель.</span><span class="sxs-lookup"><span data-stu-id="2f2cb-160">If you enable multisampling and draw to a non-multisampled render target, you produce the same result as if multisampling were not enabled; sampling is done with a single sample per-pixel.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2f2cb-161">См. также</span><span class="sxs-lookup"><span data-stu-id="2f2cb-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f2cb-162">Этап растеризации</span><span class="sxs-lookup"><span data-stu-id="2f2cb-162">Rasterizer Stage</span></span>](d3d10-graphics-programming-guide-rasterizer-stage.md)
</dt> </dl>

 

 