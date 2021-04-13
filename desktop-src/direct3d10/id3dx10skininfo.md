---
description: ID3DX10SkinInfo позволяет оптимизировать, обрабатывать и вручную устанавливать связи между костями и вершинами в ваших сетках (см. статью анимация скелетообразных в Википедии).
ms.assetid: bea0fe71-c201-45c6-8036-d0d76d5851fd
title: Интерфейс ID3DX10SkinInfo (D3DX10. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10SkinInfo
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3216765ab9ef2ba9f2b0883c31a878a7eae6861f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354930"
---
# <a name="id3dx10skininfo-interface"></a><span data-ttu-id="701b5-103">Интерфейс ID3DX10SkinInfo</span><span class="sxs-lookup"><span data-stu-id="701b5-103">ID3DX10SkinInfo interface</span></span>

<span data-ttu-id="701b5-104">ID3DX10SkinInfo позволяет оптимизировать, обрабатывать и вручную устанавливать связи между костями и вершинами в ваших сетках (см. статью [анимация скелетообразных в Википедии](https://en.wikipedia.org/wiki/Skeletal_animation)).</span><span class="sxs-lookup"><span data-stu-id="701b5-104">ID3DX10SkinInfo allows you to optimize, process, and manually set the relationship between bones and vertices in your meshes (see [Skeletal Animation on Wikipedia](https://en.wikipedia.org/wiki/Skeletal_animation)).</span></span> <span data-ttu-id="701b5-105">Это наиболее полезно для создания файлов. x, экспортируемых приложениями ДКК (например, 3DS Max и Maya), более удобной для оборудования, а также для повышения скорости рендеринга в ролевых сетках в режиме рендеринга программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="701b5-105">It is most useful for making .x files exported by DCC Apps (such as 3DS Max and Maya) more hardware-friendly, and for improving the render speed of your skinned meshes in software render mode.</span></span>

## <a name="members"></a><span data-ttu-id="701b5-106">Элементы</span><span class="sxs-lookup"><span data-stu-id="701b5-106">Members</span></span>

<span data-ttu-id="701b5-107">Интерфейс **ID3DX10SkinInfo** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="701b5-107">The **ID3DX10SkinInfo** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="701b5-108">**ID3DX10SkinInfo** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="701b5-108">**ID3DX10SkinInfo** also has these types of members:</span></span>

-   [<span data-ttu-id="701b5-109">Методы</span><span class="sxs-lookup"><span data-stu-id="701b5-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="701b5-110">Методы</span><span class="sxs-lookup"><span data-stu-id="701b5-110">Methods</span></span>

<span data-ttu-id="701b5-111">Интерфейс **ID3DX10SkinInfo** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="701b5-111">The **ID3DX10SkinInfo** interface has these methods.</span></span>



| <span data-ttu-id="701b5-112">Метод</span><span class="sxs-lookup"><span data-stu-id="701b5-112">Method</span></span>                                                                   | <span data-ttu-id="701b5-113">Описание</span><span class="sxs-lookup"><span data-stu-id="701b5-113">Description</span></span>                                                                                                                        |
|:-------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="701b5-114">**аддбонеинфлуенцес**</span><span class="sxs-lookup"><span data-stu-id="701b5-114">**AddBoneInfluences**</span></span>](id3dx10skininfo-addboneinfluences.md)           | <span data-ttu-id="701b5-115">Включите существующую кость, чтобы она влияла на группу вершин, и определите, насколько сильно влияют на эту кость на каждой вершине.</span><span class="sxs-lookup"><span data-stu-id="701b5-115">Enable an existing bone to influence a group of vertices and define how much influence the bone has on each vertex.</span></span><br/>     |
| [<span data-ttu-id="701b5-116">**аддбонес**</span><span class="sxs-lookup"><span data-stu-id="701b5-116">**AddBones**</span></span>](id3dx10skininfo-addbones.md)                             | <span data-ttu-id="701b5-117">Выделение пространства для дополнительных костей.</span><span class="sxs-lookup"><span data-stu-id="701b5-117">Allocate space for more bones.</span></span><br/>                                                                                          |
| [<span data-ttu-id="701b5-118">**аддвертицес**</span><span class="sxs-lookup"><span data-stu-id="701b5-118">**AddVertices**</span></span>](id3dx10skininfo-addvertices.md)                       | <span data-ttu-id="701b5-119">Выделение пространства для дополнительных вершин.</span><span class="sxs-lookup"><span data-stu-id="701b5-119">Allocate space for additional vertices.</span></span><br/>                                                                                 |
| [<span data-ttu-id="701b5-120">**клеарбонеинфлуенцес**</span><span class="sxs-lookup"><span data-stu-id="701b5-120">**ClearBoneInfluences**</span></span>](id3dx10skininfo-clearboneinfluences.md)       | <span data-ttu-id="701b5-121">Очистите список вершин, которые она влияет на кость.</span><span class="sxs-lookup"><span data-stu-id="701b5-121">Clear a bone's list of vertices that it influences.</span></span><br/>                                                                     |
| [<span data-ttu-id="701b5-122">**Компактный**</span><span class="sxs-lookup"><span data-stu-id="701b5-122">**Compact**</span></span>](id3dx10skininfo-compact.md)                               | <span data-ttu-id="701b5-123">Ограничьте число костей, которые могут повлиять на вершину и/или ограничить объем влияния на кость на вершину.</span><span class="sxs-lookup"><span data-stu-id="701b5-123">Limit the number of bones that can influence a vertex and/or limit the amount of influence a bone can have on a vertex.</span></span><br/> |
| [<span data-ttu-id="701b5-124">**дософтварескиннинг**</span><span class="sxs-lookup"><span data-stu-id="701b5-124">**DoSoftwareSkinning**</span></span>](id3dx10skininfo-dosoftwareskinning.md)         | <span data-ttu-id="701b5-125">Выпустить программное обеспечение на массиве вершин.</span><span class="sxs-lookup"><span data-stu-id="701b5-125">Do software skinning on an array of vertices.</span></span><br/>                                                                           |
| [<span data-ttu-id="701b5-126">**финдбонеинфлуенцеиндекс**</span><span class="sxs-lookup"><span data-stu-id="701b5-126">**FindBoneInfluenceIndex**</span></span>](id3dx10skininfo-findboneinfluenceindex.md) | <span data-ttu-id="701b5-127">Найдите индекс, указывающий, где заданная вершина находится в списке заданных вершин на заданной кости.</span><span class="sxs-lookup"><span data-stu-id="701b5-127">Find the index that indicates where a given vertex is in a given bone's list of influenced vertices.</span></span><br/>                    |
| [<span data-ttu-id="701b5-128">**жетбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="701b5-128">**GetBoneInfluence**</span></span>](id3dx10skininfo-getboneinfluence.md)             | <span data-ttu-id="701b5-129">Получение суммы влияния на заданную кость на заданную вершину.</span><span class="sxs-lookup"><span data-stu-id="701b5-129">Get the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |
| [<span data-ttu-id="701b5-130">**жетбонеинфлуенцекаунт**</span><span class="sxs-lookup"><span data-stu-id="701b5-130">**GetBoneInfluenceCount**</span></span>](id3dx10skininfo-getboneinfluencecount.md)   | <span data-ttu-id="701b5-131">Возвращает количество вершин, на которые влияет заданная кость.</span><span class="sxs-lookup"><span data-stu-id="701b5-131">Get the number of vertices that a given bone influences.</span></span><br/>                                                                |
| [<span data-ttu-id="701b5-132">**жетбонеинфлуенцес**</span><span class="sxs-lookup"><span data-stu-id="701b5-132">**GetBoneInfluences**</span></span>](id3dx10skininfo-getboneinfluences.md)           | <span data-ttu-id="701b5-133">Получение списка вершин, на которые влияет заданная кость, и списка интенсивности влияния этой кости на каждую вершину.</span><span class="sxs-lookup"><span data-stu-id="701b5-133">Get a list of vertices that a given bone influences and a list of the amount of influence that bone has on each vertex.</span></span><br/> |
| [<span data-ttu-id="701b5-134">**жетмаксбонеинфлуенцес**</span><span class="sxs-lookup"><span data-stu-id="701b5-134">**GetMaxBoneInfluences**</span></span>](id3dx10skininfo-getmaxboneinfluences.md)     | <span data-ttu-id="701b5-135">Получите число вершин, которые могут максимально повлиять на кость.</span><span class="sxs-lookup"><span data-stu-id="701b5-135">Get the number of vertices a bone can maximally influence.</span></span><br/>                                                              |
| [<span data-ttu-id="701b5-136">**жетнумбонес**</span><span class="sxs-lookup"><span data-stu-id="701b5-136">**GetNumBones**</span></span>](id3dx10skininfo-getnumbones.md)                       | <span data-ttu-id="701b5-137">Возвращает число костей в ID3DX10SkinInfo.</span><span class="sxs-lookup"><span data-stu-id="701b5-137">Get the number of bones in ID3DX10SkinInfo.</span></span><br/>                                                                             |
| [<span data-ttu-id="701b5-138">**жетнумвертицес**</span><span class="sxs-lookup"><span data-stu-id="701b5-138">**GetNumVertices**</span></span>](id3dx10skininfo-getnumvertices.md)                 | <span data-ttu-id="701b5-139">Возвращает количество вершин в ID3DX10SkinInfo.</span><span class="sxs-lookup"><span data-stu-id="701b5-139">Get the number of vertices in ID3DX10SkinInfo.</span></span><br/>                                                                          |
| [<span data-ttu-id="701b5-140">**ремапбонес**</span><span class="sxs-lookup"><span data-stu-id="701b5-140">**RemapBones**</span></span>](id3dx10skininfo-remapbones.md)                         | <span data-ttu-id="701b5-141">Изменение того, какие кости влияют на вершины.</span><span class="sxs-lookup"><span data-stu-id="701b5-141">Change which bones influence which vertices.</span></span><br/>                                                                            |
| [<span data-ttu-id="701b5-142">**ремапвертицес**</span><span class="sxs-lookup"><span data-stu-id="701b5-142">**RemapVertices**</span></span>](id3dx10skininfo-remapvertices.md)                   | <span data-ttu-id="701b5-143">Изменение вершин, на которые влияют эти кости.</span><span class="sxs-lookup"><span data-stu-id="701b5-143">Change which vertices are influenced by which bones.</span></span><br/>                                                                    |
| [<span data-ttu-id="701b5-144">**ремовебоне**</span><span class="sxs-lookup"><span data-stu-id="701b5-144">**RemoveBone**</span></span>](id3dx10skininfo-removebone.md)                         | <span data-ttu-id="701b5-145">Удалить кость.</span><span class="sxs-lookup"><span data-stu-id="701b5-145">Remove a bone.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="701b5-146">**сетбонеинфлуенце**</span><span class="sxs-lookup"><span data-stu-id="701b5-146">**SetBoneInfluence**</span></span>](id3dx10skininfo-setboneinfluence.md)             | <span data-ttu-id="701b5-147">Установка объема влияния на заданную кость на заданную вершину.</span><span class="sxs-lookup"><span data-stu-id="701b5-147">Set the amount of influence a given bone has over a given vertex.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="701b5-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="701b5-148">Remarks</span></span>

<span data-ttu-id="701b5-149">Создание интерфейса ID3DX10SkinInfo с помощью [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh** или **D3DX10CreateSkinInfoFVF**.</span><span class="sxs-lookup"><span data-stu-id="701b5-149">Create a ID3DX10SkinInfo interface with [**D3DX10CreateSkinInfo**](d3d10-d3dx10createskininfo.md), **D3DX10CreateSkinInfoFromBlendedMesh**, or **D3DX10CreateSkinInfoFVF**.</span></span>

<span data-ttu-id="701b5-150">Тип LPD3DX10SKININFO определяется как указатель на интерфейс **ID3DX10SkinInfo** .</span><span class="sxs-lookup"><span data-stu-id="701b5-150">The LPD3DX10SKININFO type is defined as a pointer to the **ID3DX10SkinInfo** interface.</span></span>


```
typedef struct ID3DX10SkinInfo *LPD3DX10SKININFO;
```



## <a name="requirements"></a><span data-ttu-id="701b5-151">Требования</span><span class="sxs-lookup"><span data-stu-id="701b5-151">Requirements</span></span>



| <span data-ttu-id="701b5-152">Требование</span><span class="sxs-lookup"><span data-stu-id="701b5-152">Requirement</span></span> | <span data-ttu-id="701b5-153">Значение</span><span class="sxs-lookup"><span data-stu-id="701b5-153">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="701b5-154">Header</span><span class="sxs-lookup"><span data-stu-id="701b5-154">Header</span></span><br/>  | <dl> <span data-ttu-id="701b5-155"><dt>D3DX10. h</dt></span><span class="sxs-lookup"><span data-stu-id="701b5-155"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="701b5-156">Библиотека</span><span class="sxs-lookup"><span data-stu-id="701b5-156">Library</span></span><br/> | <dl> <span data-ttu-id="701b5-157"><dt>D3DX10. lib</dt></span><span class="sxs-lookup"><span data-stu-id="701b5-157"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="701b5-158">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="701b5-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="701b5-159">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="701b5-159">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
