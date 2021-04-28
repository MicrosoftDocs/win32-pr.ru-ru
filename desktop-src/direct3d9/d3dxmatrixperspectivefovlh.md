---
description: Функция D3DXMatrixPerspectiveFovLH (D3dx9math. h) — формирует матрицу левой проекции перспективы на основе поля представления.
ms.assetid: 90328798-f124-4b61-90a9-971946066b02
title: Функция D3DXMatrixPerspectiveFovLH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveFovLH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: eec478fec30567fbf301054ddfa60f1689bfee8e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118352"
---
# <a name="d3dxmatrixperspectivefovlh-function-d3dx9mathh"></a><span data-ttu-id="87c27-103">Функция D3DXMatrixPerspectiveFovLH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="87c27-103">D3DXMatrixPerspectiveFovLH function (D3dx9math.h)</span></span>

<span data-ttu-id="87c27-104">Строит левовинтовую матрицу перспективной проекции на основании поля зрения.</span><span class="sxs-lookup"><span data-stu-id="87c27-104">Builds a left-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="87c27-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="87c27-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovLH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="87c27-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="87c27-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87c27-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="87c27-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="87c27-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="87c27-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="87c27-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="87c27-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="87c27-110">*ФОВИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87c27-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87c27-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87c27-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87c27-112">Поле представления в направлении y (в радианах).</span><span class="sxs-lookup"><span data-stu-id="87c27-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="87c27-113">*Аспект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87c27-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87c27-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87c27-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87c27-115">Пропорции, определенные как ширина представления, деленная на высоту.</span><span class="sxs-lookup"><span data-stu-id="87c27-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="87c27-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87c27-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87c27-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87c27-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87c27-118">Z-значение ближней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="87c27-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="87c27-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="87c27-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87c27-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="87c27-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="87c27-121">Z-значение дальней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="87c27-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87c27-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87c27-122">Return value</span></span>

<span data-ttu-id="87c27-123">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="87c27-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="87c27-124">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является матрицей перспективной проекции влево.</span><span class="sxs-lookup"><span data-stu-id="87c27-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a left-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="87c27-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="87c27-125">Remarks</span></span>

<span data-ttu-id="87c27-126">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="87c27-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="87c27-127">Таким образом, функция **D3DXMatrixPerspectiveFovLH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="87c27-127">In this way, the **D3DXMatrixPerspectiveFovLH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="87c27-128">Чтобы изменить ось пропорций, используйте формулу вычисления: ФОВИ = 2 \* Math. ATAN (Math. Tan (ФОВИ \* 0,5)/аспект).</span><span class="sxs-lookup"><span data-stu-id="87c27-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="87c27-129">Кроме того, добавьте в структуру переменные пропорций X и Y, чтобы масштабировать вертикальное пространство представления: ФОВИ = 2 \* Math. ATAN (Math. Tan (ФОВИ \* 0,5)/пропорции), аспект = Аспекткс \* аспект Y.</span><span class="sxs-lookup"><span data-stu-id="87c27-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="87c27-130">Эта функция вычислит возвращаемую матрицу, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="87c27-130">This function computes the returned matrix as shown:</span></span>


```
xScale     0          0               0
0        yScale       0               0
0          0       zf/(zf-zn)         1
0          0       -zn*zf/(zf-zn)     0
where:
yScale = cot(fovY/2)

xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="87c27-131">Требования</span><span class="sxs-lookup"><span data-stu-id="87c27-131">Requirements</span></span>



| <span data-ttu-id="87c27-132">Требование</span><span class="sxs-lookup"><span data-stu-id="87c27-132">Requirement</span></span> | <span data-ttu-id="87c27-133">Значение</span><span class="sxs-lookup"><span data-stu-id="87c27-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87c27-134">Header</span><span class="sxs-lookup"><span data-stu-id="87c27-134">Header</span></span><br/>  | <dl> <span data-ttu-id="87c27-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="87c27-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="87c27-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="87c27-136">Library</span></span><br/> | <dl> <span data-ttu-id="87c27-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="87c27-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="87c27-138">См. также</span><span class="sxs-lookup"><span data-stu-id="87c27-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87c27-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="87c27-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="87c27-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="87c27-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="87c27-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="87c27-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="87c27-142">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="87c27-142">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="87c27-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="87c27-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="87c27-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="87c27-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
