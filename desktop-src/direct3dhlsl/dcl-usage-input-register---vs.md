---
title: Ввод dcl_usage (SM1, SM2, SM3-VS ASM)
description: Объявите ассоциацию между использованием элемента вершины и индексом использования для входного регистра шейдера вершин.
ms.assetid: e0360f4d-1250-4dc5-b790-372b303a37a8
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: ae4b024bbce0636127b0ed0fc5f42bc466e1b7fd
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129691"
---
# <a name="dcl_usage-input-sm1-sm2-sm3---vs-asm"></a><span data-ttu-id="41782-103">\_входные данные об использовании дкл (SM1, SM2, SM3-VS ASM)</span><span class="sxs-lookup"><span data-stu-id="41782-103">dcl\_usage input (sm1, sm2, sm3 - vs asm)</span></span>

<span data-ttu-id="41782-104">Объявите ассоциацию между использованием элемента вершины и индексом использования для входного регистра шейдера вершин.</span><span class="sxs-lookup"><span data-stu-id="41782-104">Declare the association between a vertex element usage and a usage index for a vertex shader input register.</span></span>

## <a name="syntax"></a><span data-ttu-id="41782-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="41782-105">Syntax</span></span>

<span data-ttu-id="41782-106">\_ \[ индекс использования дкл \_ Usage \] v\#</span><span class="sxs-lookup"><span data-stu-id="41782-106">dcl\_usage\[usage\_index\] v\#</span></span>



 

<span data-ttu-id="41782-107">Где:</span><span class="sxs-lookup"><span data-stu-id="41782-107">Where:</span></span>

-   <span data-ttu-id="41782-108">\_Использование дкл определяет, как будут использоваться данные регистра.</span><span class="sxs-lookup"><span data-stu-id="41782-108">dcl\_usage identifies how the register data will be used.</span></span> <span data-ttu-id="41782-109">Это то же значение, что и члены [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) без префикса D3DDECLUSAGE.</span><span class="sxs-lookup"><span data-stu-id="41782-109">This is the same value as the members of [**D3DDECLUSAGE**](/windows/desktop/direct3d9/d3ddeclusage) without the D3DDECLUSAGE prefix.</span></span>
-   <span data-ttu-id="41782-110">\_индекс использования — это необязательный целочисленный индекс от 0 до 15.</span><span class="sxs-lookup"><span data-stu-id="41782-110">usage\_index is an optional integer index between 0 and 15.</span></span> <span data-ttu-id="41782-111">Он изменяет данные об использовании.</span><span class="sxs-lookup"><span data-stu-id="41782-111">It modifies the usage data.</span></span> <span data-ttu-id="41782-112">Индекс соответствует индексу использования в объявлении вершины.</span><span class="sxs-lookup"><span data-stu-id="41782-112">The index matches the usage index in a vertex declaration.</span></span> <span data-ttu-id="41782-113">См. [Описание вершины (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span><span class="sxs-lookup"><span data-stu-id="41782-113">See [Vertex Declaration (Direct3D 9)](/windows/desktop/direct3d9/vertex-declaration).</span></span> <span data-ttu-id="41782-114">Индекс добавляется к значению использования (дкл \_ Usage) без пробелов.</span><span class="sxs-lookup"><span data-stu-id="41782-114">The index is appended to the usage value (dcl\_usage ) with no space.</span></span> <span data-ttu-id="41782-115">Если он не указан, предполагается, что он равен 0.</span><span class="sxs-lookup"><span data-stu-id="41782-115">If it is not supplied, it is assumed to be 0.</span></span>
-   <span data-ttu-id="41782-116">v \# является [входным регистром](dx9-graphics-reference-asm-vs-registers-input.md).</span><span class="sxs-lookup"><span data-stu-id="41782-116">v\# is a [Input Register](dx9-graphics-reference-asm-vs-registers-input.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="41782-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="41782-117">Remarks</span></span>



| <span data-ttu-id="41782-118">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="41782-118">Vertex shader versions</span></span> | <span data-ttu-id="41782-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="41782-119">1\_1</span></span> | <span data-ttu-id="41782-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="41782-120">2\_0</span></span> | <span data-ttu-id="41782-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="41782-121">2\_x</span></span> | <span data-ttu-id="41782-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="41782-122">2\_sw</span></span> | <span data-ttu-id="41782-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="41782-123">3\_0</span></span> | <span data-ttu-id="41782-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="41782-124">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="41782-125">\_Использование дкл</span><span class="sxs-lookup"><span data-stu-id="41782-125">dcl\_usage</span></span>             | <span data-ttu-id="41782-126">x</span><span class="sxs-lookup"><span data-stu-id="41782-126">x</span></span>    | <span data-ttu-id="41782-127">x</span><span class="sxs-lookup"><span data-stu-id="41782-127">x</span></span>    | <span data-ttu-id="41782-128">x</span><span class="sxs-lookup"><span data-stu-id="41782-128">x</span></span>    | <span data-ttu-id="41782-129">x</span><span class="sxs-lookup"><span data-stu-id="41782-129">x</span></span>     | <span data-ttu-id="41782-130">x</span><span class="sxs-lookup"><span data-stu-id="41782-130">x</span></span>    | <span data-ttu-id="41782-131">x</span><span class="sxs-lookup"><span data-stu-id="41782-131">x</span></span>     |



 

<span data-ttu-id="41782-132">Все \_ инструкции по использованию дкл должны располагаться перед первой исполняемой инструкцией.</span><span class="sxs-lookup"><span data-stu-id="41782-132">All dcl\_usage instructions must appear before the first executable instruction.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41782-133">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="41782-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41782-134">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="41782-134">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 
