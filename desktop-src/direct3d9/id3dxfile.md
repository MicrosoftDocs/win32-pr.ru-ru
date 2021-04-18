---
description: Приложения используют методы интерфейса ID3DXFile для создания экземпляров интерфейсов ID3DXFileEnumObject и ID3DXFileSaveObject, а также для регистрации шаблонов.
ms.assetid: 472d45b1-5c03-4417-a005-91f802667919
title: Интерфейс ID3DXFile (D3DX9Xof. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXFile
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 45af79c4fb01c95b25803788f79588a3880fe264
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713777"
---
# <a name="id3dxfile-interface"></a><span data-ttu-id="9d0bd-103">Интерфейс ID3DXFile</span><span class="sxs-lookup"><span data-stu-id="9d0bd-103">ID3DXFile interface</span></span>

<span data-ttu-id="9d0bd-104">Приложения используют методы интерфейса ID3DXFile для создания экземпляров интерфейсов [**ID3DXFileEnumObject**](id3dxfileenumobject.md) и [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) , а также для регистрации шаблонов.</span><span class="sxs-lookup"><span data-stu-id="9d0bd-104">Applications use the methods of the ID3DXFile interface to create instances of the [**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) interfaces, and to register templates.</span></span>

## <a name="members"></a><span data-ttu-id="9d0bd-105">Элементы</span><span class="sxs-lookup"><span data-stu-id="9d0bd-105">Members</span></span>

<span data-ttu-id="9d0bd-106">Интерфейс **ID3DXFile** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9d0bd-106">The **ID3DXFile** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9d0bd-107">**ID3DXFile** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="9d0bd-107">**ID3DXFile** also has these types of members:</span></span>

-   [<span data-ttu-id="9d0bd-108">Методы</span><span class="sxs-lookup"><span data-stu-id="9d0bd-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9d0bd-109">Методы</span><span class="sxs-lookup"><span data-stu-id="9d0bd-109">Methods</span></span>

<span data-ttu-id="9d0bd-110">Интерфейс **ID3DXFile** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="9d0bd-110">The **ID3DXFile** interface has these methods.</span></span>



| <span data-ttu-id="9d0bd-111">Метод</span><span class="sxs-lookup"><span data-stu-id="9d0bd-111">Method</span></span>                                                            | <span data-ttu-id="9d0bd-112">Описание</span><span class="sxs-lookup"><span data-stu-id="9d0bd-112">Description</span></span>                                                                                                            |
|:------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9d0bd-113">**креатинумобжект**</span><span class="sxs-lookup"><span data-stu-id="9d0bd-113">**CreateEnumObject**</span></span>](id3dxfile--createenumobject.md)           | <span data-ttu-id="9d0bd-114">Создает объект перечислителя, который будет считывать x-файл.</span><span class="sxs-lookup"><span data-stu-id="9d0bd-114">Creates an enumerator object that will read a .x file.</span></span><br/>                                                      |
| [<span data-ttu-id="9d0bd-115">**креатесавеобжект**</span><span class="sxs-lookup"><span data-stu-id="9d0bd-115">**CreateSaveObject**</span></span>](id3dxfile--createsaveobject.md)           | <span data-ttu-id="9d0bd-116">Создает объект Save, который будет использоваться для сохранения данных в файл. x.</span><span class="sxs-lookup"><span data-stu-id="9d0bd-116">Creates a save object that will be used to save data to a .x file.</span></span><br/>                                          |
| [<span data-ttu-id="9d0bd-117">**регистеренумтемплатес**</span><span class="sxs-lookup"><span data-stu-id="9d0bd-117">**RegisterEnumTemplates**</span></span>](id3dxfile--registerenumtemplates.md) | <span data-ttu-id="9d0bd-118">Регистрирует пользовательские шаблоны при наличии объекта перечисления [**ID3DXFileEnumObject**](id3dxfileenumobject.md) .</span><span class="sxs-lookup"><span data-stu-id="9d0bd-118">Registers custom templates, given an [**ID3DXFileEnumObject**](id3dxfileenumobject.md) enumeration object.</span></span><br/> |
| [<span data-ttu-id="9d0bd-119">**регистертемплатес**</span><span class="sxs-lookup"><span data-stu-id="9d0bd-119">**RegisterTemplates**</span></span>](id3dxfile--registertemplates.md)         | <span data-ttu-id="9d0bd-120">Регистрирует пользовательские шаблоны.</span><span class="sxs-lookup"><span data-stu-id="9d0bd-120">Registers custom templates.</span></span><br/>                                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="9d0bd-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d0bd-121">Remarks</span></span>

<span data-ttu-id="9d0bd-122">Объект ID3DXFile также содержит локальное хранилище шаблонов.</span><span class="sxs-lookup"><span data-stu-id="9d0bd-122">An ID3DXFile object also contains a local template store.</span></span> <span data-ttu-id="9d0bd-123">Это локальное хранилище может быть добавлено только с методами [**ID3DXFile:: регистеренумтемплатес**](id3dxfile--registerenumtemplates.md) и [**ID3DXFile:: регистертемплатес**](id3dxfile--registertemplates.md) .</span><span class="sxs-lookup"><span data-stu-id="9d0bd-123">This local storage may be added to only with the [**ID3DXFile::RegisterEnumTemplates**](id3dxfile--registerenumtemplates.md) and [**ID3DXFile::RegisterTemplates**](id3dxfile--registertemplates.md) methods.</span></span>

<span data-ttu-id="9d0bd-124">Объекты [**ID3DXFileEnumObject**](id3dxfileenumobject.md) и [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) , созданные с помощью [**ID3DXFile:: Креатинумобжект**](id3dxfile--createenumobject.md) и [**ID3DXFile:: креатесавеобжект**](id3dxfile--createsaveobject.md) , также используют хранилище шаблонов родительского объекта ID3DXFile.</span><span class="sxs-lookup"><span data-stu-id="9d0bd-124">[**ID3DXFileEnumObject**](id3dxfileenumobject.md) and [**ID3DXFileSaveObject**](id3dxfilesaveobject.md) objects created with [**ID3DXFile::CreateEnumObject**](id3dxfile--createenumobject.md) and [**ID3DXFile::CreateSaveObject**](id3dxfile--createsaveobject.md) also utilize the template store of the parent ID3DXFile object.</span></span>

<span data-ttu-id="9d0bd-125">Интерфейс ID3DXFile получается путем вызова функции [**D3DXFileCreate**](d3dxfilecreate.md) .</span><span class="sxs-lookup"><span data-stu-id="9d0bd-125">The ID3DXFile interface is obtained by calling the [**D3DXFileCreate**](d3dxfilecreate.md) function.</span></span>

<span data-ttu-id="9d0bd-126">Глобальный уникальный идентификатор (GUID) для интерфейса ID3DXFile — IID \_ ID3DXFile.</span><span class="sxs-lookup"><span data-stu-id="9d0bd-126">The globally unique identifier (GUID) for the ID3DXFile interface is IID\_ID3DXFile.</span></span>

<span data-ttu-id="9d0bd-127">Тип LPD3DXFILE определяется как указатель на интерфейс ID3DXFile.</span><span class="sxs-lookup"><span data-stu-id="9d0bd-127">The LPD3DXFILE type is defined as a pointer to the ID3DXFile interface.</span></span>


```
typedef interface ID3DXFile *LPD3DXFILE;
```



## <a name="requirements"></a><span data-ttu-id="9d0bd-128">Требования</span><span class="sxs-lookup"><span data-stu-id="9d0bd-128">Requirements</span></span>



| <span data-ttu-id="9d0bd-129">Требование</span><span class="sxs-lookup"><span data-stu-id="9d0bd-129">Requirement</span></span> | <span data-ttu-id="9d0bd-130">Значение</span><span class="sxs-lookup"><span data-stu-id="9d0bd-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="9d0bd-131">Header</span><span class="sxs-lookup"><span data-stu-id="9d0bd-131">Header</span></span><br/>  | <dl> <span data-ttu-id="9d0bd-132"><dt>D3DX9Xof. h</dt></span><span class="sxs-lookup"><span data-stu-id="9d0bd-132"><dt>D3DX9Xof.h</dt></span></span> </dl> |
| <span data-ttu-id="9d0bd-133">Библиотека</span><span class="sxs-lookup"><span data-stu-id="9d0bd-133">Library</span></span><br/> | <dl> <span data-ttu-id="9d0bd-134"><dt>D3dx9. lib</dt></span><span class="sxs-lookup"><span data-stu-id="9d0bd-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="9d0bd-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d0bd-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d0bd-136">Файловые интерфейсы D3DX X</span><span class="sxs-lookup"><span data-stu-id="9d0bd-136">D3DX X File Interfaces</span></span>](dx9-graphics-reference-d3dx-x-file-interfaces.md)
</dt> </dl>

 

 
