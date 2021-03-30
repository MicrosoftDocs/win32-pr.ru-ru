---
description: Использует левую систему координат для создания сетки, содержащей цилиндр.
ms.assetid: 54b8a59e-d13f-44cb-84c0-f63c7b1ffb1b
title: Функция D3DXCreateCylinder (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCylinder
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec97755d45b21a85e1a73bbcd2214ee4c1e2358f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "103821141"
---
# <a name="d3dxcreatecylinder-function"></a><span data-ttu-id="1fac9-103">Функция D3DXCreateCylinder</span><span class="sxs-lookup"><span data-stu-id="1fac9-103">D3DXCreateCylinder function</span></span>

<span data-ttu-id="1fac9-104">Использует левую систему координат для создания сетки, содержащей цилиндр.</span><span class="sxs-lookup"><span data-stu-id="1fac9-104">Uses a left-handed coordinate system to create a mesh containing a cylinder.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fac9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1fac9-105">Syntax</span></span>


```C++
HRESULT D3DXCreateCylinder(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             Radius1,
  _In_  FLOAT             Radius2,
  _In_  FLOAT             Length,
  _In_  UINT              Slices,
  _In_  UINT              Stacks,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="1fac9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1fac9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fac9-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fac9-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fac9-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="1fac9-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="1fac9-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с созданной сеткой цилиндра.</span><span class="sxs-lookup"><span data-stu-id="1fac9-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created cylinder mesh.</span></span>

</dd> <dt>

<span data-ttu-id="1fac9-110">*Radius1* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fac9-110">*Radius1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fac9-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fac9-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fac9-112">Радиус в отрицательном конце оси Z.</span><span class="sxs-lookup"><span data-stu-id="1fac9-112">Radius at the negative Z end.</span></span> <span data-ttu-id="1fac9-113">Значение должно быть больше или равно 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="1fac9-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="1fac9-114">*Radius2* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fac9-114">*Radius2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fac9-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fac9-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fac9-116">Радиус в положительном Z-конце.</span><span class="sxs-lookup"><span data-stu-id="1fac9-116">Radius at the positive Z end.</span></span> <span data-ttu-id="1fac9-117">Значение должно быть больше или равно 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="1fac9-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="1fac9-118">*Длина* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fac9-118">*Length* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fac9-119">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fac9-119">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fac9-120">Длина цилиндра вдоль оси z.</span><span class="sxs-lookup"><span data-stu-id="1fac9-120">Length of the cylinder along the z-axis.</span></span>

</dd> <dt>

<span data-ttu-id="1fac9-121">*Срезы* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fac9-121">*Slices* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fac9-122">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fac9-122">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fac9-123">Количество срезов относительно основной оси.</span><span class="sxs-lookup"><span data-stu-id="1fac9-123">Number of slices about the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="1fac9-124">*Стеки* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="1fac9-124">*Stacks* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1fac9-125">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1fac9-125">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1fac9-126">Количество стеков на главной оси.</span><span class="sxs-lookup"><span data-stu-id="1fac9-126">Number of stacks along the main axis.</span></span>

</dd> <dt>

<span data-ttu-id="1fac9-127">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1fac9-127">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fac9-128">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="1fac9-128">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="1fac9-129">Адрес указателя на выходную форму, интерфейс [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="1fac9-129">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="1fac9-130">*ппаджаценци* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="1fac9-130">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fac9-131">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="1fac9-131">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="1fac9-132">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="1fac9-132">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="1fac9-133">Когда метод возвращает значение, этот параметр заполняется массивом из трех DWORD на грань, которые указывают три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="1fac9-133">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="1fac9-134">Можно указать **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="1fac9-134">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fac9-135">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1fac9-135">Return value</span></span>

<span data-ttu-id="1fac9-136">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1fac9-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1fac9-137">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="1fac9-137">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1fac9-138">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="1fac9-138">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fac9-139">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1fac9-139">Remarks</span></span>

<span data-ttu-id="1fac9-140">Созданный цилиндр выравнивается по центру источника, а его ось — по оси z.</span><span class="sxs-lookup"><span data-stu-id="1fac9-140">The created cylinder is centered at the origin, and its axis is aligned with the z-axis.</span></span>

<span data-ttu-id="1fac9-141">Эта функция создает сетку с \_ параметром управляемого создания D3DXMESH и [D3DFVF \_ XYZ D3DFVF с \| \_ нормальным](d3dfvf.md) гибким форматом вершин (фвф).</span><span class="sxs-lookup"><span data-stu-id="1fac9-141">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="1fac9-142">Требования</span><span class="sxs-lookup"><span data-stu-id="1fac9-142">Requirements</span></span>



| <span data-ttu-id="1fac9-143">Требование</span><span class="sxs-lookup"><span data-stu-id="1fac9-143">Requirement</span></span> | <span data-ttu-id="1fac9-144">Значение</span><span class="sxs-lookup"><span data-stu-id="1fac9-144">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fac9-145">Header</span><span class="sxs-lookup"><span data-stu-id="1fac9-145">Header</span></span><br/>  | <dl> <span data-ttu-id="1fac9-146"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fac9-146"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="1fac9-147">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1fac9-147">Library</span></span><br/> | <dl> <span data-ttu-id="1fac9-148"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1fac9-148"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="1fac9-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1fac9-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fac9-150">Функции рисования фигур</span><span class="sxs-lookup"><span data-stu-id="1fac9-150">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
