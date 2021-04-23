---
title: Вопросы и ответы по Direct3D 10
description: Эта статья содержит некоторые часто задаваемые вопросы, связанные с Direct3D 10, от точки зрения разработчика, который переносит существующее приложение с Direct3D 9 (D3D9) на Direct3D 10 (D3D10).
ms.assetid: da3022ca-b120-d0d7-6747-65b946dbc73c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7aae228923715400e5ba7e4f795e3ea6bfacfd98
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134131"
---
# <a name="direct3d-10-frequently-asked-questions"></a><span data-ttu-id="b439f-103">Вопросы и ответы по Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="b439f-103">Direct3D 10 Frequently Asked Questions</span></span>

<span data-ttu-id="b439f-104">Эта статья содержит некоторые часто задаваемые вопросы, связанные с Direct3D 10, от точки зрения разработчика, который переносит существующее приложение с Direct3D 9 (D3D9) на Direct3D 10 (D3D10).</span><span class="sxs-lookup"><span data-stu-id="b439f-104">This article contains some of the frequently asked questions surrounding Direct3D 10 from the point of view of a developer who is porting an existing application from Direct3D 9 (D3D9) to Direct3D 10 (D3D10).</span></span>

-   [<span data-ttu-id="b439f-105">Буферы констант</span><span class="sxs-lookup"><span data-stu-id="b439f-105">Constant Buffers</span></span>](#constant-buffers)
-   [<span data-ttu-id="b439f-106">Состояние</span><span class="sxs-lookup"><span data-stu-id="b439f-106">State</span></span>](#state)
-   [<span data-ttu-id="b439f-107">Форматы</span><span class="sxs-lookup"><span data-stu-id="b439f-107">Formats</span></span>](#formats)
-   [<span data-ttu-id="b439f-108">Компоновка шейдера</span><span class="sxs-lookup"><span data-stu-id="b439f-108">Shader Linkage</span></span>](#shader-linkage)
-   [<span data-ttu-id="b439f-109">Вызовы Draw</span><span class="sxs-lookup"><span data-stu-id="b439f-109">Draw Calls</span></span>](#draw-calls)
-   [<span data-ttu-id="b439f-110">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="b439f-110">Resources</span></span>](#resources)
-   [<span data-ttu-id="b439f-111">Глубина как текстура</span><span class="sxs-lookup"><span data-stu-id="b439f-111">Depth as Texture</span></span>](#depth-as-texture)
-   [<span data-ttu-id="b439f-112">MSAA</span><span class="sxs-lookup"><span data-stu-id="b439f-112">MSAA</span></span>](#msaa)
-   [<span data-ttu-id="b439f-113">Сбои</span><span class="sxs-lookup"><span data-stu-id="b439f-113">Crashes</span></span>](#crashes)
-   [<span data-ttu-id="b439f-114">Отрисовка с предикатом</span><span class="sxs-lookup"><span data-stu-id="b439f-114">Predicated Rendering</span></span>](#predicated-rendering)
-   [<span data-ttu-id="b439f-115">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="b439f-115">Geometry Shader</span></span>](#geometry-shader)
-   [<span data-ttu-id="b439f-116">HLSL</span><span class="sxs-lookup"><span data-stu-id="b439f-116">HLSL</span></span>](#hlsl)

## <a name="constant-buffers"></a><span data-ttu-id="b439f-117">Буферы констант</span><span class="sxs-lookup"><span data-stu-id="b439f-117">Constant Buffers</span></span>

<dl> <dt>

<span data-ttu-id="b439f-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>Как лучше всего обновлять буферы констант?</span><span class="sxs-lookup"><span data-stu-id="b439f-118"><span id="What_is_the_best_way_to_update_constant_buffers_"></span><span id="what_is_the_best_way_to_update_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_UPDATE_CONSTANT_BUFFERS_"></span>What is the best way to update constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="b439f-119">Упдатесубресаурце и Map с отклонениями должны иметь одинаковую скорость.</span><span class="sxs-lookup"><span data-stu-id="b439f-119">UpdateSubresource and Map with Discard should be about the same speed.</span></span> <span data-ttu-id="b439f-120">Выберите один из них в зависимости от того, какой из них копирует минимальный объем памяти.</span><span class="sxs-lookup"><span data-stu-id="b439f-120">Choose between them depending on which one copies the least amount of memory.</span></span> <span data-ttu-id="b439f-121">Если данные, хранящиеся в памяти, уже хранятся в одном непрерывном блоке, используйте Упдатесубресаурце.</span><span class="sxs-lookup"><span data-stu-id="b439f-121">If you already have your data stored in memory in one contiguous block, use UpdateSubresource.</span></span> <span data-ttu-id="b439f-122">Если необходимо накапливать данные из других мест, используйте Map с параметром Discard.</span><span class="sxs-lookup"><span data-stu-id="b439f-122">If you need to accumulate data from other places, use Map with Discard.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>Каков самый худший способ организации буферов констант?</span><span class="sxs-lookup"><span data-stu-id="b439f-123"><span id="What_is_the_worst_way_to_organize_constant_buffers_"></span><span id="what_is_the_worst_way_to_organize_constant_buffers_"></span><span id="WHAT_IS_THE_WORST_WAY_TO_ORGANIZE_CONSTANT_BUFFERS_"></span>What is the worst way to organize constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="b439f-124">Наихудшая производительность достигается путем помещения всех констант для конкретного шейдера в один буфер констант.</span><span class="sxs-lookup"><span data-stu-id="b439f-124">The worst performance is realized by putting all constants for a particular shader into one constant buffer.</span></span> <span data-ttu-id="b439f-125">Хотя это и часто является самым простым способом переноса с D3D9 на D3D10, он может криппле производительность.</span><span class="sxs-lookup"><span data-stu-id="b439f-125">While this often is the easiest way to port from D3D9 to D3D10, it can cripple performance.</span></span> <span data-ttu-id="b439f-126">Например, рассмотрим ситуацию, в которой используется следующий буфер констант:</span><span class="sxs-lookup"><span data-stu-id="b439f-126">For example, consider a scenario that uses the following constant buffer:</span></span>

``` syntax
cbuffer VSGlobalsCB
{
    matrix  ViewProj;
    matrix  Bones[100];
    matrix  World;
    float   SpecPower;
    float4  BDRFCoefficients;
    float   AppTime;
    uint2   RenderTargetSize;
};
```

<span data-ttu-id="b439f-127">Буфер равен 6560 байт.</span><span class="sxs-lookup"><span data-stu-id="b439f-127">The buffer is 6560 bytes.</span></span> <span data-ttu-id="b439f-128">Предположим, что имеется приложение с 1000 объектами для подготовки к просмотру, 100 из которых представляют собой сетчатые сети, а 900 — статические сетки.</span><span class="sxs-lookup"><span data-stu-id="b439f-128">Assume there is an application with 1000 objects to be rendered, 100 of which are skinned meshes, and 900 of which are static meshes.</span></span> <span data-ttu-id="b439f-129">Кроме того, предположим, что это приложение использует теневое сопоставление с одним источником освещения.</span><span class="sxs-lookup"><span data-stu-id="b439f-129">Also, assume that this application is using shadow mapping with one light source.</span></span> <span data-ttu-id="b439f-130">Это означает, что существует два прохода: один для карты глубины, отображаемый на свете, и один для прохода прямой отрисовки.</span><span class="sxs-lookup"><span data-stu-id="b439f-130">This means there are two passes, one for the depth map rendered from the light, and one for the forward rendering pass.</span></span> <span data-ttu-id="b439f-131">Это приводит к 2000 вызовов Draw.</span><span class="sxs-lookup"><span data-stu-id="b439f-131">This results in 2000 draw calls.</span></span> <span data-ttu-id="b439f-132">Хотя каждому вызову Draw не требуется обновлять все части буфера констант, весь буфер констант по-прежнему обновляется и отправляется на карту.</span><span class="sxs-lookup"><span data-stu-id="b439f-132">Although each draw call does not NEED to update every part of the constant buffer, the entire constant buffer still is updated and sent to the card.</span></span> <span data-ttu-id="b439f-133">Это приводит к обновлению 13 МБ данных в каждом кадре (2000 вызовов времени вызова 6560 КБ).</span><span class="sxs-lookup"><span data-stu-id="b439f-133">This results in the update of 13 MB of data every frame (2000 draw calls times 6560 KB).</span></span>

</dd> <dt>

<span data-ttu-id="b439f-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>Каков лучший способ организации постоянных буферов?</span><span class="sxs-lookup"><span data-stu-id="b439f-134"><span id="What_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="what_is_the_best_way_to_organize_my_constant_buffers_"></span><span id="WHAT_IS_THE_BEST_WAY_TO_ORGANIZE_MY_CONSTANT_BUFFERS_"></span>What is the best way to organize my constant buffers?</span></span>
</dt> <dd>

<span data-ttu-id="b439f-135">Лучший способ — упорядочить постоянные буферы по частоте обновления.</span><span class="sxs-lookup"><span data-stu-id="b439f-135">The best way is to organize constant buffers by frequency of update.</span></span> <span data-ttu-id="b439f-136">Константы, которые обновляются с одинаковыми частотой, должны находиться в одном буфере.</span><span class="sxs-lookup"><span data-stu-id="b439f-136">Constants that are updated at similar frequencies should be in the same buffer.</span></span> <span data-ttu-id="b439f-137">Например, рассмотрим сценарий, представленный в разделе "что является наихудшим способом организации буферов констант?", но с более подходящим макетом постоянной структуры:</span><span class="sxs-lookup"><span data-stu-id="b439f-137">For example, consider the scenario presented under, "What is the worst way to organize constant buffers?," but with a better constant layout:</span></span>

``` syntax
cbuffer VSGlobalPerFrameCB
  { 
    float   AppTime; 
  };
cbuffer VSPerSkinnedCB
  { 
    matrix  Bones[100]; 
  };
cbuffer VSPerStaticCB
  {
    matrix  World;
  };
cbuffer VSPerPassCB
  {
    matrix  ViewProj;
    uint2   RenderTargetSize;
  };
cbuffer VSPerMaterialCB
  {
    float   SpecPower;
    float4  BDRFCoefficients;
  };    
```

<span data-ttu-id="b439f-138">Буферы констант разбиваются по частоте обновления, но это лишь половина решения.</span><span class="sxs-lookup"><span data-stu-id="b439f-138">Constant buffers are split by their update frequency, but this only is half of the solution.</span></span> <span data-ttu-id="b439f-139">Приложению необходимо правильно обновить буферы констант, чтобы воспользоваться всеми преимуществами разбиения.</span><span class="sxs-lookup"><span data-stu-id="b439f-139">The application needs to update the constant buffers correctly in order to take full advantage of the split.</span></span> <span data-ttu-id="b439f-140">Мы будем рассчитывать на ту же сцену, что и на примере выше: 900. статические сетки, 100 в обложках, один проход и один проход вперед.</span><span class="sxs-lookup"><span data-stu-id="b439f-140">We will assume the same scene as above: 900 static meshes, 100 skinned meshes, one light pass, and one forward pass.</span></span> <span data-ttu-id="b439f-141">Также предполагается, что будут храниться некоторые константные буферы на объект.</span><span class="sxs-lookup"><span data-stu-id="b439f-141">We also will assume that some constant buffers per-object will be stored.</span></span> <span data-ttu-id="b439f-142">Это означает, что каждый объект будет содержать либо Всперскиннедкб, либо Всперстатиккб в зависимости от того, является ли он обложкой или статичным.</span><span class="sxs-lookup"><span data-stu-id="b439f-142">This means that each object will contain either a VSPerSkinnedCB or a VSPerStaticCB, depending on whether or not it is skinned or static.</span></span> <span data-ttu-id="b439f-143">Мы делаем это, чтобы избежать удвоения количества матриц, отправленных по конвейеру.</span><span class="sxs-lookup"><span data-stu-id="b439f-143">We do this in order to avoid doubling the amount of matrices sent through the pipeline.</span></span>

<span data-ttu-id="b439f-144">Мы разбиваем фрейм на три фазы.</span><span class="sxs-lookup"><span data-stu-id="b439f-144">We split the frame into three phases.</span></span> <span data-ttu-id="b439f-145">Первый этап является началом кадра и не включает отрисовку, а только постоянные обновления.</span><span class="sxs-lookup"><span data-stu-id="b439f-145">The first phase is the beginning of the frame and involves no rendering, just constant updates.</span></span>

<dl> <dt>

<span data-ttu-id="b439f-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Начальный кадр**</span><span class="sxs-lookup"><span data-stu-id="b439f-146"><span id="Begin_Frame"></span><span id="begin_frame"></span><span id="BEGIN_FRAME"></span>**Begin Frame**</span></span>
</dt> <dd>

-   <span data-ttu-id="b439f-147">Обновление Всглобалперфрамекб для времени приложения (4 байта)</span><span class="sxs-lookup"><span data-stu-id="b439f-147">Update VSGlobalPerFrameCB for application time (4 bytes)</span></span>
-   <span data-ttu-id="b439f-148">Обновление 100 Всперскиннедкб для объектов с обложкой 100 (640000 байт)</span><span class="sxs-lookup"><span data-stu-id="b439f-148">Update 100 VSPerSkinnedCB for the 100 skinned objects (640000 bytes)</span></span>
-   <span data-ttu-id="b439f-149">Обновление Всперстатиккб для 900 статических объектов (57600 байт)</span><span class="sxs-lookup"><span data-stu-id="b439f-149">Update VSPerStaticCB for 900 static objects (57600 bytes)</span></span>

<span data-ttu-id="b439f-150">Далее следует проход теневой карты.</span><span class="sxs-lookup"><span data-stu-id="b439f-150">Next is the shadow map pass.</span></span> <span data-ttu-id="b439f-151">Обратите внимание, что фактически обновляются только постоянные буферы Всперпасскб.</span><span class="sxs-lookup"><span data-stu-id="b439f-151">Notice that the only constant buffer that actually updates is VSPerPassCB.</span></span> <span data-ttu-id="b439f-152">Все остальные буферы констант были обновлены во время прохода начала кадра.</span><span class="sxs-lookup"><span data-stu-id="b439f-152">All other constant buffers were updated during the begin frame pass.</span></span> <span data-ttu-id="b439f-153">Хотя нам все равно нужно привязывать эти буферы констант, объем данных, передаваемых видеоадаптеру, минимальен, поскольку буферы уже обновлены.</span><span class="sxs-lookup"><span data-stu-id="b439f-153">While we still need to bind these constant buffers, the amount of information passed to the video card is minimal, because the buffers already have been updated.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Проход тени**</span><span class="sxs-lookup"><span data-stu-id="b439f-154"><span id="Shadow_Pass"></span><span id="shadow_pass"></span><span id="SHADOW_PASS"></span>**Shadow Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="b439f-155">Обновление Всперпасскб (72 байт)</span><span class="sxs-lookup"><span data-stu-id="b439f-155">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="b439f-156">Рисование 100 сеток с обложками (100, привязки, без обновлений)</span><span class="sxs-lookup"><span data-stu-id="b439f-156">Draw 100 skinned meshes (100 binds, no updates)</span></span>
-   <span data-ttu-id="b439f-157">Рисование 900 статических сеток (100 привязок, без обновлений)</span><span class="sxs-lookup"><span data-stu-id="b439f-157">Draw 900 static meshes (100 binds, no updates)</span></span>

<span data-ttu-id="b439f-158">Аналогичным образом, проход прямой визуализации должен обновить данные для каждого материала, так как он не хранился отдельно для каждой сети.</span><span class="sxs-lookup"><span data-stu-id="b439f-158">Similarly, the forward rendering pass only needs to update per-material data, because it was not stored per-mesh.</span></span> <span data-ttu-id="b439f-159">Если предполагается, что в сцене используется 500 материалов:</span><span class="sxs-lookup"><span data-stu-id="b439f-159">If we assume that there are 500 materials in use in the scene:</span></span>

</dd> <dt>

<span data-ttu-id="b439f-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Прямой проход**</span><span class="sxs-lookup"><span data-stu-id="b439f-160"><span id="Forward_Pass"></span><span id="forward_pass"></span><span id="FORWARD_PASS"></span>**Forward Pass**</span></span>
</dt> <dd>

-   <span data-ttu-id="b439f-161">Обновление Всперпасскб (72 байт)</span><span class="sxs-lookup"><span data-stu-id="b439f-161">Update VSPerPassCB (72 bytes)</span></span>
-   <span data-ttu-id="b439f-162">Обновление 500 Всперматериалкбс (10000 байт)</span><span class="sxs-lookup"><span data-stu-id="b439f-162">Update 500 VSPerMaterialCBs (10000 bytes)</span></span>

<span data-ttu-id="b439f-163">Это приводит к общему объему всего 707 КБ.</span><span class="sxs-lookup"><span data-stu-id="b439f-163">This results in a total of just 707 KB.</span></span> <span data-ttu-id="b439f-164">Хотя это очень надуманный сценарий, он показывает, сколько постоянных затрат на обновление можно уменьшить, сортируя константы по частоте обновления.</span><span class="sxs-lookup"><span data-stu-id="b439f-164">Although this is a very contrived scenario, it illustrates just how much constant update overhead can be reduced by sorting constants by frequency of update.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b439f-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>Что делать, если у меня недостаточно места для хранения отдельных буферов констант для моих сеток, материалов и т. д.?</span><span class="sxs-lookup"><span data-stu-id="b439f-165"><span id="What_if_I_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="what_if_i_do_not_have_enough_space_to_store_individual_constant_buffers_for_my_meshes__material__and_so_on___"></span><span id="WHAT_IF_I_DO_NOT_HAVE_ENOUGH_SPACE_TO_STORE_INDIVIDUAL_CONSTANT_BUFFERS_FOR_MY_MESHES__MATERIAL__AND_SO_ON___"></span>What if I do not have enough space to store individual constant buffers for my meshes, material, and so on?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-166">Вы всегда можете использовать многоуровневые системы буферов констант.</span><span class="sxs-lookup"><span data-stu-id="b439f-166">You always can use a tiered system of constant buffers.</span></span> <span data-ttu-id="b439f-167">Создайте буферы констант с переменным размером (16 байт, 32 байт, 64 байт и т. д.) вплоть до самого большого необходимого размера буфера константы.</span><span class="sxs-lookup"><span data-stu-id="b439f-167">Create variable-sized constant buffers (16 bytes, 32 bytes, 64 bytes, and so on) up to the largest constant buffer size needed.</span></span> <span data-ttu-id="b439f-168">Когда необходимо привязать буфер константы к шейдеру, выберите наименьший буфер констант, который может содержать данные, необходимые шейдеру.</span><span class="sxs-lookup"><span data-stu-id="b439f-168">When it is time to bind a constant buffer to a shader, select the smallest constant buffer that can hold the data needed by the shader.</span></span> <span data-ttu-id="b439f-169">Хотя этот подход немного менее эффективен, это хороший промежуточный шаг.</span><span class="sxs-lookup"><span data-stu-id="b439f-169">Although this approach is slightly less efficient, it is a good intermediate step.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>Я использую постоянные буферы между разными шейдерами.</span><span class="sxs-lookup"><span data-stu-id="b439f-170"><span id="I_am_sharing_constant_buffers_between_different_shaders._One_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._What_is_the_best_way_to_update_these___"></span><span id="i_am_sharing_constant_buffers_between_different_shaders._one_shader_may_use_all_of_the_constants__but_another_may_use_some_of_the_constants._what_is_the_best_way_to_update_these___"></span><span id="I_AM_SHARING_CONSTANT_BUFFERS_BETWEEN_DIFFERENT_SHADERS._ONE_SHADER_MAY_USE_ALL_OF_THE_CONSTANTS__BUT_ANOTHER_MAY_USE_SOME_OF_THE_CONSTANTS._WHAT_IS_THE_BEST_WAY_TO_UPDATE_THESE___"></span>I am sharing constant buffers between different shaders.</span></span> <span data-ttu-id="b439f-171">Один шейдер может использовать все константы, но другой может использовать некоторые константы.</span><span class="sxs-lookup"><span data-stu-id="b439f-171">One shader may use all of the constants, but another may use some of the constants.</span></span> <span data-ttu-id="b439f-172">Как лучше всего обновлять эти данные?</span><span class="sxs-lookup"><span data-stu-id="b439f-172">What is the best way to update these?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-173">Один из подходов состоит в том, чтобы разделить буфер констант еще дальше.</span><span class="sxs-lookup"><span data-stu-id="b439f-173">One approach is to split the constant buffer even further.</span></span> <span data-ttu-id="b439f-174">Однако имеется точка, в которой привязано слишком много буферов констант.</span><span class="sxs-lookup"><span data-stu-id="b439f-174">However, there comes a point at which too many constant buffers are bound.</span></span> <span data-ttu-id="b439f-175">В этом случае переместите константы, которые, скорее всего, не будут использоваться несколькими шейдерами, в конец буфера констант.</span><span class="sxs-lookup"><span data-stu-id="b439f-175">In this case, move the constants that are likely to be unused by several shaders to the end of the constant buffer.</span></span> <span data-ttu-id="b439f-176">При получении данных переменной из шейдера используйте \_ флаг D3D10 SVF \_ из \_ переменной D3D10 шейдера \_ DESC, \_ чтобы определить, используется ли переменная.</span><span class="sxs-lookup"><span data-stu-id="b439f-176">When getting the variable data from the shader, use the D3D10\_SVF\_USED flag from the D3D10\_SHADER\_VARIABLE\_DESC to determine if the variable is used.</span></span> <span data-ttu-id="b439f-177">Поместив неиспользуемые переменные в конец буфера констант, можно привязать меньший буфер к шейдеру, который не использует эти переменные, тем самым сохраняя стоимость обновления.</span><span class="sxs-lookup"><span data-stu-id="b439f-177">By placing unused variables at the end of the constant buffer, you can bind a smaller buffer to the shader that does not use these variables, thus saving the update cost.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>Сколько я могу улучшить свою частоту кадров, если только я загрузил кости моего знака один раз для каждого кадра, а не один раз для каждого прохода или рисования?</span><span class="sxs-lookup"><span data-stu-id="b439f-178"><span id="How_much_can_I_improve_my_frame_rate_if_I_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="how_much_can_i_improve_my_frame_rate_if_i_only_upload_my_character_s_bones_once_per_frame_instead_of_once_per_pass_draw___"></span><span id="HOW_MUCH_CAN_I_IMPROVE_MY_FRAME_RATE_IF_I_ONLY_UPLOAD_MY_CHARACTER_S_BONES_ONCE_PER_FRAME_INSTEAD_OF_ONCE_PER_PASS_DRAW___"></span>How much can I improve my frame rate if I only upload my character's bones once per frame instead of once per pass/draw?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-179">Можно увеличить частоту кадров в диапазоне от 8 до 50 процентов в зависимости от объема избыточных данных.</span><span class="sxs-lookup"><span data-stu-id="b439f-179">You can improve frame rate between 8 percent and 50 percent depending on the amount of redundant data.</span></span> <span data-ttu-id="b439f-180">В худшем случае производительность не будет снижена.</span><span class="sxs-lookup"><span data-stu-id="b439f-180">In the worst case, performance will not be reduced.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>Сколько буферов констант следует привязать сразу?</span><span class="sxs-lookup"><span data-stu-id="b439f-181"><span id="How_many_constant_buffers_should_I_have_bound_at_once__"></span><span id="how_many_constant_buffers_should_i_have_bound_at_once__"></span><span id="HOW_MANY_CONSTANT_BUFFERS_SHOULD_I_HAVE_BOUND_AT_ONCE__"></span>How many constant buffers should I have bound at once?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-182">Привяжите минимальное число буферов констант, необходимое для получения всех данных в шейдер.</span><span class="sxs-lookup"><span data-stu-id="b439f-182">Bind the minimum number of constant buffers it takes to get all of your data into the shader.</span></span> <span data-ttu-id="b439f-183">В реалистичном сценарии для использования рекомендуется использовать пять буферов констант.</span><span class="sxs-lookup"><span data-stu-id="b439f-183">In a realistic scenario, five is the recommended number of constant buffers to use.</span></span> <span data-ttu-id="b439f-184">Предоставление общего доступа к постоянным буферам между шейдерами (привязка одного и того же CB к VS и PS) также может повысить производительность.</span><span class="sxs-lookup"><span data-stu-id="b439f-184">Sharing constant buffers between shaders (binding the same CB to the VS and PS) also can improve performance.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Существуют ли затраты на связывание буферов констант без их использования?</span><span class="sxs-lookup"><span data-stu-id="b439f-185"><span id="Is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="is_there_a_cost_for_binding_constant_buffers_without_using_them__"></span><span id="IS_THERE_A_COST_FOR_BINDING_CONSTANT_BUFFERS_WITHOUT_USING_THEM__"></span>Is there a cost for binding constant buffers without using them?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-186">Да, если вы не собираетесь использовать буфер, не вызывайте Вссетконсантбуффер или Пссетконстантбуффер.</span><span class="sxs-lookup"><span data-stu-id="b439f-186">Yes, if you are not actually going to use the buffer, then do not call VSSetConsantBuffer or PSSetConstantBuffer.</span></span> <span data-ttu-id="b439f-187">Эти дополнительные издержки на API могут сложиться в рамках нескольких вызовов Draw.</span><span class="sxs-lookup"><span data-stu-id="b439f-187">This extra API overhead can add up over the course of multiple draw calls.</span></span>

</dd> </dl>

## <a name="state"></a><span data-ttu-id="b439f-188">Состояние</span><span class="sxs-lookup"><span data-stu-id="b439f-188">State</span></span>

<dl> <dt>

<span data-ttu-id="b439f-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>Каков лучший способ управления состоянием в D3D10?</span><span class="sxs-lookup"><span data-stu-id="b439f-189"><span id="What_is_the_best_way_to_manage_state_in_D3D10___"></span><span id="what_is_the_best_way_to_manage_state_in_d3d10___"></span><span id="WHAT_IS_THE_BEST_WAY_TO_MANAGE_STATE_IN_D3D10___"></span>What is the best way to manage state in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-190">Лучшим решением является знание всех состояний на передний план и создание объектов состояния на передний план.</span><span class="sxs-lookup"><span data-stu-id="b439f-190">The best solution is to know all of your state up front and to create the state objects up front.</span></span> <span data-ttu-id="b439f-191">Это означает, что во время визуализации привязка состояния является единственной операцией, которая должна быть выполнена.</span><span class="sxs-lookup"><span data-stu-id="b439f-191">This means that at render time, state binding is the only operation that needs to happen.</span></span> <span data-ttu-id="b439f-192">D3D10 также отфильтровывает дубликаты.</span><span class="sxs-lookup"><span data-stu-id="b439f-192">D3D10 also filter outs duplicates.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>Моя игра загружена динамически или содержит содержимое, созданное пользователем.</span><span class="sxs-lookup"><span data-stu-id="b439f-193"><span id="My_game_has_dynamically_loaded_or_has_user-generated_content._I_cannot_load_all_of_my_state_objects_up_front._What_should_I_do___"></span><span id="my_game_has_dynamically_loaded_or_has_user-generated_content._i_cannot_load_all_of_my_state_objects_up_front._what_should_i_do___"></span><span id="MY_GAME_HAS_DYNAMICALLY_LOADED_OR_HAS_USER-GENERATED_CONTENT._I_CANNOT_LOAD_ALL_OF_MY_STATE_OBJECTS_UP_FRONT._WHAT_SHOULD_I_DO___"></span>My game has dynamically loaded or has user-generated content.</span></span> <span data-ttu-id="b439f-194">Не удается загрузить все объекты состояния впереди.</span><span class="sxs-lookup"><span data-stu-id="b439f-194">I cannot load all of my state objects up front.</span></span> <span data-ttu-id="b439f-195">  Что следует делать?</span><span class="sxs-lookup"><span data-stu-id="b439f-195">What should I do?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-196">Здесь есть два решения.</span><span class="sxs-lookup"><span data-stu-id="b439f-196">There are two solutions here.</span></span> <span data-ttu-id="b439f-197">Первый — просто создать объекты состояния на лету и позволить D3D10 отфильтровать дубликаты.</span><span class="sxs-lookup"><span data-stu-id="b439f-197">The first is to just create state objects on the fly and to let D3D10 filter out duplicates.</span></span> <span data-ttu-id="b439f-198">Однако это не рекомендуется для сценариев с множеством изменений объектов состояния на кадр.</span><span class="sxs-lookup"><span data-stu-id="b439f-198">This, however, is not recommended for scenarios with many state object changes per frame.</span></span> <span data-ttu-id="b439f-199">Лучшее решение заключается в том, чтобы вручную хэшировать объекты состояния и создавать объекты состояния, только если в хэш-таблице не найден соответствующий требованиям.</span><span class="sxs-lookup"><span data-stu-id="b439f-199">A better solution is to hash the state objects yourself and to create a state object only if one that fits the requirements is not found in the hash table.</span></span> <span data-ttu-id="b439f-200">Причиной использования пользовательской хэш-таблицы является то, что приложение может выбрать быстрый хэш на основе сценария использования, определенного для этого приложения.</span><span class="sxs-lookup"><span data-stu-id="b439f-200">The reasoning behind using a custom hash table is that an application can select a fast hash based upon the usage scenario particular to that application.</span></span> <span data-ttu-id="b439f-201">Например, если приложение изменяет только рендертаржетвритемаск в Блендстате и сохраняет все остальные значения, приложение может создать хэш из рендертаржетвритемаск, а не всю структуру.</span><span class="sxs-lookup"><span data-stu-id="b439f-201">For example, if an application only changes the rendertargetwritemask in the BlendState and keeps all other values the same, the application can generate a hash from the rendertargetwritemask instead of the entire structure.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>Состояние Алфатест.</span><span class="sxs-lookup"><span data-stu-id="b439f-202"><span id="AlphaTest_state_is_gone._Where_did_it_go___"></span><span id="alphatest_state_is_gone._where_did_it_go___"></span><span id="ALPHATEST_STATE_IS_GONE._WHERE_DID_IT_GO___"></span>AlphaTest state is gone.</span></span> <span data-ttu-id="b439f-203">Куда она пойдет?</span><span class="sxs-lookup"><span data-stu-id="b439f-203">Where did it go?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-204">Алфатест теперь должен быть производительностью шейдера.</span><span class="sxs-lookup"><span data-stu-id="b439f-204">AlphaTest now should be performance in the shader.</span></span> <span data-ttu-id="b439f-205">См. пример Фикседфунцему.</span><span class="sxs-lookup"><span data-stu-id="b439f-205">See the FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>Что случилось с пользовательскими роликами?</span><span class="sxs-lookup"><span data-stu-id="b439f-206"><span id="What_happened_to_user_clip_planes___"></span><span id="what_happened_to_user_clip_planes___"></span><span id="WHAT_HAPPENED_TO_USER_CLIP_PLANES___"></span>What happened to user clip planes?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-207">Ролики пользователя были перемещены в шейдер.</span><span class="sxs-lookup"><span data-stu-id="b439f-207">User clip planes have moved into the shader.</span></span> <span data-ttu-id="b439f-208">Это можно решить двумя способами.</span><span class="sxs-lookup"><span data-stu-id="b439f-208">There are two ways to handle this.</span></span> <span data-ttu-id="b439f-209">Первый — вывод SV \_ клипдистанце из шейдера вершин или шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="b439f-209">The first is to output SV\_ClipDistance from the vertex shader or the geometry shader.</span></span> <span data-ttu-id="b439f-210">Другой вариант — использовать параметр «отбросить» в шейдере пикселей в зависимости от значения, переданного с помощью шейдера вершин или шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="b439f-210">The other option is to use discard in the pixel shader based upon some value passed down by the vertex shader or the geometry shader.</span></span> <span data-ttu-id="b439f-211">Поэкспериментируйте с обоими, чтобы узнать, какой из них быстрее в вашем конкретном сценарии.</span><span class="sxs-lookup"><span data-stu-id="b439f-211">Experiment with both to see which is faster for your particular scenario.</span></span> <span data-ttu-id="b439f-212">Использование SV \_ клипдистанце может привести к тому, что оборудование будет использовать подпрограмму отсечения, основанную на геометрии, которая может привести к более медленному запуску вызовов рисования геометрических границ.</span><span class="sxs-lookup"><span data-stu-id="b439f-212">Using SV\_ClipDistance could cause the hardware to use a geometry-based clipping routine that may cause geometry bound draw calls to run slower.</span></span> <span data-ttu-id="b439f-213">Аналогично, использование функции «отмена» сдвигает работу на шейдер пикселей, что может привести к более медленному выполнению вызовов рисования, привязанных к пикселю.</span><span class="sxs-lookup"><span data-stu-id="b439f-213">Likewise, using discard shifts the work to the pixel shader, which may cause pixel-bound draw calls to run slower.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Снятые флажки не учитывают параметры состояния, такие как параметры прямоугольного Rect в своем состоянии средства программной прорисовки.</span><span class="sxs-lookup"><span data-stu-id="b439f-214"><span id="Clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_Rasterizer_State.__"></span><span id="clears_do_not_respect_any_state_settings__such_as_my_scissor_rect_settings_in_my_rasterizer_state.__"></span><span id="CLEARS_DO_NOT_RESPECT_ANY_STATE_SETTINGS__SUCH_AS_MY_SCISSOR_RECT_SETTINGS_IN_MY_RASTERIZER_STATE.__"></span>Clears do not respect any state settings, such as my scissor rect settings in my Rasterizer State.</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-215">Очистки были отделены от состояния конвейера.</span><span class="sxs-lookup"><span data-stu-id="b439f-215">Clears have been separated from the pipeline state.</span></span> <span data-ttu-id="b439f-216">Чтобы получить поведение в стиле D3D9, нужно эмулировать очистку, выполняя четыре экрана.</span><span class="sxs-lookup"><span data-stu-id="b439f-216">In order to get D3D9-style behavior, emulate clears by drawing a full-screen quad.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>Я установил для моих состояний значение по умолчанию, чтобы попробовать и диагностировать ошибку отрисовки.</span><span class="sxs-lookup"><span data-stu-id="b439f-217"><span id="I_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._Now_my_screen_just_shows_black__although_I_know_I_am_drawing_objects_onto_the_screen.__"></span><span id="i_set_my_states_back_to_default_to_try_and_diagnose_a_rendering_error._now_my_screen_just_shows_black__although_i_know_i_am_drawing_objects_onto_the_screen.__"></span><span id="I_SET_MY_STATES_BACK_TO_DEFAULT_TO_TRY_AND_DIAGNOSE_A_RENDERING_ERROR._NOW_MY_SCREEN_JUST_SHOWS_BLACK__ALTHOUGH_I_KNOW_I_AM_DRAWING_OBJECTS_ONTO_THE_SCREEN.__"></span>I set my states back to default to try and diagnose a rendering error.</span></span> <span data-ttu-id="b439f-218">Теперь на экране отображается черный цвет, хотя я могу понять, что на экране рисуются объекты.</span><span class="sxs-lookup"><span data-stu-id="b439f-218">Now my screen just shows black, although I know I am drawing objects onto the screen.</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-219">При установке состояния обратно в значения по умолчанию (NULL) убедитесь, что Самплемаск в вызове Омсетблендстате никогда не равен нулю.</span><span class="sxs-lookup"><span data-stu-id="b439f-219">When setting state back to default values (NULL), ensure that the SampleMask in the call to OMSetBlendState is never zero.</span></span> <span data-ttu-id="b439f-220">Если Самплемаск имеет значение 0, то все примеры логически и с нулевым значением.</span><span class="sxs-lookup"><span data-stu-id="b439f-220">If SampleMask is set to zero, then all samples will logically AND with zero.</span></span> <span data-ttu-id="b439f-221">В этом случае ни один из примеров не будет проходить тест Blend.</span><span class="sxs-lookup"><span data-stu-id="b439f-221">In this scenario, no samples will pass the blend test.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Куда D3DSAMP \_ состояние сргбтекстуреа?</span><span class="sxs-lookup"><span data-stu-id="b439f-222"><span id="Where_did_the_D3DSAMP_SRGBTEXTURE_state_go___"></span><span id="where_did_the_d3dsamp_srgbtexture_state_go___"></span><span id="WHERE_DID_THE_D3DSAMP_SRGBTEXTURE_STATE_GO___"></span>Where did the D3DSAMP\_SRGBTEXTURE state go?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-223">SRGB был удален как часть состояния образца и теперь привязан к формату текстуры.</span><span class="sxs-lookup"><span data-stu-id="b439f-223">SRGB was removed as part of the sampler state and now is tied to the texture format.</span></span> <span data-ttu-id="b439f-224">Привязка текстуры SRGB приведет к той же выборки, которая будет возникать, если вы указали D3DSAMP \_ сргбтекстуре в Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="b439f-224">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> </dl>

## <a name="formats"></a><span data-ttu-id="b439f-225">Форматы</span><span class="sxs-lookup"><span data-stu-id="b439f-225">Formats</span></span>

<dl> <dt>

<span data-ttu-id="b439f-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Какой формат D3D9 соответствует формату D3D10?</span><span class="sxs-lookup"><span data-stu-id="b439f-226"><span id="Which_D3D9_format_corresponds_to_which_D3D10_format___"></span><span id="which_d3d9_format_corresponds_to_which_d3d10_format___"></span><span id="WHICH_D3D9_FORMAT_CORRESPONDS_TO_WHICH_D3D10_FORMAT___"></span>Which D3D9 format corresponds to which D3D10 format?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-227">Дополнительные сведения см. [в статье требования Direct3D 9 к Direct3D 10](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).</span><span class="sxs-lookup"><span data-stu-id="b439f-227">For info, see [Direct3D 9 to Direct3D 10 Considerations](/windows/desktop/direct3d10/d3d10-graphics-programming-guide-d3d9-to-d3d10-considerations).</span></span>

</dd> <dt>

<span data-ttu-id="b439f-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>Что случилось с форматами текстур A8R8G8B8?</span><span class="sxs-lookup"><span data-stu-id="b439f-228"><span id="What_happened_to_A8R8G8B8_texture_formats___"></span><span id="what_happened_to_a8r8g8b8_texture_formats___"></span><span id="WHAT_HAPPENED_TO_A8R8G8B8_TEXTURE_FORMATS___"></span>What happened to A8R8G8B8 texture formats?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-229">Они являются устаревшими в D3D10.</span><span class="sxs-lookup"><span data-stu-id="b439f-229">They have been deprecated in D3D10.</span></span> <span data-ttu-id="b439f-230">Вы можете повторно источникировать текстуры как R8G8B8A8 или свиззле по нагрузке или свиззле в шейдере.</span><span class="sxs-lookup"><span data-stu-id="b439f-230">You can re-source your textures as R8G8B8A8, or you can swizzle on load, or you can swizzle in the shader.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>Разделы справки использовать текстуры палеттизед?</span><span class="sxs-lookup"><span data-stu-id="b439f-231"><span id="How_do_I_use_palettized_textures___"></span><span id="how_do_i_use_palettized_textures___"></span><span id="HOW_DO_I_USE_PALETTIZED_TEXTURES___"></span>How do I use palettized textures?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-232">Поместите цветовую палитру в текстуру или буфер констант и привяжите ее к конвейеру.</span><span class="sxs-lookup"><span data-stu-id="b439f-232">Place your color palette in a texture or a constant buffer and bind it to the pipeline.</span></span> <span data-ttu-id="b439f-233">В шейдере пикселей выполните косвенный Просмотр с помощью индекса в текстуре палеттизед.</span><span class="sxs-lookup"><span data-stu-id="b439f-233">In the pixel shader do an indirect lookup using the index in your palettized texture.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>Что такое новые форматы SRGB?</span><span class="sxs-lookup"><span data-stu-id="b439f-234"><span id="What_are_these_new_SRGB_formats___"></span><span id="what_are_these_new_srgb_formats___"></span><span id="WHAT_ARE_THESE_NEW_SRGB_FORMATS___"></span>What are these new SRGB formats?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-235">SRGB был удален как часть состояния образца и теперь привязан к формату текстуры.</span><span class="sxs-lookup"><span data-stu-id="b439f-235">SRGB was removed as part of the sampler state and is now tied to the texture format.</span></span> <span data-ttu-id="b439f-236">Привязка текстуры SRGB приведет к той же выборки, которая будет возникать, если вы указали D3DSAMP \_ сргбтекстуре в Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="b439f-236">Binding an SRGB texture will result in the same sampling you would get if you specified D3DSAMP\_SRGBTEXTURE in Direct3D 9.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Где находятся вентиляторы треугольника?</span><span class="sxs-lookup"><span data-stu-id="b439f-237"><span id="Where_did_triangle_fans_go___"></span><span id="where_did_triangle_fans_go___"></span><span id="WHERE_DID_TRIANGLE_FANS_GO___"></span>Where did triangle fans go?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-238">Треугольные вентиляторы не рекомендуются в D3D10.</span><span class="sxs-lookup"><span data-stu-id="b439f-238">Triangle fans have been deprecated in D3D10.</span></span> <span data-ttu-id="b439f-239">Вентиляторы треугольника необходимо преобразовать в конвейер содержимого или при загрузке.</span><span class="sxs-lookup"><span data-stu-id="b439f-239">Triangle fans will need to be converted either in the content pipeline or on load.</span></span>

</dd> </dl>

## <a name="shader-linkage"></a><span data-ttu-id="b439f-240">Компоновка шейдера</span><span class="sxs-lookup"><span data-stu-id="b439f-240">Shader Linkage</span></span>

<dl> <dt>

<span data-ttu-id="b439f-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>Мои шейдеры Direct3D 9 прекрасно компилируются в модель шейдера 4,0, но, когда я привязал их к конвейеру, я получаю ошибки компоновки, которые отображаются в отладочном выводе с помощью отладочной среды выполнения.</span><span class="sxs-lookup"><span data-stu-id="b439f-241"><span id="My_Direct3D_9_shaders_compile_fine_to_Shader_Model_4.0__but_when_I_bind_them_to_the_pipeline__I_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="my_direct3d_9_shaders_compile_fine_to_shader_model_4.0__but_when_i_bind_them_to_the_pipeline__i_get_linkage_errors_showing_up_in_the_debug_output_with_the_debug_runtime.__"></span><span id="MY_DIRECT3D_9_SHADERS_COMPILE_FINE_TO_SHADER_MODEL_4.0__BUT_WHEN_I_BIND_THEM_TO_THE_PIPELINE__I_GET_LINKAGE_ERRORS_SHOWING_UP_IN_THE_DEBUG_OUTPUT_WITH_THE_DEBUG_RUNTIME.__"></span>My Direct3D 9 shaders compile fine to Shader Model 4.0, but when I bind them to the pipeline, I get linkage errors showing up in the debug output with the debug runtime.</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-242">Компоновка шейдера является намного более строгой в D3D10.</span><span class="sxs-lookup"><span data-stu-id="b439f-242">Shader linkage is much stricter in D3D10.</span></span> <span data-ttu-id="b439f-243">Элементы на следующем этапе должны считываться в том порядке, в котором они выводятся на предыдущем этапе.</span><span class="sxs-lookup"><span data-stu-id="b439f-243">Elements in a subsequent stage must be read in the order they are output from the previous stage.</span></span> <span data-ttu-id="b439f-244">Пример:</span><span class="sxs-lookup"><span data-stu-id="b439f-244">For example:</span></span>

<span data-ttu-id="b439f-245">Выходные данные шейдера вершин:</span><span class="sxs-lookup"><span data-stu-id="b439f-245">A vertex shader outputs:</span></span>

``` syntax
    float4 Pos  : SV_POSITION;
    float3 Norm : NORMAL;
    float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="b439f-246">Построитель текстуры считывает в:</span><span class="sxs-lookup"><span data-stu-id="b439f-246">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="b439f-247">Хотя в шейдере пикселей это не требуется, это вызовет ошибку компоновки, так как расположение выводится из шейдера вершин, но не считывается шейдером пикселей.</span><span class="sxs-lookup"><span data-stu-id="b439f-247">Although the position is not needed in the pixel shader, this will cause a linkage error, because position is being output from the vertex shader, but not read by the pixel shader.</span></span> <span data-ttu-id="b439f-248">Более правильная версия будет выглядеть следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b439f-248">The more correct version would look like this:</span></span>

<span data-ttu-id="b439f-249">Выходные данные шейдера вершин:</span><span class="sxs-lookup"><span data-stu-id="b439f-249">A vertex shader outputs:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
        float4 Pos  : SV_POSITION;
```

<span data-ttu-id="b439f-250">Построитель текстуры считывает в:</span><span class="sxs-lookup"><span data-stu-id="b439f-250">A pixel shader reads in:</span></span>

``` syntax
        float3 Norm : NORMAL;
        float2 Tex  : TEXCOORD0;
```

<span data-ttu-id="b439f-251">В этом случае шейдер вершин выводит одну и ту же информацию, но теперь шейдер пикселей считывает элементы в выходных данных заказа.</span><span class="sxs-lookup"><span data-stu-id="b439f-251">In this case, the vertex shader is outputting the same information, but now the pixel shader is reading things in the order output.</span></span> <span data-ttu-id="b439f-252">Поскольку построитель текстуры не читается что-то после Да, нам не нужно беспокоиться о том, чтобы в VS выводиться больше информации, чем при считывании PS.</span><span class="sxs-lookup"><span data-stu-id="b439f-252">Because the pixel shader is not reading anything after Tex, we do not have to worry that the VS is outputting more information than the PS is reading.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>Для создания макета ввода требуется подпись шейдера, но перед созданием шейдеров необходимо загрузить сетки и создать макеты.</span><span class="sxs-lookup"><span data-stu-id="b439f-253"><span id="I_need_a_shader_signature_in_order_to_create_an_Input_Layout__but_I_load_my_meshes_and_create_layouts_before_creating_shaders._What_do_I_do___"></span><span id="i_need_a_shader_signature_in_order_to_create_an_input_layout__but_i_load_my_meshes_and_create_layouts_before_creating_shaders._what_do_i_do___"></span><span id="I_NEED_A_SHADER_SIGNATURE_IN_ORDER_TO_CREATE_AN_INPUT_LAYOUT__BUT_I_LOAD_MY_MESHES_AND_CREATE_LAYOUTS_BEFORE_CREATING_SHADERS._WHAT_DO_I_DO___"></span>I need a shader signature in order to create an Input Layout, but I load my meshes and create layouts before creating shaders.</span></span> <span data-ttu-id="b439f-254">Что делать?</span><span class="sxs-lookup"><span data-stu-id="b439f-254">What do I do?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-255">Одним из решений является переключение параметров Order и Load перед загрузкой сеток.</span><span class="sxs-lookup"><span data-stu-id="b439f-255">One solution is to switch the order and load shaders before loading meshes.</span></span> <span data-ttu-id="b439f-256">Однако это гораздо проще сказать, чем это сделано.</span><span class="sxs-lookup"><span data-stu-id="b439f-256">However, this is much easier said than done.</span></span> <span data-ttu-id="b439f-257">Вы всегда можете создать входные макеты по запросу, если это необходимо для приложения.</span><span class="sxs-lookup"><span data-stu-id="b439f-257">You always can create the Input Layouts on demand when needed by the application.</span></span> <span data-ttu-id="b439f-258">Вам потребуется использовать версию сигнатуры шейдера.</span><span class="sxs-lookup"><span data-stu-id="b439f-258">You will have to keep a version of the shader signature around.</span></span> <span data-ttu-id="b439f-259">Необходимо создать хэш, основанный на шейдере и макете буфера, и создать только входной макет, если тот, который соответствует, еще не существует.</span><span class="sxs-lookup"><span data-stu-id="b439f-259">You should create a hash based off of the shader and buffer layout, and only create the Input Layout if one that matches does not exist already.</span></span>

</dd> </dl>

## <a name="draw-calls"></a><span data-ttu-id="b439f-260">Вызовы Draw</span><span class="sxs-lookup"><span data-stu-id="b439f-260">Draw Calls</span></span>

<dl> <dt>

<span data-ttu-id="b439f-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>Каково ограничение на вызовы Draw для D3D10 до 60 Гц?</span><span class="sxs-lookup"><span data-stu-id="b439f-261"><span id="What_is_my_limit_on_draw_calls_for_D3D10_to_reach_60_Hz__30_Hz___"></span><span id="what_is_my_limit_on_draw_calls_for_d3d10_to_reach_60_hz__30_hz___"></span><span id="WHAT_IS_MY_LIMIT_ON_DRAW_CALLS_FOR_D3D10_TO_REACH_60_HZ__30_HZ___"></span>What is my limit on draw calls for D3D10 to reach 60 Hz?</span></span> <span data-ttu-id="b439f-262">30 Гц?</span><span class="sxs-lookup"><span data-stu-id="b439f-262">30 Hz?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-263">Direct3D 9 имел ограничение на количество вызовов Draw из-за стоимости ЦП на вызов Draw.</span><span class="sxs-lookup"><span data-stu-id="b439f-263">Direct3D 9 had a limitation on the number of draw calls because of the CPU cost per draw call.</span></span> <span data-ttu-id="b439f-264">В Direct3D 10 стоимость каждого вызова Draw уменьшилась.</span><span class="sxs-lookup"><span data-stu-id="b439f-264">On Direct3D 10, the cost of each draw call has been reduced.</span></span> <span data-ttu-id="b439f-265">Однако больше не существует определенной корреляции между вызовами рисования и частотой кадров.</span><span class="sxs-lookup"><span data-stu-id="b439f-265">However, there is no longer a definite correlation between draw calls and frame rates.</span></span> <span data-ttu-id="b439f-266">Поскольку вызовы Draw часто потребовали много обращений в службу поддержки (обновления буфера констант, привязки текстур, настройки состояния и т. д.), воздействие частоты кадров API теперь более зависит от общего использования API, а не просто выводит число вызовов.</span><span class="sxs-lookup"><span data-stu-id="b439f-266">Because draw calls often require many support calls ( constant buffer updates, texture bindings, state setting, and so on) the frame rate impact of the API is now more dependent on the overall API usage as opposed to simply draw call counts.</span></span>

</dd> </dl>

## <a name="resources"></a><span data-ttu-id="b439f-267">Ресурсы</span><span class="sxs-lookup"><span data-stu-id="b439f-267">Resources</span></span>

<dl> <dt>

<span data-ttu-id="b439f-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>Какой тип использования ресурсов следует использовать для каких операций?</span><span class="sxs-lookup"><span data-stu-id="b439f-268"><span id="What_resource_usage_type_should_I_use_for_what_operations___"></span><span id="what_resource_usage_type_should_i_use_for_what_operations___"></span><span id="WHAT_RESOURCE_USAGE_TYPE_SHOULD_I_USE_FOR_WHAT_OPERATIONS___"></span>What resource usage type should I use for what operations?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-269">Используйте следующий Памятка по-лист:</span><span class="sxs-lookup"><span data-stu-id="b439f-269">Use the following cheat-sheet:</span></span>

-   <span data-ttu-id="b439f-270">ЦП обновляет ресурс более одного раза в кадре: D3D10 \_ использование \_ dynamic.</span><span class="sxs-lookup"><span data-stu-id="b439f-270">The CPU updates the resource more than once per frame: D3D10\_USAGE\_DYNAMIC</span></span>
-   <span data-ttu-id="b439f-271">ЦП обновляет ресурс менее одного раза в кадре: D3D10 \_ использование \_ по умолчанию</span><span class="sxs-lookup"><span data-stu-id="b439f-271">The CPU updates the resource less than once per frame: D3D10\_USAGE\_DEFAULT</span></span>
-   <span data-ttu-id="b439f-272">ЦП не обновляет ресурс: D3D10 \_ Usage \_ неизменяемый</span><span class="sxs-lookup"><span data-stu-id="b439f-272">The CPU does not update the resource: D3D10\_USAGE\_IMMUTABLE</span></span>
-   <span data-ttu-id="b439f-273">ЦП должен прочитать ресурс: D3D10 \_ использование \_ промежуточного хранения</span><span class="sxs-lookup"><span data-stu-id="b439f-273">The CPU needs to read the resource: D3D10\_USAGE\_STAGING</span></span>

<span data-ttu-id="b439f-274">Так как постоянные буферы всегда предназначены для регулярного обновления, они не соответствуют "Памятка по-Sheet".</span><span class="sxs-lookup"><span data-stu-id="b439f-274">Because constant buffers are always meant to be update frequently, they do not conform to the "cheat-sheet."</span></span> <span data-ttu-id="b439f-275">Сведения о типах ресурсов, используемых для буферов констант, см. в разделе [постоянные буферы](#constant-buffers) .</span><span class="sxs-lookup"><span data-stu-id="b439f-275">For which resource types to use for constant buffers, see the [Constant Buffers](#constant-buffers) section.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>Что случилось с Дравпримитивеуп и Дравиндекседпримитивеуп?</span><span class="sxs-lookup"><span data-stu-id="b439f-276"><span id="What_happened_to_DrawPrimitiveUP_and_DrawIndexedPrimitiveUP___"></span><span id="what_happened_to_drawprimitiveup_and_drawindexedprimitiveup___"></span><span id="WHAT_HAPPENED_TO_DRAWPRIMITIVEUP_AND_DRAWINDEXEDPRIMITIVEUP___"></span>What happened to DrawPrimitiveUP and DrawIndexedPrimitiveUP?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-277">Они исчезают в D3D10.</span><span class="sxs-lookup"><span data-stu-id="b439f-277">They are gone in D3D10.</span></span> <span data-ttu-id="b439f-278">Для динамической геометрии используйте динамический буфер D3D10 большого объема \_ использования \_ .</span><span class="sxs-lookup"><span data-stu-id="b439f-278">For dynamic geometry use a large D3D10\_USAGE\_DYNAMIC buffer.</span></span> <span data-ttu-id="b439f-279">В начале кадра сопоставьте его с D3D10ной \_ \_ записью \_ отказа в карте.</span><span class="sxs-lookup"><span data-stu-id="b439f-279">At the beginning of the frame, map it with D3D10\_MAP\_WRITE\_DISCARD.</span></span> <span data-ttu-id="b439f-280">Для каждого последующего вызова Draw измените указатель записи после позиции ранее рисуемых вершин и сопоставьте буфер с D3D10 \_ Map \_ \_ не \_ перезаписывает.</span><span class="sxs-lookup"><span data-stu-id="b439f-280">For each subsequent draw call advance the write pointer past the position of the previously drawn vertices and map the buffer with D3D10\_MAP\_WRITE\_NO\_OVERWRITE.</span></span> <span data-ttu-id="b439f-281">Если ближе к концу буфера перед концом кадра, заключите указатель записи в начало и карту с D3D10ом \_ записи в Map \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="b439f-281">If you near the end of the buffer before the end of the frame, wrap the write pointer around to the beginning and map with D3D10\_MAP\_WRITE\_DISCARD.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Можно ли записывать 16-битные индексы и 32-битовые индексы в один и тот же динамический буфер Geometry?</span><span class="sxs-lookup"><span data-stu-id="b439f-282"><span id="Can_I_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="can_i_write_16-bit_indices_and_32-bit_indices_into_the_same_dynamic_geometry_buffer___"></span><span id="CAN_I_WRITE_16-BIT_INDICES_AND_32-BIT_INDICES_INTO_THE_SAME_DYNAMIC_GEOMETRY_BUFFER___"></span>Can I write 16-bit indices and 32-bit indices into the same dynamic geometry buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-283">Да, можно, но это может привести к снижению производительности на определенном оборудовании.</span><span class="sxs-lookup"><span data-stu-id="b439f-283">Yes, you can, but this can incur a performance penalty on certain hardware.</span></span> <span data-ttu-id="b439f-284">Можно более безопасно создавать отдельные буферы для динамических 16-битных данных индекса и 32-битных индексных данных.</span><span class="sxs-lookup"><span data-stu-id="b439f-284">It is a safer to create separate buffers for dynamic 16-bit index data and 32-bit index data.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>Разделы справки считать данные из GPU в ЦП?</span><span class="sxs-lookup"><span data-stu-id="b439f-285"><span id="How_do_I_read_data_back_from_the_GPU_to_the_CPU___"></span><span id="how_do_i_read_data_back_from_the_gpu_to_the_cpu___"></span><span id="HOW_DO_I_READ_DATA_BACK_FROM_THE_GPU_TO_THE_CPU___"></span>How do I read data back from the GPU to the CPU?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-286">Необходимо использовать промежуточный ресурс.</span><span class="sxs-lookup"><span data-stu-id="b439f-286">You must use a staging resource.</span></span> <span data-ttu-id="b439f-287">Скопируйте данные из ресурса GPU в промежуточный ресурс с помощью Копиресаурце.</span><span class="sxs-lookup"><span data-stu-id="b439f-287">Copy the data from the GPU resource to the staging resource using CopyResource.</span></span> <span data-ttu-id="b439f-288">Сопоставьте промежуточный ресурс для чтения данных.</span><span class="sxs-lookup"><span data-stu-id="b439f-288">Map the staging resource to read the data.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>Приложение было зависело от функциональных возможностей Стретчрект.</span><span class="sxs-lookup"><span data-stu-id="b439f-289"><span id="My_application_was_dependent_on_StretchRect_functionality.__"></span><span id="my_application_was_dependent_on_stretchrect_functionality.__"></span><span id="MY_APPLICATION_WAS_DEPENDENT_ON_STRETCHRECT_FUNCTIONALITY.__"></span>My application was dependent on StretchRect functionality.</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-290">Поскольку это является, по сути, оболочкой для базовых функций Direct3D, она была удалена из API.</span><span class="sxs-lookup"><span data-stu-id="b439f-290">Because this was essentially a wrapper for basic Direct3D functionality, it was removed from the API.</span></span> <span data-ttu-id="b439f-291">Некоторые функции Стретчрект были перемещены в D3DX10LoadTextureFromTexture.</span><span class="sxs-lookup"><span data-stu-id="b439f-291">Some of the StretchRect functionality was moved into D3DX10LoadTextureFromTexture.</span></span> <span data-ttu-id="b439f-292">Для преобразований формата и копирования текстур D3DX10LoadTextureFromTexture может выполнить задание.</span><span class="sxs-lookup"><span data-stu-id="b439f-292">For format conversions and copying textures, D3DX10LoadTextureFromTexture may do the job.</span></span> <span data-ttu-id="b439f-293">Однако операции, такие как преобразование из одного размера в другой, скорее всего, потребует выполнения операции рендеринга для текстуры в приложении.</span><span class="sxs-lookup"><span data-stu-id="b439f-293">However, operations such as converting from one size to another likely will require a render to texture operation in the application.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>Нет смещений или размеров для вызовов карт для ресурсов.</span><span class="sxs-lookup"><span data-stu-id="b439f-294"><span id="There_are_no_offsets_or_sizes_on_Map_calls_for_resources._These_were_there_on_Lock_calls_on_Direct3D_9__why_did_they_change___"></span><span id="there_are_no_offsets_or_sizes_on_map_calls_for_resources._these_were_there_on_lock_calls_on_direct3d_9__why_did_they_change___"></span><span id="THERE_ARE_NO_OFFSETS_OR_SIZES_ON_MAP_CALLS_FOR_RESOURCES._THESE_WERE_THERE_ON_LOCK_CALLS_ON_DIRECT3D_9__WHY_DID_THEY_CHANGE___"></span>There are no offsets or sizes on Map calls for resources.</span></span> <span data-ttu-id="b439f-295">Это было вызвано вызовами блокировок на Direct3D 9; Почему они изменились?</span><span class="sxs-lookup"><span data-stu-id="b439f-295">These were there on Lock calls on Direct3D 9; why did they change?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-296">Смещения и размеры вызовов блокировок в Direct3D 9, по сути, были перегружены API и часто игнорируются драйвером.</span><span class="sxs-lookup"><span data-stu-id="b439f-296">The offsets and sizes on Lock calls on Direct3D 9 were basically API clutter and often ignored by the driver.</span></span> <span data-ttu-id="b439f-297">Смещение должно рассчитываться приложением из указателя, возвращенного в вызове Map.</span><span class="sxs-lookup"><span data-stu-id="b439f-297">Offsets should be calculated instead by the application from the pointer returned in the Map call.</span></span>

</dd> </dl>

## <a name="depth-as-texture"></a><span data-ttu-id="b439f-298">Глубина как текстура</span><span class="sxs-lookup"><span data-stu-id="b439f-298">Depth as Texture</span></span>

<dl> <dt>

<span data-ttu-id="b439f-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Что быстрее?</span><span class="sxs-lookup"><span data-stu-id="b439f-299"><span id="Which_is_faster__Using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="which_is_faster__using_depth_as_a_texture_or_writing_depth_to_alpha_and_reading_that___"></span><span id="WHICH_IS_FASTER__USING_DEPTH_AS_A_TEXTURE_OR_WRITING_DEPTH_TO_ALPHA_AND_READING_THAT___"></span>Which is faster?</span></span> <span data-ttu-id="b439f-300">Как использовать глубину в качестве текстуры или глубины записи в альфа-канал и считывать их?</span><span class="sxs-lookup"><span data-stu-id="b439f-300">Using depth as a texture or writing depth to alpha and reading that?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-301">Это зависит от приложения и оборудования.</span><span class="sxs-lookup"><span data-stu-id="b439f-301">This is application and hardware specific.</span></span> <span data-ttu-id="b439f-302">Используйте любой из них, чтобы сохранить наибольшую пропускную способность.</span><span class="sxs-lookup"><span data-stu-id="b439f-302">Use whichever one saves the most bandwidth.</span></span> <span data-ttu-id="b439f-303">Если вы уже используете несколько целевых объектов рендеринга и у вас есть дополнительный канал, то более эффективным решением может стать запись глубины из шейдера.</span><span class="sxs-lookup"><span data-stu-id="b439f-303">If you already are using multiple render targets and have an extra channel, then writing depth from the shader may be a better solution.</span></span> <span data-ttu-id="b439f-304">Кроме того, запись глубины в альфа или другой целевой объект прорисовки позволяет создавать линейные значения глубины, которые могут ускорить вычисления, которым требуется доступ к буферу глубины.</span><span class="sxs-lookup"><span data-stu-id="b439f-304">Also, writing depth to alpha or another render target allows you to write linear depth values that may speed up calculations that need to access the depth buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>Можно ли привязать текстуру в качестве входных данных и привязать ее как текстуру трафарета глубины, если отключить запись глубины?</span><span class="sxs-lookup"><span data-stu-id="b439f-305"><span id="Can_I_have_a_texture_bound_as_an_input_AND_bound_as_a_depth-stencil_texture_as_long_as_I_disable_depth_writes___"></span><span id="can_i_have_a_texture_bound_as_an_input_and_bound_as_a_depth-stencil_texture_as_long_as_i_disable_depth_writes___"></span><span id="CAN_I_HAVE_A_TEXTURE_BOUND_AS_AN_INPUT_AND_BOUND_AS_A_DEPTH-STENCIL_TEXTURE_AS_LONG_AS_I_DISABLE_DEPTH_WRITES___"></span>Can I have a texture bound as an input AND bound as a depth-stencil texture as long as I disable depth writes?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-306">Не в D3D10.</span><span class="sxs-lookup"><span data-stu-id="b439f-306">Not in D3D10.</span></span>

</dd> </dl>

## <a name="msaa"></a><span data-ttu-id="b439f-307">MSAA</span><span class="sxs-lookup"><span data-stu-id="b439f-307">MSAA</span></span>

<dl> <dt>

<span data-ttu-id="b439f-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Можно ли разрешить текстуру набора элементов в MSAA с глубиной?</span><span class="sxs-lookup"><span data-stu-id="b439f-308"><span id="Can_I_resolve_an_MSAA_depth-stencil_texture___"></span><span id="can_i_resolve_an_msaa_depth-stencil_texture___"></span><span id="CAN_I_RESOLVE_AN_MSAA_DEPTH-STENCIL_TEXTURE___"></span>Can I resolve an MSAA depth-stencil texture?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-309">Не в D3D10.</span><span class="sxs-lookup"><span data-stu-id="b439f-309">Not in D3D10.</span></span> <span data-ttu-id="b439f-310">Однако можно выполнить выборку отдельных образцов из текстуры MSAA.</span><span class="sxs-lookup"><span data-stu-id="b439f-310">However, you can sample individual samples from the MSAA texture.</span></span> <span data-ttu-id="b439f-311">Дополнительные сведения см. в разделе [HLSL](#hlsl) .</span><span class="sxs-lookup"><span data-stu-id="b439f-311">See the [HLSL](#hlsl) section for details.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Почему происходит сбой моего приложения сразу после включения MSAA?</span><span class="sxs-lookup"><span data-stu-id="b439f-312"><span id="Why_does_my_application_crash_as_soon_as_I_enable_MSAA___"></span><span id="why_does_my_application_crash_as_soon_as_i_enable_msaa___"></span><span id="WHY_DOES_MY_APPLICATION_CRASH_AS_SOON_AS_I_ENABLE_MSAA___"></span>Why does my application crash as soon as I enable MSAA?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-313">Убедитесь, что вы включаете число образцов MSAA и номер качества, которые фактически перечисляются драйвером.</span><span class="sxs-lookup"><span data-stu-id="b439f-313">Ensure you are enabling an MSAA sample count and quality number that actually are enumerated by the driver.</span></span>

</dd> </dl>

## <a name="crashes"></a><span data-ttu-id="b439f-314">Сбои</span><span class="sxs-lookup"><span data-stu-id="b439f-314">Crashes</span></span>

<dl> <dt>

<span data-ttu-id="b439f-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>Мое приложение аварийно завершает работу в D3D10 или в драйвере, и я не знал, почему.</span><span class="sxs-lookup"><span data-stu-id="b439f-315"><span id="My_application_crashes_in_D3D10_or_in_the_driver_and_I_do_not_know_why.__"></span><span id="my_application_crashes_in_d3d10_or_in_the_driver_and_i_do_not_know_why.__"></span><span id="MY_APPLICATION_CRASHES_IN_D3D10_OR_IN_THE_DRIVER_AND_I_DO_NOT_KNOW_WHY.__"></span>My application crashes in D3D10 or in the driver and I do not know why.</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-316">Первым шагом является включение среды выполнения отладки ([**D3D10 \_ CREATE Device флаг \_ \_ отладки**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) , переданный в [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span><span class="sxs-lookup"><span data-stu-id="b439f-316">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="b439f-317">Это позволит вывести наиболее распространенные ошибки как выходные данные отладки.</span><span class="sxs-lookup"><span data-stu-id="b439f-317">This will expose the most common errors as debug output.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX аварийно завершает работу при попытке использовать приложение с ним.</span><span class="sxs-lookup"><span data-stu-id="b439f-318"><span id="PIX_crashes_when_I_try_to_use_my_application_with_it.__"></span><span id="pix_crashes_when_i_try_to_use_my_application_with_it.__"></span><span id="PIX_CRASHES_WHEN_I_TRY_TO_USE_MY_APPLICATION_WITH_IT.__"></span>PIX crashes when I try to use my application with it.</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-319">Первым шагом является включение среды выполнения отладки ([**D3D10 \_ CREATE Device флаг \_ \_ отладки**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) , переданный в [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span><span class="sxs-lookup"><span data-stu-id="b439f-319">The first step is to enable the debug runtime ([**D3D10\_CREATE\_DEVICE\_DEBUG**](/windows/desktop/api/d3d10/ne-d3d10-d3d10_create_device_flag) flag passed into [**D3D10CreateDevice**](/windows/desktop/api/d3d10misc/nf-d3d10misc-d3d10createdevice)).</span></span> <span data-ttu-id="b439f-320">В случае неочистки выходных данных отладки PIX имеет более высокую вероятность сбоя.</span><span class="sxs-lookup"><span data-stu-id="b439f-320">PIX has a much higher probability of crashing if the debug output is not clean.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>Моя игра заканчивается виртуальным адресным пространством в 32-разрядной версии Vista в D3D10.</span><span class="sxs-lookup"><span data-stu-id="b439f-321"><span id="My_game_runs_out_of_virtual_address_space_on_32-bit_Vista_under_D3D10._It_does_not_have_problems_on_D3D9.__"></span><span id="my_game_runs_out_of_virtual_address_space_on_32-bit_vista_under_d3d10._it_does_not_have_problems_on_d3d9.__"></span><span id="MY_GAME_RUNS_OUT_OF_VIRTUAL_ADDRESS_SPACE_ON_32-BIT_VISTA_UNDER_D3D10._IT_DOES_NOT_HAVE_PROBLEMS_ON_D3D9.__"></span>My game runs out of virtual address space on 32-bit Vista under D3D10.</span></span> <span data-ttu-id="b439f-322">У него нет проблем с D3D9.</span><span class="sxs-lookup"><span data-stu-id="b439f-322">It does not have problems on D3D9.</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-323">Возникли проблемы с D3D10 и виртуальным адресным пространством.</span><span class="sxs-lookup"><span data-stu-id="b439f-323">There were some issues with D3D10 and virtual address space.</span></span> <span data-ttu-id="b439f-324">Это было исправлено в [KB940105](https://support.microsoft.com/kb/940105).</span><span class="sxs-lookup"><span data-stu-id="b439f-324">This has been fixed in [KB940105](https://support.microsoft.com/kb/940105).</span></span> <span data-ttu-id="b439f-325">Если это не устраняет проблему, убедитесь, что вы не создаете больше ресурсов, которые могут быть сопоставлены (заблокированы) в D3D10, чем при создании в D3D9.</span><span class="sxs-lookup"><span data-stu-id="b439f-325">If that does not fix your problem, ensure you are not creating more resources that can be mapped (locked) in D3D10 than you were creating in D3D9.</span></span> <span data-ttu-id="b439f-326">Также Подумайте о переносе в 64-бит, так как это станет более распространенным в будущем.</span><span class="sxs-lookup"><span data-stu-id="b439f-326">Also think about porting to 64-bit since this will become more prevalent in the future.</span></span>

</dd> </dl>

## <a name="predicated-rendering"></a><span data-ttu-id="b439f-327">Отрисовка с предикатом</span><span class="sxs-lookup"><span data-stu-id="b439f-327">Predicated Rendering</span></span>

<dl> <dt>

<span data-ttu-id="b439f-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>Я использовал отработку по предикату (на основе результатов запроса перекрытия).</span><span class="sxs-lookup"><span data-stu-id="b439f-328"><span id="I_used_Predicated_rendering__based_on_occlusion_query_results_._Why_is_my_app_still_the_same_speed___"></span><span id="i_used_predicated_rendering__based_on_occlusion_query_results_._why_is_my_app_still_the_same_speed___"></span><span id="I_USED_PREDICATED_RENDERING__BASED_ON_OCCLUSION_QUERY_RESULTS_._WHY_IS_MY_APP_STILL_THE_SAME_SPEED___"></span>I used Predicated rendering (based on occlusion query results).</span></span> <span data-ttu-id="b439f-329">Почему мое приложение по-прежнему имеет одинаковую скорость?</span><span class="sxs-lookup"><span data-stu-id="b439f-329">Why is my app still the same speed?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-330">Во-первых, убедитесь, что визуализация, которую нужно пропустить, на самом деле является узким местом приложения.</span><span class="sxs-lookup"><span data-stu-id="b439f-330">First, ensure that the rendering you would like to skip is actually the application bottleneck.</span></span> <span data-ttu-id="b439f-331">Если это не узкое место, то пропуск отрисовки не поможет оценить частоту кадров.</span><span class="sxs-lookup"><span data-stu-id="b439f-331">If it is not the bottleneck, then skipping the rendering will not help frame rate.</span></span>

<span data-ttu-id="b439f-332">Во вторых, убедитесь в том, что между выпуском запроса и отрисовкой, которую вы хотите отдать предикату, достаточно времени.</span><span class="sxs-lookup"><span data-stu-id="b439f-332">Second, make sure that enough time has passed between the issue of the query and rendering that you wish to predicate.</span></span> <span data-ttu-id="b439f-333">Если запрос не завершен до тех пор, пока вызов прорисовки не достигнет графического процессора, отрисовка будет выполняться в любом случае.</span><span class="sxs-lookup"><span data-stu-id="b439f-333">If the query has not finished by the time the render call hits the GPU, the rendering will occur anyway.</span></span>

<span data-ttu-id="b439f-334">В третьих, затенения пропускает только определенные вызовы.</span><span class="sxs-lookup"><span data-stu-id="b439f-334">Third, predication only skips certain calls.</span></span> <span data-ttu-id="b439f-335">Пропущенные вызовы — это прорисовка, очистка, копирование, обновление, Ресолвесубресаурце и Женератемипс.</span><span class="sxs-lookup"><span data-stu-id="b439f-335">The calls that are skipped are Draw, Clear, Copy, Update, ResolveSubresource and GenerateMips.</span></span> <span data-ttu-id="b439f-336">Параметры состояния, установки IA, Map и CREATE не учитывают затенения.</span><span class="sxs-lookup"><span data-stu-id="b439f-336">State setting, IA setup, Map, and Create calls do not respect predication.</span></span> <span data-ttu-id="b439f-337">При наличии большого количества вызовов параметра State для предиката Draw все равно будут заданы эти состояния.</span><span class="sxs-lookup"><span data-stu-id="b439f-337">If there are a lot of state setting calls around the draw call to be predicated, these states still will be set.</span></span>

</dd> </dl>

## <a name="geometry-shader"></a><span data-ttu-id="b439f-338">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="b439f-338">Geometry Shader</span></span>

<dl> <dt>

<span data-ttu-id="b439f-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Следует ли использовать шейдер Geometry для тесселяции My (вставить здесь все)?</span><span class="sxs-lookup"><span data-stu-id="b439f-339"><span id="Should_I_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="should_i_use_the_geometry_shader_to_tessellate_my__insert_anything_here____"></span><span id="SHOULD_I_USE_THE_GEOMETRY_SHADER_TO_TESSELLATE_MY__INSERT_ANYTHING_HERE____"></span>Should I use the geometry shader to tessellate my (insert anything here)?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-340">Нет.</span><span class="sxs-lookup"><span data-stu-id="b439f-340">No.</span></span> <span data-ttu-id="b439f-341">Шейдер геометрии не следует использовать для тесселяции.</span><span class="sxs-lookup"><span data-stu-id="b439f-341">The geometry shader should NOT be used for tessellation.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Можно ли использовать шейдер геометрии для создания геометрии?</span><span class="sxs-lookup"><span data-stu-id="b439f-342"><span id="Can_I_use_the_geometry_shader_to_create_geometry___"></span><span id="can_i_use_the_geometry_shader_to_create_geometry___"></span><span id="CAN_I_USE_THE_GEOMETRY_SHADER_TO_CREATE_GEOMETRY___"></span>Can I use the geometry shader to create geometry?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-343">Да, в очень ограниченных сценариях.</span><span class="sxs-lookup"><span data-stu-id="b439f-343">Yes, in very limited scenarios.</span></span> <span data-ttu-id="b439f-344">Шейдер геометрии в текущих частях D3D10 (2008) не может справиться с большим расширением.</span><span class="sxs-lookup"><span data-stu-id="b439f-344">The geometry shader in current D3D10 (2008) parts is not equipped to handle much expansion.</span></span> <span data-ttu-id="b439f-345">Это может измениться в будущем.</span><span class="sxs-lookup"><span data-stu-id="b439f-345">This may change in the future.</span></span> <span data-ttu-id="b439f-346">Производители видеоадаптеров могут иметь специальный путь для одного и четырех расширений из-за имеющегося оборудования для работы с точками спрайта.</span><span class="sxs-lookup"><span data-stu-id="b439f-346">Video card vendors may have a special path for one to four expansions because of existing point-sprite hardware.</span></span> <span data-ttu-id="b439f-347">Любое другое расширение должно быть очень ограниченным.</span><span class="sxs-lookup"><span data-stu-id="b439f-347">Any other expansion would have to be very limited.</span></span> <span data-ttu-id="b439f-348">Примеры Партиклесгс и Пипесгс обеспечивают высокую частоту кадров, выполняя только ограниченное расширение.</span><span class="sxs-lookup"><span data-stu-id="b439f-348">The ParticlesGS and PipesGS samples achieve high frame rates by only doing limited expansion.</span></span> <span data-ttu-id="b439f-349">Для каждого кадра разворачивается всего несколько точек.</span><span class="sxs-lookup"><span data-stu-id="b439f-349">Only a few points are expanded per frame.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>Для чего следует использовать шейдер геометрии?</span><span class="sxs-lookup"><span data-stu-id="b439f-350"><span id="What_should_I_use_the_geometry_shader_for___"></span><span id="what_should_i_use_the_geometry_shader_for___"></span><span id="WHAT_SHOULD_I_USE_THE_GEOMETRY_SHADER_FOR___"></span>What should I use the geometry shader for?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-351">Все, что требует операций над целым примитивом, таким как обнаружение силуэт, координаты барицентрик и т. д.</span><span class="sxs-lookup"><span data-stu-id="b439f-351">Anything that requires operations on an entire primitive such as silhouette detection, barycentric coordinates, and so on.</span></span> <span data-ttu-id="b439f-352">Также используйте его для выбора среза целевого массива прорисовки для отправки примитивов.</span><span class="sxs-lookup"><span data-stu-id="b439f-352">Also use it to select which slice of a render target array to send primitives to.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Можно ли выводить переменные объемов геометрии из шейдера Geometry?</span><span class="sxs-lookup"><span data-stu-id="b439f-353"><span id="Can_I_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="can_i_output_variable_amounts_of_geometry_from_the_geometry_shader___"></span><span id="CAN_I_OUTPUT_VARIABLE_AMOUNTS_OF_GEOMETRY_FROM_THE_GEOMETRY_SHADER___"></span>Can I output variable amounts of geometry from the geometry shader?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-354">Да, но это может вызвать проблемы с производительностью.</span><span class="sxs-lookup"><span data-stu-id="b439f-354">Yes, but this can cause performance issues.</span></span> <span data-ttu-id="b439f-355">Возьмем пример вывода 1 точки для одного вызова и 4 точек для другого.</span><span class="sxs-lookup"><span data-stu-id="b439f-355">Take the example of outputting 1 point for one invocation and 4 points for another.</span></span> <span data-ttu-id="b439f-356">При соблюдении правил расширения это может привести к последовательному выполнению потоков шейдеров Geometry.</span><span class="sxs-lookup"><span data-stu-id="b439f-356">While fitting within the expansion guidelines, this can cause the geometry shader threads to run serially.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>Как D3D10 знает, как создавать смежные индексы для моей сетки?</span><span class="sxs-lookup"><span data-stu-id="b439f-357"><span id="How_does_D3D10_know_how_to_generate_adjacency_indices_for_my_mesh__Or__why_does_D3D10_not_render_correctly_when_I_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="how_does_d3d10_know_how_to_generate_adjacency_indices_for_my_mesh__or__why_does_d3d10_not_render_correctly_when_i_specify_that_the_geometry_shader_needs_adjacency_information.__"></span><span id="HOW_DOES_D3D10_KNOW_HOW_TO_GENERATE_ADJACENCY_INDICES_FOR_MY_MESH__OR__WHY_DOES_D3D10_NOT_RENDER_CORRECTLY_WHEN_I_SPECIFY_THAT_THE_GEOMETRY_SHADER_NEEDS_ADJACENCY_INFORMATION.__"></span>How does D3D10 know how to generate adjacency indices for my mesh?</span></span> <span data-ttu-id="b439f-358">Или, почему D3D10 не отображается правильно при указании того, что шейдеру Geometry требуются сведения о смежности.</span><span class="sxs-lookup"><span data-stu-id="b439f-358">Or, why does D3D10 not render correctly when I specify that the geometry shader needs adjacency information.</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-359">Сведения о соседических данных не создаются D3D10, а приложением.</span><span class="sxs-lookup"><span data-stu-id="b439f-359">The adjacency information is not created by D3D10, but by the application.</span></span> <span data-ttu-id="b439f-360">Смежные индексы создаются приложением и должны содержать шесть индексов для каждого примитива; из шести нечетных пронумерованных индексов расположены граничные смежные вершины.</span><span class="sxs-lookup"><span data-stu-id="b439f-360">Adjacency indices are generated by the application and must contain six indices per primitive; of the six, the odd numbered indices are the edge adjacent vertices.</span></span> <span data-ttu-id="b439f-361">Для создания этих данных можно использовать ID3DX10Mesh:: Женератеаджаценциандпоинтсрепс.</span><span class="sxs-lookup"><span data-stu-id="b439f-361">ID3DX10Mesh::GenerateAdjacencyAndPointsReps can be used to generate this data.</span></span>

</dd> </dl>

## <a name="hlsl"></a><span data-ttu-id="b439f-362">HLSL</span><span class="sxs-lookup"><span data-stu-id="b439f-362">HLSL</span></span>

<dl> <dt>

<span data-ttu-id="b439f-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Являются ли целочисленные и побитовые инструкции замедляются?</span><span class="sxs-lookup"><span data-stu-id="b439f-363"><span id="Are_integer_and_bitwise_instructions_slow___"></span><span id="are_integer_and_bitwise_instructions_slow___"></span><span id="ARE_INTEGER_AND_BITWISE_INSTRUCTIONS_SLOW___"></span>Are integer and bitwise instructions slow?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-364">Они могут быть.</span><span class="sxs-lookup"><span data-stu-id="b439f-364">They can be.</span></span> <span data-ttu-id="b439f-365">Различные карты D3D10 могут быть способны выдавать целочисленные операции только для подмножества доступных единиц ALU.</span><span class="sxs-lookup"><span data-stu-id="b439f-365">Various D3D10 cards may be able only to issue integer operations on a subset of the available ALU units.</span></span> <span data-ttu-id="b439f-366">Это сильно зависит от оборудования.</span><span class="sxs-lookup"><span data-stu-id="b439f-366">This is highly dependent on the hardware.</span></span> <span data-ttu-id="b439f-367">Рекомендации по устранению целочисленных операций на этом конкретном оборудовании см. в отдельном поставщике оборудования.</span><span class="sxs-lookup"><span data-stu-id="b439f-367">See your individual hardware vendor for recommendations on how to address integer operations on that particular hardware.</span></span> <span data-ttu-id="b439f-368">Кроме того, будьте внимательны при приведении типов.</span><span class="sxs-lookup"><span data-stu-id="b439f-368">Also, be very careful of casts between types.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>Что случилось с ВПОС?</span><span class="sxs-lookup"><span data-stu-id="b439f-369"><span id="What_happened_to_VPOS___"></span><span id="what_happened_to_vpos___"></span><span id="WHAT_HAPPENED_TO_VPOS___"></span>What happened to VPOS?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-370">Если вы объявили входные данные для шейдера пикселей как значение ОКП \_ , вы получите то же поведение, что и объявление его как впос.</span><span class="sxs-lookup"><span data-stu-id="b439f-370">If you declare an input to your pixel shader as SV\_POSITION, you will get the same behavior as declaring it as VPOS.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>Разделы справки пример текстуры MSAA?</span><span class="sxs-lookup"><span data-stu-id="b439f-371"><span id="How_do_I_sample_an_MSAA_texture___"></span><span id="how_do_i_sample_an_msaa_texture___"></span><span id="HOW_DO_I_SAMPLE_AN_MSAA_TEXTURE___"></span>How do I sample an MSAA texture?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-372">В шейдере объявите текстуру как Texture2DMS.</span><span class="sxs-lookup"><span data-stu-id="b439f-372">In your shader, declare your texture as Texture2DMS.</span></span> <span data-ttu-id="b439f-373">Затем можно получить отдельные образцы, используя примеры методов из объекта Texture2DMS.</span><span class="sxs-lookup"><span data-stu-id="b439f-373">You then can fetch individual samples using the Sample methods off of the Texture2DMS object.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>Разделы справки определить, действительно ли используется переменная шейдера в буфере константы?</span><span class="sxs-lookup"><span data-stu-id="b439f-374"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_used___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USED___"></span>How do I tell if a shader variable in a constant buffer actually is used?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-375">Взгляните на отраженную \_ переменную D3D10 шейдера \_ \_ DESC struct для этой переменной.</span><span class="sxs-lookup"><span data-stu-id="b439f-375">Look at the reflected D3D10\_SHADER\_VARIABLE\_DESC struct for that variable.</span></span> <span data-ttu-id="b439f-376">для Уфлагс должен быть \_ \_ установлен флаг D3D10 SVF.</span><span class="sxs-lookup"><span data-stu-id="b439f-376">uFlags should have the D3D10\_SVF\_USED flag set.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>Разделы справки определить, использует ли переменная шейдера в буфере константы FX10?</span><span class="sxs-lookup"><span data-stu-id="b439f-377"><span id="How_do_I_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_FX10___"></span><span id="how_do_i_tell_if_a_shader_variable_in_a_constant_buffer_actually_is_using_fx10___"></span><span id="HOW_DO_I_TELL_IF_A_SHADER_VARIABLE_IN_A_CONSTANT_BUFFER_ACTUALLY_IS_USING_FX10___"></span>How do I tell if a shader variable in a constant buffer actually is using FX10?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-378">В настоящее время это невозможно сделать с помощью FX10.</span><span class="sxs-lookup"><span data-stu-id="b439f-378">This currently is not possible using FX10.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>У меня нет возможности управлять константными буферами, создаваемыми FX10.</span><span class="sxs-lookup"><span data-stu-id="b439f-379"><span id="I_have_no_control_over_constant_buffers_that_FX10_creates._How_are_they_created_and_updated___"></span><span id="i_have_no_control_over_constant_buffers_that_fx10_creates._how_are_they_created_and_updated___"></span><span id="I_HAVE_NO_CONTROL_OVER_CONSTANT_BUFFERS_THAT_FX10_CREATES._HOW_ARE_THEY_CREATED_AND_UPDATED___"></span>I have no control over constant buffers that FX10 creates.</span></span> <span data-ttu-id="b439f-380">Как они создаются и обновляются?</span><span class="sxs-lookup"><span data-stu-id="b439f-380">How are they created and updated?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-381">Все управляемые FX10 буферы констант создаются как \_ \_ ресурсы по умолчанию для D3D10 использования и обновляются с помощью упдатесубресаурце.</span><span class="sxs-lookup"><span data-stu-id="b439f-381">All FX10-managed constant buffers are created as D3D10\_USAGE\_DEFAULT resources and are updated using UpdateSubresource.</span></span> <span data-ttu-id="b439f-382">Так как FX10 сохраняет резервное хранилище всех постоянных данных, Упдатесубресаурце является лучшим подходом к их обновлению.</span><span class="sxs-lookup"><span data-stu-id="b439f-382">Because FX10 keeps a backing store of all constant data, UpdateSubresource is the best approach for updating these.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>Разделы справки эмулировать фиксированный конвейер функций с помощью шейдеров?</span><span class="sxs-lookup"><span data-stu-id="b439f-383"><span id="How_do_I_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="how_do_i_emulate_the_fixed_function_pipeline_using_shaders___"></span><span id="HOW_DO_I_EMULATE_THE_FIXED_FUNCTION_PIPELINE_USING_SHADERS___"></span>How do I emulate the fixed function pipeline using shaders?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-384">См. пример Фикседфунцему.</span><span class="sxs-lookup"><span data-stu-id="b439f-384">See FixedFuncEMU sample.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Следует ли использовать новую \[ \] \[ подсказку компилятора (unroll, цикл \] , \[ ветвь \] и т. д.)?</span><span class="sxs-lookup"><span data-stu-id="b439f-385"><span id="Should_I_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="should_i_use_the_new__unroll____loop____branch___and_so_on__compiler_hints___"></span><span id="SHOULD_I_USE_THE_NEW__UNROLL____LOOP____BRANCH___AND_SO_ON__COMPILER_HINTS___"></span>Should I use the new \[unroll\], \[loop\], \[branch\], and so on, compiler hints?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-386">Как правило, нет.</span><span class="sxs-lookup"><span data-stu-id="b439f-386">In general, no.</span></span> <span data-ttu-id="b439f-387">Компилятор часто пытается воспользоваться обоими способами и выбирает самый быстрый из них.</span><span class="sxs-lookup"><span data-stu-id="b439f-387">The compiler will often try both ways and choose the fastest one.</span></span> <span data-ttu-id="b439f-388">В некоторых случаях может потребоваться использовать \[ unroll \] , например, когда выбор текстуры в цикле требует доступа к градиенту.</span><span class="sxs-lookup"><span data-stu-id="b439f-388">In some cases, it may be necessary to use \[unroll\], for example, when a texture fetch inside a loop needs access to a gradient.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>Отличается ли частичная точность от D3D10?</span><span class="sxs-lookup"><span data-stu-id="b439f-389"><span id="Does_partial_precision_make_any_difference_on_D3D10__I_can_specify_partial_precision_in_my_D3D9_HLSL__but_not_in_my_D3D10_HLSL.__"></span><span id="does_partial_precision_make_any_difference_on_d3d10__i_can_specify_partial_precision_in_my_d3d9_hlsl__but_not_in_my_d3d10_hlsl.__"></span><span id="DOES_PARTIAL_PRECISION_MAKE_ANY_DIFFERENCE_ON_D3D10__I_CAN_SPECIFY_PARTIAL_PRECISION_IN_MY_D3D9_HLSL__BUT_NOT_IN_MY_D3D10_HLSL.__"></span>Does partial precision make any difference on D3D10?</span></span> <span data-ttu-id="b439f-390">Я могу указать частичную точность в моем D3D9 HLSL, но не в D3D10 HLSL.</span><span class="sxs-lookup"><span data-stu-id="b439f-390">I can specify partial precision in my D3D9 HLSL, but not in my D3D10 HLSL.</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-391">Все операции D3D10 заданы для выполнения с точностью до 32 бит с плавающей точкой.</span><span class="sxs-lookup"><span data-stu-id="b439f-391">All D3D10 operations are specified to run at 32-bit floating point precision.</span></span> <span data-ttu-id="b439f-392">Поэтому частичная точность не должна делать никаких различий в D3D10.</span><span class="sxs-lookup"><span data-stu-id="b439f-392">Therefore, partial precision should not make any difference in D3D10.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>В D3D9 я могу выполнить HW PCF Shadow Filtering, привязывая буфер глубины в качестве текстуры и используя регулярные инструкции tex2d HLSL.</span><span class="sxs-lookup"><span data-stu-id="b439f-393"><span id="In_D3D9__I_could_do_HW_PCF_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._How_do_I_do_this_on_D3D10___"></span><span id="in_d3d9__i_could_do_hw_pcf_shadow_filtering_by_binding_a_depth_buffer_as_a_texture_and_using_regular_tex2d_hlsl_instructions._how_do_i_do_this_on_d3d10___"></span><span id="IN_D3D9__I_COULD_DO_HW_PCF_SHADOW_FILTERING_BY_BINDING_A_DEPTH_BUFFER_AS_A_TEXTURE_AND_USING_REGULAR_TEX2D_HLSL_INSTRUCTIONS._HOW_DO_I_DO_THIS_ON_D3D10___"></span>In D3D9, I could do HW PCF shadow filtering by binding a depth buffer as a texture and using regular tex2d hlsl instructions.</span></span> <span data-ttu-id="b439f-394">Разделы справки сделать это в D3D10?</span><span class="sxs-lookup"><span data-stu-id="b439f-394">How do I do this on D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-395">Необходимо использовать состояние образца сравнения и использовать инструкции Самплекмп.</span><span class="sxs-lookup"><span data-stu-id="b439f-395">You have to use a comparison sampler state and use SampleCmp instructions.</span></span>

</dd> <dt>

<span data-ttu-id="b439f-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>Как это ключевое слово Register работает в D3D10?</span><span class="sxs-lookup"><span data-stu-id="b439f-396"><span id="How_does_this_register_keyword_work_in_D3D10___"></span><span id="how_does_this_register_keyword_work_in_d3d10___"></span><span id="HOW_DOES_THIS_REGISTER_KEYWORD_WORK_IN_D3D10___"></span>How does this register keyword work in D3D10?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-397">Ключевое слово Register в D3D10 теперь применяется к области, к которой привязан конкретный ресурс.</span><span class="sxs-lookup"><span data-stu-id="b439f-397">The register keyword in D3D10 now applies to which slot a particular resource is bound to.</span></span> <span data-ttu-id="b439f-398">В этом случае ресурсом может быть буфер (константа или иным образом), текстура или образец.</span><span class="sxs-lookup"><span data-stu-id="b439f-398">In this case, the resource can be a Buffer (constant or otherwise), Texture, or Sampler.</span></span>

-   <span data-ttu-id="b439f-399">Для буферов констант используйте синтаксис: Register (млрд долл), где N — входной слот (0-15)</span><span class="sxs-lookup"><span data-stu-id="b439f-399">For constant buffers, use the syntax: register(bN), where N is the input slot (0-15)</span></span>
-   <span data-ttu-id="b439f-400">Для текстур используйте синтаксис: Register (тн), где N — входной слот (0-127).</span><span class="sxs-lookup"><span data-stu-id="b439f-400">For textures, use the syntax: register(tN), where N is the input slot (0-127)</span></span>
-   <span data-ttu-id="b439f-401">Для пробов используйте синтаксис: Register (sN), где N — входной слот (0-127)</span><span class="sxs-lookup"><span data-stu-id="b439f-401">For samplers, use the syntax: register(sN), where N is the input slot (0-127)</span></span>

</dd> <dt>

<span data-ttu-id="b439f-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>Разделы справки поместить переменную в буфер константы, если регистр используется только для указания места привязки всего буфера?</span><span class="sxs-lookup"><span data-stu-id="b439f-402"><span id="How_do_I_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="how_do_i_place_a_variable_inside_a_constant_buffer_if_register_is_just_used_to_specify_where_to_bind_the_entire_buffer___"></span><span id="HOW_DO_I_PLACE_A_VARIABLE_INSIDE_A_CONSTANT_BUFFER_IF_REGISTER_IS_JUST_USED_TO_SPECIFY_WHERE_TO_BIND_THE_ENTIRE_BUFFER___"></span>How do I place a variable inside a constant buffer if register is just used to specify where to bind the entire buffer?</span></span> 
</dt> <dd>

<span data-ttu-id="b439f-403">Используйте ключевое слово паккоффсет.</span><span class="sxs-lookup"><span data-stu-id="b439f-403">Use the packoffset keyword.</span></span> <span data-ttu-id="b439f-404">Аргумент для паккоффсет имеет формат c \[ 0-4095 \] . \[ x, y, z, w \] .</span><span class="sxs-lookup"><span data-stu-id="b439f-404">The argument to packoffset is in the form of c\[0-4095\].\[x,y,z,w\].</span></span> <span data-ttu-id="b439f-405">Пример:</span><span class="sxs-lookup"><span data-stu-id="b439f-405">For example:</span></span>

``` syntax
        cbuffer cbLotsOfEmptySpace
        {
        float   IWaste2Floats   : packoffset(c0.z);
        float4  IWasteMore  : packoffset(c13);
        };
```

<span data-ttu-id="b439f-406">В этом буфере констант IWaste2Floats помещается в третий массив с плавающей запятой (12-й байт) в буфер констант.</span><span class="sxs-lookup"><span data-stu-id="b439f-406">In this constant buffer, IWaste2Floats is placed at the third float (12th byte) in the constant buffer.</span></span> <span data-ttu-id="b439f-407">Ивастеморе помещается в 13-й float4 или 52nd float в буфере констант.</span><span class="sxs-lookup"><span data-stu-id="b439f-407">IWasteMore is placed at the 13th float4 or 52nd float in the constant buffer.</span></span>

</dd> </dl>

 

 