---
description: Буфер сетки — это буфер, содержащий данные о сетке.
ms.assetid: a9fdfa22-531d-4da0-89f0-8766c2635e20
title: Интерфейс ID3DX10MeshBuffer (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10MeshBuffer
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 42076393c3be5443688ec4db954131935b62f696
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105651551"
---
# <a name="id3dx10meshbuffer-interface"></a><span data-ttu-id="52622-103">Интерфейс ID3DX10MeshBuffer</span><span class="sxs-lookup"><span data-stu-id="52622-103">ID3DX10MeshBuffer interface</span></span>

<span data-ttu-id="52622-104">Буфер сетки — это буфер, содержащий данные о сетке.</span><span class="sxs-lookup"><span data-stu-id="52622-104">A mesh buffer is a buffer that contains data about a mesh.</span></span> <span data-ttu-id="52622-105">Он может содержать один из пяти различных типов данных: данные вершин, индексные данные, соседство, данные атрибутов или данные-контейнеры.</span><span class="sxs-lookup"><span data-stu-id="52622-105">It can contain one of five different types of data: vertex data, index data, adjacency data, attribute data, or point rep data.</span></span> <span data-ttu-id="52622-106">Эта структура используется для доступа к этим пяти фрагментам данных с помощью следующих пяти API: [**ID3DX10Mesh:: жетвертексбуффер**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh:: жетиндексбуффер**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh:: Жетаджаценцибуффер**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh:: жетаттрибутебуффер**](id3dx10mesh-getattributebuffer.md)или [**ID3DX10Mesh:: жетпоинтрепбуффер**](id3dx10mesh-getpointrepbuffer.md).</span><span class="sxs-lookup"><span data-stu-id="52622-106">The structure is used to access these five pieces of data through the following five APIs: [**ID3DX10Mesh::GetVertexBuffer**](id3dx10mesh-getvertexbuffer.md), [**ID3DX10Mesh::GetIndexBuffer**](id3dx10mesh-getindexbuffer.md), [**ID3DX10Mesh::GetAdjacencyBuffer**](id3dx10mesh-getadjacencybuffer.md), [**ID3DX10Mesh::GetAttributeBuffer**](id3dx10mesh-getattributebuffer.md), or [**ID3DX10Mesh::GetPointRepBuffer**](id3dx10mesh-getpointrepbuffer.md).</span></span>

## <a name="members"></a><span data-ttu-id="52622-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="52622-107">Members</span></span>

<span data-ttu-id="52622-108">Интерфейс **ID3DX10MeshBuffer** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="52622-108">The **ID3DX10MeshBuffer** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="52622-109">**ID3DX10MeshBuffer** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="52622-109">**ID3DX10MeshBuffer** also has these types of members:</span></span>

-   [<span data-ttu-id="52622-110">Методы</span><span class="sxs-lookup"><span data-stu-id="52622-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="52622-111">Методы</span><span class="sxs-lookup"><span data-stu-id="52622-111">Methods</span></span>

<span data-ttu-id="52622-112">Интерфейс **ID3DX10MeshBuffer** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="52622-112">The **ID3DX10MeshBuffer** interface has these methods.</span></span>



| <span data-ttu-id="52622-113">Метод</span><span class="sxs-lookup"><span data-stu-id="52622-113">Method</span></span>                                       | <span data-ttu-id="52622-114">Описание</span><span class="sxs-lookup"><span data-stu-id="52622-114">Description</span></span>                                                                |
|:---------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="52622-115">**GetSize**</span><span class="sxs-lookup"><span data-stu-id="52622-115">**GetSize**</span></span>](id3dx10meshbuffer-getsize.md) | <span data-ttu-id="52622-116">Возвращает размер буфера сетки в байтах.</span><span class="sxs-lookup"><span data-stu-id="52622-116">Get the size of the mesh buffer, in bytes.</span></span><br/>                      |
| [<span data-ttu-id="52622-117">**Таблица**</span><span class="sxs-lookup"><span data-stu-id="52622-117">**Map**</span></span>](id3dx10meshbuffer-map.md)         | <span data-ttu-id="52622-118">Получите указатель на память буфера сетки, чтобы изменить ее содержимое.</span><span class="sxs-lookup"><span data-stu-id="52622-118">Get a pointer to the mesh buffer memory to modify its contents.</span></span><br/> |
| [<span data-ttu-id="52622-119">**Unmap**</span><span class="sxs-lookup"><span data-stu-id="52622-119">**Unmap**</span></span>](id3dx10meshbuffer-unmap.md)     | <span data-ttu-id="52622-120">Отмена сопоставления буфера.</span><span class="sxs-lookup"><span data-stu-id="52622-120">Unmap a buffer.</span></span><br/>                                                 |



 

## <a name="requirements"></a><span data-ttu-id="52622-121">Требования</span><span class="sxs-lookup"><span data-stu-id="52622-121">Requirements</span></span>



| <span data-ttu-id="52622-122">Требование</span><span class="sxs-lookup"><span data-stu-id="52622-122">Requirement</span></span> | <span data-ttu-id="52622-123">Значение</span><span class="sxs-lookup"><span data-stu-id="52622-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="52622-124">Header</span><span class="sxs-lookup"><span data-stu-id="52622-124">Header</span></span><br/>  | <dl> <span data-ttu-id="52622-125"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="52622-125"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="52622-126">Библиотека</span><span class="sxs-lookup"><span data-stu-id="52622-126">Library</span></span><br/> | <dl> <span data-ttu-id="52622-127"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="52622-127"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="52622-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="52622-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="52622-129">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="52622-129">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
