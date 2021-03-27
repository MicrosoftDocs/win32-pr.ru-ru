---
title: Группы состояний эффектов (Direct3D 11)
description: Состояния эффектов — это пары "имя — значение" в виде выражения.
ms.assetid: 87883483-4fa6-4362-807e-53b79b7d1370
keywords:
- воздействие, группы состояний (Direct3D 11)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58def71b6362706eb831129b1d222ef3d1cc9341
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987537"
---
# <a name="effect-state-groups-direct3d-11"></a><span data-ttu-id="1eb0e-104">Группы состояний эффектов (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="1eb0e-104">Effect State Groups (Direct3D 11)</span></span>

<span data-ttu-id="1eb0e-105">Состояния эффектов — это пары "имя — значение" в виде выражения.</span><span class="sxs-lookup"><span data-stu-id="1eb0e-105">Effect states are name value pairs in the form of an expression.</span></span>

-   [<span data-ttu-id="1eb0e-106">Состояние смешения</span><span class="sxs-lookup"><span data-stu-id="1eb0e-106">Blend State</span></span>](#blend-state)
-   [<span data-ttu-id="1eb0e-107">Состояние глубины и трафарета</span><span class="sxs-lookup"><span data-stu-id="1eb0e-107">Depth and Stencil State</span></span>](#depth-and-stencil-state)
-   [<span data-ttu-id="1eb0e-108">Состояние средства программной прорисовки</span><span class="sxs-lookup"><span data-stu-id="1eb0e-108">Rasterizer State</span></span>](#rasterizer-state)
-   [<span data-ttu-id="1eb0e-109">Состояние образца</span><span class="sxs-lookup"><span data-stu-id="1eb0e-109">Sampler State</span></span>](#sampler-state)
-   [<span data-ttu-id="1eb0e-110">Состояние объекта Effect</span><span class="sxs-lookup"><span data-stu-id="1eb0e-110">Effect Object State</span></span>](#effect-object-state)
-   [<span data-ttu-id="1eb0e-111">Определение и использование объектов состояния</span><span class="sxs-lookup"><span data-stu-id="1eb0e-111">Defining and using state objects</span></span>](#defining-and-using-state-objects)
-   [<span data-ttu-id="1eb0e-112">См. также</span><span class="sxs-lookup"><span data-stu-id="1eb0e-112">Related topics</span></span>](#related-topics)

## <a name="blend-state"></a><span data-ttu-id="1eb0e-113">Состояние смешения</span><span class="sxs-lookup"><span data-stu-id="1eb0e-113">Blend State</span></span>



|                                                                                                                       |                                                           |
|-----------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span data-ttu-id="1eb0e-114">АЛФАТОКОВЕРАЖЕЕНАБЛЕБЛЕНДЕНАБЛЕСРКБЛЕНДДЕСТБЛЕНДБЛЕНДОП СРКБЛЕНДАЛФАДЕСТБЛЕНДАЛФАБЛЕНДОПАЛФАРЕНДЕРТАРЖЕТВРИТЕМАСК</span><span class="sxs-lookup"><span data-stu-id="1eb0e-114">ALPHATOCOVERAGEENABLEBLENDENABLESRCBLENDDESTBLENDBLENDOP SRCBLENDALPHADESTBLENDALPHABLENDOPALPHARENDERTARGETWRITEMASK</span></span> | <span data-ttu-id="1eb0e-115">Члены [ **D3D11 \_ Blend \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="1eb0e-115">Members of [**D3D11\_BLEND\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_blend_desc)</span></span> |



 

## <a name="depth-and-stencil-state"></a><span data-ttu-id="1eb0e-116">Состояние глубины и трафарета</span><span class="sxs-lookup"><span data-stu-id="1eb0e-116">Depth and Stencil State</span></span>



|                                                                                                                                                                |                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="1eb0e-117">депсенабледепсвритемаскдепсфункстенЦиленаблестенЦилреадмаскстенЦилвритемаск</span><span class="sxs-lookup"><span data-stu-id="1eb0e-117">DEPTHENABLEDEPTHWRITEMASKDEPTHFUNCSTENCILENABLESTENCILREADMASKSTENCILWRITEMASK</span></span>                                                                                 | <span data-ttu-id="1eb0e-118">Элементы в [ **\_ \_ наборе элементов \_ глубины D3D11 DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="1eb0e-118">Members of [**D3D11\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencil_desc)</span></span>    |
| <span data-ttu-id="1eb0e-119">фронтфацестенЦилфаилфронтфацестенЦилзфаилфронтфацестенЦилпассфронтфацестенЦилфункбаккфацестенЦилфаилбаккфацестенЦилзфаилбаккфацестенЦилпассбаккфацестенЦилфунк</span><span class="sxs-lookup"><span data-stu-id="1eb0e-119">FRONTFACESTENCILFAILFRONTFACESTENCILZFAILFRONTFACESTENCILPASSFRONTFACESTENCILFUNCBACKFACESTENCILFAILBACKFACESTENCILZFAILBACKFACESTENCILPASSBACKFACESTENCILFUNC</span></span> | <span data-ttu-id="1eb0e-120">Член [ **D3D11 \_ глубины \_ стенЦилоп \_ DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="1eb0e-120">Member of [**D3D11\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_depth_stencilop_desc)</span></span> |



 

## <a name="rasterizer-state"></a><span data-ttu-id="1eb0e-121">Состояние средства прорисовки</span><span class="sxs-lookup"><span data-stu-id="1eb0e-121">Rasterizer State</span></span>



|                                                                                                                                 |                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1eb0e-122">филлмоде</span><span class="sxs-lookup"><span data-stu-id="1eb0e-122">FILLMODE</span></span>                                                                                                                        | [<span data-ttu-id="1eb0e-123">**\_Режим заполнения \_ D3D11**</span><span class="sxs-lookup"><span data-stu-id="1eb0e-123">**D3D11\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_fill_mode)                        |
| <span data-ttu-id="1eb0e-124">куллмоде</span><span class="sxs-lookup"><span data-stu-id="1eb0e-124">CULLMODE</span></span>                                                                                                                        | [<span data-ttu-id="1eb0e-125">**Режим D3D11ного \_ отбора \_**</span><span class="sxs-lookup"><span data-stu-id="1eb0e-125">**D3D11\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D11/ne-d3d11-d3d11_cull_mode)                        |
| <span data-ttu-id="1eb0e-126">ФРОНТКАУНТЕРКЛОККВИСЕДЕПСБИАСДЕПСБИАСКЛАМПСЛОПЕСКАЛЕДДЕПСБИАС ЗКЛИПЕНАБЛЕСЦИССОРЕНАБЛЕМУЛТИСАМПЛИНАБЛЕАНТИАЛИАСЕДЛИНИНАБЛЕ</span><span class="sxs-lookup"><span data-stu-id="1eb0e-126">FRONTCOUNTERCLOCKWISEDEPTHBIASDEPTHBIASCLAMPSLOPESCALEDDEPTHBIAS ZCLIPENABLESCISSORENABLEMULTISAMPLEENABLEANTIALIASEDLINEENABLE</span></span> | <span data-ttu-id="1eb0e-127">Члены класса [ **D3D11 средство \_ растеризации \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="1eb0e-127">Members of [**D3D11\_RASTERIZER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_rasterizer_desc)</span></span> |



 

## <a name="sampler-state"></a><span data-ttu-id="1eb0e-128">Состояние образца</span><span class="sxs-lookup"><span data-stu-id="1eb0e-128">Sampler State</span></span>



|                                                                                                     |                                                               |
|-----------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="1eb0e-129">Filter Аддрессу Аддрессв Аддрессв Миплодбиас Максанисотропи Компарисонфунк BorderColor Минлод Макслод</span><span class="sxs-lookup"><span data-stu-id="1eb0e-129">Filter AddressU AddressV AddressW MipLODBias MaxAnisotropy ComparisonFunc BorderColor MinLOD MaxLOD</span></span> | <span data-ttu-id="1eb0e-130">Члены [ **D3D11ного \_ образца \_**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="1eb0e-130">Members of [**D3D11\_SAMPLER\_DESC**](/windows/desktop/api/D3D11/ns-d3d11-d3d11_sampler_desc)</span></span> |



 

<span data-ttu-id="1eb0e-131">Примеры см. в разделе [тип образца (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) .</span><span class="sxs-lookup"><span data-stu-id="1eb0e-131">See [Sampler Type (DirectX HLSL)](/windows/desktop/direct3dhlsl/dx-graphics-hlsl-sampler) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="1eb0e-132">Состояние объекта Effect</span><span class="sxs-lookup"><span data-stu-id="1eb0e-132">Effect Object State</span></span>



| <span data-ttu-id="1eb0e-133">Этот объект Effect</span><span class="sxs-lookup"><span data-stu-id="1eb0e-133">This Effect Object</span></span>                          | <span data-ttu-id="1eb0e-134">Соответствует параметру</span><span class="sxs-lookup"><span data-stu-id="1eb0e-134">Maps to</span></span>                                                             |
|---------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="1eb0e-135">растеризерстате</span><span class="sxs-lookup"><span data-stu-id="1eb0e-135">RASTERIZERSTATE</span></span>                             | <span data-ttu-id="1eb0e-136">Объект состояния состояния средства программной [прорисовки](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="1eb0e-136">A [Rasterizer State](#rasterizer-state) state object.</span></span>               |
| <span data-ttu-id="1eb0e-137">депсстенЦилстате</span><span class="sxs-lookup"><span data-stu-id="1eb0e-137">DEPTHSTENCILSTATE</span></span>                           | <span data-ttu-id="1eb0e-138">Объект состояния " [глубина" и "набор элементов](#depth-and-stencil-state) ".</span><span class="sxs-lookup"><span data-stu-id="1eb0e-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="1eb0e-139">блендстате</span><span class="sxs-lookup"><span data-stu-id="1eb0e-139">BLENDSTATE</span></span>                                  | <span data-ttu-id="1eb0e-140">Объект состояния [смешения состояния](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="1eb0e-140">A [Blend State](#blend-state) state object.</span></span>                         |
| <span data-ttu-id="1eb0e-141">вертексшадер</span><span class="sxs-lookup"><span data-stu-id="1eb0e-141">VERTEXSHADER</span></span>                                | <span data-ttu-id="1eb0e-142">Скомпилированный объект шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="1eb0e-142">A compiled vertex shader object.</span></span>                                    |
| <span data-ttu-id="1eb0e-143">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="1eb0e-143">PIXELSHADER</span></span>                                 | <span data-ttu-id="1eb0e-144">Скомпилированный объект шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="1eb0e-144">A compiled pixel shader object.</span></span>                                     |
| <span data-ttu-id="1eb0e-145">жеометришадер</span><span class="sxs-lookup"><span data-stu-id="1eb0e-145">GEOMETRYSHADER</span></span>                              | <span data-ttu-id="1eb0e-146">Скомпилированный объект шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="1eb0e-146">A compiled geometry shader object.</span></span>                                  |
| <span data-ttu-id="1eb0e-147">DS \_ стенЦилрефаб \_ блендфактораб \_ самплемаск</span><span class="sxs-lookup"><span data-stu-id="1eb0e-147">DS\_STENCILREFAB\_BLENDFACTORAB\_SAMPLEMASK</span></span> | <span data-ttu-id="1eb0e-148">Члены [**D3DX11 \_ Pass \_ DESC**](d3dx11-pass-desc.md).</span><span class="sxs-lookup"><span data-stu-id="1eb0e-148">Members of [**D3DX11\_PASS\_DESC**](d3dx11-pass-desc.md).</span></span>          |



 

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="1eb0e-149">Определение и использование объектов состояния</span><span class="sxs-lookup"><span data-stu-id="1eb0e-149">Defining and using state objects</span></span>

<span data-ttu-id="1eb0e-150">Объекты состояния объявляются в файлах FX в следующем формате.</span><span class="sxs-lookup"><span data-stu-id="1eb0e-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="1eb0e-151">Статеобжекттипе — одно из состояний, перечисленных выше, а MemberName — имя любого члена, который будет иметь значение, отличное от значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1eb0e-151">StateObjectType is one of the states listed above and MemberName is the name of any member that will have a non-default value.</span></span>


```
StateObjectType ObjectName {
  MemberName = value;
  ...
  MemberName = value;
};
    
```



<span data-ttu-id="1eb0e-152">Например, чтобы настроить объект состояния Blend с Алфатоковеражеенабле, а Бленденабле 0 — \[ \] значением **false** , будет использован следующий код.</span><span class="sxs-lookup"><span data-stu-id="1eb0e-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE** the following code would be used.</span></span>


```
BlendState NoBlend {
  AlphaToCoverageEnable = FALSE;
  BlendEnable[0] = FALSE;
};
    
```



<span data-ttu-id="1eb0e-153">Объект состояния применяется к методу Pass с помощью одной из функций Сетстатеграуп, описанных в разделе [синтаксис методики действия (Direct3D 11)](d3d11-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="1eb0e-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 11)](d3d11-effect-technique-syntax.md).</span></span> <span data-ttu-id="1eb0e-154">Например, для применения объекта Блендстате, описанного выше, будет использоваться следующий код.</span><span class="sxs-lookup"><span data-stu-id="1eb0e-154">For example, to apply the BlendState object described above the following code would be used.</span></span>


```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
    
```



## <a name="related-topics"></a><span data-ttu-id="1eb0e-155">См. также</span><span class="sxs-lookup"><span data-stu-id="1eb0e-155">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1eb0e-156">Синтаксис методики эффектов</span><span class="sxs-lookup"><span data-stu-id="1eb0e-156">Effect Technique Syntax</span></span>](d3d11-effect-technique-syntax.md)
</dt> <dt>

[<span data-ttu-id="1eb0e-157">Формат эффектов (Direct3D 11)</span><span class="sxs-lookup"><span data-stu-id="1eb0e-157">Effect Format (Direct3D 11)</span></span>](d3d11-effect-format.md)
</dt> </dl>

 

 