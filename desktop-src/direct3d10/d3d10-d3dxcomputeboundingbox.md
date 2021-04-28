---
description: Функция D3DXComputeBoundingBox (D3DX10math. h) — вычисление ограничивающего прямоугольника, ориентированного на ось координат.
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
ms.openlocfilehash: 2a12e7e302fb36ffb8856e6402f110e01bb2afb2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108103532"
---
# <a name="d3dxcomputeboundingbox-function-d3dx10mathh"></a><span data-ttu-id="88079-103">Функция D3DXComputeBoundingBox (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="88079-103">D3DXComputeBoundingBox function (D3DX10math.h)</span></span>

<span data-ttu-id="88079-104">Вычисляются ориентированный ограничивающий прямоугольник на оси координат.</span><span class="sxs-lookup"><span data-stu-id="88079-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="88079-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="88079-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="88079-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="88079-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="88079-107">*пфирстпоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88079-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88079-108">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="88079-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="88079-109">Указатель на первую точку.</span><span class="sxs-lookup"><span data-stu-id="88079-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="88079-110">*Нумвертицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88079-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88079-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88079-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="88079-112">Число вершин.</span><span class="sxs-lookup"><span data-stu-id="88079-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="88079-113">*двстриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="88079-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="88079-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="88079-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="88079-115">Количество или число байтов между вершинами.</span><span class="sxs-lookup"><span data-stu-id="88079-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="88079-116">*ПМИН* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="88079-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88079-117">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="88079-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="88079-118">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , описывающий возвращенный нижний левый угол ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="88079-118">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span>

</dd> <dt>

<span data-ttu-id="88079-119">*ПМАКС* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="88079-119">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="88079-120">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="88079-120">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="88079-121">Указатель на структуру [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , описывающий возвращенный правый верхний угол ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="88079-121">Pointer to a [**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="88079-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="88079-122">Return value</span></span>

<span data-ttu-id="88079-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="88079-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="88079-124">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="88079-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="88079-125">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="88079-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="88079-126">Требования</span><span class="sxs-lookup"><span data-stu-id="88079-126">Requirements</span></span>



| <span data-ttu-id="88079-127">Требование</span><span class="sxs-lookup"><span data-stu-id="88079-127">Requirement</span></span> | <span data-ttu-id="88079-128">Значение</span><span class="sxs-lookup"><span data-stu-id="88079-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="88079-129">Header</span><span class="sxs-lookup"><span data-stu-id="88079-129">Header</span></span><br/>  | <dl> <span data-ttu-id="88079-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="88079-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="88079-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="88079-131">Library</span></span><br/> | <dl> <span data-ttu-id="88079-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="88079-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="88079-133">См. также</span><span class="sxs-lookup"><span data-stu-id="88079-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88079-134">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="88079-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
