---
title: vs
description: Эта инструкция указывает номер версии шейдера. Эта инструкция работает со всеми версиями шейдера.
ms.assetid: edcbaff3-eb32-49e6-80de-621b67d4df75
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: baf773d7607aa575bd575339bde072b3dc04b224
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412229"
---
# <a name="vs"></a><span data-ttu-id="a7f3d-104">vs</span><span class="sxs-lookup"><span data-stu-id="a7f3d-104">vs</span></span>

<span data-ttu-id="a7f3d-105">Эта инструкция указывает номер версии шейдера.</span><span class="sxs-lookup"><span data-stu-id="a7f3d-105">This instruction specifies the shader version number.</span></span> <span data-ttu-id="a7f3d-106">Эта инструкция работает со всеми версиями шейдера.</span><span class="sxs-lookup"><span data-stu-id="a7f3d-106">This instruction works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7f3d-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a7f3d-107">Syntax</span></span>


```
vs_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="a7f3d-108">Входные аргументы</span><span class="sxs-lookup"><span data-stu-id="a7f3d-108">Input Arguments</span></span>

<span data-ttu-id="a7f3d-109">Входные аргументы содержат один основной номер версии с одним вложенным номером версии.</span><span class="sxs-lookup"><span data-stu-id="a7f3d-109">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="a7f3d-110">Допустимые сочетания перечислены в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="a7f3d-110">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="a7f3d-111">Основные версии</span><span class="sxs-lookup"><span data-stu-id="a7f3d-111">Main versions</span></span> | <span data-ttu-id="a7f3d-112">Подверсии</span><span class="sxs-lookup"><span data-stu-id="a7f3d-112">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="a7f3d-113">1</span><span class="sxs-lookup"><span data-stu-id="a7f3d-113">1</span></span>             | <span data-ttu-id="a7f3d-114">1</span><span class="sxs-lookup"><span data-stu-id="a7f3d-114">1</span></span>                              |
| <span data-ttu-id="a7f3d-115">2</span><span class="sxs-lookup"><span data-stu-id="a7f3d-115">2</span></span>             | <span data-ttu-id="a7f3d-116">0, SW (программное обеспечение), x (расширенная)</span><span class="sxs-lookup"><span data-stu-id="a7f3d-116">0, sw (software), x (extended)</span></span> |
| <span data-ttu-id="a7f3d-117">3</span><span class="sxs-lookup"><span data-stu-id="a7f3d-117">3</span></span>             | <span data-ttu-id="a7f3d-118">0, SW (программное обеспечение)</span><span class="sxs-lookup"><span data-stu-id="a7f3d-118">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="a7f3d-119">Примечания</span><span class="sxs-lookup"><span data-stu-id="a7f3d-119">Remarks</span></span>



| <span data-ttu-id="a7f3d-120">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="a7f3d-120">Vertex shader versions</span></span> | <span data-ttu-id="a7f3d-121">1\_1</span><span class="sxs-lookup"><span data-stu-id="a7f3d-121">1\_1</span></span> | <span data-ttu-id="a7f3d-122">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a7f3d-122">2\_0</span></span> | <span data-ttu-id="a7f3d-123">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="a7f3d-123">2\_x</span></span> | <span data-ttu-id="a7f3d-124">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a7f3d-124">2\_sw</span></span> | <span data-ttu-id="a7f3d-125">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="a7f3d-125">3\_0</span></span> | <span data-ttu-id="a7f3d-126">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="a7f3d-126">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="a7f3d-127">vs</span><span class="sxs-lookup"><span data-stu-id="a7f3d-127">vs</span></span>                     | <span data-ttu-id="a7f3d-128">x</span><span class="sxs-lookup"><span data-stu-id="a7f3d-128">x</span></span>    | <span data-ttu-id="a7f3d-129">x</span><span class="sxs-lookup"><span data-stu-id="a7f3d-129">x</span></span>    | <span data-ttu-id="a7f3d-130">x</span><span class="sxs-lookup"><span data-stu-id="a7f3d-130">x</span></span>    | <span data-ttu-id="a7f3d-131">x</span><span class="sxs-lookup"><span data-stu-id="a7f3d-131">x</span></span>     | <span data-ttu-id="a7f3d-132">x</span><span class="sxs-lookup"><span data-stu-id="a7f3d-132">x</span></span>    | <span data-ttu-id="a7f3d-133">x</span><span class="sxs-lookup"><span data-stu-id="a7f3d-133">x</span></span>     |



 

<span data-ttu-id="a7f3d-134">Эта инструкция должна быть первой инструкцией, отличной от комментария, в шейдере вершин.</span><span class="sxs-lookup"><span data-stu-id="a7f3d-134">This instruction must be the first non-comment instruction in a vertex shader.</span></span>

<span data-ttu-id="a7f3d-135">Эта инструкция поддерживается во всех версиях шейдеров вершин.</span><span class="sxs-lookup"><span data-stu-id="a7f3d-135">This instruction is supported in all vertex shader versions.</span></span>

<span data-ttu-id="a7f3d-136">Аппаратно-ускоренные версии программного обеспечения (версии без \_ SW в номере версии) могут обрабатывать вершины с акцелеаратион оборудования или использовать программную обработку вершин.</span><span class="sxs-lookup"><span data-stu-id="a7f3d-136">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="a7f3d-137">Версии программного обеспечения (версии с \_ SW по номеру версии) обрабатывают вершины только с программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="a7f3d-137">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="a7f3d-138">Примеры</span><span class="sxs-lookup"><span data-stu-id="a7f3d-138">Examples</span></span>

<span data-ttu-id="a7f3d-139">В этом частичном примере объявляется \_ шейдер вершин версии 1 1.</span><span class="sxs-lookup"><span data-stu-id="a7f3d-139">This partial example declares a version 1\_1 vertex shader.</span></span>


```
vs_1_1
```



<span data-ttu-id="a7f3d-140">В этом частичном примере объявляется программный шейдер вершин версии 2.</span><span class="sxs-lookup"><span data-stu-id="a7f3d-140">This partial example declares a version 2 software vertex shader.</span></span>


```
vs_2_sw
```



## <a name="related-topics"></a><span data-ttu-id="a7f3d-141">См. также</span><span class="sxs-lookup"><span data-stu-id="a7f3d-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a7f3d-142">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="a7f3d-142">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




