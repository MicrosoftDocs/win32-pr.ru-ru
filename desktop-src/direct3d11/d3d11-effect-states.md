---
title: Группы состояний эффектов (Direct3D 11)
description: Состояния эффектов — это пары "имя — значение" в виде выражения.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- воздействие, группы состояний (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5a757926d8c4c259adc94f505a778cf73233b5a
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335344"
---
# <a name="effect-state-groups-direct3d-11"></a><span data-ttu-id="1476d-104">Группы состояний эффектов (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="1476d-104">Effect State Groups (Direct3D 11)</span></span>

<span data-ttu-id="1476d-105">Состояния эффектов — это пары "имя — значение" в виде выражения.</span><span class="sxs-lookup"><span data-stu-id="1476d-105">Effect states are name value pairs in the form of an expression.</span></span>

-   [<span data-ttu-id="1476d-106">Состояние смешения</span><span class="sxs-lookup"><span data-stu-id="1476d-106">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="1476d-107">Состояние глубины и трафарета</span><span class="sxs-lookup"><span data-stu-id="1476d-107">Depth and Stencil State</span></span>](#depth-and-stencil-state)
-   [<span data-ttu-id="1476d-108">Состояние средства программной прорисовки</span><span class="sxs-lookup"><span data-stu-id="1476d-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="1476d-109">Состояние образца</span><span class="sxs-lookup"><span data-stu-id="1476d-109">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="1476d-110">Состояние объекта Effect</span><span class="sxs-lookup"><span data-stu-id="1476d-110">Effect Object State</span></span>](#effect-object-state)
-   [<span data-ttu-id="1476d-111">Определение и использование объектов состояния</span><span class="sxs-lookup"><span data-stu-id="1476d-111">Defining and using state objects</span></span>](#defining-and-using-state-objects)
-   [<span data-ttu-id="1476d-112">См. также</span><span class="sxs-lookup"><span data-stu-id="1476d-112">Related topics</span></span>](#related-topics)

## <a name="blend-state"></a><span data-ttu-id="1476d-113">Состояние смешения</span><span class="sxs-lookup"><span data-stu-id="1476d-113">Blend State</span></span>



| <span data-ttu-id="1476d-114">Состояние действия</span><span class="sxs-lookup"><span data-stu-id="1476d-114">Effect state</span></span>                                                                                                                      | <span data-ttu-id="1476d-115">Group</span><span class="sxs-lookup"><span data-stu-id="1476d-115">Group</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1476d-116">АЛФАТОКОВЕРАЖЕЕНАБЛЕБЛЕНДЕНАБЛЕСРКБЛЕНДДЕСТБЛЕНДБЛЕНДОП СРКБЛЕНДАЛФАДЕСТБЛЕНДАЛФАБЛЕНДОПАЛФАРЕНДЕРТАРЖЕТВРИТЕМАСК</span><span class="sxs-lookup"><span data-stu-id="1476d-116">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span></span> | <span data-ttu-id="1476d-117">Члены [ **D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="1476d-117">Members of [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span></span> |



 

## <a name="depth-and-stencil-state"></a><span data-ttu-id="1476d-118">Состояние глубины и трафарета</span><span class="sxs-lookup"><span data-stu-id="1476d-118">Depth and Stencil State</span></span>



|  <span data-ttu-id="1476d-119">Состояние действия</span><span class="sxs-lookup"><span data-stu-id="1476d-119">Effect state</span></span>                                                                                                                                                              | <span data-ttu-id="1476d-120">Group</span><span class="sxs-lookup"><span data-stu-id="1476d-120">Group</span></span>                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="1476d-121">депсенабледепсвритемаскдепсфункстенЦиленаблестенЦилреадмаскстенЦилвритемаск</span><span class="sxs-lookup"><span data-stu-id="1476d-121">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span></span>                                                                                 | <span data-ttu-id="1476d-122">Элементы в [ **\_ \_ наборе элементов \_ глубины D3D11 DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="1476d-122">Members of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span>    |
| <span data-ttu-id="1476d-123">фронтфацестенЦилфаилфронтфацестенЦилзфаилфронтфацестенЦилпассфронтфацестенЦилфункбаккфацестенЦилфаилбаккфацестенЦилзфаилбаккфацестенЦилпассбаккфацестенЦилфунк</span><span class="sxs-lookup"><span data-stu-id="1476d-123">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span></span> | <span data-ttu-id="1476d-124">Член [ **D3D11 \_ глубины \_ стенЦилоп \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="1476d-124">Member of [**D3D11\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span></span> |



 

## <a name="rasterizer-state"></a><span data-ttu-id="1476d-125">Состояние средства прорисовки</span><span class="sxs-lookup"><span data-stu-id="1476d-125">Rasterizer State</span></span>



| <span data-ttu-id="1476d-126">Состояние действия</span><span class="sxs-lookup"><span data-stu-id="1476d-126">Effect state</span></span>                                                                                                                                | <span data-ttu-id="1476d-127">Group</span><span class="sxs-lookup"><span data-stu-id="1476d-127">Group</span></span>                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1476d-128">филлмоде</span><span class="sxs-lookup"><span data-stu-id="1476d-128">FILLMODE</span></span>                                                                                                                        | [<span data-ttu-id="1476d-129">**\_Режим заполнения \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="1476d-129">**D3D11\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| <span data-ttu-id="1476d-130">куллмоде</span><span class="sxs-lookup"><span data-stu-id="1476d-130">CULLMODE</span></span>                                                                                                                        | [<span data-ttu-id="1476d-131">**Режим D3D11ного \_ отбора \_**</span><span class="sxs-lookup"><span data-stu-id="1476d-131">**D3D11\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| <span data-ttu-id="1476d-132">ФРОНТКАУНТЕРКЛОККВИСЕДЕПСБИАСДЕПСБИАСКЛАМПСЛОПЕСКАЛЕДДЕПСБИАС ЗКЛИПЕНАБЛЕСЦИССОРЕНАБЛЕМУЛТИСАМПЛИНАБЛЕАНТИАЛИАСЕДЛИНИНАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="1476d-132">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span></span> | <span data-ttu-id="1476d-133">Члены класса [ **D3D11 средство \_ растеризации \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="1476d-133">Members of [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span></span> |



 

## <a name="sampler-state"></a><span data-ttu-id="1476d-134">Состояние образца</span><span class="sxs-lookup"><span data-stu-id="1476d-134">Sampler State</span></span>



| <span data-ttu-id="1476d-135">Состояние действия</span><span class="sxs-lookup"><span data-stu-id="1476d-135">Effect state</span></span>                                                                                                    | <span data-ttu-id="1476d-136">Group</span><span class="sxs-lookup"><span data-stu-id="1476d-136">Group</span></span>                                                              |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1476d-137">Filter Аддрессу Аддрессв Аддрессв Миплодбиас Максанисотропи Компарисонфунк BorderColor Минлод Макслод</span><span class="sxs-lookup"><span data-stu-id="1476d-137">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span></span> | <span data-ttu-id="1476d-138">Члены [ **D3D11ного \_ образца \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="1476d-138">Members of [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span></span> |



 

<span data-ttu-id="1476d-139">Примеры см. в разделе [тип образца (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) .</span><span class="sxs-lookup"><span data-stu-id="1476d-139">See [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="1476d-140">Состояние объекта Effect</span><span class="sxs-lookup"><span data-stu-id="1476d-140">Effect Object State</span></span>



| <span data-ttu-id="1476d-141">Этот объект Effect</span><span class="sxs-lookup"><span data-stu-id="1476d-141">This Effect Object</span></span>                          | <span data-ttu-id="1476d-142">Соответствует параметру</span><span class="sxs-lookup"><span data-stu-id="1476d-142">Maps to</span></span>                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1476d-143">растеризерстате</span><span class="sxs-lookup"><span data-stu-id="1476d-143">RASTERIZERSTATE</span></span>                             | <span data-ttu-id="1476d-144">Объект состояния состояния средства программной [прорисовки](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="1476d-144">A [Rasterizer State](#rasterizer-state) state object.</span></span>               |
| <span data-ttu-id="1476d-145">депсстенЦилстате</span><span class="sxs-lookup"><span data-stu-id="1476d-145">DEPTHSTENCILSTATE</span></span>                           | <span data-ttu-id="1476d-146">Объект состояния " [глубина" и "набор элементов](#depth-and-stencil-state) ".</span><span class="sxs-lookup"><span data-stu-id="1476d-146">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="1476d-147">блендстате</span><span class="sxs-lookup"><span data-stu-id="1476d-147">BLENDSTATE</span></span>                                  | <span data-ttu-id="1476d-148">Объект состояния [смешения состояния](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="1476d-148">A [Blend State](#blend-state) state object.</span></span>                         |
| <span data-ttu-id="1476d-149">вертексшадер</span><span class="sxs-lookup"><span data-stu-id="1476d-149">VERTEXSHADER</span></span>                                | <span data-ttu-id="1476d-150">Скомпилированный объект шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="1476d-150">A compiled vertex shader object.</span></span>                                    |
| <span data-ttu-id="1476d-151">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="1476d-151">PIXELSHADER</span></span>                                 | <span data-ttu-id="1476d-152">Скомпилированный объект шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="1476d-152">A compiled pixel shader object.</span></span>                                     |
| <span data-ttu-id="1476d-153">жеометришадер</span><span class="sxs-lookup"><span data-stu-id="1476d-153">GEOMETRYSHADER</span></span>                              | <span data-ttu-id="1476d-154">Скомпилированный объект шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="1476d-154">A compiled geometry shader object.</span></span>                                  |
| <span data-ttu-id="1476d-155">DS \_ стенЦилрефаб \_ блендфактораб \_ самплемаск</span><span class="sxs-lookup"><span data-stu-id="1476d-155">DS\_STENCILREFAB\_BLENDFACTORAB\_SAMPLEMASK</span></span> | <span data-ttu-id="1476d-156">Члены [**D3DX11 \_ Pass \_ DESC**](d3dx11-pass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="1476d-156">Members of [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md).</span></span>          |



 

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="1476d-157">Определение и использование объектов состояния</span><span class="sxs-lookup"><span data-stu-id="1476d-157">Defining and using state objects</span></span>

<span data-ttu-id="1476d-158">Объекты состояния объявляются в файлах FX в следующем формате.</span><span class="sxs-lookup"><span data-stu-id="1476d-158">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="1476d-159">Статеобжекттипе — одно из состояний, перечисленных выше, а MemberName — имя любого члена, который будет иметь значение, отличное от значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1476d-159">StateObjectType is one of the states listed above and MemberName is the name of any member that will have a non-default value.</span></span>


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



<span data-ttu-id="1476d-160">Например, чтобы настроить объект состояния Blend с Алфатоковеражеенабле, а Бленденабле 0 — \[ \] значением **false** , будет использован следующий код.</span><span class="sxs-lookup"><span data-stu-id="1476d-160">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE** the following code would be used.</span></span>


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



<span data-ttu-id="1476d-161">Объект состояния применяется к методу Pass с помощью одной из функций Сетстатеграуп, описанных в разделе [синтаксис методики действия (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="1476d-161">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span> <span data-ttu-id="1476d-162">Например, для применения объекта Блендстате, описанного выше, будет использоваться следующий код.</span><span class="sxs-lookup"><span data-stu-id="1476d-162">For example, to apply the BlendState object described above the following code would be used.</span></span>


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a><span data-ttu-id="1476d-163">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="1476d-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1476d-164">Синтаксис методики эффектов</span><span class="sxs-lookup"><span data-stu-id="1476d-164">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)
</dt> <dt>

[<span data-ttu-id="1476d-165">Формат эффектов (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="1476d-165">Effect Format (Direct3D 11)</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 