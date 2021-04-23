---
title: Настройка функций смешения
description: Операции смешения выполняются на всех выходных данных шейдера пикселей (значение RGBA) перед записью выходного значения в целевой объект отрисовки. Если включена многовыборка, смешивание выполняется для каждого мультисэмплинга; в противном случае смешивание выполняется для каждого пикселя.
ms.assetid: f5c79baf-7bd3-4f58-abe7-8e96cd6be9d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08acf1ea286b29a1cb96873bbfe170c6f38699f7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997063"
---
# <a name="configuring-blending-functionality"></a><span data-ttu-id="6b779-104">Настройка функций смешения</span><span class="sxs-lookup"><span data-stu-id="6b779-104">Configuring Blending Functionality</span></span>

<span data-ttu-id="6b779-105">Операции смешения выполняются на всех выходных данных шейдера пикселей (значение RGBA) перед записью выходного значения в целевой объект отрисовки.</span><span class="sxs-lookup"><span data-stu-id="6b779-105">Blending operations are performed on every pixel shader output (RGBA value) before the output value is written to a render target.</span></span> <span data-ttu-id="6b779-106">Если включена многовыборка, смешивание выполняется для каждого мультисэмплинга; в противном случае смешивание выполняется для каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="6b779-106">If multisampling is enabled, blending is done on each multisample; otherwise, blending is performed on each pixel.</span></span>

-   [<span data-ttu-id="6b779-107">Создание состояния смешения</span><span class="sxs-lookup"><span data-stu-id="6b779-107">Create the Blend State</span></span>](#create-the-blend-state)
-   [<span data-ttu-id="6b779-108">Привязка состояния смешения</span><span class="sxs-lookup"><span data-stu-id="6b779-108">Bind the Blend State</span></span>](#bind-the-blend-state)
-   [<span data-ttu-id="6b779-109">Разделы, посвященные расширенному смешению</span><span class="sxs-lookup"><span data-stu-id="6b779-109">Advanced Blending Topics</span></span>](#advanced-blending-topics)
    -   [<span data-ttu-id="6b779-110">Альфа-версия</span><span class="sxs-lookup"><span data-stu-id="6b779-110">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
    -   [<span data-ttu-id="6b779-111">Выходные данные шейдера пикселей смешения</span><span class="sxs-lookup"><span data-stu-id="6b779-111">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)
-   [<span data-ttu-id="6b779-112">См. также</span><span class="sxs-lookup"><span data-stu-id="6b779-112">Related topics</span></span>](#related-topics)

## <a name="create-the-blend-state"></a><span data-ttu-id="6b779-113">Создание состояния смешения</span><span class="sxs-lookup"><span data-stu-id="6b779-113">Create the Blend State</span></span>

<span data-ttu-id="6b779-114">Состояние смешения — это коллекция состояний, используемых для управления наложением.</span><span class="sxs-lookup"><span data-stu-id="6b779-114">The blend state is a collection of states used to control blending.</span></span> <span data-ttu-id="6b779-115">Эти состояния (определенные в [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) используются для создания объекта состояния смешения путем вызова [**ID3D11Device1:: CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).</span><span class="sxs-lookup"><span data-stu-id="6b779-115">These states (defined in [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1)) are used to create the blend state object by calling [**ID3D11Device1::CreateBlendState1**](/windows/desktop/api/D3D11_1/nf-d3d11_1-id3d11device1-createblendstate1).</span></span>

<span data-ttu-id="6b779-116">Например, ниже приведен очень простой пример создания состояния смешения, который отключает альфа-смешение и не использует маскирование пикселов для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="6b779-116">For instance, here is a very simple example of blend-state creation that disables alpha blending and uses no per-component pixel masking.</span></span>


```
ID3D11BlendState1* g_pBlendStateNoBlend = NULL;

D3D11_BLEND_DESC1 BlendState;
ZeroMemory(&BlendState, sizeof(D3D11_BLEND_DESC1));
BlendState.RenderTarget[0].BlendEnable = FALSE;
BlendState.RenderTarget[0].RenderTargetWriteMask = D3D11_COLOR_WRITE_ENABLE_ALL;
pd3dDevice->CreateBlendState1(&BlendState, &g_pBlendStateNoBlend);
```



<span data-ttu-id="6b779-117">Этот пример похож на [Пример HLSLWithoutFX10](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="6b779-117">This example is similar to the [HLSLWithoutFX10 Sample](https://msdn.microsoft.com/library/Ee416414(v=VS.85).aspx).</span></span>

## <a name="bind-the-blend-state"></a><span data-ttu-id="6b779-118">Привязка состояния смешения</span><span class="sxs-lookup"><span data-stu-id="6b779-118">Bind the Blend State</span></span>

<span data-ttu-id="6b779-119">После создания объекта состояния Blend привяжите объект состояния Blend к этапу слияния вывода путем вызова [**ссылку ID3D11DeviceContext:: омсетблендстате**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).</span><span class="sxs-lookup"><span data-stu-id="6b779-119">After you create the blend-state object, bind the blend-state object to the output-merger stage by calling [**ID3D11DeviceContext::OMSetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetblendstate).</span></span>


```
float blendFactor[4] = { 0.0f, 0.0f, 0.0f, 0.0f };
UINT sampleMask   = 0xffffffff;

pd3dDevice->OMSetBlendState(g_pBlendStateNoBlend, blendFactor, sampleMask);
```



<span data-ttu-id="6b779-120">Этот API принимает три параметра: объект состояния Blend, коэффициент смешения четырех компонентов и пример маски.</span><span class="sxs-lookup"><span data-stu-id="6b779-120">This API takes three parameters: the blend-state object, a four-component blend factor, and a sample mask.</span></span> <span data-ttu-id="6b779-121">Можно передать **значение NULL** для объекта режима Blend, чтобы указать состояние смешения по умолчанию или передать объект состояния Blend.</span><span class="sxs-lookup"><span data-stu-id="6b779-121">You can pass in **NULL** for the blend-state object to specify the default blend state or pass in a blend-state object.</span></span> <span data-ttu-id="6b779-122">Если вы создали объект-состояние Blend с [**\_ \_ \_ коэффициентом смешения D3D11 Blend**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) или [**D3D11 \_ Blend \_ Inv \_ \_**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), можно передать коэффициент смешения для модуляции значений для шейдера пикселей, целевого объекта прорисовки или и того и другого.</span><span class="sxs-lookup"><span data-stu-id="6b779-122">If you created the blend-state object with [**D3D11\_BLEND\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend) or [**D3D11\_BLEND\_INV\_BLEND\_FACTOR**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_blend), you can pass a blend factor to modulate values for the pixel shader, render target, or both.</span></span> <span data-ttu-id="6b779-123">Если вы не создали объект состояния Blend с коэффициентом **\_ \_ смешения D3D11 \_ Blend** или **D3D11 \_ Blend \_ Inv \_ \_**, вы по-прежнему можете передать коэффициент смешения, отличный от NULL, но на этапе смешения не используется коэффициент смешения; среда выполнения сохраняет коэффициент смешения, и позднее можно вызвать [**ссылку ID3D11DeviceContext:: омжетблендстате**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) , чтобы получить коэффициент смешения.</span><span class="sxs-lookup"><span data-stu-id="6b779-123">If you didn't create the blend-state object with **D3D11\_BLEND\_BLEND\_FACTOR** or **D3D11\_BLEND\_INV\_BLEND\_FACTOR**, you can still pass a non-NULL blend factor, but the blending stage does not use the blend factor; the runtime stores the blend factor, and you can later call [**ID3D11DeviceContext::OMGetBlendState**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omgetblendstate) to retrieve the blend factor.</span></span> <span data-ttu-id="6b779-124">Если передать **значение NULL**, среда выполнения использует или сохраняет коэффициент смешения, равный {1, 1, 1, 1}.</span><span class="sxs-lookup"><span data-stu-id="6b779-124">If you pass **NULL**, the runtime uses or stores a blend factor equal to { 1, 1, 1, 1 }.</span></span> <span data-ttu-id="6b779-125">Образец маски — это определяемая пользователем маска, которая определяет способ выборки существующего целевого объекта отрисовки перед его обновлением.</span><span class="sxs-lookup"><span data-stu-id="6b779-125">The sample mask is a user-defined mask that determines how to sample the existing render target before updating it.</span></span> <span data-ttu-id="6b779-126">Маска выборки по умолчанию — 0xFFFFFFFF, которая обозначает выборку точек.</span><span class="sxs-lookup"><span data-stu-id="6b779-126">The default sampling mask is 0xffffffff which designates point sampling.</span></span>

<span data-ttu-id="6b779-127">В самых глубоких схемах буферизации точка, ближайшая к камере, — это тот, который рисуется.</span><span class="sxs-lookup"><span data-stu-id="6b779-127">In most depth buffering schemes, the pixel closest to the camera is the one that gets drawn.</span></span> <span data-ttu-id="6b779-128">При [настройке состояния трафарета глубины](d3d10-graphics-programming-guide-depth-stencil.md)элемент **Депсфунк** [**\_ шаблона глубины D3D11 \_ \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) может быть любым [**D3D11ным \_ сравнением \_ Func**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func).</span><span class="sxs-lookup"><span data-stu-id="6b779-128">When [setting up the depth stencil state](d3d10-graphics-programming-guide-depth-stencil.md), the **DepthFunc** member of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc) can be any [**D3D11\_COMPARISON\_FUNC**](/windows/desktop/api/D3D11/ne-d3d11-d3d11_comparison_func).</span></span> <span data-ttu-id="6b779-129">Как правило, необходимо, чтобы **Депсфунк** **D3D11 \_ Сравнение \_**, так что пикселы, ближайшие к камере, будут перезаписывать Пиксели, находящиеся за ними.</span><span class="sxs-lookup"><span data-stu-id="6b779-129">Normally, you would want **DepthFunc** to be **D3D11\_COMPARISON\_LESS**, so that the pixels closest to the camera will overwrite the pixels behind them.</span></span> <span data-ttu-id="6b779-130">Однако в зависимости от потребностей приложения для тестирования глубины можно использовать любые другие функции сравнения.</span><span class="sxs-lookup"><span data-stu-id="6b779-130">However, depending on the needs of your application, any of the other comparison functions may be used to do the depth test.</span></span>

## <a name="advanced-blending-topics"></a><span data-ttu-id="6b779-131">Разделы, посвященные расширенному смешению</span><span class="sxs-lookup"><span data-stu-id="6b779-131">Advanced Blending Topics</span></span>

-   [<span data-ttu-id="6b779-132">Альфа-версия</span><span class="sxs-lookup"><span data-stu-id="6b779-132">Alpha-To-Coverage</span></span>](#alpha-to-coverage)
-   [<span data-ttu-id="6b779-133">Выходные данные шейдера пикселей смешения</span><span class="sxs-lookup"><span data-stu-id="6b779-133">Blending Pixel Shader Outputs</span></span>](#blending-pixel-shader-outputs)

### <a name="alpha-to-coverage"></a><span data-ttu-id="6b779-134">Альфа-версия</span><span class="sxs-lookup"><span data-stu-id="6b779-134">Alpha-To-Coverage</span></span>

<span data-ttu-id="6b779-135">Альфа-версия — это метод многофакторной выборки, который наиболее удобен для таких ситуаций, как сжатый фолиаже, где имеется несколько перекрывающихся многоугольников, которые используют альфа-прозрачность для определения краев внутри поверхности.</span><span class="sxs-lookup"><span data-stu-id="6b779-135">Alpha-to-coverage is a multisampling technique that is most useful for situations such as dense foliage where there are several overlapping polygons that use alpha transparency to define edges within the surface.</span></span>

<span data-ttu-id="6b779-136">Вы можете использовать элемент **алфатоковеражеенабле** из [**D3D11 \_ Blend \_ DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) или [**D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) , чтобы указать, будет ли среда выполнения преобразовывать. компонент (альфа) выходной регистр [( \_](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)Alpha) из шейдера пикселей в n-этапную маску покрытия (с учетом n-примерного **рендертаржет**).</span><span class="sxs-lookup"><span data-stu-id="6b779-136">You can use the **AlphaToCoverageEnable** member of [**D3D11\_BLEND\_DESC1**](/windows/desktop/api/D3D11_1/ns-d3d11_1-cd3d11_blend_desc1) or [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc) to toggle whether the runtime converts the .a component (alpha) of output register [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 from the pixel shader to an n-step coverage mask (given an n-sample **RenderTarget**).</span></span> <span data-ttu-id="6b779-137">Среда выполнения выполняет операцию **и** для этой маски с типичным примером покрытия для пикселя в примитиве (в дополнение к образцу маски), чтобы определить, какие примеры следует обновить во всех активных **рендертаржет**.</span><span class="sxs-lookup"><span data-stu-id="6b779-137">The runtime performs an **AND** operation of this mask with the typical sample coverage for the pixel in the primitive (in addition to the sample mask) to determine which samples to update in all the active **RenderTarget** s.</span></span>

<span data-ttu-id="6b779-138">Если построитель текстуры выводит данные о [ \_ покрытии](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), среда выполнения отключает альфа-покрытие.</span><span class="sxs-lookup"><span data-stu-id="6b779-138">If the pixel shader outputs [SV\_Coverage](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics), the runtime disables alpha-to-coverage.</span></span>

> [!Note]  
> <span data-ttu-id="6b779-139">При многовыборочной обработке среда выполнения использует только одно покрытие для всех **рендертаржет**.</span><span class="sxs-lookup"><span data-stu-id="6b779-139">In multisampling, the runtime shares only one coverage for all **RenderTarget** s.</span></span> <span data-ttu-id="6b779-140">Тот факт, что среда выполнения считывает и преобразует. из выходной [позиции \_ ОКП](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 в покрытие, когда **алфатоковеражеенабле** имеет значение true, не изменяет. значение, которое передается в режим смешения по **рендертаржет** 0 (если **рендертаржет** нужно задать).</span><span class="sxs-lookup"><span data-stu-id="6b779-140">The fact that the runtime reads and converts .a from output [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0 to coverage when **AlphaToCoverageEnable** is TRUE does not change the .a value that goes to the blender at **RenderTarget** 0 (if a **RenderTarget** happens to be set there).</span></span> <span data-ttu-id="6b779-141">В общем случае, если включить альфа-покрытие, вы не повлияете на то, как все цветовые выводы шейдеров пикселей взаимодействуют с **рендертаржет** s через [стадию слияния (Output-слиянием](d3d10-graphics-programming-guide-output-merger-stage.md) ), за исключением того, что среда выполнения выполняет операцию **и** маску покрытия с маской альфа-покрытия.</span><span class="sxs-lookup"><span data-stu-id="6b779-141">In general, if you enable alpha-to-coverage, you don't affect how all color outputs from pixel shaders interact with **RenderTarget** s through the [output-merger stage](d3d10-graphics-programming-guide-output-merger-stage.md) except that the runtime performs an **AND** operation of the coverage mask with the alpha-to-coverage mask.</span></span> <span data-ttu-id="6b779-142">Альфа-к покрытию работает независимо от того, может ли среда выполнения смешивать **рендертаржет** или использовать смешивание в **рендертаржет**.</span><span class="sxs-lookup"><span data-stu-id="6b779-142">Alpha-to-coverage works independently to whether the runtime can blend **RenderTarget** or whether you use blending on **RenderTarget**.</span></span>

 

<span data-ttu-id="6b779-143">Графическое оборудование не точно указывает, как оно преобразует построитель текстуры [ОКП в \_ мишень](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0. a (альфа) в маску покрытия, за исключением того, что альфа-канал 0 (или меньше) должен сопоставляться с покрытием, а альфа-канал 1 (или больше) должен сопоставляться с полным покрытием (перед выполнением операции **и** с фактическим покрытием примитивов).</span><span class="sxs-lookup"><span data-stu-id="6b779-143">Graphics hardware doesn't precisely specify exactly how it converts pixel shader [SV\_Target](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-semantics)0.a (alpha) to a coverage mask, except that alpha of 0 (or less) must map to no coverage and alpha of 1 (or greater) must map to full coverage (before the runtime performs an **AND** operation with actual primitive coverage).</span></span> <span data-ttu-id="6b779-144">Так как альфа-канал переходит от 0 к 1, результирующий объем обычно увеличивается монотонно.</span><span class="sxs-lookup"><span data-stu-id="6b779-144">As alpha goes from 0 to 1, the resulting coverage should generally increase monotonically.</span></span> <span data-ttu-id="6b779-145">Тем не менее, оборудование может выполнять дизеринг участка, чтобы обеспечить более дискретизация альфа-значений за счет пространственного разрешения и шума.</span><span class="sxs-lookup"><span data-stu-id="6b779-145">However, hardware might perform area dithering to provide some better quantization of alpha values at the cost of spatial resolution and noise.</span></span> <span data-ttu-id="6b779-146">Альфа-значение NaN (не число) приводит к отсутствию покрытия (нулевой) маски.</span><span class="sxs-lookup"><span data-stu-id="6b779-146">An alpha value of NaN (Not a Number) results in a no coverage (zero) mask.</span></span>

<span data-ttu-id="6b779-147">Альфа-к покрытию также традиционно используется для прозрачности экранной дверцы или для определения подробного силхауеттес для непрозрачных других спрайтов.</span><span class="sxs-lookup"><span data-stu-id="6b779-147">Alpha-to-coverage is also traditionally used for screen-door transparency or defining detailed silhouettes for otherwise opaque sprites.</span></span>

### <a name="blending-pixel-shader-outputs"></a><span data-ttu-id="6b779-148">Выходные данные шейдера пикселей смешения</span><span class="sxs-lookup"><span data-stu-id="6b779-148">Blending Pixel Shader Outputs</span></span>

<span data-ttu-id="6b779-149">Эта функция позволяет слиянию выходных данных использовать одновременно выходные данные шейдера пикселей в качестве источников входных данных в операцию смешения с одним целевым объектом рендеринга в слоте 0.</span><span class="sxs-lookup"><span data-stu-id="6b779-149">This feature enables the output merger to use both the pixel shader outputs simultaneously as input sources to a blending operation with the single render target at slot 0.</span></span>

<span data-ttu-id="6b779-150">Этот пример принимает два результата и объединяет их в один проход, объединяя один в назначение с множителем, а другой — с помощью Add:</span><span class="sxs-lookup"><span data-stu-id="6b779-150">This example takes two results and combines them in a single pass, blending one into the destination with a multiply and the other with an add:</span></span>


```
SrcBlend = D3D11_BLEND_ONE;
DestBlend = D3D11_BLEND_SRC1_COLOR;
```



<span data-ttu-id="6b779-151">Этот пример настраивает первый выход шейдера пикселей в качестве исходного цвета и второй выход в качестве коэффициента смешения для каждого цвета.</span><span class="sxs-lookup"><span data-stu-id="6b779-151">This example configures the first pixel shader output as the source color and the second output as a per-color component blend factor.</span></span>


```
SrcBlend = D3D11_BLEND_SRC1_COLOR;
DestBlend = D3D11_BLEND_INV_SRC1_COLOR;
```



<span data-ttu-id="6b779-152">В этом примере показано, как коэффициенты смешения должны соответствовать свиззлес шейдера:</span><span class="sxs-lookup"><span data-stu-id="6b779-152">This example illustrates how the blend factors must match the shader swizzles:</span></span>


```
SrcFactor = D3D11_BLEND_SRC1_ALPHA;
DestFactor = D3D11_BLEND_SRC_COLOR;
OutputWriteMask[0] = .ra; // pseudocode for setting the mask at
                          // RenderTarget slot 0 to .ra
```



<span data-ttu-id="6b779-153">Вместе факторы смешения и код шейдера подразумевают, что шейдер пикселей требуется для вывода как минимум O0. r и O1. a.</span><span class="sxs-lookup"><span data-stu-id="6b779-153">Together, the blend factors and the shader code imply that the pixel shader is required to output at least o0.r and o1.a.</span></span> <span data-ttu-id="6b779-154">Дополнительные выходные компоненты могут выводиться шейдером, но они будут проигнорированы, но меньшее количество компонентов приведет к неопределенному результату.</span><span class="sxs-lookup"><span data-stu-id="6b779-154">Extra output components can be output by the shader but would be ignored, fewer components would produce undefined results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b779-155">См. также</span><span class="sxs-lookup"><span data-stu-id="6b779-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b779-156">Стадия средства слияния вывода</span><span class="sxs-lookup"><span data-stu-id="6b779-156">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="6b779-157">Этапы конвейера (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="6b779-157">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 