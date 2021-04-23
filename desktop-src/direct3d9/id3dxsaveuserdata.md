---
description: Этот интерфейс реализуется приложением для сохранения любых дополнительных пользовательских данных, внедренных в файлы. x.
ms.assetid: 6294f942-9c14-4eed-92a8-af2821fd7e13
title: Интерфейс ID3DXSaveUserData (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSaveUserData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 77529a5a7b260dd27dc4af1752c88f55117bc974
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105664969"
---
# <a name="id3dxsaveuserdata-interface"></a><span data-ttu-id="2925c-103">Интерфейс ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="2925c-103">ID3DXSaveUserData interface</span></span>

<span data-ttu-id="2925c-104">Этот интерфейс реализуется приложением для сохранения любых дополнительных пользовательских данных, внедренных в файлы. x.</span><span class="sxs-lookup"><span data-stu-id="2925c-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="2925c-105">Экземпляр этого интерфейса передается в [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), и D3DX вызывает соответствующий метод для этого интерфейса каждый раз при обнаружении соответствующих данных.</span><span class="sxs-lookup"><span data-stu-id="2925c-105">An instance of this interface is passed to [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="2925c-106">Например, для каждого объекта Frame в файле. x вызывается [**ID3DXSaveUserData:: аддфрамечилддата**](id3dxsaveuserdata--addframechilddata.md) и ему передаются дочерние данные.</span><span class="sxs-lookup"><span data-stu-id="2925c-106">For example, for each frame object in the .x file, [**ID3DXSaveUserData::AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="2925c-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="2925c-107">Members</span></span>

<span data-ttu-id="2925c-108">Интерфейс **ID3DXSaveUserData** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="2925c-108">The **ID3DXSaveUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="2925c-109">**ID3DXSaveUserData** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="2925c-109">**ID3DXSaveUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="2925c-110">Методы</span><span class="sxs-lookup"><span data-stu-id="2925c-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="2925c-111">Методы</span><span class="sxs-lookup"><span data-stu-id="2925c-111">Methods</span></span>

<span data-ttu-id="2925c-112">Интерфейс **ID3DXSaveUserData** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="2925c-112">The **ID3DXSaveUserData** interface has these methods.</span></span>



| <span data-ttu-id="2925c-113">Метод</span><span class="sxs-lookup"><span data-stu-id="2925c-113">Method</span></span>                                                                              | <span data-ttu-id="2925c-114">Описание</span><span class="sxs-lookup"><span data-stu-id="2925c-114">Description</span></span>                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="2925c-115">**аддфрамечилддата**</span><span class="sxs-lookup"><span data-stu-id="2925c-115">**AddFrameChildData**</span></span>](id3dxsaveuserdata--addframechilddata.md)                   | <span data-ttu-id="2925c-116">Добавьте дочерние данные в рамку.</span><span class="sxs-lookup"><span data-stu-id="2925c-116">Add child data to the frame.</span></span><br/>                            |
| [<span data-ttu-id="2925c-117">**аддмешчилддата**</span><span class="sxs-lookup"><span data-stu-id="2925c-117">**AddMeshChildData**</span></span>](id3dxsaveuserdata--addmeshchilddata.md)                     | <span data-ttu-id="2925c-118">Добавление дочерних данных в сетку.</span><span class="sxs-lookup"><span data-stu-id="2925c-118">Add child data to the mesh.</span></span><br/>                             |
| [<span data-ttu-id="2925c-119">**аддтоплевелдатаобжектспост**</span><span class="sxs-lookup"><span data-stu-id="2925c-119">**AddTopLevelDataObjectsPost**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspost.md) | <span data-ttu-id="2925c-120">Добавьте объект верхнего уровня после иерархии Frame.</span><span class="sxs-lookup"><span data-stu-id="2925c-120">Add a top level object after the frame hierarchy.</span></span><br/>       |
| [<span data-ttu-id="2925c-121">**аддтоплевелдатаобжектспре**</span><span class="sxs-lookup"><span data-stu-id="2925c-121">**AddTopLevelDataObjectsPre**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | <span data-ttu-id="2925c-122">Добавьте объект верхнего уровня перед иерархией Frame.</span><span class="sxs-lookup"><span data-stu-id="2925c-122">Add a top level object before the frame hierarchy.</span></span><br/>      |
| [<span data-ttu-id="2925c-123">**регистертемплатес**</span><span class="sxs-lookup"><span data-stu-id="2925c-123">**RegisterTemplates**</span></span>](id3dxsaveuserdata--registertemplates.md)                   | <span data-ttu-id="2925c-124">Обратный вызов, позволяющий пользователю зарегистрировать шаблон файла. x.</span><span class="sxs-lookup"><span data-stu-id="2925c-124">A callback for the user to register a .x file template.</span></span><br/> |
| [<span data-ttu-id="2925c-125">**саветемплатес**</span><span class="sxs-lookup"><span data-stu-id="2925c-125">**SaveTemplates**</span></span>](id3dxsaveuserdata--savetemplates.md)                           | <span data-ttu-id="2925c-126">Обратный вызов для пользователя при сохранении шаблона файла. x.</span><span class="sxs-lookup"><span data-stu-id="2925c-126">A callback for the user to save a .x file template.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="2925c-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2925c-127">Remarks</span></span>

<span data-ttu-id="2925c-128">Тип LPD3DXSAVEUSERDATA определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2925c-128">The LPD3DXSAVEUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="2925c-129">Требования</span><span class="sxs-lookup"><span data-stu-id="2925c-129">Requirements</span></span>



| <span data-ttu-id="2925c-130">Требование</span><span class="sxs-lookup"><span data-stu-id="2925c-130">Requirement</span></span> | <span data-ttu-id="2925c-131">Значение</span><span class="sxs-lookup"><span data-stu-id="2925c-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2925c-132">Header</span><span class="sxs-lookup"><span data-stu-id="2925c-132">Header</span></span><br/>  | <dl> <span data-ttu-id="2925c-133"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="2925c-133"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="2925c-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="2925c-134">Library</span></span><br/> | <dl> <span data-ttu-id="2925c-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2925c-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="2925c-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2925c-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2925c-137">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="2925c-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
