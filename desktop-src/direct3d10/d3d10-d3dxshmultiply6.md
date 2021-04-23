---
description: Выполняет вычисление произведения двух сферовых гармонических функций (f и g). Обе функции имеют порядок N = 6.
ms.assetid: 3b68b238-c1ae-4ab8-89ed-bdf815463143
title: Функция D3DXSHMultiply6 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply6
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0768bb8be1f2f23693a431a2c0ea8f3d5a6846d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647867"
---
# <a name="d3dxshmultiply6-function"></a><span data-ttu-id="56154-104">Функция D3DXSHMultiply6</span><span class="sxs-lookup"><span data-stu-id="56154-104">D3DXSHMultiply6 function</span></span>

<span data-ttu-id="56154-105">Выполняет вычисление произведения двух сферовых гармонических функций (f и g).</span><span class="sxs-lookup"><span data-stu-id="56154-105">Computes the product of two spherical harmonics functions (f and g).</span></span> <span data-ttu-id="56154-106">Обе функции имеют порядок N = 6.</span><span class="sxs-lookup"><span data-stu-id="56154-106">Both functions are of order N = 6.</span></span>

## <a name="syntax"></a><span data-ttu-id="56154-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="56154-107">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply6(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="56154-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="56154-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56154-109">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="56154-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56154-110">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="56154-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="56154-111">Указатель на выводимые коэффициенты SH — функция *Y* LM хранится в l ² + *m* + l.</span><span class="sxs-lookup"><span data-stu-id="56154-111">Pointer to the output SH coefficients — the basis function *Y* ₗₘ is stored at l² + *m* + l.</span></span> <span data-ttu-id="56154-112">Порядок *n* определяет длину массива, где всегда должно быть коэффициентов *n*².</span><span class="sxs-lookup"><span data-stu-id="56154-112">The order *N* determines the length of the array, where there should always be *N*² coefficients.</span></span>

</dd> <dt>

<span data-ttu-id="56154-113">*Общая папка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="56154-113">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56154-114">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="56154-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="56154-115">Входные коэффициенты SH для первой функции.</span><span class="sxs-lookup"><span data-stu-id="56154-115">Input SH coefficients for first function.</span></span>

</dd> <dt>

<span data-ttu-id="56154-116">*PG* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="56154-116">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56154-117">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="56154-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="56154-118">Второй набор коэффициентов входных данных SH.</span><span class="sxs-lookup"><span data-stu-id="56154-118">Second set of input SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56154-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56154-119">Return value</span></span>

<span data-ttu-id="56154-120">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="56154-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="56154-121">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="56154-121">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="56154-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="56154-122">Remarks</span></span>

<span data-ttu-id="56154-123">Произведение двух функций SH в заказе N = 6 создает функцию SH в заказе 2 × *N* -1 = 11, но результаты усекаются.</span><span class="sxs-lookup"><span data-stu-id="56154-123">The product of two SH functions of order N = 6 generates an SH function of order 2 × *N* - 1 = 11, but the results are truncated.</span></span> <span data-ttu-id="56154-124">Это означает, что продукт работает ( *f* × *g*  =  *g* x *f* ), но не связан ( *f* × ( *g* x *h* ) ≠ ( *f* × *g* ) × *h* ).</span><span class="sxs-lookup"><span data-stu-id="56154-124">This means that the product commutes ( *f* × *g* = *g* × *f* ) but doesn't associate ( *f* × ( *g* × *h* ) ≠ ( *f* × *g* ) × *h* ).</span></span>

<span data-ttu-id="56154-125">Эта функция использует следующее уравнение:</span><span class="sxs-lookup"><span data-stu-id="56154-125">This function uses the following equation:</span></span>


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



<span data-ttu-id="56154-126">где y \_ i (s) — это функция-i sh, где f (s) и g (s) используют следующую функцию SH:</span><span class="sxs-lookup"><span data-stu-id="56154-126">where y\_i(s) is the ith SH basis function, and where f(s) and g(s) use the following SH function:</span></span>


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a><span data-ttu-id="56154-127">Требования</span><span class="sxs-lookup"><span data-stu-id="56154-127">Requirements</span></span>



| <span data-ttu-id="56154-128">Требование</span><span class="sxs-lookup"><span data-stu-id="56154-128">Requirement</span></span> | <span data-ttu-id="56154-129">Значение</span><span class="sxs-lookup"><span data-stu-id="56154-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="56154-130">Header</span><span class="sxs-lookup"><span data-stu-id="56154-130">Header</span></span><br/>  | <dl> <span data-ttu-id="56154-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="56154-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="56154-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="56154-132">Library</span></span><br/> | <dl> <span data-ttu-id="56154-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="56154-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="56154-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56154-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56154-135">Математические функции</span><span class="sxs-lookup"><span data-stu-id="56154-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
