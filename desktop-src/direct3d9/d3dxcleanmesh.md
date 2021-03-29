---
description: Очищает сетку, подготавливая ее к упрощению.
ms.assetid: 2b586ecc-db87-4b20-a4fc-c8b547bebf65
title: Функция D3DXCleanMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCleanMesh
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5565978dc1ad0e80c33718275ea65080930ce7cf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105647857"
---
# <a name="d3dxcleanmesh-function"></a><span data-ttu-id="197d9-103">Функция D3DXCleanMesh</span><span class="sxs-lookup"><span data-stu-id="197d9-103">D3DXCleanMesh function</span></span>

<span data-ttu-id="197d9-104">Очищает сетку, подготавливая ее к упрощению.</span><span class="sxs-lookup"><span data-stu-id="197d9-104">Cleans a mesh, preparing it for simplification.</span></span>

## <a name="syntax"></a><span data-ttu-id="197d9-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="197d9-105">Syntax</span></span>


```C++
HRESULT D3DXCleanMesh(
  _In_        D3DXCLEANTYPE CleanType,
  _In_        LPD3DXMESH    pMeshIn,
  _In_  const DWORD         *pAdjacencyIn,
  _Out_       LPD3DXMESH    *ppMeshOut,
  _Out_       DWORD         *pAdjacencyOut,
  _Out_       LPD3DXBUFFER  *ppErrorsAndWarnings
);
```



## <a name="parameters"></a><span data-ttu-id="197d9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="197d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="197d9-107">*Клеантипе* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="197d9-107">*CleanType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="197d9-108">Тип: **[ **D3DXCLEANTYPE**](./d3dxcleantype.md)**</span><span class="sxs-lookup"><span data-stu-id="197d9-108">Type: **[**D3DXCLEANTYPE**](./d3dxcleantype.md)**</span></span>

<span data-ttu-id="197d9-109">Операции вершин, выполняемые при подготовке к очистке сетки.</span><span class="sxs-lookup"><span data-stu-id="197d9-109">Vertex operations to perform in preparation for mesh cleaning.</span></span> <span data-ttu-id="197d9-110">См. [**D3DXCLEANTYPE**](./d3dxcleantype.md).</span><span class="sxs-lookup"><span data-stu-id="197d9-110">See [**D3DXCLEANTYPE**](./d3dxcleantype.md).</span></span>

</dd> <dt>

<span data-ttu-id="197d9-111">*пмешин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="197d9-111">*pMeshIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="197d9-112">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)**</span><span class="sxs-lookup"><span data-stu-id="197d9-112">Type: **[**LPD3DXMESH**](id3dxmesh.md)**</span></span>

<span data-ttu-id="197d9-113">Указатель на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий удаляемую сеть.</span><span class="sxs-lookup"><span data-stu-id="197d9-113">Pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="197d9-114">*паджаценциин* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="197d9-114">*pAdjacencyIn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="197d9-115">Тип: **const [**DWORD**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="197d9-115">Type: **const [**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="197d9-116">Указатель на массив из трех DWORD на грань, указывающий три соседа для каждого лица в удаляемой сети.</span><span class="sxs-lookup"><span data-stu-id="197d9-116">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the mesh to be cleaned.</span></span>

</dd> <dt>

<span data-ttu-id="197d9-117">*ппмешаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="197d9-117">*ppMeshOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="197d9-118">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="197d9-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="197d9-119">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий возвращенную очищенную сетку.</span><span class="sxs-lookup"><span data-stu-id="197d9-119">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the returned cleaned mesh.</span></span> <span data-ttu-id="197d9-120">Возвращается та же сетка, которая была передана, если очистка не была выполнена.</span><span class="sxs-lookup"><span data-stu-id="197d9-120">The same mesh is returned that was passed in if no cleaning was necessary.</span></span>

</dd> <dt>

<span data-ttu-id="197d9-121">*паджаценциаут* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="197d9-121">*pAdjacencyOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="197d9-122">Тип: **[ **DWORD**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="197d9-122">Type: **[**DWORD**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="197d9-123">Указатель на массив из трех DWORD на грань, который указывает три соседа для каждой грани в сетке выходных данных.</span><span class="sxs-lookup"><span data-stu-id="197d9-123">Pointer to an array of three DWORDs per face that specify the three neighbors for each face in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="197d9-124">*пперрорсандварнингс* \[ заполняет\]</span><span class="sxs-lookup"><span data-stu-id="197d9-124">*ppErrorsAndWarnings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="197d9-125">Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***</span><span class="sxs-lookup"><span data-stu-id="197d9-125">Type: **[**LPD3DXBUFFER**](id3dxbuffer.md)\***</span></span>

<span data-ttu-id="197d9-126">Возвращает буфер, содержащий строку ошибок и предупреждений, в которых объясняются проблемы, обнаруженные в сетке.</span><span class="sxs-lookup"><span data-stu-id="197d9-126">Returns a buffer containing a string of errors and warnings, which explain the problems found in the mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="197d9-127">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="197d9-127">Return value</span></span>

<span data-ttu-id="197d9-128">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="197d9-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="197d9-129">Если функция выполнена успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="197d9-129">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="197d9-130">Если функция завершается ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="197d9-130">If the function fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="197d9-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="197d9-131">Remarks</span></span>

<span data-ttu-id="197d9-132">Эта функция очищает сетку с помощью метода очистки и параметров, указанных в параметре Клеантипе.</span><span class="sxs-lookup"><span data-stu-id="197d9-132">This function cleans a mesh using the cleaning method and options specified in the CleanType parameter.</span></span> <span data-ttu-id="197d9-133">Описание доступных параметров см. в описании перечисления [**D3DXCLEANTYPE**](./d3dxcleantype.md) .</span><span class="sxs-lookup"><span data-stu-id="197d9-133">See the [**D3DXCLEANTYPE**](./d3dxcleantype.md) enumeration for a description of the available options.</span></span>

## <a name="requirements"></a><span data-ttu-id="197d9-134">Требования</span><span class="sxs-lookup"><span data-stu-id="197d9-134">Requirements</span></span>



| <span data-ttu-id="197d9-135">Требование</span><span class="sxs-lookup"><span data-stu-id="197d9-135">Requirement</span></span> | <span data-ttu-id="197d9-136">Значение</span><span class="sxs-lookup"><span data-stu-id="197d9-136">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="197d9-137">Header</span><span class="sxs-lookup"><span data-stu-id="197d9-137">Header</span></span><br/>  | <dl> <span data-ttu-id="197d9-138"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="197d9-138"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="197d9-139">Библиотека</span><span class="sxs-lookup"><span data-stu-id="197d9-139">Library</span></span><br/> | <dl> <span data-ttu-id="197d9-140"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="197d9-140"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="197d9-141">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="197d9-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="197d9-142">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="197d9-142">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
