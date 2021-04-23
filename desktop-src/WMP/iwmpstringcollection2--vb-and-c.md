---
title: Интерфейс IWMPStringCollection2 (VB и C) (WMP. h)
description: Предоставляет методы, дополняют интерфейс Ивмпстрингколлектион.
ms.assetid: be93ff47-7f76-4b5e-ad30-3094a75147c8
keywords:
- IWMPStringCollection2 (VB и C) интерфейс проигрывателя Windows Media
- IWMPStringCollection2 (VB и C) интерфейс проигрывателя Windows Media, описание
topic_type:
- apiref
api_name:
- IWMPStringCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184e1a16ea0e6b33cc5b67eaeac6b050e5cda97a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105695132"
---
# <a name="iwmpstringcollection2-vb-and-c-interface"></a><span data-ttu-id="cbe94-105">Интерфейс IWMPStringCollection2 (VB и C#)</span><span class="sxs-lookup"><span data-stu-id="cbe94-105">IWMPStringCollection2 (VB and C#) interface</span></span>

<span data-ttu-id="cbe94-106">Предоставляет методы, дополняют интерфейс **ивмпстрингколлектион** .</span><span class="sxs-lookup"><span data-stu-id="cbe94-106">Provides methods that supplement the **IWMPStringCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="cbe94-107">Элементы</span><span class="sxs-lookup"><span data-stu-id="cbe94-107">Members</span></span>

<span data-ttu-id="cbe94-108">Интерфейс **IWMPStringCollection2 (VB и C#)** имеет следующие типы членов:</span><span class="sxs-lookup"><span data-stu-id="cbe94-108">The **IWMPStringCollection2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="cbe94-109">Методы</span><span class="sxs-lookup"><span data-stu-id="cbe94-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="cbe94-110">Методы</span><span class="sxs-lookup"><span data-stu-id="cbe94-110">Methods</span></span>

<span data-ttu-id="cbe94-111">Интерфейс **IWMPStringCollection2 (VB и C#)** содержит следующие методы.</span><span class="sxs-lookup"><span data-stu-id="cbe94-111">The **IWMPStringCollection2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="cbe94-112">Метод</span><span class="sxs-lookup"><span data-stu-id="cbe94-112">Method</span></span>                                                                                                                 | <span data-ttu-id="cbe94-113">Описание</span><span class="sxs-lookup"><span data-stu-id="cbe94-113">Description</span></span>                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cbe94-114">**жетаттрибутекаунтбитипе**</span><span class="sxs-lookup"><span data-stu-id="cbe94-114">**getAttributeCountByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getattributecountbytype--vb-and-c.md) | <span data-ttu-id="cbe94-115">Возвращает число атрибутов, связанных с указанным индексом элемента коллекции строк, именем атрибута и языком.</span><span class="sxs-lookup"><span data-stu-id="cbe94-115">Returns the number of attributes associated with the specified string collection item index, attribute name, and language.</span></span><br/> |
| [<span data-ttu-id="cbe94-116">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="cbe94-116">**getItemInfo**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)                         | <span data-ttu-id="cbe94-117">Возвращает строку, соответствующую указанному индексу элемента коллекции строк и имени.</span><span class="sxs-lookup"><span data-stu-id="cbe94-117">Returns the string corresponding to the specified string collection item index and name.</span></span><br/>                                   |
| [<span data-ttu-id="cbe94-118">**жетитеминфобитипе**</span><span class="sxs-lookup"><span data-stu-id="cbe94-118">**getItemInfoByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)             | <span data-ttu-id="cbe94-119">Возвращает значение, соответствующее указанному индексу элемента коллекции строк, имени, языку и индексу атрибута.</span><span class="sxs-lookup"><span data-stu-id="cbe94-119">Returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span><br/>        |
| [<span data-ttu-id="cbe94-120">**Идентично**</span><span class="sxs-lookup"><span data-stu-id="cbe94-120">**isIdentical**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-isidentical--vb-and-c.md)                         | <span data-ttu-id="cbe94-121">Возвращает значение, указывающее, совпадает ли указанный объект с текущим объектом.</span><span class="sxs-lookup"><span data-stu-id="cbe94-121">Returns a value indicating whether the supplied object is the same as the current one.</span></span><br/>                                     |



 

<span data-ttu-id="cbe94-122">Получите интерфейс **IWMPStringCollection2** путем приведения значения, возвращаемого методом [**ивмпмедиаколлектион. жетаттрибутестрингколлектион**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection) .</span><span class="sxs-lookup"><span data-stu-id="cbe94-122">Get an **IWMPStringCollection2** interface by casting the value returned by the [**IWMPMediaCollection.getAttributeStringCollection**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="cbe94-123">Требования</span><span class="sxs-lookup"><span data-stu-id="cbe94-123">Requirements</span></span>



| <span data-ttu-id="cbe94-124">Требование</span><span class="sxs-lookup"><span data-stu-id="cbe94-124">Requirement</span></span> | <span data-ttu-id="cbe94-125">Значение</span><span class="sxs-lookup"><span data-stu-id="cbe94-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="cbe94-126">Header</span><span class="sxs-lookup"><span data-stu-id="cbe94-126">Header</span></span><br/> | <dl> <span data-ttu-id="cbe94-127"><dt>WMP. h</dt></span><span class="sxs-lookup"><span data-stu-id="cbe94-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbe94-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cbe94-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbe94-129">**Интерфейсы для Visual Basic .NET и C #**</span><span class="sxs-lookup"><span data-stu-id="cbe94-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="cbe94-130">**Интерфейс Ивмпстрингколлектион (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="cbe94-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





