---
description: Выполняет вычисление произведения двух функций, представленных с помощью SH (f и g).
ms.assetid: 632400a4-2ac9-438d-85f7-869101f350c8
title: Функция D3DXSHMultiply2 (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHMultiply2
- D3DXSHMultiply3
- D3DXSHMultiply4
- D3DXSHMultiply5
- D3DXSHMultiply6
api_type:
- HeaderDef
api_location:
- d3dx9math.h
ms.openlocfilehash: f7b9adaf5caf7b4b2d35035fd5c2a916298b0c8c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713610"
---
# <a name="d3dxshmultiply2-function-d3dx9mathh"></a><span data-ttu-id="f5305-103">Функция D3DXSHMultiply2 (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="f5305-103">D3DXSHMultiply2 function (D3dx9math.h)</span></span>

<span data-ttu-id="f5305-104">Выполняет вычисление произведения двух функций, представленных с помощью SH (f и g).</span><span class="sxs-lookup"><span data-stu-id="f5305-104">Computes the product of two functions represented using SH (f and g).</span></span>

## <a name="syntax"></a><span data-ttu-id="f5305-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f5305-105">Syntax</span></span>


```C++
FLOAT* D3DXSHMultiply2(
  _In_       FLOAT *pOut,
  _In_ const FLOAT *pF,
  _In_ const FLOAT *pG
);
```



## <a name="parameters"></a><span data-ttu-id="f5305-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f5305-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5305-107">*тоска* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5305-107">*pOut* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5305-108">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f5305-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f5305-109">Указатель на выходную функцию SH илм хранится в l \* l + m + l.</span><span class="sxs-lookup"><span data-stu-id="f5305-109">Pointer to the output SH coefficients - basis function Ylm is stored at l\*l + m+l.</span></span>

</dd> <dt>

<span data-ttu-id="f5305-110">*Общая папка* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5305-110">*pF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5305-111">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f5305-111">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f5305-112">Вход SH коеффс для первой функции.</span><span class="sxs-lookup"><span data-stu-id="f5305-112">Input SH coeffs for first function.</span></span>

</dd> <dt>

<span data-ttu-id="f5305-113">*PG* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="f5305-113">*pG* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5305-114">Тип: **const [**float**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="f5305-114">Type: **const [**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f5305-115">Второй набор входных данных SH коеффс.</span><span class="sxs-lookup"><span data-stu-id="f5305-115">Second set of input SH coeffs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5305-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f5305-116">Return value</span></span>

<span data-ttu-id="f5305-117">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="f5305-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="f5305-118">Указатель на коэффициенты вывода SH.</span><span class="sxs-lookup"><span data-stu-id="f5305-118">Pointer to SH output coefficients.</span></span>

## <a name="remarks"></a><span data-ttu-id="f5305-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f5305-119">Remarks</span></span>

<span data-ttu-id="f5305-120">Порядок — это число от 2 до 6 включительно.</span><span class="sxs-lookup"><span data-stu-id="f5305-120">The order is a number between 2 and 6 inclusive.</span></span> <span data-ttu-id="f5305-121">В действительности эта страница документирует несколько функций: D3DXSHMultiply2, D3DXSHMultiply3,... D3DXSHMultiply6.</span><span class="sxs-lookup"><span data-stu-id="f5305-121">So this page actually documents several functions: D3DXSHMultiply2, D3DXSHMultiply3, ... D3DXSHMultiply6.</span></span>

<span data-ttu-id="f5305-122">Вычисляет произведение двух функций, представленных с помощью SH (f и g), где *тоска* \[ i \] = int (y i (s) f (s) g (s) \_ \* \* ), где y \_ i (s) — это функция i-го sh, f (s) и g (s) — функции SH (сумма \_ i (y \_ i (s) \* c \_ i)).</span><span class="sxs-lookup"><span data-stu-id="f5305-122">Computes the product of two functions represented using SH (f and g), where *pOut*\[i\] = int(y\_i(s) \* f(s) \* g(s)), where y\_i(s) is the ith SH basis function, f(s) and g(s) are SH functions (sum\_i(y\_i(s)\*c\_i)).</span></span> <span data-ttu-id="f5305-123">Order O определяет длины массивов, где всегда должно быть коэффициенты O ^ 2.</span><span class="sxs-lookup"><span data-stu-id="f5305-123">The order O determines the lengths of the arrays, where there should always be O^2 coefficients.</span></span> <span data-ttu-id="f5305-124">В целом, произведение двух функций SH для Order O создает функцию SH в порядке 2 \* o-1, но результаты усекаются.</span><span class="sxs-lookup"><span data-stu-id="f5305-124">In general the product of two SH functions of order O generates an SH function of order 2\*O - 1, but the results are truncated.</span></span> <span data-ttu-id="f5305-125">Это означает, что продукт работает (f \* g = = g \* f), но не связан (f \* (g \* h)! = (f \* g) \* h.</span><span class="sxs-lookup"><span data-stu-id="f5305-125">This means that the product commutes (f\*g == g\*f) but doesn't associate (f\*(g\*h) != (f\*g)\*h.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5305-126">Требования</span><span class="sxs-lookup"><span data-stu-id="f5305-126">Requirements</span></span>



| <span data-ttu-id="f5305-127">Требование</span><span class="sxs-lookup"><span data-stu-id="f5305-127">Requirement</span></span> | <span data-ttu-id="f5305-128">Значение</span><span class="sxs-lookup"><span data-stu-id="f5305-128">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5305-129">Header</span><span class="sxs-lookup"><span data-stu-id="f5305-129">Header</span></span><br/> | <dl> <span data-ttu-id="f5305-130"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="f5305-130"><dt>D3dx9math.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f5305-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f5305-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5305-132">Математические функции</span><span class="sxs-lookup"><span data-stu-id="f5305-132">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
