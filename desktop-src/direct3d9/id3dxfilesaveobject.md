---
description: Приложения используют методы интерфейса ID3DXFileSaveObject для записи файла. x на диск, а также для добавления и сохранения объектов и шаблонов данных.
ms.assetid: 1131c151-fa21-4654-9776-484922d58487
title: Интерфейс ID3DXFileSaveObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileSaveObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f8d657c327c75045cf4feb2080a2e57d80f752df
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713654"
---
# <a name="id3dxfilesaveobject-interface"></a><span data-ttu-id="05541-103">Интерфейс ID3DXFileSaveObject</span><span class="sxs-lookup"><span data-stu-id="05541-103">ID3DXFileSaveObject interface</span></span>

<span data-ttu-id="05541-104">Приложения используют методы интерфейса ID3DXFileSaveObject для записи файла. x на диск, а также для добавления и сохранения объектов и шаблонов данных.</span><span class="sxs-lookup"><span data-stu-id="05541-104">Applications use the methods of the ID3DXFileSaveObject interface to write a .x file to disk, and to add and save data objects and templates.</span></span>

## <a name="members"></a><span data-ttu-id="05541-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="05541-105">Members</span></span>

<span data-ttu-id="05541-106">Интерфейс **ID3DXFileSaveObject** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="05541-106">The **ID3DXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="05541-107">**ID3DXFileSaveObject** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="05541-107">**ID3DXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="05541-108">Методы</span><span class="sxs-lookup"><span data-stu-id="05541-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="05541-109">Методы</span><span class="sxs-lookup"><span data-stu-id="05541-109">Methods</span></span>

<span data-ttu-id="05541-110">Интерфейс **ID3DXFileSaveObject** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="05541-110">The **ID3DXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="05541-111">Метод</span><span class="sxs-lookup"><span data-stu-id="05541-111">Method</span></span>                                                      | <span data-ttu-id="05541-112">Описание</span><span class="sxs-lookup"><span data-stu-id="05541-112">Description</span></span>                                                                                                                  |
|:------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05541-113">**адддатаобжект**</span><span class="sxs-lookup"><span data-stu-id="05541-113">**AddDataObject**</span></span>](id3dxfilesaveobject--adddataobject.md) | <span data-ttu-id="05541-114">Добавляет объект данных в качестве дочернего элемента для объекта [**ID3DXFileSaveData**](id3dxfilesavedata.md) .</span><span class="sxs-lookup"><span data-stu-id="05541-114">Adds a data object as a child of the [**ID3DXFileSaveData**](id3dxfilesavedata.md) object.</span></span><br/>                       |
| [<span data-ttu-id="05541-115">**Файл.**</span><span class="sxs-lookup"><span data-stu-id="05541-115">**GetFile**</span></span>](id3dxfilesaveobject--getfile.md)             | <span data-ttu-id="05541-116">Возвращает интерфейс [**ID3DXFile**](id3dxfile.md) объекта, который создал этот объект **ID3DXFileSaveObject** .</span><span class="sxs-lookup"><span data-stu-id="05541-116">Gets the [**ID3DXFile**](id3dxfile.md) interface of the object that created this **ID3DXFileSaveObject** object.</span></span><br/> |
| [<span data-ttu-id="05541-117">**Сохранить**</span><span class="sxs-lookup"><span data-stu-id="05541-117">**Save**</span></span>](id3dxfilesaveobject--save.md)                   | <span data-ttu-id="05541-118">Сохраняет объект данных и его дочерние элементы в файл. x на диске.</span><span class="sxs-lookup"><span data-stu-id="05541-118">Saves a data object and its children to a .x file on disk.</span></span><br/>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="05541-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="05541-119">Remarks</span></span>

<span data-ttu-id="05541-120">Шаблоны не являются обязательными для каждого файла.</span><span class="sxs-lookup"><span data-stu-id="05541-120">Templates are not required in every file.</span></span> <span data-ttu-id="05541-121">Например, можно разместить все шаблоны в одном файле x, а не дублировать их в каждый файл. x.</span><span class="sxs-lookup"><span data-stu-id="05541-121">For example, you could put all templates into a single .x file rather than duplicating them in every .x file.</span></span>

<span data-ttu-id="05541-122">Интерфейс ID3DXFileSaveObject получается путем вызова метода [**ID3DXFile:: креатесавеобжект**](id3dxfile--createsaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="05541-122">The ID3DXFileSaveObject interface is obtained by calling the [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="05541-123">Глобальный уникальный идентификатор (GUID) для интерфейса ID3DXFileSaveObject — IID \_ ID3DXFileSaveObject.</span><span class="sxs-lookup"><span data-stu-id="05541-123">The globally unique identifier (GUID) for the ID3DXFileSaveObject interface is IID\_ID3DXFileSaveObject.</span></span>

<span data-ttu-id="05541-124">Тип LPD3DXFILESAVEOBJECT определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="05541-124">The LPD3DXFILESAVEOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileSaveObject *LPD3DXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="05541-125">Требования</span><span class="sxs-lookup"><span data-stu-id="05541-125">Requirements</span></span>



| <span data-ttu-id="05541-126">Требование</span><span class="sxs-lookup"><span data-stu-id="05541-126">Requirement</span></span> | <span data-ttu-id="05541-127">Значение</span><span class="sxs-lookup"><span data-stu-id="05541-127">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="05541-128">Header</span><span class="sxs-lookup"><span data-stu-id="05541-128">Header</span></span><br/>  | <dl> <span data-ttu-id="05541-129"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="05541-129"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="05541-130">Библиотека</span><span class="sxs-lookup"><span data-stu-id="05541-130">Library</span></span><br/> | <dl> <span data-ttu-id="05541-131"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="05541-131"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="05541-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05541-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05541-133">Файловые интерфейсы D3DX X</span><span class="sxs-lookup"><span data-stu-id="05541-133">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
