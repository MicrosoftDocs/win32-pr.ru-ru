---
title: освещенность — VS
description: Обеспечивает частичную поддержку освещения путем вычисления коэффициентов освещения из двух изделий с точками и экспоненты.
ms.assetid: e0ed1a75-6682-4d05-b0e5-dc65e201de98
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 99c25c377ff6064a704d56b9e7b31d41b37117e5
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/20/2019
ms.locfileid: "104983857"
---
# <a name="lit---vs"></a><span data-ttu-id="acf37-103">освещенность — VS</span><span class="sxs-lookup"><span data-stu-id="acf37-103">lit - vs</span></span>

<span data-ttu-id="acf37-104">Обеспечивает частичную поддержку освещения путем вычисления коэффициентов освещения из двух изделий с точками и экспоненты.</span><span class="sxs-lookup"><span data-stu-id="acf37-104">Provides partial support for lighting by calculating lighting coefficients from two dot products and an exponent.</span></span>

## <a name="syntax"></a><span data-ttu-id="acf37-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="acf37-105">Syntax</span></span>



| <span data-ttu-id="acf37-106">освещенный DST, src</span><span class="sxs-lookup"><span data-stu-id="acf37-106">lit dst, src</span></span> |
|--------------|



 

<span data-ttu-id="acf37-107">где</span><span class="sxs-lookup"><span data-stu-id="acf37-107">where</span></span>

-   <span data-ttu-id="acf37-108">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="acf37-108">dst is the destination register.</span></span>
-   <span data-ttu-id="acf37-109">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="acf37-109">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="acf37-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="acf37-110">Remarks</span></span>



| <span data-ttu-id="acf37-111">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="acf37-111">Vertex shader versions</span></span> | <span data-ttu-id="acf37-112">1\_1</span><span class="sxs-lookup"><span data-stu-id="acf37-112">1\_1</span></span> | <span data-ttu-id="acf37-113">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="acf37-113">2\_0</span></span> | <span data-ttu-id="acf37-114">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="acf37-114">2\_x</span></span> | <span data-ttu-id="acf37-115">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="acf37-115">2\_sw</span></span> | <span data-ttu-id="acf37-116">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="acf37-116">3\_0</span></span> | <span data-ttu-id="acf37-117">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="acf37-117">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="acf37-118">индикатор</span><span class="sxs-lookup"><span data-stu-id="acf37-118">lit</span></span>                    | <span data-ttu-id="acf37-119">x</span><span class="sxs-lookup"><span data-stu-id="acf37-119">x</span></span>    | <span data-ttu-id="acf37-120">x</span><span class="sxs-lookup"><span data-stu-id="acf37-120">x</span></span>    | <span data-ttu-id="acf37-121">x</span><span class="sxs-lookup"><span data-stu-id="acf37-121">x</span></span>    | <span data-ttu-id="acf37-122">x</span><span class="sxs-lookup"><span data-stu-id="acf37-122">x</span></span>     | <span data-ttu-id="acf37-123">x</span><span class="sxs-lookup"><span data-stu-id="acf37-123">x</span></span>    | <span data-ttu-id="acf37-124">x</span><span class="sxs-lookup"><span data-stu-id="acf37-124">x</span></span>     |



 

<span data-ttu-id="acf37-125">Предполагается, что исходный вектор содержит значения, показанные в следующем псевдокоде.</span><span class="sxs-lookup"><span data-stu-id="acf37-125">The source vector is assumed to contain the values shown in the following pseudocode.</span></span>


```
src.x = N*L        ; The dot product between normal and direction to light
src.y = N*H        ; The dot product between normal and half vector
src.z = ignored    ; This value is ignored
src.w = exponent   ; The value must be between -128.0 and 128.0
```



<span data-ttu-id="acf37-126">В следующем фрагменте кода показаны выполняемые операции.</span><span class="sxs-lookup"><span data-stu-id="acf37-126">The following code fragment shows the operations performed.</span></span>


```
dest.x = 1;
dest.y = 0;
dest.z = 0;
dest.w = 1;

float power = src.w;
const float MAXPOWER = 127.9961f;
if (power < -MAXPOWER)
    power = -MAXPOWER;          // Fits into 8.8 fixed point format
else if (power > MAXPOWER)
    power = MAXPOWER;          // Fits into 8.8 fixed point format

if (src.x > 0)
{
    dest.y = src.x;
    if (src.y > 0)
    {
        // Allowed approximation is EXP(power * LOG(src.y))
        dest.z = (float)(pow(src.y, power));
    }
}
```



<span data-ttu-id="acf37-127">Арифметическая точность с ограниченной точностью приемлема при оценке целевого компонента y (dest. y).</span><span class="sxs-lookup"><span data-stu-id="acf37-127">Reduced precision arithmetic is acceptable in evaluating the destination y component (dest.y).</span></span> <span data-ttu-id="acf37-128">Реализация должна поддерживать по крайней мере восемь дробных разрядов в аргументе питания.</span><span class="sxs-lookup"><span data-stu-id="acf37-128">An implementation must support at least eight fraction bits in the power argument.</span></span> <span data-ttu-id="acf37-129">Продукты с точками вычисляются с помощью нормализованных векторов, а пределы для срезов — от-128 до 128.</span><span class="sxs-lookup"><span data-stu-id="acf37-129">Dot products are calculated with normalized vectors, and clamp limits are -128 to 128.</span></span>

<span data-ttu-id="acf37-130">Ошибка должна соответствовать сочетанию [логп-VS](logp---vs.md) и [exp-VS](exp---vs.md) или не более приблизительно одного значащих бит для 8-разрядного компонента цвета.</span><span class="sxs-lookup"><span data-stu-id="acf37-130">Error should correspond to a [logp - vs](logp---vs.md) and [exp - vs](exp---vs.md) combination, or no more than approximately one significant bit for an 8-bit color component.</span></span>

## <a name="related-topics"></a><span data-ttu-id="acf37-131">См. также</span><span class="sxs-lookup"><span data-stu-id="acf37-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="acf37-132">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="acf37-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




