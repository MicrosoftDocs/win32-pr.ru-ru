---
description: Вычисляются ориентированный ограничивающий прямоугольник на оси координат.
ms.assetid: 74e1b84e-1264-49eb-9172-7842af7e25e0
title: Функция D3DXComputeBoundingBox (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: df0376428153cfc02e499c9e26226cce81154023
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273819"
---
# <a name="d3dxcomputeboundingbox-function-d3dx9meshh"></a><span data-ttu-id="da2e4-103">Функция D3DXComputeBoundingBox (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="da2e4-103">D3DXComputeBoundingBox function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="da2e4-104">Вычисляются ориентированный ограничивающий прямоугольник на оси координат.</span><span class="sxs-lookup"><span data-stu-id="da2e4-104">Computes a coordinate-axis oriented bounding box.</span></span>

## <a name="syntax"></a><span data-ttu-id="da2e4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="da2e4-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingBox(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pMin,
  _Out_       D3DXVECTOR3 *pMax
);
```



## <a name="parameters"></a><span data-ttu-id="da2e4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="da2e4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da2e4-107">*пфирстпоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da2e4-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da2e4-108">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="da2e4-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="da2e4-109">Указатель на первую точку.</span><span class="sxs-lookup"><span data-stu-id="da2e4-109">Pointer to the first position.</span></span>

</dd> <dt>

<span data-ttu-id="da2e4-110">*Нумвертицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da2e4-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da2e4-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da2e4-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da2e4-112">Число вершин.</span><span class="sxs-lookup"><span data-stu-id="da2e4-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="da2e4-113">*двстриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="da2e4-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da2e4-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="da2e4-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="da2e4-115">Количество или число байтов между вершинами.</span><span class="sxs-lookup"><span data-stu-id="da2e4-115">Count or number of bytes between vertices.</span></span>

</dd> <dt>

<span data-ttu-id="da2e4-116">*ПМИН* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="da2e4-116">*pMin* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da2e4-117">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="da2e4-117">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="da2e4-118">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , описывающий возвращенный нижний левый угол ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="da2e4-118">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned lower-left corner of the bounding box.</span></span> <span data-ttu-id="da2e4-119">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="da2e4-119">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="da2e4-120">*ПМАКС* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="da2e4-120">*pMax* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da2e4-121">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="da2e4-121">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="da2e4-122">Указатель на структуру [**D3DXVECTOR3**](d3dxvector3.md) , описывающий возвращенный правый верхний угол ограничивающего прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="da2e4-122">Pointer to a [**D3DXVECTOR3**](d3dxvector3.md) structure, describing the returned upper-right corner of the bounding box.</span></span> <span data-ttu-id="da2e4-123">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="da2e4-123">See Remarks.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da2e4-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="da2e4-124">Return value</span></span>

<span data-ttu-id="da2e4-125">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="da2e4-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="da2e4-126">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="da2e4-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="da2e4-127">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="da2e4-127">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="remarks"></a><span data-ttu-id="da2e4-128">Remarks</span><span class="sxs-lookup"><span data-stu-id="da2e4-128">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="da2e4-129">Требования</span><span class="sxs-lookup"><span data-stu-id="da2e4-129">Requirements</span></span>



| <span data-ttu-id="da2e4-130">Требование</span><span class="sxs-lookup"><span data-stu-id="da2e4-130">Requirement</span></span> | <span data-ttu-id="da2e4-131">Значение</span><span class="sxs-lookup"><span data-stu-id="da2e4-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="da2e4-132">Header</span><span class="sxs-lookup"><span data-stu-id="da2e4-132">Header</span></span><br/>  | <dl> <span data-ttu-id="da2e4-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="da2e4-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="da2e4-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="da2e4-134">Library</span></span><br/> | <dl> <span data-ttu-id="da2e4-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="da2e4-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="da2e4-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="da2e4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da2e4-137">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="da2e4-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
