---
description: Функция D3DXMatrixPerspectiveFovRH (D3dx9math. h) — формирует матрицу правой проекции перспективы на основе поля представления.
ms.assetid: 3f4bc5d8-90af-4fdc-bc0c-931407cd7a9b
title: Функция D3DXMatrixPerspectiveFovRH (D3dx9math. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e8860a5d9fed13e8acdedfe67ed94a97911a6de0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118332"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx9mathh"></a><span data-ttu-id="53475-103">Функция D3DXMatrixPerspectiveFovRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="53475-103">D3DXMatrixPerspectiveFovRH function (D3dx9math.h)</span></span>

<span data-ttu-id="53475-104">Строит правовинтовую матрицу перспективной проекции на основании поля зрения.</span><span class="sxs-lookup"><span data-stu-id="53475-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="53475-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="53475-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="53475-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="53475-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="53475-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="53475-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="53475-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="53475-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="53475-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="53475-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="53475-110">*ФОВИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53475-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53475-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53475-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53475-112">Поле представления в направлении y (в радианах).</span><span class="sxs-lookup"><span data-stu-id="53475-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="53475-113">*Аспект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53475-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53475-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53475-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53475-115">Пропорции, определенные как ширина представления, деленная на высоту.</span><span class="sxs-lookup"><span data-stu-id="53475-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="53475-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53475-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53475-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53475-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53475-118">Z-значение ближней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="53475-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="53475-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="53475-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="53475-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="53475-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="53475-121">Z-значение дальней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="53475-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="53475-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53475-122">Return value</span></span>

<span data-ttu-id="53475-123">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="53475-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="53475-124">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является матрицей с правой стороны проекций.</span><span class="sxs-lookup"><span data-stu-id="53475-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="53475-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="53475-125">Remarks</span></span>

<span data-ttu-id="53475-126">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="53475-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="53475-127">Таким образом, функция **D3DXMatrixPerspectiveFovRH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="53475-127">In this way, the **D3DXMatrixPerspectiveFovRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="53475-128">Чтобы изменить ось пропорций, используйте формулу вычисления: ФОВИ = 2 \* Math. ATAN (Math. Tan (ФОВИ \* 0,5)/аспект).</span><span class="sxs-lookup"><span data-stu-id="53475-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="53475-129">Кроме того, добавьте в структуру переменные пропорций X и Y, чтобы масштабировать вертикальное пространство представления: ФОВИ = 2 \* Math. ATAN (Math. Tan (ФОВИ \* 0,5)/пропорции), аспект = Аспекткс \* аспект Y.</span><span class="sxs-lookup"><span data-stu-id="53475-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="53475-130">Эта функция вычислит возвращаемую матрицу, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="53475-130">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0        0        zf/(zn-zf)        -1
0        0        zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="53475-131">Требования</span><span class="sxs-lookup"><span data-stu-id="53475-131">Requirements</span></span>



| <span data-ttu-id="53475-132">Требование</span><span class="sxs-lookup"><span data-stu-id="53475-132">Requirement</span></span> | <span data-ttu-id="53475-133">Значение</span><span class="sxs-lookup"><span data-stu-id="53475-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="53475-134">Header</span><span class="sxs-lookup"><span data-stu-id="53475-134">Header</span></span><br/>  | <dl> <span data-ttu-id="53475-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="53475-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="53475-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="53475-136">Library</span></span><br/> | <dl> <span data-ttu-id="53475-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="53475-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="53475-138">См. также</span><span class="sxs-lookup"><span data-stu-id="53475-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53475-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="53475-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="53475-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="53475-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="53475-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="53475-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="53475-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="53475-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="53475-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="53475-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="53475-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="53475-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
