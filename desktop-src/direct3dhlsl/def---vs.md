---
title: Сравнение DEF и
description: Определяет константы шейдера вершин.
ms.assetid: 13274e16-990f-4de8-9c99-6c268c7c06ef
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 7b5a55cb13eb7197986349c602ec35855a3f6364
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104261000"
---
# <a name="def---vs"></a><span data-ttu-id="e6a95-103">Сравнение DEF и</span><span class="sxs-lookup"><span data-stu-id="e6a95-103">def - vs</span></span>

<span data-ttu-id="e6a95-104">Определяет константы шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="e6a95-104">Defines vertex shader constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a95-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6a95-105">Syntax</span></span>



| <span data-ttu-id="e6a95-106">DEF, float1, float2, float3, float4</span><span class="sxs-lookup"><span data-stu-id="e6a95-106">def dst, float1, float2, float3, float4</span></span> |
|-----------------------------------------|



 

<span data-ttu-id="e6a95-107">где</span><span class="sxs-lookup"><span data-stu-id="e6a95-107">where</span></span>

-   <span data-ttu-id="e6a95-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="e6a95-108">dst is the destination register.</span></span>
-   <span data-ttu-id="e6a95-109">float1, float2, float3, float4 — четыре числа с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="e6a95-109">float1, float2, float3, float4 are four floating point numbers.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a95-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="e6a95-110">Remarks</span></span>



| <span data-ttu-id="e6a95-111">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="e6a95-111">Vertex shader versions</span></span> | <span data-ttu-id="e6a95-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="e6a95-112">1\_1</span></span> | <span data-ttu-id="e6a95-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e6a95-113">2\_0</span></span> | <span data-ttu-id="e6a95-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="e6a95-114">2\_x</span></span> | <span data-ttu-id="e6a95-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e6a95-115">2\_sw</span></span> | <span data-ttu-id="e6a95-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="e6a95-116">3\_0</span></span> | <span data-ttu-id="e6a95-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="e6a95-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="e6a95-118">def</span><span class="sxs-lookup"><span data-stu-id="e6a95-118">def</span></span>                    | <span data-ttu-id="e6a95-119">x</span><span class="sxs-lookup"><span data-stu-id="e6a95-119">x</span></span>    | <span data-ttu-id="e6a95-120">x</span><span class="sxs-lookup"><span data-stu-id="e6a95-120">x</span></span>    | <span data-ttu-id="e6a95-121">x</span><span class="sxs-lookup"><span data-stu-id="e6a95-121">x</span></span>    | <span data-ttu-id="e6a95-122">x</span><span class="sxs-lookup"><span data-stu-id="e6a95-122">x</span></span>     | <span data-ttu-id="e6a95-123">x</span><span class="sxs-lookup"><span data-stu-id="e6a95-123">x</span></span>    | <span data-ttu-id="e6a95-124">x</span><span class="sxs-lookup"><span data-stu-id="e6a95-124">x</span></span>     |



 

<span data-ttu-id="e6a95-125">Инструкция DEF определяет константу шейдера, значение которой загружается в любое время в качестве шейдера для устройства.</span><span class="sxs-lookup"><span data-stu-id="e6a95-125">The def instruction defines a shader constant whose value is loaded anytime a shader is set to a device.</span></span> <span data-ttu-id="e6a95-126">Они называются прямыми константами.</span><span class="sxs-lookup"><span data-stu-id="e6a95-126">These are called immediate constants.</span></span> <span data-ttu-id="e6a95-127">Немедленные константы имеют приоритет над константами, заданными методами API Сетвертексшадерконстантф.</span><span class="sxs-lookup"><span data-stu-id="e6a95-127">Immediate constants take precedence over constants set by API methods SetVertexShaderConstantF.</span></span>

<span data-ttu-id="e6a95-128">Существует два способа задать константу в шейдере.</span><span class="sxs-lookup"><span data-stu-id="e6a95-128">There are two ways to set a constant in a shader.</span></span>

1.  <span data-ttu-id="e6a95-129">Используйте DEF-и для определения константы непосредственно внутри шейдера.</span><span class="sxs-lookup"><span data-stu-id="e6a95-129">Use def - vs to define the constant directly inside a shader.</span></span>

    <span data-ttu-id="e6a95-130">DEF-VS может определять только константы с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="e6a95-130">def - vs can only define floating-point constants.</span></span>

2.  <span data-ttu-id="e6a95-131">Используйте методы API для задания константы.</span><span class="sxs-lookup"><span data-stu-id="e6a95-131">Use the API methods to set a constant.</span></span>
    -   <span data-ttu-id="e6a95-132">Используйте [**сетвертексшадерконстантф**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) для установки константы с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="e6a95-132">Use [**SetVertexShaderConstantF**](/windows/desktop/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstantf) to set a floating-point constant.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e6a95-133">См. также</span><span class="sxs-lookup"><span data-stu-id="e6a95-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e6a95-134">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="e6a95-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> <dt>

[<span data-ttu-id="e6a95-135">дефи — VS</span><span class="sxs-lookup"><span data-stu-id="e6a95-135">defi - vs</span></span>](defi---vs.md)
</dt> <dt>

[<span data-ttu-id="e6a95-136">дефб — VS</span><span class="sxs-lookup"><span data-stu-id="e6a95-136">defb - vs</span></span>](defb---vs.md)
</dt> </dl>

 

 