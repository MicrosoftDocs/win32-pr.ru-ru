---
title: Настройка функциональных возможностей Depth-Stencil
description: В этом разделе приводится пошаговая инструкция по настройке буфера трафарета глубины и рассматривается состояние трафарета глубины для стадии слияния вывода.
ms.assetid: e8f52d5f-266f-4e2c-b38d-d7fd9e27fe1f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65bf48b0ba9a782be25568ac3fc0569314dae76e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792708"
---
# <a name="configuring-depth-stencil-functionality"></a><span data-ttu-id="c9323-103">Настройка функциональных возможностей Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="c9323-103">Configuring Depth-Stencil Functionality</span></span>

<span data-ttu-id="c9323-104">В этом разделе приводится пошаговая инструкция по настройке буфера трафарета глубины и рассматривается состояние трафарета глубины для стадии слияния вывода.</span><span class="sxs-lookup"><span data-stu-id="c9323-104">This section covers the steps for setting up the depth-stencil buffer, and depth-stencil state for the output-merger stage.</span></span>

-   [<span data-ttu-id="c9323-105">Создание Depth-Stencil ресурса</span><span class="sxs-lookup"><span data-stu-id="c9323-105">Create a Depth-Stencil Resource</span></span>](#create-a-depth-stencil-resource)
-   [<span data-ttu-id="c9323-106">Создание состояния Depth-Stencil</span><span class="sxs-lookup"><span data-stu-id="c9323-106">Create Depth-Stencil State</span></span>](#create-depth-stencil-state)
-   [<span data-ttu-id="c9323-107">Привязка Depth-Stencil данных к этапу OM</span><span class="sxs-lookup"><span data-stu-id="c9323-107">Bind Depth-Stencil Data to the OM Stage</span></span>](#bind-depth-stencil-data-to-the-om-stage)

<span data-ttu-id="c9323-108">Узнав, как использовать буфер трафарета глубины и соответствующее состояние трафарета глубины, приступайте к изучению [сложных техник работы с трафаретами](#advanced-stencil-techniques).</span><span class="sxs-lookup"><span data-stu-id="c9323-108">Once you know how to use the depth-stencil buffer and the corresponding depth-stencil state, refer to [advanced-stencil techniques](#advanced-stencil-techniques).</span></span>

## <a name="create-a-depth-stencil-resource"></a><span data-ttu-id="c9323-109">Создание Depth-Stencil ресурса</span><span class="sxs-lookup"><span data-stu-id="c9323-109">Create a Depth-Stencil Resource</span></span>

<span data-ttu-id="c9323-110">Создайте буфер шаблона глубины с помощью ресурса текстуры.</span><span class="sxs-lookup"><span data-stu-id="c9323-110">Create the depth-stencil buffer using a texture resource.</span></span>


```
ID3D11Texture2D* pDepthStencil = NULL;
D3D11_TEXTURE2D_DESC descDepth;
descDepth.Width = backBufferSurfaceDesc.Width;
descDepth.Height = backBufferSurfaceDesc.Height;
descDepth.MipLevels = 1;
descDepth.ArraySize = 1;
descDepth.Format = pDeviceSettings->d3d11.AutoDepthStencilFormat;
descDepth.SampleDesc.Count = 1;
descDepth.SampleDesc.Quality = 0;
descDepth.Usage = D3D11_USAGE_DEFAULT;
descDepth.BindFlags = D3D11_BIND_DEPTH_STENCIL;
descDepth.CPUAccessFlags = 0;
descDepth.MiscFlags = 0;
hr = pd3dDevice->CreateTexture2D( &descDepth, NULL, &pDepthStencil );
```



## <a name="create-depth-stencil-state"></a><span data-ttu-id="c9323-111">Создание состояния трафарета глубины</span><span class="sxs-lookup"><span data-stu-id="c9323-111">Create Depth-Stencil State</span></span>

<span data-ttu-id="c9323-112">Состояние трафарета глубины сообщает стадии средства слияния вывода способ выполнения [проверки трафарета глубины](d3d10-graphics-programming-guide-output-merger-stage.md).</span><span class="sxs-lookup"><span data-stu-id="c9323-112">The depth-stencil state tells the output-merger stage how to perform the [depth-stencil test](d3d10-graphics-programming-guide-output-merger-stage.md).</span></span> <span data-ttu-id="c9323-113">Проверка трафарета глубины позволяет определить, нужно ли рисовать тот или иной пиксель.</span><span class="sxs-lookup"><span data-stu-id="c9323-113">The depth-stencil test determines whether or not a given pixel should be drawn.</span></span>


```
D3D11_DEPTH_STENCIL_DESC dsDesc;

// Depth test parameters
dsDesc.DepthEnable = true;
dsDesc.DepthWriteMask = D3D11_DEPTH_WRITE_MASK_ALL;
dsDesc.DepthFunc = D3D11_COMPARISON_LESS;

// Stencil test parameters
dsDesc.StencilEnable = true;
dsDesc.StencilReadMask = 0xFF;
dsDesc.StencilWriteMask = 0xFF;

// Stencil operations if pixel is front-facing
dsDesc.FrontFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilDepthFailOp = D3D11_STENCIL_OP_INCR;
dsDesc.FrontFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.FrontFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Stencil operations if pixel is back-facing
dsDesc.BackFace.StencilFailOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilDepthFailOp = D3D11_STENCIL_OP_DECR;
dsDesc.BackFace.StencilPassOp = D3D11_STENCIL_OP_KEEP;
dsDesc.BackFace.StencilFunc = D3D11_COMPARISON_ALWAYS;

// Create depth stencil state
ID3D11DepthStencilState * pDSState;
pd3dDevice->CreateDepthStencilState(&dsDesc, &pDSState);
```



<span data-ttu-id="c9323-114">Депсенабле и СтенЦиленабле включают (и отключают) глубину и тестирование трафаретов.</span><span class="sxs-lookup"><span data-stu-id="c9323-114">DepthEnable and StencilEnable enable (and disable) depth and stencil testing.</span></span> <span data-ttu-id="c9323-115">Задайте для Депсенабле **значение false** , чтобы отключить тестирование глубины и запретить запись в буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="c9323-115">Set DepthEnable to **FALSE** to disable depth testing and prevent writing to the depth buffer.</span></span> <span data-ttu-id="c9323-116">Задайте для СтенЦиленабле **значение false** , чтобы отключить тестирование наборов элементов и предотвратить запись в буфер шаблона (если Депсенабле имеет **значение false** , а стенЦиленабле имеет **значение true**, тест глубины всегда передается в операцию с набором элементов).</span><span class="sxs-lookup"><span data-stu-id="c9323-116">Set StencilEnable to **FALSE** to disable stencil testing and prevent writing to the stencil buffer (when DepthEnable is **FALSE** and StencilEnable is **TRUE**, the depth test always passes in the stencil operation).</span></span>

<span data-ttu-id="c9323-117">Депсенабле влияет только на этап слияния (Output-слияние). он не влияет на обрезание, сдвиг глубины или фиксацию значений перед вводом данных в шейдер пикселей.</span><span class="sxs-lookup"><span data-stu-id="c9323-117">DepthEnable only affects the output-merger stage - it does not affect clipping, depth bias, or clamping of values before the data is input to a pixel shader.</span></span>

## <a name="bind-depth-stencil-data-to-the-om-stage"></a><span data-ttu-id="c9323-118">Привязка данных трафарета глубины к стадии средства слияния вывода</span><span class="sxs-lookup"><span data-stu-id="c9323-118">Bind Depth-Stencil Data to the OM Stage</span></span>

<span data-ttu-id="c9323-119">Привязка состояния трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="c9323-119">Bind the depth-stencil state.</span></span>


```
// Bind depth stencil state
pDevice->OMSetDepthStencilState(pDSState, 1);
```



<span data-ttu-id="c9323-120">Привязка ресурса трафарета глубины с использованием представления.</span><span class="sxs-lookup"><span data-stu-id="c9323-120">Bind the depth-stencil resource using a view.</span></span>


```
D3D11_DEPTH_STENCIL_VIEW_DESC descDSV;
descDSV.Format = DXGI_FORMAT_D32_FLOAT_S8X24_UINT;
descDSV.ViewDimension = D3D11_DSV_DIMENSION_TEXTURE2D;
descDSV.Texture2D.MipSlice = 0;

// Create the depth stencil view
ID3D11DepthStencilView* pDSV;
hr = pd3dDevice->CreateDepthStencilView( pDepthStencil, // Depth stencil texture
                                         &descDSV, // Depth stencil desc
                                         &pDSV );  // [out] Depth stencil view

// Bind the depth stencil view
pd3dDeviceContext->OMSetRenderTargets( 1,          // One rendertarget view
                                &pRTV,      // Render target view, created earlier
                                pDSV );     // Depth stencil view for the render target
```



<span data-ttu-id="c9323-121">В [**ссылку ID3D11DeviceContext:: омсетрендертаржетс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets)можно передать массив представлений целевого объекта визуализации, однако все эти представления целевого объекта будут соответствовать одному представлению трафарета глубины.</span><span class="sxs-lookup"><span data-stu-id="c9323-121">An array of render-target views may be passed into [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets), however all of those render-target views will correspond to a single depth stencil view.</span></span> <span data-ttu-id="c9323-122">Массив целевых объектов отрисовки в Direct3D 11 — это функция, которая позволяет приложению отображать несколько целевых объектов отрисовки одновременно на уровне примитивов.</span><span class="sxs-lookup"><span data-stu-id="c9323-122">The render target array in Direct3D 11 is a feature that enables an application to render onto multiple render targets simultaneously at the primitive level.</span></span> <span data-ttu-id="c9323-123">Целевые массивы визуализации обеспечивают повышенную производительность по сравнению с индивидуальной установкой целевых объектов отрисовки с несколькими вызовами метода **ссылку ID3D11DeviceContext:: омсетрендертаржетс** (по сути, метод, используемый в Direct3D 9).</span><span class="sxs-lookup"><span data-stu-id="c9323-123">Render target arrays offer increased performance over individually setting render targets with multiple calls to **ID3D11DeviceContext::OMSetRenderTargets** (essentially the method employed in Direct3D 9).</span></span>

<span data-ttu-id="c9323-124">Все однобуферные прорисовки должны относиться к одному типу ресурса.</span><span class="sxs-lookup"><span data-stu-id="c9323-124">Render targets must all be the same type of resource.</span></span> <span data-ttu-id="c9323-125">Если используется сглаживание с множественной дискретизацией, все связанные однобуферные прорисовки и буферы глубины должны иметь одинаковое число выборок.</span><span class="sxs-lookup"><span data-stu-id="c9323-125">If multisample antialiasing is used, all bound render targets and depth buffers must have the same sample counts.</span></span>

<span data-ttu-id="c9323-126">Если буфер используется в качестве однобуферной прорисовки, проверка трафарета глубины и использование нескольких однобуферных прорисовок не поддерживаются.</span><span class="sxs-lookup"><span data-stu-id="c9323-126">When a buffer is used as a render target, depth-stencil testing and multiple render targets are not supported.</span></span>

-   <span data-ttu-id="c9323-127">Одновременно можно связать до 8 однобуферных прорисовок.</span><span class="sxs-lookup"><span data-stu-id="c9323-127">As many as 8 render targets can be bound simultaneously.</span></span>
-   <span data-ttu-id="c9323-128">Все целевые объекты отрисовки должны иметь одинаковый размер во всех измерениях (ширина и высота, а также глубину для объемных массивов или массивов для \* типов массива).</span><span class="sxs-lookup"><span data-stu-id="c9323-128">All render targets must have the same size in all dimensions (width and height, and depth for 3D or array size for \*Array types).</span></span>
-   <span data-ttu-id="c9323-129">Каждая однобуферная прорисовка может иметь свой формат данных.</span><span class="sxs-lookup"><span data-stu-id="c9323-129">Each render target may have a different data format.</span></span>
-   <span data-ttu-id="c9323-130">Маски записи контролируют, какие данные записываются в однобуферную прорисовку.</span><span class="sxs-lookup"><span data-stu-id="c9323-130">Write masks control what data gets written to a render target.</span></span> <span data-ttu-id="c9323-131">Маски записи вывода контролируют, какие данные записываются в однобуферные прорисовки на уровне однобуферных прорисовок и компонентов.</span><span class="sxs-lookup"><span data-stu-id="c9323-131">The output write masks control on a per-render target, per-component level what data gets written to the render target(s).</span></span>

## <a name="advanced-stencil-techniques"></a><span data-ttu-id="c9323-132">Сложные техники работы с трафаретами</span><span class="sxs-lookup"><span data-stu-id="c9323-132">Advanced Stencil Techniques</span></span>

<span data-ttu-id="c9323-133">Трафаретная часть буфера трафарета глубины может использоваться для создания эффектов отрисовки, таких как компоновка, переводные картинки и структурирование.</span><span class="sxs-lookup"><span data-stu-id="c9323-133">The stencil portion of the depth-stencil buffer can be used for creating rendering effects such as compositing, decaling, and outlining.</span></span>

-   [<span data-ttu-id="c9323-134">Компоновка</span><span class="sxs-lookup"><span data-stu-id="c9323-134">Compositing</span></span>](#compositing)
-   [<span data-ttu-id="c9323-135">Переводные картинки</span><span class="sxs-lookup"><span data-stu-id="c9323-135">Decaling</span></span>](#decaling)
-   [<span data-ttu-id="c9323-136">Контуры и Силхауеттес</span><span class="sxs-lookup"><span data-stu-id="c9323-136">Outlines and Silhouettes</span></span>](#outlines-and-silhouettes)
-   [<span data-ttu-id="c9323-137">Двухсторонний набор элементов</span><span class="sxs-lookup"><span data-stu-id="c9323-137">Two-Sided Stencil</span></span>](#two-sided-stencil)
-   [<span data-ttu-id="c9323-138">Считывание Depth-Stencil буфера в виде текстуры</span><span class="sxs-lookup"><span data-stu-id="c9323-138">Reading the Depth-Stencil Buffer as a Texture</span></span>](#reading-the-depth-stencil-buffer-as-a-texture)

### <a name="compositing"></a><span data-ttu-id="c9323-139">Компоновка</span><span class="sxs-lookup"><span data-stu-id="c9323-139">Compositing</span></span>

<span data-ttu-id="c9323-140">Ваше приложение может использовать буфер трафарета для создания двух- или трехмерных изображений в трехмерной сцене.</span><span class="sxs-lookup"><span data-stu-id="c9323-140">Your application can use the stencil buffer to composite 2D or 3D images onto a 3D scene.</span></span> <span data-ttu-id="c9323-141">Маска в буфере трафарета используется для ограждения области, которая является поверхностью однобуферной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="c9323-141">A mask in the stencil buffer is used to occlude an area of the rendering target surface.</span></span> <span data-ttu-id="c9323-142">Сохраненную двухмерную информацию, такую как текст или точечные рисунки, затем можно записать в огороженную область.</span><span class="sxs-lookup"><span data-stu-id="c9323-142">Stored 2D information, such as text or bitmaps, can then be written to the occluded area.</span></span> <span data-ttu-id="c9323-143">Кроме того, ваше приложение может отрисовывать дополнительные трехмерные примитивы в замаскированный трафаретом регион поверхности однобуферной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="c9323-143">Alternately, your application can render additional 3D primitives to the stencil-masked region of the rendering target surface.</span></span> <span data-ttu-id="c9323-144">Приложение даже может отрисовывать всю сцену.</span><span class="sxs-lookup"><span data-stu-id="c9323-144">It can even render an entire scene.</span></span>

<span data-ttu-id="c9323-145">Игры часто предполагают компоновку нескольких трехмерных сцен.</span><span class="sxs-lookup"><span data-stu-id="c9323-145">Games often composite multiple 3D scenes together.</span></span> <span data-ttu-id="c9323-146">Так, в симуляторах вождения, как правило, показано отражение в зеркале заднего вида.</span><span class="sxs-lookup"><span data-stu-id="c9323-146">For instance, driving games typically display a rear-view mirror.</span></span> <span data-ttu-id="c9323-147">В нем отражается происходящее за водителем в трехмерном формате.</span><span class="sxs-lookup"><span data-stu-id="c9323-147">The mirror contains the view of the 3D scene behind the driver.</span></span> <span data-ttu-id="c9323-148">Это вторая трехмерная сцена, скомпонованная с передним обзором водителя.</span><span class="sxs-lookup"><span data-stu-id="c9323-148">It is essentially a second 3D scene composited with the driver's forward view.</span></span>

### <a name="decaling"></a><span data-ttu-id="c9323-149">Переводные картинки</span><span class="sxs-lookup"><span data-stu-id="c9323-149">Decaling</span></span>

<span data-ttu-id="c9323-150">В приложениях Direct3D пользователи с помощью переводных картинок контролируют, какие пиксели из определенного изображения-примитива рисуются на поверхность однобуферной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="c9323-150">Direct3D applications use decaling to control which pixels from a particular primitive image are drawn to the rendering target surface.</span></span> <span data-ttu-id="c9323-151">Приложения применяют переводные картинки к изображениям примитивов для правильной отрисовки многоугольников.</span><span class="sxs-lookup"><span data-stu-id="c9323-151">Applications apply decals to the images of primitives to enable coplanar polygons to render correctly.</span></span>

<span data-ttu-id="c9323-152">Например, следы шин и желтая дорожная разметка должны отображаться непосредственно на поверхности дороги.</span><span class="sxs-lookup"><span data-stu-id="c9323-152">For instance, when applying tire marks and yellow lines to a roadway, the markings should appear directly on top of the road.</span></span> <span data-ttu-id="c9323-153">Однако значения разметки и дорожной поверхности по оси Z совпадают.</span><span class="sxs-lookup"><span data-stu-id="c9323-153">However, the z values of the markings and the road are the same.</span></span> <span data-ttu-id="c9323-154">Поэтому велика вероятность нечеткого разделения этих сущностей буфером глубины.</span><span class="sxs-lookup"><span data-stu-id="c9323-154">Therefore, the depth buffer might not produce a clean separation between the two.</span></span> <span data-ttu-id="c9323-155">Некоторые пиксели в примитиве заднего вида могут отображаться поверх пикселей в примитиве переднего вида, и наоборот.</span><span class="sxs-lookup"><span data-stu-id="c9323-155">Some pixels in the back primitive may be rendered on top of the front primitive and vice versa.</span></span> <span data-ttu-id="c9323-156">В результате изображение может дрожать при смене кадра.</span><span class="sxs-lookup"><span data-stu-id="c9323-156">The resulting image appears to shimmer from frame to frame.</span></span> <span data-ttu-id="c9323-157">Этот эффект называется Z-буферизация или "мерцание".</span><span class="sxs-lookup"><span data-stu-id="c9323-157">This effect is called z-fighting or flimmering.</span></span>

<span data-ttu-id="c9323-158">Чтобы решить эту проблему, используйте трафарет для маскировки раздела примитива заднего вида, в котором будет отображаться переводная картинка.</span><span class="sxs-lookup"><span data-stu-id="c9323-158">To solve this problem, use a stencil to mask the section of the back primitive where the decal will appear.</span></span> <span data-ttu-id="c9323-159">Выключите Z-буферизацию и отрисуйте изображение примитива переднего обзора в замаскированной области поверхности однобуферной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="c9323-159">Turn off z-buffering and render the image of the front primitive into the masked-off area of the render-target surface.</span></span>

<span data-ttu-id="c9323-160">Для решения этой проблемы можно использовать наложение нескольких текстур.</span><span class="sxs-lookup"><span data-stu-id="c9323-160">Multiple texture blending can be used to solve this problem.</span></span>

### <a name="outlines-and-silhouettes"></a><span data-ttu-id="c9323-161">Структуры и силуэты</span><span class="sxs-lookup"><span data-stu-id="c9323-161">Outlines and Silhouettes</span></span>

<span data-ttu-id="c9323-162">Буфер трафарета можно использовать и для более абстрактных эффектов, таких как создание структур и силуэтов.</span><span class="sxs-lookup"><span data-stu-id="c9323-162">You can use the stencil buffer for more abstract effects, such as outlining and silhouetting.</span></span>

<span data-ttu-id="c9323-163">Если ваше приложение выполняет два прохода отрисовки (один — чтобы создать маску трафарета, а второй — чтобы применить маску трафарета к изображению, однако во втором проходе используются несколько более мелкие примитивы), получившееся изображение будет содержать только структуру примитива.</span><span class="sxs-lookup"><span data-stu-id="c9323-163">If your application does two render passes - one to generate the stencil mask and second to apply the stencil mask to the image, but with the primitives slightly smaller on the second pass - the resulting image will contain only the primitive's outline.</span></span> <span data-ttu-id="c9323-164">Затем приложение может заполнить замаскированную трафаретом область изображения сплошным цветом, создавая для примитива эффект приподнятости.</span><span class="sxs-lookup"><span data-stu-id="c9323-164">The application can then fill the stencil-masked area of the image with a solid color, giving the primitive an embossed look.</span></span>

<span data-ttu-id="c9323-165">Если маска трафарета имеет те же размеры и форму, что и примитив, который вы отрисовываете, на полученном изображении на месте примитива будет отверстие.</span><span class="sxs-lookup"><span data-stu-id="c9323-165">If the stencil mask is the same size and shape as the primitive you are rendering, the resulting image contains a hole where the primitive should be.</span></span> <span data-ttu-id="c9323-166">Затем приложение может заполнить это отверстие черным, создавая силуэт примитива.</span><span class="sxs-lookup"><span data-stu-id="c9323-166">Your application can then fill the hole with black to produce a silhouette of the primitive.</span></span>

### <a name="two-sided-stencil"></a><span data-ttu-id="c9323-167">Двусторонний трафарет</span><span class="sxs-lookup"><span data-stu-id="c9323-167">Two-Sided Stencil</span></span>

<span data-ttu-id="c9323-168">Теневые тома используются для рисования теней с использованием буфера трафарета.</span><span class="sxs-lookup"><span data-stu-id="c9323-168">Shadow Volumes are used for drawing shadows with the stencil buffer.</span></span> <span data-ttu-id="c9323-169">Приложение вычисляет теневые тома, переданные геометрией ограждения, вычисляя края силуэта и вытягивая их от света в набор трехмерных томов.</span><span class="sxs-lookup"><span data-stu-id="c9323-169">The application computes the shadow volumes cast by occluding geometry, by computing the silhouette edges and extruding them away from the light into a set of 3D volumes.</span></span> <span data-ttu-id="c9323-170">Затем эти тома дважды отрисовываются в буфер трафарета.</span><span class="sxs-lookup"><span data-stu-id="c9323-170">These volumes are then rendered twice into the stencil buffer.</span></span>

<span data-ttu-id="c9323-171">В ходе первой отрисовки рисуются многоугольники переднего обзора и увеличиваются значения буфера трафарета.</span><span class="sxs-lookup"><span data-stu-id="c9323-171">The first render draws forward-facing polygons, and increments the stencil-buffer values.</span></span> <span data-ttu-id="c9323-172">В ходе второй отрисовки рисуются многоугольники заднего вида, относящиеся к теневому тому, а значения буфера трафарета уменьшаются.</span><span class="sxs-lookup"><span data-stu-id="c9323-172">The second render draws the back-facing polygons of the shadow volume, and decrements the stencil buffer values.</span></span> <span data-ttu-id="c9323-173">Как правило, значения увеличения и уменьшения уравновешивают друг друга. Однако сцена уже была отрисована с нормальной геометрией, из-за чего некоторые пиксели не прошли проверку Z-буфера при отрисовке теневого тома.</span><span class="sxs-lookup"><span data-stu-id="c9323-173">Normally, all incremented and decremented values cancel each other out. However, the scene was already rendered with normal geometry causing some pixels to fail the z-buffer test as the shadow volume is rendered.</span></span> <span data-ttu-id="c9323-174">Значения, оставшиеся в буфере трафарета, соответствуют пикселям в тени.</span><span class="sxs-lookup"><span data-stu-id="c9323-174">Values left in the stencil buffer correspond to pixels that are in the shadow.</span></span> <span data-ttu-id="c9323-175">Оставшееся содержимое буфера трафарета используется в качестве маски, чтобы выполнить альфа-смешение крупного, всеобъемлющего черного квартета со сценой.</span><span class="sxs-lookup"><span data-stu-id="c9323-175">These remaining stencil-buffer contents are used as a mask, to alpha-blend a large, all-encompassing black quad into the scene.</span></span> <span data-ttu-id="c9323-176">Если буфер трафарета используется в качестве маски, в результате затеняются пиксели, которые находятся в тени.</span><span class="sxs-lookup"><span data-stu-id="c9323-176">With the stencil buffer acting as a mask, the result is to darken pixels that are in the shadows.</span></span>

<span data-ttu-id="c9323-177">Это означает, что теневая геометрия рисуется дважды для каждого источника света, оказывая давление на пропускную способность вершин графического процессора.</span><span class="sxs-lookup"><span data-stu-id="c9323-177">This means that the shadow geometry is drawn twice per light source, hence putting pressure on the vertex throughput of the GPU.</span></span> <span data-ttu-id="c9323-178">Для устранения этого эффекта разработана функция двустороннего трафарета.</span><span class="sxs-lookup"><span data-stu-id="c9323-178">The two-sided stencil feature has been designed to mitigate this situation.</span></span> <span data-ttu-id="c9323-179">При таком подходе существует два набора состояний трафарета (они указаны ниже): один — для треугольников переднего обзора, другой — для треугольников заднего вида.</span><span class="sxs-lookup"><span data-stu-id="c9323-179">In this approach, there are two sets of stencil state (named below), one set each for the front-facing triangles and the other for the back-facing triangles.</span></span> <span data-ttu-id="c9323-180">В этом случае для каждого теневого тома рисуется по одному проходу на источник освещения.</span><span class="sxs-lookup"><span data-stu-id="c9323-180">This way, only a single pass is drawn per shadow volume, per light.</span></span>

<span data-ttu-id="c9323-181">Пример двусторонней реализации трафарета можно найти в [примере ShadowVolume10](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="c9323-181">An example of two-sided stencil implementation can be found in the [ShadowVolume10 Sample](https://msdn.microsoft.com/library/Ee416427(v=VS.85).aspx).</span></span>

### <a name="reading-the-depth-stencil-buffer-as-a-texture"></a><span data-ttu-id="c9323-182">Считывание буфера трафарета глубины как текстуры</span><span class="sxs-lookup"><span data-stu-id="c9323-182">Reading the Depth-Stencil Buffer as a Texture</span></span>

<span data-ttu-id="c9323-183">Неактивный буфер трафарета глубины может считываться шейдером как текстура.</span><span class="sxs-lookup"><span data-stu-id="c9323-183">An inactive depth-stencil buffer can be read by a shader as a texture.</span></span> <span data-ttu-id="c9323-184">Приложение, считывающее буфер трафарета глубины как текстуру, отрисовывается за два прохода: первый проход выполняет запись в буфер трафарета глубины, а второй — чтение из этого буфера.</span><span class="sxs-lookup"><span data-stu-id="c9323-184">An application that reads a depth-stencil buffer as a texture renders in two passes, the first pass writes to the depth-stencil buffer and the second pass reads from the buffer.</span></span> <span data-ttu-id="c9323-185">Это позволяет шейдеру сравнить значения глубины или трафарета, ранее записанные в буфер, со значением для отрисовываемого в настоящее время пикселя.</span><span class="sxs-lookup"><span data-stu-id="c9323-185">This allows a shader to compare depth or stencil values previously written to the buffer against the value for the pixel currrently being rendered.</span></span> <span data-ttu-id="c9323-186">Результат сравнения может использоваться для создания эффектов, таких как сопоставление теней или мягкие частицы в системе частиц.</span><span class="sxs-lookup"><span data-stu-id="c9323-186">The result of the comparison can be used to create effects such as shadow mapping or soft particles in a particle system.</span></span>

<span data-ttu-id="c9323-187">Чтобы создать буфер шаблона глубины, который можно использовать в качестве ресурса-шаблона глубины и ресурса шейдера, необходимо внести несколько изменений в пример кода в разделе [создание Depth-Stencil ресурса](#create-a-depth-stencil-resource) .</span><span class="sxs-lookup"><span data-stu-id="c9323-187">To create a depth-stencil buffer that can be used as both a depth-stencil resource and a shader resource a few changes need to be made to sample code in the [Create a Depth-Stencil Resource](#create-a-depth-stencil-resource) section.</span></span>

-   <span data-ttu-id="c9323-188">Ресурс шаблона глубины должен иметь нетипизированный формат, такой как формат DXGI \_ \_ R32 \_ Type.</span><span class="sxs-lookup"><span data-stu-id="c9323-188">The depth-stencil resource must have a typeless format such as DXGI\_FORMAT\_R32\_TYPELESS.</span></span>
    ```
    descDepth.Format = DXGI_FORMAT_R32_TYPELESS;
    ```

    

-   <span data-ttu-id="c9323-189">Ресурс шаблона глубины должен использовать \_ Флаги D3D10 привязки и привязки \_ \_ \_ \_ ресурса шейдера D3D10 BIND \_ .</span><span class="sxs-lookup"><span data-stu-id="c9323-189">The depth-stencil resource must use both the D3D10\_BIND\_DEPTH\_STENCIL and D3D10\_BIND\_SHADER\_RESOURCE bind flags.</span></span>
    ```
    descDepth.BindFlags = D3D10_BIND_DEPTH_STENCIL | D3D10_BIND_SHADER_RESOURCE;
    ```

    

<span data-ttu-id="c9323-190">Кроме того, необходимо создать представление ресурсов шейдера для буфера глубины с помощью структуры D3D11 в [**\_ \_ \_ представлении \_ ресурсов шейдера**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) , а также [**ID3D11Device:: креатешадерресаурцевиев**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview).</span><span class="sxs-lookup"><span data-stu-id="c9323-190">In addition a shader resource view needs to be created for the depth buffer using a [**D3D11\_SHADER\_RESOURCE\_VIEW\_DESC**](/windows/desktop/api/d3d11/ns-d3d11-d3d11_shader_resource_view_desc) structure and [**ID3D11Device::CreateShaderResourceView**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createshaderresourceview).</span></span> <span data-ttu-id="c9323-191">Представление ресурсов шейдера будет использовать типизированный формат, такой как **\_ \_ R32 \_ float** , который эквивалентен формату, указанному при создании ресурса-шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="c9323-191">The shader resource view will use a typed format such as **DXGI\_FORMAT\_R32\_FLOAT** that is the equivalent to the typeless format specified when the depth-stencil resource was created.</span></span>

<span data-ttu-id="c9323-192">На первом этапе отрисовки буфер глубины привязывается, как описано в разделе [привязка Depth-Stencil данных к этапу OM](#bind-depth-stencil-data-to-the-om-stage) .</span><span class="sxs-lookup"><span data-stu-id="c9323-192">In the first render pass the depth buffer is bound as described in the [Bind Depth-Stencil Data to the OM Stage](#bind-depth-stencil-data-to-the-om-stage) section.</span></span> <span data-ttu-id="c9323-193">Обратите внимание, что формат, передаваемый в [**D3D11 \_ \_ представление трафарета глубины \_ \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc), — DESC. Формат будет использовать типизированный формат, такой **как \_ \_ d32 \_ float**, например, в формате DXGI.</span><span class="sxs-lookup"><span data-stu-id="c9323-193">Note that the format passed to [**D3D11\_DEPTH\_STENCIL\_VIEW\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_view_desc).Format will use a typed format such as **DXGI\_FORMAT\_D32\_FLOAT**.</span></span> <span data-ttu-id="c9323-194">После первого прохода буфер глубины будет содержать значения глубины для сцены.</span><span class="sxs-lookup"><span data-stu-id="c9323-194">After the first render pass the depth buffer will contain the depth values for the scene.</span></span>

<span data-ttu-id="c9323-195">Во второй функции рендеринга функция [**ссылку ID3D11DeviceContext:: омсетрендертаржетс**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) используется, чтобы задать для представления трафарета глубины **значение NULL** или другой ресурс трафарета глубины, а представление ресурсов шейдера передается шейдеру с помощью [**ID3D11EffectShaderResourceVariable:: сетресаурце**](id3dx11effectshaderresourcevariable-setresource.md).</span><span class="sxs-lookup"><span data-stu-id="c9323-195">In the second render pass the [**ID3D11DeviceContext::OMSetRenderTargets**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-omsetrendertargets) function is used to set the depth-stencil view to **NULL** or a different depth-stencil resource and the shader resource view is passed to the shader using [**ID3D11EffectShaderResourceVariable::SetResource**](id3dx11effectshaderresourcevariable-setresource.md).</span></span> <span data-ttu-id="c9323-196">Это позволяет шейдеру искать значения глубины, вычисленные на первом этапе подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="c9323-196">This allows the shader to look up the depth values calculated in the first rendering pass.</span></span> <span data-ttu-id="c9323-197">Обратите внимание, что преобразование необходимо применить для получения значений глубины, если точка представления первого прохода прорисовки отличается от второго прохода отрисовки.</span><span class="sxs-lookup"><span data-stu-id="c9323-197">Note that a transformation will need to be applied to retrieve depth values if the point of view of the first render pass is different from the second render pass.</span></span> <span data-ttu-id="c9323-198">Например, если используется метод сопоставления теневого отображения, первый проход рендеринга будет с точки зрения источника освещения, а второй — с точки зрения средства просмотра.</span><span class="sxs-lookup"><span data-stu-id="c9323-198">For example, if a shadow mapping technique is being used the first render pass will be from the perspective of a light source while the second render pass will from the viewer's perspective.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c9323-199">См. также</span><span class="sxs-lookup"><span data-stu-id="c9323-199">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c9323-200">Стадия средства слияния вывода</span><span class="sxs-lookup"><span data-stu-id="c9323-200">Output-Merger Stage</span></span>](d3d10-graphics-programming-guide-output-merger-stage.md)
</dt> <dt>

[<span data-ttu-id="c9323-201">Этапы конвейера (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="c9323-201">Pipeline Stages (Direct3D 10)</span></span>](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages)
</dt> </dl>

 

 