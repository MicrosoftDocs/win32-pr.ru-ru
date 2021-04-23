---
description: Приложения используют методы интерфейса Идиректксфилесавеобжект для создания объектов данных, а также для сохранения шаблонов и объектов данных.
ms.assetid: 7948a7d2-b150-45cf-a1fc-5dca21d74770
title: Интерфейс Идиректксфилесавеобжект (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileSaveObject
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 4be69b10037381d4b06466d52483427b6d40499a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713625"
---
# <a name="idirectxfilesaveobject-interface"></a><span data-ttu-id="61017-103">Интерфейс Идиректксфилесавеобжект</span><span class="sxs-lookup"><span data-stu-id="61017-103">IDirectXFileSaveObject interface</span></span>

<span data-ttu-id="61017-104">Приложения используют методы интерфейса Идиректксфилесавеобжект для создания объектов данных, а также для сохранения шаблонов и объектов данных.</span><span class="sxs-lookup"><span data-stu-id="61017-104">Applications use the methods of the IDirectXFileSaveObject interface to create data objects and to save templates and data objects.</span></span> <span data-ttu-id="61017-105">Обратите внимание, что шаблоны не являются обязательными для каждого файла.</span><span class="sxs-lookup"><span data-stu-id="61017-105">Note that templates are not required in every file.</span></span> <span data-ttu-id="61017-106">Например, можно разместить все шаблоны в одном файле Microsoft DirectX, а не дублировать их в каждый файл DirectX.</span><span class="sxs-lookup"><span data-stu-id="61017-106">For example, you could put all templates into a single Microsoft DirectX file rather than duplicating them in every DirectX file.</span></span> <span data-ttu-id="61017-107">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="61017-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="61017-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="61017-108">Members</span></span>

<span data-ttu-id="61017-109">Интерфейс **идиректксфилесавеобжект** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="61017-109">The **IDirectXFileSaveObject** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="61017-110">**Идиректксфилесавеобжект** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="61017-110">**IDirectXFileSaveObject** also has these types of members:</span></span>

-   [<span data-ttu-id="61017-111">Методы</span><span class="sxs-lookup"><span data-stu-id="61017-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="61017-112">Методы</span><span class="sxs-lookup"><span data-stu-id="61017-112">Methods</span></span>

<span data-ttu-id="61017-113">Интерфейс **идиректксфилесавеобжект** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="61017-113">The **IDirectXFileSaveObject** interface has these methods.</span></span>



| <span data-ttu-id="61017-114">Метод</span><span class="sxs-lookup"><span data-stu-id="61017-114">Method</span></span>                                                               | <span data-ttu-id="61017-115">Описание</span><span class="sxs-lookup"><span data-stu-id="61017-115">Description</span></span>                                                                    |
|:---------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [<span data-ttu-id="61017-116">**креатедатаобжект**</span><span class="sxs-lookup"><span data-stu-id="61017-116">**CreateDataObject**</span></span>](idirectxfilesaveobject--createdataobject.md) | <span data-ttu-id="61017-117">Создает объект данных.</span><span class="sxs-lookup"><span data-stu-id="61017-117">Creates a data object.</span></span> <span data-ttu-id="61017-118">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="61017-118">Deprecated.</span></span><br/>                                  |
| [<span data-ttu-id="61017-119">**SaveData**</span><span class="sxs-lookup"><span data-stu-id="61017-119">**SaveData**</span></span>](idirectxfilesaveobject--savedata.md)                 | <span data-ttu-id="61017-120">Сохраняет объект данных и его дочерние элементы в файле DirectX.</span><span class="sxs-lookup"><span data-stu-id="61017-120">Saves a data object and its children to a DirectX file.</span></span> <span data-ttu-id="61017-121">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="61017-121">Deprecated.</span></span><br/> |
| [<span data-ttu-id="61017-122">**саветемплатес**</span><span class="sxs-lookup"><span data-stu-id="61017-122">**SaveTemplates**</span></span>](idirectxfilesaveobject--savetemplates.md)       | <span data-ttu-id="61017-123">Сохраняет шаблоны в файл DirectX.</span><span class="sxs-lookup"><span data-stu-id="61017-123">Saves templates to a DirectX file.</span></span> <span data-ttu-id="61017-124">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="61017-124">Deprecated.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="61017-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="61017-125">Remarks</span></span>

<span data-ttu-id="61017-126">Глобальный уникальный идентификатор (GUID) для интерфейса Идиректксфилесавеобжект — **IID \_ идиректксфилесавеобжект**.</span><span class="sxs-lookup"><span data-stu-id="61017-126">The globally unique identifier (GUID) for the IDirectXFileSaveObject interface is **IID\_IDirectXFileSaveObject**.</span></span>

<span data-ttu-id="61017-127">Интерфейс **идиректксфилесавеобжект** получается путем вызова метода [**Идиректксфиле:: креатесавеобжект**](idirectxfile--createsaveobject.md) .</span><span class="sxs-lookup"><span data-stu-id="61017-127">The **IDirectXFileSaveObject** interface is obtained by calling the [**IDirectXFile::CreateSaveObject**](idirectxfile--createsaveobject.md) method.</span></span>

<span data-ttu-id="61017-128">Тип **лпдиректксфилесавеобжект** определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="61017-128">The **LPDIRECTXFILESAVEOBJECT** type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileSaveObject *LPDIRECTXFILESAVEOBJECT;
```



## <a name="requirements"></a><span data-ttu-id="61017-129">Требования</span><span class="sxs-lookup"><span data-stu-id="61017-129">Requirements</span></span>



| <span data-ttu-id="61017-130">Требование</span><span class="sxs-lookup"><span data-stu-id="61017-130">Requirement</span></span> | <span data-ttu-id="61017-131">Значение</span><span class="sxs-lookup"><span data-stu-id="61017-131">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61017-132">Header</span><span class="sxs-lookup"><span data-stu-id="61017-132">Header</span></span><br/>  | <dl> <span data-ttu-id="61017-133"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="61017-133"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="61017-134">Библиотека</span><span class="sxs-lookup"><span data-stu-id="61017-134">Library</span></span><br/> | <dl> <span data-ttu-id="61017-135"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="61017-135"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61017-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="61017-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61017-137">Файловые интерфейсы X</span><span class="sxs-lookup"><span data-stu-id="61017-137">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 
