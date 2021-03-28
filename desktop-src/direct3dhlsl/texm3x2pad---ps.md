---
title: texm3x2pad-PS
description: Выполняет умножение первой строки на матрицу с двумя строками. Эту инструкцию необходимо сочетать с texm3x2tex-PS или texm3x2depth-PS. Дополнительные сведения об использовании тексмпад см. в любой из этих инструкций.
ms.assetid: 26eb3237-6e48-4880-b40d-37de8d65daa6
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 91d161d0b3cc7a90bbbfcee17774b1a587e4c04f
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "103890020"
---
# <a name="texm3x2pad---ps"></a><span data-ttu-id="fbe33-105">texm3x2pad-PS</span><span class="sxs-lookup"><span data-stu-id="fbe33-105">texm3x2pad - ps</span></span>

<span data-ttu-id="fbe33-106">Выполняет умножение первой строки на матрицу с двумя строками.</span><span class="sxs-lookup"><span data-stu-id="fbe33-106">Performs the first row multiplication of a two-row matrix multiply.</span></span> <span data-ttu-id="fbe33-107">Эту инструкцию необходимо сочетать с [texm3x2tex-PS](texm3x2tex---ps.md) или [texm3x2depth-PS](texm3x2depth---ps.md).</span><span class="sxs-lookup"><span data-stu-id="fbe33-107">This instruction must be combined with either [texm3x2tex - ps](texm3x2tex---ps.md) or [texm3x2depth - ps](texm3x2depth---ps.md).</span></span> <span data-ttu-id="fbe33-108">Дополнительные сведения об использовании тексмпад см. в любой из этих инструкций.</span><span class="sxs-lookup"><span data-stu-id="fbe33-108">Refer to either of these instructions for details on using texmpad.</span></span>

## <a name="syntax"></a><span data-ttu-id="fbe33-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fbe33-109">Syntax</span></span>



| <span data-ttu-id="fbe33-110">tex3x2pad DST, src</span><span class="sxs-lookup"><span data-stu-id="fbe33-110">tex3x2pad dst, src</span></span> |
|--------------------|



 

<span data-ttu-id="fbe33-111">где</span><span class="sxs-lookup"><span data-stu-id="fbe33-111">where</span></span>

-   <span data-ttu-id="fbe33-112">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="fbe33-112">dst is the destination register.</span></span>
-   <span data-ttu-id="fbe33-113">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="fbe33-113">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="fbe33-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="fbe33-114">Remarks</span></span>



| <span data-ttu-id="fbe33-115">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="fbe33-115">Pixel shader versions</span></span> | <span data-ttu-id="fbe33-116">1\_1</span><span class="sxs-lookup"><span data-stu-id="fbe33-116">1\_1</span></span> | <span data-ttu-id="fbe33-117">1\_2</span><span class="sxs-lookup"><span data-stu-id="fbe33-117">1\_2</span></span> | <span data-ttu-id="fbe33-118">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="fbe33-118">1\_3</span></span> | <span data-ttu-id="fbe33-119">1\_4</span><span class="sxs-lookup"><span data-stu-id="fbe33-119">1\_4</span></span> | <span data-ttu-id="fbe33-120">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fbe33-120">2\_0</span></span> | <span data-ttu-id="fbe33-121">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="fbe33-121">2\_x</span></span> | <span data-ttu-id="fbe33-122">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fbe33-122">2\_sw</span></span> | <span data-ttu-id="fbe33-123">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="fbe33-123">3\_0</span></span> | <span data-ttu-id="fbe33-124">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="fbe33-124">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="fbe33-125">texm3x2pad</span><span class="sxs-lookup"><span data-stu-id="fbe33-125">texm3x2pad</span></span>            | <span data-ttu-id="fbe33-126">x</span><span class="sxs-lookup"><span data-stu-id="fbe33-126">x</span></span>    | <span data-ttu-id="fbe33-127">x</span><span class="sxs-lookup"><span data-stu-id="fbe33-127">x</span></span>    | <span data-ttu-id="fbe33-128">x</span><span class="sxs-lookup"><span data-stu-id="fbe33-128">x</span></span>    |      |      |      |       |      |       |



 

<span data-ttu-id="fbe33-129">Эта инструкция не может использоваться сама по себе.</span><span class="sxs-lookup"><span data-stu-id="fbe33-129">This instruction cannot be used by itself.</span></span>

## <a name="related-topics"></a><span data-ttu-id="fbe33-130">См. также</span><span class="sxs-lookup"><span data-stu-id="fbe33-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fbe33-131">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="fbe33-131">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




