---
description: Использует левую систему координат для создания сетки, содержащей сферу.
ms.assetid: d3198805-9435-4849-892d-ec98dc2221d2
title: Функция D3DXCreateSphere (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateSphere
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e56ac6b8e8cc2195e2176e505cf430ea33b6b6ce
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273788"
---
# <a name="d3dxcreatesphere-function"></a><span data-ttu-id="60489-103">Функция D3DXCreateSphere</span><span class="sxs-lookup"><span data-stu-id="60489-103">D3DXCreateSphere function</span></span>

<span data-ttu-id="60489-104">Использует левую систему координат для создания сетки, содержащей сферу.</span><span class="sxs-lookup"><span data-stu-id="60489-104">Uses a left-handed coordinate system to create a mesh containing a sphere.</span></span>

## <a name="syntax"></a><span data-ttu-id="60489-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="60489-105">Syntax</span></span>


```C++
HRESULT D3DXCreateSphere(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="60489-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="60489-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60489-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60489-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60489-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="60489-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="60489-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с созданной сеткой сферы.</span><span class="sxs-lookup"><span data-stu-id="60489-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created sphere mesh.</span></span>

</dd> <dt>

<span data-ttu-id="60489-110">*Радиус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60489-110">*Radius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60489-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60489-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60489-112">Радиус сферы.</span><span class="sxs-lookup"><span data-stu-id="60489-112">Radius of the sphere.</span></span> <span data-ttu-id="60489-113">Это значение должно быть больше или равно 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="60489-113">This value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="60489-114">*Срезы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60489-114">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60489-115">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60489-115">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60489-116">Количество срезов относительно основной оси.</span><span class="sxs-lookup"><span data-stu-id="60489-116">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="60489-117">*Стеки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="60489-117">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60489-118">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="60489-118">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="60489-119">Количество стеков на главной оси.</span><span class="sxs-lookup"><span data-stu-id="60489-119">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="60489-120">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="60489-120">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60489-121">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="60489-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="60489-122">Адрес указателя на выходную форму, интерфейс [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="60489-122">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="60489-123">*ппаджаценци* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="60489-123">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="60489-124">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="60489-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="60489-125">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="60489-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="60489-126">Когда метод возвращает значение, этот параметр заполняется массивом из трех DWORD на грань, которые указывают три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="60489-126">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="60489-127">Можно указать **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="60489-127">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60489-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="60489-128">Return value</span></span>

<span data-ttu-id="60489-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="60489-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="60489-130">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="60489-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="60489-131">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="60489-131">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="60489-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="60489-132">Remarks</span></span>

<span data-ttu-id="60489-133">Созданная сфера располагается по центру источника, а ее ось — по оси z.</span><span class="sxs-lookup"><span data-stu-id="60489-133">The created sphere is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="60489-134">Эта функция создает сетку с \_ параметром управляемого создания D3DXMESH и [D3DFVF \_ XYZ D3DFVF с \| \_ нормальным](d3dfvf.md) гибким форматом вершин (фвф).</span><span class="sxs-lookup"><span data-stu-id="60489-134">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="60489-135">Требования</span><span class="sxs-lookup"><span data-stu-id="60489-135">Requirements</span></span>



| <span data-ttu-id="60489-136">Требование</span><span class="sxs-lookup"><span data-stu-id="60489-136">Requirement</span></span> | <span data-ttu-id="60489-137">Значение</span><span class="sxs-lookup"><span data-stu-id="60489-137">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60489-138">Header</span><span class="sxs-lookup"><span data-stu-id="60489-138">Header</span></span><br/>  | <dl> <span data-ttu-id="60489-139"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="60489-139"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="60489-140">Библиотека</span><span class="sxs-lookup"><span data-stu-id="60489-140">Library</span></span><br/> | <dl> <span data-ttu-id="60489-141"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="60489-141"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="60489-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="60489-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60489-143">Функции рисования фигур</span><span class="sxs-lookup"><span data-stu-id="60489-143">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
