---
description: Использует левую систему координат для создания сетки, содержащей Торус.
ms.assetid: 68df7650-8a87-4762-8b57-5704c419b0d7
title: Функция D3DXCreateTorus (D3dx9shape. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateTorus
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 384950ca1f00d0115135cf9ae36a2883ec5470e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273784"
---
# <a name="d3dxcreatetorus-function"></a><span data-ttu-id="0ff94-103">Функция D3DXCreateTorus</span><span class="sxs-lookup"><span data-stu-id="0ff94-103">D3DXCreateTorus function</span></span>

<span data-ttu-id="0ff94-104">Использует левую систему координат для создания сетки, содержащей Торус.</span><span class="sxs-lookup"><span data-stu-id="0ff94-104">Uses a left-handed coordinate system to create a mesh containing a torus.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ff94-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ff94-105">Syntax</span></span>


```C++
HRESULT D3DXCreateTorus(
  _In_  LPDIRECT3DDEVICE9 pDevice,
  _In_  FLOAT             InnerRadius,
  _In_  FLOAT             OuterRadius,
  _In_  UINT              Sides,
  _In_  UINT              Rings,
  _Out_ LPD3DXMESH        *ppMesh,
  _Out_ LPD3DXBUFFER      *ppAdjacency
);
```



## <a name="parameters"></a><span data-ttu-id="0ff94-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ff94-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ff94-107">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ff94-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff94-108">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="0ff94-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="0ff94-109">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий устройство, связанное с созданной сеткой Торус.</span><span class="sxs-lookup"><span data-stu-id="0ff94-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the created torus mesh.</span></span>

</dd> <dt>

<span data-ttu-id="0ff94-110">*Иннеррадиус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ff94-110">*InnerRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff94-111">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ff94-111">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ff94-112">Внутренний радиус Торус.</span><span class="sxs-lookup"><span data-stu-id="0ff94-112">Inner-radius of the torus.</span></span> <span data-ttu-id="0ff94-113">Значение должно быть больше или равно 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0ff94-113">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="0ff94-114">*Аутеррадиус* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ff94-114">*OuterRadius* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff94-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ff94-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ff94-116">Внешний радиус Торус.</span><span class="sxs-lookup"><span data-stu-id="0ff94-116">Outer-radius of the torus.</span></span> <span data-ttu-id="0ff94-117">Значение должно быть больше или равно 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0ff94-117">Value should be greater than or equal to 0.0f.</span></span>

</dd> <dt>

<span data-ttu-id="0ff94-118">*Стороны* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ff94-118">*Sides* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff94-119">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ff94-119">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ff94-120">Количество сторон в перекрестном разделе.</span><span class="sxs-lookup"><span data-stu-id="0ff94-120">Number of sides in a cross-section.</span></span> <span data-ttu-id="0ff94-121">Значение должно быть больше или равно 3.</span><span class="sxs-lookup"><span data-stu-id="0ff94-121">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="0ff94-122">*Колец* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="0ff94-122">*Rings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff94-123">Тип: **[ **uint**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0ff94-123">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0ff94-124">Число колец, составляющих Торус.</span><span class="sxs-lookup"><span data-stu-id="0ff94-124">Number of rings making up the torus.</span></span> <span data-ttu-id="0ff94-125">Значение должно быть больше или равно 3.</span><span class="sxs-lookup"><span data-stu-id="0ff94-125">Value must be greater than or equal to 3.</span></span>

</dd> <dt>

<span data-ttu-id="0ff94-126">*ппмеш* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0ff94-126">*ppMesh* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff94-127">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ff94-127">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="0ff94-128">Адрес указателя на выходную форму, интерфейс [**ID3DXMesh**](id3dxmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="0ff94-128">Address of a pointer to the output shape, an [**ID3DXMesh**](id3dxmesh.md) interface.</span></span>

</dd> <dt>

<span data-ttu-id="0ff94-129">*ппаджаценци* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="0ff94-129">*ppAdjacency* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0ff94-130">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="0ff94-130">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="0ff94-131">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="0ff94-131">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="0ff94-132">Когда метод возвращает значение, этот параметр заполняется массивом из трех DWORD на грань, которые указывают три соседа для каждой грани в сети.</span><span class="sxs-lookup"><span data-stu-id="0ff94-132">When the method returns, this parameter is filled with an array of three DWORDs per face that specify the three neighbors for each face in the mesh.</span></span> <span data-ttu-id="0ff94-133">Можно указать **значение NULL** .</span><span class="sxs-lookup"><span data-stu-id="0ff94-133">**NULL** can be specified.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ff94-134">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ff94-134">Return value</span></span>

<span data-ttu-id="0ff94-135">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0ff94-135">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0ff94-136">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="0ff94-136">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="0ff94-137">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="0ff94-137">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ff94-138">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ff94-138">Remarks</span></span>

<span data-ttu-id="0ff94-139">Созданный Торус выравнивается по центру источника, а его ось — по оси z.</span><span class="sxs-lookup"><span data-stu-id="0ff94-139">The created torus is centered at the origin, and its axis is aligned with the z-axis.</span></span> <span data-ttu-id="0ff94-140">Внутренний радиус торуса — это радиус перекрестной секции (дополнительный радиус), а внешний радиус Торус — радиус центрального отверстия.</span><span class="sxs-lookup"><span data-stu-id="0ff94-140">The inner radius of the torus is the radius of the cross-section (the minor radius), and the outer radius of the torus is the radius of the central hole.</span></span>

<span data-ttu-id="0ff94-141">Эта функция возвращает сетку, которую можно использовать позже для рисования или обработки приложением.</span><span class="sxs-lookup"><span data-stu-id="0ff94-141">This function returns a mesh that can be used later for drawing or manipulation by the application.</span></span>

<span data-ttu-id="0ff94-142">Эта функция создает сетку с \_ параметром управляемого создания D3DXMESH и [D3DFVF \_ XYZ D3DFVF с \| \_ нормальным](d3dfvf.md) гибким форматом вершин (фвф).</span><span class="sxs-lookup"><span data-stu-id="0ff94-142">This function creates a mesh with the D3DXMESH\_MANAGED creation option and [D3DFVF\_XYZ \| D3DFVF\_NORMAL](d3dfvf.md) flexible vertex format (FVF).</span></span>

## <a name="requirements"></a><span data-ttu-id="0ff94-143">Требования</span><span class="sxs-lookup"><span data-stu-id="0ff94-143">Requirements</span></span>



| <span data-ttu-id="0ff94-144">Требование</span><span class="sxs-lookup"><span data-stu-id="0ff94-144">Requirement</span></span> | <span data-ttu-id="0ff94-145">Значение</span><span class="sxs-lookup"><span data-stu-id="0ff94-145">Value</span></span> |
|--------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ff94-146">Header</span><span class="sxs-lookup"><span data-stu-id="0ff94-146">Header</span></span><br/>  | <dl> <span data-ttu-id="0ff94-147"><dt>D3dx9shape. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ff94-147"><dt>D3dx9shape.h</dt></span></span> </dl> |
| <span data-ttu-id="0ff94-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="0ff94-148">Library</span></span><br/> | <dl> <span data-ttu-id="0ff94-149"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0ff94-149"><dt>D3dx9.lib</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0ff94-150">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ff94-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ff94-151">Функции рисования фигур</span><span class="sxs-lookup"><span data-stu-id="0ff94-151">Shape Drawing Functions</span></span>](dx9-graphics-reference-d3dx-functions-shape.md)
</dt> </dl>

 

 
