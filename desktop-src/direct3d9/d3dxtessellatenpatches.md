---
description: Тесселяция заданной сетки с помощью схемы тесселяции N-patch.
ms.assetid: e804905d-ee0b-484f-a621-58b197bd370b
title: Функция D3DXTessellateNPatches (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXTessellateNPatches
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c8811816447deb858b5c8b42d651d219f06fef5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713607"
---
# <a name="d3dxtessellatenpatches-function"></a><span data-ttu-id="99bd2-103">Функция D3DXTessellateNPatches</span><span class="sxs-lookup"><span data-stu-id="99bd2-103">D3DXTessellateNPatches function</span></span>

<span data-ttu-id="99bd2-104">Тесселяция заданной сетки с помощью схемы тесселяции N-patch.</span><span class="sxs-lookup"><span data-stu-id="99bd2-104">Tessellates the given mesh using the N-patch tessellation scheme.</span></span>

## <a name="syntax"></a><span data-ttu-id="99bd2-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="99bd2-105">Syntax</span></span>


```C++
HRESULT D3DXTessellateNPatches(
  _In_        LPD3DXMESH   pMeshIn,
  _In_  const CONST DWORD  *pAdjacencyIn,
  _In_        FLOAT        NumSegs,
  _In_        BOOL         QuadraticInterpNormals,
  _Out_       LPD3DXMESH   *ppMeshOut,
  _Out_       LPD3DXBUFFER *ppAdjacencyOut
);
```



## <a name="parameters"></a><span data-ttu-id="99bd2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="99bd2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="99bd2-107">*пмешин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="99bd2-107">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99bd2-108">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="99bd2-108">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="99bd2-109">Указатель на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий сетку для тесселяции.</span><span class="sxs-lookup"><span data-stu-id="99bd2-109">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="99bd2-110">*паджаценциин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="99bd2-110">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99bd2-111">Тип: **CONST const DWORD \***</span><span class="sxs-lookup"><span data-stu-id="99bd2-111">Type: **const CONST DWORD\***</span></span>

<span data-ttu-id="99bd2-112">Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в исходной сетке.</span><span class="sxs-lookup"><span data-stu-id="99bd2-112">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the source mesh.</span></span> <span data-ttu-id="99bd2-113">Этот параметр может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="99bd2-113">This parameter may be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="99bd2-114">*Нумсегс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="99bd2-114">*NumSegs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99bd2-115">Тип: **[ **float**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99bd2-115">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99bd2-116">Число сегментов на границе для тесселяции.</span><span class="sxs-lookup"><span data-stu-id="99bd2-116">Number of segments per edge to tessellate.</span></span>

</dd> <dt>

<span data-ttu-id="99bd2-117">*КуадратиЦинтерпнормалс* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="99bd2-117">*QuadraticInterpNormals* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="99bd2-118">Тип: **[ **bool** .](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="99bd2-118">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="99bd2-119">Задайте значение **true** , чтобы использовать квадратичную интерполяцию для обычных. Задайте значение **false** для линейной интерполяции.</span><span class="sxs-lookup"><span data-stu-id="99bd2-119">Set to **TRUE** to use quadratic interpolation for normals; set to **FALSE** for linear interpolation.</span></span>

</dd> <dt>

<span data-ttu-id="99bd2-120">*ппмешаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="99bd2-120">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99bd2-121">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="99bd2-121">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="99bd2-122">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий возвращаемую тесселяцию сетку.</span><span class="sxs-lookup"><span data-stu-id="99bd2-122">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned tessellated mesh.</span></span>

</dd> <dt>

<span data-ttu-id="99bd2-123">*ппаджаценциаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="99bd2-123">*ppAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="99bd2-124">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="99bd2-124">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="99bd2-125">Адрес указателя на интерфейс [**ID3DXBuffer**](id3dxbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="99bd2-125">Address of a pointer to an [**ID3DXBuffer**](id3dxbuffer.md) interface.</span></span> <span data-ttu-id="99bd2-126">Если значение этого параметра не равно **null**, этот буфер будет содержать массив из трех DWORD на грань, задающих три соседи для каждой грани в выходной сетке.</span><span class="sxs-lookup"><span data-stu-id="99bd2-126">If the value of this parameter is not set to **NULL**, this buffer will contain an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span> <span data-ttu-id="99bd2-127">Этот параметр может иметь **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="99bd2-127">This parameter may be **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="99bd2-128">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="99bd2-128">Return value</span></span>

<span data-ttu-id="99bd2-129">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="99bd2-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="99bd2-130">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="99bd2-130">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="99bd2-131">Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="99bd2-131">If the function fails, the return value can be one of the following values: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="99bd2-132">Комментарии</span><span class="sxs-lookup"><span data-stu-id="99bd2-132">Remarks</span></span>

<span data-ttu-id="99bd2-133">Эта функция тесселяциа с помощью алгоритма N-patch.</span><span class="sxs-lookup"><span data-stu-id="99bd2-133">This function tessellates by using the N-patch algorithm.</span></span>

## <a name="requirements"></a><span data-ttu-id="99bd2-134">Требования</span><span class="sxs-lookup"><span data-stu-id="99bd2-134">Requirements</span></span>



| <span data-ttu-id="99bd2-135">Требование</span><span class="sxs-lookup"><span data-stu-id="99bd2-135">Requirement</span></span> | <span data-ttu-id="99bd2-136">Значение</span><span class="sxs-lookup"><span data-stu-id="99bd2-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="99bd2-137">Header</span><span class="sxs-lookup"><span data-stu-id="99bd2-137">Header</span></span><br/>  | <dl> <span data-ttu-id="99bd2-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="99bd2-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="99bd2-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="99bd2-139">Library</span></span><br/> | <dl> <span data-ttu-id="99bd2-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="99bd2-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="99bd2-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="99bd2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="99bd2-142">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="99bd2-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
