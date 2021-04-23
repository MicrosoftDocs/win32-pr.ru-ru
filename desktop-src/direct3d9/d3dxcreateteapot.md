---
description: Использует левую систему координат для создания сетки, содержащей чайник.
ms.assetid: c002d6d4-1829-4293-9a86-d8560d6ec0e9
title: Функция D3DXCreateTeapot (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTeapot
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 13f5ed44bdc31958729209f01183eba409298fcd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273787"
---
# <a name="d3dxcreateteapot-function"></a><span data-ttu-id="ece7f-103">Функция D3DXCreateTeapot</span><span class="sxs-lookup"><span data-stu-id="ece7f-103">D3DXCreateTeapot function</span></span>

<span data-ttu-id="ece7f-104">Использует левую систему координат для создания сетки, содержащей чайник.</span><span class="sxs-lookup"><span data-stu-id="ece7f-104">Uses a left-handed coordinate system to create a mesh containing a teapot.</span></span>

## <a name="syntax"></a><span data-ttu-id="ece7f-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ece7f-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTeapot(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="ece7f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="ece7f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ece7f-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="ece7f-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ece7f-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="ece7f-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="ece7f-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с созданной сеткой чайник.</span><span class="sxs-lookup"><span data-stu-id="ece7f-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created teapot mesh.</span></span>

</dd> <dt>

<span data-ttu-id="ece7f-110">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ece7f-110">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ece7f-111">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="ece7f-111">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="ece7f-112">Адрес указателя на выходную форму, интерфейс [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="ece7f-112">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ece7f-113">*ппаджаценци* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="ece7f-113">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ece7f-114">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="ece7f-114">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="ece7f-115">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="ece7f-115">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="ece7f-116">Когда метод возвращает значение, этот параметр заполняется массивом из трех DWORD на грань, которые указывают три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="ece7f-116">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="ece7f-117">Можно указать **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="ece7f-117">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ece7f-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ece7f-118">Return value</span></span>

<span data-ttu-id="ece7f-119">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ece7f-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ece7f-120">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="ece7f-120">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ece7f-121">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="ece7f-121">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="ece7f-122">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ece7f-122">Remarks</span></span>

<span data-ttu-id="ece7f-123">Эта функция создает сетку с \_ параметром управляемого создания D3DXMESH и [D3DFVF \_ XYZ D3DFVF с \| \_ нормальным](d3dfvf.md) гибким форматом вершин (фвф).</span><span class="sxs-lookup"><span data-stu-id="ece7f-123">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="ece7f-124">Требования</span><span class="sxs-lookup"><span data-stu-id="ece7f-124">Requirements</span></span>



| <span data-ttu-id="ece7f-125">Требование</span><span class="sxs-lookup"><span data-stu-id="ece7f-125">Requirement</span></span> | <span data-ttu-id="ece7f-126">Значение</span><span class="sxs-lookup"><span data-stu-id="ece7f-126">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ece7f-127">Header</span><span class="sxs-lookup"><span data-stu-id="ece7f-127">Header</span></span><br/>  | <dl> <span data-ttu-id="ece7f-128"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="ece7f-128"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="ece7f-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="ece7f-129">Library</span></span><br/> | <dl> <span data-ttu-id="ece7f-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ece7f-130"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="ece7f-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ece7f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ece7f-132">Функции рисования фигур</span><span class="sxs-lookup"><span data-stu-id="ece7f-132">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
