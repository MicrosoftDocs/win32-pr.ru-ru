---
description: Строит матрицу, отражающую систему координат для плоскости.
ms.assetid: bd2c5905-780e-4fac-a848-d7dbcfc390c6
title: Функция D3DXMatrixReflect (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixReflect
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: d8c8f0fc8529730a46c403432ec0b5b5a86c8afa
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720942"
---
# <a name="d3dxmatrixreflect-function-d3dx10mathh"></a><span data-ttu-id="6600e-103">Функция D3DXMatrixReflect (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="6600e-103">D3DXMatrixReflect function (D3DX10Math.h)</span></span>

<span data-ttu-id="6600e-104">Строит матрицу, отражающую систему координат для плоскости.</span><span class="sxs-lookup"><span data-stu-id="6600e-104">Builds a matrix that reflects the coordinate system about a plane.</span></span>

## <a name="syntax"></a><span data-ttu-id="6600e-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6600e-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixReflect(
  _Inout_       D3DXMATRIX *pOut,
  _In_    const D3DXPLANE  *pPlane
);
```



## <a name="parameters"></a><span data-ttu-id="6600e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6600e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6600e-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="6600e-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="6600e-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6600e-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6600e-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="6600e-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="6600e-110">*пплане* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="6600e-110">*pPlane* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6600e-111">Тип: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md) \***</span><span class="sxs-lookup"><span data-stu-id="6600e-111">Type: **const [**D3DXPLANE**](../direct3d9/d3dxplane.md)\***</span></span>

<span data-ttu-id="6600e-112">Указатель на источник [**D3DXPLANE**](d3d10-d3dxplane.md).</span><span class="sxs-lookup"><span data-stu-id="6600e-112">Pointer to the source [**D3DXPLANE**](d3d10-d3dxplane.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6600e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6600e-113">Return value</span></span>

<span data-ttu-id="6600e-114">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="6600e-114">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="6600e-115">Указатель на структуру D3DXMATRIX, отражающую систему координат относительно исходной плоскости.</span><span class="sxs-lookup"><span data-stu-id="6600e-115">Pointer to a D3DXMATRIX structure that reflects the coordinate system about the source plane.</span></span>

## <a name="remarks"></a><span data-ttu-id="6600e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6600e-116">Remarks</span></span>

<span data-ttu-id="6600e-117">Эта функция нормализует уравнение плоскости перед созданием отраженной матрицы.</span><span class="sxs-lookup"><span data-stu-id="6600e-117">This function normalizes the plane equation before it creates the reflected matrix.</span></span>

<span data-ttu-id="6600e-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="6600e-118">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="6600e-119">Таким образом, функция D3DXMatrixReflect может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="6600e-119">In this way, the D3DXMatrixReflect function can be used as a parameter for another function.</span></span>

<span data-ttu-id="6600e-120">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="6600e-120">This function uses the following formula to compute the returned matrix.</span></span>


```
P = normalize(Plane);
    
-2 * P.a * P.a + 1  -2 * P.b * P.a      -2 * P.c * P.a        0
-2 * P.a * P.b      -2 * P.b * P.b + 1  -2 * P.c * P.b        0
-2 * P.a * P.c      -2 * P.b * P.c      -2 * P.c * P.c + 1    0
-2 * P.a * P.d      -2 * P.b * P.d      -2 * P.c * P.d        1
```



## <a name="requirements"></a><span data-ttu-id="6600e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="6600e-121">Requirements</span></span>



| <span data-ttu-id="6600e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="6600e-122">Requirement</span></span> | <span data-ttu-id="6600e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="6600e-123">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6600e-124">Header</span><span class="sxs-lookup"><span data-stu-id="6600e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="6600e-125"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="6600e-125"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="6600e-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="6600e-126">Library</span></span><br/> | <dl> <span data-ttu-id="6600e-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="6600e-127"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="6600e-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6600e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6600e-129">Математические функции</span><span class="sxs-lookup"><span data-stu-id="6600e-129">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
