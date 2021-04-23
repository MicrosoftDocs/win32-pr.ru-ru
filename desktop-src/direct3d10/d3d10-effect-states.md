---
description: Состояния эффектов — это пары "имя-значение" в виде выражения.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Группы состояний эффектов (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c132db3a5258cbe3573ddc5103df8b3cbcf2085d
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "104351742"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="7f7dc-103">Группы состояний эффектов (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="7f7dc-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="7f7dc-104">Состояния эффектов — это пары "имя-значение" в виде выражения.</span><span class="sxs-lookup"><span data-stu-id="7f7dc-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="7f7dc-105">Состояние смешения</span><span class="sxs-lookup"><span data-stu-id="7f7dc-105">Blend state</span></span>

| | |
|-|-|
| <span data-ttu-id="7f7dc-106">**алфатоковеражеенабле**, **бленденабле**, **сркбленд**, **дестбленд**, **блендоп**, **сркблендалфа**, **дестблендалфа**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="7f7dc-106">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="7f7dc-107">Члены [ **D3D10 \_ Blend \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="7f7dc-107">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="7f7dc-108">Состояние глубины и трафарета</span><span class="sxs-lookup"><span data-stu-id="7f7dc-108">Depth and stencil state</span></span>

| | |
|-|-|
| <span data-ttu-id="7f7dc-109">**депсенабле**, **депсвритемаск**, **депсфунк**, **стенЦиленабле**, **стенЦилреадмаск**, **стенЦилвритемаск**</span><span class="sxs-lookup"><span data-stu-id="7f7dc-109">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="7f7dc-110">Элементы в [ **\_ \_ наборе элементов \_ глубины D3D10 DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="7f7dc-110">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="7f7dc-111">ФРОНТФАЦЕСТЕНЦИЛФАИЛ \* \*, **фронтфацестенЦилзфаил**, **фронтфацестенЦилпасс**, **фронтфацестенЦилфунк**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="7f7dc-111">FRONTFACESTENCILFAIL\*\*, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="7f7dc-112">Член [ **D3D10 \_ глубины \_ стенЦилоп \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="7f7dc-112">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="7f7dc-113">Состояние средства программной прорисовки</span><span class="sxs-lookup"><span data-stu-id="7f7dc-113">Rasterizer state</span></span>

| | |
|-|-|
| <span data-ttu-id="7f7dc-114">филлмоде</span><span class="sxs-lookup"><span data-stu-id="7f7dc-114">FILLMODE</span></span> | [<span data-ttu-id="7f7dc-115">**\_Режим заполнения \_ D3D10**</span><span class="sxs-lookup"><span data-stu-id="7f7dc-115">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="7f7dc-116">куллмоде</span><span class="sxs-lookup"><span data-stu-id="7f7dc-116">CULLMODE</span></span> | [<span data-ttu-id="7f7dc-117">**Режим D3D10ного \_ отбора \_**</span><span class="sxs-lookup"><span data-stu-id="7f7dc-117">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="7f7dc-118">**фронткаунтерклокквисе**, **депсбиас**, **депсбиаскламп**, **слопескаледдепсбиас**, **зклипенабле**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="7f7dc-118">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="7f7dc-119">Члены класса [ **D3D10 средство \_ растеризации \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="7f7dc-119">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="7f7dc-120">Состояние дискретизатора</span><span class="sxs-lookup"><span data-stu-id="7f7dc-120">Sampler state</span></span>

| | |
|-|-|
| <span data-ttu-id="7f7dc-121">**Filter**, **аддрессу**, **аддрессв**, **аддрессв**, **миплодбиас**, **максанисотропи**, **компарисонфунк**, **BorderColor**, **минлод**, **макслод**</span><span class="sxs-lookup"><span data-stu-id="7f7dc-121">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="7f7dc-122">Члены [ **D3D10ного \_ образца \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="7f7dc-122">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="7f7dc-123">Примеры см. в разделе [тип образца (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) .</span><span class="sxs-lookup"><span data-stu-id="7f7dc-123">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="7f7dc-124">Состояние объекта Effect</span><span class="sxs-lookup"><span data-stu-id="7f7dc-124">Effect object state</span></span>

| <span data-ttu-id="7f7dc-125">Этот объект Effect</span><span class="sxs-lookup"><span data-stu-id="7f7dc-125">This effect object</span></span> | <span data-ttu-id="7f7dc-126">Соответствует параметру</span><span class="sxs-lookup"><span data-stu-id="7f7dc-126">Maps to</span></span> |
|-|-|
| <span data-ttu-id="7f7dc-127">растеризерстате</span><span class="sxs-lookup"><span data-stu-id="7f7dc-127">RASTERIZERSTATE</span></span> | <span data-ttu-id="7f7dc-128">Объект состояния состояния средства программной [прорисовки](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="7f7dc-128">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="7f7dc-129">депсстенЦилстате</span><span class="sxs-lookup"><span data-stu-id="7f7dc-129">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="7f7dc-130">Объект состояния " [глубина" и "набор элементов](#depth-and-stencil-state) ".</span><span class="sxs-lookup"><span data-stu-id="7f7dc-130">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="7f7dc-131">блендстате</span><span class="sxs-lookup"><span data-stu-id="7f7dc-131">BLENDSTATE</span></span> | <span data-ttu-id="7f7dc-132">Объект состояния [смешения состояния](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="7f7dc-132">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="7f7dc-133">вертексшадер</span><span class="sxs-lookup"><span data-stu-id="7f7dc-133">VERTEXSHADER</span></span> | <span data-ttu-id="7f7dc-134">Скомпилированный объект шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="7f7dc-134">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="7f7dc-135">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="7f7dc-135">PIXELSHADER</span></span> | <span data-ttu-id="7f7dc-136">Скомпилированный объект шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="7f7dc-136">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="7f7dc-137">жеометришадер</span><span class="sxs-lookup"><span data-stu-id="7f7dc-137">GEOMETRYSHADER</span></span> | <span data-ttu-id="7f7dc-138">Скомпилированный объект шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="7f7dc-138">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="7f7dc-139">DS \_ СТЕНЦИЛРЕФ AB \_ блендфактор AB \_ самплемаск</span><span class="sxs-lookup"><span data-stu-id="7f7dc-139">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="7f7dc-140">Члены [**D3D10 \_ Pass \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span><span class="sxs-lookup"><span data-stu-id="7f7dc-140">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="7f7dc-141">Определение и использование объектов состояния</span><span class="sxs-lookup"><span data-stu-id="7f7dc-141">Defining and using state objects</span></span>

<span data-ttu-id="7f7dc-142">Объекты состояния объявляются в файлах FX в следующем формате.</span><span class="sxs-lookup"><span data-stu-id="7f7dc-142">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="7f7dc-143">*Статеобжекттипе* — одно из состояний, перечисленных выше, а *MemberName* — имя любого члена, который будет иметь значение, отличное от значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="7f7dc-143">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="7f7dc-144">Например, чтобы настроить объект состояния Blend с Алфатоковеражеенабле, а Бленденабле \[ 0 \] — значением **false**, используется следующий код.</span><span class="sxs-lookup"><span data-stu-id="7f7dc-144">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="7f7dc-145">Объект состояния применяется к методу Pass с помощью одной из функций Сетстатеграуп, описанных в разделе [синтаксис методики работы (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="7f7dc-145">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="7f7dc-146">Например, для применения объекта Блендстате, описанного выше, будет использоваться следующий код.</span><span class="sxs-lookup"><span data-stu-id="7f7dc-146">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="7f7dc-147">Учебник, в котором описывается использование состояний, см. в разделе [Управление состоянием](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="7f7dc-147">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f7dc-148">См. также</span><span class="sxs-lookup"><span data-stu-id="7f7dc-148">Related topics</span></span>

* [<span data-ttu-id="7f7dc-149">Синтаксис методики эффектов</span><span class="sxs-lookup"><span data-stu-id="7f7dc-149">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="7f7dc-150">Формат эффектов (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="7f7dc-150">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
