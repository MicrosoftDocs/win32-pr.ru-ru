---
title: COLUMN. columnID
description: Атрибут columnID указывает или получает идентификатор столбца в элементе управления списка воспроизведения.
ms.assetid: c7b51f0b-e347-46be-a26d-aaa0bce83e0c
keywords:
- COLUMN. columnID проигрыватель Windows Media
topic_type:
- apiref
api_name:
- COLUMN.columnID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4bc9aa6485443ae17486616b030b903a911a8e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698807"
---
# <a name="columncolumnid"></a><span data-ttu-id="1ed88-104">COLUMN. columnID</span><span class="sxs-lookup"><span data-stu-id="1ed88-104">COLUMN.columnID</span></span>

<span data-ttu-id="1ed88-105">Атрибут **columnid** указывает или получает идентификатор столбца в элементе управления **списка воспроизведения** .</span><span class="sxs-lookup"><span data-stu-id="1ed88-105">The **columnID** attribute specifies or retrieves a column ID in the **PLAYLIST** control.</span></span>

``` syntax
        elementID.columnID
```

## <a name="possible-values"></a><span data-ttu-id="1ed88-106">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="1ed88-106">Possible Values</span></span>

<span data-ttu-id="1ed88-107">Этот атрибут является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="1ed88-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="1ed88-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1ed88-108">Remarks</span></span>

<span data-ttu-id="1ed88-109">Значения **columnid** являются теми же значениями, которые используются с методом **GetItemInfo** для объекта **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="1ed88-109">The **columnID** values are the same values used with the **getItemInfo** method on a **Media** object.</span></span> <span data-ttu-id="1ed88-110">Список можно получить с помощью *носителя*. Свойство **аттрибутекаунт** для определения количества атрибутов, доступных для данного объекта **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="1ed88-110">A list can be obtained by using the *Media*.**attributeCount** property to determine the number of attributes available for a given **Media** object.</span></span> <span data-ttu-id="1ed88-111">Номера индексов можно использовать с *носителем*. метод **жетаттрибутенаме** для определения имен атрибутов, которые, в свою очередь, могут передаваться на *носитель*. **getItemInfo**.</span><span class="sxs-lookup"><span data-stu-id="1ed88-111">Index numbers can then be used with the *Media*.**getAttributeName** method to determine the names of the attributes, which can in turn be passed to *Media*.**getItemInfo**.</span></span> <span data-ttu-id="1ed88-112">Свойству **columnid** можно присвоить только эти значения, за исключением некоторых значений, которые не могут быть возвращены *носителем*. **жетаттрибутенаме**.</span><span class="sxs-lookup"><span data-stu-id="1ed88-112">The **columnID** property can only be set to these values, with the exception of some values that may not be returned by *Media*.**getAttributeName**.</span></span> <span data-ttu-id="1ed88-113">Эти значения перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="1ed88-113">These values are listed below.</span></span>



| <span data-ttu-id="1ed88-114">Значение</span><span class="sxs-lookup"><span data-stu-id="1ed88-114">Value</span></span>     | <span data-ttu-id="1ed88-115">Описание</span><span class="sxs-lookup"><span data-stu-id="1ed88-115">Description</span></span>                                                                        |
|-----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="1ed88-116">name</span><span class="sxs-lookup"><span data-stu-id="1ed88-116">name</span></span>      | <span data-ttu-id="1ed88-117">Отображает имя объекта **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="1ed88-117">Displays the name of the **Media** object.</span></span>                                         |
| <span data-ttu-id="1ed88-118">длительность</span><span class="sxs-lookup"><span data-stu-id="1ed88-118">duration</span></span>  | <span data-ttu-id="1ed88-119">Отображает длительность объекта **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="1ed88-119">Displays the duration of the **Media** object.</span></span>                                     |
| <span data-ttu-id="1ed88-120">саурцеурл</span><span class="sxs-lookup"><span data-stu-id="1ed88-120">sourceURL</span></span> | <span data-ttu-id="1ed88-121">Отображает URL-адрес объекта **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="1ed88-121">Displays the URL of the **Media** object.</span></span>                                          |
| <span data-ttu-id="1ed88-122">status</span><span class="sxs-lookup"><span data-stu-id="1ed88-122">status</span></span>    | <span data-ttu-id="1ed88-123">Отображает состояние копирования файлов.</span><span class="sxs-lookup"><span data-stu-id="1ed88-123">Displays the status of copying files.</span></span>                                              |
| <span data-ttu-id="1ed88-124">size</span><span class="sxs-lookup"><span data-stu-id="1ed88-124">size</span></span>      | <span data-ttu-id="1ed88-125">Отображает размер файла, который представляет объект **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="1ed88-125">Displays the size of the file that the **Media** object represents.</span></span>                |
| <span data-ttu-id="1ed88-126">Расширение</span><span class="sxs-lookup"><span data-stu-id="1ed88-126">extension</span></span> | <span data-ttu-id="1ed88-127">Отображает расширение имени файла, представляемого объектом **мультимедиа** .</span><span class="sxs-lookup"><span data-stu-id="1ed88-127">Displays the file name extension of the file that the **Media** object represents.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="1ed88-128">Требования</span><span class="sxs-lookup"><span data-stu-id="1ed88-128">Requirements</span></span>



| <span data-ttu-id="1ed88-129">Требование</span><span class="sxs-lookup"><span data-stu-id="1ed88-129">Requirement</span></span> | <span data-ttu-id="1ed88-130">Значение</span><span class="sxs-lookup"><span data-stu-id="1ed88-130">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="1ed88-131">Версия</span><span class="sxs-lookup"><span data-stu-id="1ed88-131">Version</span></span><br/> | <span data-ttu-id="1ed88-132">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1ed88-132">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ed88-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1ed88-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed88-134">**COLUMN, элемент**</span><span class="sxs-lookup"><span data-stu-id="1ed88-134">**COLUMN Element**</span></span>](column-element.md)
</dt> <dt>

[<span data-ttu-id="1ed88-135">**Объект мультимедиа**</span><span class="sxs-lookup"><span data-stu-id="1ed88-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="1ed88-136">**Media. Аттрибутекаунт**</span><span class="sxs-lookup"><span data-stu-id="1ed88-136">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="1ed88-137">**Media. Жетаттрибутенаме**</span><span class="sxs-lookup"><span data-stu-id="1ed88-137">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="1ed88-138">**Media. getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="1ed88-138">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> </dl>

 

 





