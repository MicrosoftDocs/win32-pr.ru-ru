---
description: Вычисление ограничивающей сферы для сетки.
ms.assetid: 54f486d2-45e9-4fc1-90a3-97488ed4d900
title: Функция D3DXComputeBoundingSphere (D3DX10math. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeBoundingSphere
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 0c8e59b4d39652d02ce19f4c1bf6b0617fee7772
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273902"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx10mathh"></a><span data-ttu-id="d5ee2-103">Функция D3DXComputeBoundingSphere (D3DX10math. h)</span><span class="sxs-lookup"><span data-stu-id="d5ee2-103">D3DXComputeBoundingSphere function (D3DX10math.h)</span></span>

<span data-ttu-id="d5ee2-104">Вычисление ограничивающей сферы для сетки.</span><span class="sxs-lookup"><span data-stu-id="d5ee2-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5ee2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d5ee2-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_ const D3DXVECTOR3 *pFirstPosition,
  _In_       DWORD       NumVertices,
  _In_       DWORD       dwStride,
  _In_       D3DXVECTOR3 *pCenter,
  _In_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="d5ee2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d5ee2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d5ee2-107">*пфирстпоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5ee2-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ee2-108">Тип: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="d5ee2-108">Type: **const [**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d5ee2-109">Указатель на первую точку.</span><span class="sxs-lookup"><span data-stu-id="d5ee2-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="d5ee2-110">*Нумвертицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5ee2-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ee2-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5ee2-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5ee2-112">Число вершин.</span><span class="sxs-lookup"><span data-stu-id="d5ee2-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d5ee2-113">*двстриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5ee2-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ee2-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="d5ee2-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="d5ee2-115">Число байтов между векторами позиционирования.</span><span class="sxs-lookup"><span data-stu-id="d5ee2-115">Number of bytes between position vectors.</span></span>

</dd> <dt>

<span data-ttu-id="d5ee2-116">*пцентер* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5ee2-116">*pCenter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ee2-117">Тип: **[ **D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="d5ee2-117">Type: **[**D3DXVECTOR3**](../direct3d9/d3dxvector3.md)\***</span></span>

<span data-ttu-id="d5ee2-118">Структура [**D3DXVECTOR3**](d3d10-d3dxvector3.md) , определяющая центр координат возвращаемой ограничивающей сферы.</span><span class="sxs-lookup"><span data-stu-id="d5ee2-118">[**D3DXVECTOR3**](d3d10-d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="d5ee2-119">*Прадиус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="d5ee2-119">*pRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d5ee2-120">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="d5ee2-120">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="d5ee2-121">Радиус возвращаемой ограничивающей сферы.</span><span class="sxs-lookup"><span data-stu-id="d5ee2-121">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d5ee2-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d5ee2-122">Return value</span></span>

<span data-ttu-id="d5ee2-123">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d5ee2-123">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d5ee2-124">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="d5ee2-124">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="d5ee2-125">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="d5ee2-125">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5ee2-126">Требования</span><span class="sxs-lookup"><span data-stu-id="d5ee2-126">Requirements</span></span>



| <span data-ttu-id="d5ee2-127">Требование</span><span class="sxs-lookup"><span data-stu-id="d5ee2-127">Requirement</span></span> | <span data-ttu-id="d5ee2-128">Значение</span><span class="sxs-lookup"><span data-stu-id="d5ee2-128">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d5ee2-129">Header</span><span class="sxs-lookup"><span data-stu-id="d5ee2-129">Header</span></span><br/>  | <dl> <span data-ttu-id="d5ee2-130"><dt>D3DX10math. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5ee2-130"><dt>D3DX10math.h</dt></span></span> </dl> |
| <span data-ttu-id="d5ee2-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="d5ee2-131">Library</span></span><br/> | <dl> <span data-ttu-id="d5ee2-132"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d5ee2-132"><dt>D3DX10.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="d5ee2-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5ee2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5ee2-134">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="d5ee2-134">Mesh Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-mesh.md)
</dt> </dl>

 

 
