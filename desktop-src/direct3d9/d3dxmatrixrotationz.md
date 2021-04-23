---
description: Строит матрицу, которая поворачивается вокруг оси z.
ms.assetid: 73db43e6-3831-4867-8eda-80127b61e169
title: Функция D3DXMatrixRotationZ (D3dx9math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXMatrixRotationZ
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 61d94df676016c0e22e7c0842eebe9af05b9ff71
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694248"
---
# <a name="d3dxmatrixrotationz-function-d3dx9mathh"></a><span data-ttu-id="2ff0b-103">Функция D3DXMatrixRotationZ (D3dx9math. h)</span><span class="sxs-lookup"><span data-stu-id="2ff0b-103">D3DXMatrixRotationZ function (D3dx9math.h)</span></span>

<span data-ttu-id="2ff0b-104">Строит матрицу, которая поворачивается вокруг оси z.</span><span class="sxs-lookup"><span data-stu-id="2ff0b-104">Builds a matrix that rotates around the z-axis.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff0b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2ff0b-105">Syntax</span></span>


```C++
D3DXMATRIX* D3DXMatrixRotationZ(
  _Inout_ D3DXMATRIX *pOut,
  _In_    FLOAT      Angle
);
```



## <a name="parameters"></a><span data-ttu-id="2ff0b-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2ff0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2ff0b-107">*тоска* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="2ff0b-107">*pOut* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff0b-108">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ff0b-108">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ff0b-109">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , которая является результатом операции.</span><span class="sxs-lookup"><span data-stu-id="2ff0b-109">Pointer to the [**D3DXMATRIX**](d3dxmatrix.md) structure that is the result of the operation.</span></span>

</dd> <dt>

<span data-ttu-id="2ff0b-110">*Угол* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="2ff0b-110">*Angle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2ff0b-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2ff0b-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2ff0b-112">Угол поворота в радианах.</span><span class="sxs-lookup"><span data-stu-id="2ff0b-112">Angle of rotation, in radians.</span></span> <span data-ttu-id="2ff0b-113">Углы измеряются по часовой стрелке при просмотре из оси вращения (положительная сторона) в направлении к источнику.</span><span class="sxs-lookup"><span data-stu-id="2ff0b-113">Angles are measured clockwise when viewed from the rotation axis (positive side) toward the origin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2ff0b-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2ff0b-114">Return value</span></span>

<span data-ttu-id="2ff0b-115">Тип: **[ **D3DXMATRIX**](d3dxmatrix.md)\***</span><span class="sxs-lookup"><span data-stu-id="2ff0b-115">Type: **[**D3DXMATRIX**](d3dxmatrix.md)\***</span></span>

<span data-ttu-id="2ff0b-116">Указатель на структуру [**D3DXMATRIX**](d3dxmatrix.md) , повернутую вокруг оси z.</span><span class="sxs-lookup"><span data-stu-id="2ff0b-116">Pointer to a [**D3DXMATRIX**](d3dxmatrix.md) structure rotated around the z-axis.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ff0b-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ff0b-117">Remarks</span></span>

<span data-ttu-id="2ff0b-118">Возвращаемое значение для этой функции совпадает со значением, возвращаемым в параметре *тоска* .</span><span class="sxs-lookup"><span data-stu-id="2ff0b-118">The return value for this function is the same value returned in the *pOut* parameter.</span></span> <span data-ttu-id="2ff0b-119">Таким образом, функция **D3DXMatrixRotationZ** может использоваться в качестве параметра для другой функции.</span><span class="sxs-lookup"><span data-stu-id="2ff0b-119">In this way, the **D3DXMatrixRotationZ** function can be used as a parameter for another function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff0b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="2ff0b-120">Requirements</span></span>



| <span data-ttu-id="2ff0b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="2ff0b-121">Requirement</span></span> | <span data-ttu-id="2ff0b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="2ff0b-122">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff0b-123">Header</span><span class="sxs-lookup"><span data-stu-id="2ff0b-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2ff0b-124"><dt>D3dx9math. h</dt></span><span class="sxs-lookup"><span data-stu-id="2ff0b-124"><dt>D3dx9math.h</dt></span></span> </dl> |
| <span data-ttu-id="2ff0b-125">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2ff0b-125">Library</span></span><br/> | <dl> <span data-ttu-id="2ff0b-126"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2ff0b-126"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2ff0b-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ff0b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff0b-128">Математические функции</span><span class="sxs-lookup"><span data-stu-id="2ff0b-128">Math Functions</span></span>](dx9-graphics-reference-d3dx-functions-math.md)
</dt> <dt>

[<span data-ttu-id="2ff0b-129">**D3DXMatrixRotationAxis**</span><span class="sxs-lookup"><span data-stu-id="2ff0b-129">**D3DXMatrixRotationAxis**</span></span>](d3dxmatrixrotationaxis.md)
</dt> <dt>

[<span data-ttu-id="2ff0b-130">**D3DXMatrixRotationQuaternion**</span><span class="sxs-lookup"><span data-stu-id="2ff0b-130">**D3DXMatrixRotationQuaternion**</span></span>](d3dxmatrixrotationquaternion.md)
</dt> <dt>

[<span data-ttu-id="2ff0b-131">**D3DXMatrixRotationX**</span><span class="sxs-lookup"><span data-stu-id="2ff0b-131">**D3DXMatrixRotationX**</span></span>](d3dxmatrixrotationx.md)
</dt> <dt>

[<span data-ttu-id="2ff0b-132">**D3DXMatrixRotationY**</span><span class="sxs-lookup"><span data-stu-id="2ff0b-132">**D3DXMatrixRotationY**</span></span>](d3dxmatrixrotationy.md)
</dt> <dt>

[<span data-ttu-id="2ff0b-133">**D3DXMatrixRotationYawPitchRoll**</span><span class="sxs-lookup"><span data-stu-id="2ff0b-133">**D3DXMatrixRotationYawPitchRoll**</span></span>](d3dxmatrixrotationyawpitchroll.md)
</dt> </dl>

 

 
