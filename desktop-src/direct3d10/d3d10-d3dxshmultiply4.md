---
description: Выполняет вычисление произведения двух сферовых гармонических функций (f и g). Обе функции имеют порядок N = 4.
ms.assetid: 05427a18-447e-45d7-a851-e580298c9a1f
title: Функция D3DXSHMultiply4 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply4
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 13e8b62674ccbabbb03259f06b79f330424ddf84
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273885"
---
# <a name="d3dxshmultiply4-function"></a><span data-ttu-id="06233-104">Функция D3DXSHMultiply4</span><span class="sxs-lookup"><span data-stu-id="06233-104">D3DXSHMultiply4 function</span></span>

<span data-ttu-id="06233-105">Выполняет вычисление произведения двух сферовых гармонических функций (*f* и *g*).</span><span class="sxs-lookup"><span data-stu-id="06233-105">Computes the product of two spherical harmonics functions (*f* and *g*).</span></span> <span data-ttu-id="06233-106">Обе функции имеют порядок N = 4.</span><span class="sxs-lookup"><span data-stu-id="06233-106">Both functions are of order N = 4.</span></span>

## <a name="syntax"></a><span data-ttu-id="06233-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="06233-107">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply4(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="06233-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="06233-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06233-109">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="06233-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06233-110">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="06233-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="06233-111">Указатель на выходные коэффициенты SH: базисная функция *Y* LM хранится в l ² + *m* + l.</span><span class="sxs-lookup"><span data-stu-id="06233-111">Pointer to the output SH coefficients — basis function *Y* ₗₘ is stored at l² + *m* + l.</span></span> <span data-ttu-id="06233-112">Порядок *n* определяет длину массива, где всегда должно быть коэффициентов *n*².</span><span class="sxs-lookup"><span data-stu-id="06233-112">The order *N* determines the length of the array, where there should always be *N*² coefficients.</span></span>

</dd> <dt>

<span data-ttu-id="06233-113">*Общая папка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="06233-113">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06233-114">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="06233-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="06233-115">Входные коэффициенты SH для первой функции.</span><span class="sxs-lookup"><span data-stu-id="06233-115">Input SH coefficients for first function.</span></span>

</dd> <dt>

<span data-ttu-id="06233-116">*PG* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="06233-116">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="06233-117">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="06233-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="06233-118">Второй набор коэффициентов входных данных SH.</span><span class="sxs-lookup"><span data-stu-id="06233-118">Second set of input SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="06233-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="06233-119">Return value</span></span>

<span data-ttu-id="06233-120">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="06233-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="06233-121">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="06233-121">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="06233-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="06233-122">Remarks</span></span>

<span data-ttu-id="06233-123">Произведение двух функций SH в заказе N = 4 создает функцию SH в заказе 2 × *N* -1 = 7, но результаты усекаются.</span><span class="sxs-lookup"><span data-stu-id="06233-123">The product of two SH functions of order N = 4 generates an SH function of order 2 × *N* - 1 = 7, but the results are truncated.</span></span> <span data-ttu-id="06233-124">Это означает, что продукт работает ( *f* × *g*  =  *g* x *f* ), но не связан ( *f* × ( *g* x *h* ) ≠ ( *f* × *g* ) × *h* ).</span><span class="sxs-lookup"><span data-stu-id="06233-124">This means that the product commutes ( *f* × *g* = *g* × *f* ) but doesn't associate ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span></span>

<span data-ttu-id="06233-125">Эта функция использует следующее уравнение:</span><span class="sxs-lookup"><span data-stu-id="06233-125">This function uses the following equation:</span></span>


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



<span data-ttu-id="06233-126">где y \_ i (s) — это функция-i sh, где f (s) и g (s) используют следующую функцию SH:</span><span class="sxs-lookup"><span data-stu-id="06233-126">where y\_i(s) is the ith SH basis function, and where f(s) and g(s) use the following SH function:</span></span>


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a><span data-ttu-id="06233-127">Требования</span><span class="sxs-lookup"><span data-stu-id="06233-127">Requirements</span></span>



| <span data-ttu-id="06233-128">Требование</span><span class="sxs-lookup"><span data-stu-id="06233-128">Requirement</span></span> | <span data-ttu-id="06233-129">Значение</span><span class="sxs-lookup"><span data-stu-id="06233-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="06233-130">Header</span><span class="sxs-lookup"><span data-stu-id="06233-130">Header</span></span><br/>  | <dl> <span data-ttu-id="06233-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="06233-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="06233-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="06233-132">Library</span></span><br/> | <dl> <span data-ttu-id="06233-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="06233-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="06233-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06233-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06233-135">Математические функции</span><span class="sxs-lookup"><span data-stu-id="06233-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
