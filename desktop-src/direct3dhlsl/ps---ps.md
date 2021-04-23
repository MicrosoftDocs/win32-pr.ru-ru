---
title: ps
description: Эта инструкция указывает номер версии шейдера и работает во всех версиях шейдера.
ms.assetid: 953b1d66-09c1-4ad5-96d4-acb49a1f244c
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: bdf251d8b5618916365348ab3bf62a89ea552de1
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104996963"
---
# <a name="ps"></a><span data-ttu-id="6bc68-103">ps</span><span class="sxs-lookup"><span data-stu-id="6bc68-103">ps</span></span>

<span data-ttu-id="6bc68-104">Эта инструкция указывает номер версии шейдера и работает во всех версиях шейдера.</span><span class="sxs-lookup"><span data-stu-id="6bc68-104">This instruction specifies the shader version number and works on all shader versions.</span></span>

## <a name="syntax"></a><span data-ttu-id="6bc68-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6bc68-105">Syntax</span></span>


```
ps_mainVer_subVer
```



## <a name="input-arguments"></a><span data-ttu-id="6bc68-106">Входные аргументы</span><span class="sxs-lookup"><span data-stu-id="6bc68-106">Input Arguments</span></span>

<span data-ttu-id="6bc68-107">Входные аргументы содержат один основной номер версии с одним вложенным номером версии.</span><span class="sxs-lookup"><span data-stu-id="6bc68-107">Input arguments contain a single main version number with a single sub version number.</span></span> <span data-ttu-id="6bc68-108">Допустимые сочетания перечислены в таблице ниже.</span><span class="sxs-lookup"><span data-stu-id="6bc68-108">The allowable combinations are listed in the table below.</span></span>



| <span data-ttu-id="6bc68-109">Основные версии</span><span class="sxs-lookup"><span data-stu-id="6bc68-109">Main versions</span></span> | <span data-ttu-id="6bc68-110">Подверсии</span><span class="sxs-lookup"><span data-stu-id="6bc68-110">Sub versions</span></span>                   |
|---------------|--------------------------------|
| <span data-ttu-id="6bc68-111">1</span><span class="sxs-lookup"><span data-stu-id="6bc68-111">1</span></span>             | <span data-ttu-id="6bc68-112">1, 2, 3, 4</span><span class="sxs-lookup"><span data-stu-id="6bc68-112">1, 2, 3, 4</span></span>                     |
| <span data-ttu-id="6bc68-113">2</span><span class="sxs-lookup"><span data-stu-id="6bc68-113">2</span></span>             | <span data-ttu-id="6bc68-114">0, x (расширенная), SW (программное обеспечение)</span><span class="sxs-lookup"><span data-stu-id="6bc68-114">0, x (extended), sw (software)</span></span> |
| <span data-ttu-id="6bc68-115">3</span><span class="sxs-lookup"><span data-stu-id="6bc68-115">3</span></span>             | <span data-ttu-id="6bc68-116">0, SW (программное обеспечение)</span><span class="sxs-lookup"><span data-stu-id="6bc68-116">0, sw (software)</span></span>               |



 

## <a name="remarks"></a><span data-ttu-id="6bc68-117">Примечания</span><span class="sxs-lookup"><span data-stu-id="6bc68-117">Remarks</span></span>



| <span data-ttu-id="6bc68-118">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="6bc68-118">Pixel shader versions</span></span> | <span data-ttu-id="6bc68-119">1\_1</span><span class="sxs-lookup"><span data-stu-id="6bc68-119">1\_1</span></span> | <span data-ttu-id="6bc68-120">1\_2</span><span class="sxs-lookup"><span data-stu-id="6bc68-120">1\_2</span></span> | <span data-ttu-id="6bc68-121">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="6bc68-121">1\_3</span></span> | <span data-ttu-id="6bc68-122">1\_4</span><span class="sxs-lookup"><span data-stu-id="6bc68-122">1\_4</span></span> | <span data-ttu-id="6bc68-123">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6bc68-123">2\_0</span></span> | <span data-ttu-id="6bc68-124">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="6bc68-124">2\_x</span></span> | <span data-ttu-id="6bc68-125">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6bc68-125">2\_sw</span></span> | <span data-ttu-id="6bc68-126">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="6bc68-126">3\_0</span></span> | <span data-ttu-id="6bc68-127">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="6bc68-127">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="6bc68-128">ps</span><span class="sxs-lookup"><span data-stu-id="6bc68-128">ps</span></span>                    | <span data-ttu-id="6bc68-129">x</span><span class="sxs-lookup"><span data-stu-id="6bc68-129">x</span></span>    | <span data-ttu-id="6bc68-130">x</span><span class="sxs-lookup"><span data-stu-id="6bc68-130">x</span></span>    | <span data-ttu-id="6bc68-131">x</span><span class="sxs-lookup"><span data-stu-id="6bc68-131">x</span></span>    | <span data-ttu-id="6bc68-132">x</span><span class="sxs-lookup"><span data-stu-id="6bc68-132">x</span></span>    | <span data-ttu-id="6bc68-133">x</span><span class="sxs-lookup"><span data-stu-id="6bc68-133">x</span></span>    | <span data-ttu-id="6bc68-134">x</span><span class="sxs-lookup"><span data-stu-id="6bc68-134">x</span></span>    | <span data-ttu-id="6bc68-135">x</span><span class="sxs-lookup"><span data-stu-id="6bc68-135">x</span></span>     | <span data-ttu-id="6bc68-136">x</span><span class="sxs-lookup"><span data-stu-id="6bc68-136">x</span></span>    | <span data-ttu-id="6bc68-137">x</span><span class="sxs-lookup"><span data-stu-id="6bc68-137">x</span></span>     |



 

<span data-ttu-id="6bc68-138">Эта инструкция должна быть первой инструкцией, не являющейся комментарием, в шейдере пикселей.</span><span class="sxs-lookup"><span data-stu-id="6bc68-138">This instruction must be the first non-comment instruction in a pixel shader.</span></span>

<span data-ttu-id="6bc68-139">Аппаратно-ускоренные версии программного обеспечения (версии без \_ SW в номере версии) могут обрабатывать вершины с акцелеаратион оборудования или использовать программную обработку вершин.</span><span class="sxs-lookup"><span data-stu-id="6bc68-139">Hardware accelerated versions of the software (versions without \_sw in the version number), can process vertices with hardware accelearation or use software vertex processing.</span></span> <span data-ttu-id="6bc68-140">Версии программного обеспечения (версии с \_ SW по номеру версии) обрабатывают вершины только с программным обеспечением.</span><span class="sxs-lookup"><span data-stu-id="6bc68-140">Software versions (versions with \_sw in the version number) process vertices only with software.</span></span>

## <a name="examples"></a><span data-ttu-id="6bc68-141">Примеры</span><span class="sxs-lookup"><span data-stu-id="6bc68-141">Examples</span></span>

<span data-ttu-id="6bc68-142">В этом частичном примере объявляется шейдер версии 1 \_ 1 пиксель.</span><span class="sxs-lookup"><span data-stu-id="6bc68-142">This partial example declares a version 1\_1 pixel shader.</span></span>


```
ps_1_1
```



<span data-ttu-id="6bc68-143">В этом частичном примере объявляется шейдер версии 1 \_ 4 пикселей.</span><span class="sxs-lookup"><span data-stu-id="6bc68-143">This partial example declares a version 1\_4 pixel shader.</span></span>


```
ps_1_4
```



## <a name="related-topics"></a><span data-ttu-id="6bc68-144">См. также</span><span class="sxs-lookup"><span data-stu-id="6bc68-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6bc68-145">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="6bc68-145">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




