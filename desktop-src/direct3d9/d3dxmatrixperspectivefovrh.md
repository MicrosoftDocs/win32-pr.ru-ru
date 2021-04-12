---
description: Строит правовинтовую матрицу перспективной проекции на основании поля зрения.
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
ms.openlocfilehash: da478a027db8c366a2cfec827075d3d4b73ae014
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355413"
---
# <a name="d3dxmatrixperspectivefovrh-function-d3dx9mathh"></a><span data-ttu-id="363ed-103">Функция D3DXMatrixPerspectiveFovRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="363ed-103">D3DXMatrixPerspectiveFovRH function (D3dx9math.h)</span></span>

<span data-ttu-id="363ed-104">Строит правовинтовую матрицу перспективной проекции на основании поля зрения.</span><span class="sxs-lookup"><span data-stu-id="363ed-104">Builds a right-handed perspective projection matrix based on a field of view.</span></span>

## <a name="syntax"></a><span data-ttu-id="363ed-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="363ed-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveFovRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      fovy,
  _In_    FLOAT      Aspect,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="363ed-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="363ed-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="363ed-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="363ed-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="363ed-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="363ed-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="363ed-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="363ed-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="363ed-110">*ФОВИ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="363ed-110">*fovy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="363ed-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="363ed-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="363ed-112">Поле представления в направлении y (в радианах).</span><span class="sxs-lookup"><span data-stu-id="363ed-112">Field of view in the y direction, in radians.</span></span>

</dd> <dt>

<span data-ttu-id="363ed-113">*Аспект* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="363ed-113">*Aspect* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="363ed-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="363ed-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="363ed-115">Пропорции, определенные как ширина представления, деленная на высоту.</span><span class="sxs-lookup"><span data-stu-id="363ed-115">Aspect ratio, defined as view space width divided by height.</span></span>

</dd> <dt>

<span data-ttu-id="363ed-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="363ed-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="363ed-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="363ed-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="363ed-118">Z-значение ближней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="363ed-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="363ed-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="363ed-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="363ed-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="363ed-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="363ed-121">Z-значение дальней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="363ed-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="363ed-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="363ed-122">Return value</span></span>

<span data-ttu-id="363ed-123">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="363ed-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="363ed-124">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является матрицей с правой стороны проекций.</span><span class="sxs-lookup"><span data-stu-id="363ed-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="363ed-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="363ed-125">Remarks</span></span>

<span data-ttu-id="363ed-126">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="363ed-126">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="363ed-127">Таким образом, функция **D3DXMatrixPerspectiveFovRH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="363ed-127">In this way, the **D3DXMatrixPerspectiveFovRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="363ed-128">Чтобы изменить ось пропорций, используйте формулу вычисления: ФОВИ = 2 \* Math. ATAN (Math. Tan (ФОВИ \* 0,5)/аспект).</span><span class="sxs-lookup"><span data-stu-id="363ed-128">To change the aspect ratio axis, use the calculation formula: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspect).</span></span> <span data-ttu-id="363ed-129">Кроме того, добавьте в структуру переменные пропорций X и Y, чтобы масштабировать вертикальное пространство представления: ФОВИ = 2 \* Math. ATAN (Math. Tan (ФОВИ \* 0,5)/пропорции), аспект = Аспекткс \* аспект Y.</span><span class="sxs-lookup"><span data-stu-id="363ed-129">Alternatively, add X and Y aspect ratio variables in the structure to scale the vertical view space: fovy = 2 \* math.atan(math.tan(fovy \* 0.5) / aspectY), aspect = aspectX \* aspect Y.</span></span>

<span data-ttu-id="363ed-130">Эта функция вычислит возвращаемую матрицу, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="363ed-130">This function computes the returned matrix as shown.</span></span>


```
xScale     0          0              0
0        yScale       0              0
0        0        zf/(zn-zf)        -1
0        0        zn*zf/(zn-zf)      0
where:
yScale = cot(fovY/2)
    
xScale = yScale / aspect ratio
```



## <a name="requirements"></a><span data-ttu-id="363ed-131">Требования</span><span class="sxs-lookup"><span data-stu-id="363ed-131">Requirements</span></span>



| <span data-ttu-id="363ed-132">Требование</span><span class="sxs-lookup"><span data-stu-id="363ed-132">Requirement</span></span> | <span data-ttu-id="363ed-133">Значение</span><span class="sxs-lookup"><span data-stu-id="363ed-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="363ed-134">Header</span><span class="sxs-lookup"><span data-stu-id="363ed-134">Header</span></span><br/>  | <dl> <span data-ttu-id="363ed-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="363ed-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="363ed-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="363ed-136">Library</span></span><br/> | <dl> <span data-ttu-id="363ed-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="363ed-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="363ed-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="363ed-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="363ed-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="363ed-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="363ed-140">**D3DXMatrixPerspectiveRH**</span><span class="sxs-lookup"><span data-stu-id="363ed-140">**D3DXMatrixPerspectiveRH**</span></span>](d3dxmatrixperspectiverh.md)
</dt> <dt>

[<span data-ttu-id="363ed-141">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="363ed-141">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="363ed-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="363ed-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="363ed-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="363ed-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="363ed-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="363ed-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
