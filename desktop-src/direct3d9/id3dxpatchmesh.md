---
description: Этот интерфейс инкапсулирует функциональность сетки исправлений.
ms.assetid: c70c0fe0-b695-4ad9-b0c6-7854cf8f7593
title: Интерфейс ID3DXPatchMesh (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPatchMesh
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f1f13e6abe3a164e8027ddcb6bb33e9f0ca618fb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355210"
---
# <a name="id3dxpatchmesh-interface"></a><span data-ttu-id="8afc7-103">Интерфейс ID3DXPatchMesh</span><span class="sxs-lookup"><span data-stu-id="8afc7-103">ID3DXPatchMesh interface</span></span>

<span data-ttu-id="8afc7-104">Этот интерфейс инкапсулирует функциональность сетки исправлений.</span><span class="sxs-lookup"><span data-stu-id="8afc7-104">This interface encapsulates patch mesh functionality.</span></span>

## <a name="members"></a><span data-ttu-id="8afc7-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="8afc7-105">Members</span></span>

<span data-ttu-id="8afc7-106">Интерфейс **ID3DXPatchMesh** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8afc7-106">The **ID3DXPatchMesh** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8afc7-107">**ID3DXPatchMesh** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8afc7-107">**ID3DXPatchMesh** also has these types of members:</span></span>

-   [<span data-ttu-id="8afc7-108">Методы</span><span class="sxs-lookup"><span data-stu-id="8afc7-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8afc7-109">Методы</span><span class="sxs-lookup"><span data-stu-id="8afc7-109">Methods</span></span>

<span data-ttu-id="8afc7-110">Интерфейс **ID3DXPatchMesh** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8afc7-110">The **ID3DXPatchMesh** interface has these methods.</span></span>



| <span data-ttu-id="8afc7-111">Метод</span><span class="sxs-lookup"><span data-stu-id="8afc7-111">Method</span></span>                                                                           | <span data-ttu-id="8afc7-112">Описание</span><span class="sxs-lookup"><span data-stu-id="8afc7-112">Description</span></span>                                                                                     |
|:---------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8afc7-113">**клонемеш**</span><span class="sxs-lookup"><span data-stu-id="8afc7-113">**CloneMesh**</span></span>](id3dxpatchmesh--clonemesh.md)                                   | <span data-ttu-id="8afc7-114">Создает новую сетку исправлений с указанным объявлением вершины.</span><span class="sxs-lookup"><span data-stu-id="8afc7-114">Creates a new patch mesh with the specified vertex declaration.</span></span><br/>                      |
| [<span data-ttu-id="8afc7-115">**женератеаджаценци**</span><span class="sxs-lookup"><span data-stu-id="8afc7-115">**GenerateAdjacency**</span></span>](id3dxpatchmesh--generateadjacency.md)                   | <span data-ttu-id="8afc7-116">Создание списка границ сетки и исправлений, которые совместно используют каждое ребро.</span><span class="sxs-lookup"><span data-stu-id="8afc7-116">Generate a list of mesh edges and the patches that share each edge.</span></span><br/>                  |
| [<span data-ttu-id="8afc7-117">**жетконтролвертицесперпатч**</span><span class="sxs-lookup"><span data-stu-id="8afc7-117">**GetControlVerticesPerPatch**</span></span>](id3dxpatchmesh--getcontrolverticesperpatch.md) | <span data-ttu-id="8afc7-118">Возвращает число вершин управления на каждое исправление.</span><span class="sxs-lookup"><span data-stu-id="8afc7-118">Gets the number of control vertices per patch.</span></span><br/>                                       |
| [<span data-ttu-id="8afc7-119">**Объявление о выходе**</span><span class="sxs-lookup"><span data-stu-id="8afc7-119">**GetDeclaration**</span></span>](id3dxpatchmesh--getdeclaration.md)                         | <span data-ttu-id="8afc7-120">Возвращает объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="8afc7-120">Gets the vertex declaration.</span></span><br/>                                                         |
| [<span data-ttu-id="8afc7-121">**GetDevice**</span><span class="sxs-lookup"><span data-stu-id="8afc7-121">**GetDevice**</span></span>](id3dxpatchmesh--getdevice.md)                                   | <span data-ttu-id="8afc7-122">Возвращает устройство, создавшее сетку.</span><span class="sxs-lookup"><span data-stu-id="8afc7-122">Gets the device that created the mesh.</span></span><br/>                                               |
| [<span data-ttu-id="8afc7-123">**жетдисплацепарам**</span><span class="sxs-lookup"><span data-stu-id="8afc7-123">**GetDisplaceParam**</span></span>](id3dxpatchmesh--getdisplaceparam.md)                     | <span data-ttu-id="8afc7-124">Возвращает параметры смещения геометрического объекта сетки.</span><span class="sxs-lookup"><span data-stu-id="8afc7-124">Gets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="8afc7-125">**жетиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="8afc7-125">**GetIndexBuffer**</span></span>](id3dxpatchmesh--getindexbuffer.md)                         | <span data-ttu-id="8afc7-126">Возвращает буфер индекса сетки.</span><span class="sxs-lookup"><span data-stu-id="8afc7-126">Gets the mesh index buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="8afc7-127">**жетнумпатчес**</span><span class="sxs-lookup"><span data-stu-id="8afc7-127">**GetNumPatches**</span></span>](id3dxpatchmesh--getnumpatches.md)                           | <span data-ttu-id="8afc7-128">Возвращает число исправлений в сетке.</span><span class="sxs-lookup"><span data-stu-id="8afc7-128">Gets the number of patches in the mesh.</span></span><br/>                                              |
| [<span data-ttu-id="8afc7-129">**жетнумвертицес**</span><span class="sxs-lookup"><span data-stu-id="8afc7-129">**GetNumVertices**</span></span>](id3dxpatchmesh--getnumvertices.md)                         | <span data-ttu-id="8afc7-130">Возвращает количество вершин в сетке.</span><span class="sxs-lookup"><span data-stu-id="8afc7-130">Gets the number of vertices in the mesh.</span></span><br/>                                             |
| [<span data-ttu-id="8afc7-131">**Параметры команды**</span><span class="sxs-lookup"><span data-stu-id="8afc7-131">**GetOptions**</span></span>](id3dxpatchmesh--getoptions.md)                                 | <span data-ttu-id="8afc7-132">Возвращает тип исправления.</span><span class="sxs-lookup"><span data-stu-id="8afc7-132">Gets the type of patch.</span></span><br/>                                                              |
| [<span data-ttu-id="8afc7-133">**жетпатчинфо**</span><span class="sxs-lookup"><span data-stu-id="8afc7-133">**GetPatchInfo**</span></span>](id3dxpatchmesh--getpatchinfo.md)                             | <span data-ttu-id="8afc7-134">Возвращает атрибуты исправления.</span><span class="sxs-lookup"><span data-stu-id="8afc7-134">Gets the attributes of the patch.</span></span><br/>                                                    |
| [<span data-ttu-id="8afc7-135">**жеттесссизе**</span><span class="sxs-lookup"><span data-stu-id="8afc7-135">**GetTessSize**</span></span>](id3dxpatchmesh--gettesssize.md)                               | <span data-ttu-id="8afc7-136">Возвращает размер тесселяции сетки по заданному уровню тесселяции.</span><span class="sxs-lookup"><span data-stu-id="8afc7-136">Gets the size of the tessellated mesh, given a tessellation level.</span></span><br/>                   |
| [<span data-ttu-id="8afc7-137">**жетвертексбуффер**</span><span class="sxs-lookup"><span data-stu-id="8afc7-137">**GetVertexBuffer**</span></span>](id3dxpatchmesh--getvertexbuffer.md)                       | <span data-ttu-id="8afc7-138">Возвращает буфер вершин сетки.</span><span class="sxs-lookup"><span data-stu-id="8afc7-138">Gets the mesh vertex buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="8afc7-139">**локкаттрибутебуффер**</span><span class="sxs-lookup"><span data-stu-id="8afc7-139">**LockAttributeBuffer**</span></span>](id3dxpatchmesh--lockattributebuffer.md)               | <span data-ttu-id="8afc7-140">Блокирует буфер атрибута.</span><span class="sxs-lookup"><span data-stu-id="8afc7-140">Locks the attribute buffer.</span></span><br/>                                                          |
| [<span data-ttu-id="8afc7-141">**локкиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="8afc7-141">**LockIndexBuffer**</span></span>](id3dxpatchmesh--lockindexbuffer.md)                       | <span data-ttu-id="8afc7-142">Блокировка буфера индекса.</span><span class="sxs-lookup"><span data-stu-id="8afc7-142">Lock the index buffer.</span></span><br/>                                                               |
| [<span data-ttu-id="8afc7-143">**локквертексбуффер**</span><span class="sxs-lookup"><span data-stu-id="8afc7-143">**LockVertexBuffer**</span></span>](id3dxpatchmesh--lockvertexbuffer.md)                     | <span data-ttu-id="8afc7-144">Блокировка буфера вершин.</span><span class="sxs-lookup"><span data-stu-id="8afc7-144">Lock the vertex buffer.</span></span><br/>                                                              |
| [<span data-ttu-id="8afc7-145">**Увеличить**</span><span class="sxs-lookup"><span data-stu-id="8afc7-145">**Optimize**</span></span>](id3dxpatchmesh--optimize.md)                                     | <span data-ttu-id="8afc7-146">Оптимизирует сетку исправлений для эффективной тесселяции.</span><span class="sxs-lookup"><span data-stu-id="8afc7-146">Optimizes the patch mesh for efficient tessellation.</span></span><br/>                                 |
| [<span data-ttu-id="8afc7-147">**сетдисплацепарам**</span><span class="sxs-lookup"><span data-stu-id="8afc7-147">**SetDisplaceParam**</span></span>](id3dxpatchmesh--setdisplaceparam.md)                     | <span data-ttu-id="8afc7-148">Задает параметры смещения геометрических объектов сетки.</span><span class="sxs-lookup"><span data-stu-id="8afc7-148">Sets mesh geometry displacement parameters.</span></span><br/>                                          |
| [<span data-ttu-id="8afc7-149">**Проводить тесселяцию**</span><span class="sxs-lookup"><span data-stu-id="8afc7-149">**Tessellate**</span></span>](id3dxpatchmesh--tessellate.md)                                 | <span data-ttu-id="8afc7-150">Выполняет однородную тесселяцию на основе уровня тесселяции.</span><span class="sxs-lookup"><span data-stu-id="8afc7-150">Performs uniform tessellation based on the tessellation level.</span></span><br/>                       |
| [<span data-ttu-id="8afc7-151">**тесселлатеадаптиве**</span><span class="sxs-lookup"><span data-stu-id="8afc7-151">**TessellateAdaptive**</span></span>](id3dxpatchmesh--tessellateadaptive.md)                 | <span data-ttu-id="8afc7-152">Выполняет адаптивную тесселяцию на основе z-критерия адаптивной тесселяции.</span><span class="sxs-lookup"><span data-stu-id="8afc7-152">Performs adaptive tessellation based on the z-based adaptive tessellation criterion.</span></span><br/> |
| [<span data-ttu-id="8afc7-153">**унлоккаттрибутебуффер**</span><span class="sxs-lookup"><span data-stu-id="8afc7-153">**UnlockAttributeBuffer**</span></span>](id3dxpatchmesh--unlockattributebuffer.md)           | <span data-ttu-id="8afc7-154">Разблокируйте буфер атрибута.</span><span class="sxs-lookup"><span data-stu-id="8afc7-154">Unlock the attribute buffer.</span></span><br/>                                                         |
| [<span data-ttu-id="8afc7-155">**унлоккиндексбуффер**</span><span class="sxs-lookup"><span data-stu-id="8afc7-155">**UnlockIndexBuffer**</span></span>](id3dxpatchmesh--unlockindexbuffer.md)                   | <span data-ttu-id="8afc7-156">Разблокируйте буфер индексов.</span><span class="sxs-lookup"><span data-stu-id="8afc7-156">Unlock the index buffer.</span></span><br/>                                                             |
| [<span data-ttu-id="8afc7-157">**унлокквертексбуффер**</span><span class="sxs-lookup"><span data-stu-id="8afc7-157">**UnlockVertexBuffer**</span></span>](id3dxpatchmesh--unlockvertexbuffer.md)                 | <span data-ttu-id="8afc7-158">Разблокируйте буфер вершин.</span><span class="sxs-lookup"><span data-stu-id="8afc7-158">Unlock the vertex buffer.</span></span><br/>                                                            |



 

## <a name="remarks"></a><span data-ttu-id="8afc7-159">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8afc7-159">Remarks</span></span>

<span data-ttu-id="8afc7-160">Сетка исправлений — это сетка, которая состоит из серии исправлений.</span><span class="sxs-lookup"><span data-stu-id="8afc7-160">A patch mesh is a mesh that consists of a series of patches.</span></span>

<span data-ttu-id="8afc7-161">Чтобы получить интерфейс **ID3DXPatchMesh** , вызовите функцию [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) .</span><span class="sxs-lookup"><span data-stu-id="8afc7-161">To obtain the **ID3DXPatchMesh** interface, call the [**D3DXCreatePatchMesh**](d3dxcreatepatchmesh.md) function.</span></span>

<span data-ttu-id="8afc7-162">Тип LPD3DXPATCHMESH определяется как указатель на интерфейс **ID3DXPatchMesh** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="8afc7-162">The LPD3DXPATCHMESH type is defined as a pointer to the **ID3DXPatchMesh** interface, as follows:</span></span>


```
typedef struct ID3DXPatchMesh *LPD3DXPATCHMESH;
```



## <a name="requirements"></a><span data-ttu-id="8afc7-163">Требования</span><span class="sxs-lookup"><span data-stu-id="8afc7-163">Requirements</span></span>



| <span data-ttu-id="8afc7-164">Требование</span><span class="sxs-lookup"><span data-stu-id="8afc7-164">Requirement</span></span> | <span data-ttu-id="8afc7-165">Значение</span><span class="sxs-lookup"><span data-stu-id="8afc7-165">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8afc7-166">Header</span><span class="sxs-lookup"><span data-stu-id="8afc7-166">Header</span></span><br/>  | <dl> <span data-ttu-id="8afc7-167"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="8afc7-167"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="8afc7-168">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8afc7-168">Library</span></span><br/> | <dl> <span data-ttu-id="8afc7-169"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8afc7-169"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8afc7-170">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8afc7-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8afc7-171">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="8afc7-171">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> <dt>

[<span data-ttu-id="8afc7-172">Функции сетки</span><span class="sxs-lookup"><span data-stu-id="8afc7-172">Mesh Functions</span></span>](dx9-graphics-reference-d3dx-functions-mesh.md)
</dt> </dl>

 

 
