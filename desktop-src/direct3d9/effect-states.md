---
description: Состояния эффектов используются для инициализации состояний конвейера при подготовке к обработке вершин и пикселей.
ms.assetid: b62a6ccc-a1ea-455c-9659-544d4bcaf6a2
title: Состояния эффектов (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e208c0c7c14564a9967562ff2fd04a400cb7901
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314767"
---
# <a name="effect-states-direct3d-9"></a><span data-ttu-id="779a2-103">Состояния эффектов (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="779a2-103">Effect States (Direct3D 9)</span></span>

<span data-ttu-id="779a2-104">Состояния эффектов используются для инициализации состояний конвейера при подготовке к обработке вершин и пикселей.</span><span class="sxs-lookup"><span data-stu-id="779a2-104">Effect states are used to initialize pipeline states in preparation for vertex and pixel processing.</span></span>


```
effect state [ [index] ] = expression;
```



<span data-ttu-id="779a2-105">Где:</span><span class="sxs-lookup"><span data-stu-id="779a2-105">Where:</span></span>

-   <span data-ttu-id="779a2-106">состояние результата — аналогично традиционному состоянию конвейера фиксированной функции.</span><span class="sxs-lookup"><span data-stu-id="779a2-106">effect state - Similar to the traditional fixed function pipeline states.</span></span> <span data-ttu-id="779a2-107">Ниже приведен полный список состояний.</span><span class="sxs-lookup"><span data-stu-id="779a2-107">A complete list of states is provided below.</span></span>
-   <span data-ttu-id="779a2-108">\[\[ \] Индекс \] — Необязательный целочисленный индекс.</span><span class="sxs-lookup"><span data-stu-id="779a2-108">\[ \[index\] \] - Optional integer index.</span></span> <span data-ttu-id="779a2-109">Индекс определяет определенное состояние в массиве состояний эффектов.</span><span class="sxs-lookup"><span data-stu-id="779a2-109">The index identifies a particular state within an array of effect states.</span></span> <span data-ttu-id="779a2-110">Внешние скобки указывают, что индекс является необязательным.</span><span class="sxs-lookup"><span data-stu-id="779a2-110">The outer brackets indicate that an index is optional.</span></span> <span data-ttu-id="779a2-111">Если используется индекс, обязательно используйте внутренние скобки.</span><span class="sxs-lookup"><span data-stu-id="779a2-111">If an index is used, be sure to use the inner brackets.</span></span>
-   <span data-ttu-id="779a2-112">выражение назначения состояния выражения.</span><span class="sxs-lookup"><span data-stu-id="779a2-112">expression - State assignment expression.</span></span> <span data-ttu-id="779a2-113">См. раздел [выражения (Direct3D 9)](expressions.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-113">See [Expressions (Direct3D 9)](expressions.md).</span></span>

<span data-ttu-id="779a2-114">Каждое состояние имеет собственный тип данных.</span><span class="sxs-lookup"><span data-stu-id="779a2-114">Each state has a native data type.</span></span> <span data-ttu-id="779a2-115">Это тип данных, в котором состояние принимает значения в момент их назначения.</span><span class="sxs-lookup"><span data-stu-id="779a2-115">This is the data type that the state expects values to be in when the effect assigns them.</span></span> <span data-ttu-id="779a2-116">Ниже перечислены типы данных, которые требуются для каждого состояния.</span><span class="sxs-lookup"><span data-stu-id="779a2-116">The data types that each state expects are listed below.</span></span>

<span data-ttu-id="779a2-117">Обратите внимание, что интерфейс Effect будет пытаться привести значения к соответствующему типу как можно раньше.</span><span class="sxs-lookup"><span data-stu-id="779a2-117">Note that the effect interface will attempt to cast values to the appropriate type as early as possible.</span></span> <span data-ttu-id="779a2-118">Литеральные значения могут быть приведены во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="779a2-118">Literal values can be cast at compile time.</span></span> <span data-ttu-id="779a2-119">Не литералы (т. е. обычные переменные) должны быть приведены при вызове соответствующих методов набора.</span><span class="sxs-lookup"><span data-stu-id="779a2-119">Non-literals (i.e. regular variables) need to be cast when the appropriate Set methods are called.</span></span> <span data-ttu-id="779a2-120">Например, интерфейс Effect будет приводить значения, заданные с помощью [**сетбул**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md)и других аналогичных функций, если это необходимо.</span><span class="sxs-lookup"><span data-stu-id="779a2-120">For example, the effect interface will cast values set using [**SetBool**](id3dxbaseeffect--setbool.md), [**SetValue**](id3dxbaseeffect--setvalue.md), and other similar functions if necessary.</span></span> <span data-ttu-id="779a2-121">Для повышения производительности убедитесь, что значения, передаваемые в интерфейс Effect, уже имеют правильный тип и не требуют приведения.</span><span class="sxs-lookup"><span data-stu-id="779a2-121">For better performance ensure that the values passed to the effect interface are already the correct type and will not need casting.</span></span> <span data-ttu-id="779a2-122">Если среде выполнения не удается привести значение, возвращается ошибка.</span><span class="sxs-lookup"><span data-stu-id="779a2-122">If the runtime is unable to cast a value, an error is returned.</span></span>

<span data-ttu-id="779a2-123">Состояния эффектов можно разделить на следующие категории:</span><span class="sxs-lookup"><span data-stu-id="779a2-123">Effect states can be broken up into the following categories:</span></span>

-   [<span data-ttu-id="779a2-124">Состояния освещения</span><span class="sxs-lookup"><span data-stu-id="779a2-124">Light States</span></span>](#light-states)
-   [<span data-ttu-id="779a2-125">Состояния материалов</span><span class="sxs-lookup"><span data-stu-id="779a2-125">Material States</span></span>](#material-states)
-   [<span data-ttu-id="779a2-126">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="779a2-126">Render States</span></span>](#render-states)
    -   [<span data-ttu-id="779a2-127">Состояния рендеринга пиксельного канала</span><span class="sxs-lookup"><span data-stu-id="779a2-127">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
    -   [<span data-ttu-id="779a2-128">Состояния рендеринга канала вершин</span><span class="sxs-lookup"><span data-stu-id="779a2-128">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)
-   [<span data-ttu-id="779a2-129">Состояния образцов</span><span class="sxs-lookup"><span data-stu-id="779a2-129">Sampler States</span></span>](#sampler-states)
-   [<span data-ttu-id="779a2-130">Состояния стадий образца</span><span class="sxs-lookup"><span data-stu-id="779a2-130">Sampler Stage States</span></span>](#sampler-stage-states)
-   [<span data-ttu-id="779a2-131">Состояния шейдера</span><span class="sxs-lookup"><span data-stu-id="779a2-131">Shader States</span></span>](#shader-states)
-   [<span data-ttu-id="779a2-132">Состояния констант шейдера</span><span class="sxs-lookup"><span data-stu-id="779a2-132">Shader Constant States</span></span>](#shader-constant-states)
-   [<span data-ttu-id="779a2-133">Состояния текстуры</span><span class="sxs-lookup"><span data-stu-id="779a2-133">Texture States</span></span>](#texture-states)
-   [<span data-ttu-id="779a2-134">Состояния стадии текстуры</span><span class="sxs-lookup"><span data-stu-id="779a2-134">Texture Stage States</span></span>](#texture-stage-states)
-   [<span data-ttu-id="779a2-135">Состояния преобразования</span><span class="sxs-lookup"><span data-stu-id="779a2-135">Transform States</span></span>](#transform-states)

## <a name="light-states"></a><span data-ttu-id="779a2-136">Состояния освещения</span><span class="sxs-lookup"><span data-stu-id="779a2-136">Light States</span></span>

<span data-ttu-id="779a2-137">Чтобы обеспечить наилучшую производительность при применении эффектов, все компоненты источника «источник» или «материал» должны быть указаны в файле результатов.</span><span class="sxs-lookup"><span data-stu-id="779a2-137">To enable the best performance for applying an effect, all components of a light or a material should be specified in the effect file.</span></span> <span data-ttu-id="779a2-138">Для состояний, которые не удалось объявить, задается какое-либо значение по умолчанию, так как Direct3D не может устанавливать состояния освещения по отдельности.</span><span class="sxs-lookup"><span data-stu-id="779a2-138">States that you fail to declare are set to some default value because there is no way for Direct3D to set light states individually.</span></span>



|                        |        |                                                                                                                     |
|------------------------|--------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="779a2-139">Светлое состояние</span><span class="sxs-lookup"><span data-stu-id="779a2-139">Light State</span></span>            | <span data-ttu-id="779a2-140">Тип</span><span class="sxs-lookup"><span data-stu-id="779a2-140">Type</span></span>   | <span data-ttu-id="779a2-141">Значения</span><span class="sxs-lookup"><span data-stu-id="779a2-141">Values</span></span>                                                                                                              |
| <span data-ttu-id="779a2-142">Лигхтамбиент \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-142">LightAmbient\[n\]</span></span>      | <span data-ttu-id="779a2-143">float4</span><span class="sxs-lookup"><span data-stu-id="779a2-143">float4</span></span> | <span data-ttu-id="779a2-144">См. элемент окружения [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-144">See the Ambient member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="779a2-145">LightAttenuation0 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-145">LightAttenuation0\[n\]</span></span> | <span data-ttu-id="779a2-146">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-146">float</span></span>  | <span data-ttu-id="779a2-147">См. элемент Attenuation0 элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-147">See the Attenuation0 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="779a2-148">LightAttenuation1 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-148">LightAttenuation1\[n\]</span></span> | <span data-ttu-id="779a2-149">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-149">float</span></span>  | <span data-ttu-id="779a2-150">См. элемент Attenuation1 элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-150">See the Attenuation1 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="779a2-151">LightAttenuation2 \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-151">LightAttenuation2\[n\]</span></span> | <span data-ttu-id="779a2-152">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-152">float</span></span>  | <span data-ttu-id="779a2-153">См. элемент Attenuation2 элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-153">See the Attenuation2 member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                      |
| <span data-ttu-id="779a2-154">Лигхтдиффусе \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-154">LightDiffuse\[n\]</span></span>      | <span data-ttu-id="779a2-155">float4</span><span class="sxs-lookup"><span data-stu-id="779a2-155">float4</span></span> | <span data-ttu-id="779a2-156">См. элемент диффузия [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-156">See the Diffuse member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                           |
| <span data-ttu-id="779a2-157">Лигхтдиректион \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-157">LightDirection\[n\]</span></span>    | <span data-ttu-id="779a2-158">float3</span><span class="sxs-lookup"><span data-stu-id="779a2-158">float3</span></span> | <span data-ttu-id="779a2-159">См. элемент Direction элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-159">See the Direction member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                         |
| <span data-ttu-id="779a2-160">Досветлить \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-160">LightEnable\[n\]</span></span>       | <span data-ttu-id="779a2-161">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-161">bool</span></span>   | <span data-ttu-id="779a2-162">**True** или **false**.</span><span class="sxs-lookup"><span data-stu-id="779a2-162">**TRUE** or **FALSE**.</span></span> <span data-ttu-id="779a2-163">См. аргумент Бенабле в качестве более [**светлого**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span><span class="sxs-lookup"><span data-stu-id="779a2-163">See the bEnable argument in [**LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable).</span></span>            |
| <span data-ttu-id="779a2-164">Лигхтфаллофф \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-164">LightFalloff\[n\]</span></span>      | <span data-ttu-id="779a2-165">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-165">float</span></span>  | <span data-ttu-id="779a2-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-166">[**D3DCOLORVALUE**](d3dcolorvalue.md).</span></span> <span data-ttu-id="779a2-167">См. элемент рассеивания [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-167">See the Falloff member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                   |
| <span data-ttu-id="779a2-168">Лигхтфи \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-168">LightPhi\[n\]</span></span>          | <span data-ttu-id="779a2-169">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-169">float</span></span>  | <span data-ttu-id="779a2-170">См. элемент фи элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-170">See the Phi member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                               |
| <span data-ttu-id="779a2-171">Лигхтпоситион \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-171">LightPosition\[n\]</span></span>     | <span data-ttu-id="779a2-172">float3</span><span class="sxs-lookup"><span data-stu-id="779a2-172">float3</span></span> | <span data-ttu-id="779a2-173">См. элемент расположения [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-173">See the Position member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="779a2-174">Лигхтранже \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-174">LightRange\[n\]</span></span>        | <span data-ttu-id="779a2-175">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-175">float</span></span>  | <span data-ttu-id="779a2-176">См. элемент Range элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-176">See the Range member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="779a2-177">Лигхтспекулар \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-177">LightSpecular\[n\]</span></span>     | <span data-ttu-id="779a2-178">float4</span><span class="sxs-lookup"><span data-stu-id="779a2-178">float4</span></span> | <span data-ttu-id="779a2-179">См. отраженный элемент [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-179">See the Specular member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                          |
| <span data-ttu-id="779a2-180">Лигхтсета \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-180">LightTheta\[n\]</span></span>        | <span data-ttu-id="779a2-181">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-181">float</span></span>  | <span data-ttu-id="779a2-182">См. элемент тета элемента [**D3DLIGHT9**](d3dlight9.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-182">See the Theta member of [**D3DLIGHT9**](d3dlight9.md).</span></span>                                                             |
| <span data-ttu-id="779a2-183">Лигхттипе \[ n\]</span><span class="sxs-lookup"><span data-stu-id="779a2-183">LightType\[n\]</span></span>         | <span data-ttu-id="779a2-184">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-184">dword</span></span>  | <span data-ttu-id="779a2-185">То же значение, что и для массива до n значений [**D3DLIGHTTYPE**](./d3dlighttype.md) без \_ префикса D3DLIGHT.</span><span class="sxs-lookup"><span data-stu-id="779a2-185">Same value as the array of up to n [**D3DLIGHTTYPE**](./d3dlighttype.md) values without the D3DLIGHT\_ prefix.</span></span> |



 

<span data-ttu-id="779a2-186">Пример:</span><span class="sxs-lookup"><span data-stu-id="779a2-186">Example:</span></span>


```
LightEnable[0] = TRUE;
LightType[0] = POINT;
LightPosition[0] = float3<10.0f, 1.0f, 23.0f>;
LightAmbient[0] = float4<0.7f, 0.0f, 0.0f, 1.0f>;
```



<span data-ttu-id="779a2-187">Это позволит включить освещение, сделать выбор для типа, установить для параметра "источник света" значение float3<10.0 f, 1.0 f, 23.0 f> и задать окружающий цвет float4<0,7 f, 0,0 f, 0,0 f, 1.0 f>.</span><span class="sxs-lookup"><span data-stu-id="779a2-187">This will enable lighting, make point lighting the type, set the light position to float3<10.0f, 1.0f, 23.0f>, and set the ambient color to float4<0.7f, 0.0f, 0.0f, 1.0f>.</span></span>

## <a name="material-states"></a><span data-ttu-id="779a2-188">Состояния материалов</span><span class="sxs-lookup"><span data-stu-id="779a2-188">Material States</span></span>

<span data-ttu-id="779a2-189">Для состояний, которые не удалось объявить, задается какое-либо значение по умолчанию, так как Direct3D не может устанавливать материальновые состояния по отдельности.</span><span class="sxs-lookup"><span data-stu-id="779a2-189">States that you fail to declare are set to some default value because there is no way for Direct3D to set material states individually.</span></span>



|                  |        |                                                |
|------------------|--------|------------------------------------------------|
| <span data-ttu-id="779a2-190">Состояние материала</span><span class="sxs-lookup"><span data-stu-id="779a2-190">Material State</span></span>   | <span data-ttu-id="779a2-191">Тип</span><span class="sxs-lookup"><span data-stu-id="779a2-191">Type</span></span>   | <span data-ttu-id="779a2-192">Значения</span><span class="sxs-lookup"><span data-stu-id="779a2-192">Values</span></span>                                         |
| <span data-ttu-id="779a2-193">Свойство materialambient</span><span class="sxs-lookup"><span data-stu-id="779a2-193">MaterialAmbient</span></span>  | <span data-ttu-id="779a2-194">float4</span><span class="sxs-lookup"><span data-stu-id="779a2-194">float4</span></span> | <span data-ttu-id="779a2-195">То же значение, что и во [ **внешнем**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="779a2-195">Same value as [**Ambient**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="779a2-196">MaterialDiffuse</span><span class="sxs-lookup"><span data-stu-id="779a2-196">MaterialDiffuse</span></span>  | <span data-ttu-id="779a2-197">float4</span><span class="sxs-lookup"><span data-stu-id="779a2-197">float4</span></span> | <span data-ttu-id="779a2-198">То же значение, что и [ **рассеянный**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="779a2-198">Same value as [**Diffuse**](d3dmaterial9.md)</span></span>  |
| <span data-ttu-id="779a2-199">MaterialEmissive</span><span class="sxs-lookup"><span data-stu-id="779a2-199">MaterialEmissive</span></span> | <span data-ttu-id="779a2-200">float4</span><span class="sxs-lookup"><span data-stu-id="779a2-200">float4</span></span> | <span data-ttu-id="779a2-201">То же значение, что и [ **эмиссионный**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="779a2-201">Same value as [**Emissive**](d3dmaterial9.md)</span></span> |
| <span data-ttu-id="779a2-202">материалповер</span><span class="sxs-lookup"><span data-stu-id="779a2-202">MaterialPower</span></span>    | <span data-ttu-id="779a2-203">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-203">float</span></span>  | <span data-ttu-id="779a2-204">То же значение, что и для [ **Power**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="779a2-204">Same value as [**Power**](d3dmaterial9.md)</span></span>    |
| <span data-ttu-id="779a2-205">MaterialSpecular</span><span class="sxs-lookup"><span data-stu-id="779a2-205">MaterialSpecular</span></span> | <span data-ttu-id="779a2-206">float4</span><span class="sxs-lookup"><span data-stu-id="779a2-206">float4</span></span> | <span data-ttu-id="779a2-207">То же значение, что и для [ **отражения**](d3dmaterial9.md)</span><span class="sxs-lookup"><span data-stu-id="779a2-207">Same value as [**Specular**](d3dmaterial9.md)</span></span> |



 

<span data-ttu-id="779a2-208">Пример:</span><span class="sxs-lookup"><span data-stu-id="779a2-208">Example:</span></span>


```
MaterialDiffuse = float4<0.7f, 0.0f, 0.0f, 1.0f>;
MaterialPower = 3.0f;
```



<span data-ttu-id="779a2-209">При этом для рассеянного цвета будет задано значение float4<0,7 f, 0,0 f, 0,0 f, 1.0 f> и сделать возможной мощь материала 3.0 f.</span><span class="sxs-lookup"><span data-stu-id="779a2-209">This will set the diffuse color to float4<0.7f, 0.0f, 0.0f, 1.0f> and make the power of the material 3.0f.</span></span>

## <a name="render-states"></a><span data-ttu-id="779a2-210">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="779a2-210">Render States</span></span>

<span data-ttu-id="779a2-211">Существует два типа состояний рендеринга:</span><span class="sxs-lookup"><span data-stu-id="779a2-211">There are two types of render states:</span></span>

-   [<span data-ttu-id="779a2-212">Состояния рендеринга пиксельного канала</span><span class="sxs-lookup"><span data-stu-id="779a2-212">Pixel Pipe Render States</span></span>](#pixel-pipe-render-states)
-   [<span data-ttu-id="779a2-213">Состояния рендеринга канала вершин</span><span class="sxs-lookup"><span data-stu-id="779a2-213">Vertex Pipe Render States</span></span>](#vertex-pipe-render-states)

### <a name="pixel-pipe-render-states"></a><span data-ttu-id="779a2-214">Состояния рендеринга пиксельного канала</span><span class="sxs-lookup"><span data-stu-id="779a2-214">Pixel Pipe Render States</span></span>

<span data-ttu-id="779a2-215">Состояния визуализации файла эффектов имеют имена, аналогичные состояниям конвейера фиксированной функции, часто с удаленным префиксом.</span><span class="sxs-lookup"><span data-stu-id="779a2-215">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="779a2-216">Состояние визуализации</span><span class="sxs-lookup"><span data-stu-id="779a2-216">Render State</span></span></td>
<td><span data-ttu-id="779a2-217">Тип</span><span class="sxs-lookup"><span data-stu-id="779a2-217">Type</span></span></td>
<td><span data-ttu-id="779a2-218">Значения</span><span class="sxs-lookup"><span data-stu-id="779a2-218">Values</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-219">алфабленденабле</span><span class="sxs-lookup"><span data-stu-id="779a2-219">AlphaBlendEnable</span></span></td>
<td><span data-ttu-id="779a2-220">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-220">bool</span></span></td>
<td><span data-ttu-id="779a2-221">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-221">True or False.</span></span> <span data-ttu-id="779a2-222">Те же значения, что и D3DRS_ALPHABLENDENABLE в <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="779a2-222">Same values as D3DRS_ALPHABLENDENABLE in <a href="/windows/desktop/direct3d9/d3drenderstatetype"><strong>D3DRENDERSTATETYPE</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-223">алфафунк</span><span class="sxs-lookup"><span data-stu-id="779a2-223">AlphaFunc</span></span></td>
<td><span data-ttu-id="779a2-224">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-224">dword</span></span></td>
<td><span data-ttu-id="779a2-225">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> без префикса D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="779a2-225">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="779a2-226">См. D3DRS_ALPHAFUNC.</span><span class="sxs-lookup"><span data-stu-id="779a2-226">See D3DRS_ALPHAFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-227">алфареф</span><span class="sxs-lookup"><span data-stu-id="779a2-227">AlphaRef</span></span></td>
<td><span data-ttu-id="779a2-228">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-228">dword</span></span></td>
<td><span data-ttu-id="779a2-229">Те же значения, что и D3DRS_ALPHAREF.</span><span class="sxs-lookup"><span data-stu-id="779a2-229">Same values as D3DRS_ALPHAREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-230">алфатестенабле</span><span class="sxs-lookup"><span data-stu-id="779a2-230">AlphaTestEnable</span></span></td>
<td><span data-ttu-id="779a2-231">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-231">dword</span></span></td>
<td><span data-ttu-id="779a2-232">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-232">True or False.</span></span> <span data-ttu-id="779a2-233">См. D3DRS_ALPHATESTENABLE.</span><span class="sxs-lookup"><span data-stu-id="779a2-233">See D3DRS_ALPHATESTENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-234">блендоп</span><span class="sxs-lookup"><span data-stu-id="779a2-234">BlendOp</span></span></td>
<td><span data-ttu-id="779a2-235">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-235">dword</span></span></td>
<td><span data-ttu-id="779a2-236">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> без префикса D3DBLENDOP_.</span><span class="sxs-lookup"><span data-stu-id="779a2-236">Same values as <a href="/windows/desktop/direct3d9/d3dblendop"><strong>D3DBLENDOP</strong></a> without the D3DBLENDOP_ prefix.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-237">колорвритинабле</span><span class="sxs-lookup"><span data-stu-id="779a2-237">ColorWriteEnable</span></span></td>
<td><span data-ttu-id="779a2-238">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-238">dword</span></span></td>
<td><span data-ttu-id="779a2-239">Побитовое сочетание красного цвета | ЗЕЛЕНЫЙ | СИНИЙ | Буквы.</span><span class="sxs-lookup"><span data-stu-id="779a2-239">Bitwise combination of RED|GREEN|BLUE|ALPHA.</span></span> <span data-ttu-id="779a2-240">См. D3DRS_COLORWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="779a2-240">See D3DRS_COLORWRITEENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-241">депсбиас</span><span class="sxs-lookup"><span data-stu-id="779a2-241">DepthBias</span></span></td>
<td><span data-ttu-id="779a2-242">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-242">float</span></span></td>
<td><span data-ttu-id="779a2-243">Те же значения, что и D3DRS_DEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="779a2-243">Same values as D3DRS_DEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-244">дестбленд</span><span class="sxs-lookup"><span data-stu-id="779a2-244">DestBlend</span></span></td>
<td><span data-ttu-id="779a2-245">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-245">dword</span></span></td>
<td><span data-ttu-id="779a2-246">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> без префикса D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="779a2-246">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-247">дисеренабле</span><span class="sxs-lookup"><span data-stu-id="779a2-247">DitherEnable</span></span></td>
<td><span data-ttu-id="779a2-248">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-248">bool</span></span></td>
<td><span data-ttu-id="779a2-249">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-249">True or False.</span></span> <span data-ttu-id="779a2-250">Те же значения, что и D3DRS_DITHERENABLE.</span><span class="sxs-lookup"><span data-stu-id="779a2-250">Same values as D3DRS_DITHERENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-251">филлмоде</span><span class="sxs-lookup"><span data-stu-id="779a2-251">FillMode</span></span></td>
<td><span data-ttu-id="779a2-252">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-252">dword</span></span></td>
<td><span data-ttu-id="779a2-253">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> без префикса D3DFILL_.</span><span class="sxs-lookup"><span data-stu-id="779a2-253">Same values as <a href="/windows/desktop/direct3d9/d3dfillmode"><strong>D3DFILLMODE</strong></a> without the D3DFILL_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-254">ластпиксел</span><span class="sxs-lookup"><span data-stu-id="779a2-254">LastPixel</span></span></td>
<td><span data-ttu-id="779a2-255">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-255">dword</span></span></td>
<td><span data-ttu-id="779a2-256">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-256">True or False.</span></span> <span data-ttu-id="779a2-257">См. D3DRS_LASTPIXEL.</span><span class="sxs-lookup"><span data-stu-id="779a2-257">See D3DRS_LASTPIXEL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-258">шадемоде</span><span class="sxs-lookup"><span data-stu-id="779a2-258">ShadeMode</span></span></td>
<td><span data-ttu-id="779a2-259">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-259">dword</span></span></td>
<td><span data-ttu-id="779a2-260">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> без префикса D3DSHADE_.</span><span class="sxs-lookup"><span data-stu-id="779a2-260">Same values as <a href="/windows/desktop/direct3d9/d3dshademode"><strong>D3DSHADEMODE</strong></a> without the D3DSHADE_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-261">слопескаледепсбиас</span><span class="sxs-lookup"><span data-stu-id="779a2-261">SlopeScaleDepthBias</span></span></td>
<td><span data-ttu-id="779a2-262">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-262">float</span></span></td>
<td><span data-ttu-id="779a2-263">Те же значения, что и D3DRS_SLOPESCALEDEPTHBIAS.</span><span class="sxs-lookup"><span data-stu-id="779a2-263">Same values as D3DRS_SLOPESCALEDEPTHBIAS.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-264">сркбленд</span><span class="sxs-lookup"><span data-stu-id="779a2-264">SrcBlend</span></span></td>
<td><span data-ttu-id="779a2-265">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-265">dword</span></span></td>
<td><span data-ttu-id="779a2-266">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> без префикса D3DBLEND_.</span><span class="sxs-lookup"><span data-stu-id="779a2-266">Same values as <a href="/windows/desktop/direct3d9/d3dblend"><strong>D3DBLEND</strong></a> without the D3DBLEND_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-267">сргбвритинабле</span><span class="sxs-lookup"><span data-stu-id="779a2-267">SRGBWriteEnable</span></span></td>
<td><span data-ttu-id="779a2-268">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-268">bool</span></span></td>
<td><span data-ttu-id="779a2-269">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-269">True or False.</span></span> <span data-ttu-id="779a2-270">Те же значения, что и D3DRS_SRGBWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="779a2-270">Same values as D3DRS_SRGBWRITEENABLE.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-271">стенЦиленабле</span><span class="sxs-lookup"><span data-stu-id="779a2-271">StencilEnable</span></span></td>
<td><span data-ttu-id="779a2-272">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-272">bool</span></span></td>
<td><span data-ttu-id="779a2-273">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-273">True or False.</span></span> <span data-ttu-id="779a2-274">Те же значения, что и D3DRS_STENCILENABLE.</span><span class="sxs-lookup"><span data-stu-id="779a2-274">Same values as D3DRS_STENCILENABLE.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-275">стенЦилфаил</span><span class="sxs-lookup"><span data-stu-id="779a2-275">StencilFail</span></span></td>
<td><span data-ttu-id="779a2-276">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-276">dword</span></span></td>
<td><span data-ttu-id="779a2-277">Те же значения, что и <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> без префикса D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="779a2-277">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="779a2-278">См. D3DRS_STENCILFAIL.</span><span class="sxs-lookup"><span data-stu-id="779a2-278">See D3DRS_STENCILFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-279">стенЦилфунк</span><span class="sxs-lookup"><span data-stu-id="779a2-279">StencilFunc</span></span></td>
<td><span data-ttu-id="779a2-280">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-280">dword</span></span></td>
<td><span data-ttu-id="779a2-281">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> без префикса D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="779a2-281">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="779a2-282">См. D3DRS_STENCILFUNC.</span><span class="sxs-lookup"><span data-stu-id="779a2-282">See D3DRS_STENCILFUNC.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-283">стенЦилмаск</span><span class="sxs-lookup"><span data-stu-id="779a2-283">StencilMask</span></span></td>
<td><span data-ttu-id="779a2-284">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-284">dword</span></span></td>
<td><span data-ttu-id="779a2-285">Те же значения, что и D3DRS_STENCILMASK.</span><span class="sxs-lookup"><span data-stu-id="779a2-285">Same values as D3DRS_STENCILMASK.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-286">стенЦилпасс</span><span class="sxs-lookup"><span data-stu-id="779a2-286">StencilPass</span></span></td>
<td><span data-ttu-id="779a2-287">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-287">dword</span></span></td>
<td><span data-ttu-id="779a2-288">Те же значения, что и <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> без префикса D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="779a2-288">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="779a2-289">См. D3DRS_STENCILPASS.</span><span class="sxs-lookup"><span data-stu-id="779a2-289">See D3DRS_STENCILPASS.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-290">стенЦилреф</span><span class="sxs-lookup"><span data-stu-id="779a2-290">StencilRef</span></span></td>
<td><span data-ttu-id="779a2-291">INT</span><span class="sxs-lookup"><span data-stu-id="779a2-291">int</span></span></td>
<td><span data-ttu-id="779a2-292">Те же значения, что и D3DRS_STENCILREF.</span><span class="sxs-lookup"><span data-stu-id="779a2-292">Same values as D3DRS_STENCILREF.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-293">стенЦилвритемаск</span><span class="sxs-lookup"><span data-stu-id="779a2-293">StencilWriteMask</span></span></td>
<td><span data-ttu-id="779a2-294">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-294">dword</span></span></td>
<td><span data-ttu-id="779a2-295">Те же значения, что и D3DRS_STENCILWRITEMASK.</span><span class="sxs-lookup"><span data-stu-id="779a2-295">Same values as D3DRS_STENCILWRITEMASK.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-296">стенЦилзфаил</span><span class="sxs-lookup"><span data-stu-id="779a2-296">StencilZFail</span></span></td>
<td><span data-ttu-id="779a2-297">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-297">dword</span></span></td>
<td><span data-ttu-id="779a2-298">Те же значения, что и <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> без префикса D3DSTENCILCAP_.</span><span class="sxs-lookup"><span data-stu-id="779a2-298">Same values as <a href="d3dstencilcaps.md">D3DSTENCILCAPS</a> without the D3DSTENCILCAP_ prefix.</span></span> <span data-ttu-id="779a2-299">См. D3DRS_STENCILZFAIL.</span><span class="sxs-lookup"><span data-stu-id="779a2-299">See D3DRS_STENCILZFAIL.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-300">текстурефактор</span><span class="sxs-lookup"><span data-stu-id="779a2-300">TextureFactor</span></span></td>
<td><span data-ttu-id="779a2-301">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-301">dword</span></span></td>
<td><span data-ttu-id="779a2-302">Те же значения, что и <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="779a2-302">Same values as <a href="d3dcolor.md"><strong>D3DCOLOR</strong></a>.</span></span> <span data-ttu-id="779a2-303">Те же значения, что и D3DRS_TEXTUREFACTOR.</span><span class="sxs-lookup"><span data-stu-id="779a2-303">Same values as D3DRS_TEXTUREFACTOR.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-304">Wrap0 - Wrap15</span><span class="sxs-lookup"><span data-stu-id="779a2-304">Wrap0 - Wrap15</span></span></td>
<td><span data-ttu-id="779a2-305">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-305">dword</span></span></td>
<td><span data-ttu-id="779a2-306">Значения совпадают со значениями, используемыми D3DRS_WRAP0.</span><span class="sxs-lookup"><span data-stu-id="779a2-306">Values are the same as the values used by D3DRS_WRAP0.</span></span> <span data-ttu-id="779a2-307">Допустимые значения:</span><span class="sxs-lookup"><span data-stu-id="779a2-307">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="779a2-308">COORD0 (соответствует D3DWRAPCOORD_0)</span><span class="sxs-lookup"><span data-stu-id="779a2-308">COORD0 (which corresponds to D3DWRAPCOORD_0)</span></span></li>
<li><span data-ttu-id="779a2-309">COORD1 (соответствует D3DWRAPCOORD_1)</span><span class="sxs-lookup"><span data-stu-id="779a2-309">COORD1 (which corresponds to D3DWRAPCOORD_1)</span></span></li>
<li><span data-ttu-id="779a2-310">COORD2 (соответствует D3DWRAPCOORD_2)</span><span class="sxs-lookup"><span data-stu-id="779a2-310">COORD2 (which corresponds to D3DWRAPCOORD_2)</span></span></li>
<li><span data-ttu-id="779a2-311">COORD3 (соответствует D3DWRAPCOORD_3)</span><span class="sxs-lookup"><span data-stu-id="779a2-311">COORD3 (which corresponds to D3DWRAPCOORD_3)</span></span></li>
<li><span data-ttu-id="779a2-312">U (соответствует D3DWRAP_U)</span><span class="sxs-lookup"><span data-stu-id="779a2-312">U (which corresponds to D3DWRAP_U)</span></span></li>
<li><span data-ttu-id="779a2-313">V (соответствует D3DWRAP_V)</span><span class="sxs-lookup"><span data-stu-id="779a2-313">V (which corresponds to D3DWRAP_V)</span></span></li>
<li><span data-ttu-id="779a2-314">W (соответствует D3DWRAP_W)</span><span class="sxs-lookup"><span data-stu-id="779a2-314">W (which corresponds to D3DWRAP_W)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-315">зенабле</span><span class="sxs-lookup"><span data-stu-id="779a2-315">ZEnable</span></span></td>
<td><span data-ttu-id="779a2-316">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-316">dword</span></span></td>
<td><span data-ttu-id="779a2-317">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> без префикса D3DZB_.</span><span class="sxs-lookup"><span data-stu-id="779a2-317">Same values as <a href="/windows/desktop/direct3d9/d3dzbuffertype"><strong>D3DZBUFFERTYPE</strong></a> without the D3DZB_ prefix.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="779a2-318">зфунк</span><span class="sxs-lookup"><span data-stu-id="779a2-318">ZFunc</span></span></td>
<td><span data-ttu-id="779a2-319">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-319">dword</span></span></td>
<td><span data-ttu-id="779a2-320">Те же значения, что и <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> без префикса D3DCMP_.</span><span class="sxs-lookup"><span data-stu-id="779a2-320">Same values as <a href="/windows/desktop/direct3d9/d3dcmpfunc"><strong>D3DCMPFUNC</strong></a> without the D3DCMP_ prefix.</span></span> <span data-ttu-id="779a2-321">См. D3DRS_ZFUNC.</span><span class="sxs-lookup"><span data-stu-id="779a2-321">See D3DRS_ZFUNC.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="779a2-322">звритинабле</span><span class="sxs-lookup"><span data-stu-id="779a2-322">ZWriteEnable</span></span></td>
<td><span data-ttu-id="779a2-323">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-323">bool</span></span></td>
<td><span data-ttu-id="779a2-324">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-324">True or False.</span></span> <span data-ttu-id="779a2-325">См. D3DRS_ZWRITEENABLE.</span><span class="sxs-lookup"><span data-stu-id="779a2-325">See D3DRS_ZWRITEENABLE.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="779a2-326">Пример:</span><span class="sxs-lookup"><span data-stu-id="779a2-326">Example:</span></span>


```
AlphaBlendEnable = TRUE;
FillMode = WIREFRAME;
```



<span data-ttu-id="779a2-327">Это позволит включить альфа-смешение и сделать все геометрические отрисовкой в каркасе.</span><span class="sxs-lookup"><span data-stu-id="779a2-327">This will enable alpha blending and make all geometries render in wireframe.</span></span>

### <a name="vertex-pipe-render-states"></a><span data-ttu-id="779a2-328">Состояния рендеринга канала вершин</span><span class="sxs-lookup"><span data-stu-id="779a2-328">Vertex Pipe Render States</span></span>

<span data-ttu-id="779a2-329">Состояния визуализации файла эффектов имеют имена, аналогичные состояниям конвейера фиксированной функции, часто с удаленным префиксом.</span><span class="sxs-lookup"><span data-stu-id="779a2-329">Effect file render states have names similar to the fixed function pipeline states, often with the prefix removed.</span></span>



|                          |        |                                                                                                                                               |
|--------------------------|--------|-----------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="779a2-330">Состояние визуализации</span><span class="sxs-lookup"><span data-stu-id="779a2-330">Render State</span></span>             | <span data-ttu-id="779a2-331">Тип</span><span class="sxs-lookup"><span data-stu-id="779a2-331">Type</span></span>   | <span data-ttu-id="779a2-332">Значения</span><span class="sxs-lookup"><span data-stu-id="779a2-332">Values</span></span>                                                                                                                                        |
| <span data-ttu-id="779a2-333">Окружающее</span><span class="sxs-lookup"><span data-stu-id="779a2-333">Ambient</span></span>                  | <span data-ttu-id="779a2-334">float4</span><span class="sxs-lookup"><span data-stu-id="779a2-334">float4</span></span> | <span data-ttu-id="779a2-335">Те же значения, что и во \_ внешнем D3DRS.</span><span class="sxs-lookup"><span data-stu-id="779a2-335">Same values as D3DRS\_AMBIENT.</span></span>                                                                                                                |
| <span data-ttu-id="779a2-336">амбиентматериалсаурце</span><span class="sxs-lookup"><span data-stu-id="779a2-336">AmbientMaterialSource</span></span>    | <span data-ttu-id="779a2-337">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-337">dword</span></span>  | <span data-ttu-id="779a2-338">Те же значения, что и [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) без \_ префикса D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="779a2-338">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="779a2-339">См. раздел D3DRS \_ амбиентматериалсаурце.</span><span class="sxs-lookup"><span data-stu-id="779a2-339">See D3DRS\_AMBIENTMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="779a2-340">Усечение</span><span class="sxs-lookup"><span data-stu-id="779a2-340">Clipping</span></span>                 | <span data-ttu-id="779a2-341">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-341">bool</span></span>   | <span data-ttu-id="779a2-342">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-342">True or False.</span></span> <span data-ttu-id="779a2-343">Те же значения, что и D3DRSная \_ Обрезка.</span><span class="sxs-lookup"><span data-stu-id="779a2-343">Same values as D3DRS\_CLIPPING.</span></span>                                                                                                |
| <span data-ttu-id="779a2-344">клиппланинабле</span><span class="sxs-lookup"><span data-stu-id="779a2-344">ClipPlaneEnable</span></span>          | <span data-ttu-id="779a2-345">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-345">dword</span></span>  | <span data-ttu-id="779a2-346">Побитовое сочетание макросов D3DCLIPPLANE0-D3DCLIPPLANE5.</span><span class="sxs-lookup"><span data-stu-id="779a2-346">Bitwise combination of D3DCLIPPLANE0 - D3DCLIPPLANE5 macros.</span></span> <span data-ttu-id="779a2-347">См. раздел [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS \_ клиппланинабле.</span><span class="sxs-lookup"><span data-stu-id="779a2-347">See [**D3DCLIPPLANEn**](d3dclipplanen.md) and D3DRS\_CLIPPLANEENABLE.</span></span>           |
| <span data-ttu-id="779a2-348">колорвертекс</span><span class="sxs-lookup"><span data-stu-id="779a2-348">ColorVertex</span></span>              | <span data-ttu-id="779a2-349">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-349">bool</span></span>   | <span data-ttu-id="779a2-350">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-350">True or False.</span></span> <span data-ttu-id="779a2-351">Те же значения, что и в D3DRS \_ колорвертекс.</span><span class="sxs-lookup"><span data-stu-id="779a2-351">Same values as D3DRS\_COLORVERTEX.</span></span>                                                                                             |
| <span data-ttu-id="779a2-352">куллмоде</span><span class="sxs-lookup"><span data-stu-id="779a2-352">CullMode</span></span>                 | <span data-ttu-id="779a2-353">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-353">dword</span></span>  | <span data-ttu-id="779a2-354">Те же значения, что и [**D3DCULL**](./d3dcull.md) без \_ префикса D3DCULL.</span><span class="sxs-lookup"><span data-stu-id="779a2-354">Same values as [**D3DCULL**](./d3dcull.md) without the D3DCULL\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="779a2-355">диффусематериалсаурце</span><span class="sxs-lookup"><span data-stu-id="779a2-355">DiffuseMaterialSource</span></span>    | <span data-ttu-id="779a2-356">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-356">dword</span></span>  | <span data-ttu-id="779a2-357">Те же значения, что и [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) без \_ префикса D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="779a2-357">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="779a2-358">См. раздел D3DRS \_ диффусематериалсаурце.</span><span class="sxs-lookup"><span data-stu-id="779a2-358">See D3DRS\_DIFFUSEMATERIALSOURCE.</span></span>  |
| <span data-ttu-id="779a2-359">емиссивематериалсаурце</span><span class="sxs-lookup"><span data-stu-id="779a2-359">EmissiveMaterialSource</span></span>   | <span data-ttu-id="779a2-360">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-360">dword</span></span>  | <span data-ttu-id="779a2-361">Те же значения, что и [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) без \_ префикса D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="779a2-361">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="779a2-362">См. раздел D3DRS \_ емиссивематериалсаурце.</span><span class="sxs-lookup"><span data-stu-id="779a2-362">See D3DRS\_EMISSIVEMATERIALSOURCE.</span></span> |
| <span data-ttu-id="779a2-363">фогколор</span><span class="sxs-lookup"><span data-stu-id="779a2-363">FogColor</span></span>                 | <span data-ttu-id="779a2-364">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-364">dword</span></span>  | <span data-ttu-id="779a2-365">Те же значения, что и [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-365">Same values as [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="779a2-366">См. раздел D3DRS \_ фогколор.</span><span class="sxs-lookup"><span data-stu-id="779a2-366">See D3DRS\_FOGCOLOR.</span></span>                                                                             |
| <span data-ttu-id="779a2-367">фогденсити</span><span class="sxs-lookup"><span data-stu-id="779a2-367">FogDensity</span></span>               | <span data-ttu-id="779a2-368">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-368">float</span></span>  | <span data-ttu-id="779a2-369">Те же значения, что и в D3DRS \_ фогденсити.</span><span class="sxs-lookup"><span data-stu-id="779a2-369">Same values as D3DRS\_FOGDENSITY.</span></span>                                                                                                             |
| <span data-ttu-id="779a2-370">фоженабле</span><span class="sxs-lookup"><span data-stu-id="779a2-370">FogEnable</span></span>                | <span data-ttu-id="779a2-371">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-371">bool</span></span>   | <span data-ttu-id="779a2-372">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-372">True or False.</span></span> <span data-ttu-id="779a2-373">Те же значения, что и в D3DRS \_ фоженабле.</span><span class="sxs-lookup"><span data-stu-id="779a2-373">Same values as D3DRS\_FOGENABLE.</span></span>                                                                                               |
| <span data-ttu-id="779a2-374">фоженд</span><span class="sxs-lookup"><span data-stu-id="779a2-374">FogEnd</span></span>                   | <span data-ttu-id="779a2-375">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-375">float</span></span>  | <span data-ttu-id="779a2-376">Те же значения, что и в D3DRS \_ фоженд.</span><span class="sxs-lookup"><span data-stu-id="779a2-376">Same values as D3DRS\_FOGEND.</span></span>                                                                                                                 |
| <span data-ttu-id="779a2-377">фогстарт</span><span class="sxs-lookup"><span data-stu-id="779a2-377">FogStart</span></span>                 | <span data-ttu-id="779a2-378">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-378">float</span></span>  | <span data-ttu-id="779a2-379">Те же значения, что и в D3DRS \_ фогстарт.</span><span class="sxs-lookup"><span data-stu-id="779a2-379">Same values as D3DRS\_FOGSTART.</span></span>                                                                                                               |
| <span data-ttu-id="779a2-380">фогтаблемоде</span><span class="sxs-lookup"><span data-stu-id="779a2-380">FogTableMode</span></span>             | <span data-ttu-id="779a2-381">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-381">dword</span></span>  | <span data-ttu-id="779a2-382">Те же значения, что и [**D3DFOGMODE**](./d3dfogmode.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-382">Same values as [**D3DFOGMODE**](./d3dfogmode.md).</span></span> <span data-ttu-id="779a2-383">См. раздел D3DRS \_ фогтаблемоде in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span><span class="sxs-lookup"><span data-stu-id="779a2-383">See D3DRS\_FOGTABLEMODE in [**D3DRENDERSTATETYPE**](./d3drenderstatetype.md).</span></span>     |
| <span data-ttu-id="779a2-384">фогвертексмоде</span><span class="sxs-lookup"><span data-stu-id="779a2-384">FogVertexMode</span></span>            | <span data-ttu-id="779a2-385">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-385">dword</span></span>  | <span data-ttu-id="779a2-386">Те же значения, что и [**D3DFOGMODE**](./d3dfogmode.md) без \_ префикса D3DFOG.</span><span class="sxs-lookup"><span data-stu-id="779a2-386">Same values as [**D3DFOGMODE**](./d3dfogmode.md) without the D3DFOG\_ prefix.</span></span>                                                            |
| <span data-ttu-id="779a2-387">индекседвертексбленденабле</span><span class="sxs-lookup"><span data-stu-id="779a2-387">IndexedVertexBlendEnable</span></span> | <span data-ttu-id="779a2-388">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-388">bool</span></span>   | <span data-ttu-id="779a2-389">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-389">True or False.</span></span> <span data-ttu-id="779a2-390">Те же значения, что и в D3DRS \_ индекседвертексбленденабле.</span><span class="sxs-lookup"><span data-stu-id="779a2-390">Same values as D3DRS\_INDEXEDVERTEXBLENDENABLE.</span></span>                                                                                |
| <span data-ttu-id="779a2-391">Освещение</span><span class="sxs-lookup"><span data-stu-id="779a2-391">Lighting</span></span>                 | <span data-ttu-id="779a2-392">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-392">bool</span></span>   | <span data-ttu-id="779a2-393">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-393">True or False.</span></span> <span data-ttu-id="779a2-394">Те же значения, что и D3DRS \_ освещение.</span><span class="sxs-lookup"><span data-stu-id="779a2-394">Same values as D3DRS\_LIGHTING.</span></span>                                                                                                |
| <span data-ttu-id="779a2-395">локалвиевер</span><span class="sxs-lookup"><span data-stu-id="779a2-395">LocalViewer</span></span>              | <span data-ttu-id="779a2-396">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-396">bool</span></span>   | <span data-ttu-id="779a2-397">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-397">True or False.</span></span> <span data-ttu-id="779a2-398">Те же значения, что и в D3DRS \_ локалвиевер.</span><span class="sxs-lookup"><span data-stu-id="779a2-398">Same values as D3DRS\_LOCALVIEWER.</span></span>                                                                                             |
| <span data-ttu-id="779a2-399">мултисамплеантиалиас</span><span class="sxs-lookup"><span data-stu-id="779a2-399">MultiSampleAntialias</span></span>     | <span data-ttu-id="779a2-400">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-400">bool</span></span>   | <span data-ttu-id="779a2-401">Те же значения, что и в D3DRS \_ мултисамплеантиалиас.</span><span class="sxs-lookup"><span data-stu-id="779a2-401">Same values as D3DRS\_MULTISAMPLEANTIALIAS.</span></span>                                                                                                   |
| <span data-ttu-id="779a2-402">мултисамплемаск</span><span class="sxs-lookup"><span data-stu-id="779a2-402">MultiSampleMask</span></span>          | <span data-ttu-id="779a2-403">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-403">dword</span></span>  | <span data-ttu-id="779a2-404">Те же значения, что и в D3DRS \_ мултисамплемаск.</span><span class="sxs-lookup"><span data-stu-id="779a2-404">Same values as D3DRS\_MULTISAMPLEMASK.</span></span>                                                                                                        |
| <span data-ttu-id="779a2-405">нормализенормалс</span><span class="sxs-lookup"><span data-stu-id="779a2-405">NormalizeNormals</span></span>         | <span data-ttu-id="779a2-406">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-406">bool</span></span>   | <span data-ttu-id="779a2-407">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-407">True or False.</span></span> <span data-ttu-id="779a2-408">Те же значения, что и в D3DRS \_ нормализенормалс.</span><span class="sxs-lookup"><span data-stu-id="779a2-408">Same values as D3DRS\_NORMALIZENORMALS.</span></span>                                                                                        |
| <span data-ttu-id="779a2-409">патчсегментс</span><span class="sxs-lookup"><span data-stu-id="779a2-409">PatchSegments</span></span>            | <span data-ttu-id="779a2-410">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-410">float</span></span>  | <span data-ttu-id="779a2-411">Те же значения, что и в Нсегментс в [**сетнпатчмоде**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span><span class="sxs-lookup"><span data-stu-id="779a2-411">Same values as nSegments in [**SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>                                                         |
| <span data-ttu-id="779a2-412">Поинтскале \_ A</span><span class="sxs-lookup"><span data-stu-id="779a2-412">PointScale\_A</span></span>            | <span data-ttu-id="779a2-413">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-413">float</span></span>  | <span data-ttu-id="779a2-414">Те же значения, что и D3DRS \_ поинтскале \_ A.</span><span class="sxs-lookup"><span data-stu-id="779a2-414">Same values as D3DRS\_POINTSCALE\_A.</span></span>                                                                                                          |
| <span data-ttu-id="779a2-415">Поинтскале \_ б</span><span class="sxs-lookup"><span data-stu-id="779a2-415">PointScale\_B</span></span>            | <span data-ttu-id="779a2-416">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-416">float</span></span>  | <span data-ttu-id="779a2-417">Те же значения, что и в D3DRS \_ поинтскале \_ B.</span><span class="sxs-lookup"><span data-stu-id="779a2-417">Same values as D3DRS\_POINTSCALE\_B.</span></span>                                                                                                          |
| <span data-ttu-id="779a2-418">Поинтскале \_ C</span><span class="sxs-lookup"><span data-stu-id="779a2-418">PointScale\_C</span></span>            | <span data-ttu-id="779a2-419">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-419">float</span></span>  | <span data-ttu-id="779a2-420">Те же значения, что и D3DRS \_ поинтскале \_ C.</span><span class="sxs-lookup"><span data-stu-id="779a2-420">Same values as D3DRS\_POINTSCALE\_C.</span></span>                                                                                                          |
| <span data-ttu-id="779a2-421">поинтскалинабле</span><span class="sxs-lookup"><span data-stu-id="779a2-421">PointScaleEnable</span></span>         | <span data-ttu-id="779a2-422">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-422">bool</span></span>   | <span data-ttu-id="779a2-423">Те же значения, что и в D3DRS \_ поинтскалинабле.</span><span class="sxs-lookup"><span data-stu-id="779a2-423">Same values as D3DRS\_POINTSCALEENABLE.</span></span>                                                                                                       |
| <span data-ttu-id="779a2-424">PointSize</span><span class="sxs-lookup"><span data-stu-id="779a2-424">PointSize</span></span>                | <span data-ttu-id="779a2-425">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-425">float</span></span>  | <span data-ttu-id="779a2-426">Те же значения, что и в D3DRS \_ POINTSIZE.</span><span class="sxs-lookup"><span data-stu-id="779a2-426">Same values as D3DRS\_POINTSIZE.</span></span>                                                                                                              |
| <span data-ttu-id="779a2-427">PointSize \_ мин</span><span class="sxs-lookup"><span data-stu-id="779a2-427">PointSize\_Min</span></span>           | <span data-ttu-id="779a2-428">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-428">float</span></span>  | <span data-ttu-id="779a2-429">Те же значения, что и D3DRS \_ POINTSIZE \_ min.</span><span class="sxs-lookup"><span data-stu-id="779a2-429">Same values as D3DRS\_POINTSIZE\_MIN.</span></span>                                                                                                         |
| <span data-ttu-id="779a2-430">PointSize \_ Max</span><span class="sxs-lookup"><span data-stu-id="779a2-430">PointSize\_Max</span></span>           | <span data-ttu-id="779a2-431">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-431">float</span></span>  | <span data-ttu-id="779a2-432">Те же значения, что и D3DRS \_ POINTSIZE \_ Max без \_ префикса D3DRS.</span><span class="sxs-lookup"><span data-stu-id="779a2-432">Same values as D3DRS\_POINTSIZE\_MAX without the D3DRS\_ prefix.</span></span>                                                                              |
| <span data-ttu-id="779a2-433">поинтспритинабле</span><span class="sxs-lookup"><span data-stu-id="779a2-433">PointSpriteEnable</span></span>        | <span data-ttu-id="779a2-434">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-434">bool</span></span>   | <span data-ttu-id="779a2-435">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-435">True or False.</span></span> <span data-ttu-id="779a2-436">Те же значения, что и в D3DRS \_ поинтспритинабле.</span><span class="sxs-lookup"><span data-stu-id="779a2-436">Same values as D3DRS\_POINTSPRITEENABLE.</span></span>                                                                                       |
| <span data-ttu-id="779a2-437">ранжефоженабле</span><span class="sxs-lookup"><span data-stu-id="779a2-437">RangeFogEnable</span></span>           | <span data-ttu-id="779a2-438">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-438">bool</span></span>   | <span data-ttu-id="779a2-439">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-439">True or False.</span></span> <span data-ttu-id="779a2-440">Те же значения, что и в D3DRS \_ ранжефоженабле.</span><span class="sxs-lookup"><span data-stu-id="779a2-440">Same values as D3DRS\_RANGEFOGENABLE.</span></span>                                                                                          |
| <span data-ttu-id="779a2-441">спекуларенабле</span><span class="sxs-lookup"><span data-stu-id="779a2-441">SpecularEnable</span></span>           | <span data-ttu-id="779a2-442">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-442">bool</span></span>   | <span data-ttu-id="779a2-443">Верно или неверно.</span><span class="sxs-lookup"><span data-stu-id="779a2-443">True or False.</span></span> <span data-ttu-id="779a2-444">Те же значения, что и в D3DRS \_ спекуларенабле.</span><span class="sxs-lookup"><span data-stu-id="779a2-444">Same values as D3DRS\_SPECULARENABLE.</span></span>                                                                                          |
| <span data-ttu-id="779a2-445">спекуларматериалсаурце</span><span class="sxs-lookup"><span data-stu-id="779a2-445">SpecularMaterialSource</span></span>   | <span data-ttu-id="779a2-446">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-446">dword</span></span>  | <span data-ttu-id="779a2-447">Те же значения, что и [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) без \_ префикса D3DMCS.</span><span class="sxs-lookup"><span data-stu-id="779a2-447">Same values as [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) without the D3DMCS\_ prefix.</span></span> <span data-ttu-id="779a2-448">См. раздел D3DRS \_ спекуларматериалсаурце.</span><span class="sxs-lookup"><span data-stu-id="779a2-448">See D3DRS\_SPECULARMATERIALSOURCE.</span></span> |
| <span data-ttu-id="779a2-449">твинфактор</span><span class="sxs-lookup"><span data-stu-id="779a2-449">TweenFactor</span></span>              | <span data-ttu-id="779a2-450">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-450">float</span></span>  | <span data-ttu-id="779a2-451">Те же значения, что и в D3DRS \_ твинфактор.</span><span class="sxs-lookup"><span data-stu-id="779a2-451">Same values as D3DRS\_TWEENFACTOR.</span></span>                                                                                                            |
| <span data-ttu-id="779a2-452">вертексбленд</span><span class="sxs-lookup"><span data-stu-id="779a2-452">VertexBlend</span></span>              | <span data-ttu-id="779a2-453">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-453">dword</span></span>  | <span data-ttu-id="779a2-454">Те же значения, что и [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) без \_ префикса D3DVBF.</span><span class="sxs-lookup"><span data-stu-id="779a2-454">Same values as [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) without the D3DVBF\_ prefix.</span></span> <span data-ttu-id="779a2-455">См. раздел D3DRS \_ вертексбленд.</span><span class="sxs-lookup"><span data-stu-id="779a2-455">See D3DRS\_VERTEXBLEND.</span></span>                  |



 

<span data-ttu-id="779a2-456">Пример:</span><span class="sxs-lookup"><span data-stu-id="779a2-456">Example:</span></span>


```
Ambient = float4<0.7f, 0.0f, 0.0f, 1.0f>;
CullMode = CCW;
FogColor = 0xff0000;
```



<span data-ttu-id="779a2-457">Это сделает окружающий цвет float4<0,7 f, 0,0 f, 0,0 f, 1.0 f>, задать для режима исчисления задних граней значение по часовой стрелке и установить красный цвет тумана.</span><span class="sxs-lookup"><span data-stu-id="779a2-457">This will make the ambient color float4<0.7f, 0.0f, 0.0f, 1.0f>, set the backface culling mode to counter-clockwise, and set the fog color to red.</span></span>

## <a name="sampler-states"></a><span data-ttu-id="779a2-458">Состояния образцов</span><span class="sxs-lookup"><span data-stu-id="779a2-458">Sampler States</span></span>

<span data-ttu-id="779a2-459">Состояние образца представляет объект образца.</span><span class="sxs-lookup"><span data-stu-id="779a2-459">A sampler state represents a sampler object.</span></span>



|         |         |                                     |
|---------|---------|-------------------------------------|
| <span data-ttu-id="779a2-460">Состояние</span><span class="sxs-lookup"><span data-stu-id="779a2-460">State</span></span>   | <span data-ttu-id="779a2-461">Тип</span><span class="sxs-lookup"><span data-stu-id="779a2-461">Type</span></span>    | <span data-ttu-id="779a2-462">Значения</span><span class="sxs-lookup"><span data-stu-id="779a2-462">Values</span></span>                              |
| <span data-ttu-id="779a2-463">Образец</span><span class="sxs-lookup"><span data-stu-id="779a2-463">Sampler</span></span> | <span data-ttu-id="779a2-464">образец</span><span class="sxs-lookup"><span data-stu-id="779a2-464">sampler</span></span> | <span data-ttu-id="779a2-465">**Значение NULL** или блок состояния образца.</span><span class="sxs-lookup"><span data-stu-id="779a2-465">**NULL**, or a sampler state block.</span></span> |



 

## <a name="sampler-stage-states"></a><span data-ttu-id="779a2-466">Состояния стадий образца</span><span class="sxs-lookup"><span data-stu-id="779a2-466">Sampler Stage States</span></span>

<span data-ttu-id="779a2-467">Состояния этапов образца используются для выборки текстур.</span><span class="sxs-lookup"><span data-stu-id="779a2-467">Sampler stage states are used to sample textures.</span></span> <span data-ttu-id="779a2-468">Состояние образца определяет типы фильтрации и режимы адресации текстур.</span><span class="sxs-lookup"><span data-stu-id="779a2-468">Sampler state determines filtering types and texture addressing modes.</span></span>



|                     |                              |                                                                                                                                   |
|---------------------|------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="779a2-469">Состояние образца</span><span class="sxs-lookup"><span data-stu-id="779a2-469">Sampler State</span></span>       | <span data-ttu-id="779a2-470">Тип</span><span class="sxs-lookup"><span data-stu-id="779a2-470">Type</span></span>                         | <span data-ttu-id="779a2-471">Значения</span><span class="sxs-lookup"><span data-stu-id="779a2-471">Values</span></span>                                                                                                                            |
| <span data-ttu-id="779a2-472">Аддрессу \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="779a2-472">AddressU\[16\]</span></span>      | <span data-ttu-id="779a2-473">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-473">dword</span></span>                        | <span data-ttu-id="779a2-474">Те же значения, что и [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) без \_ префикса D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="779a2-474">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="779a2-475">См. раздел D3DSAMP \_ аддрессу.</span><span class="sxs-lookup"><span data-stu-id="779a2-475">See D3DSAMP\_ADDRESSU.</span></span>      |
| <span data-ttu-id="779a2-476">Аддрессв \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="779a2-476">AddressV\[16\]</span></span>      | <span data-ttu-id="779a2-477">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-477">dword</span></span>                        | <span data-ttu-id="779a2-478">Те же значения, что и [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) без \_ префикса D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="779a2-478">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="779a2-479">См. раздел D3DSAMP \_ аддрессв.</span><span class="sxs-lookup"><span data-stu-id="779a2-479">See D3DSAMP\_ADDRESSV.</span></span>      |
| <span data-ttu-id="779a2-480">Аддрессв \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="779a2-480">AddressW\[16\]</span></span>      | <span data-ttu-id="779a2-481">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-481">dword</span></span>                        | <span data-ttu-id="779a2-482">Те же значения, что и [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) без \_ префикса D3DTADDRESS.</span><span class="sxs-lookup"><span data-stu-id="779a2-482">Same values as [**D3DTEXTUREADDRESS**](./d3dtextureaddress.md) without the D3DTADDRESS\_ prefix.</span></span> <span data-ttu-id="779a2-483">См. раздел D3DSAMP \_ аддрессв.</span><span class="sxs-lookup"><span data-stu-id="779a2-483">See D3DSAMP\_ADDRESSW.</span></span>      |
| <span data-ttu-id="779a2-484">BorderColor \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="779a2-484">BorderColor\[16\]</span></span>   | [<span data-ttu-id="779a2-485">**D3DCOLOR**</span><span class="sxs-lookup"><span data-stu-id="779a2-485">**D3DCOLOR**</span></span>](d3dcolor.md) | <span data-ttu-id="779a2-486">Те же значения, что и [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) без \_ префикса D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="779a2-486">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="779a2-487">См. раздел D3DSAMP \_ BORDERCOLOR.</span><span class="sxs-lookup"><span data-stu-id="779a2-487">See D3DSAMP\_BORDERCOLOR.</span></span> |
| <span data-ttu-id="779a2-488">Магфилтер \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="779a2-488">MagFilter\[16\]</span></span>     | <span data-ttu-id="779a2-489">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-489">dword</span></span>                        | <span data-ttu-id="779a2-490">Те же значения, что и [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) без \_ префикса D3DTEXF.</span><span class="sxs-lookup"><span data-stu-id="779a2-490">Same values as [**D3DTEXTUREFILTERTYPE**](./d3dtexturefiltertype.md) without the D3DTEXF\_ prefix.</span></span> <span data-ttu-id="779a2-491">См. раздел D3DSAMP \_ магфилтер.</span><span class="sxs-lookup"><span data-stu-id="779a2-491">See D3DSAMP\_MAGFILTER.</span></span>   |
| <span data-ttu-id="779a2-492">Максанисотропи \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="779a2-492">MaxAnisotropy\[16\]</span></span> | <span data-ttu-id="779a2-493">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-493">dword</span></span>                        | <span data-ttu-id="779a2-494">Те же значения, что и \_ в D3DSAMP максанисотропи без \_ префикса D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="779a2-494">Same values as D3DSAMP\_MAXANISOTROPY without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="779a2-495">Максмиплевел \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="779a2-495">MaxMipLevel\[16\]</span></span>   | <span data-ttu-id="779a2-496">INT</span><span class="sxs-lookup"><span data-stu-id="779a2-496">int</span></span>                          | <span data-ttu-id="779a2-497">Те же значения, что и \_ в D3DSAMP максмиплевел без \_ префикса D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="779a2-497">Same values as D3DSAMP\_MAXMIPLEVEL without the D3DSAMP\_ prefix.</span></span>                                                                 |
| <span data-ttu-id="779a2-498">Минфилтер \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="779a2-498">MinFilter\[16\]</span></span>     | <span data-ttu-id="779a2-499">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-499">dword</span></span>                        | <span data-ttu-id="779a2-500">Те же значения, что и \_ в D3DSAMP минфилтер без \_ префикса D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="779a2-500">Same values as D3DSAMP\_MINFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="779a2-501">Мипфилтер \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="779a2-501">MipFilter\[16\]</span></span>     | <span data-ttu-id="779a2-502">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-502">dword</span></span>                        | <span data-ttu-id="779a2-503">Те же значения, что и \_ в D3DSAMP мипфилтер без \_ префикса D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="779a2-503">Same values as D3DSAMP\_MIPFILTER without the D3DSAMP\_ prefix.</span></span>                                                                   |
| <span data-ttu-id="779a2-504">Мипмаплодбиас \[ 16\]</span><span class="sxs-lookup"><span data-stu-id="779a2-504">MipMapLodBias\[16\]</span></span> | <span data-ttu-id="779a2-505">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-505">float</span></span>                        | <span data-ttu-id="779a2-506">Те же значения, что и \_ в D3DSAMP мипмаплодбиас без \_ префикса D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="779a2-506">Same values as D3DSAMP\_MIPMAPLODBIAS without the D3DSAMP\_ prefix.</span></span>                                                               |
| <span data-ttu-id="779a2-507">сргбтекстуре</span><span class="sxs-lookup"><span data-stu-id="779a2-507">SRGBTexture</span></span>         | <span data-ttu-id="779a2-508">bool</span><span class="sxs-lookup"><span data-stu-id="779a2-508">bool</span></span>                         | <span data-ttu-id="779a2-509">То же значение, что и D3DSAMP \_ сргбтекстуре без \_ префикса D3DSAMP.</span><span class="sxs-lookup"><span data-stu-id="779a2-509">Same value as D3DSAMP\_SRGBTEXTURE without the D3DSAMP\_ prefix.</span></span>                                                                   |



 

<span data-ttu-id="779a2-510">Пример:</span><span class="sxs-lookup"><span data-stu-id="779a2-510">Example:</span></span>


```
AddressU[0] = CLAMP;
AddressV[0] = CLAMP;
AddressW[0] = CLAMP;
```



<span data-ttu-id="779a2-511">Этот зажим УВВ значения в диапазоне от 0 до 1.</span><span class="sxs-lookup"><span data-stu-id="779a2-511">This clamps UVW values to be in between 0 and 1.</span></span>

## <a name="shader-states"></a><span data-ttu-id="779a2-512">Состояния шейдера</span><span class="sxs-lookup"><span data-stu-id="779a2-512">Shader States</span></span>

<span data-ttu-id="779a2-513">Существует только два состояния шейдера: одно связано с объектом шейдера вершин и другим, связанным с объектом шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="779a2-513">There are only two effect shader states: one associated with a vertex shader object and the other associated with a pixel shader object.</span></span>



|              |              |                                                                             |
|--------------|--------------|-----------------------------------------------------------------------------|
| <span data-ttu-id="779a2-514">Состояние шейдера</span><span class="sxs-lookup"><span data-stu-id="779a2-514">Shader State</span></span> | <span data-ttu-id="779a2-515">Тип</span><span class="sxs-lookup"><span data-stu-id="779a2-515">Type</span></span>         | <span data-ttu-id="779a2-516">Значения</span><span class="sxs-lookup"><span data-stu-id="779a2-516">Values</span></span>                                                                      |
| <span data-ttu-id="779a2-517">PixelShader</span><span class="sxs-lookup"><span data-stu-id="779a2-517">PixelShader</span></span>  | <span data-ttu-id="779a2-518">PixelShader</span><span class="sxs-lookup"><span data-stu-id="779a2-518">pixelshader</span></span>  | <span data-ttu-id="779a2-519">**Null**, блок сборки, Цель компиляции или параметр шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="779a2-519">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |
| <span data-ttu-id="779a2-520">вертексшадер</span><span class="sxs-lookup"><span data-stu-id="779a2-520">VertexShader</span></span> | <span data-ttu-id="779a2-521">вертексшадер</span><span class="sxs-lookup"><span data-stu-id="779a2-521">vertexshader</span></span> | <span data-ttu-id="779a2-522">**Null**, блок сборки, Цель компиляции или параметр шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="779a2-522">**NULL**, an assembly block, a compile target, or a pixel shader parameter.</span></span> |



 

<span data-ttu-id="779a2-523">Пример:</span><span class="sxs-lookup"><span data-stu-id="779a2-523">Example:</span></span>


```
VertexShader = compile vs_1_1 VSTexture();
PixelShader  = NULL;
```



<span data-ttu-id="779a2-524">Это приведет к компиляции Встекстуре, шейдера вершин, определенного ранее в файле FX, в шейдер вершин версии 1,1, а затем задает этот Скомпилированный шейдер в качестве шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="779a2-524">This will compile VSTexture, a vertex shader defined earlier in the .fx file, to the vertex shader version 1.1, and then set that compiled shader as the vertex shader.</span></span> <span data-ttu-id="779a2-525">Шейдер пикселей присваивается **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="779a2-525">The pixel shader is assigned to **NULL**.</span></span>

## <a name="shader-constant-states"></a><span data-ttu-id="779a2-526">Состояния констант шейдера</span><span class="sxs-lookup"><span data-stu-id="779a2-526">Shader Constant States</span></span>

<span data-ttu-id="779a2-527">Состояния констант шейдера используются для доступа к параметрам констант шейдера.</span><span class="sxs-lookup"><span data-stu-id="779a2-527">Shader constant states are used to access shader constant parameters.</span></span>



|                       |                 |                                              |
|-----------------------|-----------------|----------------------------------------------|
| <span data-ttu-id="779a2-528">Состояние констант шейдера</span><span class="sxs-lookup"><span data-stu-id="779a2-528">Shader Constant State</span></span> | <span data-ttu-id="779a2-529">Тип</span><span class="sxs-lookup"><span data-stu-id="779a2-529">Type</span></span>            | <span data-ttu-id="779a2-530">Значения</span><span class="sxs-lookup"><span data-stu-id="779a2-530">Values</span></span>                                       |
| <span data-ttu-id="779a2-531">пикселшадерконстант</span><span class="sxs-lookup"><span data-stu-id="779a2-531">PixelShaderConstant</span></span>   | <span data-ttu-id="779a2-532">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="779a2-532">float\[m\[n\]\]</span></span> | <span data-ttu-id="779a2-533">m x n массивов с плавающей запятой; m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="779a2-533">m x n array of floats; m and n are optional.</span></span> |
| <span data-ttu-id="779a2-534">PixelShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="779a2-534">PixelShaderConstant1</span></span>  | <span data-ttu-id="779a2-535">float4</span><span class="sxs-lookup"><span data-stu-id="779a2-535">float4</span></span>          | <span data-ttu-id="779a2-536">Один 4D с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="779a2-536">One 4D float.</span></span>                                |
| <span data-ttu-id="779a2-537">PixelShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="779a2-537">PixelShaderConstant2</span></span>  | <span data-ttu-id="779a2-538">float4x2</span><span class="sxs-lookup"><span data-stu-id="779a2-538">float4x2</span></span>        | <span data-ttu-id="779a2-539">Два типа с плавающей точкой 4D.</span><span class="sxs-lookup"><span data-stu-id="779a2-539">Two 4D floats.</span></span>                               |
| <span data-ttu-id="779a2-540">PixelShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="779a2-540">PixelShaderConstant3</span></span>  | <span data-ttu-id="779a2-541">float4x3</span><span class="sxs-lookup"><span data-stu-id="779a2-541">float4x3</span></span>        | <span data-ttu-id="779a2-542">Три типа 4D с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="779a2-542">Three 4D floats.</span></span>                             |
| <span data-ttu-id="779a2-543">PixelShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="779a2-543">PixelShaderConstant4</span></span>  | <span data-ttu-id="779a2-544">float4x4</span><span class="sxs-lookup"><span data-stu-id="779a2-544">float4x4</span></span>        | <span data-ttu-id="779a2-545">Четыре типа с плавающей точкой 4D.</span><span class="sxs-lookup"><span data-stu-id="779a2-545">Four 4D floats.</span></span>                              |
| <span data-ttu-id="779a2-546">пикселшадерконстантб</span><span class="sxs-lookup"><span data-stu-id="779a2-546">PixelShaderConstantB</span></span>  | <span data-ttu-id="779a2-547">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="779a2-547">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="779a2-548">m x n массивов bools; m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="779a2-548">m x n array of bools; m and n are optional.</span></span>  |
| <span data-ttu-id="779a2-549">пикселшадерконстанти</span><span class="sxs-lookup"><span data-stu-id="779a2-549">PixelShaderConstantI</span></span>  | <span data-ttu-id="779a2-550">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="779a2-550">int\[m\[n\]\]</span></span>   | <span data-ttu-id="779a2-551">m x n массива ints.</span><span class="sxs-lookup"><span data-stu-id="779a2-551">m x n array of ints.</span></span> <span data-ttu-id="779a2-552">m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="779a2-552">m and n are optional.</span></span>   |
| <span data-ttu-id="779a2-553">пикселшадерконстантф</span><span class="sxs-lookup"><span data-stu-id="779a2-553">PixelShaderConstantF</span></span>  | <span data-ttu-id="779a2-554">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="779a2-554">float\[m\[n\]\]</span></span> | <span data-ttu-id="779a2-555">m x n массивов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="779a2-555">m x n array of floats.</span></span> <span data-ttu-id="779a2-556">m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="779a2-556">m and n are optional.</span></span> |
| <span data-ttu-id="779a2-557">вертексшадерконстант</span><span class="sxs-lookup"><span data-stu-id="779a2-557">VertexShaderConstant</span></span>  | <span data-ttu-id="779a2-558">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="779a2-558">float\[m\[n\]\]</span></span> | <span data-ttu-id="779a2-559">m x n массивов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="779a2-559">m x n array of floats.</span></span> <span data-ttu-id="779a2-560">m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="779a2-560">m and n are optional.</span></span> |
| <span data-ttu-id="779a2-561">VertexShaderConstant1</span><span class="sxs-lookup"><span data-stu-id="779a2-561">VertexShaderConstant1</span></span> | <span data-ttu-id="779a2-562">float4</span><span class="sxs-lookup"><span data-stu-id="779a2-562">float4</span></span>          | <span data-ttu-id="779a2-563">Один 4D с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="779a2-563">One 4D float.</span></span>                                |
| <span data-ttu-id="779a2-564">VertexShaderConstant2</span><span class="sxs-lookup"><span data-stu-id="779a2-564">VertexShaderConstant2</span></span> | <span data-ttu-id="779a2-565">float4x2</span><span class="sxs-lookup"><span data-stu-id="779a2-565">float4x2</span></span>        | <span data-ttu-id="779a2-566">Два типа с плавающей точкой 4D.</span><span class="sxs-lookup"><span data-stu-id="779a2-566">Two 4D floats.</span></span>                               |
| <span data-ttu-id="779a2-567">VertexShaderConstant3</span><span class="sxs-lookup"><span data-stu-id="779a2-567">VertexShaderConstant3</span></span> | <span data-ttu-id="779a2-568">float4x3</span><span class="sxs-lookup"><span data-stu-id="779a2-568">float4x3</span></span>        | <span data-ttu-id="779a2-569">Три типа 4D с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="779a2-569">Three 4D floats.</span></span>                             |
| <span data-ttu-id="779a2-570">VertexShaderConstant4</span><span class="sxs-lookup"><span data-stu-id="779a2-570">VertexShaderConstant4</span></span> | <span data-ttu-id="779a2-571">float4x4</span><span class="sxs-lookup"><span data-stu-id="779a2-571">float4x4</span></span>        | <span data-ttu-id="779a2-572">Четыре типа с плавающей точкой 4D.</span><span class="sxs-lookup"><span data-stu-id="779a2-572">Four 4D floats.</span></span>                              |
| <span data-ttu-id="779a2-573">вертексшадерконстантб</span><span class="sxs-lookup"><span data-stu-id="779a2-573">VertexShaderConstantB</span></span> | <span data-ttu-id="779a2-574">bool \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="779a2-574">bool\[m\[n\]\]</span></span>  | <span data-ttu-id="779a2-575">массив логических координат m x n.</span><span class="sxs-lookup"><span data-stu-id="779a2-575">m x n array of bools.</span></span> <span data-ttu-id="779a2-576">m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="779a2-576">m and n are optional.</span></span>  |
| <span data-ttu-id="779a2-577">вертексшадерконстанти</span><span class="sxs-lookup"><span data-stu-id="779a2-577">VertexShaderConstantI</span></span> | <span data-ttu-id="779a2-578">int \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="779a2-578">int\[m\[n\]\]</span></span>   | <span data-ttu-id="779a2-579">m x n массива ints.</span><span class="sxs-lookup"><span data-stu-id="779a2-579">m x n array of ints.</span></span> <span data-ttu-id="779a2-580">m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="779a2-580">m and n are optional.</span></span>   |
| <span data-ttu-id="779a2-581">вертексшадерконстантф</span><span class="sxs-lookup"><span data-stu-id="779a2-581">VertexShaderConstantF</span></span> | <span data-ttu-id="779a2-582">float \[ m \[ n\]\]</span><span class="sxs-lookup"><span data-stu-id="779a2-582">float\[m\[n\]\]</span></span> | <span data-ttu-id="779a2-583">m x n массивов с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="779a2-583">m x n array of floats.</span></span> <span data-ttu-id="779a2-584">m и n являются необязательными.</span><span class="sxs-lookup"><span data-stu-id="779a2-584">m and n are optional.</span></span> |



 

## <a name="texture-states"></a><span data-ttu-id="779a2-585">Состояния текстуры</span><span class="sxs-lookup"><span data-stu-id="779a2-585">Texture States</span></span>

<span data-ttu-id="779a2-586">Состояние текстуры инициализирует текстуры, используемые многотекстурным смешением.</span><span class="sxs-lookup"><span data-stu-id="779a2-586">Texture states initialize textures used by the multitexture blender.</span></span>



|               |         |                                   |
|---------------|---------|-----------------------------------|
| <span data-ttu-id="779a2-587">Состояние текстуры</span><span class="sxs-lookup"><span data-stu-id="779a2-587">Texture State</span></span> | <span data-ttu-id="779a2-588">Тип</span><span class="sxs-lookup"><span data-stu-id="779a2-588">Type</span></span>    | <span data-ttu-id="779a2-589">Значения</span><span class="sxs-lookup"><span data-stu-id="779a2-589">Values</span></span>                            |
| <span data-ttu-id="779a2-590">Текстура \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-590">Texture\[8\]</span></span>  | <span data-ttu-id="779a2-591">текстура</span><span class="sxs-lookup"><span data-stu-id="779a2-591">texture</span></span> | <span data-ttu-id="779a2-592">**Null** или параметр текстуры.</span><span class="sxs-lookup"><span data-stu-id="779a2-592">**NULL**, or a texture parameter.</span></span> |



 

## <a name="texture-stage-states"></a><span data-ttu-id="779a2-593">Состояния стадии текстуры</span><span class="sxs-lookup"><span data-stu-id="779a2-593">Texture Stage States</span></span>

<span data-ttu-id="779a2-594">Состояния стадии текстуры настраиваются текстуры и этапы текстуры в многотекстурном смешении.</span><span class="sxs-lookup"><span data-stu-id="779a2-594">Texture stage states set up textures and the texture stages in the multitexture blender.</span></span>



|                            |       |                                                                                                                                                           |
|----------------------------|-------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="779a2-595">Состояние этапа текстуры</span><span class="sxs-lookup"><span data-stu-id="779a2-595">Texture Stage State</span></span>        | <span data-ttu-id="779a2-596">Тип</span><span class="sxs-lookup"><span data-stu-id="779a2-596">Type</span></span>  | <span data-ttu-id="779a2-597">Значения</span><span class="sxs-lookup"><span data-stu-id="779a2-597">Values</span></span>                                                                                                                                                    |
| <span data-ttu-id="779a2-598">Алфаоп \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-598">AlphaOp\[8\]</span></span>               | <span data-ttu-id="779a2-599">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-599">dword</span></span> | <span data-ttu-id="779a2-600">То же, что и [**D3DTEXTUREOP**](./d3dtextureop.md) без \_ префикса D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="779a2-600">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="779a2-601">См. раздел D3DTSS \_ алфаоп.</span><span class="sxs-lookup"><span data-stu-id="779a2-601">See D3DTSS\_ALPHAOP.</span></span>                                                      |
| <span data-ttu-id="779a2-602">AlphaArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-602">AlphaArg0\[8\]</span></span>             | <span data-ttu-id="779a2-603">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-603">dword</span></span> | <span data-ttu-id="779a2-604">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="779a2-604">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="779a2-605">См. раздел D3DTSS \_ ALPHAARG0.</span><span class="sxs-lookup"><span data-stu-id="779a2-605">See D3DTSS\_ALPHAARG0.</span></span>                                                                             |
| <span data-ttu-id="779a2-606">AlphaArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-606">AlphaArg1\[8\]</span></span>             | <span data-ttu-id="779a2-607">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-607">dword</span></span> | <span data-ttu-id="779a2-608">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="779a2-608">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="779a2-609">См. раздел D3DTSS \_ ALPHAARG1.</span><span class="sxs-lookup"><span data-stu-id="779a2-609">See D3DTSS\_ALPHAARG1.</span></span>                                                                             |
| <span data-ttu-id="779a2-610">AlphaArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-610">AlphaArg2\[8\]</span></span>             | <span data-ttu-id="779a2-611">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-611">dword</span></span> | <span data-ttu-id="779a2-612">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="779a2-612">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="779a2-613">См. раздел D3DTSS \_ ALPHAARG2.</span><span class="sxs-lookup"><span data-stu-id="779a2-613">See D3DTSS\_ALPHAARG2.</span></span>                                                                             |
| <span data-ttu-id="779a2-614">ColorArg0 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-614">ColorArg0\[8\]</span></span>             | <span data-ttu-id="779a2-615">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-615">dword</span></span> | <span data-ttu-id="779a2-616">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="779a2-616">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="779a2-617">См. раздел D3DTSS \_ COLORARG0.</span><span class="sxs-lookup"><span data-stu-id="779a2-617">See D3DTSS\_COLORARG0.</span></span>                                                                             |
| <span data-ttu-id="779a2-618">ColorArg1 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-618">ColorArg1\[8\]</span></span>             | <span data-ttu-id="779a2-619">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-619">dword</span></span> | <span data-ttu-id="779a2-620">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="779a2-620">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="779a2-621">См. раздел D3DTSS \_ COLORARG1.</span><span class="sxs-lookup"><span data-stu-id="779a2-621">See D3DTSS\_COLORARG1.</span></span>                                                                             |
| <span data-ttu-id="779a2-622">ColorArg2 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-622">ColorArg2\[8\]</span></span>             | <span data-ttu-id="779a2-623">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-623">dword</span></span> | <span data-ttu-id="779a2-624">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="779a2-624">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="779a2-625">См. раздел D3DTSS \_ COLORARG2.</span><span class="sxs-lookup"><span data-stu-id="779a2-625">See D3DTSS\_COLORARG2.</span></span>                                                                             |
| <span data-ttu-id="779a2-626">Колороп \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-626">ColorOp\[8\]</span></span>               | <span data-ttu-id="779a2-627">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-627">dword</span></span> | <span data-ttu-id="779a2-628">То же, что и [**D3DTEXTUREOP**](./d3dtextureop.md) без \_ префикса D3DTOP.</span><span class="sxs-lookup"><span data-stu-id="779a2-628">Same as [**D3DTEXTUREOP**](./d3dtextureop.md) without the D3DTOP\_ prefix.</span></span> <span data-ttu-id="779a2-629">См. раздел D3DTSS \_ колороп.</span><span class="sxs-lookup"><span data-stu-id="779a2-629">See D3DTSS\_COLOROP.</span></span>                                                      |
| <span data-ttu-id="779a2-630">Бумпенвлскале \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-630">BumpEnvLScale\[8\]</span></span>         | <span data-ttu-id="779a2-631">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-631">float</span></span> | <span data-ttu-id="779a2-632">Те же значения, что и D3DTSS \_ бумпенвлскале без \_ префикса D3DTSS тЦи.</span><span class="sxs-lookup"><span data-stu-id="779a2-632">Same values as D3DTSS\_BUMPENVLSCALE without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="779a2-633">Бумпенвлоффсет \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-633">BumpEnvLOffset\[8\]</span></span>        | <span data-ttu-id="779a2-634">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-634">float</span></span> | <span data-ttu-id="779a2-635">Те же значения, что и D3DTSS \_ бумпенвлоффсет без \_ префикса D3DTSS тЦи.</span><span class="sxs-lookup"><span data-stu-id="779a2-635">Same values as D3DTSS\_BUMPENVLOFFSET without the D3DTSS\_TCI prefix.</span></span>                                                                                     |
| <span data-ttu-id="779a2-636">BumpEnvMat00 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-636">BumpEnvMat00\[8\]</span></span>          | <span data-ttu-id="779a2-637">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-637">float</span></span> | <span data-ttu-id="779a2-638">Те же значения, что и в D3DTSS \_ BUMPENVMAT00.</span><span class="sxs-lookup"><span data-stu-id="779a2-638">Same values as D3DTSS\_BUMPENVMAT00.</span></span>                                                                                                                      |
| <span data-ttu-id="779a2-639">BumpEnvMat01 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-639">BumpEnvMat01\[8\]</span></span>          | <span data-ttu-id="779a2-640">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-640">float</span></span> | <span data-ttu-id="779a2-641">Те же значения, что и в D3DTSS \_ BUMPENVMAT01.</span><span class="sxs-lookup"><span data-stu-id="779a2-641">Same values as D3DTSS\_BUMPENVMAT01.</span></span>                                                                                                                      |
| <span data-ttu-id="779a2-642">BumpEnvMat10 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-642">BumpEnvMat10\[8\]</span></span>          | <span data-ttu-id="779a2-643">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-643">float</span></span> | <span data-ttu-id="779a2-644">Те же значения, что и в D3DTSS \_ BUMPENVMAT10.</span><span class="sxs-lookup"><span data-stu-id="779a2-644">Same values as D3DTSS\_BUMPENVMAT10.</span></span>                                                                                                                      |
| <span data-ttu-id="779a2-645">BumpEnvMat11 \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-645">BumpEnvMat11\[8\]</span></span>          | <span data-ttu-id="779a2-646">FLOAT</span><span class="sxs-lookup"><span data-stu-id="779a2-646">float</span></span> | <span data-ttu-id="779a2-647">Те же значения, что и в D3DTSS \_ BUMPENVMAT11.</span><span class="sxs-lookup"><span data-stu-id="779a2-647">Same values as D3DTSS\_BUMPENVMAT11.</span></span>                                                                                                                      |
| <span data-ttu-id="779a2-648">Ресултарг \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-648">ResultArg\[8\]</span></span>             | <span data-ttu-id="779a2-649">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-649">dword</span></span> | <span data-ttu-id="779a2-650">То же, что и [D3DTA](d3dta.md) без \_ префикса D3DTA.</span><span class="sxs-lookup"><span data-stu-id="779a2-650">Same as [D3DTA](d3dta.md) without the D3DTA\_ prefix.</span></span> <span data-ttu-id="779a2-651">См. раздел D3DTSS \_ ресултарг.</span><span class="sxs-lookup"><span data-stu-id="779a2-651">See D3DTSS\_RESULTARG.</span></span>                                                                             |
| <span data-ttu-id="779a2-652">Текскурдиндекс \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-652">TexCoordIndex\[8\]</span></span>         | <span data-ttu-id="779a2-653">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-653">dword</span></span> | <span data-ttu-id="779a2-654">Те же значения, что и D3DTSS \_ текскурдиндекс без \_ префикса D3DTSS тЦи.</span><span class="sxs-lookup"><span data-stu-id="779a2-654">Same values as D3DTSS\_TEXCOORDINDEX without the D3DTSS\_TCI prefix.</span></span>                                                                                      |
| <span data-ttu-id="779a2-655">Текстуретрансформфлагс \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-655">TextureTransformFlags\[8\]</span></span> | <span data-ttu-id="779a2-656">dword</span><span class="sxs-lookup"><span data-stu-id="779a2-656">dword</span></span> | <span data-ttu-id="779a2-657">Те же значения, что и значения [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) без \_ префикса D3DTTFF.</span><span class="sxs-lookup"><span data-stu-id="779a2-657">Same values as [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) values without the D3DTTFF\_ prefix.</span></span> <span data-ttu-id="779a2-658">См. раздел D3DTSS \_ текстуретрансформфлагс.</span><span class="sxs-lookup"><span data-stu-id="779a2-658">See D3DTSS\_TEXTURETRANSFORMFLAGS.</span></span> |



 

## <a name="transform-states"></a><span data-ttu-id="779a2-659">Состояния преобразования</span><span class="sxs-lookup"><span data-stu-id="779a2-659">Transform States</span></span>

<span data-ttu-id="779a2-660">Задайте состояния преобразования, чтобы инициализировать матрицы преобразования.</span><span class="sxs-lookup"><span data-stu-id="779a2-660">Set transform states to initialize transformation matrices.</span></span> <span data-ttu-id="779a2-661">Эффекты используют перелагаемые матрицы для повышения эффективности.</span><span class="sxs-lookup"><span data-stu-id="779a2-661">Effects use transposed matrices for efficiency.</span></span> <span data-ttu-id="779a2-662">Можно указать, что в результате передаются матрицы, или результат автоматически перестанет представлять собой матрицы перед их использованием.</span><span class="sxs-lookup"><span data-stu-id="779a2-662">You can provide transposed matrices to an effect, or an effect will automatically transpose the matrices before using them.</span></span>



|                       |          |                                                                                                                                 |
|-----------------------|----------|---------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="779a2-663">Состояние преобразования</span><span class="sxs-lookup"><span data-stu-id="779a2-663">Transform State</span></span>       | <span data-ttu-id="779a2-664">Тип</span><span class="sxs-lookup"><span data-stu-id="779a2-664">Type</span></span>     | <span data-ttu-id="779a2-665">Значения</span><span class="sxs-lookup"><span data-stu-id="779a2-665">Values</span></span>                                                                                                                          |
| <span data-ttu-id="779a2-666">прожектионтрансформ</span><span class="sxs-lookup"><span data-stu-id="779a2-666">ProjectionTransform</span></span>   | <span data-ttu-id="779a2-667">float4x4</span><span class="sxs-lookup"><span data-stu-id="779a2-667">float4x4</span></span> | <span data-ttu-id="779a2-668">Матрица 4x4 с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="779a2-668">A 4x4 matrix of floats.</span></span> <span data-ttu-id="779a2-669">Те же значения, что и \_ у D3DTS проекции без \_ префикса D3DTS.</span><span class="sxs-lookup"><span data-stu-id="779a2-669">Same values as D3DTS\_PROJECTION without the D3DTS\_ prefix.</span></span>                                            |
| <span data-ttu-id="779a2-670">Текстуретрансформ \[ 8\]</span><span class="sxs-lookup"><span data-stu-id="779a2-670">TextureTransform\[8\]</span></span> | <span data-ttu-id="779a2-671">float4x4</span><span class="sxs-lookup"><span data-stu-id="779a2-671">float4x4</span></span> | <span data-ttu-id="779a2-672">Матрица 4x4 с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="779a2-672">A 4x4 matrix of floats.</span></span> <span data-ttu-id="779a2-673">Те же значения, что и [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) без \_ префикса D3DTS.</span><span class="sxs-lookup"><span data-stu-id="779a2-673">Same values as [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md) without the D3DTS\_ prefix.</span></span> |
| <span data-ttu-id="779a2-674">виевтрансформ</span><span class="sxs-lookup"><span data-stu-id="779a2-674">ViewTransform</span></span>         | <span data-ttu-id="779a2-675">float4x4</span><span class="sxs-lookup"><span data-stu-id="779a2-675">float4x4</span></span> | <span data-ttu-id="779a2-676">Матрица 4x4 с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="779a2-676">A 4x4 matrix of floats.</span></span> <span data-ttu-id="779a2-677">Те же значения, что и \_ в представлении D3DTS без \_ префикса D3DTS.</span><span class="sxs-lookup"><span data-stu-id="779a2-677">Same values as D3DTS\_VIEW without the D3DTS\_ prefix.</span></span>                                                  |
| <span data-ttu-id="779a2-678">ворлдтрансформ</span><span class="sxs-lookup"><span data-stu-id="779a2-678">WorldTransform</span></span>        | <span data-ttu-id="779a2-679">float4x4</span><span class="sxs-lookup"><span data-stu-id="779a2-679">float4x4</span></span> | <span data-ttu-id="779a2-680">Матрица 4x4 с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="779a2-680">A 4x4 matrix of floats.</span></span>                                                                                                         |



 

## <a name="related-topics"></a><span data-ttu-id="779a2-681">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="779a2-681">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="779a2-682">Формат эффектов</span><span class="sxs-lookup"><span data-stu-id="779a2-682">Effect Format</span></span>](dx9-graphics-reference-effects-file-format.md)
</dt> </dl>

 

 
