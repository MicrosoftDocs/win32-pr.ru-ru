---
description: Приложения используют методы интерфейса Идиректксфиледата для создания или доступа к немедленной иерархии объекта данных.
ms.assetid: 8810162f-76a8-45ba-b069-7910fd611a60
title: Интерфейс Идиректксфиледата (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileData
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: 30d2fb26e3752e302726edce51354369f3b067eb
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713866"
---
# <a name="idirectxfiledata-interface"></a><span data-ttu-id="402ba-103">Интерфейс Идиректксфиледата</span><span class="sxs-lookup"><span data-stu-id="402ba-103">IDirectXFileData interface</span></span>

<span data-ttu-id="402ba-104">Приложения используют методы интерфейса Идиректксфиледата для создания или доступа к немедленной иерархии объекта данных.</span><span class="sxs-lookup"><span data-stu-id="402ba-104">Applications use the methods of the IDirectXFileData interface to build or to access the immediate hierarchy of the data object.</span></span> <span data-ttu-id="402ba-105">Иерархия определяется ограничениями шаблонов.</span><span class="sxs-lookup"><span data-stu-id="402ba-105">Template restrictions determine the hierarchy.</span></span> <span data-ttu-id="402ba-106">Типы данных, разрешенные шаблоном, называются необязательными членами.</span><span class="sxs-lookup"><span data-stu-id="402ba-106">Data types allowed by the template are called optional members.</span></span> <span data-ttu-id="402ba-107">Необязательные элементы не являются обязательными, но объект может пропустить важную информацию без них.</span><span class="sxs-lookup"><span data-stu-id="402ba-107">The optional members are not required, but an object might miss important information without them.</span></span> <span data-ttu-id="402ba-108">Эти необязательные члены сохраняются как дочерние элементы объекта данных.</span><span class="sxs-lookup"><span data-stu-id="402ba-108">These optional members are saved as children of the data object.</span></span> <span data-ttu-id="402ba-109">Дочерние элементы могут быть другими объектами данных, ссылками на более ранний объект данных или двоичным объектом.</span><span class="sxs-lookup"><span data-stu-id="402ba-109">The children can be another data object, a reference to an earlier data object, or a binary object.</span></span> <span data-ttu-id="402ba-110">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="402ba-110">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="402ba-111">Элементы</span><span class="sxs-lookup"><span data-stu-id="402ba-111">Members</span></span>

<span data-ttu-id="402ba-112">Интерфейс **идиректксфиледата** наследует от [**идиректксфилеобжект**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="402ba-112">The **IDirectXFileData** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="402ba-113">**Идиректксфиледата** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="402ba-113">**IDirectXFileData** also has these types of members:</span></span>

-   [<span data-ttu-id="402ba-114">Методы</span><span class="sxs-lookup"><span data-stu-id="402ba-114">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="402ba-115">Методы</span><span class="sxs-lookup"><span data-stu-id="402ba-115">Methods</span></span>

<span data-ttu-id="402ba-116">Интерфейс **идиректксфиледата** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="402ba-116">The **IDirectXFileData** interface has these methods.</span></span>



| <span data-ttu-id="402ba-117">Метод</span><span class="sxs-lookup"><span data-stu-id="402ba-117">Method</span></span>                                                         | <span data-ttu-id="402ba-118">Описание</span><span class="sxs-lookup"><span data-stu-id="402ba-118">Description</span></span>                                                                                                               |
|:---------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="402ba-119">**аддбинарйобжект**</span><span class="sxs-lookup"><span data-stu-id="402ba-119">**AddBinaryObject**</span></span>](idirectxfiledata--addbinaryobject.md)   | <span data-ttu-id="402ba-120">Создает двоичный объект и добавляет его в качестве дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="402ba-120">Creates a binary object and adds it as a child object.</span></span> <span data-ttu-id="402ba-121">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="402ba-121">Deprecated.</span></span><br/>                                             |
| [<span data-ttu-id="402ba-122">**адддатаобжект**</span><span class="sxs-lookup"><span data-stu-id="402ba-122">**AddDataObject**</span></span>](idirectxfiledata--adddataobject.md)       | <span data-ttu-id="402ba-123">Добавляет объект данных в качестве дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="402ba-123">Adds a data object as a child object.</span></span> <span data-ttu-id="402ba-124">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="402ba-124">Deprecated.</span></span><br/>                                                              |
| [<span data-ttu-id="402ba-125">**адддатареференце**</span><span class="sxs-lookup"><span data-stu-id="402ba-125">**AddDataReference**</span></span>](idirectxfiledata--adddatareference.md) | <span data-ttu-id="402ba-126">Создает и добавляет объект ссылки на данные в качестве дочернего объекта.</span><span class="sxs-lookup"><span data-stu-id="402ba-126">Creates and adds a data reference object as a child object.</span></span> <span data-ttu-id="402ba-127">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="402ba-127">Deprecated.</span></span><br/>                                        |
| [<span data-ttu-id="402ba-128">**GetData**</span><span class="sxs-lookup"><span data-stu-id="402ba-128">**GetData**</span></span>](idirectxfiledata--getdata.md)                   | <span data-ttu-id="402ba-129">Извлекает данные для одного из элементов объекта или данные для всех элементов.</span><span class="sxs-lookup"><span data-stu-id="402ba-129">Retrieves the data for one of the object's members or the data for all members.</span></span> <span data-ttu-id="402ba-130">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="402ba-130">Deprecated.</span></span><br/>                    |
| [<span data-ttu-id="402ba-131">**жетнекстобжект**</span><span class="sxs-lookup"><span data-stu-id="402ba-131">**GetNextObject**</span></span>](idirectxfiledata--getnextobject.md)       | <span data-ttu-id="402ba-132">Извлекает следующий дочерний объект данных, объект ссылки на данные или двоичный объект в файле DirectX.</span><span class="sxs-lookup"><span data-stu-id="402ba-132">Retrieves the next child data object, data reference object, or binary object in the DirectX file.</span></span> <span data-ttu-id="402ba-133">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="402ba-133">Deprecated.</span></span><br/> |
| [<span data-ttu-id="402ba-134">**GetType**</span><span class="sxs-lookup"><span data-stu-id="402ba-134">**GetType**</span></span>](idirectxfiledata--gettype.md)                   | <span data-ttu-id="402ba-135">Извлекает идентификатор GUID шаблона объекта.</span><span class="sxs-lookup"><span data-stu-id="402ba-135">Retrieves the GUID of the object's template.</span></span> <span data-ttu-id="402ba-136">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="402ba-136">Deprecated.</span></span><br/>                                                       |



 

## <a name="remarks"></a><span data-ttu-id="402ba-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="402ba-137">Remarks</span></span>

<span data-ttu-id="402ba-138">Идентификатор GUID для интерфейса Идиректксфиледата — IID \_ идиректксфиледата.</span><span class="sxs-lookup"><span data-stu-id="402ba-138">The GUID for the IDirectXFileData interface is IID\_IDirectXFileData.</span></span>

<span data-ttu-id="402ba-139">Тип ЛПДИРЕКТКСФИЛЕДАТА определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="402ba-139">The LPDIRECTXFILEDATA type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileData *LPDIRECTXFILEDATA;
```



## <a name="requirements"></a><span data-ttu-id="402ba-140">Требования</span><span class="sxs-lookup"><span data-stu-id="402ba-140">Requirements</span></span>



| <span data-ttu-id="402ba-141">Требование</span><span class="sxs-lookup"><span data-stu-id="402ba-141">Requirement</span></span> | <span data-ttu-id="402ba-142">Значение</span><span class="sxs-lookup"><span data-stu-id="402ba-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="402ba-143">Header</span><span class="sxs-lookup"><span data-stu-id="402ba-143">Header</span></span><br/>  | <dl> <span data-ttu-id="402ba-144"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="402ba-144"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="402ba-145">Библиотека</span><span class="sxs-lookup"><span data-stu-id="402ba-145">Library</span></span><br/> | <dl> <span data-ttu-id="402ba-146"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="402ba-146"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="402ba-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="402ba-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="402ba-148">**идиректксфилеобжект**</span><span class="sxs-lookup"><span data-stu-id="402ba-148">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="402ba-149">Файловые интерфейсы X</span><span class="sxs-lookup"><span data-stu-id="402ba-149">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




