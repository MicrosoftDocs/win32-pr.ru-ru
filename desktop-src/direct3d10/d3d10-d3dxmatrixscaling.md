---
description: Функция D3DXMatrixScaling (D3DX10Math. h) — строит матрицу, которая масштабируется вдоль оси x, оси y и оси z.
ms.assetid: 1804bf41-26de-4be1-ad62-7a871d7408e6
title: Функция D3DXMatrixScaling (D3DX10Math. h)
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
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bf11b2196953775fb41412ad484a77ab00ae578e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108108932"
---
# <a name="d3dxmatrixscaling-function-d3dx10mathh"></a><span data-ttu-id="2e37c-103">Функция D3DXMatrixScaling (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="2e37c-103">D3DXMatrixScaling function (D3DX10Math.h)</span></span>

<span data-ttu-id="2e37c-104">Строит матрицу, которая масштабируется вдоль оси x, оси y и оси z.</span><span class="sxs-lookup"><span data-stu-id="2e37c-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e37c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2e37c-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="2e37c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2e37c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2e37c-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="2e37c-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2e37c-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e37c-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2e37c-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="2e37c-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2e37c-110">*SX* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2e37c-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e37c-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e37c-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e37c-112">Коэффициент масштабирования, применяемый вдоль оси x.</span><span class="sxs-lookup"><span data-stu-id="2e37c-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="2e37c-113">*SY* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2e37c-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e37c-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e37c-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e37c-115">Коэффициент масштабирования, применяемый вдоль оси y.</span><span class="sxs-lookup"><span data-stu-id="2e37c-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="2e37c-116">*SZ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2e37c-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2e37c-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2e37c-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2e37c-118">Коэффициент масштабирования, применяемый вдоль оси z.</span><span class="sxs-lookup"><span data-stu-id="2e37c-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2e37c-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e37c-119">Return value</span></span>

<span data-ttu-id="2e37c-120">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2e37c-120">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2e37c-121">Указатель на D3DXMATRIX преобразования масштабирования.</span><span class="sxs-lookup"><span data-stu-id="2e37c-121">Pointer to the scaling transformation D3DXMATRIX.</span></span>

## <a name="remarks"></a><span data-ttu-id="2e37c-122">Remarks</span><span class="sxs-lookup"><span data-stu-id="2e37c-122">Remarks</span></span>

<span data-ttu-id="2e37c-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="2e37c-123">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="2e37c-124">Таким образом, функция D3DXMatrixScaling может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="2e37c-124">In this way, the D3DXMatrixScaling function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2e37c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="2e37c-125">Requirements</span></span>



| <span data-ttu-id="2e37c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="2e37c-126">Requirement</span></span> | <span data-ttu-id="2e37c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="2e37c-127">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2e37c-128">Header</span><span class="sxs-lookup"><span data-stu-id="2e37c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="2e37c-129"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2e37c-129"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="2e37c-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2e37c-130">Library</span></span><br/> | <dl> <span data-ttu-id="2e37c-131"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2e37c-131"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2e37c-132">См. также</span><span class="sxs-lookup"><span data-stu-id="2e37c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e37c-133">Математические функции</span><span class="sxs-lookup"><span data-stu-id="2e37c-133">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
