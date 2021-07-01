---
title: Бем-PS
description: Примените фиктивное преобразование «среда выпуклости».
ms.assetid: b41009d4-a2bb-4397-ad23-c95ef2620a66
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1adae07e3e2ebbca085981ca03a3b6449e2ffd9d
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129933"
---
# <a name="bem---ps"></a><span data-ttu-id="0766c-103">Бем-PS</span><span class="sxs-lookup"><span data-stu-id="0766c-103">bem - ps</span></span>

<span data-ttu-id="0766c-104">Примените фиктивное преобразование «среда выпуклости».</span><span class="sxs-lookup"><span data-stu-id="0766c-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="0766c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0766c-105">Syntax</span></span>



| <span data-ttu-id="0766c-106">Бем DST. RG, src0, src1</span><span class="sxs-lookup"><span data-stu-id="0766c-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="0766c-107">where</span><span class="sxs-lookup"><span data-stu-id="0766c-107">where</span></span>

-   <span data-ttu-id="0766c-108">DST. RG DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="0766c-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="0766c-109">Необходимо использовать маску записи красного и зеленого компонентов.</span><span class="sxs-lookup"><span data-stu-id="0766c-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="0766c-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="0766c-110">src0 is a source register.</span></span>
-   <span data-ttu-id="0766c-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="0766c-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="0766c-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="0766c-112">Remarks</span></span>



| <span data-ttu-id="0766c-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="0766c-113">Pixel shader versions</span></span> | <span data-ttu-id="0766c-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="0766c-114">1\_1</span></span> | <span data-ttu-id="0766c-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="0766c-115">1\_2</span></span> | <span data-ttu-id="0766c-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0766c-116">1\_3</span></span> | <span data-ttu-id="0766c-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="0766c-117">1\_4</span></span> | <span data-ttu-id="0766c-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0766c-118">2\_0</span></span> | <span data-ttu-id="0766c-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="0766c-119">2\_x</span></span> | <span data-ttu-id="0766c-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0766c-120">2\_sw</span></span> | <span data-ttu-id="0766c-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="0766c-121">3\_0</span></span> | <span data-ttu-id="0766c-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="0766c-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="0766c-123">бем</span><span class="sxs-lookup"><span data-stu-id="0766c-123">bem</span></span>                   |      |      |      | <span data-ttu-id="0766c-124">x</span><span class="sxs-lookup"><span data-stu-id="0766c-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="0766c-125">Эта инструкция выполняет следующие вычисления.</span><span class="sxs-lookup"><span data-stu-id="0766c-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="0766c-126">Правила использования Бем:</span><span class="sxs-lookup"><span data-stu-id="0766c-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="0766c-127">Бем должен располагаться на первом этапе шейдера (то есть перед маркером этапа).</span><span class="sxs-lookup"><span data-stu-id="0766c-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="0766c-128">Бем использует два слота арифметических инструкций.</span><span class="sxs-lookup"><span data-stu-id="0766c-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="0766c-129">Для шейдера допускается только одно использование этой инструкции.</span><span class="sxs-lookup"><span data-stu-id="0766c-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="0766c-130">Целевой вритемаск должен быть. RG/.КСИ.</span><span class="sxs-lookup"><span data-stu-id="0766c-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="0766c-131">Эта инструкция не может быть выполнена совместно.</span><span class="sxs-lookup"><span data-stu-id="0766c-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="0766c-132">Кроме ограничения, маска записи назначения имеет значение. RG, модификаторы для исходных src0, src1 и модификаторы инструкций не ограничены.</span><span class="sxs-lookup"><span data-stu-id="0766c-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="0766c-133">Сведения о инструкции</span><span class="sxs-lookup"><span data-stu-id="0766c-133">Instruction Information</span></span>



| <span data-ttu-id="0766c-134">Требование</span><span class="sxs-lookup"><span data-stu-id="0766c-134">Requirement</span></span>                         | <span data-ttu-id="0766c-135">Значение</span><span class="sxs-lookup"><span data-stu-id="0766c-135">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="0766c-136">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="0766c-136">Minimum operating system</span></span> | <span data-ttu-id="0766c-137">Windows 98</span><span class="sxs-lookup"><span data-stu-id="0766c-137">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="0766c-138">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="0766c-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0766c-139">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="0766c-139">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




