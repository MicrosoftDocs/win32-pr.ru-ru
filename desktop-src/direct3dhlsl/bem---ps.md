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
ms.openlocfilehash: 7c591555e2cbd2c6eaebf6e392bb94d6ec50e748
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104412201"
---
# <a name="bem---ps"></a><span data-ttu-id="f7e63-103">Бем-PS</span><span class="sxs-lookup"><span data-stu-id="f7e63-103">bem - ps</span></span>

<span data-ttu-id="f7e63-104">Примените фиктивное преобразование «среда выпуклости».</span><span class="sxs-lookup"><span data-stu-id="f7e63-104">Apply a fake bump environment-map transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="f7e63-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f7e63-105">Syntax</span></span>



| <span data-ttu-id="f7e63-106">Бем DST. RG, src0, src1</span><span class="sxs-lookup"><span data-stu-id="f7e63-106">bem dst.rg, src0, src1</span></span> |
|------------------------|



 

<span data-ttu-id="f7e63-107">где</span><span class="sxs-lookup"><span data-stu-id="f7e63-107">where</span></span>

-   <span data-ttu-id="f7e63-108">DST. RG DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="f7e63-108">dst.rg dst is the destination register.</span></span> <span data-ttu-id="f7e63-109">Необходимо использовать маску записи красного и зеленого компонентов.</span><span class="sxs-lookup"><span data-stu-id="f7e63-109">The red and green component write mask must be used.</span></span>
-   <span data-ttu-id="f7e63-110">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="f7e63-110">src0 is a source register.</span></span>
-   <span data-ttu-id="f7e63-111">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="f7e63-111">src1 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="f7e63-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="f7e63-112">Remarks</span></span>



| <span data-ttu-id="f7e63-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="f7e63-113">Pixel shader versions</span></span> | <span data-ttu-id="f7e63-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="f7e63-114">1\_1</span></span> | <span data-ttu-id="f7e63-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="f7e63-115">1\_2</span></span> | <span data-ttu-id="f7e63-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="f7e63-116">1\_3</span></span> | <span data-ttu-id="f7e63-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="f7e63-117">1\_4</span></span> | <span data-ttu-id="f7e63-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f7e63-118">2\_0</span></span> | <span data-ttu-id="f7e63-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="f7e63-119">2\_x</span></span> | <span data-ttu-id="f7e63-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f7e63-120">2\_sw</span></span> | <span data-ttu-id="f7e63-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="f7e63-121">3\_0</span></span> | <span data-ttu-id="f7e63-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="f7e63-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="f7e63-123">бем</span><span class="sxs-lookup"><span data-stu-id="f7e63-123">bem</span></span>                   |      |      |      | <span data-ttu-id="f7e63-124">x</span><span class="sxs-lookup"><span data-stu-id="f7e63-124">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="f7e63-125">Эта инструкция выполняет следующие вычисления.</span><span class="sxs-lookup"><span data-stu-id="f7e63-125">This instruction performs the following calculation.</span></span>


```
(Given n == dest register #)
dest.r = src0.r + D3DTSS_BUMPENVMAT00(stage n) * src1.r 
                + D3DTSS_BUMPENVMAT10(stage n) * src1.g

dest.g = src0.g + D3DTSS_BUMPENVMAT01(stage n) * src1.r
                + D3DTSS_BUMPENVMAT11(stage n) * src1.g
```



<span data-ttu-id="f7e63-126">Правила использования Бем:</span><span class="sxs-lookup"><span data-stu-id="f7e63-126">Rules for using bem:</span></span>

1.  <span data-ttu-id="f7e63-127">Бем должен располагаться на первом этапе шейдера (то есть перед маркером этапа).</span><span class="sxs-lookup"><span data-stu-id="f7e63-127">bem must appear in the first phase of a shader (that is, before a phase marker).</span></span>
2.  <span data-ttu-id="f7e63-128">Бем использует два слота арифметических инструкций.</span><span class="sxs-lookup"><span data-stu-id="f7e63-128">bem consumes two arithmetic instruction slots.</span></span>
3.  <span data-ttu-id="f7e63-129">Для шейдера допускается только одно использование этой инструкции.</span><span class="sxs-lookup"><span data-stu-id="f7e63-129">Only one use of this instruction is allowed per shader.</span></span>
4.  <span data-ttu-id="f7e63-130">Целевой вритемаск должен быть. RG/.КСИ.</span><span class="sxs-lookup"><span data-stu-id="f7e63-130">Destination writemask must be .rg /.xy.</span></span>
5.  <span data-ttu-id="f7e63-131">Эта инструкция не может быть выполнена совместно.</span><span class="sxs-lookup"><span data-stu-id="f7e63-131">This instruction cannot be co-issued.</span></span>
6.  <span data-ttu-id="f7e63-132">Кроме ограничения, маска записи назначения имеет значение. RG, модификаторы для исходных src0, src1 и модификаторы инструкций не ограничены.</span><span class="sxs-lookup"><span data-stu-id="f7e63-132">Aside from the restriction that destination write mask be .rg, modifiers on source src0, src1, and instruction modifiers are unconstrained.</span></span>

## <a name="instruction-information"></a><span data-ttu-id="f7e63-133">Сведения о инструкции</span><span class="sxs-lookup"><span data-stu-id="f7e63-133">Instruction Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="f7e63-134">Минимальная операционная система</span><span class="sxs-lookup"><span data-stu-id="f7e63-134">Minimum operating system</span></span> | <span data-ttu-id="f7e63-135">Windows 98</span><span class="sxs-lookup"><span data-stu-id="f7e63-135">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="f7e63-136">См. также</span><span class="sxs-lookup"><span data-stu-id="f7e63-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7e63-137">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="f7e63-137">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




