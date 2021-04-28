---
description: Функция D3DXMatrixScaling (D3dx9math. h) — строит матрицу, которая масштабируется вдоль оси x, оси y и оси z.
ms.assetid: f51baa4e-0aec-4de8-b746-24cb52f318d6
title: Функция D3DXMatrixScaling (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixScaling
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 97ccd4cc6207bb211259833d163793c3499b51a1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118072"
---
# <a name="d3dxmatrixscaling-function-d3dx9mathh"></a><span data-ttu-id="9aa80-103">Функция D3DXMatrixScaling (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="9aa80-103">D3DXMatrixScaling function (D3dx9math.h)</span></span>

<span data-ttu-id="9aa80-104">Строит матрицу, которая масштабируется вдоль оси x, оси y и оси z.</span><span class="sxs-lookup"><span data-stu-id="9aa80-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="9aa80-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="9aa80-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="9aa80-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9aa80-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9aa80-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="9aa80-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa80-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9aa80-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9aa80-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="9aa80-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="9aa80-110">*SX* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9aa80-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa80-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aa80-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aa80-112">Коэффициент масштабирования, применяемый вдоль оси x.</span><span class="sxs-lookup"><span data-stu-id="9aa80-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9aa80-113">*SY* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9aa80-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa80-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aa80-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aa80-115">Коэффициент масштабирования, применяемый вдоль оси y.</span><span class="sxs-lookup"><span data-stu-id="9aa80-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="9aa80-116">*SZ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="9aa80-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9aa80-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="9aa80-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="9aa80-118">Коэффициент масштабирования, применяемый вдоль оси z.</span><span class="sxs-lookup"><span data-stu-id="9aa80-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9aa80-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9aa80-119">Return value</span></span>

<span data-ttu-id="9aa80-120">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="9aa80-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="9aa80-121">Указатель на [**D3DXMATRIX**](d3dxmatrix.md)преобразования масштабирования.</span><span class="sxs-lookup"><span data-stu-id="9aa80-121">Pointer to the scaling transformation [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="9aa80-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="9aa80-122">Remarks</span></span>

<span data-ttu-id="9aa80-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="9aa80-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="9aa80-124">Таким образом, функция **D3DXMatrixScaling** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="9aa80-124">In this way, the **D3DXMatrixScaling** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="9aa80-125">Требования</span><span class="sxs-lookup"><span data-stu-id="9aa80-125">Requirements</span></span>



| <span data-ttu-id="9aa80-126">Требование</span><span class="sxs-lookup"><span data-stu-id="9aa80-126">Requirement</span></span> | <span data-ttu-id="9aa80-127">Значение</span><span class="sxs-lookup"><span data-stu-id="9aa80-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9aa80-128">Header</span><span class="sxs-lookup"><span data-stu-id="9aa80-128">Header</span></span><br/>  | <dl> <span data-ttu-id="9aa80-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="9aa80-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="9aa80-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9aa80-130">Library</span></span><br/> | <dl> <span data-ttu-id="9aa80-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9aa80-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="9aa80-132">См. также</span><span class="sxs-lookup"><span data-stu-id="9aa80-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9aa80-133">Математические функции</span><span class="sxs-lookup"><span data-stu-id="9aa80-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
