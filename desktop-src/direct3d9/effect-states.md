---
description: Состояния эффектов используются для инициализации состояний конвейера при подготовке к обработке вершин и пикселей.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Состояния эффектов (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 674e72d818cd280bfe75a2cb02733576bc68319e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104072256"
---
# <a name="effect-states-direct3d-9"></a><span data-ttu-id="4d04b-103">Состояния эффектов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="4d04b-103">Effect States (Direct3D 9)</span></span>

<span data-ttu-id="4d04b-104">Состояния эффектов используются для инициализации состояний конвейера при подготовке к обработке вершин и пикселей.</span><span class="sxs-lookup"><span data-stu-id="4d04b-104">Effect states are used to initialize pipeline states in preparation for vertex and pixel processing.</span></span>


```
effect state [ [index] ] = expression;
```



<span data-ttu-id="4d04b-105">Где:</span><span class="sxs-lookup"><span data-stu-id="4d04b-105">Where:</span></span>

-   <span data-ttu-id="4d04b-106">состояние результата — аналогично традиционному состоянию конвейера фиксированной функции.</span><span class="sxs-lookup"><span data-stu-id="4d04b-106">effect state - Similar to the traditional fixed function pipeline states.</span></span> <span data-ttu-id="4d04b-107">Ниже приведен полный список состояний.</span><span class="sxs-lookup"><span data-stu-id="4d04b-107">A complete list of states is provided below.</span></span>
-   <span data-ttu-id="4d04b-108">\[\[ \] Индекс \] — Необязательный целочисленный индекс.</span><span class="sxs-lookup"><span data-stu-id="4d04b-108">\[ \[index\] \] - Optional integer index.</span></span> <span data-ttu-id="4d04b-109">Индекс определяет определенное состояние в массиве состояний эффектов.</span><span class="sxs-lookup"><span data-stu-id="4d04b-109">The index identifies a particular state within an array of effect states.</span></span> <span data-ttu-id="4d04b-110">Внешние скобки указывают, что индекс является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4d04b-110">The outer brackets indicate that an index is optional.</span></span> <span data-ttu-id="4d04b-111">Если используется индекс, обязательно используйте внутренние скобки.</span><span class="sxs-lookup"><span data-stu-id="4d04b-111">If an index is used, be sure to use the inner brackets.</span></span>
-   <span data-ttu-id="4d04b-112">выражение назначения состояния выражения.</span><span class="sxs-lookup"><span data-stu-id="4d04b-112">expression - State assignment expression.</span></span> <span data-ttu-id="4d04b-113">См. раздел [выражения (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-113">See [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="4d04b-114">Каждое состояние имеет собственный тип данных.</span><span class="sxs-lookup"><span data-stu-id="4d04b-114">Each state has a native data type.</span></span> <span data-ttu-id="4d04b-115">Это тип данных, в котором состояние принимает значения в момент их назначения.</span><span class="sxs-lookup"><span data-stu-id="4d04b-115">This is the data type that the state expects values to be in when the effect assigns them.</span></span> <span data-ttu-id="4d04b-116">Ниже перечислены типы данных, которые требуются для каждого состояния.</span><span class="sxs-lookup"><span data-stu-id="4d04b-116">The data types that each state expects are listed below.</span></span>

<span data-ttu-id="4d04b-117">Обратите внимание, что интерфейс Effect будет пытаться привести значения к соответствующему типу как можно раньше.</span><span class="sxs-lookup"><span data-stu-id="4d04b-117">Note that the effect interface will attempt to cast values to the appropriate type as early as possible.</span></span> <span data-ttu-id="4d04b-118">Литеральные значения могут быть приведены во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="4d04b-118">Literal values can be cast at compile time.</span></span> <span data-ttu-id="4d04b-119">Не литералы (т. е. обычные переменные) должны быть приведены при вызове соответствующих методов набора.</span><span class="sxs-lookup"><span data-stu-id="4d04b-119">Non-literals (i.e. regular variables) need to be cast when the appropriate Set methods are called.</span></span> <span data-ttu-id="4d04b-120">Например, интерфейс Effect будет приводить значения, заданные с помощью [**сетбул**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md)и других аналогичных функций, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="4d04b-120">For example, the effect interface will cast values set using [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md), and other similar functions if necessary.</span></span> <span data-ttu-id="4d04b-121">Для повышения производительности убедитесь, что значения, передаваемые в интерфейс Effect, уже имеют правильный тип и не требуют приведения.</span><span class="sxs-lookup"><span data-stu-id="4d04b-121">For better performance ensure that the values passed to the effect interface are already the correct type and will not need casting.</span></span> <span data-ttu-id="4d04b-122">Если среде выполнения не удается привести значение, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="4d04b-122">If the runtime is unable to cast a value, an error is returned.</span></span>

<span data-ttu-id="4d04b-123">Состояния эффектов можно разделить на следующие категории:</span><span class="sxs-lookup"><span data-stu-id="4d04b-123">Effect states can be broken up into the following categories:</span></span>

-   [<span data-ttu-id="4d04b-124">Состояния освещения</span><span class="sxs-lookup"><span data-stu-id="4d04b-124">Light States</span></span>](#light-states)
-   [<span data-ttu-id="4d04b-125">Состояния материалов</span><span class="sxs-lookup"><span data-stu-id="4d04b-125">Material States</span></span>](#material-states)
-   [<span data-ttu-id="4d04b-126">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="4d04b-126">Render States</span></span>](#render-states)
    -   [<span data-ttu-id="4d04b-127">Состояния рендеринга пиксельного канала</span><span class="sxs-lookup"><span data-stu-id="4d04b-127">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
    -   [<span data-ttu-id="4d04b-128">Состояния рендеринга канала вершин</span><span class="sxs-lookup"><span data-stu-id="4d04b-128">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)
-   [<span data-ttu-id="4d04b-129">Состояния образцов</span><span class="sxs-lookup"><span data-stu-id="4d04b-129">Sampler States</span></span>](#sampler-states)
-   [<span data-ttu-id="4d04b-130">Состояния стадий образца</span><span class="sxs-lookup"><span data-stu-id="4d04b-130">Sampler Stage States</span></span>](#sampler-stage-states)
-   [<span data-ttu-id="4d04b-131">Состояния шейдера</span><span class="sxs-lookup"><span data-stu-id="4d04b-131">Shader States</span></span>](#shader-states)
-   [<span data-ttu-id="4d04b-132">Состояния констант шейдера</span><span class="sxs-lookup"><span data-stu-id="4d04b-132">Shader Constant States</span></span>](#shader-constant-states)
-   [<span data-ttu-id="4d04b-133">Состояния текстуры</span><span class="sxs-lookup"><span data-stu-id="4d04b-133">Texture States</span></span>](#texture-states)
-   [<span data-ttu-id="4d04b-134">Состояния стадии текстуры</span><span class="sxs-lookup"><span data-stu-id="4d04b-134">Texture Stage States</span></span>](#texture-stage-states)
-   [<span data-ttu-id="4d04b-135">Состояния преобразования</span><span class="sxs-lookup"><span data-stu-id="4d04b-135">Transform States</span></span>](#transform-states)

## <a name="light-states"></a><span data-ttu-id="4d04b-136">Состояния освещения</span><span class="sxs-lookup"><span data-stu-id="4d04b-136">Light States</span></span>

<span data-ttu-id="4d04b-137">Чтобы обеспечить наилучшую производительность при применении эффектов, все компоненты источника «источник» или «материал» должны быть указаны в файле результатов.</span><span class="sxs-lookup"><span data-stu-id="4d04b-137">To enable the best performance for applying an effect, all components of a light or a material should be specified in the effect file.</span></span> <span data-ttu-id="4d04b-138">Для состояний, которые не удалось объявить, задается какое-либо значение по умолчанию, так как Direct3D не может устанавливать состояния освещения по отдельности.</span><span class="sxs-lookup"><span data-stu-id="4d04b-138">States that you fail to declare are set to some default value because there is no way for Direct3D to set light states individually.</span></span>



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d04b-139">Светлое состояние</span><span class="sxs-lookup"><span data-stu-id="4d04b-139">Light State</span></span>            | <span data-ttu-id="4d04b-140">Тип</span><span class="sxs-lookup"><span data-stu-id="4d04b-140">Type</span></span>   | <span data-ttu-id="4d04b-141">Значения</span><span class="sxs-lookup"><span data-stu-id="4d04b-141">Values</span></span>                                                                                                              |
| <span data-ttu-id="4d04b-142">Лигхтамбиент \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-142">LightAmbient\[n\]</span></span>      | <span data-ttu-id="4d04b-143">float4</span><span class="sxs-lookup"><span data-stu-id="4d04b-143">float4</span></span> | <span data-ttu-id="4d04b-144">См. элемент окружения [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-144">See the Ambient member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="4d04b-145">LightAttenuation0 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-145">LightAttenuation0\[n\]</span></span> | <span data-ttu-id="4d04b-146">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-146">float</span></span>  | <span data-ttu-id="4d04b-147">См. элемент Attenuation0 элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-147">See the Attenuation0 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="4d04b-148">LightAttenuation1 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-148">LightAttenuation1\[n\]</span></span> | <span data-ttu-id="4d04b-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-149">float</span></span>  | <span data-ttu-id="4d04b-150">См. элемент Attenuation1 элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-150">See the Attenuation1 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="4d04b-151">LightAttenuation2 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-151">LightAttenuation2\[n\]</span></span> | <span data-ttu-id="4d04b-152">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-152">float</span></span>  | <span data-ttu-id="4d04b-153">См. элемент Attenuation2 элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-153">See the Attenuation2 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="4d04b-154">Лигхтдиффусе \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-154">LightDiffuse\[n\]</span></span>      | <span data-ttu-id="4d04b-155">float4</span><span class="sxs-lookup"><span data-stu-id="4d04b-155">float4</span></span> | <span data-ttu-id="4d04b-156">См. элемент диффузия [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-156">See the Diffuse member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="4d04b-157">Лигхтдиректион \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-157">LightDirection\[n\]</span></span>    | <span data-ttu-id="4d04b-158">float3</span><span class="sxs-lookup"><span data-stu-id="4d04b-158">float3</span></span> | <span data-ttu-id="4d04b-159">См. элемент Direction элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-159">See the Direction member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                         |
| <span data-ttu-id="4d04b-160">Досветлить \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-160">LightEnable\[n\]</span></span>       | <span data-ttu-id="4d04b-161">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-161">bool</span></span>   | <span data-ttu-id="4d04b-162">**True** или **false**.</span><span class="sxs-lookup"><span data-stu-id="4d04b-162">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="4d04b-163">См. аргумент Бенабле в качестве более [**светлого**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="4d04b-163">See the bEnable argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>            |
| <span data-ttu-id="4d04b-164">Лигхтфаллофф \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-164">LightFalloff\[n\]</span></span>      | <span data-ttu-id="4d04b-165">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-165">float</span></span>  | <span data-ttu-id="4d04b-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span> <span data-ttu-id="4d04b-167">См. элемент рассеивания [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-167">See the Falloff member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                   |
| <span data-ttu-id="4d04b-168">Лигхтфи \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-168">LightPhi\[n\]</span></span>          | <span data-ttu-id="4d04b-169">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-169">float</span></span>  | <span data-ttu-id="4d04b-170">См. элемент фи элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-170">See the Phi member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                               |
| <span data-ttu-id="4d04b-171">Лигхтпоситион \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-171">LightPosition\[n\]</span></span>     | <span data-ttu-id="4d04b-172">float3</span><span class="sxs-lookup"><span data-stu-id="4d04b-172">float3</span></span> | <span data-ttu-id="4d04b-173">См. элемент расположения [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-173">See the Position member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="4d04b-174">Лигхтранже \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-174">LightRange\[n\]</span></span>        | <span data-ttu-id="4d04b-175">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-175">float</span></span>  | <span data-ttu-id="4d04b-176">См. элемент Range элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-176">See the Range member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="4d04b-177">Лигхтспекулар \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-177">LightSpecular\[n\]</span></span>     | <span data-ttu-id="4d04b-178">float4</span><span class="sxs-lookup"><span data-stu-id="4d04b-178">float4</span></span> | <span data-ttu-id="4d04b-179">См. отраженный элемент [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-179">See the Specular member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="4d04b-180">Лигхтсета \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-180">LightTheta\[n\]</span></span>        | <span data-ttu-id="4d04b-181">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-181">float</span></span>  | <span data-ttu-id="4d04b-182">См. элемент тета элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-182">See the Theta member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="4d04b-183">Лигхттипе \[ n\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-183">LightType\[n\]</span></span>         | <span data-ttu-id="4d04b-184">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-184">dword</span></span>  | <span data-ttu-id="4d04b-185">То же значение, что и для массива до n значений [**D3DLIGHTTYPE**](./d3dlighttype.md) без \_ префикса D3DLIGHT.</span><span class="sxs-lookup"><span data-stu-id="4d04b-185">Same value as the array of up to n [**D3DLIGHTTYPE**](./d3dlighttype.md) values without the D3DLIGHT\_ prefix.</span></span> |



 

<span data-ttu-id="4d04b-186">Пример.</span><span class="sxs-lookup"><span data-stu-id="4d04b-186">Example:</span></span>


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



<span data-ttu-id="4d04b-187">Это позволит включить освещение, сделать выбор для типа, установить для параметра "источник света" значение float3<10.0 f, 1.0 f, 23.0 f> и задать окружающий цвет float4<0,7 f, 0,0 f, 0,0 f, 1.0 f>.</span><span class="sxs-lookup"><span data-stu-id="4d04b-187">This will enable lighting, make point lighting the type, set the light position to float3<10.0f, 1.0f, 23.0f>, and set the ambient color to float4<0.7f, 0.0f, 0.0f, 1.0f>.</span></span>

## <a name="material-states"></a><span data-ttu-id="4d04b-188">Состояния материалов</span><span class="sxs-lookup"><span data-stu-id="4d04b-188">Material States</span></span>

<span data-ttu-id="4d04b-189">Для состояний, которые не удалось объявить, задается какое-либо значение по умолчанию, так как Direct3D не может устанавливать материальновые состояния по отдельности.</span><span class="sxs-lookup"><span data-stu-id="4d04b-189">States that you fail to declare are set to some default value because there is no way for Direct3D to set material states individually.</span></span>



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| <span data-ttu-id="4d04b-190">Состояние материала</span><span class="sxs-lookup"><span data-stu-id="4d04b-190">Material State</span></span>   | <span data-ttu-id="4d04b-191">Тип</span><span class="sxs-lookup"><span data-stu-id="4d04b-191">Type</span></span>   | <span data-ttu-id="4d04b-192">Значения</span><span class="sxs-lookup"><span data-stu-id="4d04b-192">Values</span></span>                                         |
| <span data-ttu-id="4d04b-193">Свойство materialambient</span><span class="sxs-lookup"><span data-stu-id="4d04b-193">MaterialAmbient</span></span>  | <span data-ttu-id="4d04b-194">float4</span><span class="sxs-lookup"><span data-stu-id="4d04b-194">float4</span></span> | <span data-ttu-id="4d04b-195">То же значение, что и во [ **внешнем**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="4d04b-195">Same value as [**Ambient**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="4d04b-196">MaterialDiffuse</span><span class="sxs-lookup"><span data-stu-id="4d04b-196">MaterialDiffuse</span></span>  | <span data-ttu-id="4d04b-197">float4</span><span class="sxs-lookup"><span data-stu-id="4d04b-197">float4</span></span> | <span data-ttu-id="4d04b-198">То же значение, что и [ **рассеянный**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="4d04b-198">Same value as [**Diffuse**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="4d04b-199">MaterialEmissive</span><span class="sxs-lookup"><span data-stu-id="4d04b-199">MaterialEmissive</span></span> | <span data-ttu-id="4d04b-200">float4</span><span class="sxs-lookup"><span data-stu-id="4d04b-200">float4</span></span> | <span data-ttu-id="4d04b-201">То же значение, что и [ **эмиссионный**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="4d04b-201">Same value as [**Emissive**](d3dmaterial9.md)</span></span> |
| <span data-ttu-id="4d04b-202">материалповер</span><span class="sxs-lookup"><span data-stu-id="4d04b-202">MaterialPower</span></span>    | <span data-ttu-id="4d04b-203">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-203">float</span></span>  | <span data-ttu-id="4d04b-204">То же значение, что и для [ **Power**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="4d04b-204">Same value as [**Power**](d3dmaterial9.md)</span></span>    |
| <span data-ttu-id="4d04b-205">MaterialSpecular</span><span class="sxs-lookup"><span data-stu-id="4d04b-205">MaterialSpecular</span></span> | <span data-ttu-id="4d04b-206">float4</span><span class="sxs-lookup"><span data-stu-id="4d04b-206">float4</span></span> | <span data-ttu-id="4d04b-207">То же значение, что и для [ **отражения**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="4d04b-207">Same value as [**Specular**](d3dmaterial9.md)</span></span> |



 

<span data-ttu-id="4d04b-208">Пример.</span><span class="sxs-lookup"><span data-stu-id="4d04b-208">Example:</span></span>


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



<span data-ttu-id="4d04b-209">При этом для рассеянного цвета будет задано значение float4<0,7 f, 0,0 f, 0,0 f, 1.0 f> и сделать возможной мощь материала 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="4d04b-209">This will set the diffuse color to float4<0.7f, 0.0f, 0.0f, 1.0f> and make the power of the material 3.0f.</span></span>

## <a name="render-states"></a><span data-ttu-id="4d04b-210">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="4d04b-210">Render States</span></span>

<span data-ttu-id="4d04b-211">Существует два типа состояний рендеринга:</span><span class="sxs-lookup"><span data-stu-id="4d04b-211">There are two types of render states:</span></span>

-   [<span data-ttu-id="4d04b-212">Состояния рендеринга пиксельного канала</span><span class="sxs-lookup"><span data-stu-id="4d04b-212">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
-   [<span data-ttu-id="4d04b-213">Состояния рендеринга канала вершин</span><span class="sxs-lookup"><span data-stu-id="4d04b-213">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a><span data-ttu-id="4d04b-214">Состояния рендеринга пиксельного канала</span><span class="sxs-lookup"><span data-stu-id="4d04b-214">Pixel Pipe Render States</span></span>

<span data-ttu-id="4d04b-215">Состояния визуализации файла эффектов имеют имена, аналогичные состояниям конвейера фиксированной функции, часто с удаленным префиксом.</span><span class="sxs-lookup"><span data-stu-id="4d04b-215">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="4d04b-216">Состояние визуализации</span><span class="sxs-lookup"><span data-stu-id="4d04b-216">Render State</span></span></td>
<td><span data-ttu-id="4d04b-217">Тип</span><span class="sxs-lookup"><span data-stu-id="4d04b-217">Type</span></span></td>
<td><span data-ttu-id="4d04b-218">Значения</span><span class="sxs-lookup"><span data-stu-id="4d04b-218">Values</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-219">алфабленденабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-219">AlphaBlendEnable</span></span></td>
<td><span data-ttu-id="4d04b-220">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-220">bool</span></span></td>
<td><span data-ttu-id="4d04b-221">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-221">True or False.</span></span> <span data-ttu-id="4d04b-222">Те же значения, что и D3DRS_ALPHABLENDENABLE в <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4d04b-222">Same values as D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d04b-223">алфафунк</span><span class="sxs-lookup"><span data-stu-id="4d04b-223">AlphaFunc</span></span></td>
<td><span data-ttu-id="4d04b-224">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-224">dword</span></span></td>
<td><span data-ttu-id="4d04b-225">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> без префикса D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="4d04b-225">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="4d04b-226">См. D3DRS_ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="4d04b-226">See D3DRS_ALPHAFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-227">алфареф</span><span class="sxs-lookup"><span data-stu-id="4d04b-227">AlphaRef</span></span></td>
<td><span data-ttu-id="4d04b-228">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-228">dword</span></span></td>
<td><span data-ttu-id="4d04b-229">Те же значения, что и D3DRS_ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="4d04b-229">Same values as D3DRS_ALPHAREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d04b-230">алфатестенабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-230">AlphaTestEnable</span></span></td>
<td><span data-ttu-id="4d04b-231">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-231">dword</span></span></td>
<td><span data-ttu-id="4d04b-232">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-232">True or False.</span></span> <span data-ttu-id="4d04b-233">См. D3DRS_ALPHATESTENABLE.</span><span class="sxs-lookup"><span data-stu-id="4d04b-233">See D3DRS_ALPHATESTENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-234">блендоп</span><span class="sxs-lookup"><span data-stu-id="4d04b-234">BlendOp</span></span></td>
<td><span data-ttu-id="4d04b-235">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-235">dword</span></span></td>
<td><span data-ttu-id="4d04b-236">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> без префикса D3DBLENDOP_.</span><span class="sxs-lookup"><span data-stu-id="4d04b-236">Same values as <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> without the D3DBLENDOP_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d04b-237">колорвритинабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-237">ColorWriteEnable</span></span></td>
<td><span data-ttu-id="4d04b-238">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-238">dword</span></span></td>
<td><span data-ttu-id="4d04b-239">Побитовое сочетание красного цвета | ЗЕЛЕНЫЙ | СИНИЙ | Буквы.</span><span class="sxs-lookup"><span data-stu-id="4d04b-239">Bitwise combination of RED|GREEN|BLUE|ALPHA.</span></span> <span data-ttu-id="4d04b-240">См. D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="4d04b-240">See D3DRS_COLORWRITEENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-241">депсбиас</span><span class="sxs-lookup"><span data-stu-id="4d04b-241">DepthBias</span></span></td>
<td><span data-ttu-id="4d04b-242">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-242">float</span></span></td>
<td><span data-ttu-id="4d04b-243">Те же значения, что и D3DRS_DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-243">Same values as D3DRS_DEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d04b-244">дестбленд</span><span class="sxs-lookup"><span data-stu-id="4d04b-244">DestBlend</span></span></td>
<td><span data-ttu-id="4d04b-245">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-245">dword</span></span></td>
<td><span data-ttu-id="4d04b-246">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> без префикса D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="4d04b-246">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-247">дисеренабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-247">DitherEnable</span></span></td>
<td><span data-ttu-id="4d04b-248">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-248">bool</span></span></td>
<td><span data-ttu-id="4d04b-249">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-249">True or False.</span></span> <span data-ttu-id="4d04b-250">Те же значения, что и D3DRS_DITHERENABLE.</span><span class="sxs-lookup"><span data-stu-id="4d04b-250">Same values as D3DRS_DITHERENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d04b-251">филлмоде</span><span class="sxs-lookup"><span data-stu-id="4d04b-251">FillMode</span></span></td>
<td><span data-ttu-id="4d04b-252">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-252">dword</span></span></td>
<td><span data-ttu-id="4d04b-253">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> без префикса D3DFILL_.</span><span class="sxs-lookup"><span data-stu-id="4d04b-253">Same values as <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> without the D3DFILL_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-254">ластпиксел</span><span class="sxs-lookup"><span data-stu-id="4d04b-254">LastPixel</span></span></td>
<td><span data-ttu-id="4d04b-255">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-255">dword</span></span></td>
<td><span data-ttu-id="4d04b-256">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-256">True or False.</span></span> <span data-ttu-id="4d04b-257">См. D3DRS_LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="4d04b-257">See D3DRS_LASTPIXEL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d04b-258">шадемоде</span><span class="sxs-lookup"><span data-stu-id="4d04b-258">ShadeMode</span></span></td>
<td><span data-ttu-id="4d04b-259">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-259">dword</span></span></td>
<td><span data-ttu-id="4d04b-260">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> без префикса D3DSHADE_.</span><span class="sxs-lookup"><span data-stu-id="4d04b-260">Same values as <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> without the D3DSHADE_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-261">слопескаледепсбиас</span><span class="sxs-lookup"><span data-stu-id="4d04b-261">SlopeScaleDepthBias</span></span></td>
<td><span data-ttu-id="4d04b-262">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-262">float</span></span></td>
<td><span data-ttu-id="4d04b-263">Те же значения, что и D3DRS_SLOPESCALEDEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-263">Same values as D3DRS_SLOPESCALEDEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d04b-264">сркбленд</span><span class="sxs-lookup"><span data-stu-id="4d04b-264">SrcBlend</span></span></td>
<td><span data-ttu-id="4d04b-265">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-265">dword</span></span></td>
<td><span data-ttu-id="4d04b-266">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> без префикса D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="4d04b-266">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-267">стенЦиленабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-267">StencilEnable</span></span></td>
<td><span data-ttu-id="4d04b-268">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-268">bool</span></span></td>
<td><span data-ttu-id="4d04b-269">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-269">True or False.</span></span> <span data-ttu-id="4d04b-270">Те же значения, что и D3DRS_STENCILENABLE.</span><span class="sxs-lookup"><span data-stu-id="4d04b-270">Same values as D3DRS_STENCILENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d04b-271">стенЦилфаил</span><span class="sxs-lookup"><span data-stu-id="4d04b-271">StencilFail</span></span></td>
<td><span data-ttu-id="4d04b-272">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-272">dword</span></span></td>
<td><span data-ttu-id="4d04b-273">Те же значения, что и <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> без префикса D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="4d04b-273">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="4d04b-274">См. D3DRS_STENCILFAIL.</span><span class="sxs-lookup"><span data-stu-id="4d04b-274">See D3DRS_STENCILFAIL.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-275">стенЦилфунк</span><span class="sxs-lookup"><span data-stu-id="4d04b-275">StencilFunc</span></span></td>
<td><span data-ttu-id="4d04b-276">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-276">dword</span></span></td>
<td><span data-ttu-id="4d04b-277">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> без префикса D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="4d04b-277">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="4d04b-278">См. D3DRS_STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="4d04b-278">See D3DRS_STENCILFUNC.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d04b-279">стенЦилмаск</span><span class="sxs-lookup"><span data-stu-id="4d04b-279">StencilMask</span></span></td>
<td><span data-ttu-id="4d04b-280">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-280">dword</span></span></td>
<td><span data-ttu-id="4d04b-281">Те же значения, что и D3DRS_STENCILMASK.</span><span class="sxs-lookup"><span data-stu-id="4d04b-281">Same values as D3DRS_STENCILMASK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-282">стенЦилпасс</span><span class="sxs-lookup"><span data-stu-id="4d04b-282">StencilPass</span></span></td>
<td><span data-ttu-id="4d04b-283">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-283">dword</span></span></td>
<td><span data-ttu-id="4d04b-284">Те же значения, что и <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> без префикса D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="4d04b-284">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="4d04b-285">См. D3DRS_STENCILPASS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-285">See D3DRS_STENCILPASS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d04b-286">стенЦилреф</span><span class="sxs-lookup"><span data-stu-id="4d04b-286">StencilRef</span></span></td>
<td><span data-ttu-id="4d04b-287">INT</span><span class="sxs-lookup"><span data-stu-id="4d04b-287">int</span></span></td>
<td><span data-ttu-id="4d04b-288">Те же значения, что и D3DRS_STENCILREF.</span><span class="sxs-lookup"><span data-stu-id="4d04b-288">Same values as D3DRS_STENCILREF.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-289">стенЦилвритемаск</span><span class="sxs-lookup"><span data-stu-id="4d04b-289">StencilWriteMask</span></span></td>
<td><span data-ttu-id="4d04b-290">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-290">dword</span></span></td>
<td><span data-ttu-id="4d04b-291">Те же значения, что и D3DRS_STENCILWRITEMASK.</span><span class="sxs-lookup"><span data-stu-id="4d04b-291">Same values as D3DRS_STENCILWRITEMASK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d04b-292">стенЦилзфаил</span><span class="sxs-lookup"><span data-stu-id="4d04b-292">StencilZFail</span></span></td>
<td><span data-ttu-id="4d04b-293">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-293">dword</span></span></td>
<td><span data-ttu-id="4d04b-294">Те же значения, что и <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> без префикса D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="4d04b-294">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="4d04b-295">См. D3DRS_STENCILZFAIL.</span><span class="sxs-lookup"><span data-stu-id="4d04b-295">See D3DRS_STENCILZFAIL.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-296">текстурефактор</span><span class="sxs-lookup"><span data-stu-id="4d04b-296">TextureFactor</span></span></td>
<td><span data-ttu-id="4d04b-297">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-297">dword</span></span></td>
<td><span data-ttu-id="4d04b-298">Те же значения, что и <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="4d04b-298">Same values as <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span></span> <span data-ttu-id="4d04b-299">Те же значения, что и D3DRS_TEXTUREFACTOR.</span><span class="sxs-lookup"><span data-stu-id="4d04b-299">Same values as D3DRS_TEXTUREFACTOR.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d04b-300">Wrap0 - Wrap15</span><span class="sxs-lookup"><span data-stu-id="4d04b-300">Wrap0 - Wrap15</span></span></td>
<td><span data-ttu-id="4d04b-301">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-301">dword</span></span></td>
<td><span data-ttu-id="4d04b-302">Значения совпадают со значениями, используемыми D3DRS_WRAP0.</span><span class="sxs-lookup"><span data-stu-id="4d04b-302">Values are the same as the values used by D3DRS_WRAP0.</span></span> <span data-ttu-id="4d04b-303">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="4d04b-303">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="4d04b-304">COORD0 (соответствует D3DWRAPCOORD_0)</span><span class="sxs-lookup"><span data-stu-id="4d04b-304">COORD0 (which corresponds to D3DWRAPCOORD_0)</span></span></li>
<li><span data-ttu-id="4d04b-305">COORD1 (соответствует D3DWRAPCOORD_1)</span><span class="sxs-lookup"><span data-stu-id="4d04b-305">COORD1 (which corresponds to D3DWRAPCOORD_1)</span></span></li>
<li><span data-ttu-id="4d04b-306">COORD2 (соответствует D3DWRAPCOORD_2)</span><span class="sxs-lookup"><span data-stu-id="4d04b-306">COORD2 (which corresponds to D3DWRAPCOORD_2)</span></span></li>
<li><span data-ttu-id="4d04b-307">COORD3 (соответствует D3DWRAPCOORD_3)</span><span class="sxs-lookup"><span data-stu-id="4d04b-307">COORD3 (which corresponds to D3DWRAPCOORD_3)</span></span></li>
<li><span data-ttu-id="4d04b-308">U (соответствует D3DWRAP_U)</span><span class="sxs-lookup"><span data-stu-id="4d04b-308">U (which corresponds to D3DWRAP_U)</span></span></li>
<li><span data-ttu-id="4d04b-309">V (соответствует D3DWRAP_V)</span><span class="sxs-lookup"><span data-stu-id="4d04b-309">V (which corresponds to D3DWRAP_V)</span></span></li>
<li><span data-ttu-id="4d04b-310">W (соответствует D3DWRAP_W)</span><span class="sxs-lookup"><span data-stu-id="4d04b-310">W (which corresponds to D3DWRAP_W)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-311">зенабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-311">ZEnable</span></span></td>
<td><span data-ttu-id="4d04b-312">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-312">dword</span></span></td>
<td><span data-ttu-id="4d04b-313">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> без префикса D3DZB_.</span><span class="sxs-lookup"><span data-stu-id="4d04b-313">Same values as <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> without the D3DZB_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="4d04b-314">зфунк</span><span class="sxs-lookup"><span data-stu-id="4d04b-314">ZFunc</span></span></td>
<td><span data-ttu-id="4d04b-315">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-315">dword</span></span></td>
<td><span data-ttu-id="4d04b-316">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> без префикса D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="4d04b-316">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="4d04b-317">См. D3DRS_ZFUNC.</span><span class="sxs-lookup"><span data-stu-id="4d04b-317">See D3DRS_ZFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="4d04b-318">звритинабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-318">ZWriteEnable</span></span></td>
<td><span data-ttu-id="4d04b-319">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-319">bool</span></span></td>
<td><span data-ttu-id="4d04b-320">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-320">True or False.</span></span> <span data-ttu-id="4d04b-321">См. D3DRS_ZWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="4d04b-321">See D3DRS_ZWRITEENABLE.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="4d04b-322">Пример.</span><span class="sxs-lookup"><span data-stu-id="4d04b-322">Example:</span></span>


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



<span data-ttu-id="4d04b-323">Это позволит включить альфа-смешение и сделать все геометрические отрисовкой в каркасе.</span><span class="sxs-lookup"><span data-stu-id="4d04b-323">This will enable alpha blending and make all geometries render in wireframe.</span></span>

### <a name="vertex-pipe-render-states"></a><span data-ttu-id="4d04b-324">Состояния рендеринга канала вершин</span><span class="sxs-lookup"><span data-stu-id="4d04b-324">Vertex Pipe Render States</span></span>

<span data-ttu-id="4d04b-325">Состояния визуализации файла эффектов имеют имена, аналогичные состояниям конвейера фиксированной функции, часто с удаленным префиксом.</span><span class="sxs-lookup"><span data-stu-id="4d04b-325">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d04b-326">Состояние визуализации</span><span class="sxs-lookup"><span data-stu-id="4d04b-326">Render State</span></span>             | <span data-ttu-id="4d04b-327">Тип</span><span class="sxs-lookup"><span data-stu-id="4d04b-327">Type</span></span>   | <span data-ttu-id="4d04b-328">Значения</span><span class="sxs-lookup"><span data-stu-id="4d04b-328">Values</span></span>                                                                                                                                        |
| <span data-ttu-id="4d04b-329">Окружающее</span><span class="sxs-lookup"><span data-stu-id="4d04b-329">Ambient</span></span>                  | <span data-ttu-id="4d04b-330">float4</span><span class="sxs-lookup"><span data-stu-id="4d04b-330">float4</span></span> | <span data-ttu-id="4d04b-331">Те же значения, что и во \_ внешнем D3DRS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-331">Same values as D3DRS\_AMBIENT.</span></span>                                                                                                                |
| <span data-ttu-id="4d04b-332">амбиентматериалсаурце</span><span class="sxs-lookup"><span data-stu-id="4d04b-332">AmbientMaterialSource</span></span>    | <span data-ttu-id="4d04b-333">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-333">dword</span></span>  | <span data-ttu-id="4d04b-334">Те же значения, что и [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) без \_ префикса D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-334">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="4d04b-335">См. раздел D3DRS \_ амбиентматериалсаурце.</span><span class="sxs-lookup"><span data-stu-id="4d04b-335">See D3DRS\_AMBIENTMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="4d04b-336">Усечение</span><span class="sxs-lookup"><span data-stu-id="4d04b-336">Clipping</span></span>                 | <span data-ttu-id="4d04b-337">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-337">bool</span></span>   | <span data-ttu-id="4d04b-338">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-338">True or False.</span></span> <span data-ttu-id="4d04b-339">Те же значения, что и D3DRSная \_ Обрезка.</span><span class="sxs-lookup"><span data-stu-id="4d04b-339">Same values as D3DRS\_CLIPPING.</span></span>                                                                                                |
| <span data-ttu-id="4d04b-340">клиппланинабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-340">ClipPlaneEnable</span></span>          | <span data-ttu-id="4d04b-341">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-341">dword</span></span>  | <span data-ttu-id="4d04b-342">Побитовое сочетание макросов D3DCLIPPLANE0-D3DCLIPPLANE5.</span><span class="sxs-lookup"><span data-stu-id="4d04b-342">Bitwise combination of D3DCLIPPLANE0 - D3DCLIPPLANE5 macros.</span></span> <span data-ttu-id="4d04b-343">См. раздел [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS \_ клиппланинабле.</span><span class="sxs-lookup"><span data-stu-id="4d04b-343">See [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS\_CLIPPLANEENABLE.</span></span>           |
| <span data-ttu-id="4d04b-344">колорвертекс</span><span class="sxs-lookup"><span data-stu-id="4d04b-344">ColorVertex</span></span>              | <span data-ttu-id="4d04b-345">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-345">bool</span></span>   | <span data-ttu-id="4d04b-346">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-346">True or False.</span></span> <span data-ttu-id="4d04b-347">Те же значения, что и в D3DRS \_ колорвертекс.</span><span class="sxs-lookup"><span data-stu-id="4d04b-347">Same values as D3DRS\_COLORVERTEX.</span></span>                                                                                             |
| <span data-ttu-id="4d04b-348">куллмоде</span><span class="sxs-lookup"><span data-stu-id="4d04b-348">CullMode</span></span>                 | <span data-ttu-id="4d04b-349">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-349">dword</span></span>  | <span data-ttu-id="4d04b-350">Те же значения, что и [**D3DCULL**](./d3dcull.md) без \_ префикса D3DCULL.</span><span class="sxs-lookup"><span data-stu-id="4d04b-350">Same values as [**D3DCULL**](./d3dcull.md) without the D3DCULL\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="4d04b-351">диффусематериалсаурце</span><span class="sxs-lookup"><span data-stu-id="4d04b-351">DiffuseMaterialSource</span></span>    | <span data-ttu-id="4d04b-352">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-352">dword</span></span>  | <span data-ttu-id="4d04b-353">Те же значения, что и [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) без \_ префикса D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-353">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="4d04b-354">См. раздел D3DRS \_ диффусематериалсаурце.</span><span class="sxs-lookup"><span data-stu-id="4d04b-354">See D3DRS\_DIFFUSEMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="4d04b-355">емиссивематериалсаурце</span><span class="sxs-lookup"><span data-stu-id="4d04b-355">EmissiveMaterialSource</span></span>   | <span data-ttu-id="4d04b-356">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-356">dword</span></span>  | <span data-ttu-id="4d04b-357">Те же значения, что и [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) без \_ префикса D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-357">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="4d04b-358">См. раздел D3DRS \_ емиссивематериалсаурце.</span><span class="sxs-lookup"><span data-stu-id="4d04b-358">See D3DRS\_EMISSIVEMATERIALSOURCE.</span></span> |
| <span data-ttu-id="4d04b-359">фогколор</span><span class="sxs-lookup"><span data-stu-id="4d04b-359">FogColor</span></span>                 | <span data-ttu-id="4d04b-360">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-360">dword</span></span>  | <span data-ttu-id="4d04b-361">Те же значения, что и [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-361">Same values as [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="4d04b-362">См. раздел D3DRS \_ фогколор.</span><span class="sxs-lookup"><span data-stu-id="4d04b-362">See D3DRS\_FOGCOLOR.</span></span>                                                                             |
| <span data-ttu-id="4d04b-363">фогденсити</span><span class="sxs-lookup"><span data-stu-id="4d04b-363">FogDensity</span></span>               | <span data-ttu-id="4d04b-364">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-364">float</span></span>  | <span data-ttu-id="4d04b-365">Те же значения, что и в D3DRS \_ фогденсити.</span><span class="sxs-lookup"><span data-stu-id="4d04b-365">Same values as D3DRS\_FOGDENSITY.</span></span>                                                                                                             |
| <span data-ttu-id="4d04b-366">фоженабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-366">FogEnable</span></span>                | <span data-ttu-id="4d04b-367">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-367">bool</span></span>   | <span data-ttu-id="4d04b-368">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-368">True or False.</span></span> <span data-ttu-id="4d04b-369">Те же значения, что и в D3DRS \_ фоженабле.</span><span class="sxs-lookup"><span data-stu-id="4d04b-369">Same values as D3DRS\_FOGENABLE.</span></span>                                                                                               |
| <span data-ttu-id="4d04b-370">фоженд</span><span class="sxs-lookup"><span data-stu-id="4d04b-370">FogEnd</span></span>                   | <span data-ttu-id="4d04b-371">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-371">float</span></span>  | <span data-ttu-id="4d04b-372">Те же значения, что и в D3DRS \_ фоженд.</span><span class="sxs-lookup"><span data-stu-id="4d04b-372">Same values as D3DRS\_FOGEND.</span></span>                                                                                                                 |
| <span data-ttu-id="4d04b-373">фогстарт</span><span class="sxs-lookup"><span data-stu-id="4d04b-373">FogStart</span></span>                 | <span data-ttu-id="4d04b-374">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-374">float</span></span>  | <span data-ttu-id="4d04b-375">Те же значения, что и в D3DRS \_ фогстарт.</span><span class="sxs-lookup"><span data-stu-id="4d04b-375">Same values as D3DRS\_FOGSTART.</span></span>                                                                                                               |
| <span data-ttu-id="4d04b-376">фогтаблемоде</span><span class="sxs-lookup"><span data-stu-id="4d04b-376">FogTableMode</span></span>             | <span data-ttu-id="4d04b-377">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-377">dword</span></span>  | <span data-ttu-id="4d04b-378">Те же значения, что и [**D3DFOGMODE**](./d3dfogmode.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-378">Same values as [**D3DFOGMODE**](./d3dfogmode.md).</span></span> <span data-ttu-id="4d04b-379">См. раздел D3DRS \_ фогтаблемоде in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="4d04b-379">See D3DRS\_FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span>     |
| <span data-ttu-id="4d04b-380">фогвертексмоде</span><span class="sxs-lookup"><span data-stu-id="4d04b-380">FogVertexMode</span></span>            | <span data-ttu-id="4d04b-381">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-381">dword</span></span>  | <span data-ttu-id="4d04b-382">Те же значения, что и [**D3DFOGMODE**](./d3dfogmode.md) без \_ префикса D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="4d04b-382">Same values as [**D3DFOGMODE**](./d3dfogmode.md) without the D3DFOG\_ prefix.</span></span>                                                            |
| <span data-ttu-id="4d04b-383">индекседвертексбленденабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-383">IndexedVertexBlendEnable</span></span> | <span data-ttu-id="4d04b-384">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-384">bool</span></span>   | <span data-ttu-id="4d04b-385">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-385">True or False.</span></span> <span data-ttu-id="4d04b-386">Те же значения, что и в D3DRS \_ индекседвертексбленденабле.</span><span class="sxs-lookup"><span data-stu-id="4d04b-386">Same values as D3DRS\_INDEXEDVERTEXBLENDENABLE.</span></span>                                                                                |
| <span data-ttu-id="4d04b-387">Освещение</span><span class="sxs-lookup"><span data-stu-id="4d04b-387">Lighting</span></span>                 | <span data-ttu-id="4d04b-388">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-388">bool</span></span>   | <span data-ttu-id="4d04b-389">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-389">True or False.</span></span> <span data-ttu-id="4d04b-390">Те же значения, что и D3DRS \_ освещение.</span><span class="sxs-lookup"><span data-stu-id="4d04b-390">Same values as D3DRS\_LIGHTING.</span></span>                                                                                                |
| <span data-ttu-id="4d04b-391">локалвиевер</span><span class="sxs-lookup"><span data-stu-id="4d04b-391">LocalViewer</span></span>              | <span data-ttu-id="4d04b-392">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-392">bool</span></span>   | <span data-ttu-id="4d04b-393">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-393">True or False.</span></span> <span data-ttu-id="4d04b-394">Те же значения, что и в D3DRS \_ локалвиевер.</span><span class="sxs-lookup"><span data-stu-id="4d04b-394">Same values as D3DRS\_LOCALVIEWER.</span></span>                                                                                             |
| <span data-ttu-id="4d04b-395">мултисамплеантиалиас</span><span class="sxs-lookup"><span data-stu-id="4d04b-395">MultiSampleAntialias</span></span>     | <span data-ttu-id="4d04b-396">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-396">bool</span></span>   | <span data-ttu-id="4d04b-397">Те же значения, что и в D3DRS \_ мултисамплеантиалиас.</span><span class="sxs-lookup"><span data-stu-id="4d04b-397">Same values as D3DRS\_MULTISAMPLEANTIALIAS.</span></span>                                                                                                   |
| <span data-ttu-id="4d04b-398">мултисамплемаск</span><span class="sxs-lookup"><span data-stu-id="4d04b-398">MultiSampleMask</span></span>          | <span data-ttu-id="4d04b-399">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-399">dword</span></span>  | <span data-ttu-id="4d04b-400">Те же значения, что и в D3DRS \_ мултисамплемаск.</span><span class="sxs-lookup"><span data-stu-id="4d04b-400">Same values as D3DRS\_MULTISAMPLEMASK.</span></span>                                                                                                        |
| <span data-ttu-id="4d04b-401">нормализенормалс</span><span class="sxs-lookup"><span data-stu-id="4d04b-401">NormalizeNormals</span></span>         | <span data-ttu-id="4d04b-402">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-402">bool</span></span>   | <span data-ttu-id="4d04b-403">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-403">True or False.</span></span> <span data-ttu-id="4d04b-404">Те же значения, что и в D3DRS \_ нормализенормалс.</span><span class="sxs-lookup"><span data-stu-id="4d04b-404">Same values as D3DRS\_NORMALIZENORMALS.</span></span>                                                                                        |
| <span data-ttu-id="4d04b-405">патчсегментс</span><span class="sxs-lookup"><span data-stu-id="4d04b-405">PatchSegments</span></span>            | <span data-ttu-id="4d04b-406">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-406">float</span></span>  | <span data-ttu-id="4d04b-407">Те же значения, что и в Нсегментс в [**сетнпатчмоде**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="4d04b-407">Same values as nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>                                                         |
| <span data-ttu-id="4d04b-408">Поинтскале \_ A</span><span class="sxs-lookup"><span data-stu-id="4d04b-408">PointScale\_A</span></span>            | <span data-ttu-id="4d04b-409">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-409">float</span></span>  | <span data-ttu-id="4d04b-410">Те же значения, что и D3DRS \_ поинтскале \_ A.</span><span class="sxs-lookup"><span data-stu-id="4d04b-410">Same values as D3DRS\_POINTSCALE\_A.</span></span>                                                                                                          |
| <span data-ttu-id="4d04b-411">Поинтскале \_ б</span><span class="sxs-lookup"><span data-stu-id="4d04b-411">PointScale\_B</span></span>            | <span data-ttu-id="4d04b-412">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-412">float</span></span>  | <span data-ttu-id="4d04b-413">Те же значения, что и в D3DRS \_ поинтскале \_ B.</span><span class="sxs-lookup"><span data-stu-id="4d04b-413">Same values as D3DRS\_POINTSCALE\_B.</span></span>                                                                                                          |
| <span data-ttu-id="4d04b-414">Поинтскале \_ C</span><span class="sxs-lookup"><span data-stu-id="4d04b-414">PointScale\_C</span></span>            | <span data-ttu-id="4d04b-415">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-415">float</span></span>  | <span data-ttu-id="4d04b-416">Те же значения, что и D3DRS \_ поинтскале \_ C.</span><span class="sxs-lookup"><span data-stu-id="4d04b-416">Same values as D3DRS\_POINTSCALE\_C.</span></span>                                                                                                          |
| <span data-ttu-id="4d04b-417">поинтскалинабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-417">PointScaleEnable</span></span>         | <span data-ttu-id="4d04b-418">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-418">bool</span></span>   | <span data-ttu-id="4d04b-419">Те же значения, что и в D3DRS \_ поинтскалинабле.</span><span class="sxs-lookup"><span data-stu-id="4d04b-419">Same values as D3DRS\_POINTSCALEENABLE.</span></span>                                                                                                       |
| <span data-ttu-id="4d04b-420">PointSize</span><span class="sxs-lookup"><span data-stu-id="4d04b-420">PointSize</span></span>                | <span data-ttu-id="4d04b-421">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-421">float</span></span>  | <span data-ttu-id="4d04b-422">Те же значения, что и в D3DRS \_ POINTSIZE.</span><span class="sxs-lookup"><span data-stu-id="4d04b-422">Same values as D3DRS\_POINTSIZE.</span></span>                                                                                                              |
| <span data-ttu-id="4d04b-423">PointSize \_ мин</span><span class="sxs-lookup"><span data-stu-id="4d04b-423">PointSize\_Min</span></span>           | <span data-ttu-id="4d04b-424">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-424">float</span></span>  | <span data-ttu-id="4d04b-425">Те же значения, что и D3DRS \_ POINTSIZE \_ min.</span><span class="sxs-lookup"><span data-stu-id="4d04b-425">Same values as D3DRS\_POINTSIZE\_MIN.</span></span>                                                                                                         |
| <span data-ttu-id="4d04b-426">PointSize \_ Max</span><span class="sxs-lookup"><span data-stu-id="4d04b-426">PointSize\_Max</span></span>           | <span data-ttu-id="4d04b-427">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-427">float</span></span>  | <span data-ttu-id="4d04b-428">Те же значения, что и D3DRS \_ POINTSIZE \_ Max без \_ префикса D3DRS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-428">Same values as D3DRS\_POINTSIZE\_MAX without the D3DRS\_ prefix.</span></span>                                                                              |
| <span data-ttu-id="4d04b-429">поинтспритинабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-429">PointSpriteEnable</span></span>        | <span data-ttu-id="4d04b-430">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-430">bool</span></span>   | <span data-ttu-id="4d04b-431">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-431">True or False.</span></span> <span data-ttu-id="4d04b-432">Те же значения, что и в D3DRS \_ поинтспритинабле.</span><span class="sxs-lookup"><span data-stu-id="4d04b-432">Same values as D3DRS\_POINTSPRITEENABLE.</span></span>                                                                                       |
| <span data-ttu-id="4d04b-433">ранжефоженабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-433">RangeFogEnable</span></span>           | <span data-ttu-id="4d04b-434">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-434">bool</span></span>   | <span data-ttu-id="4d04b-435">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-435">True or False.</span></span> <span data-ttu-id="4d04b-436">Те же значения, что и в D3DRS \_ ранжефоженабле.</span><span class="sxs-lookup"><span data-stu-id="4d04b-436">Same values as D3DRS\_RANGEFOGENABLE.</span></span>                                                                                          |
| <span data-ttu-id="4d04b-437">спекуларенабле</span><span class="sxs-lookup"><span data-stu-id="4d04b-437">SpecularEnable</span></span>           | <span data-ttu-id="4d04b-438">bool</span><span class="sxs-lookup"><span data-stu-id="4d04b-438">bool</span></span>   | <span data-ttu-id="4d04b-439">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="4d04b-439">True or False.</span></span> <span data-ttu-id="4d04b-440">Те же значения, что и в D3DRS \_ спекуларенабле.</span><span class="sxs-lookup"><span data-stu-id="4d04b-440">Same values as D3DRS\_SPECULARENABLE.</span></span>                                                                                          |
| <span data-ttu-id="4d04b-441">спекуларматериалсаурце</span><span class="sxs-lookup"><span data-stu-id="4d04b-441">SpecularMaterialSource</span></span>   | <span data-ttu-id="4d04b-442">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-442">dword</span></span>  | <span data-ttu-id="4d04b-443">Те же значения, что и [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) без \_ префикса D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-443">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="4d04b-444">См. раздел D3DRS \_ спекуларматериалсаурце.</span><span class="sxs-lookup"><span data-stu-id="4d04b-444">See D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="4d04b-445">твинфактор</span><span class="sxs-lookup"><span data-stu-id="4d04b-445">TweenFactor</span></span>              | <span data-ttu-id="4d04b-446">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-446">float</span></span>  | <span data-ttu-id="4d04b-447">Те же значения, что и в D3DRS \_ твинфактор.</span><span class="sxs-lookup"><span data-stu-id="4d04b-447">Same values as D3DRS\_TWEENFACTOR.</span></span>                                                                                                            |
| <span data-ttu-id="4d04b-448">вертексбленд</span><span class="sxs-lookup"><span data-stu-id="4d04b-448">VertexBlend</span></span>              | <span data-ttu-id="4d04b-449">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-449">dword</span></span>  | <span data-ttu-id="4d04b-450">Те же значения, что и [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) без \_ префикса D3DVBF.</span><span class="sxs-lookup"><span data-stu-id="4d04b-450">Same values as [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) without the D3DVBF\_ prefix.</span></span> <span data-ttu-id="4d04b-451">См. раздел D3DRS \_ вертексбленд.</span><span class="sxs-lookup"><span data-stu-id="4d04b-451">See D3DRS\_VERTEXBLEND.</span></span>                  |



 

<span data-ttu-id="4d04b-452">Пример.</span><span class="sxs-lookup"><span data-stu-id="4d04b-452">Example:</span></span>


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



<span data-ttu-id="4d04b-453">Это сделает окружающий цвет float4<0,7 f, 0,0 f, 0,0 f, 1.0 f>, задать для режима исчисления задних граней значение по часовой стрелке и установить красный цвет тумана.</span><span class="sxs-lookup"><span data-stu-id="4d04b-453">This will make the ambient color float4<0.7f, 0.0f, 0.0f, 1.0f>, set the backface culling mode to counter-clockwise, and set the fog color to red.</span></span>

## <a name="sampler-states"></a><span data-ttu-id="4d04b-454">Состояния образцов</span><span class="sxs-lookup"><span data-stu-id="4d04b-454">Sampler States</span></span>

<span data-ttu-id="4d04b-455">Состояние образца представляет объект образца.</span><span class="sxs-lookup"><span data-stu-id="4d04b-455">A sampler state represents a sampler object.</span></span>



|         |         |                                     |
|---------|---------|-------------------------------------|
| <span data-ttu-id="4d04b-456">Состояние</span><span class="sxs-lookup"><span data-stu-id="4d04b-456">State</span></span>   | <span data-ttu-id="4d04b-457">Тип</span><span class="sxs-lookup"><span data-stu-id="4d04b-457">Type</span></span>    | <span data-ttu-id="4d04b-458">Значения</span><span class="sxs-lookup"><span data-stu-id="4d04b-458">Values</span></span>                              |
| <span data-ttu-id="4d04b-459">Образец</span><span class="sxs-lookup"><span data-stu-id="4d04b-459">Sampler</span></span> | <span data-ttu-id="4d04b-460">образец</span><span class="sxs-lookup"><span data-stu-id="4d04b-460">sampler</span></span> | <span data-ttu-id="4d04b-461">**Значение NULL** или блок состояния образца.</span><span class="sxs-lookup"><span data-stu-id="4d04b-461">**NULL**, or a sampler state block.</span></span> |



 

## <a name="sampler-stage-states"></a><span data-ttu-id="4d04b-462">Состояния стадий образца</span><span class="sxs-lookup"><span data-stu-id="4d04b-462">Sampler Stage States</span></span>

<span data-ttu-id="4d04b-463">Состояния этапов образца используются для выборки текстур.</span><span class="sxs-lookup"><span data-stu-id="4d04b-463">Sampler stage states are used to sample textures.</span></span> <span data-ttu-id="4d04b-464">Состояние образца определяет типы фильтрации и режимы адресации текстур.</span><span class="sxs-lookup"><span data-stu-id="4d04b-464">Sampler state determines filtering types and texture addressing modes.</span></span>



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d04b-465">Состояние образца</span><span class="sxs-lookup"><span data-stu-id="4d04b-465">Sampler State</span></span>       | <span data-ttu-id="4d04b-466">Тип</span><span class="sxs-lookup"><span data-stu-id="4d04b-466">Type</span></span>                         | <span data-ttu-id="4d04b-467">Значения</span><span class="sxs-lookup"><span data-stu-id="4d04b-467">Values</span></span>                                                                                                                            |
| <span data-ttu-id="4d04b-468">Аддрессу \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-468">AddressU\[16\]</span></span>      | <span data-ttu-id="4d04b-469">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-469">dword</span></span>                        | <span data-ttu-id="4d04b-470">Те же значения, что и [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) без \_ префикса D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-470">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="4d04b-471">См. раздел D3DSAMP \_ аддрессу.</span><span class="sxs-lookup"><span data-stu-id="4d04b-471">See D3DSAMP\_ADDRESSU.</span></span>      |
| <span data-ttu-id="4d04b-472">Аддрессв \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-472">AddressV\[16\]</span></span>      | <span data-ttu-id="4d04b-473">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-473">dword</span></span>                        | <span data-ttu-id="4d04b-474">Те же значения, что и [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) без \_ префикса D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-474">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="4d04b-475">См. раздел D3DSAMP \_ аддрессв.</span><span class="sxs-lookup"><span data-stu-id="4d04b-475">See D3DSAMP\_ADDRESSV.</span></span>      |
| <span data-ttu-id="4d04b-476">Аддрессв \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-476">AddressW\[16\]</span></span>      | <span data-ttu-id="4d04b-477">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-477">dword</span></span>                        | <span data-ttu-id="4d04b-478">Те же значения, что и [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) без \_ префикса D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-478">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="4d04b-479">См. раздел D3DSAMP \_ аддрессв.</span><span class="sxs-lookup"><span data-stu-id="4d04b-479">See D3DSAMP\_ADDRESSW.</span></span>      |
| <span data-ttu-id="4d04b-480">BorderColor \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-480">BorderColor\[16\]</span></span>   | [<span data-ttu-id="4d04b-481">**D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="4d04b-481">**D3DCOLOR**</span></span>](d3dcolor.md) | <span data-ttu-id="4d04b-482">Те же значения, что и [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) без \_ префикса D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="4d04b-482">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="4d04b-483">См. раздел D3DSAMP \_ BORDERCOLOR.</span><span class="sxs-lookup"><span data-stu-id="4d04b-483">See D3DSAMP\_BORDERCOLOR.</span></span> |
| <span data-ttu-id="4d04b-484">Магфилтер \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-484">MagFilter\[16\]</span></span>     | <span data-ttu-id="4d04b-485">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-485">dword</span></span>                        | <span data-ttu-id="4d04b-486">Те же значения, что и [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) без \_ префикса D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="4d04b-486">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="4d04b-487">См. раздел D3DSAMP \_ магфилтер.</span><span class="sxs-lookup"><span data-stu-id="4d04b-487">See D3DSAMP\_MAGFILTER.</span></span>   |
| <span data-ttu-id="4d04b-488">Максанисотропи \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-488">MaxAnisotropy\[16\]</span></span> | <span data-ttu-id="4d04b-489">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-489">dword</span></span>                        | <span data-ttu-id="4d04b-490">Те же значения, что и \_ в D3DSAMP максанисотропи без \_ префикса D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="4d04b-490">Same values as D3DSAMP\_MAXANISOTROPY without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="4d04b-491">Максмиплевел \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-491">MaxMipLevel\[16\]</span></span>   | <span data-ttu-id="4d04b-492">INT</span><span class="sxs-lookup"><span data-stu-id="4d04b-492">int</span></span>                          | <span data-ttu-id="4d04b-493">Те же значения, что и \_ в D3DSAMP максмиплевел без \_ префикса D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="4d04b-493">Same values as D3DSAMP\_MAXMIPLEVEL without the D3DSAMP\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="4d04b-494">Минфилтер \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-494">MinFilter\[16\]</span></span>     | <span data-ttu-id="4d04b-495">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-495">dword</span></span>                        | <span data-ttu-id="4d04b-496">Те же значения, что и \_ в D3DSAMP минфилтер без \_ префикса D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="4d04b-496">Same values as D3DSAMP\_MINFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="4d04b-497">Мипфилтер \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-497">MipFilter\[16\]</span></span>     | <span data-ttu-id="4d04b-498">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-498">dword</span></span>                        | <span data-ttu-id="4d04b-499">Те же значения, что и \_ в D3DSAMP мипфилтер без \_ префикса D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="4d04b-499">Same values as D3DSAMP\_MIPFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="4d04b-500">Мипмаплодбиас \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-500">MipMapLodBias\[16\]</span></span> | <span data-ttu-id="4d04b-501">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-501">float</span></span>                        | <span data-ttu-id="4d04b-502">Те же значения, что и \_ в D3DSAMP мипмаплодбиас без \_ префикса D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="4d04b-502">Same values as D3DSAMP\_MIPMAPLODBIAS without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="4d04b-503">сргбтекстуре</span><span class="sxs-lookup"><span data-stu-id="4d04b-503">SRGBTexture</span></span>         | <span data-ttu-id="4d04b-504">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-504">float</span></span>                        | <span data-ttu-id="4d04b-505">То же значение, что и D3DSAMP \_ сргбтекстуре без \_ префикса D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="4d04b-505">Same value as D3DSAMP\_SRGBTEXTURE without the D3DSAMP\_ prefix.</span></span>                                                                  |



 

<span data-ttu-id="4d04b-506">Пример.</span><span class="sxs-lookup"><span data-stu-id="4d04b-506">Example:</span></span>


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



<span data-ttu-id="4d04b-507">Этот зажим УВВ значения в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="4d04b-507">This clamps UVW values to be in between 0 and 1.</span></span>

## <a name="shader-states"></a><span data-ttu-id="4d04b-508">Состояния шейдера</span><span class="sxs-lookup"><span data-stu-id="4d04b-508">Shader States</span></span>

<span data-ttu-id="4d04b-509">Существует только два состояния шейдера: одно связано с объектом шейдера вершин и другим, связанным с объектом шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="4d04b-509">There are only two effect shader states: one associated with a vertex shader object and the other associated with a pixel shader object.</span></span>



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="4d04b-510">Состояние шейдера</span><span class="sxs-lookup"><span data-stu-id="4d04b-510">Shader State</span></span> | <span data-ttu-id="4d04b-511">Тип</span><span class="sxs-lookup"><span data-stu-id="4d04b-511">Type</span></span>         | <span data-ttu-id="4d04b-512">Значения</span><span class="sxs-lookup"><span data-stu-id="4d04b-512">Values</span></span>                                                                      |
| <span data-ttu-id="4d04b-513">PixelShader</span><span class="sxs-lookup"><span data-stu-id="4d04b-513">PixelShader</span></span>  | <span data-ttu-id="4d04b-514">PixelShader</span><span class="sxs-lookup"><span data-stu-id="4d04b-514">pixelshader</span></span>  | <span data-ttu-id="4d04b-515">**Null**, блок сборки, Цель компиляции или параметр шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="4d04b-515">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |
| <span data-ttu-id="4d04b-516">вертексшадер</span><span class="sxs-lookup"><span data-stu-id="4d04b-516">VertexShader</span></span> | <span data-ttu-id="4d04b-517">вертексшадер</span><span class="sxs-lookup"><span data-stu-id="4d04b-517">vertexshader</span></span> | <span data-ttu-id="4d04b-518">**Null**, блок сборки, Цель компиляции или параметр шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="4d04b-518">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |



 

<span data-ttu-id="4d04b-519">Пример.</span><span class="sxs-lookup"><span data-stu-id="4d04b-519">Example:</span></span>


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



<span data-ttu-id="4d04b-520">Это приведет к компиляции Встекстуре, шейдера вершин, определенного ранее в файле FX, в шейдер вершин версии 1,1, а затем задает этот Скомпилированный шейдер в качестве шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="4d04b-520">This will compile VSTexture, a vertex shader defined earlier in the .fx file, to the vertex shader version 1.1, and then set that compiled shader as the vertex shader.</span></span> <span data-ttu-id="4d04b-521">Шейдер пикселей присваивается **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="4d04b-521">The pixel shader is assigned to **NULL**.</span></span>

## <a name="shader-constant-states"></a><span data-ttu-id="4d04b-522">Состояния констант шейдера</span><span class="sxs-lookup"><span data-stu-id="4d04b-522">Shader Constant States</span></span>

<span data-ttu-id="4d04b-523">Состояния констант шейдера используются для доступа к параметрам констант шейдера.</span><span class="sxs-lookup"><span data-stu-id="4d04b-523">Shader constant states are used to access shader constant parameters.</span></span>



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| <span data-ttu-id="4d04b-524">Состояние констант шейдера</span><span class="sxs-lookup"><span data-stu-id="4d04b-524">Shader Constant State</span></span> | <span data-ttu-id="4d04b-525">Тип</span><span class="sxs-lookup"><span data-stu-id="4d04b-525">Type</span></span>            | <span data-ttu-id="4d04b-526">Значения</span><span class="sxs-lookup"><span data-stu-id="4d04b-526">Values</span></span>                                       |
| <span data-ttu-id="4d04b-527">пикселшадерконстант</span><span class="sxs-lookup"><span data-stu-id="4d04b-527">PixelShaderConstant</span></span>   | <span data-ttu-id="4d04b-528">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-528">float\[m\[n\]\]</span></span> | <span data-ttu-id="4d04b-529">m x n массивов с плавающей запятой; m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="4d04b-529">m x n array of floats; m and n are optional.</span></span> |
| <span data-ttu-id="4d04b-530">PixelShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="4d04b-530">PixelShaderConstant1</span></span>  | <span data-ttu-id="4d04b-531">float4</span><span class="sxs-lookup"><span data-stu-id="4d04b-531">float4</span></span>          | <span data-ttu-id="4d04b-532">Один 4D с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4d04b-532">One 4D float.</span></span>                                |
| <span data-ttu-id="4d04b-533">PixelShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="4d04b-533">PixelShaderConstant2</span></span>  | <span data-ttu-id="4d04b-534">float4x2</span><span class="sxs-lookup"><span data-stu-id="4d04b-534">float4x2</span></span>        | <span data-ttu-id="4d04b-535">Два типа с плавающей точкой 4D.</span><span class="sxs-lookup"><span data-stu-id="4d04b-535">Two 4D floats.</span></span>                               |
| <span data-ttu-id="4d04b-536">PixelShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="4d04b-536">PixelShaderConstant3</span></span>  | <span data-ttu-id="4d04b-537">float4x3</span><span class="sxs-lookup"><span data-stu-id="4d04b-537">float4x3</span></span>        | <span data-ttu-id="4d04b-538">Три типа 4D с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4d04b-538">Three 4D floats.</span></span>                             |
| <span data-ttu-id="4d04b-539">PixelShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="4d04b-539">PixelShaderConstant4</span></span>  | <span data-ttu-id="4d04b-540">float4x4</span><span class="sxs-lookup"><span data-stu-id="4d04b-540">float4x4</span></span>        | <span data-ttu-id="4d04b-541">Четыре типа с плавающей точкой 4D.</span><span class="sxs-lookup"><span data-stu-id="4d04b-541">Four 4D floats.</span></span>                              |
| <span data-ttu-id="4d04b-542">пикселшадерконстантб</span><span class="sxs-lookup"><span data-stu-id="4d04b-542">PixelShaderConstantB</span></span>  | <span data-ttu-id="4d04b-543">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-543">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="4d04b-544">m x n массивов bools; m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="4d04b-544">m x n array of bools; m and n are optional.</span></span>  |
| <span data-ttu-id="4d04b-545">пикселшадерконстанти</span><span class="sxs-lookup"><span data-stu-id="4d04b-545">PixelShaderConstantI</span></span>  | <span data-ttu-id="4d04b-546">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-546">int\[m\[n\]\]</span></span>   | <span data-ttu-id="4d04b-547">m x n массива ints.</span><span class="sxs-lookup"><span data-stu-id="4d04b-547">m x n array of ints.</span></span> <span data-ttu-id="4d04b-548">m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="4d04b-548">m and n are optional.</span></span>   |
| <span data-ttu-id="4d04b-549">пикселшадерконстантф</span><span class="sxs-lookup"><span data-stu-id="4d04b-549">PixelShaderConstantF</span></span>  | <span data-ttu-id="4d04b-550">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-550">float\[m\[n\]\]</span></span> | <span data-ttu-id="4d04b-551">m x n массивов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4d04b-551">m x n array of floats.</span></span> <span data-ttu-id="4d04b-552">m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="4d04b-552">m and n are optional.</span></span> |
| <span data-ttu-id="4d04b-553">вертексшадерконстант</span><span class="sxs-lookup"><span data-stu-id="4d04b-553">VertexShaderConstant</span></span>  | <span data-ttu-id="4d04b-554">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-554">float\[m\[n\]\]</span></span> | <span data-ttu-id="4d04b-555">m x n массивов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4d04b-555">m x n array of floats.</span></span> <span data-ttu-id="4d04b-556">m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="4d04b-556">m and n are optional.</span></span> |
| <span data-ttu-id="4d04b-557">VertexShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="4d04b-557">VertexShaderConstant1</span></span> | <span data-ttu-id="4d04b-558">float4</span><span class="sxs-lookup"><span data-stu-id="4d04b-558">float4</span></span>          | <span data-ttu-id="4d04b-559">Один 4D с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4d04b-559">One 4D float.</span></span>                                |
| <span data-ttu-id="4d04b-560">VertexShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="4d04b-560">VertexShaderConstant2</span></span> | <span data-ttu-id="4d04b-561">float4x2</span><span class="sxs-lookup"><span data-stu-id="4d04b-561">float4x2</span></span>        | <span data-ttu-id="4d04b-562">Два типа с плавающей точкой 4D.</span><span class="sxs-lookup"><span data-stu-id="4d04b-562">Two 4D floats.</span></span>                               |
| <span data-ttu-id="4d04b-563">VertexShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="4d04b-563">VertexShaderConstant3</span></span> | <span data-ttu-id="4d04b-564">float4x3</span><span class="sxs-lookup"><span data-stu-id="4d04b-564">float4x3</span></span>        | <span data-ttu-id="4d04b-565">Три типа 4D с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4d04b-565">Three 4D floats.</span></span>                             |
| <span data-ttu-id="4d04b-566">VertexShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="4d04b-566">VertexShaderConstant4</span></span> | <span data-ttu-id="4d04b-567">float4x4</span><span class="sxs-lookup"><span data-stu-id="4d04b-567">float4x4</span></span>        | <span data-ttu-id="4d04b-568">Четыре типа с плавающей точкой 4D.</span><span class="sxs-lookup"><span data-stu-id="4d04b-568">Four 4D floats.</span></span>                              |
| <span data-ttu-id="4d04b-569">вертексшадерконстантб</span><span class="sxs-lookup"><span data-stu-id="4d04b-569">VertexShaderConstantB</span></span> | <span data-ttu-id="4d04b-570">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-570">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="4d04b-571">массив логических координат m x n.</span><span class="sxs-lookup"><span data-stu-id="4d04b-571">m x n array of bools.</span></span> <span data-ttu-id="4d04b-572">m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="4d04b-572">m and n are optional.</span></span>  |
| <span data-ttu-id="4d04b-573">вертексшадерконстанти</span><span class="sxs-lookup"><span data-stu-id="4d04b-573">VertexShaderConstantI</span></span> | <span data-ttu-id="4d04b-574">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-574">int\[m\[n\]\]</span></span>   | <span data-ttu-id="4d04b-575">m x n массива ints.</span><span class="sxs-lookup"><span data-stu-id="4d04b-575">m x n array of ints.</span></span> <span data-ttu-id="4d04b-576">m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="4d04b-576">m and n are optional.</span></span>   |
| <span data-ttu-id="4d04b-577">вертексшадерконстантф</span><span class="sxs-lookup"><span data-stu-id="4d04b-577">VertexShaderConstantF</span></span> | <span data-ttu-id="4d04b-578">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-578">float\[m\[n\]\]</span></span> | <span data-ttu-id="4d04b-579">m x n массивов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4d04b-579">m x n array of floats.</span></span> <span data-ttu-id="4d04b-580">m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="4d04b-580">m and n are optional.</span></span> |



 

## <a name="texture-states"></a><span data-ttu-id="4d04b-581">Состояния текстуры</span><span class="sxs-lookup"><span data-stu-id="4d04b-581">Texture States</span></span>

<span data-ttu-id="4d04b-582">Состояние текстуры инициализирует текстуры, используемые многотекстурным смешением.</span><span class="sxs-lookup"><span data-stu-id="4d04b-582">Texture states initialize textures used by the multitexture blender.</span></span>



|               |         |                                   |
|---------------|---------|-----------------------------------|
| <span data-ttu-id="4d04b-583">Состояние текстуры</span><span class="sxs-lookup"><span data-stu-id="4d04b-583">Texture State</span></span> | <span data-ttu-id="4d04b-584">Тип</span><span class="sxs-lookup"><span data-stu-id="4d04b-584">Type</span></span>    | <span data-ttu-id="4d04b-585">Значения</span><span class="sxs-lookup"><span data-stu-id="4d04b-585">Values</span></span>                            |
| <span data-ttu-id="4d04b-586">Текстура \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-586">Texture\[8\]</span></span>  | <span data-ttu-id="4d04b-587">текстура</span><span class="sxs-lookup"><span data-stu-id="4d04b-587">texture</span></span> | <span data-ttu-id="4d04b-588">**Null** или параметр текстуры.</span><span class="sxs-lookup"><span data-stu-id="4d04b-588">**NULL**, or a texture parameter.</span></span> |



 

## <a name="texture-stage-states"></a><span data-ttu-id="4d04b-589">Состояния стадии текстуры</span><span class="sxs-lookup"><span data-stu-id="4d04b-589">Texture Stage States</span></span>

<span data-ttu-id="4d04b-590">Состояния стадии текстуры настраиваются текстуры и этапы текстуры в многотекстурном смешении.</span><span class="sxs-lookup"><span data-stu-id="4d04b-590">Texture stage states set up textures and the texture stages in the multitexture blender.</span></span>



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d04b-591">Состояние этапа текстуры</span><span class="sxs-lookup"><span data-stu-id="4d04b-591">Texture Stage State</span></span>        | <span data-ttu-id="4d04b-592">Тип</span><span class="sxs-lookup"><span data-stu-id="4d04b-592">Type</span></span>  | <span data-ttu-id="4d04b-593">Значения</span><span class="sxs-lookup"><span data-stu-id="4d04b-593">Values</span></span>                                                                                                                                                    |
| <span data-ttu-id="4d04b-594">Алфаоп \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-594">AlphaOp\[8\]</span></span>               | <span data-ttu-id="4d04b-595">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-595">dword</span></span> | <span data-ttu-id="4d04b-596">То же, что и [**D3DTEXTUREOP**](./d3dtextureop.md) без \_ префикса D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="4d04b-596">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="4d04b-597">См. раздел D3DTSS \_ алфаоп.</span><span class="sxs-lookup"><span data-stu-id="4d04b-597">See D3DTSS\_ALPHAOP.</span></span>                                                      |
| <span data-ttu-id="4d04b-598">AlphaArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-598">AlphaArg0\[8\]</span></span>             | <span data-ttu-id="4d04b-599">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-599">dword</span></span> | <span data-ttu-id="4d04b-600">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="4d04b-600">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="4d04b-601">См. раздел D3DTSS \_ ALPHAARG0.</span><span class="sxs-lookup"><span data-stu-id="4d04b-601">See D3DTSS\_ALPHAARG0.</span></span>                                                                             |
| <span data-ttu-id="4d04b-602">AlphaArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-602">AlphaArg1\[8\]</span></span>             | <span data-ttu-id="4d04b-603">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-603">dword</span></span> | <span data-ttu-id="4d04b-604">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="4d04b-604">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="4d04b-605">См. раздел D3DTSS \_ ALPHAARG1.</span><span class="sxs-lookup"><span data-stu-id="4d04b-605">See D3DTSS\_ALPHAARG1.</span></span>                                                                             |
| <span data-ttu-id="4d04b-606">AlphaArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-606">AlphaArg2\[8\]</span></span>             | <span data-ttu-id="4d04b-607">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-607">dword</span></span> | <span data-ttu-id="4d04b-608">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="4d04b-608">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="4d04b-609">См. раздел D3DTSS \_ ALPHAARG2.</span><span class="sxs-lookup"><span data-stu-id="4d04b-609">See D3DTSS\_ALPHAARG2.</span></span>                                                                             |
| <span data-ttu-id="4d04b-610">ColorArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-610">ColorArg0\[8\]</span></span>             | <span data-ttu-id="4d04b-611">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-611">dword</span></span> | <span data-ttu-id="4d04b-612">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="4d04b-612">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="4d04b-613">См. раздел D3DTSS \_ COLORARG0.</span><span class="sxs-lookup"><span data-stu-id="4d04b-613">See D3DTSS\_COLORARG0.</span></span>                                                                             |
| <span data-ttu-id="4d04b-614">ColorArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-614">ColorArg1\[8\]</span></span>             | <span data-ttu-id="4d04b-615">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-615">dword</span></span> | <span data-ttu-id="4d04b-616">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="4d04b-616">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="4d04b-617">См. раздел D3DTSS \_ COLORARG1.</span><span class="sxs-lookup"><span data-stu-id="4d04b-617">See D3DTSS\_COLORARG1.</span></span>                                                                             |
| <span data-ttu-id="4d04b-618">ColorArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-618">ColorArg2\[8\]</span></span>             | <span data-ttu-id="4d04b-619">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-619">dword</span></span> | <span data-ttu-id="4d04b-620">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="4d04b-620">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="4d04b-621">См. раздел D3DTSS \_ COLORARG2.</span><span class="sxs-lookup"><span data-stu-id="4d04b-621">See D3DTSS\_COLORARG2.</span></span>                                                                             |
| <span data-ttu-id="4d04b-622">Колороп \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-622">ColorOp\[8\]</span></span>               | <span data-ttu-id="4d04b-623">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-623">dword</span></span> | <span data-ttu-id="4d04b-624">То же, что и [**D3DTEXTUREOP**](./d3dtextureop.md) без \_ префикса D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="4d04b-624">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="4d04b-625">См. раздел D3DTSS \_ колороп.</span><span class="sxs-lookup"><span data-stu-id="4d04b-625">See D3DTSS\_COLOROP.</span></span>                                                      |
| <span data-ttu-id="4d04b-626">Бумпенвлскале \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-626">BumpEnvLScale\[8\]</span></span>         | <span data-ttu-id="4d04b-627">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-627">float</span></span> | <span data-ttu-id="4d04b-628">Те же значения, что и D3DTSS \_ бумпенвлскале без \_ префикса D3DTSS тЦи.</span><span class="sxs-lookup"><span data-stu-id="4d04b-628">Same values as D3DTSS\_BUMPENVLSCALE without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="4d04b-629">Бумпенвлоффсет \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-629">BumpEnvLOffset\[8\]</span></span>        | <span data-ttu-id="4d04b-630">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-630">float</span></span> | <span data-ttu-id="4d04b-631">Те же значения, что и D3DTSS \_ бумпенвлоффсет без \_ префикса D3DTSS тЦи.</span><span class="sxs-lookup"><span data-stu-id="4d04b-631">Same values as D3DTSS\_BUMPENVLOFFSET without the D3DTSS\_TCI prefix.</span></span>                                                                                     |
| <span data-ttu-id="4d04b-632">BumpEnvMat00 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-632">BumpEnvMat00\[8\]</span></span>          | <span data-ttu-id="4d04b-633">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-633">float</span></span> | <span data-ttu-id="4d04b-634">Те же значения, что и в D3DTSS \_ BUMPENVMAT00.</span><span class="sxs-lookup"><span data-stu-id="4d04b-634">Same values as D3DTSS\_BUMPENVMAT00.</span></span>                                                                                                                      |
| <span data-ttu-id="4d04b-635">BumpEnvMat01 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-635">BumpEnvMat01\[8\]</span></span>          | <span data-ttu-id="4d04b-636">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-636">float</span></span> | <span data-ttu-id="4d04b-637">Те же значения, что и в D3DTSS \_ BUMPENVMAT01.</span><span class="sxs-lookup"><span data-stu-id="4d04b-637">Same values as D3DTSS\_BUMPENVMAT01.</span></span>                                                                                                                      |
| <span data-ttu-id="4d04b-638">BumpEnvMat10 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-638">BumpEnvMat10\[8\]</span></span>          | <span data-ttu-id="4d04b-639">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-639">float</span></span> | <span data-ttu-id="4d04b-640">Те же значения, что и в D3DTSS \_ BUMPENVMAT10.</span><span class="sxs-lookup"><span data-stu-id="4d04b-640">Same values as D3DTSS\_BUMPENVMAT10.</span></span>                                                                                                                      |
| <span data-ttu-id="4d04b-641">BumpEnvMat11 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-641">BumpEnvMat11\[8\]</span></span>          | <span data-ttu-id="4d04b-642">FLOAT</span><span class="sxs-lookup"><span data-stu-id="4d04b-642">float</span></span> | <span data-ttu-id="4d04b-643">Те же значения, что и в D3DTSS \_ BUMPENVMAT11.</span><span class="sxs-lookup"><span data-stu-id="4d04b-643">Same values as D3DTSS\_BUMPENVMAT11.</span></span>                                                                                                                      |
| <span data-ttu-id="4d04b-644">Ресултарг \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-644">ResultArg\[8\]</span></span>             | <span data-ttu-id="4d04b-645">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-645">dword</span></span> | <span data-ttu-id="4d04b-646">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="4d04b-646">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="4d04b-647">См. раздел D3DTSS \_ ресултарг.</span><span class="sxs-lookup"><span data-stu-id="4d04b-647">See D3DTSS\_RESULTARG.</span></span>                                                                             |
| <span data-ttu-id="4d04b-648">Текскурдиндекс \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-648">TexCoordIndex\[8\]</span></span>         | <span data-ttu-id="4d04b-649">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-649">dword</span></span> | <span data-ttu-id="4d04b-650">Те же значения, что и D3DTSS \_ текскурдиндекс без \_ префикса D3DTSS тЦи.</span><span class="sxs-lookup"><span data-stu-id="4d04b-650">Same values as D3DTSS\_TEXCOORDINDEX without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="4d04b-651">Текстуретрансформфлагс \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-651">TextureTransformFlags\[8\]</span></span> | <span data-ttu-id="4d04b-652">dword</span><span class="sxs-lookup"><span data-stu-id="4d04b-652">dword</span></span> | <span data-ttu-id="4d04b-653">Те же значения, что и значения [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) без \_ префикса D3DTTFF.</span><span class="sxs-lookup"><span data-stu-id="4d04b-653">Same values as [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) values without the D3DTTFF\_ prefix.</span></span> <span data-ttu-id="4d04b-654">См. раздел D3DTSS \_ текстуретрансформфлагс.</span><span class="sxs-lookup"><span data-stu-id="4d04b-654">See D3DTSS\_TEXTURETRANSFORMFLAGS.</span></span> |



 

## <a name="transform-states"></a><span data-ttu-id="4d04b-655">Состояния преобразования</span><span class="sxs-lookup"><span data-stu-id="4d04b-655">Transform States</span></span>

<span data-ttu-id="4d04b-656">Задайте состояния преобразования, чтобы инициализировать матрицы преобразования.</span><span class="sxs-lookup"><span data-stu-id="4d04b-656">Set transform states to initialize transformation matrices.</span></span> <span data-ttu-id="4d04b-657">Эффекты используют перелагаемые матрицы для повышения эффективности.</span><span class="sxs-lookup"><span data-stu-id="4d04b-657">Effects use transposed matrices for efficiency.</span></span> <span data-ttu-id="4d04b-658">Можно указать, что в результате передаются матрицы, или результат автоматически перестанет представлять собой матрицы перед их использованием.</span><span class="sxs-lookup"><span data-stu-id="4d04b-658">You can provide transposed matrices to an effect, or an effect will automatically transpose the matrices before using them.</span></span>



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4d04b-659">Состояние преобразования</span><span class="sxs-lookup"><span data-stu-id="4d04b-659">Transform State</span></span>       | <span data-ttu-id="4d04b-660">Тип</span><span class="sxs-lookup"><span data-stu-id="4d04b-660">Type</span></span>     | <span data-ttu-id="4d04b-661">Значения</span><span class="sxs-lookup"><span data-stu-id="4d04b-661">Values</span></span>                                                                                                                          |
| <span data-ttu-id="4d04b-662">прожектионтрансформ</span><span class="sxs-lookup"><span data-stu-id="4d04b-662">ProjectionTransform</span></span>   | <span data-ttu-id="4d04b-663">float4x4</span><span class="sxs-lookup"><span data-stu-id="4d04b-663">float4x4</span></span> | <span data-ttu-id="4d04b-664">Матрица 4x4 с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4d04b-664">A 4x4 matrix of floats.</span></span> <span data-ttu-id="4d04b-665">Те же значения, что и \_ у D3DTS проекции без \_ префикса D3DTS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-665">Same values as D3DTS\_PROJECTION without the D3DTS\_ prefix.</span></span>                                            |
| <span data-ttu-id="4d04b-666">Текстуретрансформ \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="4d04b-666">TextureTransform\[8\]</span></span> | <span data-ttu-id="4d04b-667">float4x4</span><span class="sxs-lookup"><span data-stu-id="4d04b-667">float4x4</span></span> | <span data-ttu-id="4d04b-668">Матрица 4x4 с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4d04b-668">A 4x4 matrix of floats.</span></span> <span data-ttu-id="4d04b-669">Те же значения, что и [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) без \_ префикса D3DTS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-669">Same values as [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) without the D3DTS\_ prefix.</span></span> |
| <span data-ttu-id="4d04b-670">виевтрансформ</span><span class="sxs-lookup"><span data-stu-id="4d04b-670">ViewTransform</span></span>         | <span data-ttu-id="4d04b-671">float4x4</span><span class="sxs-lookup"><span data-stu-id="4d04b-671">float4x4</span></span> | <span data-ttu-id="4d04b-672">Матрица 4x4 с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4d04b-672">A 4x4 matrix of floats.</span></span> <span data-ttu-id="4d04b-673">Те же значения, что и \_ в представлении D3DTS без \_ префикса D3DTS.</span><span class="sxs-lookup"><span data-stu-id="4d04b-673">Same values as D3DTS\_VIEW without the D3DTS\_ prefix.</span></span>                                                  |
| <span data-ttu-id="4d04b-674">ворлдтрансформ</span><span class="sxs-lookup"><span data-stu-id="4d04b-674">WorldTransform</span></span>        | <span data-ttu-id="4d04b-675">float4x4</span><span class="sxs-lookup"><span data-stu-id="4d04b-675">float4x4</span></span> | <span data-ttu-id="4d04b-676">Матрица 4x4 с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="4d04b-676">A 4x4 matrix of floats.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="4d04b-677">См. также</span><span class="sxs-lookup"><span data-stu-id="4d04b-677">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4d04b-678">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="4d04b-678">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
