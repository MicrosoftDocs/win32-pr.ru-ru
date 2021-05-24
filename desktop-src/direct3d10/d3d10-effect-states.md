---
description: Состояния эффектов — это пары "имя-значение" в виде выражения.
ms.assetid: 4612c6bd-bc1f-42ad-8465-c0d4b577d1db
title: Группы состояний эффектов (Direct3D 10)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4617f786b984c96b271600e05b3ea8da9b5701fd
ms.sourcegitcommit: ca37395fd832e798375e81142b97cffcffabf184
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110335577"
---
# <a name="effect-state-groups-direct3d-10"></a><span data-ttu-id="76f31-103">Группы состояний эффектов (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="76f31-103">Effect state groups (Direct3D 10)</span></span>

<span data-ttu-id="76f31-104">Состояния эффектов — это пары "имя-значение" в виде выражения.</span><span class="sxs-lookup"><span data-stu-id="76f31-104">Effect states are name-value pairs in the form of an expression.</span></span>

## <a name="blend-state"></a><span data-ttu-id="76f31-105">Состояние смешения</span><span class="sxs-lookup"><span data-stu-id="76f31-105">Blend state</span></span>

| <span data-ttu-id="76f31-106">Состояние действия</span><span class="sxs-lookup"><span data-stu-id="76f31-106">Effect state</span></span> | <span data-ttu-id="76f31-107">Group</span><span class="sxs-lookup"><span data-stu-id="76f31-107">Group</span></span> |
|-|-|
| <span data-ttu-id="76f31-108">**алфатоковеражеенабле**, **бленденабле**, **сркбленд**, **дестбленд**, **блендоп**, **сркблендалфа**, **дестблендалфа**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span><span class="sxs-lookup"><span data-stu-id="76f31-108">**ALPHATOCOVERAGEENABLE**, **BLENDENABLE**, **SRCBLEND**, **DESTBLEND**, **BLENDOP**, **SRCBLENDALPHA**, **DESTBLENDALPHA**, **BLENDOPALPHA**, **RENDERTARGETWRITEMASK**</span></span> | <span data-ttu-id="76f31-109">Члены [ **D3D10 \_ Blend \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span><span class="sxs-lookup"><span data-stu-id="76f31-109">Members of [**D3D10\_BLEND\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_blend_desc)</span></span> |

## <a name="depth-and-stencil-state"></a><span data-ttu-id="76f31-110">Состояние глубины и трафарета</span><span class="sxs-lookup"><span data-stu-id="76f31-110">Depth and stencil state</span></span>

| <span data-ttu-id="76f31-111">Состояние действия</span><span class="sxs-lookup"><span data-stu-id="76f31-111">Effect state</span></span>| <span data-ttu-id="76f31-112">Group</span><span class="sxs-lookup"><span data-stu-id="76f31-112">Group</span></span> |
|-|-|
| <span data-ttu-id="76f31-113">**депсенабле**, **депсвритемаск**, **депсфунк**, **стенЦиленабле**, **стенЦилреадмаск**, **стенЦилвритемаск**</span><span class="sxs-lookup"><span data-stu-id="76f31-113">**DEPTHENABLE**, **DEPTHWRITEMASK**, **DEPTHFUNC**, **STENCILENABLE**, **STENCILREADMASK**, **STENCILWRITEMASK**</span></span> | <span data-ttu-id="76f31-114">Элементы в [ **\_ \_ наборе элементов \_ глубины D3D10 DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span><span class="sxs-lookup"><span data-stu-id="76f31-114">Members of [**D3D10\_DEPTH\_STENCIL\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencil_desc)</span></span> |
| <span data-ttu-id="76f31-115">**фронтфацестенЦилфаил**, **фронтфацестенЦилзфаил**, **фронтфацестенЦилпасс**, **фронтфацестенЦилфунк**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span><span class="sxs-lookup"><span data-stu-id="76f31-115">**FRONTFACESTENCILFAIL**, **FRONTFACESTENCILZFAIL**, **FRONTFACESTENCILPASS**, **FRONTFACESTENCILFUNC**, **BACKFACESTENCILFAIL**, **BACKFACESTENCILZFAIL**, **BACKFACESTENCILPASS**, **BACKFACESTENCILFUNC**</span></span> | <span data-ttu-id="76f31-116">Член [ **D3D10 \_ глубины \_ стенЦилоп \_ DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span><span class="sxs-lookup"><span data-stu-id="76f31-116">Member of [**D3D10\_DEPTH\_STENCILOP\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_depth_stencilop_desc)</span></span> |

## <a name="rasterizer-state"></a><span data-ttu-id="76f31-117">Состояние средства программной прорисовки</span><span class="sxs-lookup"><span data-stu-id="76f31-117">Rasterizer state</span></span>

| <span data-ttu-id="76f31-118">Состояние действия</span><span class="sxs-lookup"><span data-stu-id="76f31-118">Effect state</span></span>| <span data-ttu-id="76f31-119">Group</span><span class="sxs-lookup"><span data-stu-id="76f31-119">Group</span></span> |
|-|-|
| <span data-ttu-id="76f31-120">филлмоде</span><span class="sxs-lookup"><span data-stu-id="76f31-120">FILLMODE</span></span> | [<span data-ttu-id="76f31-121">**\_Режим заполнения \_ D3D10**</span><span class="sxs-lookup"><span data-stu-id="76f31-121">**D3D10\_FILL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_fill_mode) |
| <span data-ttu-id="76f31-122">куллмоде</span><span class="sxs-lookup"><span data-stu-id="76f31-122">CULLMODE</span></span> | [<span data-ttu-id="76f31-123">**Режим D3D10ного \_ отбора \_**</span><span class="sxs-lookup"><span data-stu-id="76f31-123">**D3D10\_CULL\_MODE**</span></span>](/windows/desktop/api/D3D10/ne-d3d10-d3d10_cull_mode) |
| <span data-ttu-id="76f31-124">**фронткаунтерклокквисе**, **депсбиас**, **депсбиаскламп**, **слопескаледдепсбиас**, **зклипенабле**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span><span class="sxs-lookup"><span data-stu-id="76f31-124">**FRONTCOUNTERCLOCKWISE**, **DEPTHBIAS**, **DEPTHBIASCLAMP**, **SLOPESCALEDDEPTHBIAS**, **ZCLIPENABLE**, **SCISSORENABLE**, **MULTISAMPLEENABLE**, **ANTIALIASEDLINEENABLE**</span></span> | <span data-ttu-id="76f31-125">Члены класса [ **D3D10 средство \_ растеризации \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span><span class="sxs-lookup"><span data-stu-id="76f31-125">Members of [**D3D10\_RASTERIZER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_rasterizer_desc)</span></span> |

## <a name="sampler-state"></a><span data-ttu-id="76f31-126">Состояние дискретизатора</span><span class="sxs-lookup"><span data-stu-id="76f31-126">Sampler state</span></span>

| <span data-ttu-id="76f31-127">Состояние действия</span><span class="sxs-lookup"><span data-stu-id="76f31-127">Effect state</span></span> | <span data-ttu-id="76f31-128">Group</span><span class="sxs-lookup"><span data-stu-id="76f31-128">Group</span></span> |
|-|-|
| <span data-ttu-id="76f31-129">**Filter**, **аддрессу**, **аддрессв**, **аддрессв**, **миплодбиас**, **максанисотропи**, **компарисонфунк**, **BorderColor**, **минлод**, **макслод**</span><span class="sxs-lookup"><span data-stu-id="76f31-129">**Filter**, **AddressU**, **AddressV**, **AddressW**, **MipLODBias**, **MaxAnisotropy**, **ComparisonFunc**, **BorderColor**, **MinLOD**, **MaxLOD**</span></span> | <span data-ttu-id="76f31-130">Члены [ **D3D10ного \_ образца \_**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span><span class="sxs-lookup"><span data-stu-id="76f31-130">Members of [**D3D10\_SAMPLER\_DESC**](/windows/desktop/api/D3D10/ns-d3d10-d3d10_sampler_desc)</span></span> |

<span data-ttu-id="76f31-131">Примеры см. в разделе [тип образца (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) .</span><span class="sxs-lookup"><span data-stu-id="76f31-131">See [Sampler type (DirectX HLSL)](../direct3dhlsl/dx-graphics-hlsl-sampler.md) for examples.</span></span>

## <a name="effect-object-state"></a><span data-ttu-id="76f31-132">Состояние объекта Effect</span><span class="sxs-lookup"><span data-stu-id="76f31-132">Effect object state</span></span>

| <span data-ttu-id="76f31-133">Этот объект Effect</span><span class="sxs-lookup"><span data-stu-id="76f31-133">This effect object</span></span> | <span data-ttu-id="76f31-134">Соответствует параметру</span><span class="sxs-lookup"><span data-stu-id="76f31-134">Maps to</span></span> |
|-|-|
| <span data-ttu-id="76f31-135">растеризерстате</span><span class="sxs-lookup"><span data-stu-id="76f31-135">RASTERIZERSTATE</span></span> | <span data-ttu-id="76f31-136">Объект состояния состояния средства программной [прорисовки](#rasterizer-state) .</span><span class="sxs-lookup"><span data-stu-id="76f31-136">A [Rasterizer State](#rasterizer-state) state object.</span></span> |
| <span data-ttu-id="76f31-137">депсстенЦилстате</span><span class="sxs-lookup"><span data-stu-id="76f31-137">DEPTHSTENCILSTATE</span></span> | <span data-ttu-id="76f31-138">Объект состояния " [глубина" и "набор элементов](#depth-and-stencil-state) ".</span><span class="sxs-lookup"><span data-stu-id="76f31-138">A [Depth and Stencil State](#depth-and-stencil-state) state object.</span></span> |
| <span data-ttu-id="76f31-139">блендстате</span><span class="sxs-lookup"><span data-stu-id="76f31-139">BLENDSTATE</span></span> | <span data-ttu-id="76f31-140">Объект состояния [смешения состояния](#blend-state) .</span><span class="sxs-lookup"><span data-stu-id="76f31-140">A [Blend State](#blend-state) state object.</span></span> |
| <span data-ttu-id="76f31-141">вертексшадер</span><span class="sxs-lookup"><span data-stu-id="76f31-141">VERTEXSHADER</span></span> | <span data-ttu-id="76f31-142">Скомпилированный объект шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="76f31-142">A compiled vertex shader object.</span></span> |
| <span data-ttu-id="76f31-143">PIXELSHADER</span><span class="sxs-lookup"><span data-stu-id="76f31-143">PIXELSHADER</span></span> | <span data-ttu-id="76f31-144">Скомпилированный объект шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="76f31-144">A compiled pixel shader object.</span></span> |
| <span data-ttu-id="76f31-145">жеометришадер</span><span class="sxs-lookup"><span data-stu-id="76f31-145">GEOMETRYSHADER</span></span> | <span data-ttu-id="76f31-146">Скомпилированный объект шейдера Geometry.</span><span class="sxs-lookup"><span data-stu-id="76f31-146">A compiled geometry shader object.</span></span> |
| <span data-ttu-id="76f31-147">DS \_ СТЕНЦИЛРЕФ AB \_ блендфактор AB \_ самплемаск</span><span class="sxs-lookup"><span data-stu-id="76f31-147">DS\_STENCILREF AB\_BLENDFACTOR AB\_SAMPLEMASK</span></span> | <span data-ttu-id="76f31-148">Члены [**D3D10 \_ Pass \_ DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span><span class="sxs-lookup"><span data-stu-id="76f31-148">Members of [**D3D10\_PASS\_DESC**](/windows/desktop/api/d3d10effect/ns-d3d10effect-d3d10_pass_desc).</span></span> |

## <a name="defining-and-using-state-objects"></a><span data-ttu-id="76f31-149">Определение и использование объектов состояния</span><span class="sxs-lookup"><span data-stu-id="76f31-149">Defining and using state objects</span></span>

<span data-ttu-id="76f31-150">Объекты состояния объявляются в файлах FX в следующем формате.</span><span class="sxs-lookup"><span data-stu-id="76f31-150">State objects are declared in FX files in the following format.</span></span> <span data-ttu-id="76f31-151">*Статеобжекттипе* — одно из состояний, перечисленных выше, а *MemberName* — имя любого члена, который будет иметь значение, отличное от значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="76f31-151">*StateObjectType* is one of the states listed above, and *MemberName* is the name of any member that will have a non-default value.</span></span>

```
StateObjectType ObjectName {
 MemberName = value;
 ...
 MemberName = value;
};
```

<span data-ttu-id="76f31-152">Например, чтобы настроить объект состояния Blend с Алфатоковеражеенабле, а Бленденабле \[ 0 \] — значением **false**, используется следующий код.</span><span class="sxs-lookup"><span data-stu-id="76f31-152">For example, to set up a blend state object with AlphaToCoverageEnable and BlendEnable\[0\] set to **FALSE**, the following code would be used.</span></span>

```
BlendState NoBlend {
 AlphaToCoverageEnable = FALSE;
 BlendEnable[0] = FALSE;
};
```

<span data-ttu-id="76f31-153">Объект состояния применяется к методу Pass с помощью одной из функций Сетстатеграуп, описанных в разделе [синтаксис методики работы (Direct3D 10)](d3d10-effect-technique-syntax.md).</span><span class="sxs-lookup"><span data-stu-id="76f31-153">The state object is applied to a technique pass using one of the SetStateGroup functions described in [Effect Technique Syntax (Direct3D 10)](d3d10-effect-technique-syntax.md).</span></span> <span data-ttu-id="76f31-154">Например, для применения объекта Блендстате, описанного выше, будет использоваться следующий код.</span><span class="sxs-lookup"><span data-stu-id="76f31-154">For example, to apply the BlendState object described above the following code would be used.</span></span>

```
SetBlendState( NoBlend, float4( 0.0f, 0.0f, 0.0f, 0.0f ), 0xFFFFFFFF );
```

<span data-ttu-id="76f31-155">Учебник, в котором описывается использование состояний, см. в разделе [Управление состоянием](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span><span class="sxs-lookup"><span data-stu-id="76f31-155">For a tutorial describing the use of states see [State management](https://msdn.microsoft.com/library/Ee416550(v=VS.85).aspx).</span></span>

## <a name="related-topics"></a><span data-ttu-id="76f31-156">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="76f31-156">Related topics</span></span>

* [<span data-ttu-id="76f31-157">Синтаксис методики эффектов</span><span class="sxs-lookup"><span data-stu-id="76f31-157">Effect Technique Syntax</span></span>](d3d10-effect-technique-syntax.md)
* [<span data-ttu-id="76f31-158">Формат эффектов (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="76f31-158">Effect Format (Direct3D 10)</span></span>](d3d10-effect-format.md)
