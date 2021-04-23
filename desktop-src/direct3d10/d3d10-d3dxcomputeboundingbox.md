---
description: Вычисляются ориентированный ограничивающий прямоугольник на оси координат.
ms.assetid: 1b8f328c-2fe1-462e-b464-c8dd9dc03e67
title: Функция D3DXComputeBoundingBox (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingBox
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 9a93eb4a10f6c2b2fd7eda82afcc21158138a1e8
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703921"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a><span data-ttu-id="e6a8c-103">Функция D3DXComputeBoundingBox (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="e6a8c-103">D3DXComputeBoundingBox function (D3DX10math.h)</span></span>

<span data-ttu-id="e6a8c-104">Вычисляются ориентированный ограничивающий прямоугольник на оси координат.</span><span class="sxs-lookup"><span data-stu-id="e6a8c-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a8c-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6a8c-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="e6a8c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6a8c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6a8c-107">*пфирстпоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6a8c-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a8c-108">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="e6a8c-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e6a8c-109">Указатель на первую точку.</span><span class="sxs-lookup"><span data-stu-id="e6a8c-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="e6a8c-110">*Нумвертицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6a8c-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a8c-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6a8c-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6a8c-112">Число вершин.</span><span class="sxs-lookup"><span data-stu-id="e6a8c-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="e6a8c-113">*двстриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e6a8c-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a8c-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e6a8c-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e6a8c-115">Количество или число байтов между вершинами.</span><span class="sxs-lookup"><span data-stu-id="e6a8c-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="e6a8c-116">*ПМИН* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e6a8c-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a8c-117">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6a8c-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e6a8c-118">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , описывающий возвращенный нижний левый угол ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="e6a8c-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span>

</dd> <dt>

<span data-ttu-id="e6a8c-119">*ПМАКС* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e6a8c-119">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6a8c-120">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="e6a8c-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="e6a8c-121">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , описывающий возвращенный правый верхний угол ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="e6a8c-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6a8c-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6a8c-122">Return value</span></span>

<span data-ttu-id="e6a8c-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e6a8c-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e6a8c-124">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e6a8c-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e6a8c-125">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="e6a8c-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a8c-126">Требования</span><span class="sxs-lookup"><span data-stu-id="e6a8c-126">Requirements</span></span>



| <span data-ttu-id="e6a8c-127">Требование</span><span class="sxs-lookup"><span data-stu-id="e6a8c-127">Requirement</span></span> | <span data-ttu-id="e6a8c-128">Значение</span><span class="sxs-lookup"><span data-stu-id="e6a8c-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a8c-129">Header</span><span class="sxs-lookup"><span data-stu-id="e6a8c-129">Header</span></span><br/>  | <dl> <span data-ttu-id="e6a8c-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="e6a8c-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="e6a8c-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e6a8c-131">Library</span></span><br/> | <dl> <span data-ttu-id="e6a8c-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e6a8c-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e6a8c-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6a8c-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a8c-134">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="e6a8c-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
