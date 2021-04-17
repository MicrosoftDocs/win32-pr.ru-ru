---
description: Приложения используют методы интерфейса Идиректксфилинумобжект для прохода по объектам данных в файле и для получения объекта данных по его глобальному уникальному идентификатору (GUID) или по имени. Не рекомендуется.
ms.assetid: 9eefda2a-5b17-4330-8245-63a38c1b1469
title: Интерфейс Идиректксфилинумобжект (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileEnumObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: f9220f6e0a406cb4143798787276d7aa6cb5f5d1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105684993"
---
# <a name="idirectxfileenumobject-interface"></a><span data-ttu-id="1c6d4-104">Интерфейс Идиректксфилинумобжект</span><span class="sxs-lookup"><span data-stu-id="1c6d4-104">IDirectXFileEnumObject interface</span></span>

<span data-ttu-id="1c6d4-105">Приложения используют методы интерфейса Идиректксфилинумобжект для прохода по объектам данных в файле и для получения объекта данных по его глобальному уникальному идентификатору (GUID) или по имени.</span><span class="sxs-lookup"><span data-stu-id="1c6d4-105">Applications use the methods of the IDirectXFileEnumObject interface to cycle through the data objects in the file and to retrieve a data object by its globally unique identifier (GUID) or by its name.</span></span> <span data-ttu-id="1c6d4-106">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1c6d4-106">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="1c6d4-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="1c6d4-107">Members</span></span>

<span data-ttu-id="1c6d4-108">Интерфейс **идиректксфилинумобжект** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="1c6d4-108">The **IDirectXFileEnumObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="1c6d4-109">**Идиректксфилинумобжект** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="1c6d4-109">**IDirectXFileEnumObject** also has these types of members:</span></span>

-   [<span data-ttu-id="1c6d4-110">Методы</span><span class="sxs-lookup"><span data-stu-id="1c6d4-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="1c6d4-111">Методы</span><span class="sxs-lookup"><span data-stu-id="1c6d4-111">Methods</span></span>

<span data-ttu-id="1c6d4-112">Интерфейс **идиректксфилинумобжект** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="1c6d4-112">The **IDirectXFileEnumObject** interface has these methods.</span></span>



| <span data-ttu-id="1c6d4-113">Метод</span><span class="sxs-lookup"><span data-stu-id="1c6d4-113">Method</span></span>                                                                     | <span data-ttu-id="1c6d4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="1c6d4-114">Description</span></span>                                                                     |
|:---------------------------------------------------------------------------|:--------------------------------------------------------------------------------|
| [<span data-ttu-id="1c6d4-115">**жетдатаобжектбид**</span><span class="sxs-lookup"><span data-stu-id="1c6d4-115">**GetDataObjectById**</span></span>](idirectxfileenumobject--getdataobjectbyid.md)     | <span data-ttu-id="1c6d4-116">Извлекает объект данных с указанным GUID.</span><span class="sxs-lookup"><span data-stu-id="1c6d4-116">Retrieves the data object that has the specified GUID.</span></span> <span data-ttu-id="1c6d4-117">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1c6d4-117">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="1c6d4-118">**жетдатаобжектбинаме**</span><span class="sxs-lookup"><span data-stu-id="1c6d4-118">**GetDataObjectByName**</span></span>](idirectxfileenumobject--getdataobjectbyname.md) | <span data-ttu-id="1c6d4-119">Извлекает объект данных с указанным именем.</span><span class="sxs-lookup"><span data-stu-id="1c6d4-119">Retrieves the data object that has the specified name.</span></span> <span data-ttu-id="1c6d4-120">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1c6d4-120">Deprecated.</span></span><br/>   |
| [<span data-ttu-id="1c6d4-121">**жетнекстдатаобжект**</span><span class="sxs-lookup"><span data-stu-id="1c6d4-121">**GetNextDataObject**</span></span>](idirectxfileenumobject--getnextdataobject.md)     | <span data-ttu-id="1c6d4-122">Извлекает следующий объект верхнего уровня в файле DirectX.</span><span class="sxs-lookup"><span data-stu-id="1c6d4-122">Retrieves the next top-level object in the DirectX file.</span></span> <span data-ttu-id="1c6d4-123">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="1c6d4-123">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1c6d4-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1c6d4-124">Remarks</span></span>

<span data-ttu-id="1c6d4-125">Идентификатор GUID для интерфейса Идиректксфилинумобжект — IID \_ идиректксфилинумобжект.</span><span class="sxs-lookup"><span data-stu-id="1c6d4-125">The GUID for the IDirectXFileEnumObject interface is IID\_IDirectXFileEnumObject.</span></span>

<span data-ttu-id="1c6d4-126">Тип ЛПДИРЕКТКСФИЛИНУМОБЖЕКТ определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="1c6d4-126">The LPDIRECTXFILEENUMOBJECT type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileEnumObject *LPDIRECTXFILEENUMOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="1c6d4-127">Требования</span><span class="sxs-lookup"><span data-stu-id="1c6d4-127">Requirements</span></span>



| <span data-ttu-id="1c6d4-128">Требование</span><span class="sxs-lookup"><span data-stu-id="1c6d4-128">Requirement</span></span> | <span data-ttu-id="1c6d4-129">Значение</span><span class="sxs-lookup"><span data-stu-id="1c6d4-129">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c6d4-130">Header</span><span class="sxs-lookup"><span data-stu-id="1c6d4-130">Header</span></span><br/>  | <dl> <span data-ttu-id="1c6d4-131"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c6d4-131"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="1c6d4-132">Библиотека</span><span class="sxs-lookup"><span data-stu-id="1c6d4-132">Library</span></span><br/> | <dl> <span data-ttu-id="1c6d4-133"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1c6d4-133"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1c6d4-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c6d4-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c6d4-135">Файловые интерфейсы X</span><span class="sxs-lookup"><span data-stu-id="1c6d4-135">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
