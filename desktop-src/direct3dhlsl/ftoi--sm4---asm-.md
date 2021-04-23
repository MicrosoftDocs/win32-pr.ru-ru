---
title: 'ftoi (sm4 — asm) '
description: Преобразование с плавающей запятой в целое число со знаком.
ms.assetid: 580AB4A6-0C1C-409B-B2B9-BA1D37772F46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c02ce1b506d112a59d3087f59d219557575b8def
ms.sourcegitcommit: 8c658e9872a2173e3dcec94195f9067fbcd85d3d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/17/2020
ms.locfileid: "104339521"
---
# <a name="ftoi-sm4---asm"></a><span data-ttu-id="74f38-103">ftoi (sm4 — asm) </span><span class="sxs-lookup"><span data-stu-id="74f38-103">ftoi (sm4 - asm)</span></span>

<span data-ttu-id="74f38-104">Преобразование с плавающей запятой в целое число со знаком.</span><span class="sxs-lookup"><span data-stu-id="74f38-104">Floating point to signed integer conversion.</span></span>

| <span data-ttu-id="74f38-105">фтои dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . свиззле\]</span><span class="sxs-lookup"><span data-stu-id="74f38-105">ftoi dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-|

| <span data-ttu-id="74f38-106">Элемент</span><span class="sxs-lookup"><span data-stu-id="74f38-106">Item</span></span> | <span data-ttu-id="74f38-107">Описание</span><span class="sxs-lookup"><span data-stu-id="74f38-107">Description</span></span> |
|-|-|
| <span data-ttu-id="74f38-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="74f38-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="74f38-109">\[в \] адресе результата операции.</span><span class="sxs-lookup"><span data-stu-id="74f38-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="74f38-110">*конечный адрес*  =  [Round \_ z](round-z--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="74f38-110">*dest* = [round\_z](round-z--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="74f38-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="74f38-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="74f38-112">\[в \] преобразуемом компоненте.</span><span class="sxs-lookup"><span data-stu-id="74f38-112">\[in\] The component to convert.</span></span><br/> |

## <a name="remarks"></a><span data-ttu-id="74f38-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="74f38-113">Remarks</span></span>

<span data-ttu-id="74f38-114">Преобразование выполняется для каждого компонента.</span><span class="sxs-lookup"><span data-stu-id="74f38-114">The conversion is performed per component.</span></span> <span data-ttu-id="74f38-115">Округление всегда выполняется в сторону нуля, в соответствии с соглашением C для приведения типа float к типу int. Приложения, для которых требуется другая семантика округления, могут вызывать **округленные** инструкции перед приведением к целому числу.</span><span class="sxs-lookup"><span data-stu-id="74f38-115">Rounding is always performed towards zero, following the C convention for casts from float to int. Applications that require different rounding semantics can invoke the **round** instructions before casting to integer.</span></span>

<span data-ttu-id="74f38-116">Входные данные записываются в диапазон \[ 2147483648.999 f... 2147483647.999 f \] перед преобразованием, а входные значения NaN дают нулевой результат.</span><span class="sxs-lookup"><span data-stu-id="74f38-116">Inputs are clamped to the range \[-2147483648.999f ... 2147483647.999f\] prior to conversion, and input NaN values produce a zero result.</span></span>

<span data-ttu-id="74f38-117">Необязательные модификаторы отрицания и абсолютные значения применяются к исходным значениям перед преобразованием.</span><span class="sxs-lookup"><span data-stu-id="74f38-117">Optional negate and absolute value modifiers are applied to the source values before conversion.</span></span>

<span data-ttu-id="74f38-118">Эта инструкция применяется к следующим этапам шейдера:</span><span class="sxs-lookup"><span data-stu-id="74f38-118">This instruction applies to the following shader stages:</span></span>

| <span data-ttu-id="74f38-119">Вершинный построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="74f38-119">Vertex Shader</span></span> | <span data-ttu-id="74f38-120">Шейдер геометрии</span><span class="sxs-lookup"><span data-stu-id="74f38-120">Geometry Shader</span></span> | <span data-ttu-id="74f38-121">Построитель текстуры</span><span class="sxs-lookup"><span data-stu-id="74f38-121">Pixel Shader</span></span> |
|-|-|-|
| <span data-ttu-id="74f38-122">x</span><span class="sxs-lookup"><span data-stu-id="74f38-122">x</span></span> | <span data-ttu-id="74f38-123">x</span><span class="sxs-lookup"><span data-stu-id="74f38-123">x</span></span> | <span data-ttu-id="74f38-124">x</span><span class="sxs-lookup"><span data-stu-id="74f38-124">x</span></span> |

## <a name="minimum-shader-model"></a><span data-ttu-id="74f38-125">Минимальная модель шейдера</span><span class="sxs-lookup"><span data-stu-id="74f38-125">Minimum Shader Model</span></span>

<span data-ttu-id="74f38-126">Эта функция поддерживается в следующих моделях шейдеров.</span><span class="sxs-lookup"><span data-stu-id="74f38-126">This function is supported in the following shader models.</span></span>

| <span data-ttu-id="74f38-127">Модель шейдера</span><span class="sxs-lookup"><span data-stu-id="74f38-127">Shader Model</span></span> | <span data-ttu-id="74f38-128">Поддерживается</span><span class="sxs-lookup"><span data-stu-id="74f38-128">Supported</span></span> |
|-|-|
| [<span data-ttu-id="74f38-129">Модель шейдера 5</span><span class="sxs-lookup"><span data-stu-id="74f38-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md) | <span data-ttu-id="74f38-130">да</span><span class="sxs-lookup"><span data-stu-id="74f38-130">yes</span></span> |
| [<span data-ttu-id="74f38-131">Модель шейдера 4,1</span><span class="sxs-lookup"><span data-stu-id="74f38-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="74f38-132">да</span><span class="sxs-lookup"><span data-stu-id="74f38-132">yes</span></span> |
| [<span data-ttu-id="74f38-133">Модель шейдера 4</span><span class="sxs-lookup"><span data-stu-id="74f38-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md) | <span data-ttu-id="74f38-134">да</span><span class="sxs-lookup"><span data-stu-id="74f38-134">yes</span></span> |
| [<span data-ttu-id="74f38-135">Модель шейдера 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74f38-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="74f38-136">Нет</span><span class="sxs-lookup"><span data-stu-id="74f38-136">no</span></span> |
| [<span data-ttu-id="74f38-137">Модель шейдера 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74f38-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="74f38-138">Нет</span><span class="sxs-lookup"><span data-stu-id="74f38-138">no</span></span> |
| [<span data-ttu-id="74f38-139">Модель шейдера 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74f38-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="74f38-140">Нет</span><span class="sxs-lookup"><span data-stu-id="74f38-140">no</span></span> |

## <a name="related-topics"></a><span data-ttu-id="74f38-141">См. также</span><span class="sxs-lookup"><span data-stu-id="74f38-141">Related topics</span></span>

[<span data-ttu-id="74f38-142">Сборка Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="74f38-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
