---
description: Строит матрицу, которая масштабируется вдоль оси x, оси y и оси z.
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
ms.openlocfilehash: 7cfc14fc1d514f68f2881d26c4729440d709af93
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713474"
---
# <a name="d3dxmatrixscaling-function-d3dx9mathh"></a><span data-ttu-id="0d896-103">Функция D3DXMatrixScaling (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="0d896-103">D3DXMatrixScaling function (D3dx9math.h)</span></span>

<span data-ttu-id="0d896-104">Строит матрицу, которая масштабируется вдоль оси x, оси y и оси z.</span><span class="sxs-lookup"><span data-stu-id="0d896-104">Builds a matrix that scales along the x-axis, the y-axis, and the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d896-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0d896-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixScaling(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      sx,
  _In_    FLOAT      sy,
  _In_    FLOAT      sz
);
```



## <a name="parameters"></a><span data-ttu-id="0d896-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0d896-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d896-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="0d896-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="0d896-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d896-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0d896-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="0d896-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="0d896-110">*SX* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d896-110">*sx* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d896-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d896-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d896-112">Коэффициент масштабирования, применяемый вдоль оси x.</span><span class="sxs-lookup"><span data-stu-id="0d896-112">Scaling factor that is applied along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="0d896-113">*SY* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d896-113">*sy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d896-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d896-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d896-115">Коэффициент масштабирования, применяемый вдоль оси y.</span><span class="sxs-lookup"><span data-stu-id="0d896-115">Scaling factor that is applied along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="0d896-116">*SZ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0d896-116">*sz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0d896-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0d896-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0d896-118">Коэффициент масштабирования, применяемый вдоль оси z.</span><span class="sxs-lookup"><span data-stu-id="0d896-118">Scaling factor that is applied along the z-axis.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d896-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0d896-119">Return value</span></span>

<span data-ttu-id="0d896-120">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="0d896-120">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="0d896-121">Указатель на [**D3DXMATRIX**](d3dxmatrix.md)преобразования масштабирования.</span><span class="sxs-lookup"><span data-stu-id="0d896-121">Pointer to the scaling transformation [**D3DXMATRIX**](d3dxmatrix.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0d896-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d896-122">Remarks</span></span>

<span data-ttu-id="0d896-123">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="0d896-123">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="0d896-124">Таким образом, функция **D3DXMatrixScaling** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="0d896-124">In this way, the **D3DXMatrixScaling** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d896-125">Требования</span><span class="sxs-lookup"><span data-stu-id="0d896-125">Requirements</span></span>



| <span data-ttu-id="0d896-126">Требование</span><span class="sxs-lookup"><span data-stu-id="0d896-126">Requirement</span></span> | <span data-ttu-id="0d896-127">Значение</span><span class="sxs-lookup"><span data-stu-id="0d896-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0d896-128">Header</span><span class="sxs-lookup"><span data-stu-id="0d896-128">Header</span></span><br/>  | <dl> <span data-ttu-id="0d896-129"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d896-129"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="0d896-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0d896-130">Library</span></span><br/> | <dl> <span data-ttu-id="0d896-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0d896-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="0d896-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d896-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d896-133">Математические функции</span><span class="sxs-lookup"><span data-stu-id="0d896-133">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> </dl>

 

 
