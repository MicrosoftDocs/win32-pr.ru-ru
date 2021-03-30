---
description: Создает новую сетку исправлений с указанным объявлением вершины.
ms.assetid: cc488cd3-fb38-468f-8aec-17c6ed842582
title: 'Метод ID3DXPatchMesh:: Клонемеш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 249b4282aa84e3f7c5ba619a0b42e8c0b1fdf846
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354323"
---
# <a name="id3dxpatchmeshclonemesh-method"></a><span data-ttu-id="fb3dd-103">Метод ID3DXPatchMesh:: Клонемеш</span><span class="sxs-lookup"><span data-stu-id="fb3dd-103">ID3DXPatchMesh::CloneMesh method</span></span>

<span data-ttu-id="fb3dd-104">Создает новую сетку исправлений с указанным объявлением вершины.</span><span class="sxs-lookup"><span data-stu-id="fb3dd-104">Creates a new patch mesh with the specified vertex declaration.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb3dd-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fb3dd-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDecl,
  [out, retval]       LPD3DXPATCHMESH   *pMesh
);
```



## <a name="parameters"></a><span data-ttu-id="fb3dd-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fb3dd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb3dd-107">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb3dd-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3dd-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="fb3dd-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="fb3dd-109">Сочетание одного или нескольких флагов [**D3DXMESH**](./d3dxmesh.md) , задающих параметры создания для сетки.</span><span class="sxs-lookup"><span data-stu-id="fb3dd-109">Combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags that specify creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="fb3dd-110">*пдекл* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="fb3dd-110">*pDecl* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3dd-111">Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="fb3dd-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="fb3dd-112">Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , задающих формат вершины для вершин в выходной сетке.</span><span class="sxs-lookup"><span data-stu-id="fb3dd-112">Array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements that specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="fb3dd-113">*пмеш* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="fb3dd-113">*pMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="fb3dd-114">Тип: **[ **LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="fb3dd-114">Type: **[**LPD3DXPATCHMESH**](id3dxpatchmesh.md)\***</span></span>

<span data-ttu-id="fb3dd-115">Адрес указателя на интерфейс [**ID3DXPatchMesh**](id3dxpatchmesh.md) , представляющий клонированную сетку.</span><span class="sxs-lookup"><span data-stu-id="fb3dd-115">Address of a pointer to an [**ID3DXPatchMesh**](id3dxpatchmesh.md) interface that represents the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb3dd-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fb3dd-116">Return value</span></span>

<span data-ttu-id="fb3dd-117">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="fb3dd-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="fb3dd-118">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="fb3dd-118">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="fb3dd-119">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="fb3dd-119">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb3dd-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fb3dd-120">Remarks</span></span>

<span data-ttu-id="fb3dd-121">**Клонемеш** Преобразует буфер вершин в новое объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="fb3dd-121">**CloneMesh** converts the vertex buffer to the new vertex declaration.</span></span> <span data-ttu-id="fb3dd-122">Записи в объявлении вершины, которые являются новыми для исходной сетки, имеют значение 0.</span><span class="sxs-lookup"><span data-stu-id="fb3dd-122">Entries in the vertex declaration that are new to the original mesh are set to 0.</span></span> <span data-ttu-id="fb3dd-123">Если текущая сеть имеет соседства, то новая сеть также будет иметь соседства.</span><span class="sxs-lookup"><span data-stu-id="fb3dd-123">If the current mesh has adjacency, the new mesh will also have adjacency.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb3dd-124">Требования</span><span class="sxs-lookup"><span data-stu-id="fb3dd-124">Requirements</span></span>



| <span data-ttu-id="fb3dd-125">Требование</span><span class="sxs-lookup"><span data-stu-id="fb3dd-125">Requirement</span></span> | <span data-ttu-id="fb3dd-126">Значение</span><span class="sxs-lookup"><span data-stu-id="fb3dd-126">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="fb3dd-127">Header</span><span class="sxs-lookup"><span data-stu-id="fb3dd-127">Header</span></span><br/>  | <dl> <span data-ttu-id="fb3dd-128"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="fb3dd-128"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="fb3dd-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="fb3dd-129">Library</span></span><br/> | <dl> <span data-ttu-id="fb3dd-130"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="fb3dd-130"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="fb3dd-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fb3dd-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb3dd-132">ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="fb3dd-132">ID3DXPatchMesh</span></span>](id3dxpatchmesh.md)
</dt> </dl>

 

 
