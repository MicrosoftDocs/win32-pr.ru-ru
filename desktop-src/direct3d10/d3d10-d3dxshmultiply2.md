---
description: Выполняет вычисление произведения двух сферовых гармонических функций (f и g). Обе функции имеют порядок N = 2.
ms.assetid: 9e0942ce-e39d-4147-9472-cda8a97fd390
title: Функция D3DXSHMultiply2 (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: a72cdf7eb28b06e11b4901ebd048af143dfbdb5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703905"
---
# <a name="d3dxshmultiply2-function-d3dx10mathh"></a><span data-ttu-id="cb0d4-104">Функция D3DXSHMultiply2 (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="cb0d4-104">D3DXSHMultiply2 function (D3DX10Math.h)</span></span>

<span data-ttu-id="cb0d4-105">Выполняет вычисление произведения двух сферовых гармонических функций (*f* и *g*).</span><span class="sxs-lookup"><span data-stu-id="cb0d4-105">Computes the product of two spherical harmonics functions (*f* and *g*).</span></span> <span data-ttu-id="cb0d4-106">Обе функции имеют порядок N = 2.</span><span class="sxs-lookup"><span data-stu-id="cb0d4-106">Both functions are of order N = 2.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb0d4-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="cb0d4-107">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply2(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="cb0d4-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="cb0d4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cb0d4-109">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb0d4-109">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb0d4-110">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb0d4-110">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cb0d4-111">Указатель на выводимые коэффициенты SH — функция *Y* LM хранится в l ² + *m* + l.</span><span class="sxs-lookup"><span data-stu-id="cb0d4-111">Pointer to the output SH coefficients — the basis function *Y* ₗₘ is stored at l² + *m* + l.</span></span> <span data-ttu-id="cb0d4-112">Порядок *n* определяет длину массива, где всегда должно быть коэффициентов *n*².</span><span class="sxs-lookup"><span data-stu-id="cb0d4-112">The order *N* determines the length of the array, where there should always be *N*² coefficients.</span></span>

</dd> <dt>

<span data-ttu-id="cb0d4-113">*Общая папка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb0d4-113">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb0d4-114">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cb0d4-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cb0d4-115">Входные коэффициенты SH для первой функции.</span><span class="sxs-lookup"><span data-stu-id="cb0d4-115">Input SH coefficients for first function.</span></span>

</dd> <dt>

<span data-ttu-id="cb0d4-116">*PG* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="cb0d4-116">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cb0d4-117">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="cb0d4-117">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cb0d4-118">Второй набор коэффициентов входных данных SH.</span><span class="sxs-lookup"><span data-stu-id="cb0d4-118">Second set of input SH coefficients.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cb0d4-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="cb0d4-119">Return value</span></span>

<span data-ttu-id="cb0d4-120">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="cb0d4-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="cb0d4-121">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="cb0d4-121">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb0d4-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cb0d4-122">Remarks</span></span>

<span data-ttu-id="cb0d4-123">Произведение двух функций SH в заказе N = 2 создает функцию SH в заказе 2 × *N* -1 = 3, но результаты усекаются.</span><span class="sxs-lookup"><span data-stu-id="cb0d4-123">The product of two SH functions of order N = 2 generates an SH function of order 2 × *N* - 1 = 3, but the results are truncated.</span></span> <span data-ttu-id="cb0d4-124">Это означает, что продукт работает ( *f* × *g*  =  *g* x *f* ), но не связан ( *f* × (*g* x *h*) ≠ ( *f* × *g*) × *h* ).</span><span class="sxs-lookup"><span data-stu-id="cb0d4-124">This means that the product commutes ( *f* × *g* = *g* × *f* ) but doesn't associate ( *f* × (*g* × *h*) ≠ ( *f* × *g*) × *h* ).</span></span>

<span data-ttu-id="cb0d4-125">Эта функция использует следующее уравнение:</span><span class="sxs-lookup"><span data-stu-id="cb0d4-125">This function uses the following equation:</span></span>


```
pOut[i] = int(y_i(s) * f(s) * g(s))
```



<span data-ttu-id="cb0d4-126">где y \_ i (s) — это функция-i sh, где f (s) и g (s) используют следующую функцию SH:</span><span class="sxs-lookup"><span data-stu-id="cb0d4-126">where y\_i(s) is the ith SH basis function, and where f(s) and g(s) use the following SH function:</span></span>


```
sum_i(y_i(s)*c_i)
```



## <a name="requirements"></a><span data-ttu-id="cb0d4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="cb0d4-127">Requirements</span></span>



| <span data-ttu-id="cb0d4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="cb0d4-128">Requirement</span></span> | <span data-ttu-id="cb0d4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="cb0d4-129">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cb0d4-130">Header</span><span class="sxs-lookup"><span data-stu-id="cb0d4-130">Header</span></span><br/>  | <dl> <span data-ttu-id="cb0d4-131"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="cb0d4-131"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="cb0d4-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="cb0d4-132">Library</span></span><br/> | <dl> <span data-ttu-id="cb0d4-133"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="cb0d4-133"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="cb0d4-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cb0d4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb0d4-135">Математические функции</span><span class="sxs-lookup"><span data-stu-id="cb0d4-135">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
