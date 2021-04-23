---
description: Строит правовинтовую матрицу перспективной проекции.
ms.assetid: dd9b041b-922b-43df-a6e9-46c97204338a
title: Функция D3DXMatrixPerspectiveRH (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixPerspectiveRH
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bcec04202ecb2de15c479ac4ce84d4ee86c99a2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273705"
---
# <a name="d3dxmatrixperspectiverh-function-d3dx9mathh"></a><span data-ttu-id="95e41-103">Функция D3DXMatrixPerspectiveRH (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="95e41-103">D3DXMatrixPerspectiveRH function (D3dx9math.h)</span></span>

<span data-ttu-id="95e41-104">Строит правовинтовую матрицу перспективной проекции.</span><span class="sxs-lookup"><span data-stu-id="95e41-104">Builds a right-handed perspective projection matrix.</span></span>

## <a name="syntax"></a><span data-ttu-id="95e41-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="95e41-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixPerspectiveRH(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      w,
  _In_    FLOAT      h,
  _In_    FLOAT      zn,
  _In_    FLOAT      zf
);
```



## <a name="parameters"></a><span data-ttu-id="95e41-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="95e41-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95e41-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="95e41-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="95e41-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="95e41-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="95e41-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="95e41-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="95e41-110">*w* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="95e41-110">*w* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95e41-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95e41-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95e41-112">Ширина отображаемого объема на ближайшей плоскости представления.</span><span class="sxs-lookup"><span data-stu-id="95e41-112">Width of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="95e41-113">*ч* \[ в\]</span><span class="sxs-lookup"><span data-stu-id="95e41-113">*h* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95e41-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95e41-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95e41-115">Высота отображаемого объема на ближайшей плоскости представления.</span><span class="sxs-lookup"><span data-stu-id="95e41-115">Height of the view volume at the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="95e41-116">*ЗН* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95e41-116">*zn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95e41-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95e41-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95e41-118">Z-значение ближней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="95e41-118">Z-value of the near view-plane.</span></span>

</dd> <dt>

<span data-ttu-id="95e41-119">*ЗФ* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="95e41-119">*zf* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95e41-120">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="95e41-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="95e41-121">Z-значение дальней плоскости просмотра.</span><span class="sxs-lookup"><span data-stu-id="95e41-121">Z-value of the far view-plane.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95e41-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="95e41-122">Return value</span></span>

<span data-ttu-id="95e41-123">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="95e41-123">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="95e41-124">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является матрицей с правой стороны проекций.</span><span class="sxs-lookup"><span data-stu-id="95e41-124">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure that is a right-handed perspective projection matrix.</span></span>

## <a name="remarks"></a><span data-ttu-id="95e41-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="95e41-125">Remarks</span></span>

<span data-ttu-id="95e41-126">Все параметры функции **D3DXMatrixPerspectiveRH** — это расстояния в пространстве камеры.</span><span class="sxs-lookup"><span data-stu-id="95e41-126">All the parameters of the **D3DXMatrixPerspectiveRH** function are distances in camera space.</span></span> <span data-ttu-id="95e41-127">Параметры описывают размеры представления объема.</span><span class="sxs-lookup"><span data-stu-id="95e41-127">The parameters describe the dimensions of the view volume.</span></span>

<span data-ttu-id="95e41-128">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="95e41-128">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="95e41-129">Таким образом, функция **D3DXMatrixPerspectiveRH** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="95e41-129">In this way, the **D3DXMatrixPerspectiveRH** function can be used as a parameter for another function.</span></span>

<span data-ttu-id="95e41-130">Эта функция использует следующую формулу для вычисления возвращаемой матрицы.</span><span class="sxs-lookup"><span data-stu-id="95e41-130">This function uses the following formula to compute the returned matrix.</span></span>


```
2*zn/w  0       0              0
0       2*zn/h  0              0
0       0       zf/(zn-zf)    -1
0       0       zn*zf/(zn-zf)  0
```



## <a name="requirements"></a><span data-ttu-id="95e41-131">Требования</span><span class="sxs-lookup"><span data-stu-id="95e41-131">Requirements</span></span>



| <span data-ttu-id="95e41-132">Требование</span><span class="sxs-lookup"><span data-stu-id="95e41-132">Requirement</span></span> | <span data-ttu-id="95e41-133">Значение</span><span class="sxs-lookup"><span data-stu-id="95e41-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="95e41-134">Header</span><span class="sxs-lookup"><span data-stu-id="95e41-134">Header</span></span><br/>  | <dl> <span data-ttu-id="95e41-135"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="95e41-135"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="95e41-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="95e41-136">Library</span></span><br/> | <dl> <span data-ttu-id="95e41-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="95e41-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="95e41-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="95e41-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95e41-139">Математические функции</span><span class="sxs-lookup"><span data-stu-id="95e41-139">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="95e41-140">**D3DXMatrixPerspectiveLH**</span><span class="sxs-lookup"><span data-stu-id="95e41-140">**D3DXMatrixPerspectiveLH**</span></span>](d3dxmatrixperspectivelh.md)
</dt> <dt>

[<span data-ttu-id="95e41-141">**D3DXMatrixPerspectiveFovRH**</span><span class="sxs-lookup"><span data-stu-id="95e41-141">**D3DXMatrixPerspectiveFovRH**</span></span>](d3dxmatrixperspectivefovrh.md)
</dt> <dt>

[<span data-ttu-id="95e41-142">**D3DXMatrixPerspectiveFovLH**</span><span class="sxs-lookup"><span data-stu-id="95e41-142">**D3DXMatrixPerspectiveFovLH**</span></span>](d3dxmatrixperspectivefovlh.md)
</dt> <dt>

[<span data-ttu-id="95e41-143">**D3DXMatrixPerspectiveOffCenterRH**</span><span class="sxs-lookup"><span data-stu-id="95e41-143">**D3DXMatrixPerspectiveOffCenterRH**</span></span>](d3dxmatrixperspectiveoffcenterrh.md)
</dt> <dt>

[<span data-ttu-id="95e41-144">**D3DXMatrixPerspectiveOffCenterLH**</span><span class="sxs-lookup"><span data-stu-id="95e41-144">**D3DXMatrixPerspectiveOffCenterLH**</span></span>](d3dxmatrixperspectiveoffcenterlh.md)
</dt> </dl>

 

 
