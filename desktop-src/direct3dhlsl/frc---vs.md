---
title: ФРК — VS
description: Возвращает дробную часть каждого входного компонента. | ФРК — VS
ms.assetid: 6b6a4475-b665-4de0-9423-88ea8103e606
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6990d5489058d217888f34caf0305badc4cab46d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104353412"
---
# <a name="frc---vs"></a><span data-ttu-id="119af-104">ФРК — VS</span><span class="sxs-lookup"><span data-stu-id="119af-104">frc - vs</span></span>

<span data-ttu-id="119af-105">Возвращает дробную часть каждого входного компонента.</span><span class="sxs-lookup"><span data-stu-id="119af-105">Returns the fractional portion of each input component.</span></span>

## <a name="syntax"></a><span data-ttu-id="119af-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="119af-106">Syntax</span></span>



| <span data-ttu-id="119af-107">ФРК DST, src</span><span class="sxs-lookup"><span data-stu-id="119af-107">frc dst, src</span></span> |
|--------------|



 

<span data-ttu-id="119af-108">где</span><span class="sxs-lookup"><span data-stu-id="119af-108">where</span></span>

-   <span data-ttu-id="119af-109">DST — это регистр назначения.</span><span class="sxs-lookup"><span data-stu-id="119af-109">dst is the destination register.</span></span>
-   <span data-ttu-id="119af-110">src является исходным регистром.</span><span class="sxs-lookup"><span data-stu-id="119af-110">src is a source register.</span></span>

## <a name="remarks"></a><span data-ttu-id="119af-111">Примечания</span><span class="sxs-lookup"><span data-stu-id="119af-111">Remarks</span></span>



| <span data-ttu-id="119af-112">Версии шейдеров вершин</span><span class="sxs-lookup"><span data-stu-id="119af-112">Vertex shader versions</span></span> | <span data-ttu-id="119af-113">1\_1</span><span class="sxs-lookup"><span data-stu-id="119af-113">1\_1</span></span> | <span data-ttu-id="119af-114">2 \_ 0</span><span class="sxs-lookup"><span data-stu-id="119af-114">2\_0</span></span> | <span data-ttu-id="119af-115">2 \_ x</span><span class="sxs-lookup"><span data-stu-id="119af-115">2\_x</span></span> | <span data-ttu-id="119af-116">2 \_ SW</span><span class="sxs-lookup"><span data-stu-id="119af-116">2\_sw</span></span> | <span data-ttu-id="119af-117">3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="119af-117">3\_0</span></span> | <span data-ttu-id="119af-118">3 \_ SW</span><span class="sxs-lookup"><span data-stu-id="119af-118">3\_sw</span></span> |
|------------------------|------|------|------|-------|------|-------|
| <span data-ttu-id="119af-119">фрк</span><span class="sxs-lookup"><span data-stu-id="119af-119">frc</span></span>                    | <span data-ttu-id="119af-120">x</span><span class="sxs-lookup"><span data-stu-id="119af-120">x</span></span>    | <span data-ttu-id="119af-121">x</span><span class="sxs-lookup"><span data-stu-id="119af-121">x</span></span>    | <span data-ttu-id="119af-122">x</span><span class="sxs-lookup"><span data-stu-id="119af-122">x</span></span>    | <span data-ttu-id="119af-123">x</span><span class="sxs-lookup"><span data-stu-id="119af-123">x</span></span>     | <span data-ttu-id="119af-124">x</span><span class="sxs-lookup"><span data-stu-id="119af-124">x</span></span>    | <span data-ttu-id="119af-125">x</span><span class="sxs-lookup"><span data-stu-id="119af-125">x</span></span>     |



 

<span data-ttu-id="119af-126">В следующем фрагменте кода показано, как работает инструкция.</span><span class="sxs-lookup"><span data-stu-id="119af-126">The following code fragment shows conceptually how the instruction operates.</span></span>


```
dest.x = src.x - (float)floor(src.x);
dest.y = src.y - (float)floor(src.y);
dest.z = src.z - (float)floor(src.z);
dest.w = src.w - (float)floor(src.w);
```



<span data-ttu-id="119af-127">Функция Floor Преобразует аргумент, переданный в, в наибольшее целое число, которое меньше (или равно) аргументу.</span><span class="sxs-lookup"><span data-stu-id="119af-127">The floor function converts the argument passed in to the greatest integer that is less than (or equal to) the argument.</span></span> <span data-ttu-id="119af-128">Это преобразование преобразуется в тип float, а затем вычитается ФОМ исходное значение.</span><span class="sxs-lookup"><span data-stu-id="119af-128">This is converted to a float and then subtracted fom the original value.</span></span> <span data-ttu-id="119af-129">Результирующие дробные значения в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="119af-129">The resulting fractional value ranges from 0.0 through 1.0.</span></span>

<span data-ttu-id="119af-130">Для версии 1 \_ 1 допустимые маски записи:. y и. XY (. x не разрешены).</span><span class="sxs-lookup"><span data-stu-id="119af-130">For version 1\_1, the allowable write masks are .y and .xy (.x is not allowed).</span></span>

## <a name="related-topics"></a><span data-ttu-id="119af-131">См. также</span><span class="sxs-lookup"><span data-stu-id="119af-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="119af-132">Инструкции шейдера вершин</span><span class="sxs-lookup"><span data-stu-id="119af-132">Vertex Shader Instructions</span></span>](dx9-graphics-reference-asm-vs-instructions.md)
</dt> </dl>

 

 




