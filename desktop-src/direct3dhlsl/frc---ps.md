---
title: ФРК-PS
description: Возвращает дробную часть каждого входного компонента. | ФРК-PS
ms.assetid: 378bc516-c81e-4538-8d6f-987536b19467
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a16dd518333efa1dce878c1418547bc0527d1d64
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353415"
---
# <a name="frc---ps"></a><span data-ttu-id="5fdeb-104">ФРК-PS</span><span class="sxs-lookup"><span data-stu-id="5fdeb-104">frc - ps</span></span>

<span data-ttu-id="5fdeb-105">Возвращает дробную часть каждого входного компонента.</span><span class="sxs-lookup"><span data-stu-id="5fdeb-105">Returns the fractional portion of each input component.</span></span>

## <a name="syntax"></a><span data-ttu-id="5fdeb-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5fdeb-106">Syntax</span></span>



| <span data-ttu-id="5fdeb-107">ФРК DST, src</span><span class="sxs-lookup"><span data-stu-id="5fdeb-107">frc dst, src</span></span> |
|--------------|



 

<span data-ttu-id="5fdeb-108">где</span><span class="sxs-lookup"><span data-stu-id="5fdeb-108">where</span></span>

-   <span data-ttu-id="5fdeb-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="5fdeb-109">dst is the destination register.</span></span>
-   <span data-ttu-id="5fdeb-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="5fdeb-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fdeb-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="5fdeb-111">Remarks</span></span>



| <span data-ttu-id="5fdeb-112">Версии шейдеров пикселей</span><span class="sxs-lookup"><span data-stu-id="5fdeb-112">Pixel shader versions</span></span> | <span data-ttu-id="5fdeb-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="5fdeb-113">1\_1</span></span> | <span data-ttu-id="5fdeb-114">1\_2</span><span class="sxs-lookup"><span data-stu-id="5fdeb-114">1\_2</span></span> | <span data-ttu-id="5fdeb-115">1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="5fdeb-115">1\_3</span></span> | <span data-ttu-id="5fdeb-116">1\_4</span><span class="sxs-lookup"><span data-stu-id="5fdeb-116">1\_4</span></span> | <span data-ttu-id="5fdeb-117">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5fdeb-117">2\_0</span></span> | <span data-ttu-id="5fdeb-118">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="5fdeb-118">2\_x</span></span> | <span data-ttu-id="5fdeb-119">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5fdeb-119">2\_sw</span></span> | <span data-ttu-id="5fdeb-120">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="5fdeb-120">3\_0</span></span> | <span data-ttu-id="5fdeb-121">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="5fdeb-121">3\_sw</span></span> |
|-----------------------|------|------|------|------|------|------|-------|------|-------|
| <span data-ttu-id="5fdeb-122">фрк</span><span class="sxs-lookup"><span data-stu-id="5fdeb-122">frc</span></span>                   |      |      |      |      | <span data-ttu-id="5fdeb-123">x</span><span class="sxs-lookup"><span data-stu-id="5fdeb-123">x</span></span>    | <span data-ttu-id="5fdeb-124">x</span><span class="sxs-lookup"><span data-stu-id="5fdeb-124">x</span></span>    | <span data-ttu-id="5fdeb-125">x</span><span class="sxs-lookup"><span data-stu-id="5fdeb-125">x</span></span>     | <span data-ttu-id="5fdeb-126">x</span><span class="sxs-lookup"><span data-stu-id="5fdeb-126">x</span></span>    | <span data-ttu-id="5fdeb-127">x</span><span class="sxs-lookup"><span data-stu-id="5fdeb-127">x</span></span>     |



 

<span data-ttu-id="5fdeb-128">В следующем фрагменте кода показано, как работает инструкция.</span><span class="sxs-lookup"><span data-stu-id="5fdeb-128">The following code snippet shows conceptually how the instruction operates.</span></span>


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



<span data-ttu-id="5fdeb-129">Функция Floor Преобразует аргумент, переданный в, в наибольшее целое число, которое меньше (или равно) аргументу.</span><span class="sxs-lookup"><span data-stu-id="5fdeb-129">The floor function converts the argument passed in to the greatest integer that is less than (or equal to) the argument.</span></span> <span data-ttu-id="5fdeb-130">Это преобразование преобразуется в тип float, а затем вычитается ФОМ исходное значение.</span><span class="sxs-lookup"><span data-stu-id="5fdeb-130">This is converted to a float and then subtracted fom the original value.</span></span> <span data-ttu-id="5fdeb-131">Результирующие дробные значения в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="5fdeb-131">The resulting fractional value ranges from 0.0 through 1.0.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5fdeb-132">См. также</span><span class="sxs-lookup"><span data-stu-id="5fdeb-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5fdeb-133">Инструкции шейдера пикселей</span><span class="sxs-lookup"><span data-stu-id="5fdeb-133">Pixel Shader Instructions</span></span>](dx9-graphics-reference-asm-ps-instructions.md)
</dt> </dl>

 

 




