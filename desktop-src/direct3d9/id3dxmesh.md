---
description: Приложения используют методы интерфейса ID3DXMesh для управления объектами сетки.
ms.assetid: f571fe0b-3f0c-43c9-809c-d1e14f85b720
title: Интерфейс ID3DXMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 9c2a677edba4bad5e908b6dd69aa21a467b2a245
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355713"
---
# <a name="id3dxmesh-interface"></a><span data-ttu-id="021c2-103">Интерфейс ID3DXMesh</span><span class="sxs-lookup"><span data-stu-id="021c2-103">ID3DXMesh interface</span></span>

<span data-ttu-id="021c2-104">Приложения используют методы интерфейса ID3DXMesh для управления объектами сетки.</span><span class="sxs-lookup"><span data-stu-id="021c2-104">Applications use the methods of the ID3DXMesh interface to manipulate mesh objects.</span></span>

## <a name="members"></a><span data-ttu-id="021c2-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="021c2-105">Members</span></span>

<span data-ttu-id="021c2-106">Интерфейс **ID3DXMesh** наследует от [**ID3DXBaseMesh**](id3dxbasemesh.md).</span><span class="sxs-lookup"><span data-stu-id="021c2-106">The **ID3DXMesh** interface inherits from [**ID3DXBaseMesh**](id3dxbasemesh.md).</span></span> <span data-ttu-id="021c2-107">**ID3DXMesh** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="021c2-107">**ID3DXMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="021c2-108">Методы</span><span class="sxs-lookup"><span data-stu-id="021c2-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="021c2-109">Методы</span><span class="sxs-lookup"><span data-stu-id="021c2-109">Methods</span></span>

<span data-ttu-id="021c2-110">Интерфейс **ID3DXMesh** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="021c2-110">The **ID3DXMesh** interface has these methods.</span></span>



| <span data-ttu-id="021c2-111">Метод</span><span class="sxs-lookup"><span data-stu-id="021c2-111">Method</span></span>                                                            | <span data-ttu-id="021c2-112">Описание</span><span class="sxs-lookup"><span data-stu-id="021c2-112">Description</span></span>                                                                                                                            |
|:------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="021c2-113">**локкаттрибутебуффер**</span><span class="sxs-lookup"><span data-stu-id="021c2-113">**LockAttributeBuffer**</span></span>](id3dxmesh--lockattributebuffer.md)     | <span data-ttu-id="021c2-114">Блокирует буфер сетки, содержащий данные атрибута сетки, и возвращает указатель на него.</span><span class="sxs-lookup"><span data-stu-id="021c2-114">Locks the mesh buffer that contains the mesh attribute data, and returns a pointer to it.</span></span><br/>                                   |
| [<span data-ttu-id="021c2-115">**Увеличить**</span><span class="sxs-lookup"><span data-stu-id="021c2-115">**Optimize**</span></span>](id3dxmesh--optimize.md)                           | <span data-ttu-id="021c2-116">Создает новую сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования.</span><span class="sxs-lookup"><span data-stu-id="021c2-116">Generates a new mesh with reordered faces and vertices to optimize drawing performance.</span></span><br/>                                     |
| [<span data-ttu-id="021c2-117">**оптимизеинплаце**</span><span class="sxs-lookup"><span data-stu-id="021c2-117">**OptimizeInplace**</span></span>](id3dxmesh--optimizeinplace.md)             | <span data-ttu-id="021c2-118">Создает сетку с переупорядоченными лицами и вершинами для оптимизации производительности рисования.</span><span class="sxs-lookup"><span data-stu-id="021c2-118">Generates a mesh with reordered faces and vertices to optimize drawing performance.</span></span> <span data-ttu-id="021c2-119">Этот метод переупорядочивает существующую сетку.</span><span class="sxs-lookup"><span data-stu-id="021c2-119">This method reorders the existing mesh.</span></span><br/> |
| [<span data-ttu-id="021c2-120">**сетаттрибутетабле**</span><span class="sxs-lookup"><span data-stu-id="021c2-120">**SetAttributeTable**</span></span>](id3dxmesh--setattributetable.md)         | <span data-ttu-id="021c2-121">Задает таблицу атрибутов для сетки и число записей, хранящихся в таблице.</span><span class="sxs-lookup"><span data-stu-id="021c2-121">Sets the attribute table for a mesh and the number of entries stored in the table.</span></span><br/>                                          |
| [<span data-ttu-id="021c2-122">**унлоккаттрибутебуффер**</span><span class="sxs-lookup"><span data-stu-id="021c2-122">**UnlockAttributeBuffer**</span></span>](id3dxmesh--unlockattributebuffer.md) | <span data-ttu-id="021c2-123">Разблокирует буфер атрибута.</span><span class="sxs-lookup"><span data-stu-id="021c2-123">Unlocks an attribute buffer.</span></span><br/>                                                                                                |



 

## <a name="remarks"></a><span data-ttu-id="021c2-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="021c2-124">Remarks</span></span>

<span data-ttu-id="021c2-125">Чтобы получить интерфейс **ID3DXMesh** , вызовите функцию [**D3DXCreateMesh**](d3dxcreatemesh.md) или [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) .</span><span class="sxs-lookup"><span data-stu-id="021c2-125">To obtain the **ID3DXMesh** interface, call either the [**D3DXCreateMesh**](d3dxcreatemesh.md) or [**D3DXCreateMeshFVF**](d3dxcreatemeshfvf.md) function.</span></span>

<span data-ttu-id="021c2-126">Этот интерфейс наследует дополнительные функциональные возможности интерфейса [**ID3DXBaseMesh**](id3dxbasemesh.md) .</span><span class="sxs-lookup"><span data-stu-id="021c2-126">This interface inherits additional functionality from the [**ID3DXBaseMesh**](id3dxbasemesh.md) interface.</span></span>

<span data-ttu-id="021c2-127">Тип LPD3DXMESH определяется как указатель на интерфейс **ID3DXMesh** .</span><span class="sxs-lookup"><span data-stu-id="021c2-127">The LPD3DXMESH type is defined as a pointer to the **ID3DXMesh** interface.</span></span>


```
typedef struct ID3DXMesh *LPD3DXMESH;
```



## <a name="requirements"></a><span data-ttu-id="021c2-128">Требования</span><span class="sxs-lookup"><span data-stu-id="021c2-128">Requirements</span></span>



| <span data-ttu-id="021c2-129">Требование</span><span class="sxs-lookup"><span data-stu-id="021c2-129">Requirement</span></span> | <span data-ttu-id="021c2-130">Значение</span><span class="sxs-lookup"><span data-stu-id="021c2-130">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="021c2-131">Header</span><span class="sxs-lookup"><span data-stu-id="021c2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="021c2-132"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="021c2-132"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="021c2-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="021c2-133">Library</span></span><br/> | <dl> <span data-ttu-id="021c2-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="021c2-134"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="021c2-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="021c2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="021c2-136">**ID3DXBaseMesh**</span><span class="sxs-lookup"><span data-stu-id="021c2-136">**ID3DXBaseMesh**</span></span>](id3dxbasemesh.md)
</dt> <dt>

[<span data-ttu-id="021c2-137">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="021c2-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="021c2-138">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="021c2-138">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 




