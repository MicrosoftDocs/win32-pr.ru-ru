---
title: dcl_tessellator_domain (SM5-ASM)
description: Объявите домен тесселяции в разделе объявления поверхности Shader и шейдер домена.
ms.assetid: 11A1D9D0-D848-4750-875B-7060CE1CF42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8724ee9564239ffaca6f5c34a39fb1b4ef967e51
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412232"
---
# <a name="dcl_tessellator_domain-sm5---asm"></a><span data-ttu-id="19c0f-103">\_домен тесселяции дкл \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="19c0f-103">dcl\_tessellator\_domain (sm5 - asm)</span></span>

<span data-ttu-id="19c0f-104">Объявите домен тесселяции в разделе объявления поверхности Shader и шейдер домена.</span><span class="sxs-lookup"><span data-stu-id="19c0f-104">Declare the tessellator domain in a hull shader declaration section, and the domain shader.</span></span>



| <span data-ttu-id="19c0f-105">дкл \_ тесселяция \_ домена {Domain \_ исолине </span><span class="sxs-lookup"><span data-stu-id="19c0f-105">dcl\_tessellator\_domain {domain\_isoline </span></span>\| <span data-ttu-id="19c0f-106">домены \_ </span><span class="sxs-lookup"><span data-stu-id="19c0f-106">domain\_tri </span></span>\| <span data-ttu-id="19c0f-107">\_четыре домена}</span><span class="sxs-lookup"><span data-stu-id="19c0f-107">domain\_quad}</span></span> |
|---------------------------------------------------------------------------|



 



| <span data-ttu-id="19c0f-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="19c0f-108">Item</span></span>                                                                                                                                                                                | <span data-ttu-id="19c0f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="19c0f-109">Description</span></span>                   |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------|
| <span data-ttu-id="19c0f-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*четыре домена домен \_ исолине, \| \_ \| \_ Quad*</span><span class="sxs-lookup"><span data-stu-id="19c0f-110"><span id="domain_isoline___domain_tri___domain_quad"></span><span id="DOMAIN_ISOLINE___DOMAIN_TRI___DOMAIN_QUAD"></span>*domain\_isoline \| domain\_tri \| domain\_quad*</span></span><br/> | <span data-ttu-id="19c0f-111">\[в \] домене.</span><span class="sxs-lookup"><span data-stu-id="19c0f-111">\[in\] The domain.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="19c0f-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="19c0f-112">Remarks</span></span>

<span data-ttu-id="19c0f-113">Поведение не определено, если шейдер поверхности и Шейдер доменов предоставляют несовпадающие домены или другие конфликтующие декаларатионс.</span><span class="sxs-lookup"><span data-stu-id="19c0f-113">Behavior is undefined if the hull shader and domain shader provide mismatching domains or any other conflicting decalarations.</span></span>

<span data-ttu-id="19c0f-114">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="19c0f-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="19c0f-115">Вершина</span><span class="sxs-lookup"><span data-stu-id="19c0f-115">Vertex</span></span> | <span data-ttu-id="19c0f-116">Поверхности</span><span class="sxs-lookup"><span data-stu-id="19c0f-116">Hull</span></span>                 | <span data-ttu-id="19c0f-117">Домен</span><span class="sxs-lookup"><span data-stu-id="19c0f-117">Domain</span></span> | <span data-ttu-id="19c0f-118">Геометрия</span><span class="sxs-lookup"><span data-stu-id="19c0f-118">Geometry</span></span> | <span data-ttu-id="19c0f-119">Пиксель</span><span class="sxs-lookup"><span data-stu-id="19c0f-119">Pixel</span></span> | <span data-ttu-id="19c0f-120">Вычисления</span><span class="sxs-lookup"><span data-stu-id="19c0f-120">Compute</span></span> |
|--------|----------------------|--------|----------|-------|---------|
|        | <span data-ttu-id="19c0f-121">Раздел объявлений</span><span class="sxs-lookup"><span data-stu-id="19c0f-121">Declarations Section</span></span> | <span data-ttu-id="19c0f-122">X</span><span class="sxs-lookup"><span data-stu-id="19c0f-122">X</span></span>      |          |       |         |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="19c0f-123">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="19c0f-123">Minimum Shader Model</span></span>

<span data-ttu-id="19c0f-124">Эта инструкция поддерживается в следующих моделях шейдеров:</span><span class="sxs-lookup"><span data-stu-id="19c0f-124">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="19c0f-125">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="19c0f-125">Shader Model</span></span>                                              | <span data-ttu-id="19c0f-126">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="19c0f-126">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="19c0f-127">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="19c0f-127">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="19c0f-128">да</span><span class="sxs-lookup"><span data-stu-id="19c0f-128">yes</span></span>       |
| [<span data-ttu-id="19c0f-129">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="19c0f-129">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="19c0f-130">Нет</span><span class="sxs-lookup"><span data-stu-id="19c0f-130">no</span></span>        |
| [<span data-ttu-id="19c0f-131">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="19c0f-131">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="19c0f-132">Нет</span><span class="sxs-lookup"><span data-stu-id="19c0f-132">no</span></span>        |
| [<span data-ttu-id="19c0f-133">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19c0f-133">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="19c0f-134">Нет</span><span class="sxs-lookup"><span data-stu-id="19c0f-134">no</span></span>        |
| [<span data-ttu-id="19c0f-135">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19c0f-135">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="19c0f-136">Нет</span><span class="sxs-lookup"><span data-stu-id="19c0f-136">no</span></span>        |
| [<span data-ttu-id="19c0f-137">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19c0f-137">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="19c0f-138">Нет</span><span class="sxs-lookup"><span data-stu-id="19c0f-138">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="19c0f-139">См. также</span><span class="sxs-lookup"><span data-stu-id="19c0f-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="19c0f-140">Сборка Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="19c0f-140">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





