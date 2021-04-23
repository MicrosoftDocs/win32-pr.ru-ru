---
description: Приложения используют методы интерфейса ID3DXFileData для создания или доступа к немедленной иерархии объекта данных. Иерархия определяется ограничениями шаблонов.
ms.assetid: ce291e2b-b926-4502-8bee-55fe6d6d3267
title: Интерфейс ID3DXFileData (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileData
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 1764787864c059e9c7417525a1a5ab5ff862f7d2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273860"
---
# <a name="id3dxfiledata-interface"></a><span data-ttu-id="a206f-104">Интерфейс ID3DXFileData</span><span class="sxs-lookup"><span data-stu-id="a206f-104">ID3DXFileData interface</span></span>

<span data-ttu-id="a206f-105">Приложения используют методы интерфейса ID3DXFileData для создания или доступа к немедленной иерархии объекта данных.</span><span class="sxs-lookup"><span data-stu-id="a206f-105">Applications use the methods of the ID3DXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="a206f-106">Иерархия определяется ограничениями шаблонов.</span><span class="sxs-lookup"><span data-stu-id="a206f-106">Template restrictions determine the hierarchy.</span></span>

## <a name="members"></a><span data-ttu-id="a206f-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="a206f-107">Members</span></span>

<span data-ttu-id="a206f-108">Интерфейс **ID3DXFileData** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="a206f-108">The **ID3DXFileData** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="a206f-109">**ID3DXFileData** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="a206f-109">**ID3DXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="a206f-110">Методы</span><span class="sxs-lookup"><span data-stu-id="a206f-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="a206f-111">Методы</span><span class="sxs-lookup"><span data-stu-id="a206f-111">Methods</span></span>

<span data-ttu-id="a206f-112">Интерфейс **ID3DXFileData** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="a206f-112">The **ID3DXFileData** interface has these methods.</span></span>



| <span data-ttu-id="a206f-113">Метод</span><span class="sxs-lookup"><span data-stu-id="a206f-113">Method</span></span>                                            | <span data-ttu-id="a206f-114">Описание</span><span class="sxs-lookup"><span data-stu-id="a206f-114">Description</span></span>                                                                                                          |
|:--------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a206f-115">**GetChild**</span><span class="sxs-lookup"><span data-stu-id="a206f-115">**GetChild**</span></span>](id3dxfiledata--getchild.md)       | <span data-ttu-id="a206f-116">Извлекает дочерний объект в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="a206f-116">Retrieves a child object in this file data object.</span></span><br/>                                                        |
| [<span data-ttu-id="a206f-117">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="a206f-117">**GetChildren**</span></span>](id3dxfiledata--getchildren.md) | <span data-ttu-id="a206f-118">Возвращает количество дочерних элементов в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="a206f-118">Retrieves the number of children in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="a206f-119">**Перечисление**</span><span class="sxs-lookup"><span data-stu-id="a206f-119">**GetEnum**</span></span>](id3dxfiledata--getenum.md)         | <span data-ttu-id="a206f-120">Извлекает объект перечисления в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="a206f-120">Retrieves the enumeration object in this file data object.</span></span><br/>                                                |
| [<span data-ttu-id="a206f-121">**GetId**</span><span class="sxs-lookup"><span data-stu-id="a206f-121">**GetId**</span></span>](id3dxfiledata--getid.md)             | <span data-ttu-id="a206f-122">Извлекает идентификатор GUID для этого файлового объекта данных.</span><span class="sxs-lookup"><span data-stu-id="a206f-122">Retrieves the GUID of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="a206f-123">**GetName**</span><span class="sxs-lookup"><span data-stu-id="a206f-123">**GetName**</span></span>](id3dxfiledata--getname.md)         | <span data-ttu-id="a206f-124">Извлекает имя этого файлового объекта данных.</span><span class="sxs-lookup"><span data-stu-id="a206f-124">Retrieves the name of this file data object.</span></span><br/>                                                              |
| [<span data-ttu-id="a206f-125">**GetType**</span><span class="sxs-lookup"><span data-stu-id="a206f-125">**GetType**</span></span>](id3dxfiledata--gettype.md)         | <span data-ttu-id="a206f-126">Получает идентификатор шаблона в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="a206f-126">Retrieves the template ID in this file data object.</span></span><br/>                                                       |
| [<span data-ttu-id="a206f-127">**IsReference**</span><span class="sxs-lookup"><span data-stu-id="a206f-127">**IsReference**</span></span>](id3dxfiledata--isreference.md) | <span data-ttu-id="a206f-128">Указывает, является ли данный файловый объект данных ссылочным объектом, указывающим на другой дочерний объект данных.</span><span class="sxs-lookup"><span data-stu-id="a206f-128">Indicates whether this file data object is a reference object that points to another child data object.</span></span><br/>   |
| [<span data-ttu-id="a206f-129">**Блокировка**</span><span class="sxs-lookup"><span data-stu-id="a206f-129">**Lock**</span></span>](id3dxfiledata--lock.md)               | <span data-ttu-id="a206f-130">Обращается к данным файла. x.</span><span class="sxs-lookup"><span data-stu-id="a206f-130">Accesses the .x file data.</span></span><br/>                                                                                |
| [<span data-ttu-id="a206f-131">**Блокирован**</span><span class="sxs-lookup"><span data-stu-id="a206f-131">**Unlock**</span></span>](id3dxfiledata--unlock.md)           | <span data-ttu-id="a206f-132">Завершает срок существования указателя *ппдата* , возвращенного [**ID3DXFileData:: Lock**](id3dxfiledata--lock.md).</span><span class="sxs-lookup"><span data-stu-id="a206f-132">Ends the lifespan of the *ppData* pointer returned by [**ID3DXFileData::Lock**](id3dxfiledata--lock.md).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="a206f-133">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a206f-133">Remarks</span></span>

<span data-ttu-id="a206f-134">Типы данных, разрешенные шаблоном, называются необязательными членами.</span><span class="sxs-lookup"><span data-stu-id="a206f-134">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="a206f-135">Необязательные элементы не являются обязательными, но объект может пропустить важную информацию без них.</span><span class="sxs-lookup"><span data-stu-id="a206f-135">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="a206f-136">Эти необязательные члены сохраняются как дочерние элементы объекта данных.</span><span class="sxs-lookup"><span data-stu-id="a206f-136">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="a206f-137">Дочерний элемент может быть другим объектом данных или ссылкой на более раннюю версию объекта данных.</span><span class="sxs-lookup"><span data-stu-id="a206f-137">A child can be another data object or a reference to an earlier data object.</span></span>

<span data-ttu-id="a206f-138">Идентификатор GUID для интерфейса ID3DXFileData — IID \_ ID3DXFileData.</span><span class="sxs-lookup"><span data-stu-id="a206f-138">The GUID for the ID3DXFileData interface is IID\_ID3DXFileData.</span></span>

<span data-ttu-id="a206f-139">Тип LPD3DXFILEDATA определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="a206f-139">The LPD3DXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileData *LPD3DXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="a206f-140">Требования</span><span class="sxs-lookup"><span data-stu-id="a206f-140">Requirements</span></span>



| <span data-ttu-id="a206f-141">Требование</span><span class="sxs-lookup"><span data-stu-id="a206f-141">Requirement</span></span> | <span data-ttu-id="a206f-142">Значение</span><span class="sxs-lookup"><span data-stu-id="a206f-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a206f-143">Header</span><span class="sxs-lookup"><span data-stu-id="a206f-143">Header</span></span><br/>  | <dl> <span data-ttu-id="a206f-144"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="a206f-144"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="a206f-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="a206f-145">Library</span></span><br/> | <dl> <span data-ttu-id="a206f-146"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a206f-146"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="a206f-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a206f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a206f-148">Файловые интерфейсы D3DX X</span><span class="sxs-lookup"><span data-stu-id="a206f-148">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
