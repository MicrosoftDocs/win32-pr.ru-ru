---
description: Этот интерфейс реализуется приложением для выделения или освобождения объектов контейнера фрейма и сетки. Методы для этого вызываются во время загрузки и уничтожения иерархий фреймов.
ms.assetid: b2c4ecb7-3655-4120-b957-724a754e948a
title: Интерфейс ID3DXAllocateHierarchy (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAllocateHierarchy
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ec7fb2da335ecd84889b75e81c850d16368f31eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104081934"
---
# <a name="id3dxallocatehierarchy-interface"></a><span data-ttu-id="8899c-104">Интерфейс ID3DXAllocateHierarchy</span><span class="sxs-lookup"><span data-stu-id="8899c-104">ID3DXAllocateHierarchy interface</span></span>

<span data-ttu-id="8899c-105">Этот интерфейс реализуется приложением для выделения или освобождения объектов контейнера фрейма и сетки.</span><span class="sxs-lookup"><span data-stu-id="8899c-105">This interface is implemented by the application to allocate or free frame and mesh container objects.</span></span> <span data-ttu-id="8899c-106">Методы для этого вызываются во время загрузки и уничтожения иерархий фреймов.</span><span class="sxs-lookup"><span data-stu-id="8899c-106">Methods on this are called during loading and destroying frame hierarchies.</span></span>

## <a name="members"></a><span data-ttu-id="8899c-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="8899c-107">Members</span></span>

<span data-ttu-id="8899c-108">Интерфейс **ID3DXAllocateHierarchy** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="8899c-108">The **ID3DXAllocateHierarchy** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="8899c-109">**ID3DXAllocateHierarchy** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="8899c-109">**ID3DXAllocateHierarchy** also has these types of members:</span></span>

-   [<span data-ttu-id="8899c-110">Методы</span><span class="sxs-lookup"><span data-stu-id="8899c-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="8899c-111">Методы</span><span class="sxs-lookup"><span data-stu-id="8899c-111">Methods</span></span>

<span data-ttu-id="8899c-112">Интерфейс **ID3DXAllocateHierarchy** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="8899c-112">The **ID3DXAllocateHierarchy** interface has these methods.</span></span>



| <span data-ttu-id="8899c-113">Метод</span><span class="sxs-lookup"><span data-stu-id="8899c-113">Method</span></span>                                                                       | <span data-ttu-id="8899c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="8899c-114">Description</span></span>                                                  |
|:-----------------------------------------------------------------------------|:-------------------------------------------------------------|
| [<span data-ttu-id="8899c-115">**креатефраме**</span><span class="sxs-lookup"><span data-stu-id="8899c-115">**CreateFrame**</span></span>](id3dxallocatehierarchy--createframe.md)                   | <span data-ttu-id="8899c-116">Запрашивает выделение объекта Frame.</span><span class="sxs-lookup"><span data-stu-id="8899c-116">Requests allocation of a frame object.</span></span><br/>            |
| [<span data-ttu-id="8899c-117">**креатемешконтаинер**</span><span class="sxs-lookup"><span data-stu-id="8899c-117">**CreateMeshContainer**</span></span>](id3dxallocatehierarchy--createmeshcontainer.md)   | <span data-ttu-id="8899c-118">Запрашивает выделение объекта контейнера сетки.</span><span class="sxs-lookup"><span data-stu-id="8899c-118">Requests allocation of a mesh container object.</span></span><br/>   |
| [<span data-ttu-id="8899c-119">**дестройфраме**</span><span class="sxs-lookup"><span data-stu-id="8899c-119">**DestroyFrame**</span></span>](id3dxallocatehierarchy--destroyframe.md)                 | <span data-ttu-id="8899c-120">Запрашивает освобождение объекта Frame.</span><span class="sxs-lookup"><span data-stu-id="8899c-120">Requests deallocation of a frame object.</span></span><br/>          |
| [<span data-ttu-id="8899c-121">**дестроймешконтаинер**</span><span class="sxs-lookup"><span data-stu-id="8899c-121">**DestroyMeshContainer**</span></span>](id3dxallocatehierarchy--destroymeshcontainer.md) | <span data-ttu-id="8899c-122">Запрашивает освобождение объекта контейнера сетки.</span><span class="sxs-lookup"><span data-stu-id="8899c-122">Requests deallocation of a mesh container object.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="8899c-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8899c-123">Remarks</span></span>

<span data-ttu-id="8899c-124">Тип LPD3DXALLOCATEHIERARCHY определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8899c-124">The LPD3DXALLOCATEHIERARCHY type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXAllocateHierarchy ID3DXAllocateHierarchy;
typedef interface ID3DXAllocateHierarchy *LPD3DXALLOCATEHIERARCHY;
```



## <a name="requirements"></a><span data-ttu-id="8899c-125">Требования</span><span class="sxs-lookup"><span data-stu-id="8899c-125">Requirements</span></span>



| <span data-ttu-id="8899c-126">Требование</span><span class="sxs-lookup"><span data-stu-id="8899c-126">Requirement</span></span> | <span data-ttu-id="8899c-127">Значение</span><span class="sxs-lookup"><span data-stu-id="8899c-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8899c-128">Header</span><span class="sxs-lookup"><span data-stu-id="8899c-128">Header</span></span><br/>  | <dl> <span data-ttu-id="8899c-129"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="8899c-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="8899c-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="8899c-130">Library</span></span><br/> | <dl> <span data-ttu-id="8899c-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="8899c-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="8899c-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8899c-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8899c-133">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="8899c-133">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
