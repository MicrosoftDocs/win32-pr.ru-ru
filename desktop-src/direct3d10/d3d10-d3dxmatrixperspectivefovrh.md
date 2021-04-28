---
description: Функция D3DXMatrixPerspectiveFovRH (D3DX10Math. h) — формирует матрицу правой проекции перспективы на основе поля представления.
ms.assetid: a75e6666-e6c0-4a54-bc88-835fa012542f
title: Функция D3DXMatrixPerspectiveFovRH (D3DX10Math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovRH
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 38d48789bab9b968b6bcf657459c408abdba774b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108109112"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx10mathh"></a><span data-ttu-id="187df-103">Функция D3DXMatrixPerspectiveFovRH (D3DX10Math. h)</span><span class="sxs-lookup"><span data-stu-id="187df-103">D3DXMatrixPerspectiveFovRH function (D3DX10Math.h)</span></span>

<span data-ttu-id="187df-104">Строит правовинтовую матрицу перспективной проекции на основании поля зрения.</span><span class="sxs-lookup"><span data-stu-id="187df-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="187df-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="187df-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="187df-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="187df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="187df-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="187df-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="187df-108">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="187df-108">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="187df-109">Указатель на структуру [**D3DXMATRIX**](d3d10-d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="187df-109">Pointer to the [**D3DXMATRIX**](d3d10-d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="187df-110">*ФОВИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="187df-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="187df-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="187df-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="187df-112">Поле представления в направлении y (в радианах).</span><span class="sxs-lookup"><span data-stu-id="187df-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="187df-113">*Аспект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="187df-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="187df-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="187df-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="187df-115">Пропорции, определенные как ширина представления, деленная на высоту.</span><span class="sxs-lookup"><span data-stu-id="187df-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="187df-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="187df-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="187df-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="187df-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="187df-118">Z-значение ближней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="187df-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="187df-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="187df-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="187df-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="187df-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="187df-121">Z-значение дальней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="187df-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="187df-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="187df-122">Return value</span></span>

<span data-ttu-id="187df-123">Тип: **[ **D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="187df-123">Type: **[**D3DXMATRIX**](../direct3d9/d3dxmatrix.md)\***</span></span>

<span data-ttu-id="187df-124">Указатель на структуру D3DXMATRIX, которая является матрицей с правой стороны проекций.</span><span class="sxs-lookup"><span data-stu-id="187df-124">Pointer to a D3DXMATRIX structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="187df-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="187df-125">Remarks</span></span>

<span data-ttu-id="187df-126">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре тоска.</span><span class="sxs-lookup"><span data-stu-id="187df-126">The return value for this function is the same value returned in the pOut parameter.</span></span> <span data-ttu-id="187df-127">Таким образом, функция D3DXMatrixPerspectiveFovRH может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="187df-127">In this way, the D3DXMatrixPerspectiveFovRH function can be used as a parameter for another function.</span></span>

<span data-ttu-id="187df-128">Эта функция вычислит возвращаемую матрицу, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="187df-128">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0          0      zf/(zn-zf)        -1
0          0      zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="187df-129">Требования</span><span class="sxs-lookup"><span data-stu-id="187df-129">Requirements</span></span>



| <span data-ttu-id="187df-130">Требование</span><span class="sxs-lookup"><span data-stu-id="187df-130">Requirement</span></span> | <span data-ttu-id="187df-131">Значение</span><span class="sxs-lookup"><span data-stu-id="187df-131">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="187df-132">Header</span><span class="sxs-lookup"><span data-stu-id="187df-132">Header</span></span><br/>  | <dl> <span data-ttu-id="187df-133"><dt>D3DX10Math. h</dt></span><span class="sxs-lookup"><span data-stu-id="187df-133"><dt>D3DX10Math.h</dt></span></span> </dl> |
| <span data-ttu-id="187df-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="187df-134">Library</span></span><br/> | <dl> <span data-ttu-id="187df-135"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="187df-135"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="187df-136">См. также</span><span class="sxs-lookup"><span data-stu-id="187df-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="187df-137">Математические функции</span><span class="sxs-lookup"><span data-stu-id="187df-137">Math Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-math.md)
</dt> </dl>

 

 
