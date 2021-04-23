---
description: Приложения используют буфер трафарета для маскирования пикселов в изображении. Маска определяет рисуется пиксель или нет. Некоторые из наиболее распространенных эффектов показаны ниже.
ms.assetid: 984f0a98-4a74-44c3-a9d0-f5d3f12f7e4e
title: Методы буфера элементов шаблона (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c2dcc05475a3ddfc13e456faf60ec2d11e271a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423150"
---
# <a name="stencil-buffer-techniques-direct3d-9"></a><span data-ttu-id="e133e-105">Методы буфера элементов шаблона (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="e133e-105">Stencil Buffer Techniques (Direct3D 9)</span></span>

<span data-ttu-id="e133e-106">Приложения используют буфер трафарета для маскирования пикселов в изображении.</span><span class="sxs-lookup"><span data-stu-id="e133e-106">Applications use the stencil buffer to mask pixels in an image.</span></span> <span data-ttu-id="e133e-107">Маска определяет рисуется пиксель или нет.</span><span class="sxs-lookup"><span data-stu-id="e133e-107">The mask controls whether the pixel is drawn or not.</span></span> <span data-ttu-id="e133e-108">Некоторые из наиболее распространенных эффектов показаны ниже.</span><span class="sxs-lookup"><span data-stu-id="e133e-108">Some of the more common effects are shown below.</span></span>

-   [<span data-ttu-id="e133e-109">Компоновка</span><span class="sxs-lookup"><span data-stu-id="e133e-109">Compositing</span></span>](compositing.md)
-   [<span data-ttu-id="e133e-110">Переводные картинки</span><span class="sxs-lookup"><span data-stu-id="e133e-110">Decaling</span></span>](decaling.md)
-   [<span data-ttu-id="e133e-111">Разрешается, исчезает и прокрутка</span><span class="sxs-lookup"><span data-stu-id="e133e-111">Dissolves, Fades, and Swipes</span></span>](dissolves--fades--and-swipes.md)
-   [<span data-ttu-id="e133e-112">Контуры и Силхауеттес</span><span class="sxs-lookup"><span data-stu-id="e133e-112">Outlines and Silhouettes</span></span>](outlines-and-silhouettes.md)
-   [<span data-ttu-id="e133e-113">Двухсторонний набор элементов</span><span class="sxs-lookup"><span data-stu-id="e133e-113">Two-Sided Stencil</span></span>](two-sided-stencil.md)

<span data-ttu-id="e133e-114">Буфер трафарета включает или отключает отрисовку на целевую поверхность попиксельно.</span><span class="sxs-lookup"><span data-stu-id="e133e-114">The stencil buffer enables or disables drawing to the rendering target surface on a pixel-by-pixel basis.</span></span> <span data-ttu-id="e133e-115">На своем фундаментальном уровне буфер позволяет приложениям маскировать части выводимого изображения так, чтобы они не отображались.</span><span class="sxs-lookup"><span data-stu-id="e133e-115">At its most fundamental level, it enables applications to mask sections of the rendered image so that they are not displayed.</span></span> <span data-ttu-id="e133e-116">Приложения часто используют буферы трафарета для специальных эффектов, таких как рассеивание, наложение декалей и контуров.</span><span class="sxs-lookup"><span data-stu-id="e133e-116">Applications often use stencil buffers for special effects such as dissolves, decaling, and outlining.</span></span>

<span data-ttu-id="e133e-117">Данные буфера трафарета внедряются в данные z-буфера.</span><span class="sxs-lookup"><span data-stu-id="e133e-117">Stencil buffer information is embedded in the z-buffer data.</span></span> <span data-ttu-id="e133e-118">Приложение может использовать метод [**IDirect3D9:: чеккдевицеформат**](/windows/desktop/api) для проверки поддержки наборов элементов оборудования, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="e133e-118">Your application can use the [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) method to check for hardware stencil support, as shown in the following code example.</span></span>


```
// Reject devices that cannot perform 8-bit stencil buffering. 
// The following example assumes that pCaps is a valid pointer 
// to an initialized D3DCAPS9 structure. 

if( FAILED( m_pD3D->CheckDeviceFormat( pCaps->AdapterOrdinal,
                                       pCaps->DeviceType,  
                                       Format,  
                                       D3DUSAGE_DEPTHSTENCIL, 
                                       D3DRTYPE_SURFACE,
                                       D3DFMT_D24S8 ) ) )
return E_FAIL;
```



<span data-ttu-id="e133e-119">[**IDirect3D9:: чеккдевицеформат**](/windows/desktop/api) позволяет выбрать устройство для создания на основе возможностей этого устройства.</span><span class="sxs-lookup"><span data-stu-id="e133e-119">[**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) allows you to choose a device to create based on the capabilities of that device.</span></span> <span data-ttu-id="e133e-120">В этом случае устройства, которые не поддерживают 8-разрядные буферы трафаретов, отклоняются.</span><span class="sxs-lookup"><span data-stu-id="e133e-120">In this case, devices that do not support 8-bit stencil buffers are rejected.</span></span> <span data-ttu-id="e133e-121">Обратите внимание, что это только одно возможное использование для **IDirect3D9:: чеккдевицеформат**; Дополнительные сведения см. в разделе [Определение поддержки оборудования (Direct3D 9)](determining-hardware-support.md).</span><span class="sxs-lookup"><span data-stu-id="e133e-121">Note that this is only one possible use for **IDirect3D9::CheckDeviceFormat**; for details see [Determining Hardware Support (Direct3D 9)](determining-hardware-support.md).</span></span>

## <a name="how-the-stencil-buffer-works"></a><span data-ttu-id="e133e-122">Как работает буфер шаблона</span><span class="sxs-lookup"><span data-stu-id="e133e-122">How the Stencil Buffer Works</span></span>

<span data-ttu-id="e133e-123">Direct3D выполняет попиксельный тест содержимого буфера трафарета.</span><span class="sxs-lookup"><span data-stu-id="e133e-123">Direct3D performs a test on the contents of the stencil buffer on a pixel-by-pixel basis.</span></span> <span data-ttu-id="e133e-124">Для каждого пикселя на целевой поверхности выполняется тест с использованием соответствующего значения из буфера трафарета, контрольного значения буфера и значения маски буфера.</span><span class="sxs-lookup"><span data-stu-id="e133e-124">For each pixel in the target surface, it performs a test using the corresponding value in the stencil buffer, a stencil reference value, and a stencil mask value.</span></span> <span data-ttu-id="e133e-125">В тестовых проходах Direct3D выполняет действие.</span><span class="sxs-lookup"><span data-stu-id="e133e-125">If the test passes, Direct3D performs an action.</span></span> <span data-ttu-id="e133e-126">Тест проводится в несколько шагов.</span><span class="sxs-lookup"><span data-stu-id="e133e-126">The test is performed using the following steps.</span></span>

1.  <span data-ttu-id="e133e-127">Выполняется побитовая операция AND над контрольным значением трафарета и маской трафарета.</span><span class="sxs-lookup"><span data-stu-id="e133e-127">Perform a bitwise AND operation of the stencil reference value with the stencil mask.</span></span>
2.  <span data-ttu-id="e133e-128">Выполняется побитовая операция AND со значением буфера трафарета для текущего пикселя и маской трафарета.</span><span class="sxs-lookup"><span data-stu-id="e133e-128">Perform a bitwise AND operation of the stencil buffer value for the current pixel with the stencil mask.</span></span>
3.  <span data-ttu-id="e133e-129">Сравнивается результат 1-го шага с результатом 2-го шага 2 с помощью функции сравнения.</span><span class="sxs-lookup"><span data-stu-id="e133e-129">Compare the result of step 1 to the result of step 2, using the comparison function.</span></span>

<span data-ttu-id="e133e-130">Эти шаги показаны в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="e133e-130">These steps are shown in the following code example.</span></span>


```
(StencilRef & StencilMask) CompFunc (StencilBufferValue & StencilMask)
```




```
StencilBufferValue
```



<span data-ttu-id="e133e-131">содержимое буфера шаблона для текущего пикселя.</span><span class="sxs-lookup"><span data-stu-id="e133e-131">is the contents of the stencil buffer for the current pixel.</span></span> <span data-ttu-id="e133e-132">В этом примере кода используется символ амперсанда (&) для представления побитовой операции и.</span><span class="sxs-lookup"><span data-stu-id="e133e-132">This code example uses the ampersand (&) symbol to represent the bitwise AND operation.</span></span>


```
StencilMask
```



<span data-ttu-id="e133e-133">представляет значение маски набора элементов, а</span><span class="sxs-lookup"><span data-stu-id="e133e-133">represents the value of the stencil mask, and</span></span>


```
StencilRef
```



<span data-ttu-id="e133e-134">представляет значение ссылки на набор элементов.</span><span class="sxs-lookup"><span data-stu-id="e133e-134">represents the stencil reference value.</span></span>


```
CompFunc
```



<span data-ttu-id="e133e-135">Функция сравнения.</span><span class="sxs-lookup"><span data-stu-id="e133e-135">is the comparison function.</span></span>

<span data-ttu-id="e133e-136">Текущий пиксель записывается на целевую поверхность, если тест трафаретом пройден, в ином случае пиксель пропускается.</span><span class="sxs-lookup"><span data-stu-id="e133e-136">The current pixel is written to the target surface if the stencil test passes, and is ignored otherwise.</span></span> <span data-ttu-id="e133e-137">Поведение сравнения по умолчанию заключается в записи пикселя, независимо от того, как происходит каждая Побитовая операция (D3DCMP \_ всегда).</span><span class="sxs-lookup"><span data-stu-id="e133e-137">The default comparison behavior is to write the pixel, no matter how each bitwise operation turns out (D3DCMP\_ALWAYS).</span></span> <span data-ttu-id="e133e-138">Это поведение можно изменить, изменив значение \_ состояния рендеринга D3DRS стенЦилфунк, передав член перечислимого типа [**D3DCMPFUNC**](./d3dcmpfunc.md) , чтобы указать нужную функцию сравнения.</span><span class="sxs-lookup"><span data-stu-id="e133e-138">You can change this behavior by changing the value of the D3DRS\_STENCILFUNC render state, passing a member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type to identify the desired comparison function.</span></span>

<span data-ttu-id="e133e-139">Приложение может настроить работу буфера трафарета.</span><span class="sxs-lookup"><span data-stu-id="e133e-139">Your application can customize the operation of the stencil buffer.</span></span> <span data-ttu-id="e133e-140">Приложение может задать функцию сравнения, маску трафарета и контрольное значение трафарета.</span><span class="sxs-lookup"><span data-stu-id="e133e-140">It can set the comparison function, the stencil mask, and the stencil reference value.</span></span> <span data-ttu-id="e133e-141">Таким же образом задается действие, которое Direct3D выполняет при успешном или неудачном происхождении теста.</span><span class="sxs-lookup"><span data-stu-id="e133e-141">It can also control the action that Direct3D takes when the stencil test passes or fails.</span></span> <span data-ttu-id="e133e-142">Дополнительные сведения см. в разделе [состояние буфера набора элементов (Direct3D 9)](stencil-buffer-state.md).</span><span class="sxs-lookup"><span data-stu-id="e133e-142">For more information, see [Stencil Buffer State (Direct3D 9)](stencil-buffer-state.md).</span></span>

## <a name="examples"></a><span data-ttu-id="e133e-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="e133e-143">Examples</span></span>

<span data-ttu-id="e133e-144">В следующих примерах кода демонстрируется настройка буфера шаблона.</span><span class="sxs-lookup"><span data-stu-id="e133e-144">The following code examples demonstrate setting up the stencil buffer.</span></span>


```
// Enable stencil testing
pDevice->SetRenderState(D3DRS_STENCILENABLE, TRUE);

// Specify the stencil comparison function
pDevice->SetRenderState(D3DRS_STENCILFUNC, D3DCMP_EQUAL);

// Set the comparison reference value
pDevice->SetRenderState(D3DRS_STENCILREF, 0);

//  Specify a stencil mask 
pDevice->SetRenderState(D3DRS_STENCILMASK, 0);
```



<span data-ttu-id="e133e-145">По умолчанию значение ссылки на набор элементов равно нулю.</span><span class="sxs-lookup"><span data-stu-id="e133e-145">By default, the stencil reference value is zero.</span></span> <span data-ttu-id="e133e-146">Допустимо любое целочисленное значение.</span><span class="sxs-lookup"><span data-stu-id="e133e-146">Any integer value is valid.</span></span> <span data-ttu-id="e133e-147">Direct3D выполняет побитовую операцию и для значения ссылки на набор элементов и значение маски набора элементов перед тестом шаблона.</span><span class="sxs-lookup"><span data-stu-id="e133e-147">Direct3D performs a bitwise AND of the stencil reference value and a stencil mask value before the stencil test.</span></span>

<span data-ttu-id="e133e-148">Вы можете управлять тем, какие сведения о пикселях записываются в зависимости от сравнения наборов элементов.</span><span class="sxs-lookup"><span data-stu-id="e133e-148">You can control what pixel information is written out depending on the stencil comparison.</span></span>


```
// A write mask controls what is written
pDevice->SetRenderState(D3DRS_STENCILWRITEMASK, D3DSTENCILOP_KEEP);
// Specify when to write stencil data
pDevice->SetRenderState(D3DRS_STENCILFAIL, D3DSTENCILOP_KEEP);
```



<span data-ttu-id="e133e-149">Вы можете написать собственную формулу для значения, которое нужно записать в буфер шаблона, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="e133e-149">You can write your own formula for the value you want written into the stencil buffer as shown in the following example.</span></span>


```
NewStencilBufferValue = (StencilBufferValue & ~StencilWriteMask) | 
                        (StencilWriteMask & StencilOp(StencilBufferValue))
```



## <a name="related-topics"></a><span data-ttu-id="e133e-150">См. также</span><span class="sxs-lookup"><span data-stu-id="e133e-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e133e-151">Конвейер пикселей</span><span class="sxs-lookup"><span data-stu-id="e133e-151">Pixel Pipeline</span></span>](pixel-pipeline.md)
</dt> </dl>

 

 
