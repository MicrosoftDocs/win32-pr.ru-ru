---
description: Функция D3DXComputeBoundingSphere (D3DX9Mesh. h) — вычисление ограничивающей сферы для сетки.
ms.assetid: efa1365b-fe3a-4165-a3cb-bc1cd2ba03c0
title: Функция D3DXComputeBoundingSphere (D3DX9Mesh. h)
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
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: dbfccb13dfe15b06de98ddba114cdc62c5f4ec05
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108115822"
---
# <a name="d3dxcomputeboundingsphere-function-d3dx9meshh"></a><span data-ttu-id="ba4b3-103">Функция D3DXComputeBoundingSphere (D3DX9Mesh. h)</span><span class="sxs-lookup"><span data-stu-id="ba4b3-103">D3DXComputeBoundingSphere function (D3DX9Mesh.h)</span></span>

<span data-ttu-id="ba4b3-104">Вычисление ограничивающей сферы для сетки.</span><span class="sxs-lookup"><span data-stu-id="ba4b3-104">Computes a bounding sphere for the mesh.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba4b3-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ba4b3-105">Syntax</span></span>


```C++
HRESULT D3DXComputeBoundingSphere(
  _In_  const D3DXVECTOR3 *pFirstPosition,
  _In_        DWORD       NumVertices,
  _In_        DWORD       dwStride,
  _Out_       D3DXVECTOR3 *pCenter,
  _Out_       FLOAT       *pRadius
);
```



## <a name="parameters"></a><span data-ttu-id="ba4b3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ba4b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba4b3-107">*пфирстпоситион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba4b3-107">*pFirstPosition* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4b3-108">Тип: **const [**D3DXVECTOR3**](d3dxvector3.md) \***</span><span class="sxs-lookup"><span data-stu-id="ba4b3-108">Type: **const [**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ba4b3-109">Указатель на первую точку.</span><span class="sxs-lookup"><span data-stu-id="ba4b3-109">Pointer to first position.</span></span>

</dd> <dt>

<span data-ttu-id="ba4b3-110">*Нумвертицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba4b3-110">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4b3-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba4b3-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba4b3-112">Число вершин.</span><span class="sxs-lookup"><span data-stu-id="ba4b3-112">Number of vertices.</span></span>

</dd> <dt>

<span data-ttu-id="ba4b3-113">*двстриде* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ba4b3-113">*dwStride* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4b3-114">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ba4b3-114">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ba4b3-115">Число байтов между векторами позиционирования.</span><span class="sxs-lookup"><span data-stu-id="ba4b3-115">Number of bytes between position vectors.</span></span> <span data-ttu-id="ba4b3-116">Чтобы получить шаг вершин, используйте [**жетнумбитеспервертекс**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md)или [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) .</span><span class="sxs-lookup"><span data-stu-id="ba4b3-116">Use [**GetNumBytesPerVertex**](id3dxbasemesh--getnumbytespervertex.md), [**D3DXGetFVFVertexSize**](d3dxgetfvfvertexsize.md), or [**D3DXGetDeclVertexSize**](d3dxgetdeclvertexsize.md) to get the vertex stride.</span></span>

</dd> <dt>

<span data-ttu-id="ba4b3-117">*пцентер* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ba4b3-117">*pCenter* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4b3-118">Тип: **[ **D3DXVECTOR3**](d3dxvector3.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba4b3-118">Type: **[**D3DXVECTOR3**](d3dxvector3.md)\***</span></span>

<span data-ttu-id="ba4b3-119">Структура [**D3DXVECTOR3**](d3dxvector3.md) , определяющая центр координат возвращаемой ограничивающей сферы.</span><span class="sxs-lookup"><span data-stu-id="ba4b3-119">[**D3DXVECTOR3**](d3dxvector3.md) structure, defining the coordinate center of the returned bounding sphere.</span></span>

</dd> <dt>

<span data-ttu-id="ba4b3-120">*Прадиус* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ba4b3-120">*pRadius* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ba4b3-121">Тип: **[ **float**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="ba4b3-121">Type: **[**FLOAT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="ba4b3-122">Радиус возвращаемой ограничивающей сферы.</span><span class="sxs-lookup"><span data-stu-id="ba4b3-122">Radius of the returned bounding sphere.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba4b3-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ba4b3-123">Return value</span></span>

<span data-ttu-id="ba4b3-124">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ba4b3-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ba4b3-125">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ba4b3-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ba4b3-126">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл.</span><span class="sxs-lookup"><span data-stu-id="ba4b3-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba4b3-127">Требования</span><span class="sxs-lookup"><span data-stu-id="ba4b3-127">Requirements</span></span>



| <span data-ttu-id="ba4b3-128">Требование</span><span class="sxs-lookup"><span data-stu-id="ba4b3-128">Requirement</span></span> | <span data-ttu-id="ba4b3-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ba4b3-129">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ba4b3-130">Header</span><span class="sxs-lookup"><span data-stu-id="ba4b3-130">Header</span></span><br/>  | <dl> <span data-ttu-id="ba4b3-131"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba4b3-131"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="ba4b3-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ba4b3-132">Library</span></span><br/> | <dl> <span data-ttu-id="ba4b3-133"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ba4b3-133"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="ba4b3-134">См. также</span><span class="sxs-lookup"><span data-stu-id="ba4b3-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba4b3-135">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="ba4b3-135">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
