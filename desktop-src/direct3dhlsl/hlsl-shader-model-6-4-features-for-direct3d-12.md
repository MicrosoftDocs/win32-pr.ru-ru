---
title: Модель шейдера HLSL 6,4
description: Описывает встроенные функции машинного обучения, добавленные в модель шейдера HLSL 6,4.
ms.topic: article
ms.date: 02/21/2019
ms.openlocfilehash: 10e74b268243ab059c2d0945887a6d429d40bb53
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/05/2021
ms.locfileid: "103914263"
---
# <a name="hlsl-shader-model-64"></a><span data-ttu-id="326b6-103">Модель шейдера HLSL 6,4</span><span class="sxs-lookup"><span data-stu-id="326b6-103">HLSL Shader Model 6.4</span></span>

<span data-ttu-id="326b6-104">Описывает встроенные функции машинного обучения, добавленные в модель шейдера HLSL 6,4.</span><span class="sxs-lookup"><span data-stu-id="326b6-104">Describes the machine learning intrinsics added to HLSL Shader Model 6.4.</span></span>

## <a name="shader-model-64"></a><span data-ttu-id="326b6-105">Модель шейдера 6,4</span><span class="sxs-lookup"><span data-stu-id="326b6-105">Shader Model 6.4</span></span>
<span data-ttu-id="326b6-106">Эти встроенные функции являются обязательной и поддерживаемой функцией шейдера 6,4.</span><span class="sxs-lookup"><span data-stu-id="326b6-106">These intrinsics are a required/supported feature of Shader model 6.4.</span></span> <span data-ttu-id="326b6-107">Следовательно, отдельная проверка поразрядности функций не требуется, помимо того, чтобы гарантировать использование модели шейдера 6,4.</span><span class="sxs-lookup"><span data-stu-id="326b6-107">Consequently, no separate capability bit check is required, beyond assuring the use of Shader Model 6.4.</span></span> <span data-ttu-id="326b6-108">Минимальный поддерживаемый клиент для этих подпрограмм — Windows 10, версия 1903.</span><span class="sxs-lookup"><span data-stu-id="326b6-108">The minimum supported client for these routines is Windows 10, version 1903.</span></span>

## <a name="shading-language-intrinsics"></a><span data-ttu-id="326b6-109">Встроенные функции языка заливки</span><span class="sxs-lookup"><span data-stu-id="326b6-109">Shading language intrinsics</span></span>

### <a name="unsigned-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="326b6-110">Целое число без знака Dot-Product 4 элемента и накопление</span><span class="sxs-lookup"><span data-stu-id="326b6-110">Unsigned Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
uint32 dot4add_u8packed(uint32 a, uint32 b, uint32 acc); // ubyte4 a, b;
```
 
<span data-ttu-id="326b6-111">4-мерный целое число без знака, имеющее значение "точка — произведение" с добавлением.</span><span class="sxs-lookup"><span data-stu-id="326b6-111">A 4-dimensional unsigned integer dot-product with add.</span></span> <span data-ttu-id="326b6-112">Умножает каждую соответствующую пару 8-разрядных байтов int в два входных DWORD и суммирует результаты в 32-разрядное целое число без знака.</span><span class="sxs-lookup"><span data-stu-id="326b6-112">Multiplies together each corresponding pair of unsigned 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit unsigned integer accumulator.</span></span> <span data-ttu-id="326b6-113">Эта инструкция работает в пределах одной 32-разрядной глобальной полосы.</span><span class="sxs-lookup"><span data-stu-id="326b6-113">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="326b6-114">В качестве входных данных также предполагается 32-разрядное количество.</span><span class="sxs-lookup"><span data-stu-id="326b6-114">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="signed-integer-dot-product-of-4-elements-and-accumulate"></a><span data-ttu-id="326b6-115">Целое число со знаком Dot-Product 4 элемента и накопление</span><span class="sxs-lookup"><span data-stu-id="326b6-115">Signed Integer Dot-Product of 4 Elements and Accumulate</span></span>
```syntax
int32 dot4add_i8packed(uint32 a, uint32 b, int32 acc); // signed byte4 a, b;
```

<span data-ttu-id="326b6-116">4-мерный целое число со знаком — поточечное произведение с помощью Add.</span><span class="sxs-lookup"><span data-stu-id="326b6-116">A 4-dimensional signed integer dot-product with add.</span></span> <span data-ttu-id="326b6-117">Умножает каждую соответствующую пару из 8-разрядных байтов int в два входных DWORD и суммирует результаты по 32-разрядному целому числу со знаком.</span><span class="sxs-lookup"><span data-stu-id="326b6-117">Multiplies together each corresponding pair of signed 8-bit int bytes in the two input DWORDs, and sums the results into the 32-bit signed integer accumulator.</span></span> <span data-ttu-id="326b6-118">Эта инструкция работает в пределах одной 32-разрядной глобальной полосы.</span><span class="sxs-lookup"><span data-stu-id="326b6-118">This instruction operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="326b6-119">В качестве входных данных также предполагается 32-разрядное количество.</span><span class="sxs-lookup"><span data-stu-id="326b6-119">The inputs are also assumed to be 32-bit quantities.</span></span>
 
### <a name="single-precision-floating-point-2-element-dot-product-and-accumulate"></a><span data-ttu-id="326b6-120">Одинарная точность с плавающей запятой 2-element Dot-Product и accumulate</span><span class="sxs-lookup"><span data-stu-id="326b6-120">Single Precision Floating Point 2-Element Dot-Product and Accumulate</span></span>
```syntax
float dot2add( half2 a, half2 b, float acc );
```

<span data-ttu-id="326b6-121">Двухмерный half2 векторов с плавающей запятой с помощью Add.</span><span class="sxs-lookup"><span data-stu-id="326b6-121">A 2-dimensional floating point dot-product of half2 vectors with add.</span></span> <span data-ttu-id="326b6-122">Умножает элементы двух входных векторов с половинной точностью и суммирует результаты в 32-разрядном агрегате с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="326b6-122">Multiplies the elements of the two half-precision float input vectors together and sums the results into the 32-bit float accumulator.</span></span> <span data-ttu-id="326b6-123">Эти инструкции работают в пределах одной 32-битной глобальной полосы.</span><span class="sxs-lookup"><span data-stu-id="326b6-123">This instructions operates within a single 32-bit wide SIMD lane.</span></span> <span data-ttu-id="326b6-124">Входные данные представляют собой 16-битные количества, Упакованные в одну и ту же полосу.</span><span class="sxs-lookup"><span data-stu-id="326b6-124">The inputs are 16-bit quantities packed into the same lane.</span></span>

<span data-ttu-id="326b6-125">Это рассматривается с помощью битовой функции с наименьшей точностью (это означает, что имеется собственная половина и небольшая поддержка).</span><span class="sxs-lookup"><span data-stu-id="326b6-125">This is covered under the low-precision feature bit (indicating that native half and short support are present).</span></span>

### <a name="sv_shadingrate"></a><span data-ttu-id="326b6-126">SV_ShadingRate</span><span class="sxs-lookup"><span data-stu-id="326b6-126">SV_ShadingRate</span></span>
```syntax
uint shadingRate : SV_ShadingRate
```

<span data-ttu-id="326b6-127">Целое число без знака, представляющее количество целевых пикселей, записываемых при каждом вызове шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="326b6-127">An unsigned integer representing how many target pixels are written by each invocation of the pixel shader.</span></span> <span data-ttu-id="326b6-128">Допустимые значения принадлежат к набору значений перечисления [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).</span><span class="sxs-lookup"><span data-stu-id="326b6-128">Valid values belong to set of enumeration values [D3D12_SHADING_RATE](/windows/win32/api/d3d12/ne-d3d12-d3d12_shading_rate).</span></span>

<span data-ttu-id="326b6-129">Это системное значение доступно на платформах, которые имеют [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="326b6-129">This system value is available on platforms that are [D3D12_VARIABLE_SHADING_RATE_TIER_2](/windows/win32/api/d3d12/ne-d3d12-d3d12_variable_shading_rate_tier) or higher.</span></span> <span data-ttu-id="326b6-130">Его можно записать не более чем на одном из стадий шейдера вершин или геометрии.</span><span class="sxs-lookup"><span data-stu-id="326b6-130">It can be written from at most one of vertex or geometry shader stages.</span></span> <span data-ttu-id="326b6-131">Его можно прочитать на этапе шейдера пикселей.</span><span class="sxs-lookup"><span data-stu-id="326b6-131">It can be read from the pixel shader stage.</span></span> <span data-ttu-id="326b6-132">Дополнительные сведения см. в разделе [Заливка переменной скорости](../direct3d12/vrs.md).</span><span class="sxs-lookup"><span data-stu-id="326b6-132">For more information, see the [Variable-rate Shading](../direct3d12/vrs.md).</span></span>