---
description: Приложения используют методы интерфейса ID3DXFileSaveData для добавления объектов данных в качестве дочерних элементов узла данных файла. x.
ms.assetid: ab5bdd9a-496a-4ae1-b93a-fe5856bd97d4
title: Интерфейс ID3DXFileSaveData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d42f431dbb2f9108c5e503aea07ba6b11915f0ac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694142"
---
# <a name="id3dxfilesavedata-interface"></a><span data-ttu-id="11410-103">Интерфейс ID3DXFileSaveData</span><span class="sxs-lookup"><span data-stu-id="11410-103">ID3DXFileSaveData interface</span></span>

<span data-ttu-id="11410-104">Приложения используют методы интерфейса ID3DXFileSaveData для добавления объектов данных в качестве дочерних элементов узла данных файла. x.</span><span class="sxs-lookup"><span data-stu-id="11410-104">Applications use the methods of the ID3DXFileSaveData interface to add data objects as children of a .x file data node.</span></span>

## <a name="members"></a><span data-ttu-id="11410-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="11410-105">Members</span></span>

<span data-ttu-id="11410-106">Интерфейс **ID3DXFileSaveData** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="11410-106">The **ID3DXFileSaveData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="11410-107">**ID3DXFileSaveData** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="11410-107">**ID3DXFileSaveData** also has these types of members:</span></span>

-   [<span data-ttu-id="11410-108">Методы</span><span class="sxs-lookup"><span data-stu-id="11410-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="11410-109">Методы</span><span class="sxs-lookup"><span data-stu-id="11410-109">Methods</span></span>

<span data-ttu-id="11410-110">Интерфейс **ID3DXFileSaveData** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="11410-110">The **ID3DXFileSaveData** interface has these methods.</span></span>



| <span data-ttu-id="11410-111">Метод</span><span class="sxs-lookup"><span data-stu-id="11410-111">Method</span></span>                                                          | <span data-ttu-id="11410-112">Описание</span><span class="sxs-lookup"><span data-stu-id="11410-112">Description</span></span>                                                                                                                                |
|:----------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="11410-113">**адддатаобжект**</span><span class="sxs-lookup"><span data-stu-id="11410-113">**AddDataObject**</span></span>](id3dxfilesavedata--adddataobject.md)       | <span data-ttu-id="11410-114">Добавляет объект данных в качестве дочернего элемента для узла данных файла **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="11410-114">Adds a data object as a child of the **ID3DXFileSaveData** file data node.</span></span><br/>                                                      |
| [<span data-ttu-id="11410-115">**адддатареференце**</span><span class="sxs-lookup"><span data-stu-id="11410-115">**AddDataReference**</span></span>](id3dxfilesavedata--adddatareference.md) | <span data-ttu-id="11410-116">Добавляет ссылку на данные в качестве дочернего элемента для этого узла данных **ID3DXFileSaveData** File.</span><span class="sxs-lookup"><span data-stu-id="11410-116">Adds a data reference as a child of this **ID3DXFileSaveData** file data node.</span></span> <span data-ttu-id="11410-117">Ссылка на данные указывает на объект данных файла.</span><span class="sxs-lookup"><span data-stu-id="11410-117">The data reference points to a file data object.</span></span><br/> |
| [<span data-ttu-id="11410-118">**GetId**</span><span class="sxs-lookup"><span data-stu-id="11410-118">**GetId**</span></span>](id3dxfilesavedata--getid.md)                       | <span data-ttu-id="11410-119">Извлекает идентификатор GUID для этого узла данных файла **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="11410-119">Retrieves the GUID of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="11410-120">**GetName**</span><span class="sxs-lookup"><span data-stu-id="11410-120">**GetName**</span></span>](id3dxfilesavedata--getname.md)                   | <span data-ttu-id="11410-121">Извлекает имя этого узла данных файла **ID3DXFileSaveData** .</span><span class="sxs-lookup"><span data-stu-id="11410-121">Retrieves the name of this **ID3DXFileSaveData** file data node.</span></span><br/>                                                                |
| [<span data-ttu-id="11410-122">**Сохранение**</span><span class="sxs-lookup"><span data-stu-id="11410-122">**GetSave**</span></span>](id3dxfilesavedata--getsave.md)                   | <span data-ttu-id="11410-123">Получает указатель на этот узел данных файла [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="11410-123">Retrieves a pointer to this [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) file data node.</span></span><br/>                                  |
| [<span data-ttu-id="11410-124">**GetType**</span><span class="sxs-lookup"><span data-stu-id="11410-124">**GetType**</span></span>](id3dxfilesavedata--gettype.md)                   | <span data-ttu-id="11410-125">Получает идентификатор шаблона для этого узла файловых данных.</span><span class="sxs-lookup"><span data-stu-id="11410-125">Retrieves the template ID of this file data node.</span></span><br/>                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="11410-126">Комментарии</span><span class="sxs-lookup"><span data-stu-id="11410-126">Remarks</span></span>

<span data-ttu-id="11410-127">Идентификатор GUID для интерфейса ID3DXFileSaveObject — IID \_ ID3DXFileSaveObject.</span><span class="sxs-lookup"><span data-stu-id="11410-127">The GUID for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="11410-128">Тип LPD3DXFileSaveData определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="11410-128">The LPD3DXFileSaveData type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveData *LPD3DXFILESAVEDATA;
```



## <a name="requirements"></a><span data-ttu-id="11410-129">Требования</span><span class="sxs-lookup"><span data-stu-id="11410-129">Requirements</span></span>



| <span data-ttu-id="11410-130">Требование</span><span class="sxs-lookup"><span data-stu-id="11410-130">Requirement</span></span> | <span data-ttu-id="11410-131">Значение</span><span class="sxs-lookup"><span data-stu-id="11410-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="11410-132">Header</span><span class="sxs-lookup"><span data-stu-id="11410-132">Header</span></span><br/>  | <dl> <span data-ttu-id="11410-133"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="11410-133"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="11410-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="11410-134">Library</span></span><br/> | <dl> <span data-ttu-id="11410-135"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="11410-135"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="11410-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="11410-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11410-137">Файловые интерфейсы D3DX X</span><span class="sxs-lookup"><span data-stu-id="11410-137">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
