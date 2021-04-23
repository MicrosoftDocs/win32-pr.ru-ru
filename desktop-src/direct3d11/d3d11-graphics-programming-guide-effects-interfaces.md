---
title: Системные интерфейсы эффектов (Direct3D 11)
description: Система эффектов определяет несколько интерфейсов для управления состоянием эффектов.
ms.assetid: 5cba6055-d153-4837-9a08-96efbde5f48f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af76a54be06e52e320743ca945abb31d1d50d213
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774081"
---
# <a name="effect-system-interfaces-direct3d-11"></a><span data-ttu-id="11226-103">Системные интерфейсы эффектов (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="11226-103">Effect System Interfaces (Direct3D 11)</span></span>

<span data-ttu-id="11226-104">Система эффектов определяет несколько интерфейсов для управления состоянием эффектов.</span><span class="sxs-lookup"><span data-stu-id="11226-104">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="11226-105">Существует два типа интерфейсов: используемые средой выполнения для отрисовки эффектов и интерфейсов отражения для получения и установки переменных эффектов.</span><span class="sxs-lookup"><span data-stu-id="11226-105">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="11226-106">Интерфейсы среды выполнения Effect</span><span class="sxs-lookup"><span data-stu-id="11226-106">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="11226-107">Интерфейсы отражения эффектов</span><span class="sxs-lookup"><span data-stu-id="11226-107">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="11226-108">Интерфейсы среды выполнения Effect</span><span class="sxs-lookup"><span data-stu-id="11226-108">Effect Runtime Interfaces</span></span>

<span data-ttu-id="11226-109">Использование интерфейсов среды выполнения для визуализации эффектов.</span><span class="sxs-lookup"><span data-stu-id="11226-109">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="11226-110">Интерфейсы среды выполнения</span><span class="sxs-lookup"><span data-stu-id="11226-110">Runtime Interfaces</span></span>                                       | <span data-ttu-id="11226-111">Описание</span><span class="sxs-lookup"><span data-stu-id="11226-111">Description</span></span>                                                    |
|----------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="11226-112">**ID3DX11Effect**</span><span class="sxs-lookup"><span data-stu-id="11226-112">**ID3DX11Effect**</span></span>](id3dx11effect.md)                   | <span data-ttu-id="11226-113">Коллекция одной или нескольких групп и методов для подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="11226-113">Collection of one or more groups and techniques for rendering.</span></span> |
| [<span data-ttu-id="11226-114">**ID3DX11EffectPass**</span><span class="sxs-lookup"><span data-stu-id="11226-114">**ID3DX11EffectPass**</span></span>](id3dx11effectpass.md)           | <span data-ttu-id="11226-115">Коллекция назначений состояний.</span><span class="sxs-lookup"><span data-stu-id="11226-115">A collection of state assignments.</span></span>                             |
| [<span data-ttu-id="11226-116">**ID3DX11EffectTechnique**</span><span class="sxs-lookup"><span data-stu-id="11226-116">**ID3DX11EffectTechnique**</span></span>](id3dx11effecttechnique.md) | <span data-ttu-id="11226-117">Коллекция из одного или нескольких проходов.</span><span class="sxs-lookup"><span data-stu-id="11226-117">A collection of one or more passes.</span></span>                            |
| [<span data-ttu-id="11226-118">**ID3DX11EffectGroup**</span><span class="sxs-lookup"><span data-stu-id="11226-118">**ID3DX11EffectGroup**</span></span>](id3dx11effectgroup.md)         | <span data-ttu-id="11226-119">Коллекция из одного или нескольких методов.</span><span class="sxs-lookup"><span data-stu-id="11226-119">A collection of one or more techniques.</span></span>                        |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="11226-120">Интерфейсы отражения эффектов</span><span class="sxs-lookup"><span data-stu-id="11226-120">Effect Reflection Interfaces</span></span>

<span data-ttu-id="11226-121">Отражение реализуется в системе эффектов для поддержки чтения (и записи) состояния воздействия.</span><span class="sxs-lookup"><span data-stu-id="11226-121">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="11226-122">Существует несколько способов доступа к переменным эффектов.</span><span class="sxs-lookup"><span data-stu-id="11226-122">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="11226-123">Установка групп состояния эффектов</span><span class="sxs-lookup"><span data-stu-id="11226-123">Setting Groups of Effect State</span></span>

<span data-ttu-id="11226-124">Используйте эти интерфейсы для получения и установки группы состояний.</span><span class="sxs-lookup"><span data-stu-id="11226-124">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="11226-125">Интерфейсы отражения</span><span class="sxs-lookup"><span data-stu-id="11226-125">Reflection Interfaces</span></span>                                                          | <span data-ttu-id="11226-126">Описание</span><span class="sxs-lookup"><span data-stu-id="11226-126">Description</span></span>                      |
|--------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="11226-127">**ID3DX11EffectBlendVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-127">**ID3DX11EffectBlendVariable**</span></span>](id3dx11effectblendvariable.md)               | <span data-ttu-id="11226-128">Получение и установка состояния смешения.</span><span class="sxs-lookup"><span data-stu-id="11226-128">Get and set blend state.</span></span>         |
| [<span data-ttu-id="11226-129">**ID3DX11EffectDepthStencilVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-129">**ID3DX11EffectDepthStencilVariable**</span></span>](id3dx11effectdepthstencilvariable.md) | <span data-ttu-id="11226-130">Возвращает и задает состояние шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="11226-130">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="11226-131">**ID3DX11EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-131">**ID3DX11EffectRasterizerVariable**</span></span>](id3dx11effectrasterizervariable.md)     | <span data-ttu-id="11226-132">Получение и установка состояния средства прорисовки.</span><span class="sxs-lookup"><span data-stu-id="11226-132">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="11226-133">**ID3DX11EffectSamplerVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-133">**ID3DX11EffectSamplerVariable**</span></span>](id3dx11effectsamplervariable.md)           | <span data-ttu-id="11226-134">Получение и установка состояния образца.</span><span class="sxs-lookup"><span data-stu-id="11226-134">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="11226-135">Настройка ресурсов эффектов</span><span class="sxs-lookup"><span data-stu-id="11226-135">Setting Effect Resources</span></span>

<span data-ttu-id="11226-136">Используйте эти интерфейсы для получения и задания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="11226-136">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="11226-137">Интерфейсы отражения</span><span class="sxs-lookup"><span data-stu-id="11226-137">Reflection Interfaces</span></span>                                                                        | <span data-ttu-id="11226-138">Описание</span><span class="sxs-lookup"><span data-stu-id="11226-138">Description</span></span>                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="11226-139">**ID3DX11EffectConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="11226-139">**ID3DX11EffectConstantBuffer**</span></span>](id3dx11effectconstantbuffer.md)                           | <span data-ttu-id="11226-140">Доступ к данным в буфере текстуры или буфере констант.</span><span class="sxs-lookup"><span data-stu-id="11226-140">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="11226-141">**ID3DX11EffectDepthStencilViewVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-141">**ID3DX11EffectDepthStencilViewVariable**</span></span>](id3dx11effectdepthstencilviewvariable.md)       | <span data-ttu-id="11226-142">Доступ к данным в ресурсе с набором элементов глубины.</span><span class="sxs-lookup"><span data-stu-id="11226-142">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="11226-143">**ID3DX11EffectRenderTargetViewVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-143">**ID3DX11EffectRenderTargetViewVariable**</span></span>](id3dx11effectrendertargetviewvariable.md)       | <span data-ttu-id="11226-144">Доступ к данным в целевом объекте прорисовки.</span><span class="sxs-lookup"><span data-stu-id="11226-144">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="11226-145">**ID3DX11EffectShaderResourceVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-145">**ID3DX11EffectShaderResourceVariable**</span></span>](id3dx11effectshaderresourcevariable.md)           | <span data-ttu-id="11226-146">Доступ к данным в ресурсе шейдера.</span><span class="sxs-lookup"><span data-stu-id="11226-146">Access data in a shader resource.</span></span>                   |
| [<span data-ttu-id="11226-147">**ID3DX11EffectUnorderedAccessViewVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-147">**ID3DX11EffectUnorderedAccessViewVariable**</span></span>](id3dx11effectunorderedaccessviewvariable.md) | <span data-ttu-id="11226-148">Доступ к данным в представлении неупорядоченного доступа.</span><span class="sxs-lookup"><span data-stu-id="11226-148">Access data in an unordered access view.</span></span>            |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="11226-149">Задание других переменных эффектов</span><span class="sxs-lookup"><span data-stu-id="11226-149">Setting Other Effect Variables</span></span>

<span data-ttu-id="11226-150">Используйте эти интерфейсы для получения и задания состояния по типу переменной.</span><span class="sxs-lookup"><span data-stu-id="11226-150">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="11226-151">Интерфейсы отражения</span><span class="sxs-lookup"><span data-stu-id="11226-151">Reflection Interfaces</span></span>                                                            | <span data-ttu-id="11226-152">Описание</span><span class="sxs-lookup"><span data-stu-id="11226-152">Description</span></span>               |
|----------------------------------------------------------------------------------|---------------------------|
| [<span data-ttu-id="11226-153">**ID3DX11EffectClassInstanceVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-153">**ID3DX11EffectClassInstanceVariable**</span></span>](id3dx11effectclassinstancevariable.md) | <span data-ttu-id="11226-154">Получение экземпляра класса.</span><span class="sxs-lookup"><span data-stu-id="11226-154">Get a class instance.</span></span>     |
| [<span data-ttu-id="11226-155">**ID3DX11EffectInterfaceVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-155">**ID3DX11EffectInterfaceVariable**</span></span>](id3dx11effectinterfacevariable.md)         | <span data-ttu-id="11226-156">Получение и установка интерфейса.</span><span class="sxs-lookup"><span data-stu-id="11226-156">Get and set an interface.</span></span> |
| [<span data-ttu-id="11226-157">**ID3DX11EffectMatrixVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-157">**ID3DX11EffectMatrixVariable**</span></span>](id3dx11effectmatrixvariable.md)               | <span data-ttu-id="11226-158">Получение и задание матрицы.</span><span class="sxs-lookup"><span data-stu-id="11226-158">Get and set a matrix.</span></span>     |
| [<span data-ttu-id="11226-159">**ID3DX11EffectScalarVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-159">**ID3DX11EffectScalarVariable**</span></span>](id3dx11effectscalarvariable.md)               | <span data-ttu-id="11226-160">Получение и задание скаляра.</span><span class="sxs-lookup"><span data-stu-id="11226-160">Get and set a scalar.</span></span>     |
| [<span data-ttu-id="11226-161">**ID3DX11EffectShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-161">**ID3DX11EffectShaderVariable**</span></span>](id3dx11effectshadervariable.md)               | <span data-ttu-id="11226-162">Получение переменной шейдера.</span><span class="sxs-lookup"><span data-stu-id="11226-162">Get a shader variable.</span></span>    |
| [<span data-ttu-id="11226-163">**ID3DX11EffectStringVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-163">**ID3DX11EffectStringVariable**</span></span>](id3dx11effectstringvariable.md)               | <span data-ttu-id="11226-164">Возвращает и задает строку.</span><span class="sxs-lookup"><span data-stu-id="11226-164">Get and set a string.</span></span>     |
| [<span data-ttu-id="11226-165">**ID3DX11EffectType**</span><span class="sxs-lookup"><span data-stu-id="11226-165">**ID3DX11EffectType**</span></span>](id3dx11effecttype.md)                                   | <span data-ttu-id="11226-166">Получение типа переменной.</span><span class="sxs-lookup"><span data-stu-id="11226-166">Get a variable type.</span></span>      |
| [<span data-ttu-id="11226-167">**ID3DX11EffectVectorVariable**</span><span class="sxs-lookup"><span data-stu-id="11226-167">**ID3DX11EffectVectorVariable**</span></span>](id3dx11effectvectorvariable.md)               | <span data-ttu-id="11226-168">Возвращает и задает вектор.</span><span class="sxs-lookup"><span data-stu-id="11226-168">Get and set a vector.</span></span>     |



 

<span data-ttu-id="11226-169">Все интерфейсы отражения являются производными от [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span><span class="sxs-lookup"><span data-stu-id="11226-169">All reflection interfaces derive from [**ID3DX11EffectVariable**](id3dx11effectvariable.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="11226-170">См. также</span><span class="sxs-lookup"><span data-stu-id="11226-170">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11226-171">Эффекты (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="11226-171">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="11226-172">Руководство по программированию для Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="11226-172">Programming Guide for Direct3D 11</span></span>](dx-graphics-overviews.md)
</dt> </dl>

 

 




