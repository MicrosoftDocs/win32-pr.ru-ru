---
title: КНД-PS
description: Условно выбирает между src1 и src2 на основе сравнения src0 0,5.
ms.assetid: 7a3b49e9-d146-47dc-99a8-4f336db7d0d5
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 1fd3a14e2ac4bd283a4e67724fbb42ac965ea707
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104133314"
---
# <a name="cnd---ps"></a><span data-ttu-id="c0c5a-103">КНД-PS</span><span class="sxs-lookup"><span data-stu-id="c0c5a-103">cnd - ps</span></span>

<span data-ttu-id="c0c5a-104">Условно выбирает между src1 и src2 на основе сравнения src0 > 0,5.</span><span class="sxs-lookup"><span data-stu-id="c0c5a-104">Conditionally chooses between src1 and src2, based on the comparison src0 > 0.5.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0c5a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="c0c5a-105">Syntax</span></span>



| <span data-ttu-id="c0c5a-106">КНД DST, src0, src1, src2</span><span class="sxs-lookup"><span data-stu-id="c0c5a-106">cnd dst, src0, src1, src2</span></span> |
|---------------------------|



 

<span data-ttu-id="c0c5a-107">где</span><span class="sxs-lookup"><span data-stu-id="c0c5a-107">where</span></span>

-   <span data-ttu-id="c0c5a-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="c0c5a-108">dst is the destination register.</span></span>
-   <span data-ttu-id="c0c5a-109">src0 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="c0c5a-109">src0 is a source register.</span></span>
-   <span data-ttu-id="c0c5a-110">src1 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="c0c5a-110">src1 is a source register.</span></span>
-   <span data-ttu-id="c0c5a-111">src2 является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="c0c5a-111">src2 is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0c5a-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="c0c5a-112">Remarks</span></span>



| <span data-ttu-id="c0c5a-113">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="c0c5a-113">Pixel shader versions</span></span> | <span data-ttu-id="c0c5a-114">1\_1</span><span class="sxs-lookup"><span data-stu-id="c0c5a-114">1\_1</span></span> | <span data-ttu-id="c0c5a-115">1\_2</span><span class="sxs-lookup"><span data-stu-id="c0c5a-115">1\_2</span></span> | <span data-ttu-id="c0c5a-116">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="c0c5a-116">1\_3</span></span> | <span data-ttu-id="c0c5a-117">1\_4</span><span class="sxs-lookup"><span data-stu-id="c0c5a-117">1\_4</span></span> | <span data-ttu-id="c0c5a-118">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c0c5a-118">2\_0</span></span> | <span data-ttu-id="c0c5a-119">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="c0c5a-119">2\_x</span></span> | <span data-ttu-id="c0c5a-120">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c0c5a-120">2\_sw</span></span> | <span data-ttu-id="c0c5a-121">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="c0c5a-121">3\_0</span></span> | <span data-ttu-id="c0c5a-122">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="c0c5a-122">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="c0c5a-123">кнд</span><span class="sxs-lookup"><span data-stu-id="c0c5a-123">cnd</span></span>                   | <span data-ttu-id="c0c5a-124">x</span><span class="sxs-lookup"><span data-stu-id="c0c5a-124">x</span></span>    | <span data-ttu-id="c0c5a-125">x</span><span class="sxs-lookup"><span data-stu-id="c0c5a-125">x</span></span>    | <span data-ttu-id="c0c5a-126">x</span><span class="sxs-lookup"><span data-stu-id="c0c5a-126">x</span></span>    | <span data-ttu-id="c0c5a-127">x</span><span class="sxs-lookup"><span data-stu-id="c0c5a-127">x</span></span>    |      |      |       |      |       |



 

<span data-ttu-id="c0c5a-128">Для версий 1 \_ 1 – 1 \_ 3 src0 должен быть R0. a.</span><span class="sxs-lookup"><span data-stu-id="c0c5a-128">For versions 1\_1 to 1\_3, src0 must be r0.a.</span></span>


```
// Version 1_1 to 1_3
if (r0.a > 0.5)
  dest = src1
else
  dest = src2
```



<span data-ttu-id="c0c5a-129">В версии 1 \_ 4 каждый канал сравнивается отдельно.</span><span class="sxs-lookup"><span data-stu-id="c0c5a-129">Version 1\_4 compares each channel separately.</span></span>


```
for each component in src0
{
   if (src0.component > 0.5)
     dest.component = src1.component
   else
     dest.component = src2.component
}
```



<span data-ttu-id="c0c5a-130">В этих примерах показано сравнение четырех каналов, выполненное в \_ шейдере версии 1 4, а также одноканальное сравнение, возможное в \_ шейдере версии 1 1.</span><span class="sxs-lookup"><span data-stu-id="c0c5a-130">These examples show a four-channel comparison done in a version 1\_4 shader, as well as a single-channel comparison possible in a version 1\_1 shader.</span></span>


```
ps_1_4
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1

cnd r1, c0, c1, c2   // r0 contains 1,1,1,0 because
// r1.x = c2.x because c0.x <= 0.5
// r1.y = c2.y because c0.y <= 0.5
// r1.z = c2.z because c0.z <= 0.5
// r1.w = c1.w because c0.w >  0.5
```



<span data-ttu-id="c0c5a-131">Версия 1 \_ с 1 до 1 \_ 3 сравнивается только с реплицируемым альфа-каналом R0.</span><span class="sxs-lookup"><span data-stu-id="c0c5a-131">Version 1\_1 to 1\_3 compares against the replicated alpha channel of r0 only.</span></span>


```
ps_1_1
def c0, -0.5, 0.5, 0, 0.6
def c1,  0,0,0,0
def c2,  1,1,1,1
mov r0, c0
cnd r1, r0.a, c1, c2   // r1 gets assigned 0,0,0,0 because 
                       // r0.a > 0.5, therefore r1.xyzw = c1.xyzw
```



<span data-ttu-id="c0c5a-132">В этом примере сравниваются два значения: A и B. В примере предполагается, что объект загружен в v0 и B загружен в v1.</span><span class="sxs-lookup"><span data-stu-id="c0c5a-132">This example compares two values, A and B. The example assumes A is loaded into v0 and B is loaded into v1.</span></span> <span data-ttu-id="c0c5a-133">Значения A и B должны находиться в диапазоне от-1 до + 1, а поскольку регистры цвета (VN) определены в диапазоне от 0 до 1, в этом примере это ограничение будет удовлетворено.</span><span class="sxs-lookup"><span data-stu-id="c0c5a-133">Both A and B must be in the range of -1 to +1, and since the color registers (vₙ) are defined to be between 0 and 1, the restriction happens to be satisfied in this example.</span></span>


```
ps_1_1                // Version instruction
sub r0, v0, v1_bias   // r0 = A - (B - 0.5)
cnd r0, r0.a, c0, c1  // r0 = ( A > B ? c0 : c1 )

// r0 = c0 if A > B, otherwise, r0 = c1
```



## <a name="related-topics"></a><span data-ttu-id="c0c5a-134">См. также</span><span class="sxs-lookup"><span data-stu-id="c0c5a-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c0c5a-135">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="c0c5a-135">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




