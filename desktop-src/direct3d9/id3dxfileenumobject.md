---
description: Приложения используют методы интерфейса ID3DXFileEnumObject для прохода по объектам данных дочерних файлов в файле и для получения дочернего объекта по его глобальному уникальному идентификатору (GUID) или по имени.
ms.assetid: 23b28f07-5832-4163-953b-615d20e781f6
title: Интерфейс ID3DXFileEnumObject (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFileEnumObject
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f9b28f94c8d514f81aaa51426557c825da91c4bf
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000417"
---
# <a name="id3dxfileenumobject-interface"></a><span data-ttu-id="55cf0-103">Интерфейс ID3DXFileEnumObject</span><span class="sxs-lookup"><span data-stu-id="55cf0-103">ID3DXFileEnumObject interface</span></span>

<span data-ttu-id="55cf0-104">Приложения используют методы интерфейса ID3DXFileEnumObject для прохода по объектам данных дочерних файлов в файле и для получения дочернего объекта по его глобальному уникальному идентификатору (GUID) или по имени.</span><span class="sxs-lookup"><span data-stu-id="55cf0-104">Applications use the methods of the ID3DXFileEnumObject interface to cycle through the child file data objects in the file and to retrieve a child object by its globally unique identifier (GUID) or by its name.</span></span>

## <a name="members"></a><span data-ttu-id="55cf0-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="55cf0-105">Members</span></span>

<span data-ttu-id="55cf0-106">Интерфейс **ID3DXFileEnumObject** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="55cf0-106">The **ID3DXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="55cf0-107">**ID3DXFileEnumObject** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="55cf0-107">**ID3DXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="55cf0-108">Методы</span><span class="sxs-lookup"><span data-stu-id="55cf0-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="55cf0-109">Методы</span><span class="sxs-lookup"><span data-stu-id="55cf0-109">Methods</span></span>

<span data-ttu-id="55cf0-110">Интерфейс **ID3DXFileEnumObject** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="55cf0-110">The **ID3DXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="55cf0-111">Метод</span><span class="sxs-lookup"><span data-stu-id="55cf0-111">Method</span></span>                                                                  | <span data-ttu-id="55cf0-112">Описание</span><span class="sxs-lookup"><span data-stu-id="55cf0-112">Description</span></span>                                                                |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------|
| [<span data-ttu-id="55cf0-113">**GetChild**</span><span class="sxs-lookup"><span data-stu-id="55cf0-113">**GetChild**</span></span>](id3dxfileenumobject--getchild.md)                       | <span data-ttu-id="55cf0-114">Извлекает дочерний объект в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="55cf0-114">Retrieves a child object in this file data object.</span></span><br/>              |
| [<span data-ttu-id="55cf0-115">**GetChildren**</span><span class="sxs-lookup"><span data-stu-id="55cf0-115">**GetChildren**</span></span>](id3dxfileenumobject--getchildren.md)                 | <span data-ttu-id="55cf0-116">Возвращает количество дочерних объектов в этом объекте данных файла.</span><span class="sxs-lookup"><span data-stu-id="55cf0-116">Retrieves the number of child objects in this file data object.</span></span><br/> |
| [<span data-ttu-id="55cf0-117">**жетдатаобжектбид**</span><span class="sxs-lookup"><span data-stu-id="55cf0-117">**GetDataObjectById**</span></span>](id3dxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="55cf0-118">Извлекает объект данных с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="55cf0-118">Retrieves the data object that has the specified GUID.</span></span><br/>          |
| [<span data-ttu-id="55cf0-119">**жетдатаобжектбинаме**</span><span class="sxs-lookup"><span data-stu-id="55cf0-119">**GetDataObjectByName**</span></span>](id3dxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="55cf0-120">Извлекает объект данных с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="55cf0-120">Retrieves the data object that has the specified name.</span></span><br/>          |
| [<span data-ttu-id="55cf0-121">**Файл.**</span><span class="sxs-lookup"><span data-stu-id="55cf0-121">**GetFile**</span></span>](id3dxfileenumobject--getfile.md)                         | <span data-ttu-id="55cf0-122">Извлекает объект [**ID3DXFile**](id3dxfile.md) .</span><span class="sxs-lookup"><span data-stu-id="55cf0-122">Retrieves the [**ID3DXFile**](id3dxfile.md) object.</span></span><br/>            |



 

## <a name="remarks"></a><span data-ttu-id="55cf0-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="55cf0-123">Remarks</span></span>

<span data-ttu-id="55cf0-124">Идентификатор GUID для интерфейса ID3DXFileEnumObject — IID \_ ID3DXFileEnumObject.</span><span class="sxs-lookup"><span data-stu-id="55cf0-124">The GUID for the ID3DXFileEnumObject interface is IID\_ID3DXFileEnumObject.</span></span>

<span data-ttu-id="55cf0-125">Тип LPD3DXFILEENUMOBJECT определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="55cf0-125">The LPD3DXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface ID3DXFileEnumObject *LPD3DXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="55cf0-126">Требования</span><span class="sxs-lookup"><span data-stu-id="55cf0-126">Requirements</span></span>



| <span data-ttu-id="55cf0-127">Требование</span><span class="sxs-lookup"><span data-stu-id="55cf0-127">Requirement</span></span> | <span data-ttu-id="55cf0-128">Значение</span><span class="sxs-lookup"><span data-stu-id="55cf0-128">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="55cf0-129">Header</span><span class="sxs-lookup"><span data-stu-id="55cf0-129">Header</span></span><br/>  | <dl> <span data-ttu-id="55cf0-130"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="55cf0-130"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="55cf0-131">Библиотека</span><span class="sxs-lookup"><span data-stu-id="55cf0-131">Library</span></span><br/> | <dl> <span data-ttu-id="55cf0-132"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="55cf0-132"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="55cf0-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55cf0-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55cf0-134">Файловые интерфейсы D3DX X</span><span class="sxs-lookup"><span data-stu-id="55cf0-134">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
