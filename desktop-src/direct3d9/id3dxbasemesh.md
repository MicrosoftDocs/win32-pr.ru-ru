---
description: Приложения используют методы интерфейса ID3DXBaseMesh для управления и запроса сетки и прогрессивных сетчатых объектов.
ms.assetid: ec4ccd77-e370-470c-9325-3d794a8f7f16
title: Интерфейс ID3DXBaseMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXBaseMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 58029639852b30f5de357bb2643583615c45485c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355030"
---
# <a name="id3dxbasemesh-interface"></a><span data-ttu-id="168d8-103">Интерфейс ID3DXBaseMesh</span><span class="sxs-lookup"><span data-stu-id="168d8-103">ID3DXBaseMesh interface</span></span>

<span data-ttu-id="168d8-104">Приложения используют методы интерфейса **ID3DXBaseMesh** для управления и запроса сетки и прогрессивных сетчатых объектов.</span><span class="sxs-lookup"><span data-stu-id="168d8-104">Applications use the methods of the **ID3DXBaseMesh** interface to manipulate and query mesh and progressive mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="168d8-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="168d8-105">Members</span></span>

<span data-ttu-id="168d8-106">Интерфейс **ID3DXBaseMesh** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="168d8-106">The **ID3DXBaseMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="168d8-107">**ID3DXBaseMesh** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="168d8-107">**ID3DXBaseMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="168d8-108">Методы</span><span class="sxs-lookup"><span data-stu-id="168d8-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="168d8-109">Методы</span><span class="sxs-lookup"><span data-stu-id="168d8-109">Methods</span></span>

<span data-ttu-id="168d8-110">Интерфейс **ID3DXBaseMesh** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="168d8-110">The **ID3DXBaseMesh** interface has these methods.</span></span>



| <span data-ttu-id="168d8-111">Метод</span><span class="sxs-lookup"><span data-stu-id="168d8-111">Method</span></span>                                                                            | <span data-ttu-id="168d8-112">Описание</span><span class="sxs-lookup"><span data-stu-id="168d8-112">Description</span></span>                                                                                                                                                                                                           |
|:----------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="168d8-113">**клонемеш**</span><span class="sxs-lookup"><span data-stu-id="168d8-113">**CloneMesh**</span></span>](id3dxbasemesh--clonemesh.md)                                     | <span data-ttu-id="168d8-114">Создает точную копию сетки с помощью декларатора.</span><span class="sxs-lookup"><span data-stu-id="168d8-114">Clones a mesh using a declarator.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="168d8-115">**клонемешфвф**</span><span class="sxs-lookup"><span data-stu-id="168d8-115">**CloneMeshFVF**</span></span>](id3dxbasemesh--clonemeshfvf.md)                               | <span data-ttu-id="168d8-116">Создает точную копию сетки, используя код гибкого формата вершин (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="168d8-116">Clones a mesh using a flexible vertex format (FVF) code.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="168d8-117">**конвертаджаценцитопоинтрепс**</span><span class="sxs-lookup"><span data-stu-id="168d8-117">**ConvertAdjacencyToPointReps**</span></span>](id3dxbasemesh--convertadjacencytopointreps.md) | <span data-ttu-id="168d8-118">Преобразует сведения о смежности сетки в массив точек зрения.</span><span class="sxs-lookup"><span data-stu-id="168d8-118">Converts mesh adjacency information to an array of point representatives.</span></span><br/>                                                                                                                                  |
| [<span data-ttu-id="168d8-119">**конвертпоинтрепстоаджаценци**</span><span class="sxs-lookup"><span data-stu-id="168d8-119">**ConvertPointRepsToAdjacency**</span></span>](id3dxbasemesh--convertpointrepstoadjacency.md) | <span data-ttu-id="168d8-120">Преобразует данные репрезентативного указания в сведения о смежности сетки.</span><span class="sxs-lookup"><span data-stu-id="168d8-120">Converts point representative data to mesh adjacency information.</span></span><br/>                                                                                                                                          |
| [<span data-ttu-id="168d8-121">**дравсубсет**</span><span class="sxs-lookup"><span data-stu-id="168d8-121">**DrawSubset**</span></span>](id3dxbasemesh--drawsubset.md)                                   | <span data-ttu-id="168d8-122">Рисует подмножество сетки.</span><span class="sxs-lookup"><span data-stu-id="168d8-122">Draws a subset of a mesh.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="168d8-123">**женератеаджаценци**</span><span class="sxs-lookup"><span data-stu-id="168d8-123">**GenerateAdjacency**</span></span>](id3dxbasemesh--generateadjacency.md)                     | <span data-ttu-id="168d8-124">Создание списка границ сетки, а также списка лиц, совместно использующих каждое ребро.</span><span class="sxs-lookup"><span data-stu-id="168d8-124">Generate a list of mesh edges, as well as a list of faces that share each edge.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="168d8-125">**жетаттрибутетабле**</span><span class="sxs-lookup"><span data-stu-id="168d8-125">**GetAttributeTable**</span></span>](id3dxbasemesh--getattributetable.md)                     | <span data-ttu-id="168d8-126">Извлекает либо таблицу атрибутов для сетки, либо число записей, хранящихся в таблице атрибутов сетки.</span><span class="sxs-lookup"><span data-stu-id="168d8-126">Retrieves either an attribute table for a mesh, or the number of entries stored in an attribute table for a mesh.</span></span><br/>                                                                                          |
| [<span data-ttu-id="168d8-127">**Объявление о выходе**</span><span class="sxs-lookup"><span data-stu-id="168d8-127">**GetDeclaration**</span></span>](id3dxbasemesh--getdeclaration.md)                           | <span data-ttu-id="168d8-128">Извлекает объявление, описывающее вершины в сетке.</span><span class="sxs-lookup"><span data-stu-id="168d8-128">Retrieves a declaration describing the vertices in the mesh.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="168d8-129">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="168d8-129">**GetDevice**</span></span>](id3dxbasemesh--getdevice.md)                                     | <span data-ttu-id="168d8-130">Извлекает устройство, связанное с сеткой.</span><span class="sxs-lookup"><span data-stu-id="168d8-130">Retrieves the device associated with the mesh.</span></span><br/>                                                                                                                                                             |
| [<span data-ttu-id="168d8-131">**жетфвф**</span><span class="sxs-lookup"><span data-stu-id="168d8-131">**GetFVF**</span></span>](id3dxbasemesh--getfvf.md)                                           | <span data-ttu-id="168d8-132">Возвращает значение фиксированной вершины функции.</span><span class="sxs-lookup"><span data-stu-id="168d8-132">Gets the fixed function vertex value.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="168d8-133">**жетиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="168d8-133">**GetIndexBuffer**</span></span>](id3dxbasemesh--getindexbuffer.md)                           | <span data-ttu-id="168d8-134">Получает данные в буфере индекса.</span><span class="sxs-lookup"><span data-stu-id="168d8-134">Retrieves the data in an index buffer.</span></span><br/>                                                                                                                                                                     |
| [<span data-ttu-id="168d8-135">**жетнумбитеспервертекс**</span><span class="sxs-lookup"><span data-stu-id="168d8-135">**GetNumBytesPerVertex**</span></span>](id3dxbasemesh--getnumbytespervertex.md)               | <span data-ttu-id="168d8-136">Возвращает число байтов на вершину.</span><span class="sxs-lookup"><span data-stu-id="168d8-136">Gets the number of bytes per vertex.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="168d8-137">**жетнумфацес**</span><span class="sxs-lookup"><span data-stu-id="168d8-137">**GetNumFaces**</span></span>](id3dxbasemesh--getnumfaces.md)                                 | <span data-ttu-id="168d8-138">Извлекает количество лиц в сетке.</span><span class="sxs-lookup"><span data-stu-id="168d8-138">Retrieves the number of faces in the mesh.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="168d8-139">**жетнумвертицес**</span><span class="sxs-lookup"><span data-stu-id="168d8-139">**GetNumVertices**</span></span>](id3dxbasemesh--getnumvertices.md)                           | <span data-ttu-id="168d8-140">Возвращает количество вершин в сетке.</span><span class="sxs-lookup"><span data-stu-id="168d8-140">Retrieves the number of vertices in the mesh.</span></span><br/>                                                                                                                                                              |
| [<span data-ttu-id="168d8-141">**Параметры команды**</span><span class="sxs-lookup"><span data-stu-id="168d8-141">**GetOptions**</span></span>](id3dxbasemesh--getoptions.md)                                   | <span data-ttu-id="168d8-142">Извлекает параметры сетки, включенные для этой сетки во время создания.</span><span class="sxs-lookup"><span data-stu-id="168d8-142">Retrieves the mesh options enabled for this mesh at creation time.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="168d8-143">**жетвертексбуффер**</span><span class="sxs-lookup"><span data-stu-id="168d8-143">**GetVertexBuffer**</span></span>](id3dxbasemesh--getvertexbuffer.md)                         | <span data-ttu-id="168d8-144">Извлекает буфер вершин, связанный с сеткой.</span><span class="sxs-lookup"><span data-stu-id="168d8-144">Retrieves the vertex buffer associated with the mesh.</span></span><br/>                                                                                                                                                      |
| [<span data-ttu-id="168d8-145">**локкиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="168d8-145">**LockIndexBuffer**</span></span>](id3dxbasemesh--lockindexbuffer.md)                         | <span data-ttu-id="168d8-146">Блокирует буфер индексов и получает указатель на буфер памяти буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="168d8-146">Locks an index buffer and obtains a pointer to the index buffer memory.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="168d8-147">**локквертексбуффер**</span><span class="sxs-lookup"><span data-stu-id="168d8-147">**LockVertexBuffer**</span></span>](id3dxbasemesh--lockvertexbuffer.md)                       | <span data-ttu-id="168d8-148">Блокирует буфер вершин и получает указатель на память буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="168d8-148">Locks a vertex buffer and obtains a pointer to the vertex buffer memory.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="168d8-149">**унлоккиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="168d8-149">**UnlockIndexBuffer**</span></span>](id3dxbasemesh--unlockindexbuffer.md)                     | <span data-ttu-id="168d8-150">Разблокирует буфер индексов.</span><span class="sxs-lookup"><span data-stu-id="168d8-150">Unlocks an index buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="168d8-151">**унлокквертексбуффер**</span><span class="sxs-lookup"><span data-stu-id="168d8-151">**UnlockVertexBuffer**</span></span>](id3dxbasemesh--unlockvertexbuffer.md)                   | <span data-ttu-id="168d8-152">Разблокирует буфер вершин.</span><span class="sxs-lookup"><span data-stu-id="168d8-152">Unlocks a vertex buffer.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="168d8-153">**упдатесемантикс**</span><span class="sxs-lookup"><span data-stu-id="168d8-153">**UpdateSemantics**</span></span>](id3dxbasemesh--updatesemantics.md)                         | <span data-ttu-id="168d8-154">Этот метод позволяет пользователю изменить объявление сетки, не изменяя макет данных в буфере вершин.</span><span class="sxs-lookup"><span data-stu-id="168d8-154">This method allows the user to change the mesh declaration without changing the data layout of the vertex buffer.</span></span> <span data-ttu-id="168d8-155">Вызов допустим только в том случае, если форматы старого и нового объявлений имеют одинаковый размер вершины.</span><span class="sxs-lookup"><span data-stu-id="168d8-155">The call is valid only if the old and new declaration formats have the same vertex size.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="168d8-156">Комментарии</span><span class="sxs-lookup"><span data-stu-id="168d8-156">Remarks</span></span>

<span data-ttu-id="168d8-157">Сетка — это объект, состоящие из набора многоугольных граней.</span><span class="sxs-lookup"><span data-stu-id="168d8-157">A mesh is an object made up of a set of polygonal faces.</span></span> <span data-ttu-id="168d8-158">Сетка определяет набор вершин и набор лиц (грани определяются в виде вершин и нормалей сетки).</span><span class="sxs-lookup"><span data-stu-id="168d8-158">A mesh defines a set of vertices and a set of faces (the faces are defined in terms of the vertices and normals of the mesh).</span></span>

<span data-ttu-id="168d8-159">Тип LPD3DXBASEMESH определяется как указатель на интерфейс **ID3DXBaseMesh** .</span><span class="sxs-lookup"><span data-stu-id="168d8-159">The LPD3DXBASEMESH type is defined as a pointer to the **ID3DXBaseMesh** interface.</span></span>


```
typedef struct ID3DXBaseMesh *LPD3DXBASEMESH;
```



## <a name="requirements"></a><span data-ttu-id="168d8-160">Требования</span><span class="sxs-lookup"><span data-stu-id="168d8-160">Requirements</span></span>



| <span data-ttu-id="168d8-161">Требование</span><span class="sxs-lookup"><span data-stu-id="168d8-161">Requirement</span></span> | <span data-ttu-id="168d8-162">Значение</span><span class="sxs-lookup"><span data-stu-id="168d8-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="168d8-163">Header</span><span class="sxs-lookup"><span data-stu-id="168d8-163">Header</span></span><br/>  | <dl> <span data-ttu-id="168d8-164"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="168d8-164"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="168d8-165">Библиотека</span><span class="sxs-lookup"><span data-stu-id="168d8-165">Library</span></span><br/> | <dl> <span data-ttu-id="168d8-166"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="168d8-166"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="168d8-167">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="168d8-167">See also</span></span>

<dl> <dt>

[<span data-ttu-id="168d8-168">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="168d8-168">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
