---
description: Использует левую систему координат для создания сетки, содержащей n-сторонний многоугольник.
ms.assetid: f3313f55-3e60-4440-8bea-d2886b636c9a
title: Функция D3DXCreatePolygon (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePolygon
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 94a7e48f512d25ca53d1f3ff80889a013e2ecdcb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081866"
---
# <a name="d3dxcreatepolygon-function"></a><span data-ttu-id="e41c5-103">Функция D3DXCreatePolygon</span><span class="sxs-lookup"><span data-stu-id="e41c5-103">D3DXCreatePolygon function</span></span>

<span data-ttu-id="e41c5-104">Использует левую систему координат для создания сетки, содержащей n-сторонний многоугольник.</span><span class="sxs-lookup"><span data-stu-id="e41c5-104">Uses a left-handed coordinate system to create a mesh containing an n-sided polygon.</span></span>

## <a name="syntax"></a><span data-ttu-id="e41c5-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e41c5-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePolygon(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Length,
  _In_  UINT              Sides,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="e41c5-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e41c5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e41c5-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e41c5-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e41c5-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e41c5-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e41c5-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с созданной сеткой многоугольников.</span><span class="sxs-lookup"><span data-stu-id="e41c5-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created polygon mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e41c5-110">*Длина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e41c5-110">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e41c5-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e41c5-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e41c5-112">Длина каждой стороны.</span><span class="sxs-lookup"><span data-stu-id="e41c5-112">Length of each side.</span></span>

</dd> <dt>

<span data-ttu-id="e41c5-113">*Стороны* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e41c5-113">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e41c5-114">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e41c5-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e41c5-115">Количество сторон многоугольника.</span><span class="sxs-lookup"><span data-stu-id="e41c5-115">Number of sides for the polygon.</span></span> <span data-ttu-id="e41c5-116">Значение должно быть больше или равно 3.</span><span class="sxs-lookup"><span data-stu-id="e41c5-116">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="e41c5-117">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e41c5-117">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e41c5-118">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="e41c5-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="e41c5-119">Адрес указателя на выходную форму, интерфейс [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="e41c5-119">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="e41c5-120">*ппаджаценци* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="e41c5-120">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e41c5-121">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="e41c5-121">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="e41c5-122">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="e41c5-122">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="e41c5-123">Когда метод возвращает значение, этот параметр заполняется массивом из трех DWORD на грань, которые указывают три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="e41c5-123">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="e41c5-124">Можно указать **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="e41c5-124">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e41c5-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e41c5-125">Return value</span></span>

<span data-ttu-id="e41c5-126">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e41c5-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e41c5-127">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e41c5-127">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e41c5-128">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e41c5-128">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e41c5-129">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e41c5-129">Remarks</span></span>

<span data-ttu-id="e41c5-130">Созданный многоугольник выравнивается по центру в источнике.</span><span class="sxs-lookup"><span data-stu-id="e41c5-130">The created polygon is centered at the origin.</span></span>

<span data-ttu-id="e41c5-131">Эта функция создает сетку с \_ параметром управляемого создания D3DXMESH и [D3DFVF \_ XYZ D3DFVF с \| \_ нормальным](d3dfvf.md) гибким форматом вершин (фвф).</span><span class="sxs-lookup"><span data-stu-id="e41c5-131">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="e41c5-132">Требования</span><span class="sxs-lookup"><span data-stu-id="e41c5-132">Requirements</span></span>



| <span data-ttu-id="e41c5-133">Требование</span><span class="sxs-lookup"><span data-stu-id="e41c5-133">Requirement</span></span> | <span data-ttu-id="e41c5-134">Значение</span><span class="sxs-lookup"><span data-stu-id="e41c5-134">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e41c5-135">Header</span><span class="sxs-lookup"><span data-stu-id="e41c5-135">Header</span></span><br/>  | <dl> <span data-ttu-id="e41c5-136"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="e41c5-136"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="e41c5-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e41c5-137">Library</span></span><br/> | <dl> <span data-ttu-id="e41c5-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e41c5-138"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="e41c5-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e41c5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e41c5-140">Функции рисования фигур</span><span class="sxs-lookup"><span data-stu-id="e41c5-140">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
