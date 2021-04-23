---
description: Создает оптимизированное сопоставление лиц для списка треугольников.
ms.assetid: 428c2af8-43e7-4cf7-8b9b-04ba5cff82c8
title: Функция D3DXOptimizeFaces (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXOptimizeFaces
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6c56dec04e01b542d2c760852a58826a8186c213
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694084"
---
# <a name="d3dxoptimizefaces-function"></a><span data-ttu-id="a11b4-103">Функция D3DXOptimizeFaces</span><span class="sxs-lookup"><span data-stu-id="a11b4-103">D3DXOptimizeFaces function</span></span>

<span data-ttu-id="a11b4-104">Создает оптимизированное сопоставление лиц для списка треугольников.</span><span class="sxs-lookup"><span data-stu-id="a11b4-104">Generates an optimized face remapping for a triangle list.</span></span>

## <a name="syntax"></a><span data-ttu-id="a11b4-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a11b4-105">Syntax</span></span>


```C++
HRESULT D3DXOptimizeFaces(
  _In_    LPCVOID pIndices,
  _In_    UINT    NumFaces,
  _In_    UINT    NumVertices,
  _In_    BOOL    Indices32Bit,
  _Inout_ DWORD   *pFaceRemap
);
```



## <a name="parameters"></a><span data-ttu-id="a11b4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a11b4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a11b4-107">*пиндицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a11b4-107">*pIndices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a11b4-108">Тип: **[ **лпквоид**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a11b4-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a11b4-109">Указатель на индексы списка треугольников для использования при упорядочивании вершин.</span><span class="sxs-lookup"><span data-stu-id="a11b4-109">Pointer to triangle list indices to use for ordering vertices.</span></span>

</dd> <dt>

<span data-ttu-id="a11b4-110">*Нумфацес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a11b4-110">*NumFaces* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a11b4-111">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a11b4-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a11b4-112">Число сторон в списке треугольников.</span><span class="sxs-lookup"><span data-stu-id="a11b4-112">Number of faces in the triangle list.</span></span> <span data-ttu-id="a11b4-113">Для 16-разрядных сеток это ограничение составляет 2 ^ 16-1 (65535) или меньше лиц.</span><span class="sxs-lookup"><span data-stu-id="a11b4-113">For 16-bit meshes, this is limited to 2^16 - 1 (65535) or fewer faces.</span></span>

</dd> <dt>

<span data-ttu-id="a11b4-114">*Нумвертицес* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a11b4-114">*NumVertices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a11b4-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a11b4-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a11b4-116">Число вершин, на которые ссылается список треугольников.</span><span class="sxs-lookup"><span data-stu-id="a11b4-116">Number of vertices referenced by the triangle list.</span></span>

</dd> <dt>

<span data-ttu-id="a11b4-117">*Indices32Bit* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a11b4-117">*Indices32Bit* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a11b4-118">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a11b4-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a11b4-119">Флаг, указывающий тип индекса: **true** , если индексы являются 32-разрядными (более 65535 индексами), **значение false** , если индексы являются 16-разрядными (65535 или меньшего количества индексов).</span><span class="sxs-lookup"><span data-stu-id="a11b4-119">Flag indicating index type: **TRUE** if indices are 32-bit (more than 65535 indices), **FALSE** if indices are 16-bit (65535 or fewer indices).</span></span>

</dd> <dt>

<span data-ttu-id="a11b4-120">*пфацеремап* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="a11b4-120">*pFaceRemap* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="a11b4-121">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="a11b4-121">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="a11b4-122">Указатель на исходную сетчатую линию, разделенную для создания текущего лица.</span><span class="sxs-lookup"><span data-stu-id="a11b4-122">Pointer to the original mesh face that was split to generate the current face.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a11b4-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a11b4-123">Return value</span></span>

<span data-ttu-id="a11b4-124">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a11b4-124">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a11b4-125">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="a11b4-125">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a11b4-126">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="a11b4-126">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="a11b4-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a11b4-127">Remarks</span></span>

<span data-ttu-id="a11b4-128">Процедура оптимизации этой функции функционально эквивалентна вызову [**ID3DXMesh:: optimize**](id3dxmesh--optimize.md) с \_ флагом D3DXMESHOPT девицеиндепендент, но эта функция делает более эффективное использование кэшей вершин.</span><span class="sxs-lookup"><span data-stu-id="a11b4-128">This function's optimization procedure is functionally equivalent to calling [**ID3DXMesh::Optimize**](id3dxmesh--optimize.md) with the D3DXMESHOPT\_DEVICEINDEPENDENT flag, but this function makes more efficient use of vertex caches.</span></span>

## <a name="requirements"></a><span data-ttu-id="a11b4-129">Требования</span><span class="sxs-lookup"><span data-stu-id="a11b4-129">Requirements</span></span>



| <span data-ttu-id="a11b4-130">Требование</span><span class="sxs-lookup"><span data-stu-id="a11b4-130">Requirement</span></span> | <span data-ttu-id="a11b4-131">Значение</span><span class="sxs-lookup"><span data-stu-id="a11b4-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a11b4-132">Header</span><span class="sxs-lookup"><span data-stu-id="a11b4-132">Header</span></span><br/>  | <dl> <span data-ttu-id="a11b4-133"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="a11b4-133"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="a11b4-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a11b4-134">Library</span></span><br/> | <dl> <span data-ttu-id="a11b4-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a11b4-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a11b4-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a11b4-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a11b4-137">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="a11b4-137">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
