---
title: дефб-PS
description: Определяет логическое константное значение, которое должно быть загружено каждый раз, когда шейдер задается устройством.
ms.assetid: bb0b87cb-08a4-4790-88da-e398cea62911
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b9437c7d6347da4bafae566386e09e4bc782bd16
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793032"
---
# <a name="defb---ps"></a><span data-ttu-id="7ac2f-103">дефб-PS</span><span class="sxs-lookup"><span data-stu-id="7ac2f-103">defb - ps</span></span>

<span data-ttu-id="7ac2f-104">Определяет логическое константное значение, которое должно быть загружено каждый раз, когда шейдер задается устройством.</span><span class="sxs-lookup"><span data-stu-id="7ac2f-104">Defines a boolean constant value, which should be loaded any time a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ac2f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7ac2f-105">Syntax</span></span>



| <span data-ttu-id="7ac2f-106">дефб dest, Булеанвалуе</span><span class="sxs-lookup"><span data-stu-id="7ac2f-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="7ac2f-107">где</span><span class="sxs-lookup"><span data-stu-id="7ac2f-107">where</span></span>

-   <span data-ttu-id="7ac2f-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="7ac2f-108">dst is the destination register.</span></span>
-   <span data-ttu-id="7ac2f-109">Булеанвалуе — это одно логическое значение, true или false.</span><span class="sxs-lookup"><span data-stu-id="7ac2f-109">booleanValue is a single boolean value, either true or false.</span></span>

## <a name="remarks"></a><span data-ttu-id="7ac2f-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="7ac2f-110">Remarks</span></span>



| <span data-ttu-id="7ac2f-111">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="7ac2f-111">Pixel shader versions</span></span> | <span data-ttu-id="7ac2f-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="7ac2f-112">1\_1</span></span> | <span data-ttu-id="7ac2f-113">1\_2</span><span class="sxs-lookup"><span data-stu-id="7ac2f-113">1\_2</span></span> | <span data-ttu-id="7ac2f-114">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="7ac2f-114">1\_3</span></span> | <span data-ttu-id="7ac2f-115">1\_4</span><span class="sxs-lookup"><span data-stu-id="7ac2f-115">1\_4</span></span> | <span data-ttu-id="7ac2f-116">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7ac2f-116">2\_0</span></span> | <span data-ttu-id="7ac2f-117">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="7ac2f-117">2\_x</span></span> | <span data-ttu-id="7ac2f-118">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7ac2f-118">2\_sw</span></span> | <span data-ttu-id="7ac2f-119">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="7ac2f-119">3\_0</span></span> | <span data-ttu-id="7ac2f-120">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="7ac2f-120">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="7ac2f-121">дефб</span><span class="sxs-lookup"><span data-stu-id="7ac2f-121">defb</span></span>                  |      |      |      |      |      | <span data-ttu-id="7ac2f-122">x</span><span class="sxs-lookup"><span data-stu-id="7ac2f-122">x</span></span>    | <span data-ttu-id="7ac2f-123">x</span><span class="sxs-lookup"><span data-stu-id="7ac2f-123">x</span></span>     | <span data-ttu-id="7ac2f-124">x</span><span class="sxs-lookup"><span data-stu-id="7ac2f-124">x</span></span>    | <span data-ttu-id="7ac2f-125">x</span><span class="sxs-lookup"><span data-stu-id="7ac2f-125">x</span></span>     |



 

<span data-ttu-id="7ac2f-126">Инструкция дефб определяет логическую константу шейдера, значение которой загружается каждый раз, когда шейдер задается устройством.</span><span class="sxs-lookup"><span data-stu-id="7ac2f-126">The defb instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="7ac2f-127">Они называются прямыми константами.</span><span class="sxs-lookup"><span data-stu-id="7ac2f-127">These are called immediate constants.</span></span> <span data-ttu-id="7ac2f-128">Немедленные константы имеют приоритет над константами, заданными методом API Сетпикселшадерконстантб.</span><span class="sxs-lookup"><span data-stu-id="7ac2f-128">Immediate constants take precedence over constants set by the API method SetPixelShaderConstantB.</span></span>

<span data-ttu-id="7ac2f-129">Существует два способа задания булеанконстант в шейдере.</span><span class="sxs-lookup"><span data-stu-id="7ac2f-129">There are two ways to set a booleanconstant in a shader.</span></span>

1.  <span data-ttu-id="7ac2f-130">Используйте дефб, чтобы определить константу непосредственно внутри шейдера.</span><span class="sxs-lookup"><span data-stu-id="7ac2f-130">Use defb to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="7ac2f-131">Используйте методы API для задания константы.</span><span class="sxs-lookup"><span data-stu-id="7ac2f-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="7ac2f-132">Чтобы задать логическую константу, используйте [**сетпикселшадерконстантб**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) .</span><span class="sxs-lookup"><span data-stu-id="7ac2f-132">Use [**SetPixelShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ac2f-133">См. также</span><span class="sxs-lookup"><span data-stu-id="7ac2f-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ac2f-134">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="7ac2f-134">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> <dt>

[<span data-ttu-id="7ac2f-135">DEF-PS</span><span class="sxs-lookup"><span data-stu-id="7ac2f-135">def - ps</span></span>](def---ps.md)
</dt> <dt>

[<span data-ttu-id="7ac2f-136">дефи-PS</span><span class="sxs-lookup"><span data-stu-id="7ac2f-136">defi - ps</span></span>](defi---ps.md)
</dt> </dl>

 

 