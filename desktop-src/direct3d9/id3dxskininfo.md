---
description: Приложения используют методы интерфейса ID3DXSkinInfo для управления матрицами костей, которые используются для обложки данных вершин для анимации. Этот интерфейс более строго привязан к ID3DXMesh и может использоваться для обложек любого набора данных вершин.
ms.assetid: 4ccf88b0-2cc7-4e91-a0f2-fb8eea66a3ce
title: Интерфейс ID3DXSkinInfo (D3DX9Mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSkinInfo
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: afb93a0513bef7de1b0815b8b1f50179e2cba41d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713593"
---
# <a name="id3dxskininfo-interface"></a><span data-ttu-id="bfc88-104">Интерфейс ID3DXSkinInfo</span><span class="sxs-lookup"><span data-stu-id="bfc88-104">ID3DXSkinInfo interface</span></span>

<span data-ttu-id="bfc88-105">Приложения используют методы интерфейса ID3DXSkinInfo для управления матрицами костей, которые используются для обложки данных вершин для анимации.</span><span class="sxs-lookup"><span data-stu-id="bfc88-105">Applications use the methods of the ID3DXSkinInfo interface to manipulate bone matrices, which are used to skin vertex data for animation.</span></span> <span data-ttu-id="bfc88-106">Этот интерфейс более строго привязан к [**ID3DXMesh**](id3dxmesh.md) и может использоваться для обложек любого набора данных вершин.</span><span class="sxs-lookup"><span data-stu-id="bfc88-106">This interface is no longer strictly tied to [**ID3DXMesh**](id3dxmesh.md) and can be used to skin any set of vertex data.</span></span>

## <a name="members"></a><span data-ttu-id="bfc88-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="bfc88-107">Members</span></span>

<span data-ttu-id="bfc88-108">Интерфейс **ID3DXSkinInfo** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="bfc88-108">The **ID3DXSkinInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="bfc88-109">**ID3DXSkinInfo** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="bfc88-109">**ID3DXSkinInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="bfc88-110">Методы</span><span class="sxs-lookup"><span data-stu-id="bfc88-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="bfc88-111">Методы</span><span class="sxs-lookup"><span data-stu-id="bfc88-111">Methods</span></span>

<span data-ttu-id="bfc88-112">Интерфейс **ID3DXSkinInfo** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="bfc88-112">The **ID3DXSkinInfo** interface has these methods.</span></span>



| <span data-ttu-id="bfc88-113">Метод</span><span class="sxs-lookup"><span data-stu-id="bfc88-113">Method</span></span>                                                                              | <span data-ttu-id="bfc88-114">Описание</span><span class="sxs-lookup"><span data-stu-id="bfc88-114">Description</span></span>                                                                                                                                                                                    |
|:------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bfc88-115">**Клонировать**</span><span class="sxs-lookup"><span data-stu-id="bfc88-115">**Clone**</span></span>](id3dxskininfo--clone.md)                                               | <span data-ttu-id="bfc88-116">Создает точную копию объекта сведений об обложке.</span><span class="sxs-lookup"><span data-stu-id="bfc88-116">Clones a skin info object.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="bfc88-117">**конверттоблендедмеш**</span><span class="sxs-lookup"><span data-stu-id="bfc88-117">**ConvertToBlendedMesh**</span></span>](id3dxskininfo--converttoblendedmesh.md)                 | <span data-ttu-id="bfc88-118">Принимает сетку и возвращает новую сетку с весовым коэффициентом смешения и таблицей сочетаний костей.</span><span class="sxs-lookup"><span data-stu-id="bfc88-118">Takes a mesh and returns a new mesh with per-vertex blend weights and a bone combination table.</span></span> <span data-ttu-id="bfc88-119">В таблице описывается, какие кости влияют на подмножества сетки.</span><span class="sxs-lookup"><span data-stu-id="bfc88-119">The table describes which bones affect which subsets of the mesh.</span></span><br/>                   |
| [<span data-ttu-id="bfc88-120">**конверттоиндекседблендедмеш**</span><span class="sxs-lookup"><span data-stu-id="bfc88-120">**ConvertToIndexedBlendedMesh**</span></span>](id3dxskininfo--converttoindexedblendedmesh.md)   | <span data-ttu-id="bfc88-121">Принимает сетку и возвращает новую сетку с весовыми коэффициентами перехода на вершину, индексами и комбинацией костей.</span><span class="sxs-lookup"><span data-stu-id="bfc88-121">Takes a mesh and returns a new mesh with per-vertex blend weights, indices, and a bone combination table.</span></span> <span data-ttu-id="bfc88-122">В таблице описывается, какие палитры костей влияют на подмножества сетки.</span><span class="sxs-lookup"><span data-stu-id="bfc88-122">The table describes which bone palettes affect which subsets of the mesh.</span></span><br/> |
| [<span data-ttu-id="bfc88-123">**финдбоневертексинфлуенцеиндекс**</span><span class="sxs-lookup"><span data-stu-id="bfc88-123">**FindBoneVertexInfluenceIndex**</span></span>](id3dxskininfo--findbonevertexinfluenceindex.md) | <span data-ttu-id="bfc88-124">Извлекает индекс кости, влияющей на одну вершину.</span><span class="sxs-lookup"><span data-stu-id="bfc88-124">Retrieves the index of the bone influence affecting a single vertex.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="bfc88-125">**жетбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="bfc88-125">**GetBoneInfluence**</span></span>](id3dxskininfo--getboneinfluence.md)                         | <span data-ttu-id="bfc88-126">Возвращает вершины и весовые коэффициенты, влияющие на кость.</span><span class="sxs-lookup"><span data-stu-id="bfc88-126">Gets the vertices and weights that a bone influences.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="bfc88-127">**жетбоненаме**</span><span class="sxs-lookup"><span data-stu-id="bfc88-127">**GetBoneName**</span></span>](id3dxskininfo--getbonename.md)                                   | <span data-ttu-id="bfc88-128">Возвращает имя кости из индекса костей.</span><span class="sxs-lookup"><span data-stu-id="bfc88-128">Gets the bone name, from the bone index.</span></span><br/>                                                                                                                                            |
| [<span data-ttu-id="bfc88-129">**жетбонеоффсетматрикс**</span><span class="sxs-lookup"><span data-stu-id="bfc88-129">**GetBoneOffsetMatrix**</span></span>](id3dxskininfo--getboneoffsetmatrix.md)                   | <span data-ttu-id="bfc88-130">Возвращает матрицу смещения кости.</span><span class="sxs-lookup"><span data-stu-id="bfc88-130">Gets the bone offset matrix.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="bfc88-131">**жетбоневертексинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="bfc88-131">**GetBoneVertexInfluence**</span></span>](id3dxskininfo--getbonevertexinfluence.md)             | <span data-ttu-id="bfc88-132">Извлекает коэффициент смешения и вершину, затрагиваемые указанными костями.</span><span class="sxs-lookup"><span data-stu-id="bfc88-132">Retrieves the blend factor and vertex affected by a specified bone influence.</span></span><br/>                                                                                                       |
| [<span data-ttu-id="bfc88-133">**Объявление о выходе**</span><span class="sxs-lookup"><span data-stu-id="bfc88-133">**GetDeclaration**</span></span>](id3dxskininfo--getdeclaration.md)                             | <span data-ttu-id="bfc88-134">Возвращает объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="bfc88-134">Gets the vertex declaration.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="bfc88-135">**жетфвф**</span><span class="sxs-lookup"><span data-stu-id="bfc88-135">**GetFVF**</span></span>](id3dxskininfo--getfvf.md)                                             | <span data-ttu-id="bfc88-136">Возвращает значение фиксированной вершины функции.</span><span class="sxs-lookup"><span data-stu-id="bfc88-136">Gets the fixed function vertex value.</span></span><br/>                                                                                                                                               |
| [<span data-ttu-id="bfc88-137">**жетмаксфацеинфлуенцес**</span><span class="sxs-lookup"><span data-stu-id="bfc88-137">**GetMaxFaceInfluences**</span></span>](id3dxskininfo--getmaxfaceinfluences.md)                 | <span data-ttu-id="bfc88-138">Возвращает максимальное влияние на грань в сетке треугольников с указанным буфером индекса.</span><span class="sxs-lookup"><span data-stu-id="bfc88-138">Gets the maximum face influences in a triangle mesh with the specified index buffer.</span></span><br/>                                                                                                |
| [<span data-ttu-id="bfc88-139">**жетмаксвертексинфлуенцес**</span><span class="sxs-lookup"><span data-stu-id="bfc88-139">**GetMaxVertexInfluences**</span></span>](id3dxskininfo--getmaxvertexinfluences.md)             | <span data-ttu-id="bfc88-140">Возвращает максимальное количество влияния на любую вершину в сетке.</span><span class="sxs-lookup"><span data-stu-id="bfc88-140">Gets the maximum number of influences for any vertex in the mesh.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="bfc88-141">**жетминбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="bfc88-141">**GetMinBoneInfluence**</span></span>](id3dxskininfo--getminboneinfluence.md)                   | <span data-ttu-id="bfc88-142">Возвращает минимальную влияние на кость.</span><span class="sxs-lookup"><span data-stu-id="bfc88-142">Gets the minimum bone influence.</span></span> <span data-ttu-id="bfc88-143">Влияние значений меньше этого значения не учитывается.</span><span class="sxs-lookup"><span data-stu-id="bfc88-143">Influence values smaller than this are ignored.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="bfc88-144">**жетнумбонеинфлуенцес**</span><span class="sxs-lookup"><span data-stu-id="bfc88-144">**GetNumBoneInfluences**</span></span>](id3dxskininfo--getnumboneinfluences.md)                 | <span data-ttu-id="bfc88-145">Возвращает число повлияет на кость.</span><span class="sxs-lookup"><span data-stu-id="bfc88-145">Gets the number of influences for a bone.</span></span><br/>                                                                                                                                           |
| [<span data-ttu-id="bfc88-146">**жетнумбонес**</span><span class="sxs-lookup"><span data-stu-id="bfc88-146">**GetNumBones**</span></span>](id3dxskininfo--getnumbones.md)                                   | <span data-ttu-id="bfc88-147">Возвращает число костей.</span><span class="sxs-lookup"><span data-stu-id="bfc88-147">Gets the number of bones.</span></span><br/>                                                                                                                                                           |
| [<span data-ttu-id="bfc88-148">**Восстановить**</span><span class="sxs-lookup"><span data-stu-id="bfc88-148">**Remap**</span></span>](id3dxskininfo--remap.md)                                               | <span data-ttu-id="bfc88-149">Обновляет сведения, влияющие на кости, для сопоставления вершин после их переупорядочивания.</span><span class="sxs-lookup"><span data-stu-id="bfc88-149">Updates bone influence information to match vertices after they are reordered.</span></span> <span data-ttu-id="bfc88-150">Этот метод должен вызываться, если целевой буфер вершин был изменен заказа извне.</span><span class="sxs-lookup"><span data-stu-id="bfc88-150">This method should be called if the target vertex buffer has been reordered externally.</span></span><br/>              |
| [<span data-ttu-id="bfc88-151">**сетбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="bfc88-151">**SetBoneInfluence**</span></span>](id3dxskininfo--setboneinfluence.md)                         | <span data-ttu-id="bfc88-152">Задает значение влияния для кости.</span><span class="sxs-lookup"><span data-stu-id="bfc88-152">Sets the influence value for a bone.</span></span><br/>                                                                                                                                                |
| [<span data-ttu-id="bfc88-153">**сетбоненаме**</span><span class="sxs-lookup"><span data-stu-id="bfc88-153">**SetBoneName**</span></span>](id3dxskininfo--setbonename.md)                                   | <span data-ttu-id="bfc88-154">Задает имя кости.</span><span class="sxs-lookup"><span data-stu-id="bfc88-154">Sets the bone name.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="bfc88-155">**сетбонеоффсетматрикс**</span><span class="sxs-lookup"><span data-stu-id="bfc88-155">**SetBoneOffsetMatrix**</span></span>](id3dxskininfo--setboneoffsetmatrix.md)                   | <span data-ttu-id="bfc88-156">Задает матрицу смещения кости.</span><span class="sxs-lookup"><span data-stu-id="bfc88-156">Sets the bone offset matrix.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="bfc88-157">**сетбоневертексинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="bfc88-157">**SetBoneVertexInfluence**</span></span>](id3dxskininfo--setbonevertexinfluence.md)             | <span data-ttu-id="bfc88-158">Задает значение влияния кости на одну вершину.</span><span class="sxs-lookup"><span data-stu-id="bfc88-158">Sets an influence value of a bone on a single vertex.</span></span><br/>                                                                                                                               |
| [<span data-ttu-id="bfc88-159">**сетдекларатион**</span><span class="sxs-lookup"><span data-stu-id="bfc88-159">**SetDeclaration**</span></span>](id3dxskininfo--setdeclaration.md)                             | <span data-ttu-id="bfc88-160">Задает объявление вершины.</span><span class="sxs-lookup"><span data-stu-id="bfc88-160">Sets the vertex declaration.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="bfc88-161">**сетфвф**</span><span class="sxs-lookup"><span data-stu-id="bfc88-161">**SetFVF**</span></span>](id3dxskininfo--setfvf.md)                                             | <span data-ttu-id="bfc88-162">Задает тип гибкого формата вершин (ФВФ).</span><span class="sxs-lookup"><span data-stu-id="bfc88-162">Sets the flexible vertex format (FVF) type.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="bfc88-163">**сетминбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="bfc88-163">**SetMinBoneInfluence**</span></span>](id3dxskininfo--setminboneinfluence.md)                   | <span data-ttu-id="bfc88-164">Устанавливает минимальную влияние на кость.</span><span class="sxs-lookup"><span data-stu-id="bfc88-164">Sets the minimum bone influence.</span></span> <span data-ttu-id="bfc88-165">Влияние значений меньше этого значения не учитывается.</span><span class="sxs-lookup"><span data-stu-id="bfc88-165">Influence values smaller than this are ignored.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="bfc88-166">**упдатескиннедмеш**</span><span class="sxs-lookup"><span data-stu-id="bfc88-166">**UpdateSkinnedMesh**</span></span>](id3dxskininfo--updateskinnedmesh.md)                       | <span data-ttu-id="bfc88-167">Применяет обложки программного обеспечения к целевым вершинам на основе текущих матриц.</span><span class="sxs-lookup"><span data-stu-id="bfc88-167">Applies software skinning to the target vertices based on the current matrices.</span></span><br/>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="bfc88-168">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bfc88-168">Remarks</span></span>

<span data-ttu-id="bfc88-169">Создание интерфейса **ID3DXSkinInfo** с помощью [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md)или [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).</span><span class="sxs-lookup"><span data-stu-id="bfc88-169">Create a **ID3DXSkinInfo** interface with [**D3DXCreateSkinInfo**](d3dxcreateskininfo.md), [**D3DXCreateSkinInfoFromBlendedMesh**](d3dxcreateskininfofromblendedmesh.md), or [**D3DXCreateSkinInfoFVF**](d3dxcreateskininfofvf.md).</span></span>

<span data-ttu-id="bfc88-170">Тип LPD3DXSKININFO определяется как указатель на интерфейс **ID3DXSkinInfo** .</span><span class="sxs-lookup"><span data-stu-id="bfc88-170">The LPD3DXSKININFO type is defined as a pointer to the **ID3DXSkinInfo** interface.</span></span>


```
typedef struct ID3DXSkinInfo *LPD3DXSKININFO;
```



## <a name="requirements"></a><span data-ttu-id="bfc88-171">Требования</span><span class="sxs-lookup"><span data-stu-id="bfc88-171">Requirements</span></span>



| <span data-ttu-id="bfc88-172">Требование</span><span class="sxs-lookup"><span data-stu-id="bfc88-172">Requirement</span></span> | <span data-ttu-id="bfc88-173">Значение</span><span class="sxs-lookup"><span data-stu-id="bfc88-173">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bfc88-174">Header</span><span class="sxs-lookup"><span data-stu-id="bfc88-174">Header</span></span><br/>  | <dl> <span data-ttu-id="bfc88-175"><dt>D3DX9Mesh. h</dt></span><span class="sxs-lookup"><span data-stu-id="bfc88-175"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bfc88-176">Библиотека</span><span class="sxs-lookup"><span data-stu-id="bfc88-176">Library</span></span><br/> | <dl> <span data-ttu-id="bfc88-177"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="bfc88-177"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bfc88-178">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bfc88-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bfc88-179">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="bfc88-179">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
