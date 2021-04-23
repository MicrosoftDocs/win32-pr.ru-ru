---
title: Различия между эффектами 10 и Effects 11
description: В этом разделе показаны различия между эффектами 10 и 11.
ms.assetid: c3e5e6bc-c544-49ee-b6d9-021ce87f9b12
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29af1b9e7aec72f96a62e0f62668b81a6eec8367
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792324"
---
# <a name="differences-between-effects-10-and-effects-11"></a><span data-ttu-id="6191c-103">Различия между эффектами 10 и Effects 11</span><span class="sxs-lookup"><span data-stu-id="6191c-103">Differences Between Effects 10 and Effects 11</span></span>

<span data-ttu-id="6191c-104">В этом разделе показаны различия между эффектами 10 и 11.</span><span class="sxs-lookup"><span data-stu-id="6191c-104">This topic shows the differences between Effects 10 and Effects 11.</span></span>

## <a name="device-contexts-threading-and-cloning"></a><span data-ttu-id="6191c-105">Контексты устройств, потоки и клонирование</span><span class="sxs-lookup"><span data-stu-id="6191c-105">Device Contexts, Threading, and Cloning</span></span>

<span data-ttu-id="6191c-106">Интерфейс ID3D10Device разделен на два интерфейса в Direct3D 11: ID3D11Device и ссылку ID3D11DeviceContext.</span><span class="sxs-lookup"><span data-stu-id="6191c-106">The ID3D10Device interface has been split into two interfaces in Direct3D 11: ID3D11Device and ID3D11DeviceContext.</span></span> <span data-ttu-id="6191c-107">Можно создать несколько ID3D11DeviceContexts, чтобы упростить параллельное выполнение в нескольких потоках.</span><span class="sxs-lookup"><span data-stu-id="6191c-107">You can create multiple ID3D11DeviceContexts to facilitate concurrent execution on multiple threads.</span></span> <span data-ttu-id="6191c-108">Эффекты 11 расширяют эту концепцию до платформы Effects.</span><span class="sxs-lookup"><span data-stu-id="6191c-108">Effects 11 extends this concept to the Effects framework.</span></span>

<span data-ttu-id="6191c-109">Среда выполнения Effects 11 является однопотоковой.</span><span class="sxs-lookup"><span data-stu-id="6191c-109">The Effects 11 runtime is single-threaded.</span></span> <span data-ttu-id="6191c-110">По этой причине не следует использовать один экземпляр ID3DX11Effect с несколькими потоками одновременно.</span><span class="sxs-lookup"><span data-stu-id="6191c-110">For this reason, you should not use a single ID3DX11Effect instance with multiple threads concurrently.</span></span>

<span data-ttu-id="6191c-111">Чтобы использовать среду выполнения Effects 11 на нескольких экземплярах, необходимо создать отдельные экземпляры ID3DX11Effect.</span><span class="sxs-lookup"><span data-stu-id="6191c-111">To use the Effects 11 runtime on multiple instances, you must create separate ID3DX11Effect instances.</span></span> <span data-ttu-id="6191c-112">Так как ссылку ID3D11DeviceContext также является однопотоковым, необходимо передавать разные экземпляры ссылку ID3D11DeviceContext в каждый экземпляр Effect в Apply.</span><span class="sxs-lookup"><span data-stu-id="6191c-112">Because the ID3D11DeviceContext is also single-threaded, you should pass different ID3D11DeviceContext instances to each effect instance on Apply.</span></span> <span data-ttu-id="6191c-113">Эти отдельные контексты устройств можно использовать для создания списков команд, чтобы поток отрисовки мог применить их к контексту немедленного устройства.</span><span class="sxs-lookup"><span data-stu-id="6191c-113">You can use these separate device contexts to create command lists so that the rendering thread can apply them on the immediate device context.</span></span>

<span data-ttu-id="6191c-114">Самый простой способ создать несколько эффектов, которые инкапсулируют одну и ту же функциональность для использования в нескольких потоках, — создать один эффект, а затем создать клонированные копии.</span><span class="sxs-lookup"><span data-stu-id="6191c-114">The easiest way to create multiple effects that encapsulate the same functionality, for use on multiple threads, is to create one effect and then make cloned copies.</span></span> <span data-ttu-id="6191c-115">Клонирование имеет следующие преимущества по сравнению с созданием нескольких копий с нуля:</span><span class="sxs-lookup"><span data-stu-id="6191c-115">Cloning has the following advantages over creating multiple copies from scratch:</span></span>

1.  <span data-ttu-id="6191c-116">Подпрограммы клонирования выполняются быстрее, чем подпрограммы создания.</span><span class="sxs-lookup"><span data-stu-id="6191c-116">The cloning routine is faster than the creation routine.</span></span>
2.  <span data-ttu-id="6191c-117">Клонированные эффекты совместно используют созданные шейдеры, блоки состояний и экземпляры классов (поэтому их не нужно создавать повторно).</span><span class="sxs-lookup"><span data-stu-id="6191c-117">Cloned effects share created shaders, state blocks, and class instances (so they don't have to be recreated).</span></span>
3.  <span data-ttu-id="6191c-118">Клонированные эффекты могут совместно использовать буферы констант.</span><span class="sxs-lookup"><span data-stu-id="6191c-118">Cloned effects can share constant buffers.</span></span>
4.  <span data-ttu-id="6191c-119">Клонированные эффекты начинаются с состояния, которое соответствует текущему эффекту (значения переменных, независимо от того, была ли она оптимизирована).</span><span class="sxs-lookup"><span data-stu-id="6191c-119">Cloned effects begin with state that matches the current effect (variable values, whether or not it has been optimized).</span></span>

<span data-ttu-id="6191c-120">Дополнительные сведения см. [в разделе клонирование влияния](d3d11-graphics-programming-guide-effects-cloning.md) .</span><span class="sxs-lookup"><span data-stu-id="6191c-120">See [Cloning an Effect](d3d11-graphics-programming-guide-effects-cloning.md) for more information.</span></span>

## <a name="effect-pools-and-groups"></a><span data-ttu-id="6191c-121">Пулы и группы эффектов</span><span class="sxs-lookup"><span data-stu-id="6191c-121">Effect Pools and Groups</span></span>

<span data-ttu-id="6191c-122">До сих пор наиболее распространенным использованием пулов эффектов в Direct3D 10 было для группирования материалов.</span><span class="sxs-lookup"><span data-stu-id="6191c-122">By far the most prevalent use of effect pools in Direct3D 10 was for grouping materials.</span></span> <span data-ttu-id="6191c-123">Пулы эффектов были удалены из эффектов 11, а группы были добавлены, что является более эффективным способом группирования материалов.</span><span class="sxs-lookup"><span data-stu-id="6191c-123">Effect Pools have been removed from Effects 11 and groups have been added, which is a more efficient method of grouping materials.</span></span>

<span data-ttu-id="6191c-124">Группа эффектов — это просто набор приемов.</span><span class="sxs-lookup"><span data-stu-id="6191c-124">An effect group is simply a set of techniques.</span></span> <span data-ttu-id="6191c-125">Дополнительные сведения см. в разделе [синтаксис группы эффектов (Direct3D 11)](d3d11-effect-group-syntax.md) .</span><span class="sxs-lookup"><span data-stu-id="6191c-125">See [Effect Group Syntax (Direct3D 11)](d3d11-effect-group-syntax.md) for more information.</span></span>

<span data-ttu-id="6191c-126">Рассмотрим следующую иерархию эффектов с четырьмя дочерними эффектами и одним пулом эффектов:</span><span class="sxs-lookup"><span data-stu-id="6191c-126">Consider the following effect hierarchy with four child effects and one effect pool:</span></span>


```
// Effect Pool
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

// Effect Child 1
#include "EffectPool.fx"
technique10 GrassMaterialLowSpec { ... }

// Effect Child 2
#include "EffectPool.fx"
technique10 GrassMaterialHighSpec { ... }

// Effect Child 3
#include "EffectPool.fx"
technique10 WaterMaterialLowSpec { ... }

// Effect Child 4
#include "EffectPool.fx"
technique10 WaterMaterialHighSpec { ... }
```



<span data-ttu-id="6191c-127">Вы можете добиться тех же функций в эффекте 11 с помощью групп:</span><span class="sxs-lookup"><span data-stu-id="6191c-127">You can achieve the same functionality in Effects 11 by using groups:</span></span>


```
cbufer A { ... }
PixelShader pPSGrass;
PixelShader pPSWater;

fxgroup GrassMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}

fxgroup WaterMaterial
{
    technique10 LowSpec { ... }
    technique10 HighSpec { ... }
}
```



## <a name="new-shader-stages"></a><span data-ttu-id="6191c-128">Новые этапы шейдера</span><span class="sxs-lookup"><span data-stu-id="6191c-128">New Shader Stages</span></span>

<span data-ttu-id="6191c-129">В Direct3D 11 есть три новых этапа шейдера: шейдер поверхности, Шейдер доменов и шейдер вычислений.</span><span class="sxs-lookup"><span data-stu-id="6191c-129">There are three new shader stages in Direct3D 11: the hull shader, domain shader, and compute shader.</span></span> <span data-ttu-id="6191c-130">Эффекты 11 обрабатывают их подобным образом для шейдеров вершин, шейдеров geometry и шейдеров пикселей.</span><span class="sxs-lookup"><span data-stu-id="6191c-130">Effects 11 handles these in a similar manner to vertex shaders, geometry shaders, and pixel shaders.</span></span>

<span data-ttu-id="6191c-131">В эффекты 11 были добавлены три новых типа переменных.</span><span class="sxs-lookup"><span data-stu-id="6191c-131">Three new variable types have been added to Effects 11:</span></span>

-   <span data-ttu-id="6191c-132">хуллшадер</span><span class="sxs-lookup"><span data-stu-id="6191c-132">HullShader</span></span>
-   <span data-ttu-id="6191c-133">домаиншадер</span><span class="sxs-lookup"><span data-stu-id="6191c-133">DomainShader</span></span>
-   <span data-ttu-id="6191c-134">компутешадер</span><span class="sxs-lookup"><span data-stu-id="6191c-134">ComputeShader</span></span>

<span data-ttu-id="6191c-135">При использовании этих шейдеров в приеме необходимо пометить этот метод «technique11», а не «technique10».</span><span class="sxs-lookup"><span data-stu-id="6191c-135">If you use these shaders in a technique, you must label that technique "technique11", and not "technique10".</span></span> <span data-ttu-id="6191c-136">Невозможно задать шейдер вычислений в том же процессе, что и любое другое графическое состояние (другие шейдеры, блоки состояний или целевые объекты прорисовки).</span><span class="sxs-lookup"><span data-stu-id="6191c-136">The compute shader cannot be set in the same pass as any other graphics state (other shaders, state blocks, or render targets).</span></span>

## <a name="new-texture-types"></a><span data-ttu-id="6191c-137">Новые типы текстур</span><span class="sxs-lookup"><span data-stu-id="6191c-137">New Texture Types</span></span>

<span data-ttu-id="6191c-138">Direct3D 11 поддерживает следующие типы текстур:</span><span class="sxs-lookup"><span data-stu-id="6191c-138">Direct3D 11 supports the following texture types:</span></span>

-   [<span data-ttu-id="6191c-139">аппендструктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="6191c-139">AppendStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-appendstructuredbuffer)
-   [<span data-ttu-id="6191c-140">битеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="6191c-140">ByteAddressBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-byteaddressbuffer)
-   [<span data-ttu-id="6191c-141">консуместруктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="6191c-141">ConsumeStructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-consumestructuredbuffer)
-   [<span data-ttu-id="6191c-142">структуредбуффер</span><span class="sxs-lookup"><span data-stu-id="6191c-142">StructuredBuffer</span></span>](/windows/desktop/direct3dhlsl/sm5-object-structuredbuffer)

## <a name="unordered-access-views"></a><span data-ttu-id="6191c-143">Представления неупорядоченного доступа</span><span class="sxs-lookup"><span data-stu-id="6191c-143">Unordered Access Views</span></span>

<span data-ttu-id="6191c-144">Эффекты 11 поддерживают получение и установку новых типов представлений неупорядоченного доступа.</span><span class="sxs-lookup"><span data-stu-id="6191c-144">Effects 11 supports getting and setting the new unordered access view types.</span></span> <span data-ttu-id="6191c-145">Это работает аналогично текстурам.</span><span class="sxs-lookup"><span data-stu-id="6191c-145">This works in a similar manner as textures.</span></span>

<span data-ttu-id="6191c-146">Рассмотрим этот эффект в HLSL примере:</span><span class="sxs-lookup"><span data-stu-id="6191c-146">Consider this Effects HLSL example:</span></span>


```
  
RWTexture1D<float> myUAV;
```



<span data-ttu-id="6191c-147">Эту переменную можно задать в C++ следующим образом:</span><span class="sxs-lookup"><span data-stu-id="6191c-147">You can set this variable in C++ as follows:</span></span>


```
  
ID3D11UnorderedAccessView* pUAVTexture1D = NULL;
ID3DX11EffectUnorderedAccessViewVariable* pUAVVar;
pUAVVar = pEffect->GetVariableByName("myUAV")->AsUnorderedAccessView();
pUAVVar->SetUnorderedAccessView( pUAVTexture1D );
```



<span data-ttu-id="6191c-148">Direct3D 11 поддерживает следующие неупорядоченные типы представлений доступа:</span><span class="sxs-lookup"><span data-stu-id="6191c-148">Direct3D 11 supports the following unordered access view types:</span></span>

-   <span data-ttu-id="6191c-149">рвбуффер</span><span class="sxs-lookup"><span data-stu-id="6191c-149">RWBuffer</span></span>
-   <span data-ttu-id="6191c-150">рвбитеаддрессбуффер</span><span class="sxs-lookup"><span data-stu-id="6191c-150">RWByteAddressBuffer</span></span>
-   <span data-ttu-id="6191c-151">рвструктуредбуффер</span><span class="sxs-lookup"><span data-stu-id="6191c-151">RWStructuredBuffer</span></span>
-   <span data-ttu-id="6191c-152">RWTexture1D</span><span class="sxs-lookup"><span data-stu-id="6191c-152">RWTexture1D</span></span>
-   <span data-ttu-id="6191c-153">RWTexture1DArray</span><span class="sxs-lookup"><span data-stu-id="6191c-153">RWTexture1DArray</span></span>
-   <span data-ttu-id="6191c-154">RWTexture2D</span><span class="sxs-lookup"><span data-stu-id="6191c-154">RWTexture2D</span></span>
-   <span data-ttu-id="6191c-155">RWTexture2DArray</span><span class="sxs-lookup"><span data-stu-id="6191c-155">RWTexture2DArray</span></span>
-   <span data-ttu-id="6191c-156">RWTexture3D</span><span class="sxs-lookup"><span data-stu-id="6191c-156">RWTexture3D</span></span>

## <a name="interfaces-and-class-instances"></a><span data-ttu-id="6191c-157">Интерфейсы и экземпляры классов</span><span class="sxs-lookup"><span data-stu-id="6191c-157">Interfaces and Class Instances</span></span>

<span data-ttu-id="6191c-158">Синтаксис интерфейса и класса см. в разделе [интерфейсы и классы](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span><span class="sxs-lookup"><span data-stu-id="6191c-158">For interface and class syntax, see [Interfaces and Classes](/windows/desktop/direct3dhlsl/overviews-direct3d-11-hlsl-dynamic-linking-class).</span></span>

<span data-ttu-id="6191c-159">Сведения об использовании интерфейсов и классов в эффектах см. [в разделе интерфейсы и классы в эффектах](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).</span><span class="sxs-lookup"><span data-stu-id="6191c-159">For using interfaces and classes in effects, see [Interfaces and Classes in Effects](d3d11-graphics-programming-guide-effects-interfaces-and-classes.md).</span></span>

## <a name="addressable-stream-out"></a><span data-ttu-id="6191c-160">Исходящий поток с адресацией</span><span class="sxs-lookup"><span data-stu-id="6191c-160">Addressable Stream Out</span></span>

<span data-ttu-id="6191c-161">В Direct3D 10 шейдеры Geometry могут выводить один поток данных в блок вывода потока и в блок средства прорисовки.</span><span class="sxs-lookup"><span data-stu-id="6191c-161">In Direct3D 10, geometry shaders could output one stream of data to the stream output unit and the rasterizer unit.</span></span> <span data-ttu-id="6191c-162">В Direct3D11 шейдеры Geometry могут выводить до четырех потоков данных в выходную единицу потока и не более одного из этих потоков в блок средства прорисовки.</span><span class="sxs-lookup"><span data-stu-id="6191c-162">In Direct3D11, geometry shaders can output up to four streams of data to the stream output unit, and at most one of those streams to the rasterizer unit.</span></span> <span data-ttu-id="6191c-163">Встроенная функция **конструктгсвиссо** была обновлена для отражения этой новой функциональности.</span><span class="sxs-lookup"><span data-stu-id="6191c-163">The **ConstructGSWithSO** intrinsic has been updated to reflect this new functionality.</span></span>

<span data-ttu-id="6191c-164">Дополнительные сведения см. в разделе [потоковая передача синтаксиса](d3d11-graphics-reference-effect-streamout.md) .</span><span class="sxs-lookup"><span data-stu-id="6191c-164">See [Stream Out Syntax](d3d11-graphics-reference-effect-streamout.md) for more information.</span></span>

## <a name="setting-and-unsetting-device-state"></a><span data-ttu-id="6191c-165">Установка и сброс состояния устройства</span><span class="sxs-lookup"><span data-stu-id="6191c-165">Setting and Unsetting Device State</span></span>

<span data-ttu-id="6191c-166">В эффектах 10 можно сделать буферы констант и буферы текстур управляемыми пользователем с помощью функций [**ID3D10EffectConstantBuffer:: сетконстантбуффер**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) и [**сеттекстуребуффер**](id3dx11effectconstantbuffer-settexturebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="6191c-166">In Effects 10, you could make constant buffers and texture buffers user-managed by using the [**ID3D10EffectConstantBuffer::SetConstantBuffer**](/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectconstantbuffer-setconstantbuffer) and [**SetTextureBuffer**](id3dx11effectconstantbuffer-settexturebuffer.md) functions.</span></span> <span data-ttu-id="6191c-167">После вызова этих функций среда выполнения Effects 10 больше не управляет буфером констант или буфером текстуры, и пользователь должен заполнить данные с помощью интерфейса ID3D10Device.</span><span class="sxs-lookup"><span data-stu-id="6191c-167">After you call these functions, the Effects 10 runtime no longer manages the constant buffer or texture buffer and the user must fill the data by using the ID3D10Device interface.</span></span>

<span data-ttu-id="6191c-168">В последствиях 11 можно также сделать блоки состояния (состояние смешения, состояние средства прорисовки, состояние трафарета и состояние образца) управляемыми пользователем с помощью следующих вызовов:</span><span class="sxs-lookup"><span data-stu-id="6191c-168">In Effects 11, you can also make the state blocks (blend state, rasterizer state, depth-stencil state, and sampler state) user-managed by using the following calls:</span></span>

-   [<span data-ttu-id="6191c-169">**ID3DX11EffectBlendVariable:: Сетблендстате**</span><span class="sxs-lookup"><span data-stu-id="6191c-169">**ID3DX11EffectBlendVariable::SetBlendState**</span></span>](id3dx11effectblendvariable-setblendstate.md)
-   [<span data-ttu-id="6191c-170">**ID3DX11EffectRasterizerVariable:: Сетрастеризерстате**</span><span class="sxs-lookup"><span data-stu-id="6191c-170">**ID3DX11EffectRasterizerVariable::SetRasterizerState**</span></span>](id3dx11effectrasterizervariable-setrasterizerstate.md)
-   [<span data-ttu-id="6191c-171">**ID3DX11EffectDepthStencilVariable:: СетдепсстенЦилстате**</span><span class="sxs-lookup"><span data-stu-id="6191c-171">**ID3DX11EffectDepthStencilVariable::SetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)
-   [<span data-ttu-id="6191c-172">**ID3DX11EffectSamplerVariable:: Сетсамплер**</span><span class="sxs-lookup"><span data-stu-id="6191c-172">**ID3DX11EffectSamplerVariable::SetSampler**</span></span>](id3dx11effectsamplervariable-setsampler.md)

<span data-ttu-id="6191c-173">После вызова этих функций среда выполнения Effects 11 больше не управляет переменными блока State, и значения останутся без изменений.</span><span class="sxs-lookup"><span data-stu-id="6191c-173">After you call these functions, the Effects 11 runtime no longer manages the state block variables, and there values will remain unchanged.</span></span> <span data-ttu-id="6191c-174">Обратите внимание, что, поскольку блоки состояния являются неизменяемыми, пользователь должен задать новый блок состояния, чтобы изменить значения.</span><span class="sxs-lookup"><span data-stu-id="6191c-174">Note that because state blocks are immutable, the user must set a new state block to change the values.</span></span>

<span data-ttu-id="6191c-175">Кроме того, можно восстановить постоянные буферы, буферы текстуры и блоки состояния в неуправляемое состояние.</span><span class="sxs-lookup"><span data-stu-id="6191c-175">You can also revert constant buffers, texture buffers, and state blocks to the non-user managed state.</span></span> <span data-ttu-id="6191c-176">Если вы отмените установку этих переменных, среда выполнения Effects 11 продолжит обновлять их при необходимости.</span><span class="sxs-lookup"><span data-stu-id="6191c-176">If you unset these variables, the Effects 11 runtime will continue to update them when necessary.</span></span> <span data-ttu-id="6191c-177">Для неограниченного использования пользовательских переменных можно использовать следующие вызовы:</span><span class="sxs-lookup"><span data-stu-id="6191c-177">You can use the following calls to unset user managed variables:</span></span>

-   [<span data-ttu-id="6191c-178">**ID3DX11EffectConstantBuffer:: Ундосетконстантбуффер**</span><span class="sxs-lookup"><span data-stu-id="6191c-178">**ID3DX11EffectConstantBuffer::UndoSetConstantBuffer**</span></span>](id3dx11effectconstantbuffer-undosetconstantbuffer.md)
-   [<span data-ttu-id="6191c-179">**ID3DX11EffectConstantBuffer:: Ундосеттекстуребуффер**</span><span class="sxs-lookup"><span data-stu-id="6191c-179">**ID3DX11EffectConstantBuffer::UndoSetTextureBuffer**</span></span>](id3dx11effectconstantbuffer-undosettexturebuffer.md)
-   [<span data-ttu-id="6191c-180">**ID3DX11EffectBlendVariable:: Ундосетблендстате**</span><span class="sxs-lookup"><span data-stu-id="6191c-180">**ID3DX11EffectBlendVariable::UndoSetBlendState**</span></span>](id3dx11effectblendvariable-undosetblendstate.md)
-   [<span data-ttu-id="6191c-181">**ID3DX11EffectRasterizerVariable:: Ундосетрастеризерстате**</span><span class="sxs-lookup"><span data-stu-id="6191c-181">**ID3DX11EffectRasterizerVariable::UndoSetRasterizerState**</span></span>](id3dx11effectrasterizervariable-undosetrasterizerstate.md)
-   [<span data-ttu-id="6191c-182">**ID3DX11EffectDepthStencilVariable:: УндосетдепсстенЦилстате**</span><span class="sxs-lookup"><span data-stu-id="6191c-182">**ID3DX11EffectDepthStencilVariable::UndoSetDepthStencilState**</span></span>](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md)
-   [<span data-ttu-id="6191c-183">**ID3DX11EffectSamplerVariable:: Ундосетсамплер**</span><span class="sxs-lookup"><span data-stu-id="6191c-183">**ID3DX11EffectSamplerVariable::UndoSetSampler**</span></span>](id3dx11effectsamplervariable-undosetsampler.md)

## <a name="effects-virtual-machine"></a><span data-ttu-id="6191c-184">Воздействие виртуальной машины</span><span class="sxs-lookup"><span data-stu-id="6191c-184">Effects Virtual Machine</span></span>

<span data-ttu-id="6191c-185">Виртуальная машина Effects, которая вычисляет сложные выражения вне функций, была удалена.</span><span class="sxs-lookup"><span data-stu-id="6191c-185">The effects virtual machine, which evaluated complex expressions outside of functions, has been removed.</span></span>

<span data-ttu-id="6191c-186">Следующие примеры сложных выражений не поддерживаются:</span><span class="sxs-lookup"><span data-stu-id="6191c-186">The following examples of complex expressions are not supported:</span></span>

1.  <span data-ttu-id="6191c-187">Сетпикселшадер (Мипсаррай (i \* 3 + j));</span><span class="sxs-lookup"><span data-stu-id="6191c-187">SetPixelShader( myPSArray( i \* 3 + j ) );</span></span>
2.  <span data-ttu-id="6191c-188">Сетпикселшадер (Мипсаррай ((float) i);</span><span class="sxs-lookup"><span data-stu-id="6191c-188">SetPixelShader( myPSArray( (float)i );</span></span>
3.  <span data-ttu-id="6191c-189">ФИЛЬТР = i + 2;</span><span class="sxs-lookup"><span data-stu-id="6191c-189">FILTER = i + 2;</span></span>

<span data-ttu-id="6191c-190">Поддерживаются следующие примеры несложных выражений:</span><span class="sxs-lookup"><span data-stu-id="6191c-190">The following examples of non-complex expressions are supported:</span></span>

1.  <span data-ttu-id="6191c-191">Сетпикселшадер (МИПС);</span><span class="sxs-lookup"><span data-stu-id="6191c-191">SetPixelShader( myPS );</span></span>
2.  <span data-ttu-id="6191c-192">Сетпикселшадер (МИПС \[ i \] );</span><span class="sxs-lookup"><span data-stu-id="6191c-192">SetPixelShader( myPS\[i\] );</span></span>
3.  <span data-ttu-id="6191c-193">Сетпикселшадер (МИПС \[ уиндекс \] );//уиндекс является переменной uint</span><span class="sxs-lookup"><span data-stu-id="6191c-193">SetPixelShader( myPS\[ uIndex \] ); // uIndex is a uint variable</span></span>
4.  <span data-ttu-id="6191c-194">ФИЛЬТР = i;</span><span class="sxs-lookup"><span data-stu-id="6191c-194">FILTER = i;</span></span>
5.  <span data-ttu-id="6191c-195">FILTER = АНИЗОТРОПНЫЙ;</span><span class="sxs-lookup"><span data-stu-id="6191c-195">FILTER = ANISOTROPIC;</span></span>

<span data-ttu-id="6191c-196">Эти выражения могут появляться в выражениях блока состояния (например, FILTER) и в выражениях передачи (например, Сетпикселшадер).</span><span class="sxs-lookup"><span data-stu-id="6191c-196">These expressions could appear in state block expressions (such as FILTER) and pass expressions (such as SetPixelShader).</span></span>

## <a name="source-availability-and-location"></a><span data-ttu-id="6191c-197">Доступность источника и расположение</span><span class="sxs-lookup"><span data-stu-id="6191c-197">Source Availability and Location</span></span>

<span data-ttu-id="6191c-198">Эффекты 10 были распространены в D3D10.dll.</span><span class="sxs-lookup"><span data-stu-id="6191c-198">Effects 10 was distributed in D3D10.dll.</span></span> <span data-ttu-id="6191c-199">Эффекты 11 распространяются в виде источника, а соответствующие решения Visual Studio — для его компиляции.</span><span class="sxs-lookup"><span data-stu-id="6191c-199">Effects 11 is distributed as source, with corresponding Visual Studio solutions to compile it.</span></span> <span data-ttu-id="6191c-200">При создании приложений типа Effects рекомендуется включать источник Effects 11 непосредственно в эти приложения.</span><span class="sxs-lookup"><span data-stu-id="6191c-200">When you create effects-type applications, we recommend that you include the Effects 11 source directly in those applications.</span></span>

<span data-ttu-id="6191c-201">Вы можете получить эффекты 11 от [эффектов обновления Direct3D 11](https://github.com/Microsoft/FX11).</span><span class="sxs-lookup"><span data-stu-id="6191c-201">You can get Effects 11 from [Effects for Direct3D 11 Update](https://github.com/Microsoft/FX11).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6191c-202">См. также</span><span class="sxs-lookup"><span data-stu-id="6191c-202">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6191c-203">Эффекты (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="6191c-203">Effects (Direct3D 11)</span></span>](d3d11-graphics-programming-guide-effects.md)
</dt> </dl>

 

 