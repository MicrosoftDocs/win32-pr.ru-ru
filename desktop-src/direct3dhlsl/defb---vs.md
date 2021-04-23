---
title: дефб — VS
description: Определяет логическое константное значение, которое должно быть загружено в любое время, когда шейдер задается устройством.
ms.assetid: 1db41115-14aa-462e-a7ee-c0a53fee97d8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 9bd5ef8ea4218890c025fdebc87154ca1224d33c
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103987535"
---
# <a name="defb---vs"></a><span data-ttu-id="31def-103">дефб — VS</span><span class="sxs-lookup"><span data-stu-id="31def-103">defb - vs</span></span>

<span data-ttu-id="31def-104">Определяет логическое константное значение, которое должно быть загружено в любое время, когда шейдер задается устройством.</span><span class="sxs-lookup"><span data-stu-id="31def-104">Defines a Boolean constant value, which should be loaded anytime a shader is set to a device.</span></span>

## <a name="syntax"></a><span data-ttu-id="31def-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="31def-105">Syntax</span></span>



| <span data-ttu-id="31def-106">дефб dest, Булеанвалуе</span><span class="sxs-lookup"><span data-stu-id="31def-106">defb dest, booleanValue</span></span> |
|-------------------------|



 

<span data-ttu-id="31def-107">где</span><span class="sxs-lookup"><span data-stu-id="31def-107">where</span></span>

-   <span data-ttu-id="31def-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="31def-108">dst is the destination register.</span></span>
-   <span data-ttu-id="31def-109">Булеанвалуе — это логическое значение, true или false.</span><span class="sxs-lookup"><span data-stu-id="31def-109">booleanValue is a boolean value, either True or False.</span></span>

## <a name="remarks"></a><span data-ttu-id="31def-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="31def-110">Remarks</span></span>



| <span data-ttu-id="31def-111">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="31def-111">Vertex shader versions</span></span> | <span data-ttu-id="31def-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="31def-112">1\_1</span></span> | <span data-ttu-id="31def-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31def-113">2\_0</span></span> | <span data-ttu-id="31def-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="31def-114">2\_x</span></span> | <span data-ttu-id="31def-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="31def-115">2\_sw</span></span> | <span data-ttu-id="31def-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="31def-116">3\_0</span></span> | <span data-ttu-id="31def-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="31def-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="31def-118">дефб</span><span class="sxs-lookup"><span data-stu-id="31def-118">defb</span></span>                   |      | <span data-ttu-id="31def-119">x</span><span class="sxs-lookup"><span data-stu-id="31def-119">x</span></span>    | <span data-ttu-id="31def-120">x</span><span class="sxs-lookup"><span data-stu-id="31def-120">x</span></span>    | <span data-ttu-id="31def-121">x</span><span class="sxs-lookup"><span data-stu-id="31def-121">x</span></span>     | <span data-ttu-id="31def-122">x</span><span class="sxs-lookup"><span data-stu-id="31def-122">x</span></span>    | <span data-ttu-id="31def-123">x</span><span class="sxs-lookup"><span data-stu-id="31def-123">x</span></span>     |



 

<span data-ttu-id="31def-124">Инструкция дефб-VS определяет логическую константу шейдера, значение которой загружается каждый раз, когда шейдер задается устройством.</span><span class="sxs-lookup"><span data-stu-id="31def-124">The defb - vs instruction defines a boolean shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="31def-125">Они называются прямыми константами.</span><span class="sxs-lookup"><span data-stu-id="31def-125">These are called immediate constants.</span></span> <span data-ttu-id="31def-126">Немедленные константы имеют приоритет над константами, заданными методом API Сетвертексшадерконстантб.</span><span class="sxs-lookup"><span data-stu-id="31def-126">Immediate constants take precedence over constants set by the API method SetVertexShaderConstantB.</span></span>

<span data-ttu-id="31def-127">Существует два способа задать логическую константу в шейдере.</span><span class="sxs-lookup"><span data-stu-id="31def-127">There are two ways to set a boolean constant in a shader.</span></span>

1.  <span data-ttu-id="31def-128">Используйте дефб-VS для определения константы непосредственно внутри шейдера.</span><span class="sxs-lookup"><span data-stu-id="31def-128">Use defb - vs to define the constant directly inside a shader.</span></span>
2.  <span data-ttu-id="31def-129">Используйте методы API для задания константы.</span><span class="sxs-lookup"><span data-stu-id="31def-129">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="31def-130">Чтобы задать логическую константу, используйте [**сетвертексшадерконстантб**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) .</span><span class="sxs-lookup"><span data-stu-id="31def-130">Use [**SetVertexShaderConstantB**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantb) to set a Boolean constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="31def-131">См. также</span><span class="sxs-lookup"><span data-stu-id="31def-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="31def-132">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="31def-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="31def-133">Сравнение DEF и</span><span class="sxs-lookup"><span data-stu-id="31def-133">def - vs</span></span>](def---vs.md)
</dt> <dt>

[<span data-ttu-id="31def-134">дефи — VS</span><span class="sxs-lookup"><span data-stu-id="31def-134">defi - vs</span></span>](defi---vs.md)
</dt> </dl>

 

 