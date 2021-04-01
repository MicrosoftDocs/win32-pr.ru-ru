---
description: Приложения используют методы интерфейса Идиректксфиледатареференце для поддержки объектов ссылок на данные.
ms.assetid: e0f6046f-36d9-4a13-9a0c-0738ebb2e569
title: Интерфейс Идиректксфиледатареференце (Дксфиле. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IDirectXFileDataReference
api_type:
- COM
api_location:
- d3dxof.lib
- d3dxof.dll
ms.openlocfilehash: d04d2367f914c2e8d64a3c9c64fb55df1e51e47c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157271"
---
# <a name="idirectxfiledatareference-interface"></a><span data-ttu-id="72696-103">Интерфейс Идиректксфиледатареференце</span><span class="sxs-lookup"><span data-stu-id="72696-103">IDirectXFileDataReference interface</span></span>

<span data-ttu-id="72696-104">Приложения используют методы интерфейса Идиректксфиледатареференце для поддержки объектов ссылок на данные.</span><span class="sxs-lookup"><span data-stu-id="72696-104">Applications use the methods of the IDirectXFileDataReference interface to support data reference objects.</span></span> <span data-ttu-id="72696-105">Объект ссылки на данные ссылается на объект данных, определенный ранее в файле.</span><span class="sxs-lookup"><span data-stu-id="72696-105">A data reference object refers to a data object that is defined earlier in the file.</span></span> <span data-ttu-id="72696-106">Это позволяет использовать один и тот же объект несколько раз без повторения в файле.</span><span class="sxs-lookup"><span data-stu-id="72696-106">This enables you to use the same object multiple times without repeating it in the file.</span></span> <span data-ttu-id="72696-107">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="72696-107">Deprecated.</span></span>

## <a name="members"></a><span data-ttu-id="72696-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="72696-108">Members</span></span>

<span data-ttu-id="72696-109">Интерфейс **идиректксфиледатареференце** наследует от [**идиректксфилеобжект**](idirectxfileobject.md).</span><span class="sxs-lookup"><span data-stu-id="72696-109">The **IDirectXFileDataReference** interface inherits from [**IDirectXFileObject**](idirectxfileobject.md).</span></span> <span data-ttu-id="72696-110">**Идиректксфиледатареференце** также имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="72696-110">**IDirectXFileDataReference** also has these types of members:</span></span>

-   [<span data-ttu-id="72696-111">Методы</span><span class="sxs-lookup"><span data-stu-id="72696-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="72696-112">Методы</span><span class="sxs-lookup"><span data-stu-id="72696-112">Methods</span></span>

<span data-ttu-id="72696-113">Интерфейс **идиректксфиледатареференце** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="72696-113">The **IDirectXFileDataReference** interface has these methods.</span></span>



| <span data-ttu-id="72696-114">Метод</span><span class="sxs-lookup"><span data-stu-id="72696-114">Method</span></span>                                                | <span data-ttu-id="72696-115">Описание</span><span class="sxs-lookup"><span data-stu-id="72696-115">Description</span></span>                                      |
|:------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="72696-116">**Разрешить**</span><span class="sxs-lookup"><span data-stu-id="72696-116">**Resolve**</span></span>](idirectxfiledatareference--resolve.md) | <span data-ttu-id="72696-117">Разрешает ссылки на данные.</span><span class="sxs-lookup"><span data-stu-id="72696-117">Resolves data references.</span></span> <span data-ttu-id="72696-118">Не рекомендуется.</span><span class="sxs-lookup"><span data-stu-id="72696-118">Deprecated.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="72696-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="72696-119">Remarks</span></span>

<span data-ttu-id="72696-120">После определения того, что объект является объектом ссылки на данные, используйте метод [**идиректксфиледатареференце:: Resolve**](idirectxfiledatareference--resolve.md) для получения упоминаемого ранее объекта в файле.</span><span class="sxs-lookup"><span data-stu-id="72696-120">After you have determined that an object is a data reference object, use the [**IDirectXFileDataReference::Resolve**](idirectxfiledatareference--resolve.md) method to retrieve the referenced object defined earlier in the file.</span></span> <span data-ttu-id="72696-121">Сведения о том, как определить объект ссылки на данные, см. в разделе интерфейс [**идиректксфиледата**](idirectxfiledata.md) .</span><span class="sxs-lookup"><span data-stu-id="72696-121">For information about how to identify a data reference object, see the [**IDirectXFileData**](idirectxfiledata.md) interface.</span></span>

<span data-ttu-id="72696-122">Идентификатор GUID для интерфейса Идиректксфиледатареференце — IID \_ идиректксфиледатареференце.</span><span class="sxs-lookup"><span data-stu-id="72696-122">The GUID for the IDirectXFileDataReference interface is IID\_IDirectXFileDataReference.</span></span>

<span data-ttu-id="72696-123">Тип Лпдиректксфиледатареференце определяется как указатель на этот интерфейс.</span><span class="sxs-lookup"><span data-stu-id="72696-123">The LPDIRECTXFILEDataReference type is defined as a pointer to this interface.</span></span>


```
typedef interface IDirectXFileDataReference *LPDIRECTXFILEDATAREFERENCE;
```



## <a name="requirements"></a><span data-ttu-id="72696-124">Требования</span><span class="sxs-lookup"><span data-stu-id="72696-124">Requirements</span></span>



| <span data-ttu-id="72696-125">Требование</span><span class="sxs-lookup"><span data-stu-id="72696-125">Requirement</span></span> | <span data-ttu-id="72696-126">Значение</span><span class="sxs-lookup"><span data-stu-id="72696-126">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="72696-127">Header</span><span class="sxs-lookup"><span data-stu-id="72696-127">Header</span></span><br/>  | <dl> <span data-ttu-id="72696-128"><dt>Дксфиле. h</dt></span><span class="sxs-lookup"><span data-stu-id="72696-128"><dt>DXFile.h</dt></span></span> </dl>   |
| <span data-ttu-id="72696-129">Библиотека</span><span class="sxs-lookup"><span data-stu-id="72696-129">Library</span></span><br/> | <dl> <span data-ttu-id="72696-130"><dt>D3dxof. lib</dt></span><span class="sxs-lookup"><span data-stu-id="72696-130"><dt>D3dxof.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72696-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="72696-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72696-132">**идиректксфилеобжект**</span><span class="sxs-lookup"><span data-stu-id="72696-132">**IDirectXFileObject**</span></span>](idirectxfileobject.md)
</dt> <dt>

[<span data-ttu-id="72696-133">Файловые интерфейсы X</span><span class="sxs-lookup"><span data-stu-id="72696-133">X File Interfaces</span></span>](dx9-graphics-reference-x-file-interfaces.md)
</dt> </dl>

 

 




