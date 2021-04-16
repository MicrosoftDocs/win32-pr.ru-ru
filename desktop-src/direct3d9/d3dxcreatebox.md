---
description: Использует левую систему координат для создания сетки, содержащей прямоугольник с выровняйтем по осям.
ms.assetid: 396ef0f7-65d5-46f9-9b97-e6471f2fb5fe
title: Функция D3DXCreateBox (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateBox
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 187c389dd2d90b4457237540026a63edc4ab4f4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720877"
---
# <a name="d3dxcreatebox-function"></a><span data-ttu-id="e5349-103">Функция D3DXCreateBox</span><span class="sxs-lookup"><span data-stu-id="e5349-103">D3DXCreateBox function</span></span>

<span data-ttu-id="e5349-104">Использует левую систему координат для создания сетки, содержащей прямоугольник с выровняйтем по осям.</span><span class="sxs-lookup"><span data-stu-id="e5349-104">Uses a left-handed coordinate system to create a mesh containing an axis-aligned box.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5349-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e5349-105">Syntax</span></span>


```C++
HRESULT D3DXCreateBox(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Width,
  _In_  FLOAT             Height,
  _In_  FLOAT             Depth,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="e5349-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e5349-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e5349-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5349-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5349-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e5349-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e5349-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с сеткой созданных Box.</span><span class="sxs-lookup"><span data-stu-id="e5349-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created box mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e5349-110">*Ширина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5349-110">*Width* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5349-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5349-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5349-112">Ширина прямоугольника вдоль оси x.</span><span class="sxs-lookup"><span data-stu-id="e5349-112">Width of the box, along the x-axis.</span></span>

</dd> <dt>

<span data-ttu-id="e5349-113">*Высота* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5349-113">*Height* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5349-114">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5349-114">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5349-115">Высота поля вдоль оси y.</span><span class="sxs-lookup"><span data-stu-id="e5349-115">Height of the box, along the y-axis.</span></span>

</dd> <dt>

<span data-ttu-id="e5349-116">*Глубина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e5349-116">*Depth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e5349-117">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e5349-117">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e5349-118">Глубина бокса вдоль оси z.</span><span class="sxs-lookup"><span data-stu-id="e5349-118">Depth of the box, along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="e5349-119">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e5349-119">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5349-120">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5349-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="e5349-121">Адрес указателя на выходную форму, интерфейс [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="e5349-121">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e5349-122">*ппаджаценци* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e5349-122">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e5349-123">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e5349-123">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e5349-124">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e5349-124">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="e5349-125">Когда метод возвращает значение, этот параметр заполняется массивом из трех DWORD на грань, которые указывают три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="e5349-125">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="e5349-126">Можно указать **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="e5349-126">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e5349-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e5349-127">Return value</span></span>

<span data-ttu-id="e5349-128">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e5349-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e5349-129">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e5349-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e5349-130">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e5349-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5349-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e5349-131">Remarks</span></span>

<span data-ttu-id="e5349-132">Созданное поле выравнивается по центру источника.</span><span class="sxs-lookup"><span data-stu-id="e5349-132">The created box is centered at the origin.</span></span>

<span data-ttu-id="e5349-133">Эта функция создает сетку с \_ параметром управляемого создания D3DXMESH и [D3DFVF \_ XYZ D3DFVF с \| \_ нормальным](d3dfvf.md) гибким форматом вершин (фвф).</span><span class="sxs-lookup"><span data-stu-id="e5349-133">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="e5349-134">Требования</span><span class="sxs-lookup"><span data-stu-id="e5349-134">Requirements</span></span>



| <span data-ttu-id="e5349-135">Требование</span><span class="sxs-lookup"><span data-stu-id="e5349-135">Requirement</span></span> | <span data-ttu-id="e5349-136">Значение</span><span class="sxs-lookup"><span data-stu-id="e5349-136">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e5349-137">Header</span><span class="sxs-lookup"><span data-stu-id="e5349-137">Header</span></span><br/>  | <dl> <span data-ttu-id="e5349-138"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="e5349-138"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="e5349-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e5349-139">Library</span></span><br/> | <dl> <span data-ttu-id="e5349-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e5349-140"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e5349-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e5349-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e5349-142">Функции рисования фигур</span><span class="sxs-lookup"><span data-stu-id="e5349-142">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
