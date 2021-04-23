---
description: Используйте коллекцию Сашостпараметервалуе, чтобы определить коллекцию значений ведущего приложения, а также их тип и члены, предоставленные для эффектов.
ms.assetid: 3fef353d-323a-4cc1-a8c9-2bf154754835
title: Привязка данных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b67305d4acc8a4ed9e0827203e4602db26a99da
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104341542"
---
# <a name="data-binding"></a><span data-ttu-id="1c894-103">Привязка данных</span><span class="sxs-lookup"><span data-stu-id="1c894-103">Data Binding</span></span>

<span data-ttu-id="1c894-104">Используйте [коллекцию сашостпараметервалуе](#sashostparametervalue-collection) , чтобы определить коллекцию значений ведущего приложения, а также их тип и члены, предоставленные для эффектов.</span><span class="sxs-lookup"><span data-stu-id="1c894-104">Use [SasHostParameterValue Collection](#sashostparametervalue-collection) to define the collection of host application values, as well as their type and members, exposed to effects.</span></span> <span data-ttu-id="1c894-105">Используйте заметку [сасбиндаддресс](#sasbindaddress) в файле эффектов, чтобы связать параметр Effect с соответствующим параметром в ведущем приложении.</span><span class="sxs-lookup"><span data-stu-id="1c894-105">Use the [SasBindAddress](#sasbindaddress) annotation in an effect file to associate an effect parameter with its corresponding parameter in the host application.</span></span>

## <a name="sashostparametervalue-collection"></a><span data-ttu-id="1c894-106">Коллекция Сашостпараметервалуе</span><span class="sxs-lookup"><span data-stu-id="1c894-106">SasHostParameterValue Collection</span></span>

<span data-ttu-id="1c894-107">Сашостпараметервалуе определяется с помощью синтаксиса файла эффектов (. FX).</span><span class="sxs-lookup"><span data-stu-id="1c894-107">The SasHostParameterValue is defined using effect file (.fx) syntax.</span></span> <span data-ttu-id="1c894-108">Хотя синтаксис очень похож на синтаксис файла эффектов, существуют некоторые различия.</span><span class="sxs-lookup"><span data-stu-id="1c894-108">While the syntax is very similar to the effect file syntax, some differences exist.</span></span> <span data-ttu-id="1c894-109">Например, типы объектов, такие как Texture2D, пробы и строки, недопустимы в файлах фактических эффектов, но являются допустимыми в Сашостпараметервалуе.</span><span class="sxs-lookup"><span data-stu-id="1c894-109">For example, object types, such as texture2d, samplers, and strings, are not valid in actual effect files, but are valid in the SasHostParameterValue.</span></span> <span data-ttu-id="1c894-110">Ведущее приложение может реализовать Сашостпараметервалуе любым способом до тех пор, пока он соответствует описанию ниже. фактическое определение находится в файле стандартных эффектов ДКССАС, включаемых в файл ( \[ корень пакета SDK \] /утилитиес/саурце/САС/САС.фксх).</span><span class="sxs-lookup"><span data-stu-id="1c894-110">A host application can implement SasHostParameterValue in any way so long as it conforms to the description below; the actual definition is located in the DXSAS standard effect include file (\[SDK Root\]/Utilities/Source/Sas/Sas.fxh).</span></span>

<span data-ttu-id="1c894-111">Обратите внимание, что массивы в Сашостпараметервалуе, такие как индикаторы или камеры, имеют неограниченную длину.</span><span class="sxs-lookup"><span data-stu-id="1c894-111">Note that arrays in the SasHostParameterValue such as Lights or Cameras have unbounded length.</span></span> <span data-ttu-id="1c894-112">Это означает, что эффекты могут быть привязаны к любому произвольному индексу в этих массивах, и ведущие приложения должны предоставлять осмысленные значения по умолчанию в случаях, когда не может быть предоставлено значение приложения.</span><span class="sxs-lookup"><span data-stu-id="1c894-112">This means that effects can bind to any arbitrary index in those arrays and host applications must provide meaningful defaults in the cases where no application value can be provided.</span></span>

<span data-ttu-id="1c894-113">Некоторые типы и константы, которые необходимо определить в стандарте ДКССАС, включают, как указано в определении стандартного включения.</span><span class="sxs-lookup"><span data-stu-id="1c894-113">Some types and constants are required to be defined in the DXSAS standard include, as noted in the definition of the standard include.</span></span> <span data-ttu-id="1c894-114">Это позволяет эффектам легко привязывать агрегированные значения из Сашостпараметервалуе к параметрам структурированного эффекта.</span><span class="sxs-lookup"><span data-stu-id="1c894-114">This allows effects to easily bind aggregated values from the SasHostParameterValue to structured effect parameters.</span></span>



| <span data-ttu-id="1c894-115">Коллекция Сашостпараметервалуе</span><span class="sxs-lookup"><span data-stu-id="1c894-115">SasHostParameterValue Collection</span></span>    | <span data-ttu-id="1c894-116">Type</span><span class="sxs-lookup"><span data-stu-id="1c894-116">Type</span></span>            | <span data-ttu-id="1c894-117">Член</span><span class="sxs-lookup"><span data-stu-id="1c894-117">Member</span></span>                                       |
|-------------------------------------|-----------------|----------------------------------------------|
| [<span data-ttu-id="1c894-118">Time</span><span class="sxs-lookup"><span data-stu-id="1c894-118">Time</span></span>](#time)                       | <span data-ttu-id="1c894-119">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1c894-119">float</span></span>           | <span data-ttu-id="1c894-120">SAS. time. Now</span><span class="sxs-lookup"><span data-stu-id="1c894-120">Sas.Time.Now</span></span>                                 |
|                                     | <span data-ttu-id="1c894-121">FLOAT</span><span class="sxs-lookup"><span data-stu-id="1c894-121">float</span></span>           | <span data-ttu-id="1c894-122">SAS. time. Last</span><span class="sxs-lookup"><span data-stu-id="1c894-122">Sas.Time.Last</span></span>                                |
|                                     | <span data-ttu-id="1c894-123">INT</span><span class="sxs-lookup"><span data-stu-id="1c894-123">int</span></span>             | <span data-ttu-id="1c894-124">SAS. time. Фраменумбер</span><span class="sxs-lookup"><span data-stu-id="1c894-124">Sas.Time.FrameNumber</span></span>                         |
| [<span data-ttu-id="1c894-125">Схема среды</span><span class="sxs-lookup"><span data-stu-id="1c894-125">Environment Map</span></span>](#environment-map) | <span data-ttu-id="1c894-126">текстурекубе</span><span class="sxs-lookup"><span data-stu-id="1c894-126">textureCUBE</span></span>     | <span data-ttu-id="1c894-127">SAS. Енвиронментмап</span><span class="sxs-lookup"><span data-stu-id="1c894-127">Sas.EnvironmentMap</span></span>                           |
| [<span data-ttu-id="1c894-128">Камера</span><span class="sxs-lookup"><span data-stu-id="1c894-128">Camera</span></span>](#camera)                   | <span data-ttu-id="1c894-129">саскамера</span><span class="sxs-lookup"><span data-stu-id="1c894-129">SasCamera</span></span>       | <span data-ttu-id="1c894-130">SAS. Camera</span><span class="sxs-lookup"><span data-stu-id="1c894-130">Sas.Camera</span></span>                                   |
|                                     | <span data-ttu-id="1c894-131">float4x4</span><span class="sxs-lookup"><span data-stu-id="1c894-131">float4x4</span></span>        | <span data-ttu-id="1c894-132">SAS. Camera. Ворлдтовиев</span><span class="sxs-lookup"><span data-stu-id="1c894-132">Sas.Camera.WorldToView</span></span>                       |
|                                     | <span data-ttu-id="1c894-133">float4x4</span><span class="sxs-lookup"><span data-stu-id="1c894-133">float4x4</span></span>        | <span data-ttu-id="1c894-134">SAS. Camera. проекция</span><span class="sxs-lookup"><span data-stu-id="1c894-134">Sas.Camera.Projection</span></span>                        |
|                                     | <span data-ttu-id="1c894-135">float2</span><span class="sxs-lookup"><span data-stu-id="1c894-135">float2</span></span>          | <span data-ttu-id="1c894-136">SAS. Camera. Неарфарклиппинг</span><span class="sxs-lookup"><span data-stu-id="1c894-136">Sas.Camera.NearFarClipping</span></span>                   |
| [<span data-ttu-id="1c894-137">Светлый</span><span class="sxs-lookup"><span data-stu-id="1c894-137">Light</span></span>](#light)                     | <span data-ttu-id="1c894-138">сасамбиентлигхт</span><span class="sxs-lookup"><span data-stu-id="1c894-138">SasAmbientLight</span></span> | <span data-ttu-id="1c894-139">AmbientLight \[ зерурморе \] ;</span><span class="sxs-lookup"><span data-stu-id="1c894-139">AmbientLight\[ZeroOrMore\];</span></span>                  |
|                                     | <span data-ttu-id="1c894-140">INT</span><span class="sxs-lookup"><span data-stu-id="1c894-140">int</span></span>             | <span data-ttu-id="1c894-141">SAS. Нумамбиентлигхтс</span><span class="sxs-lookup"><span data-stu-id="1c894-141">Sas.NumAmbientLights</span></span>                         |
|                                     | <span data-ttu-id="1c894-142">сасамбиентлигхт</span><span class="sxs-lookup"><span data-stu-id="1c894-142">SasAmbientLight</span></span> | <span data-ttu-id="1c894-143">DirectionalLight \[ зерурморе \] ;</span><span class="sxs-lookup"><span data-stu-id="1c894-143">DirectionalLight\[ZeroOrMore\];</span></span>              |
|                                     | <span data-ttu-id="1c894-144">INT</span><span class="sxs-lookup"><span data-stu-id="1c894-144">int</span></span>             | <span data-ttu-id="1c894-145">SAS. Нумдиректионаллигхтс</span><span class="sxs-lookup"><span data-stu-id="1c894-145">Sas.NumDirectionalLights</span></span>                     |
|                                     | <span data-ttu-id="1c894-146">сасамбиентлигхт</span><span class="sxs-lookup"><span data-stu-id="1c894-146">SasAmbientLight</span></span> | <span data-ttu-id="1c894-147">PointLight \[ зерурморе \] ;</span><span class="sxs-lookup"><span data-stu-id="1c894-147">PointLight\[ZeroOrMore\];</span></span>                    |
|                                     | <span data-ttu-id="1c894-148">INT</span><span class="sxs-lookup"><span data-stu-id="1c894-148">int</span></span>             | <span data-ttu-id="1c894-149">SAS. Нумпоинтлигхтс</span><span class="sxs-lookup"><span data-stu-id="1c894-149">Sas.NumPointLights</span></span>                           |
|                                     | <span data-ttu-id="1c894-150">сасамбиентлигхт</span><span class="sxs-lookup"><span data-stu-id="1c894-150">SasAmbientLight</span></span> | <span data-ttu-id="1c894-151">Прожектор \[ зерурморе \] ;</span><span class="sxs-lookup"><span data-stu-id="1c894-151">SpotLight\[ZeroOrMore\];</span></span>                     |
|                                     | <span data-ttu-id="1c894-152">INT</span><span class="sxs-lookup"><span data-stu-id="1c894-152">int</span></span>             | <span data-ttu-id="1c894-153">SAS. Нумспотлигхтс</span><span class="sxs-lookup"><span data-stu-id="1c894-153">Sas.NumSpotLights</span></span>                            |
| [<span data-ttu-id="1c894-154">Shadow</span><span class="sxs-lookup"><span data-stu-id="1c894-154">Shadow</span></span>](#shadow)                   | <span data-ttu-id="1c894-155">float4x4</span><span class="sxs-lookup"><span data-stu-id="1c894-155">float4x4</span></span>        | <span data-ttu-id="1c894-156">SAS. Shadow \[ зерурморе \] . ворлдтошадов</span><span class="sxs-lookup"><span data-stu-id="1c894-156">Sas.Shadow\[ZeroOrMore\].WorldToShadow</span></span>       |
|                                     | <span data-ttu-id="1c894-157">texture2D</span><span class="sxs-lookup"><span data-stu-id="1c894-157">texture2D</span></span>       | <span data-ttu-id="1c894-158">SAS. Shadow \[ зерурморе \] . шадовмап</span><span class="sxs-lookup"><span data-stu-id="1c894-158">Sas.Shadow\[ZeroOrMore\].ShadowMap</span></span>           |
| [<span data-ttu-id="1c894-159">Скелет</span><span class="sxs-lookup"><span data-stu-id="1c894-159">Skeleton</span></span>](#skeleton)               | <span data-ttu-id="1c894-160">float4x4</span><span class="sxs-lookup"><span data-stu-id="1c894-160">float4x4</span></span>        | <span data-ttu-id="1c894-161">SAS. скелет. Мештожоинттоворлд \[ онеорморе\]</span><span class="sxs-lookup"><span data-stu-id="1c894-161">Sas.Skeleton.MeshToJointToWorld\[OneOrMore\]</span></span> |
|                                     | <span data-ttu-id="1c894-162">INT</span><span class="sxs-lookup"><span data-stu-id="1c894-162">int</span></span>             | <span data-ttu-id="1c894-163">SAS. скелет. Нумжоинтс</span><span class="sxs-lookup"><span data-stu-id="1c894-163">Sas.Skeleton.NumJoints</span></span>                       |



 

### <a name="time"></a><span data-ttu-id="1c894-164">Время</span><span class="sxs-lookup"><span data-stu-id="1c894-164">Time</span></span>

<span data-ttu-id="1c894-165">Виртуальное время или значение времени ведущего приложения.</span><span class="sxs-lookup"><span data-stu-id="1c894-165">The host application's virtual clock or time value.</span></span> <span data-ttu-id="1c894-166">Члены включают:</span><span class="sxs-lookup"><span data-stu-id="1c894-166">Members include:</span></span>

-   <span data-ttu-id="1c894-167">SAS. time. Now — значение виртуальных часов ведущего приложения в точке, в которой будет отображаться результат.</span><span class="sxs-lookup"><span data-stu-id="1c894-167">Sas.Time.Now - the value of the host application virtual clock at the point at which the effect will be rendered.</span></span>
-   <span data-ttu-id="1c894-168">SAS. time. Last — значение на предыдущем этапе рендеринга.</span><span class="sxs-lookup"><span data-stu-id="1c894-168">Sas.Time.Last - the value of Now at the previous render.</span></span>
-   <span data-ttu-id="1c894-169">SAS. time. Фраменумбер — значение счетчика, увеличивающееся один раз для каждого отображаемого кадра.</span><span class="sxs-lookup"><span data-stu-id="1c894-169">Sas.Time.FrameNumber - the counter value that is incremented once per rendered frame.</span></span>

<span data-ttu-id="1c894-170">Эффекты должны правильно обходиться на тот факт, что значения этих элементов потенциально могут быть обработаны в течение крайне долгого времени выполнения.</span><span class="sxs-lookup"><span data-stu-id="1c894-170">Effects must properly handle the fact that the values of these members can potentially wrap around during extremely long execution times.</span></span> <span data-ttu-id="1c894-171">Теперь и Last могут иметь очень большие значения.</span><span class="sxs-lookup"><span data-stu-id="1c894-171">Now and Last may have very large values.</span></span>

### <a name="environment-map"></a><span data-ttu-id="1c894-172">Схема среды</span><span class="sxs-lookup"><span data-stu-id="1c894-172">Environment Map</span></span>

<span data-ttu-id="1c894-173">Схема кубических сред.</span><span class="sxs-lookup"><span data-stu-id="1c894-173">A cubic environment map.</span></span> <span data-ttu-id="1c894-174">Ведущие приложения должны предоставить допустимую текстуру Куба, если действие пытается выполнить привязку к SAS. Енвиронментмап.</span><span class="sxs-lookup"><span data-stu-id="1c894-174">Host applications must provide a valid cube texture if an effect attempts to bind to Sas.EnvironmentMap.</span></span>

### <a name="camera"></a><span data-ttu-id="1c894-175">Камера</span><span class="sxs-lookup"><span data-stu-id="1c894-175">Camera</span></span>

<span data-ttu-id="1c894-176">Камера, которая готовится к просмотру.</span><span class="sxs-lookup"><span data-stu-id="1c894-176">The camera currently being rendered.</span></span> <span data-ttu-id="1c894-177">Члены включают:</span><span class="sxs-lookup"><span data-stu-id="1c894-177">Members include:</span></span>

-   <span data-ttu-id="1c894-178">SAS. Camera. Ворлдтовиев — составная матрица представления для камеры.</span><span class="sxs-lookup"><span data-stu-id="1c894-178">Sas.Camera.WorldToView - the composite world-view matrix for the camera.</span></span>
-   <span data-ttu-id="1c894-179">SAS. Camera. проекция — матрица проекции для камеры.</span><span class="sxs-lookup"><span data-stu-id="1c894-179">Sas.Camera.Projection - the projection matrix for the camera.</span></span>
-   <span data-ttu-id="1c894-180">SAS. Camera. Неарфарклиппинг — значения ближайших и дальне обрезанных плоскостей.</span><span class="sxs-lookup"><span data-stu-id="1c894-180">Sas.Camera.NearFarClipping - the values of the near and far clipping planes.</span></span>

### <a name="light"></a><span data-ttu-id="1c894-181">Светлая</span><span class="sxs-lookup"><span data-stu-id="1c894-181">Light</span></span>

<span data-ttu-id="1c894-182">Один или несколько индикаторов сцены.</span><span class="sxs-lookup"><span data-stu-id="1c894-182">One or more scene lights.</span></span> <span data-ttu-id="1c894-183">Коллекция источников света объявляется как массив, где:</span><span class="sxs-lookup"><span data-stu-id="1c894-183">The collection of lights is declared as an array where:</span></span>

-   <span data-ttu-id="1c894-184">Color — цвет RGB.</span><span class="sxs-lookup"><span data-stu-id="1c894-184">Color - an RGB color.</span></span> <span data-ttu-id="1c894-185">Значение по умолчанию — (0,0,0).</span><span class="sxs-lookup"><span data-stu-id="1c894-185">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="1c894-186">Направление — направление освещения.</span><span class="sxs-lookup"><span data-stu-id="1c894-186">Direction - the light direction.</span></span> <span data-ttu-id="1c894-187">Значение по умолчанию — (0,0,0).</span><span class="sxs-lookup"><span data-stu-id="1c894-187">The default value is (0,0,0).</span></span>
-   <span data-ttu-id="1c894-188">Диапазон — расстояние от освещения, где лампочки не влияют на сцену.</span><span class="sxs-lookup"><span data-stu-id="1c894-188">Range - the distance from the light where the light rays have no effect on the scene.</span></span> <span data-ttu-id="1c894-189">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="1c894-189">The default value is 0.</span></span>
-   <span data-ttu-id="1c894-190">Тета — внутренний угол конуса прожектора, измеряемый в радианах.</span><span class="sxs-lookup"><span data-stu-id="1c894-190">Theta - the inner cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="1c894-191">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="1c894-191">The default value is 0.</span></span>
-   <span data-ttu-id="1c894-192">Фи — угол внешнего конуса в центре внимания, измеряемый в радианах.</span><span class="sxs-lookup"><span data-stu-id="1c894-192">Phi - the outer cone angle of a spotlight, measured in radians.</span></span> <span data-ttu-id="1c894-193">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="1c894-193">The default value is 0.</span></span>

<span data-ttu-id="1c894-194">Число источников света должно быть равно числу источников света, привязанных к связанному массиву.</span><span class="sxs-lookup"><span data-stu-id="1c894-194">The number of lights must be set to the number of lights bound into the associated array.</span></span> <span data-ttu-id="1c894-195">Эффекты могут игнорировать количество источников света и привязывать их к любому элементу одного из массивов освещения.</span><span class="sxs-lookup"><span data-stu-id="1c894-195">Effects can choose to ignore the number of lights and bind to any element of one of the light arrays.</span></span> <span data-ttu-id="1c894-196">Поэтому ведущие приложения должны предоставить допустимую привязку для элементов, которые выходят за пределы числа источников света в массиве.</span><span class="sxs-lookup"><span data-stu-id="1c894-196">Therefore, host applications must provide a valid binding for elements beyond the number of lights in the array.</span></span>

<span data-ttu-id="1c894-197">Зерурморе подразумевает, что массив может содержать любое количество элементов.</span><span class="sxs-lookup"><span data-stu-id="1c894-197">ZeroOrMore implies that the array may have any number of elements.</span></span>

### <a name="shadow"></a><span data-ttu-id="1c894-198">Shadow</span><span class="sxs-lookup"><span data-stu-id="1c894-198">Shadow</span></span>

<span data-ttu-id="1c894-199">Теневые буферы, которые состоят из:</span><span class="sxs-lookup"><span data-stu-id="1c894-199">Shadow buffers which consists of:</span></span>

-   <span data-ttu-id="1c894-200">Ворлдтошадов — массив матриц.</span><span class="sxs-lookup"><span data-stu-id="1c894-200">WorldToShadow - an array of matrices.</span></span>
-   <span data-ttu-id="1c894-201">Шадовмап — файл двухмерной текстуры.</span><span class="sxs-lookup"><span data-stu-id="1c894-201">ShadowMap - a 2D texture file.</span></span>

<span data-ttu-id="1c894-202">Зерурморе подразумевает, что массив может содержать любое количество элементов (ноль означает пустой массив).</span><span class="sxs-lookup"><span data-stu-id="1c894-202">ZeroOrMore implies that the array may have any number of elements (zero means an empty array).</span></span>

<span data-ttu-id="1c894-203">Результатом будет объявление образца следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1c894-203">An effect would declare a sampler as follows:</span></span>


```
texture2D Shadow 
<
  string SasBindAddress = "Sas.Shadow[0].ShadowMap";
>;

sampler ShadowSampler = shadow_sampler(Shadow);
```



### <a name="skeleton"></a><span data-ttu-id="1c894-204">Скелет</span><span class="sxs-lookup"><span data-stu-id="1c894-204">Skeleton</span></span>

<span data-ttu-id="1c894-205">Набор кадров, составляющих текущий объект отрисовки.</span><span class="sxs-lookup"><span data-stu-id="1c894-205">The set of frames that compose the currently rendering object.</span></span> <span data-ttu-id="1c894-206">Примерами кадров являются кости и преобразования.</span><span class="sxs-lookup"><span data-stu-id="1c894-206">Frame examples are bones and transforms.</span></span> <span data-ttu-id="1c894-207">В том числе:</span><span class="sxs-lookup"><span data-stu-id="1c894-207">This includes:</span></span>

-   <span data-ttu-id="1c894-208">Мештожоинттоворлд — массив матриц.</span><span class="sxs-lookup"><span data-stu-id="1c894-208">MeshToJointToWorld - an array of matrices.</span></span>
-   <span data-ttu-id="1c894-209">Нумжоинтс — число соединений в скелете.</span><span class="sxs-lookup"><span data-stu-id="1c894-209">NumJoints - the number of joints in the skeleton.</span></span>

<span data-ttu-id="1c894-210">Онеорморе подразумевает, что массив содержит по крайней мере один элемент и может содержать любое количество элементов.</span><span class="sxs-lookup"><span data-stu-id="1c894-210">OneOrMore implies that the array has at least one and may contain any number of elements.</span></span>

<span data-ttu-id="1c894-211">Определение поддерживает объекты сетки как с жесткими, так и с обложками, используя один набор значений [Сашостпараметервалуе коллекций](#sashostparametervalue-collection) с разной интерпретацией.</span><span class="sxs-lookup"><span data-stu-id="1c894-211">The definition supports both rigid and skinned mesh objects using the same set of [SasHostParameterValue Collection](#sashostparametervalue-collection) values with different interpretation.</span></span>

## <a name="sasbindaddress"></a><span data-ttu-id="1c894-212">сасбиндаддресс</span><span class="sxs-lookup"><span data-stu-id="1c894-212">SasBindAddress</span></span>

<span data-ttu-id="1c894-213">Эта заметка добавляется в начало файла действия, чтобы связать параметр Effect с соответствующим параметром, определенным в [коллекции сашостпараметервалуе](#sashostparametervalue-collection).</span><span class="sxs-lookup"><span data-stu-id="1c894-213">This annotation is added to the top of an effect file to associate an effect parameter with its corresponding parameter defined in the [SasHostParameterValue Collection](#sashostparametervalue-collection).</span></span> <span data-ttu-id="1c894-214">Аннотация объявляется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="1c894-214">The annotation is declared like this:</span></span>


```
string SasBindAddress = "SasHostParameterValue";
```



<span data-ttu-id="1c894-215">В этом примере в матрицу Мештожоинттоворлд привязывается матрица, содействующая по всему миру:</span><span class="sxs-lookup"><span data-stu-id="1c894-215">This example binds the effect world matrix to the MeshToJointToWorld matrix:</span></span>


```
float4x3 World
<
  string SasBindAddress = "Sas.Skeleton.MeshToJointToWorld[0]";
>;
```



<span data-ttu-id="1c894-216">Эта заметка сообщает ведущему приложению, что ему нужно задать значение матрицы эффектов в мире, используя данные в матрице Мештожоинттоворлд.</span><span class="sxs-lookup"><span data-stu-id="1c894-216">This annotation tells the host application that it needs to set the value of the effect world matrix using the data in the MeshToJointToWorld matrix.</span></span>

<span data-ttu-id="1c894-217">Синтаксис заметки адреса привязки был очень похож на синтаксис, используемый [**ID3DXEffect**](id3dxeffect.md) для получения и установки параметров эффектов.</span><span class="sxs-lookup"><span data-stu-id="1c894-217">The bind address annotation syntax was defined to be very similar with the syntax used by [**ID3DXEffect**](id3dxeffect.md) to get and set effect parameters.</span></span> <span data-ttu-id="1c894-218">Единственное различие между методами грамматики ДКССАС и **ID3DXEffect** заключается в добавлении маркера «звездочка».</span><span class="sxs-lookup"><span data-stu-id="1c894-218">The only difference between the DXSAS grammar and **ID3DXEffect** methods is the addition of the asterisk index token.</span></span> <span data-ttu-id="1c894-219">Ниже приведен еще один пример использования указателя со звездочкой:</span><span class="sxs-lookup"><span data-stu-id="1c894-219">Here is another example using the asterisk index:</span></span>


```
float3 LightColors[6]
<
  string SasBindAddress = "Sas.Light[*].Color";
>;
```



<span data-ttu-id="1c894-220">Маркер индекса звездочки означает, что все элементы определенного массива значений енвирнмант узла (цвет в данном случае) должны быть привязаны в связанном параметре.</span><span class="sxs-lookup"><span data-stu-id="1c894-220">The asterisk index token denotes that all elements of the particular host envirnmant value array (color in this case) should be bound in the associated parameter.</span></span> <span data-ttu-id="1c894-221">Несколько маркеров индекса звездочки позволяют привязывать эффекты к вложенным элементам массива структур без необходимости привязки всей структуры.</span><span class="sxs-lookup"><span data-stu-id="1c894-221">Multiple asterisk index tokens allow effects to bind to sub-elements of an array of structures without the need to bind the entire structure itself.</span></span> <span data-ttu-id="1c894-222">В этом примере значения цвета первых шести источников привязываются к параметру Effect.</span><span class="sxs-lookup"><span data-stu-id="1c894-222">This example binds the color values of the first six lights to an effect parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1c894-223">См. также</span><span class="sxs-lookup"><span data-stu-id="1c894-223">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1c894-224">Справочник по стандарту DirectX для заметок и семантик</span><span class="sxs-lookup"><span data-stu-id="1c894-224">DirectX Standard Annotations and Semantics Reference</span></span>](dx9-graphics-reference-effects-dxsas.md)
</dt> </dl>

 

 



