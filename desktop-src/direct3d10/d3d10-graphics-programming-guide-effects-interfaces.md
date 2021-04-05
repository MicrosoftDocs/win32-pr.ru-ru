---
description: 'Система эффектов определяет несколько интерфейсов для управления состоянием эффектов. Существует два типа интерфейсов: используемые средой выполнения для отрисовки эффектов и интерфейсов отражения для получения и установки переменных эффектов.'
ms.assetid: 068d49d2-0e14-4080-9fee-20d984f22545
title: Системные интерфейсы эффектов (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b40b21d98bedaec65550343260e7c52e2df1c302
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104141202"
---
# <a name="effect-system-interfaces-direct3d-10"></a><span data-ttu-id="aa472-104">Системные интерфейсы эффектов (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="aa472-104">Effect System Interfaces (Direct3D 10)</span></span>

<span data-ttu-id="aa472-105">Система эффектов определяет несколько интерфейсов для управления состоянием эффектов.</span><span class="sxs-lookup"><span data-stu-id="aa472-105">The effect system defines several interfaces for managing effect state.</span></span> <span data-ttu-id="aa472-106">Существует два типа интерфейсов: используемые средой выполнения для отрисовки эффектов и интерфейсов отражения для получения и установки переменных эффектов.</span><span class="sxs-lookup"><span data-stu-id="aa472-106">There are two types of interfaces: those used by the runtime to render an effect and reflection interfaces for getting and setting effect variables.</span></span>

-   [<span data-ttu-id="aa472-107">Интерфейсы среды выполнения Effect</span><span class="sxs-lookup"><span data-stu-id="aa472-107">Effect Runtime Interfaces</span></span>](#effect-runtime-interfaces)
-   [<span data-ttu-id="aa472-108">Интерфейсы отражения эффектов</span><span class="sxs-lookup"><span data-stu-id="aa472-108">Effect Reflection Interfaces</span></span>](#effect-reflection-interfaces)

## <a name="effect-runtime-interfaces"></a><span data-ttu-id="aa472-109">Интерфейсы среды выполнения Effect</span><span class="sxs-lookup"><span data-stu-id="aa472-109">Effect Runtime Interfaces</span></span>

<span data-ttu-id="aa472-110">Использование интерфейсов среды выполнения для визуализации эффектов.</span><span class="sxs-lookup"><span data-stu-id="aa472-110">Use runtime interfaces to render an effect.</span></span>



| <span data-ttu-id="aa472-111">Интерфейсы среды выполнения</span><span class="sxs-lookup"><span data-stu-id="aa472-111">Runtime Interfaces</span></span>                                               | <span data-ttu-id="aa472-112">Описание</span><span class="sxs-lookup"><span data-stu-id="aa472-112">Description</span></span>                                                          |
|------------------------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="aa472-113">**Интерфейс ID3D10Effect**</span><span class="sxs-lookup"><span data-stu-id="aa472-113">**ID3D10Effect Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effect)                   | <span data-ttu-id="aa472-114">Коллекция из одного или нескольких методов для отрисовки.</span><span class="sxs-lookup"><span data-stu-id="aa472-114">Collection of one or more techniques for rendering.</span></span>                  |
| <span data-ttu-id="aa472-115">[**Интерфейс ID3D10Include**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="aa472-115">[**ID3D10Include Interface**](/previous-versions/windows/desktop/legacy/bb173775(v=vs.85))</span></span>                 | <span data-ttu-id="aa472-116">Интерфейс для добавления пользовательских поведений при чтении включаемых файлов.</span><span class="sxs-lookup"><span data-stu-id="aa472-116">An interface for adding custom behaviors when reading include files.</span></span> |
| [<span data-ttu-id="aa472-117">**Интерфейс ID3D10EffectPass**</span><span class="sxs-lookup"><span data-stu-id="aa472-117">**ID3D10EffectPass Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpass)           | <span data-ttu-id="aa472-118">Коллекция назначений состояний.</span><span class="sxs-lookup"><span data-stu-id="aa472-118">A collection of state assignments.</span></span>                                   |
| [<span data-ttu-id="aa472-119">**Интерфейс ID3D10EffectPool**</span><span class="sxs-lookup"><span data-stu-id="aa472-119">**ID3D10EffectPool Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectpool)           | <span data-ttu-id="aa472-120">Создайте место в памяти для переменных, которые будут совместно использоваться различными эффектами.</span><span class="sxs-lookup"><span data-stu-id="aa472-120">Create a memory location for variables to be shared between effects.</span></span> |
| [<span data-ttu-id="aa472-121">**Интерфейс ID3D10EffectTechnique**</span><span class="sxs-lookup"><span data-stu-id="aa472-121">**ID3D10EffectTechnique Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttechnique) | <span data-ttu-id="aa472-122">Коллекция из одного или нескольких проходов.</span><span class="sxs-lookup"><span data-stu-id="aa472-122">A collection of one or more passes.</span></span>                                  |



 

## <a name="effect-reflection-interfaces"></a><span data-ttu-id="aa472-123">Интерфейсы отражения эффектов</span><span class="sxs-lookup"><span data-stu-id="aa472-123">Effect Reflection Interfaces</span></span>

<span data-ttu-id="aa472-124">Отражение реализуется в системе эффектов для поддержки чтения (и записи) состояния воздействия.</span><span class="sxs-lookup"><span data-stu-id="aa472-124">Reflection is implemented in the effect system to support reading (and writing) effect state.</span></span> <span data-ttu-id="aa472-125">Существует несколько способов доступа к переменным эффектов.</span><span class="sxs-lookup"><span data-stu-id="aa472-125">There are multiple ways to access effect variables.</span></span>

### <a name="setting-groups-of-effect-state"></a><span data-ttu-id="aa472-126">Установка групп состояния эффектов</span><span class="sxs-lookup"><span data-stu-id="aa472-126">Setting Groups of Effect State</span></span>

<span data-ttu-id="aa472-127">Используйте эти интерфейсы для получения и установки группы состояний.</span><span class="sxs-lookup"><span data-stu-id="aa472-127">Use these interfaces to get and set a group of state.</span></span>



| <span data-ttu-id="aa472-128">Интерфейсы отражения</span><span class="sxs-lookup"><span data-stu-id="aa472-128">Reflection Interfaces</span></span>                                                                  | <span data-ttu-id="aa472-129">Описание</span><span class="sxs-lookup"><span data-stu-id="aa472-129">Description</span></span>                      |
|----------------------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="aa472-130">**Интерфейс ID3D10EffectBlendVariable**</span><span class="sxs-lookup"><span data-stu-id="aa472-130">**ID3D10EffectBlendVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectblendvariable)               | <span data-ttu-id="aa472-131">Получение и установка состояния смешения.</span><span class="sxs-lookup"><span data-stu-id="aa472-131">Get and set blend state.</span></span>         |
| [<span data-ttu-id="aa472-132">**Интерфейс ID3D10EffectDepthStencilVariable**</span><span class="sxs-lookup"><span data-stu-id="aa472-132">**ID3D10EffectDepthStencilVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilvariable) | <span data-ttu-id="aa472-133">Возвращает и задает состояние шаблона глубины.</span><span class="sxs-lookup"><span data-stu-id="aa472-133">Get and set depth-stencil state.</span></span> |
| [<span data-ttu-id="aa472-134">**Интерфейс ID3D10EffectRasterizerVariable**</span><span class="sxs-lookup"><span data-stu-id="aa472-134">**ID3D10EffectRasterizerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrasterizervariable)     | <span data-ttu-id="aa472-135">Получение и установка состояния средства прорисовки.</span><span class="sxs-lookup"><span data-stu-id="aa472-135">Get and set rasterizer state.</span></span>    |
| [<span data-ttu-id="aa472-136">**Интерфейс ID3D10EffectSamplerVariable**</span><span class="sxs-lookup"><span data-stu-id="aa472-136">**ID3D10EffectSamplerVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectsamplervariable)           | <span data-ttu-id="aa472-137">Получение и установка состояния образца.</span><span class="sxs-lookup"><span data-stu-id="aa472-137">Get and set sampler state.</span></span>       |



 

### <a name="setting-effect-resources"></a><span data-ttu-id="aa472-138">Настройка ресурсов эффектов</span><span class="sxs-lookup"><span data-stu-id="aa472-138">Setting Effect Resources</span></span>

<span data-ttu-id="aa472-139">Используйте эти интерфейсы для получения и задания ресурсов.</span><span class="sxs-lookup"><span data-stu-id="aa472-139">Use these interfaces to get and set resources.</span></span>



| <span data-ttu-id="aa472-140">Интерфейсы отражения</span><span class="sxs-lookup"><span data-stu-id="aa472-140">Reflection Interfaces</span></span>                                                                          | <span data-ttu-id="aa472-141">Описание</span><span class="sxs-lookup"><span data-stu-id="aa472-141">Description</span></span>                                         |
|------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| [<span data-ttu-id="aa472-142">**Интерфейс ID3D10EffectConstantBuffer**</span><span class="sxs-lookup"><span data-stu-id="aa472-142">**ID3D10EffectConstantBuffer Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectconstantbuffer)                     | <span data-ttu-id="aa472-143">Доступ к данным в буфере текстуры или буфере констант.</span><span class="sxs-lookup"><span data-stu-id="aa472-143">Access data in a texture buffer or constant buffer.</span></span> |
| [<span data-ttu-id="aa472-144">**Интерфейс ID3D10EffectDepthStencilViewVariable**</span><span class="sxs-lookup"><span data-stu-id="aa472-144">**ID3D10EffectDepthStencilViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectdepthstencilviewvariable) | <span data-ttu-id="aa472-145">Доступ к данным в ресурсе с набором элементов глубины.</span><span class="sxs-lookup"><span data-stu-id="aa472-145">Access data in a depth-stencil resource.</span></span>            |
| [<span data-ttu-id="aa472-146">**Интерфейс ID3D10EffectRenderTargetViewVariable**</span><span class="sxs-lookup"><span data-stu-id="aa472-146">**ID3D10EffectRenderTargetViewVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectrendertargetviewvariable) | <span data-ttu-id="aa472-147">Доступ к данным в целевом объекте прорисовки.</span><span class="sxs-lookup"><span data-stu-id="aa472-147">Access data in a render target.</span></span>                     |
| [<span data-ttu-id="aa472-148">**Интерфейс ID3D10EffectShaderResourceVariable**</span><span class="sxs-lookup"><span data-stu-id="aa472-148">**ID3D10EffectShaderResourceVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshaderresourcevariable)     | <span data-ttu-id="aa472-149">Доступ к данным в ресурсе шейдера.</span><span class="sxs-lookup"><span data-stu-id="aa472-149">Access data in a shader resource.</span></span>                   |



 

### <a name="setting-other-effect-variables"></a><span data-ttu-id="aa472-150">Задание других переменных эффектов</span><span class="sxs-lookup"><span data-stu-id="aa472-150">Setting Other Effect Variables</span></span>

<span data-ttu-id="aa472-151">Используйте эти интерфейсы для получения и задания состояния по типу переменной.</span><span class="sxs-lookup"><span data-stu-id="aa472-151">Use these interfaces to get and set state by the variable type.</span></span>



| <span data-ttu-id="aa472-152">Интерфейсы отражения</span><span class="sxs-lookup"><span data-stu-id="aa472-152">Reflection Interfaces</span></span>                                                      | <span data-ttu-id="aa472-153">Описание</span><span class="sxs-lookup"><span data-stu-id="aa472-153">Description</span></span>                    |
|----------------------------------------------------------------------------|--------------------------------|
| [<span data-ttu-id="aa472-154">**Интерфейс ID3D10EffectMatrixVariable**</span><span class="sxs-lookup"><span data-stu-id="aa472-154">**ID3D10EffectMatrixVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectmatrixvariable) | <span data-ttu-id="aa472-155">Получение и задание матрицы.</span><span class="sxs-lookup"><span data-stu-id="aa472-155">Get and set a matrix.</span></span>          |
| [<span data-ttu-id="aa472-156">**Интерфейс ID3D10EffectScalarVariable**</span><span class="sxs-lookup"><span data-stu-id="aa472-156">**ID3D10EffectScalarVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectscalarvariable) | <span data-ttu-id="aa472-157">Получение и задание скаляра.</span><span class="sxs-lookup"><span data-stu-id="aa472-157">Get and set a scalar.</span></span>          |
| [<span data-ttu-id="aa472-158">**Интерфейс ID3D10EffectShaderVariable**</span><span class="sxs-lookup"><span data-stu-id="aa472-158">**ID3D10EffectShaderVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectshadervariable) | <span data-ttu-id="aa472-159">Возвращает и задает переменную шейдера.</span><span class="sxs-lookup"><span data-stu-id="aa472-159">Get and set a shader variable.</span></span> |
| [<span data-ttu-id="aa472-160">**Интерфейс ID3D10EffectStringVariable**</span><span class="sxs-lookup"><span data-stu-id="aa472-160">**ID3D10EffectStringVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectstringvariable) | <span data-ttu-id="aa472-161">Возвращает и задает строку.</span><span class="sxs-lookup"><span data-stu-id="aa472-161">Get and set a string.</span></span>          |
| [<span data-ttu-id="aa472-162">**Интерфейс ID3D10EffectType**</span><span class="sxs-lookup"><span data-stu-id="aa472-162">**ID3D10EffectType Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effecttype)                     | <span data-ttu-id="aa472-163">Получение типа переменной.</span><span class="sxs-lookup"><span data-stu-id="aa472-163">Get a variable type.</span></span>           |
| [<span data-ttu-id="aa472-164">**Интерфейс ID3D10EffectVectorVariable**</span><span class="sxs-lookup"><span data-stu-id="aa472-164">**ID3D10EffectVectorVariable Interface**</span></span>](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvectorvariable) | <span data-ttu-id="aa472-165">Возвращает и задает вектор.</span><span class="sxs-lookup"><span data-stu-id="aa472-165">Get and set a vector.</span></span>          |



 

<span data-ttu-id="aa472-166">Все интерфейсы отражения являются производными от [**интерфейса ID3D10EffectVariable**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).</span><span class="sxs-lookup"><span data-stu-id="aa472-166">All reflection interfaces derive from [**ID3D10EffectVariable Interface**](/windows/desktop/api/D3D10Effect/nn-d3d10effect-id3d10effectvariable).</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa472-167">См. также</span><span class="sxs-lookup"><span data-stu-id="aa472-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa472-168">Эффекты</span><span class="sxs-lookup"><span data-stu-id="aa472-168">Effects</span></span>](d3d10-graphics-programming-guide-effects.md)
</dt> <dt>

[<span data-ttu-id="aa472-169">Рекомендации по программированию для Direct3D 10</span><span class="sxs-lookup"><span data-stu-id="aa472-169">Programming Guide for Direct3D 10</span></span>](d3d10-graphics-programming-guide.md)
</dt> </dl>

 

 
