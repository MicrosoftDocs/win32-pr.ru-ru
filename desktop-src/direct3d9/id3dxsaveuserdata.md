---
description: Интерфейс ID3DXSaveUserData. Этот интерфейс реализуется приложением для сохранения дополнительных пользовательских данных, внедренных в файлы. x.
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
ms.openlocfilehash: 5dbdc71239455772809e44f535634a0d06cc0653
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107182"
---
# <a name="id3dxsaveuserdata-interface"></a><span data-ttu-id="21260-103">Интерфейс ID3DXSaveUserData</span><span class="sxs-lookup"><span data-stu-id="21260-103">ID3DXSaveUserData interface</span></span>

<span data-ttu-id="21260-104">Этот интерфейс реализуется приложением для сохранения любых дополнительных пользовательских данных, внедренных в файлы. x.</span><span class="sxs-lookup"><span data-stu-id="21260-104">This interface is implemented by the application to save any additional user data embedded in .x files.</span></span> <span data-ttu-id="21260-105">Экземпляр этого интерфейса передается в [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), и D3DX вызывает соответствующий метод для этого интерфейса каждый раз при обнаружении соответствующих данных.</span><span class="sxs-lookup"><span data-stu-id="21260-105">An instance of this interface is passed to [**D3DXSaveMeshHierarchyToFile**](d3dxsavemeshhierarchytofile.md), and D3DX calls the appropriate method on this interface every time the appropriate data is encountered.</span></span> <span data-ttu-id="21260-106">Например, для каждого объекта Frame в файле. x вызывается [**ID3DXSaveUserData:: аддфрамечилддата**](id3dxsaveuserdata--addframechilddata.md) и ему передаются дочерние данные.</span><span class="sxs-lookup"><span data-stu-id="21260-106">For example, for each frame object in the .x file, [**ID3DXSaveUserData::AddFrameChildData**](id3dxsaveuserdata--addframechilddata.md) is called and passed the child data.</span></span>

## <a name="members"></a><span data-ttu-id="21260-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="21260-107">Members</span></span>

<span data-ttu-id="21260-108">Интерфейс **ID3DXSaveUserData** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="21260-108">The **ID3DXSaveUserData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="21260-109">**ID3DXSaveUserData** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="21260-109">**ID3DXSaveUserData** also has these types of members:</span></span>

-   [<span data-ttu-id="21260-110">Методы</span><span class="sxs-lookup"><span data-stu-id="21260-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="21260-111">Методы</span><span class="sxs-lookup"><span data-stu-id="21260-111">Methods</span></span>

<span data-ttu-id="21260-112">Интерфейс **ID3DXSaveUserData** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="21260-112">The **ID3DXSaveUserData** interface has these methods.</span></span>



| <span data-ttu-id="21260-113">Метод</span><span class="sxs-lookup"><span data-stu-id="21260-113">Method</span></span>                                                                              | <span data-ttu-id="21260-114">Описание</span><span class="sxs-lookup"><span data-stu-id="21260-114">Description</span></span>                                                        |
|:------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="21260-115">**аддфрамечилддата**</span><span class="sxs-lookup"><span data-stu-id="21260-115">**AddFrameChildData**</span></span>](id3dxsaveuserdata--addframechilddata.md)                   | <span data-ttu-id="21260-116">Добавьте дочерние данные в рамку.</span><span class="sxs-lookup"><span data-stu-id="21260-116">Add child data to the frame.</span></span><br/>                            |
| [<span data-ttu-id="21260-117">**аддмешчилддата**</span><span class="sxs-lookup"><span data-stu-id="21260-117">**AddMeshChildData**</span></span>](id3dxsaveuserdata--addmeshchilddata.md)                     | <span data-ttu-id="21260-118">Добавление дочерних данных в сетку.</span><span class="sxs-lookup"><span data-stu-id="21260-118">Add child data to the mesh.</span></span><br/>                             |
| [<span data-ttu-id="21260-119">**аддтоплевелдатаобжектспост**</span><span class="sxs-lookup"><span data-stu-id="21260-119">**AddTopLevelDataObjectsPost**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspost.md) | <span data-ttu-id="21260-120">Добавьте объект верхнего уровня после иерархии Frame.</span><span class="sxs-lookup"><span data-stu-id="21260-120">Add a top level object after the frame hierarchy.</span></span><br/>       |
| [<span data-ttu-id="21260-121">**аддтоплевелдатаобжектспре**</span><span class="sxs-lookup"><span data-stu-id="21260-121">**AddTopLevelDataObjectsPre**</span></span>](id3dxsaveuserdata--addtopleveldataobjectspre.md)   | <span data-ttu-id="21260-122">Добавьте объект верхнего уровня перед иерархией Frame.</span><span class="sxs-lookup"><span data-stu-id="21260-122">Add a top level object before the frame hierarchy.</span></span><br/>      |
| [<span data-ttu-id="21260-123">**регистертемплатес**</span><span class="sxs-lookup"><span data-stu-id="21260-123">**RegisterTemplates**</span></span>](id3dxsaveuserdata--registertemplates.md)                   | <span data-ttu-id="21260-124">Обратный вызов, позволяющий пользователю зарегистрировать шаблон файла. x.</span><span class="sxs-lookup"><span data-stu-id="21260-124">A callback for the user to register a .x file template.</span></span><br/> |
| [<span data-ttu-id="21260-125">**саветемплатес**</span><span class="sxs-lookup"><span data-stu-id="21260-125">**SaveTemplates**</span></span>](id3dxsaveuserdata--savetemplates.md)                           | <span data-ttu-id="21260-126">Обратный вызов для пользователя при сохранении шаблона файла. x.</span><span class="sxs-lookup"><span data-stu-id="21260-126">A callback for the user to save a .x file template.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="21260-127">Remarks</span><span class="sxs-lookup"><span data-stu-id="21260-127">Remarks</span></span>

<span data-ttu-id="21260-128">Тип LPD3DXSAVEUSERDATA определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="21260-128">The LPD3DXSAVEUSERDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXSaveUserData ID3DXSaveUserData;
typedef interface ID3DXSaveUserData *LPD3DXSAVEUSERDATA;
```



## <a name="requirements"></a><span data-ttu-id="21260-129">Требования</span><span class="sxs-lookup"><span data-stu-id="21260-129">Requirements</span></span>



| <span data-ttu-id="21260-130">Требование</span><span class="sxs-lookup"><span data-stu-id="21260-130">Requirement</span></span> | <span data-ttu-id="21260-131">Значение</span><span class="sxs-lookup"><span data-stu-id="21260-131">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="21260-132">Header</span><span class="sxs-lookup"><span data-stu-id="21260-132">Header</span></span><br/>  | <dl> <span data-ttu-id="21260-133"><dt>D3dx9anim. h</dt></span><span class="sxs-lookup"><span data-stu-id="21260-133"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="21260-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="21260-134">Library</span></span><br/> | <dl> <span data-ttu-id="21260-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="21260-135"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="21260-136">См. также</span><span class="sxs-lookup"><span data-stu-id="21260-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21260-137">Интерфейсы D3DX</span><span class="sxs-lookup"><span data-stu-id="21260-137">D3DX Interfaces</span></span>](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
