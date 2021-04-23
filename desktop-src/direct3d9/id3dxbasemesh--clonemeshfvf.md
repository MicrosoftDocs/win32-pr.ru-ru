---
description: Создает точную копию сетки, используя код гибкого формата вершин (ФВФ).
ms.assetid: b7d23ea9-1a2f-46e3-bcb5-82040d2a1e12
title: 'Метод ID3DXBaseMesh:: Клонемешфвф (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMeshFVF
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 4cb3b0ad33e54e79464949f441842173fb48a180
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703759"
---
# <a name="id3dxbasemeshclonemeshfvf-method"></a><span data-ttu-id="e344a-103">Метод ID3DXBaseMesh:: Клонемешфвф</span><span class="sxs-lookup"><span data-stu-id="e344a-103">ID3DXBaseMesh::CloneMeshFVF method</span></span>

<span data-ttu-id="e344a-104">Создает точную копию сетки, используя код гибкого формата вершин (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="e344a-104">Clones a mesh using a flexible vertex format (FVF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="e344a-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e344a-105">Syntax</span></span>


```C++
HRESULT CloneMeshFVF(
  [in]          DWORD             Options,
  [in]          DWORD             FVF,
  [in]          LPDIRECT3DDEVICE9 pDevice,
  [out, retval] LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="e344a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="e344a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e344a-107">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e344a-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e344a-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e344a-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e344a-109">Сочетание одного или нескольких флагов [**D3DXMESH**](./d3dxmesh.md) , задающее параметры создания для сетки.</span><span class="sxs-lookup"><span data-stu-id="e344a-109">A combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e344a-110">*Фвф* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e344a-110">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e344a-111">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e344a-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e344a-112">Сочетание кодов ФВФ, определяющих формат вершины для вершин в выходной сетке.</span><span class="sxs-lookup"><span data-stu-id="e344a-112">Combination of FVF codes, which specifies the vertex format for the vertices in the output mesh.</span></span> <span data-ttu-id="e344a-113">Значения кодов см. в разделе [D3DFVF](d3dfvf.md).</span><span class="sxs-lookup"><span data-stu-id="e344a-113">For the values of the codes, see [D3DFVF](d3dfvf.md).</span></span>

</dd> <dt>

<span data-ttu-id="e344a-114">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="e344a-114">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e344a-115">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="e344a-115">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="e344a-116">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий объект устройства, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="e344a-116">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface representing the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="e344a-117">*ппклонемеш* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="e344a-117">*ppCloneMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="e344a-118">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="e344a-118">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="e344a-119">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий клонированную сетку.</span><span class="sxs-lookup"><span data-stu-id="e344a-119">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e344a-120">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e344a-120">Return value</span></span>

<span data-ttu-id="e344a-121">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e344a-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e344a-122">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="e344a-122">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e344a-123">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="e344a-123">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="e344a-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e344a-124">Remarks</span></span>

<span data-ttu-id="e344a-125">**ID3DXBaseMesh:: клонемешфвф** используется для переформатирования и изменения макета данных вершин.</span><span class="sxs-lookup"><span data-stu-id="e344a-125">**ID3DXBaseMesh::CloneMeshFVF** is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="e344a-126">Это делается путем создания нового объекта сетки.</span><span class="sxs-lookup"><span data-stu-id="e344a-126">This is done by creating a new mesh object.</span></span> <span data-ttu-id="e344a-127">Например, используйте его для добавления пространства для нормалей, текстурных координат, цветов, весов и т. д., которые отсутствовали ранее.</span><span class="sxs-lookup"><span data-stu-id="e344a-127">For example, use it to to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="e344a-128">[**ID3DXBaseMesh:: упдатесемантикс**](id3dxbasemesh--updatesemantics.md) обновляет объявление вершины с другой семантической информацией без изменения макета буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="e344a-128">[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) updates the vertex declaration with different semantic information without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="e344a-129">Этот метод не изменяет содержимое буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="e344a-129">This method does not modify the contents of the vertex buffer.</span></span> <span data-ttu-id="e344a-130">Например, используйте его, чтобы переметить координату трехмерной текстуры как бинормал или тангенс или наоборот.</span><span class="sxs-lookup"><span data-stu-id="e344a-130">For example, use it to relabel a 3D texture coordinate as a binormal or tangent or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="e344a-131">Требования</span><span class="sxs-lookup"><span data-stu-id="e344a-131">Requirements</span></span>



| <span data-ttu-id="e344a-132">Требование</span><span class="sxs-lookup"><span data-stu-id="e344a-132">Requirement</span></span> | <span data-ttu-id="e344a-133">Значение</span><span class="sxs-lookup"><span data-stu-id="e344a-133">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e344a-134">Header</span><span class="sxs-lookup"><span data-stu-id="e344a-134">Header</span></span><br/>  | <dl> <span data-ttu-id="e344a-135"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="e344a-135"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="e344a-136">Библиотека</span><span class="sxs-lookup"><span data-stu-id="e344a-136">Library</span></span><br/> | <dl> <span data-ttu-id="e344a-137"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="e344a-137"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e344a-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e344a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e344a-139">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="e344a-139">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="e344a-140">**D3DXFVFFromDeclarator**</span><span class="sxs-lookup"><span data-stu-id="e344a-140">**D3DXFVFFromDeclarator**</span></span>](d3dxfvffromdeclarator.md)
</dt> </dl>

 

 
