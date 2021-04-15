---
description: Создает объект ID3DXPRTEngine, который может эффективно создавать предварительно вычисленные имитации радианце перемещения (PRT) трехмерной сцены.
ms.assetid: fdfe02b5-03fb-4bee-a53b-012ae3572644
title: Функция D3DXCreatePRTEngine (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreatePRTEngine
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 7b76b58953de81041922659c3315bba9cdf7788b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104547930"
---
# <a name="d3dxcreateprtengine-function"></a><span data-ttu-id="14757-103">Функция D3DXCreatePRTEngine</span><span class="sxs-lookup"><span data-stu-id="14757-103">D3DXCreatePRTEngine function</span></span>

<span data-ttu-id="14757-104">Создает объект [**ID3DXPRTEngine**](id3dxprtengine.md) , который может эффективно создавать предварительно вычисленные имитации радианце перемещения (PRT) трехмерной сцены.</span><span class="sxs-lookup"><span data-stu-id="14757-104">Creates an [**ID3DXPRTEngine**](id3dxprtengine.md) object that can efficiently generate precomputed radiance transfer (PRT) simulations of a 3D scene.</span></span>

## <a name="syntax"></a><span data-ttu-id="14757-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="14757-105">Syntax</span></span>


```C++
HRESULT D3DXCreatePRTEngine(
  _In_    LPD3DXMESH      pMesh,
  _In_    DWORD           *pAdjacency,
  _In_    BOOL            ExtractUVs,
  _In_    LPD3DXMESH      pBlockerMesh,
  _Inout_ LPD3DXPRTENGINE ppEngine
);
```



## <a name="parameters"></a><span data-ttu-id="14757-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="14757-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14757-107">*пмеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14757-107">*pMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14757-108">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="14757-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="14757-109">Указатель на входной объект сетки [**ID3DXMesh**](id3dxmesh.md) , моделирующий трехмерную сцену.</span><span class="sxs-lookup"><span data-stu-id="14757-109">Pointer to an input [**ID3DXMesh**](id3dxmesh.md) mesh object that models the 3D scene.</span></span> <span data-ttu-id="14757-110">Эта сеть должна иметь таблицу атрибутов, в которой вершины находятся в уникальном атрибуте.</span><span class="sxs-lookup"><span data-stu-id="14757-110">This mesh must have an attribute table in which vertices are in a unique attribute.</span></span>

</dd> <dt>

<span data-ttu-id="14757-111">*паджаценци* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14757-111">*pAdjacency* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14757-112">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="14757-112">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="14757-113">Необязательный указатель на массив из трех DWORD на лицо, заполняемый смежными индексами граней.</span><span class="sxs-lookup"><span data-stu-id="14757-113">Optional pointer to an array of three DWORDs per face to be filled with adjacent face indices.</span></span> <span data-ttu-id="14757-114">Число байтов в этом массиве должно быть не меньше ((3 \* [**жетнумфацес**](id3dxbasemesh--getnumfaces.md)) \* sizeof (DWORD)).</span><span class="sxs-lookup"><span data-stu-id="14757-114">The number of bytes in this array must be at least ((3 \* [**GetNumFaces**](id3dxbasemesh--getnumfaces.md)) \* sizeof(DWORD)).</span></span> <span data-ttu-id="14757-115">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="14757-115">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="14757-116">*Екстрактувс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14757-116">*ExtractUVs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14757-117">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14757-117">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14757-118">Если **значение — true**, текстуры будут использоваться для хранения векторов АЛБЕДОС или PRT.</span><span class="sxs-lookup"><span data-stu-id="14757-118">If **TRUE**, textures will be used to store albedos or PRT vectors.</span></span>

</dd> <dt>

<span data-ttu-id="14757-119">*пблоккермеш* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="14757-119">*pBlockerMesh* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="14757-120">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="14757-120">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="14757-121">Указатель на необязательный объект сетки [**ID3DXMesh**](id3dxmesh.md) , который блокирует трехмерную сцену.</span><span class="sxs-lookup"><span data-stu-id="14757-121">Pointer to an optional [**ID3DXMesh**](id3dxmesh.md) mesh object that blocks the 3D scene.</span></span> <span data-ttu-id="14757-122">Может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="14757-122">May be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="14757-123">*ппенгине* \[ в, out\]</span><span class="sxs-lookup"><span data-stu-id="14757-123">*ppEngine* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="14757-124">Тип: **[ **LPD3DXPRTENGINE**](id3dxprtengine.md)**</span><span class="sxs-lookup"><span data-stu-id="14757-124">Type: **[**LPD3DXPRTENGINE**](id3dxprtengine.md)**</span></span>

<span data-ttu-id="14757-125">Указатель на выходной объект [**ID3DXPRTEngine**](id3dxprtengine.md) .</span><span class="sxs-lookup"><span data-stu-id="14757-125">Pointer to an output [**ID3DXPRTEngine**](id3dxprtengine.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14757-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="14757-126">Return value</span></span>

<span data-ttu-id="14757-127">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14757-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14757-128">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="14757-128">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="14757-129">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="14757-129">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="14757-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="14757-130">Remarks</span></span>

<span data-ttu-id="14757-131">Используйте [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) для объединения нескольких сеток в один интерфейс сетки.</span><span class="sxs-lookup"><span data-stu-id="14757-131">Use [**D3DXConcatenateMeshes**](d3dxconcatenatemeshes.md) to combine multiple meshes into a single mesh interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="14757-132">Требования</span><span class="sxs-lookup"><span data-stu-id="14757-132">Requirements</span></span>



| <span data-ttu-id="14757-133">Требование</span><span class="sxs-lookup"><span data-stu-id="14757-133">Requirement</span></span> | <span data-ttu-id="14757-134">Значение</span><span class="sxs-lookup"><span data-stu-id="14757-134">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="14757-135">Header</span><span class="sxs-lookup"><span data-stu-id="14757-135">Header</span></span><br/>  | <dl> <span data-ttu-id="14757-136"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="14757-136"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="14757-137">Библиотека</span><span class="sxs-lookup"><span data-stu-id="14757-137">Library</span></span><br/> | <dl> <span data-ttu-id="14757-138"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="14757-138"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="14757-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="14757-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14757-140">Предварительно вычисленные функции пересылки Радианце</span><span class="sxs-lookup"><span data-stu-id="14757-140">Precomputed Radiance Transfer Functions</span></span>](dx9-graphics-reference-d3dx-functions-prt.md)
</dt> </dl>

 

 
