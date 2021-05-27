---
title: Связывание шейдеров эффектов
description: Direct2D использует оптимизацию, называемую связыванием шейдера эффектов, которая сочетает визуализацию диаграммы с несколькими эффектыми, передавая один проход.
ms.assetid: 431A5B39-6C84-442D-AC66-0F341E10DF2C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b6bad2170f2b897a5cf8ac3086a74945efa8bf
ms.sourcegitcommit: f848119a8faa29b27585f4df53f6e50ee9666684
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/27/2021
ms.locfileid: "110549239"
---
# <a name="effect-shader-linking"></a><span data-ttu-id="2ad17-103">Связывание шейдеров эффектов</span><span class="sxs-lookup"><span data-stu-id="2ad17-103">Effect Shader Linking</span></span>

<span data-ttu-id="2ad17-104">Direct2D использует оптимизацию, называемую связыванием шейдера эффектов, которая сочетает визуализацию диаграммы с несколькими эффектыми, передавая один проход.</span><span class="sxs-lookup"><span data-stu-id="2ad17-104">Direct2D uses an optimization called effect shader linking which combines multiple effect graph rendering passes into a single pass.</span></span>

-   [<span data-ttu-id="2ad17-105">Общие сведения о связывании шейдера эффектов</span><span class="sxs-lookup"><span data-stu-id="2ad17-105">Overview of Effect Shader Linking</span></span>](#overview-of-effect-shader-linking)
-   [<span data-ttu-id="2ad17-106">Использование связывания шейдера эффектов</span><span class="sxs-lookup"><span data-stu-id="2ad17-106">Using Effect Shader Linking</span></span>](#using-effect-shader-linking)
-   [<span data-ttu-id="2ad17-107">Создание пользовательского действия, совместимого с шейдером</span><span class="sxs-lookup"><span data-stu-id="2ad17-107">Authoring a shader linking-compatible custom effect</span></span>](#authoring-a-shader-linking-compatible-custom-effect)
-   [<span data-ttu-id="2ad17-108">Пример связывания. совместимый шейдер эффектов</span><span class="sxs-lookup"><span data-stu-id="2ad17-108">Example linking-compatible effect shader</span></span>](#example-linking-compatible-effect-shader)
-   [<span data-ttu-id="2ad17-109">Компиляция совместимого шейдера связывания</span><span class="sxs-lookup"><span data-stu-id="2ad17-109">Compiling a linking compatible-shader</span></span>](#compiling-a-linking-compatible-shader)
    -   [<span data-ttu-id="2ad17-110">Шаг 1. компиляция функции экспорта</span><span class="sxs-lookup"><span data-stu-id="2ad17-110">Step 1: Compile the export function</span></span>](#step-1-compile-the-export-function)
    -   [<span data-ttu-id="2ad17-111">Шаг 2. Компиляция полного шейдера и встраивание функции экспорта</span><span class="sxs-lookup"><span data-stu-id="2ad17-111">Step 2: Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)
-   [<span data-ttu-id="2ad17-112">Экспорт спецификаций функций</span><span class="sxs-lookup"><span data-stu-id="2ad17-112">Export function specifications</span></span>](#export-function-specifications)
-   [<span data-ttu-id="2ad17-113">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2ad17-113">Related topics</span></span>](#related-topics)

## <a name="overview-of-effect-shader-linking"></a><span data-ttu-id="2ad17-114">Общие сведения о связывании шейдера эффектов</span><span class="sxs-lookup"><span data-stu-id="2ad17-114">Overview of Effect Shader Linking</span></span>

<span data-ttu-id="2ad17-115">Оптимизация связывания с шейдером влияет на компоновку шейдера HLSL, функцию Direct3D 11,2, позволяющую создавать шейдеры пикселей и вершин во время выполнения путем связывания предварительно скомпилированных функций шейдера.</span><span class="sxs-lookup"><span data-stu-id="2ad17-115">The effect shader linking optimizations builds on top of HLSL shader linking, a Direct3D 11.2 feature that allows pixel and vertex shaders to be generated at runtime by linking pre-compiled shader functions.</span></span> <span data-ttu-id="2ad17-116">На следующих рисунках показано понятие связывания шейдера эффектов в графе эффектов.</span><span class="sxs-lookup"><span data-stu-id="2ad17-116">The following figures illustrate the concept of effect shader linking in an effect graph.</span></span> <span data-ttu-id="2ad17-117">На первой фигуре показана типичная диаграмма с Direct2Dным результатом с четырьмя преобразованиями отрисовки.</span><span class="sxs-lookup"><span data-stu-id="2ad17-117">The first figure shows a typical Direct2D effect graph with four rendering transforms.</span></span> <span data-ttu-id="2ad17-118">Без связывания с шейдером каждое преобразование использует проход отрисовки и требует промежуточной поверхности; в итоге для этого графа требуется 4 прохода и 3 промежуточных уровня.</span><span class="sxs-lookup"><span data-stu-id="2ad17-118">Without shader linking, each transform consumes a rendering pass and requires an intermediate surface; in total, this graph requires 4 passes and 3 intermediates.</span></span>

![Преобразование графа без связывания с шейдером: 4 прохода и 3 промежуточных.](images/shader-transform-graph.png)

<span data-ttu-id="2ad17-120">На втором рисунке показана та же диаграмма влияния, в которой каждое преобразование отрисовки заменено на версию связываемой функции.</span><span class="sxs-lookup"><span data-stu-id="2ad17-120">The second figure shows the same effect graph where each rendering transform has been replaced with a linkable function version.</span></span> <span data-ttu-id="2ad17-121">Direct2D может связать весь граф и выполнить его за один проход, не требуя каких-либо промежуточных уровней.</span><span class="sxs-lookup"><span data-stu-id="2ad17-121">Direct2D is able link the entire graph and execute it in one pass without requiring any intermediates.</span></span> <span data-ttu-id="2ad17-122">Это может привести к значительному снижению времени выполнения GPU и уменьшению пикового потребления памяти GPU.</span><span class="sxs-lookup"><span data-stu-id="2ad17-122">This can provide a significant decrease in GPU execution time and reduction in peak GPU memory consumption.</span></span>

![Преобразование графа с связыванием шейдера: 1 проход, промежуточный уровень 0.](images/shader-linking-graph.png)



 

<span data-ttu-id="2ad17-124">Связывание шейдера эффектов работает с отдельными преобразованиями в пределах одного действия; Это означает, что даже граф с одним эффектом может выиграть от связывания шейдера, если этот эффект имеет несколько допустимых преобразований.</span><span class="sxs-lookup"><span data-stu-id="2ad17-124">Effect shader linking operates on individual transforms within an effect; this means that even a graph with a single effect may benefit from shader linking if that effect has multiple valid transforms.</span></span>

## <a name="using-effect-shader-linking"></a><span data-ttu-id="2ad17-125">Использование связывания шейдера эффектов</span><span class="sxs-lookup"><span data-stu-id="2ad17-125">Using Effect Shader Linking</span></span>

<span data-ttu-id="2ad17-126">Если вы создаете приложение Direct2D, использующее эффекты, вам не нужно ничего делать, чтобы воспользоваться преимуществами связывания с шейдером эффектов.</span><span class="sxs-lookup"><span data-stu-id="2ad17-126">If you are building a Direct2D application that uses effects, you don’t need to do anything to take advantage of effect shader linking.</span></span> <span data-ttu-id="2ad17-127">Direct2D автоматически анализирует диаграмму эффектов, чтобы определить наиболее оптимальный способ связывания каждого преобразования.</span><span class="sxs-lookup"><span data-stu-id="2ad17-127">Direct2D automatically analyzes the effect graph to determine the most optimal way to link each transform.</span></span>

<span data-ttu-id="2ad17-128">Авторы эффектов отвечают за реализацию их влияния на способ, который поддерживает связывание шейдера эффектов; Дополнительные сведения см. в разделе [Создание пользовательского действия, совместимого с шейдером](#authoring-a-shader-linking-compatible-custom-effect) , ниже.</span><span class="sxs-lookup"><span data-stu-id="2ad17-128">Effect authors are responsible for implementing their effect in a way that supports effect shader linking; for more information, see the [Authoring a shader linking-compatible custom effect](#authoring-a-shader-linking-compatible-custom-effect) section below.</span></span> <span data-ttu-id="2ad17-129">Все встроенные эффекты поддерживают связывание с шейдером.</span><span class="sxs-lookup"><span data-stu-id="2ad17-129">All of the built-in effects support shader linking.</span></span>

<span data-ttu-id="2ad17-130">Direct2D будет связывать только смежные преобразования отрисовки в ситуациях, где это полезно.</span><span class="sxs-lookup"><span data-stu-id="2ad17-130">Direct2D will only link adjacent rendering transforms in situations where it is beneficial.</span></span> <span data-ttu-id="2ad17-131">При определении необходимости связывания двух преобразований учитывается несколько факторов.</span><span class="sxs-lookup"><span data-stu-id="2ad17-131">It takes into account multiple factors when determining whether to link two transforms.</span></span> <span data-ttu-id="2ad17-132">Например, связывание шейдера не выполняется, если в одном из преобразований используются вершины или шейдеры вычислений, так как могут быть связаны только шейдеры пикселей.</span><span class="sxs-lookup"><span data-stu-id="2ad17-132">For example, shader linking is not performed if one of the transforms uses vertex or compute shaders, as only pixel shaders can be linked.</span></span> <span data-ttu-id="2ad17-133">Кроме того, если результат не был создан для совместимости с присоединением шейдера, то окружающие преобразования не будут связаны с ним.</span><span class="sxs-lookup"><span data-stu-id="2ad17-133">Also, if an effect was not authored to be compatible with shader linking, then surrounding transforms will not be linked with it.</span></span>

<span data-ttu-id="2ad17-134">Если такая опасность связи существует, Direct2D не будет связывать никакие преобразования, присмежные к опасности, но при этом будет пытаться связать оставшуюся часть графа.</span><span class="sxs-lookup"><span data-stu-id="2ad17-134">In the case that such a linking hazard exists, Direct2D will not link any transforms adjacent to the hazard, but will still attempt to link the remainder of the graph.</span></span>

![Граф преобразования со связью опасности: 2 прохода, 1 промежуточный.](images/shader-linking-graph-hazard.png)

## <a name="authoring-a-shader-linking-compatible-custom-effect"></a><span data-ttu-id="2ad17-136">Создание пользовательского действия, совместимого с шейдером</span><span class="sxs-lookup"><span data-stu-id="2ad17-136">Authoring a shader linking-compatible custom effect</span></span>

<span data-ttu-id="2ad17-137">При создании собственного Direct2Dного действия необходимо убедиться, что его преобразования поддерживают связывание шейдеров эффектов.</span><span class="sxs-lookup"><span data-stu-id="2ad17-137">If you are authoring your own custom Direct2D effect, you need to ensure that its transforms supports effect shader linking.</span></span> <span data-ttu-id="2ad17-138">Это требует внесения некоторых незначительных изменений в реализацию предыдущих пользовательских эффектов.</span><span class="sxs-lookup"><span data-stu-id="2ad17-138">This requires some minor changes from how previous custom effects were implemented.</span></span> <span data-ttu-id="2ad17-139">Если преобразование внутри пользовательского действия не поддерживает связывание с шейдером, Direct2D не будет связывать его с любыми преобразованиями, расположенными рядом с ним на графе эффектов.</span><span class="sxs-lookup"><span data-stu-id="2ad17-139">If a transform within your custom effect does not support shader linking, then Direct2D will not link it with any transforms adjacent to it in the effect graph.</span></span>

<span data-ttu-id="2ad17-140">Разработчик пользовательского действия должен иметь представление о нескольких ключевых понятиях и требованиях:</span><span class="sxs-lookup"><span data-stu-id="2ad17-140">As a custom effect author, you should be aware of several key concepts and requirements:</span></span>

-   <span data-ttu-id="2ad17-141">**Нет изменений в реализации интерфейса Effect**</span><span class="sxs-lookup"><span data-stu-id="2ad17-141">**No changes to effect interface implementations**</span></span>

    <span data-ttu-id="2ad17-142">Нет необходимости изменять код, реализующий различные интерфейсы эффектов, например [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span><span class="sxs-lookup"><span data-stu-id="2ad17-142">You do not need to modify any code implementing the various effect interfaces such as [ID2D1DrawTransform](/windows/win32/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawtransform).</span></span>

-   <span data-ttu-id="2ad17-143">**Предоставьте полную и экспортируемую версию функции шейдеров**</span><span class="sxs-lookup"><span data-stu-id="2ad17-143">**Provide both a full and export function version of shaders**</span></span>

    <span data-ttu-id="2ad17-144">Необходимо указать версию функции экспорта для шейдеров эффектов, которые можно связать с помощью Direct2D.</span><span class="sxs-lookup"><span data-stu-id="2ad17-144">You must provide an export function version of your effect’s shaders which are linkable by Direct2D.</span></span> <span data-ttu-id="2ad17-145">Кроме того, необходимо также продолжить предоставлять исходный, полный шейдер. Это обусловлено тем, что Direct2D выбирает в среде выполнения правую версию шейдера в зависимости от того, применяется ли связывание шейдера к определенной ссылке в графе.</span><span class="sxs-lookup"><span data-stu-id="2ad17-145">In addition, you must also continue to provide the original, full shader; this is because Direct2D selects at runtime the right shader version depending on whether shader linking is to be applied to a particular link in the graph.</span></span>

    <span data-ttu-id="2ad17-146">Если преобразование предоставляет только полный большой двоичный объект шейдера пикселей (через [ID2D1EffectContext:: лоадпикселшадер](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), он не будет связан с смежными преобразованиями.</span><span class="sxs-lookup"><span data-stu-id="2ad17-146">If a transform only provides the full pixel shader blob (via [ID2D1EffectContext::LoadPixelShader](/windows/win32/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadpixelshader)), it will not be linked to adjacent transforms.</span></span>

- <span data-ttu-id="2ad17-147">**Вспомогательные функции**</span><span class="sxs-lookup"><span data-stu-id="2ad17-147">**Helper functions**</span></span>

    <span data-ttu-id="2ad17-148">Direct2D предоставляет [вспомогательные функции](hlsl-helpers.md) и макросы HLSL, которые автоматически создают версии функций шейдера Full и Export.</span><span class="sxs-lookup"><span data-stu-id="2ad17-148">Direct2D provides [HLSL helper functions](hlsl-helpers.md) and macros that will automatically generate both the full and export function versions of a shader.</span></span> <span data-ttu-id="2ad17-149">Эти вспомогательные методы можно найти в d2d1effecthelpers. hlsli.</span><span class="sxs-lookup"><span data-stu-id="2ad17-149">These helpers can be found in d2d1effecthelpers.hlsli.</span></span> <span data-ttu-id="2ad17-150">Кроме того, компилятор HLSL (FXC) позволяет вставить шейдер функции экспорта в закрытое поле в полном шейдере.</span><span class="sxs-lookup"><span data-stu-id="2ad17-150">In addition, the HLSL compiler (FXC) lets you insert the export function shader into a private field in the full shader.</span></span> <span data-ttu-id="2ad17-151">Таким образом, достаточно создать шейдер только один раз и одновременно передать обе версии в Direct2D.</span><span class="sxs-lookup"><span data-stu-id="2ad17-151">In this way, you only need to author a shader once and pass both versions to Direct2D simultaneously.</span></span> <span data-ttu-id="2ad17-152">В состав Windows SDK входит как d2d1effecthelpers. hlsli, так и компилятор FXC.</span><span class="sxs-lookup"><span data-stu-id="2ad17-152">Both d2d1effecthelpers.hlsli and the FXC compiler are included as part of the Windows SDK.</span></span>

    <span data-ttu-id="2ad17-153">Вспомогательные функции:</span><span class="sxs-lookup"><span data-stu-id="2ad17-153">The helper functions:</span></span>

  - [<span data-ttu-id="2ad17-154">D2DGetInput</span><span class="sxs-lookup"><span data-stu-id="2ad17-154">D2DGetInput</span></span>](d2dgetinput.md)  
  - [<span data-ttu-id="2ad17-155">D2DSampleInput</span><span class="sxs-lookup"><span data-stu-id="2ad17-155">D2DSampleInput</span></span>](d2dsampleinput.md)  
  - [<span data-ttu-id="2ad17-156">D2DSampleInputAtOffset</span><span class="sxs-lookup"><span data-stu-id="2ad17-156">D2DSampleInputAtOffset</span></span>](d2dsampleinputatoffset.md)  
  - [<span data-ttu-id="2ad17-157">D2DSampleInputAtPosition</span><span class="sxs-lookup"><span data-stu-id="2ad17-157">D2DSampleInputAtPosition</span></span>](d2dsampleinputatposition.md)  
  - [<span data-ttu-id="2ad17-158">D2DGetInputCoordinate</span><span class="sxs-lookup"><span data-stu-id="2ad17-158">D2DGetInputCoordinate</span></span>](d2dgetinputcoordinate.md)  
  - [<span data-ttu-id="2ad17-159">D2DGetScenePosition</span><span class="sxs-lookup"><span data-stu-id="2ad17-159">D2DGetScenePosition</span></span>](d2dgetsceneposition.md)  
  - [<span data-ttu-id="2ad17-160">\_Запись D2D PS \_</span><span class="sxs-lookup"><span data-stu-id="2ad17-160">D2D\_PS\_ENTRY</span></span>](d2d-ps-entry.md)  

  <span data-ttu-id="2ad17-161">Можно также вручную создать две версии каждого шейдера и скомпилировать их дважды, при условии соблюдения описанных ниже спецификаций в [спецификациях функций экспорта](#export-function-specifications) .</span><span class="sxs-lookup"><span data-stu-id="2ad17-161">You can also manually author two versions of each shader and compile them twice, as long as the specifications described below in [Export function specifications](#export-function-specifications) are met.</span></span>

-   <span data-ttu-id="2ad17-162">**Только шейдеры пикселей**</span><span class="sxs-lookup"><span data-stu-id="2ad17-162">**Pixel shaders only**</span></span>

    <span data-ttu-id="2ad17-163">Direct2D не поддерживает связывание вычислений или шейдеров вершин.</span><span class="sxs-lookup"><span data-stu-id="2ad17-163">Direct2D does not support linking compute or vertex shaders.</span></span> <span data-ttu-id="2ad17-164">Однако если в результате используется шейдер вершин и пиксель, выходные данные шейдера пикселей по-прежнему могут быть связаны.</span><span class="sxs-lookup"><span data-stu-id="2ad17-164">However, if your effect uses both a vertex and pixel shader, the output of the pixel shader can still be linked.</span></span>

-   <span data-ttu-id="2ad17-165">**Простая и сложная выборка**</span><span class="sxs-lookup"><span data-stu-id="2ad17-165">**Simple versus complex sampling**</span></span>

    <span data-ttu-id="2ad17-166">Связывание функций шейдера работает путем соединения выходных данных одного шейдера пикселей к входу последующего прохода шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="2ad17-166">Shader function linking works by connecting the output of one pixel shader pass to the input of a subsequent pixel shader pass.</span></span> <span data-ttu-id="2ad17-167">Это возможно только в том случае, если для выполнения вычислений для построителя текстуры требуется только одно входное значение. Обычно это значение будет получено из выборки текстуры ввода в координатах текстуры, порожденной шейдером вершин.</span><span class="sxs-lookup"><span data-stu-id="2ad17-167">This is only possible when the consuming pixel shader requires only a single input value to perform its computation; this value would normally come from sampling an input texture at the texture coordinate emitted by the vertex shader.</span></span> <span data-ttu-id="2ad17-168">Такой построитель текстуры называется простой выборкой.</span><span class="sxs-lookup"><span data-stu-id="2ad17-168">Such a pixel shader is said to perform simple sampling.</span></span>

    ![Преобразование в градациях серого является примером простой выборки.](images/simple-sampling.png)

    <span data-ttu-id="2ad17-171">Некоторые шейдеры пикселей, такие как размытие по Гауссу, вычисляют выходные данные из нескольких входных выборок, а не только для одного примера.</span><span class="sxs-lookup"><span data-stu-id="2ad17-171">Some pixel shaders, such as a Gaussian blur, compute their output from multiple input samples rather than just a single sample.</span></span> <span data-ttu-id="2ad17-172">Такой построитель текстуры называется выполнением сложной выборки.</span><span class="sxs-lookup"><span data-stu-id="2ad17-172">Such a pixel shader is said to perform complex sampling.</span></span>

    

    ![Пример сложной выборки — Размытие по Гауссу.](images/complex-sampling.png)

    
    <span data-ttu-id="2ad17-175">Входные данные, предоставляемые другой функцией шейдера, могут быть представлены только функциями шейдера с простыми входными данными.</span><span class="sxs-lookup"><span data-stu-id="2ad17-175">Only shader functions with simple inputs can have their input provided by another shader function.</span></span> <span data-ttu-id="2ad17-176">Функции шейдеров со сложными входными данными должны быть предоставлены с текстурой ввода для выборки.</span><span class="sxs-lookup"><span data-stu-id="2ad17-176">Shader functions with complex inputs must be provided with an input texture to sample.</span></span> <span data-ttu-id="2ad17-177">Это означает, что Direct2D не будет связывать шейдер со сложными входными данными для его предшественника.</span><span class="sxs-lookup"><span data-stu-id="2ad17-177">This means that Direct2D will not link a shader with complex inputs to its predecessor.</span></span>

    <span data-ttu-id="2ad17-178">При использовании [вспомогательных функций DIRECT2D HLSL](hlsl-helpers.md)необходимо указать в HLSL, использует ли шейдер сложные или простые входы.</span><span class="sxs-lookup"><span data-stu-id="2ad17-178">When using the [Direct2D HLSL helpers](hlsl-helpers.md), you must indicate in the HLSL whether a shader uses complex or simple inputs.</span></span>

## <a name="example-linking-compatible-effect-shader"></a><span data-ttu-id="2ad17-179">Пример связывания. совместимый шейдер эффектов</span><span class="sxs-lookup"><span data-stu-id="2ad17-179">Example linking-compatible effect shader</span></span>

<span data-ttu-id="2ad17-180">С помощью вспомогательных функций D2D следующий фрагмент кода представляет простой совместимый с связыванием шейдер эффектов:</span><span class="sxs-lookup"><span data-stu-id="2ad17-180">Using the D2D helpers, the following code snippet represents a simple linking-compatible effect shader:</span></span>

```syntax
#define D2D_INPUT_COUNT 1
#define D2D_INPUT0_SIMPLE
#include “d2d1effecthelpers.hlsli”

D2D_PS_ENTRY(LinkingCompatiblePixelShader)
{
    float4 input = D2DGetInput(0);
    input.rgb *= input.a;
    return input;
}          
```

<span data-ttu-id="2ad17-181">В этом коротком примере обратите внимание, что не объявлены параметры функции, что число входов и типов каждого входного параметра объявляется перед функцией ввода, входные данные извлекаются путем вызова [D2DGetInput](d2dgetinput.md), а эти директивы препроцессора должны быть определены до включения вспомогательного файла.</span><span class="sxs-lookup"><span data-stu-id="2ad17-181">In this short example note that no function parameters are declared, that the number of inputs and type of each input is declared before the entry function, the input is retrieved by calling [D2DGetInput](d2dgetinput.md), and that preprocessor directives must be defined before the helper file is included.</span></span>

<span data-ttu-id="2ad17-182">Совместимый с связыванием шейдер должен предоставлять как обычный шейдер пикселей с одним проходом, так и функцию шейдера экспорта.</span><span class="sxs-lookup"><span data-stu-id="2ad17-182">A linking-compatible shader must provide both a regular single-pass pixel shader and an export shader function.</span></span> <span data-ttu-id="2ad17-183">Макрос [ \_ \_ записи D2D PS](d2d-ps-entry.md) позволяет создавать их из одного и того же кода при использовании в сочетании с скриптом компиляции шейдера.</span><span class="sxs-lookup"><span data-stu-id="2ad17-183">The [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro allows each of these to be generated from the same code, when used in conjunction with the shader compilation script.</span></span>

<span data-ttu-id="2ad17-184">При компиляции полного шейдера макросы разворачиваются в следующий код, имеющий входную подпись, совместимую с эффектами D2D.</span><span class="sxs-lookup"><span data-stu-id="2ad17-184">When compiling a full shader, the macros are expanded into the following code, which has a D2D Effects-compatible input signature.</span></span>

```syntax
Texture2D<float4> InputTexture0;
SamplerState InputSampler0;

float4 LinkingCompatiblePixelShader(
    float4 pos   : SV_POSITION,
    float4 posScene : SCENE_POSITION,
    float4 uv0  : TEXCOORD0
    ) : SV_Target
    {
        float4 input = InputTexture0.Sample(InputSampler0, uv0.xy);
        input.rgb *= input.a;
        return input;
    }    
```

<span data-ttu-id="2ad17-185">При компиляции версии функции экспорта одного и того же кода создается следующий код:</span><span class="sxs-lookup"><span data-stu-id="2ad17-185">When compiling an export function version of the same code, the following code is generated:</span></span>

```syntax
// Shader function version
export float4 LinkingCompatiblePixelShader_Function(
    float4 input0 : INPUT0)
    {
        input.rgb *= input.a;
        return input;
    }      
```

<span data-ttu-id="2ad17-186">Обратите внимание, что входные данные текстуры, обычно получаемые с помощью выборки Texture2D, заменены на входные функции (input0).</span><span class="sxs-lookup"><span data-stu-id="2ad17-186">Note that the texture input, normally retrieved by sampling a Texture2D, has been replaced with a function input (input0).</span></span>

<span data-ttu-id="2ad17-187">Чтобы просмотреть полное пошаговое описание действий, которые необходимо выполнить для написания совместимого с связью эффекта, см. [руководство по пользовательским эффектам](custom-effects.md) и [Пример пользовательских изображений Direct2D](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span><span class="sxs-lookup"><span data-stu-id="2ad17-187">To see a full, step by step description of what you need to do to write a linking-compatible effect, see the [Custom effects tutorial](custom-effects.md) and the [Direct2D custom image effects sample](https://github.com/microsoft/Windows-universal-samples/tree/master/Samples/D2DCustomEffects).</span></span>

## <a name="compiling-a-linking-compatible-shader"></a><span data-ttu-id="2ad17-188">Компиляция совместимого шейдера связывания</span><span class="sxs-lookup"><span data-stu-id="2ad17-188">Compiling a linking compatible-shader</span></span>

<span data-ttu-id="2ad17-189">Чтобы обеспечить возможность связи, большой двоичный объект шейдера пикселей, переданный в D2D, должен содержать как полные, так и экспортируемые версии функций шейдера.</span><span class="sxs-lookup"><span data-stu-id="2ad17-189">To be linkable, the pixel shader blob passed to D2D must contain both the full and export function versions of the shader.</span></span> <span data-ttu-id="2ad17-190">Это достигается путем встраивания скомпилированной функции экспорта в \_ \_ область частных данных D3D BLOB \_ .</span><span class="sxs-lookup"><span data-stu-id="2ad17-190">This is accomplished by embedding the compiled export function into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>

<span data-ttu-id="2ad17-191">Когда шейдеры создаются с помощью вспомогательных функций D2D, целевой объект компиляции D2D должен быть определен во время компиляции.</span><span class="sxs-lookup"><span data-stu-id="2ad17-191">When the shaders are authored with the D2D helper functions, a D2D compilation target must be defined at compilation time.</span></span> <span data-ttu-id="2ad17-192">Целевыми типами компиляции являются \_ полный \_ шейдер D2D и функция D2D \_ .</span><span class="sxs-lookup"><span data-stu-id="2ad17-192">The compilation target types are D2D\_FULL\_SHADER and D2D\_FUNCTION.</span></span>

<span data-ttu-id="2ad17-193">Компиляция построителя эффектов, совместимых с связыванием, состоит из двух этапов:</span><span class="sxs-lookup"><span data-stu-id="2ad17-193">Compiling a linking-compatible effect shader is a two-step process:</span></span>

-   [<span data-ttu-id="2ad17-194">Компиляция функции экспорта</span><span class="sxs-lookup"><span data-stu-id="2ad17-194">Compile the export function</span></span>](#step-1-compile-the-export-function)
-   [<span data-ttu-id="2ad17-195">Скомпилируйте полный шейдер и внедрите функцию экспорта</span><span class="sxs-lookup"><span data-stu-id="2ad17-195">Compile the full shader and embed the export function</span></span>](#step-2-compile-the-full-shader-and-embed-the-export-function)

> [!Note]  
> <span data-ttu-id="2ad17-196">При компиляции воздействия с помощью Visual Studio следует создать пакетный файл, выполняющий обе команды FXC, и запустить этот пакетный файл в качестве настраиваемого этапа сборки, запускаемого до этапа компиляции.</span><span class="sxs-lookup"><span data-stu-id="2ad17-196">When compiling an effect using Visual Studio, you should create a batch file that executes both FXC commands and run this batch file as a custom build step that runs before the compile step.</span></span>

 

### <a name="step-1-compile-the-export-function"></a><span data-ttu-id="2ad17-197">Шаг 1. компиляция функции экспорта</span><span class="sxs-lookup"><span data-stu-id="2ad17-197">Step 1: Compile the export function</span></span>

```syntax
fxc /T <shadermodel> <MyShaderFile>.hlsl /D D2D_FUNCTION /D D2D_ENTRY=<entry> /Fl <MyShaderFile>.fxlib           
```

<span data-ttu-id="2ad17-198">Чтобы скомпилировать версию функции экспорта шейдера, необходимо передать следующие флаги в FXC.</span><span class="sxs-lookup"><span data-stu-id="2ad17-198">To compile the export function version of your shader, you must pass the following flags to FXC.</span></span>



|    <span data-ttu-id="2ad17-199">Flag</span><span class="sxs-lookup"><span data-stu-id="2ad17-199">Flag</span></span>                            |    <span data-ttu-id="2ad17-200">Описание</span><span class="sxs-lookup"><span data-stu-id="2ad17-200">Description</span></span>                       |
|--------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad17-201">/T <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="2ad17-201">/T <ShaderModel></span></span>         | <span data-ttu-id="2ad17-202">Задайте <ShaderModel> соответствующий профиль шейдера пикселей, как определено в [синтаксисе FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span><span class="sxs-lookup"><span data-stu-id="2ad17-202">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="2ad17-203">Это должен быть один из профилей, перечисленных в разделе "Связывание шейдера HLSL".</span><span class="sxs-lookup"><span data-stu-id="2ad17-203">This must be one of the profiles listed under “HLSL shader linking”.</span></span> |
| <span data-ttu-id="2ad17-204"><MyShaderFile>. HLSL</span><span class="sxs-lookup"><span data-stu-id="2ad17-204"><MyShaderFile>.hlsl</span></span>      | <span data-ttu-id="2ad17-205">Задайте <MyShaderFile> для имя файла HLSL.</span><span class="sxs-lookup"><span data-stu-id="2ad17-205">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                    |
| <span data-ttu-id="2ad17-206">/D D2D, \_ функция</span><span class="sxs-lookup"><span data-stu-id="2ad17-206">/D D2D\_FUNCTION</span></span>               | <span data-ttu-id="2ad17-207">Это определение указывает FXC скомпилировать версию функции экспорта шейдера.</span><span class="sxs-lookup"><span data-stu-id="2ad17-207">This definition instructs FXC to compile the export function version of the shader.</span></span>                                                                                                                                                                       |
| <span data-ttu-id="2ad17-208">/D \_ запись D2D =<entry></span><span class="sxs-lookup"><span data-stu-id="2ad17-208">/D D2D\_ENTRY=<entry></span></span>    | <span data-ttu-id="2ad17-209">Задайте <entry> имя точки входа HLSL, которая была определена в макросе [ \_ \_ записи D2D PS](d2d-ps-entry.md) .</span><span class="sxs-lookup"><span data-stu-id="2ad17-209">Set <entry> to the name of the HLSL entry point you defined inside the [D2D\_PS\_ENTRY](d2d-ps-entry.md) macro.</span></span>                                                                                                                                    |
| <span data-ttu-id="2ad17-210">/ФЛ <MyShaderFile> . фкслиб</span><span class="sxs-lookup"><span data-stu-id="2ad17-210">/Fl <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="2ad17-211">Задайте в качестве значения, <MyShaderfile> где будет храниться версия функции экспорта шейдера.</span><span class="sxs-lookup"><span data-stu-id="2ad17-211">Set <MyShaderfile> to where you want to store the export function version of the shader.</span></span> <span data-ttu-id="2ad17-212">Обратите внимание, что расширение. фкслиб предназначено только для простоты идентификации.</span><span class="sxs-lookup"><span data-stu-id="2ad17-212">Note the .fxlib extension is only for ease of identification.</span></span>                                                                                              |

### <a name="step-2-compile-the-full-shader-and-embed-the-export-function"></a><span data-ttu-id="2ad17-213">Шаг 2. Компиляция полного шейдера и встраивание функции экспорта</span><span class="sxs-lookup"><span data-stu-id="2ad17-213">Step 2: Compile the full shader and embed the export function</span></span>

```syntax
fxc /T ps_<shadermodel> <MyShaderFile>.hlsl /D D2D_FULL_SHADER /D D2D_ENTRY=<entry> /E <entry> /setprivate <MyShaderFile>.fxlib /Fo <MyShader>.cso /Fh <MyShader>.h           
```

<span data-ttu-id="2ad17-214">Чтобы скомпилировать полную версию шейдера с внедренной версией экспорта, необходимо передать следующие флаги в FXC.</span><span class="sxs-lookup"><span data-stu-id="2ad17-214">To compile the full version of your shader with embedded export version, you must pass the following flags to FXC.</span></span>



|    <span data-ttu-id="2ad17-215">Flag</span><span class="sxs-lookup"><span data-stu-id="2ad17-215">Flag</span></span>                                    |    <span data-ttu-id="2ad17-216">Описание</span><span class="sxs-lookup"><span data-stu-id="2ad17-216">Description</span></span>                     |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ad17-217">/T <ShaderModel></span><span class="sxs-lookup"><span data-stu-id="2ad17-217">/T <ShaderModel></span></span>                 | <span data-ttu-id="2ad17-218">Задайте <ShaderModel> соответствующий профиль шейдера пикселей, как определено в [синтаксисе FXC](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span><span class="sxs-lookup"><span data-stu-id="2ad17-218">Set <ShaderModel> to the appropriate pixel shader profile as defined in [FXC Syntax](/windows/desktop/direct3dtools/dx-graphics-tools-fxc-syntax).</span></span> <span data-ttu-id="2ad17-219">Это должен быть профиль шейдера пикселей, соответствующий профилю связывания, указанному на шаге 1.</span><span class="sxs-lookup"><span data-stu-id="2ad17-219">This must be the pixel shader profile corresponding to the linking profile specified in Step 1.</span></span> |
| <span data-ttu-id="2ad17-220"><MyShaderFile>. HLSL</span><span class="sxs-lookup"><span data-stu-id="2ad17-220"><MyShaderFile>.hlsl</span></span>              | <span data-ttu-id="2ad17-221">Задайте <MyShaderFile> для имя файла HLSL.</span><span class="sxs-lookup"><span data-stu-id="2ad17-221">Set <MyShaderFile> to the name of the HLSL file.</span></span>                                                                                                                                                                                                                               |
| <span data-ttu-id="2ad17-222">/D \_ полный \_ шейдер D2D</span><span class="sxs-lookup"><span data-stu-id="2ad17-222">/D D2D\_FULL\_SHADER</span></span>                   | <span data-ttu-id="2ad17-223">Это определение указывает FXC скомпилировать полную версию шейдера.</span><span class="sxs-lookup"><span data-stu-id="2ad17-223">This definition instructs FXC to compile the full version of the shader.</span></span>                                                                                                                                                                                                             |
| <span data-ttu-id="2ad17-224">/D \_ запись D2D =<entry></span><span class="sxs-lookup"><span data-stu-id="2ad17-224">/D D2D\_ENTRY=<entry></span></span>            | <span data-ttu-id="2ad17-225">Задайте <entry> для параметра имя точки входа HLSL, которая была определена в \_ \_ макросе записи D2D PS ().</span><span class="sxs-lookup"><span data-stu-id="2ad17-225">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="2ad17-226">/E <entry></span><span class="sxs-lookup"><span data-stu-id="2ad17-226">/E <entry></span></span>                       | <span data-ttu-id="2ad17-227">Задайте <entry> для параметра имя точки входа HLSL, которая была определена в \_ \_ макросе записи D2D PS ().</span><span class="sxs-lookup"><span data-stu-id="2ad17-227">Set <entry> to the name of the HLSL entry point you defined inside the D2D\_PS\_ENTRY() macro.</span></span>                                                                                                                                                                                 |
| <span data-ttu-id="2ad17-228">/сетпривате <MyShaderFile> . фкслиб</span><span class="sxs-lookup"><span data-stu-id="2ad17-228">/setprivate <MyShaderFile>.fxlib</span></span> | <span data-ttu-id="2ad17-229">Этот аргумент указывает FXC внедрить функцию экспорта шейдера, созданную на шаге 1, в \_ \_ область частных данных для BLOB-объекта D3D \_ .</span><span class="sxs-lookup"><span data-stu-id="2ad17-229">This argument instructs FXC to embed the export function shader generated in step 1 into the D3D\_BLOB\_PRIVATE\_DATA area.</span></span>                                                                                                                                                          |
| <span data-ttu-id="2ad17-230">/FO <MyShader> . cso</span><span class="sxs-lookup"><span data-stu-id="2ad17-230">/Fo <MyShader>.cso</span></span>               | <span data-ttu-id="2ad17-231">Задайте <MyShader> для параметра значение, где нужно сохранить окончательный Объединенный Скомпилированный шейдер.</span><span class="sxs-lookup"><span data-stu-id="2ad17-231">Set <MyShader> to where you want to store the final, combined compiled shader.</span></span>                                                                                                                                                                                                 |
| <span data-ttu-id="2ad17-232">/ФХ <MyShader> . h</span><span class="sxs-lookup"><span data-stu-id="2ad17-232">/Fh <MyShader>.h</span></span>                 | <span data-ttu-id="2ad17-233">Задайте <MyShader> для параметра значение, где вы хотите сохранить окончательный Объединенный заголовок.</span><span class="sxs-lookup"><span data-stu-id="2ad17-233">Set <MyShader> to where you want to store the final, combined header.</span></span>                                                                                                                                                                                                          |

## <a name="export-function-specifications"></a><span data-ttu-id="2ad17-234">Экспорт спецификаций функций</span><span class="sxs-lookup"><span data-stu-id="2ad17-234">Export function specifications</span></span>

<span data-ttu-id="2ad17-235">Возможно, не рекомендуется — создать совместимый шейдер эффектов без использования вспомогательных средств, предоставляемых преобразователем D2D.</span><span class="sxs-lookup"><span data-stu-id="2ad17-235">It is possible – though not recommended – to author a compatible effect shader without using the D2D-provided helpers.</span></span> <span data-ttu-id="2ad17-236">Необходимо соблюдать осторожность, чтобы убедиться, что все входные подписи функции шейдера и экспорта функций соответствуют спецификациям D2D.</span><span class="sxs-lookup"><span data-stu-id="2ad17-236">Care must be taken to ensure that both the full shader and export function input signatures conform to D2D specifications.</span></span>

<span data-ttu-id="2ad17-237">Спецификации для полных шейдеров являются теми же, что и в предыдущих версиях Windows.</span><span class="sxs-lookup"><span data-stu-id="2ad17-237">The specifications for full shaders are the same as earlier Windows versions.</span></span> <span data-ttu-id="2ad17-238">Вкратце, входные параметры шейдера пикселей должны быть \_ ПОЛОЖЕНИЕМ SV, \_ позицией сцены и одним текскурд на входные данные.</span><span class="sxs-lookup"><span data-stu-id="2ad17-238">Briefly, the pixel shader input parameters must be SV\_POSITION, SCENE\_POSITION, and one TEXCOORD per effect input.</span></span>

<span data-ttu-id="2ad17-239">Для функции экспорта функция должна возвращать float4, а ее входные данные должны быть одного из следующих типов:</span><span class="sxs-lookup"><span data-stu-id="2ad17-239">For the export function, the function must return a float4 and its inputs must be one of the following types:</span></span>

-   <span data-ttu-id="2ad17-240">Простой ввод</span><span class="sxs-lookup"><span data-stu-id="2ad17-240">Simple input</span></span>

    ```syntax
    float4 d2d_inputN : INPUTN         
    ```

    <span data-ttu-id="2ad17-241">Для простых входных данных D2D вставляет образец функции между текстурой ввода и функцией шейдера, либо входные данные будут предоставлены выходом другой функции шейдера.</span><span class="sxs-lookup"><span data-stu-id="2ad17-241">For simple inputs, D2D will either insert a Sample function between the input texture and shader function, or the input will be provided by the output of another shader function.</span></span>

-   <span data-ttu-id="2ad17-242">Сложный ввод</span><span class="sxs-lookup"><span data-stu-id="2ad17-242">Complex input</span></span>

    ```syntax
    float4 d2d_uvN  : TEXCOORDN                
    ```

    <span data-ttu-id="2ad17-243">Для сложных входов D2D будет передавать только координату текстуры, как описано в документации по Windows 8.</span><span class="sxs-lookup"><span data-stu-id="2ad17-243">For complex inputs, D2D will only pass a texture coordinate as described in Windows 8 documentation.</span></span>

-   <span data-ttu-id="2ad17-244">Расположение выходных данных</span><span class="sxs-lookup"><span data-stu-id="2ad17-244">Output location</span></span>

    ```syntax
    float4 d2d_posScene : SCENE_POSITION                
    ```

    <span data-ttu-id="2ad17-245">Можно определить только один ввод на одну \_ точку сцены.</span><span class="sxs-lookup"><span data-stu-id="2ad17-245">Only one SCENE\_POSITION input can be defined.</span></span> <span data-ttu-id="2ad17-246">Этот параметр следует включать только при необходимости, так как только одна функция на связанный шейдер может использовать этот параметр.</span><span class="sxs-lookup"><span data-stu-id="2ad17-246">This parameter should only be included when necessary, since only one function per linked shader can utilize this parameter.</span></span>

<span data-ttu-id="2ad17-247">Семантика должна быть определена как приведенная выше, так как D2D проверяет семантику, чтобы решить, как связать функции вместе.</span><span class="sxs-lookup"><span data-stu-id="2ad17-247">The semantics must be defined as above, as D2D will inspect the semantics to decide how to link functions together.</span></span> <span data-ttu-id="2ad17-248">Если входные данные функции не соответствуют одному из перечисленных выше типов, функция будет отклонена для связывания с шейдером.</span><span class="sxs-lookup"><span data-stu-id="2ad17-248">If any function input does not match one of the above types, the function will be rejected for shader linking.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ad17-249">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2ad17-249">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ad17-250">Вспомогательные методы HLSL</span><span class="sxs-lookup"><span data-stu-id="2ad17-250">HLSL Helpers</span></span>](hlsl-helpers.md)
</dt> <dt>

[<span data-ttu-id="2ad17-251">Интерфейс ID3D11Linker</span><span class="sxs-lookup"><span data-stu-id="2ad17-251">ID3D11Linker interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11linker)
</dt> <dt>

[<span data-ttu-id="2ad17-252">Интерфейс ID3D11FunctionLinkingGraph</span><span class="sxs-lookup"><span data-stu-id="2ad17-252">ID3D11FunctionLinkingGraph interface</span></span>](/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11functionlinkinggraph)
</dt> </dl>

 

 