---
description: Создает точную копию сетки с помощью декларатора.
ms.assetid: 47e0329a-ea85-478d-af8b-cf85d2a779f6
title: 'Метод ID3DXBaseMesh:: Клонемеш (D3DX9Mesh. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh.CloneMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 421b72a080564886a10c187594223fb58a0b69fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703760"
---
# <a name="id3dxbasemeshclonemesh-method"></a><span data-ttu-id="af042-103">Метод ID3DXBaseMesh:: Клонемеш</span><span class="sxs-lookup"><span data-stu-id="af042-103">ID3DXBaseMesh::CloneMesh method</span></span>

<span data-ttu-id="af042-104">Создает точную копию сетки с помощью декларатора.</span><span class="sxs-lookup"><span data-stu-id="af042-104">Clones a mesh using a declarator.</span></span>

## <a name="syntax"></a><span data-ttu-id="af042-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af042-105">Syntax</span></span>


```C++
HRESULT CloneMesh(
  [in]                DWORD             Options,
  [in]          const D3DVERTEXELEMENT9 *pDeclaration,
  [in]                LPDIRECT3DDEVICE9 pDevice,
  [out, retval]       LPD3DXMESH        *ppCloneMesh
);
```



## <a name="parameters"></a><span data-ttu-id="af042-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="af042-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="af042-107">*Параметры* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af042-107">*Options* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af042-108">Тип: **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="af042-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="af042-109">Сочетание одного или нескольких флагов [**D3DXMESH**](./d3dxmesh.md) , задающее параметры создания для сетки.</span><span class="sxs-lookup"><span data-stu-id="af042-109">A combination of one or more [**D3DXMESH**](./d3dxmesh.md) flags specifying creation options for the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="af042-110">*пдекларатион* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af042-110">*pDeclaration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af042-111">Тип: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) \***</span><span class="sxs-lookup"><span data-stu-id="af042-111">Type: **const [**D3DVERTEXELEMENT9**](d3dvertexelement9.md)\***</span></span>

<span data-ttu-id="af042-112">Массив элементов [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) , задающих формат вершины для вершин в выходной сетке.</span><span class="sxs-lookup"><span data-stu-id="af042-112">An array of [**D3DVERTEXELEMENT9**](d3dvertexelement9.md) elements, which specify the vertex format for the vertices in the output mesh.</span></span>

</dd> <dt>

<span data-ttu-id="af042-113">*пдевице* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="af042-113">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="af042-114">Тип: **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="af042-114">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="af042-115">Указатель на интерфейс [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) , представляющий объект устройства, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="af042-115">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device object associated with the mesh.</span></span>

</dd> <dt>

<span data-ttu-id="af042-116">*ппклонемеш* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="af042-116">*ppCloneMesh* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="af042-117">Тип: **[ **LPD3DXMESH**](id3dxmesh.md)\***</span><span class="sxs-lookup"><span data-stu-id="af042-117">Type: **[**LPD3DXMESH**](id3dxmesh.md)\***</span></span>

<span data-ttu-id="af042-118">Адрес указателя на интерфейс [**ID3DXMesh**](id3dxmesh.md) , представляющий клонированную сетку.</span><span class="sxs-lookup"><span data-stu-id="af042-118">Address of a pointer to an [**ID3DXMesh**](id3dxmesh.md) interface, representing the cloned mesh.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="af042-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af042-119">Return value</span></span>

<span data-ttu-id="af042-120">Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="af042-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="af042-121">Если метод выполнен успешно, возвращается значение D3D \_ ОК.</span><span class="sxs-lookup"><span data-stu-id="af042-121">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="af042-122">В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.</span><span class="sxs-lookup"><span data-stu-id="af042-122">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="af042-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af042-123">Remarks</span></span>

<span data-ttu-id="af042-124">**ID3DXBaseMesh:: клонемеш** используется для переформатирования и изменения макета данных вершин.</span><span class="sxs-lookup"><span data-stu-id="af042-124">**ID3DXBaseMesh::CloneMesh** is used to reformat and change the vertex data layout.</span></span> <span data-ttu-id="af042-125">Это делается путем создания нового объекта сетки.</span><span class="sxs-lookup"><span data-stu-id="af042-125">This is done by creating a new mesh object.</span></span> <span data-ttu-id="af042-126">Например, используйте его для добавления пространства для нормалей, текстурных координат, цветов, весов и т. д., которые отсутствовали ранее.</span><span class="sxs-lookup"><span data-stu-id="af042-126">For example, use it to add space for normals, texture coordinates, colors, weights, etc. that were not present before.</span></span>

<span data-ttu-id="af042-127">[**ID3DXBaseMesh:: упдатесемантикс**](id3dxbasemesh--updatesemantics.md) обновляет объявление вершины с другой семантической информацией без изменения макета буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="af042-127">[**ID3DXBaseMesh::UpdateSemantics**](id3dxbasemesh--updatesemantics.md) updates the vertex declaration with different semantic information without changing the layout of the vertex buffer.</span></span> <span data-ttu-id="af042-128">Этот метод не изменяет содержимое буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="af042-128">This method does not modify the contents of the vertex buffer.</span></span> <span data-ttu-id="af042-129">Например, используйте его, чтобы переметить координату трехмерной текстуры как бинормал или тангенс или наоборот.</span><span class="sxs-lookup"><span data-stu-id="af042-129">For example, use it to relabel a 3D texture coordinate as a binormal or tangent or vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="af042-130">Требования</span><span class="sxs-lookup"><span data-stu-id="af042-130">Requirements</span></span>



| <span data-ttu-id="af042-131">Требование</span><span class="sxs-lookup"><span data-stu-id="af042-131">Requirement</span></span> | <span data-ttu-id="af042-132">Значение</span><span class="sxs-lookup"><span data-stu-id="af042-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="af042-133">Header</span><span class="sxs-lookup"><span data-stu-id="af042-133">Header</span></span><br/>  | <dl> <span data-ttu-id="af042-134"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="af042-134"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="af042-135">Библиотека</span><span class="sxs-lookup"><span data-stu-id="af042-135">Library</span></span><br/> | <dl> <span data-ttu-id="af042-136"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="af042-136"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="af042-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="af042-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="af042-138">ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="af042-138">ID3DXBaseMesh</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="af042-139">**ID3DXBaseMesh:: Клонемешфвф**</span><span class="sxs-lookup"><span data-stu-id="af042-139">**ID3DXBaseMesh::CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)
</dt> <dt>

[<span data-ttu-id="af042-140">**D3DXDeclaratorFromFVF**</span><span class="sxs-lookup"><span data-stu-id="af042-140">**D3DXDeclaratorFromFVF**</span></span>](d3dxdeclaratorfromfvf.md)
</dt> </dl>

 

 
