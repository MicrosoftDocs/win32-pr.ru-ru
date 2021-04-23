---
description: Содержит содержимое для страницы журнала.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Элемент Content [средство чтения журнала]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5b5a7c9631cd69d38b8db54e2a2f8e69636f7e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693286"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="ef44d-103">\[Средство чтения журнала элементов содержимого\]</span><span class="sxs-lookup"><span data-stu-id="ef44d-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="ef44d-104">Содержит содержимое для страницы журнала.</span><span class="sxs-lookup"><span data-stu-id="ef44d-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="ef44d-105">Определение</span><span class="sxs-lookup"><span data-stu-id="ef44d-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="ef44d-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="ef44d-106">Parent Elements</span></span>

[<span data-ttu-id="ef44d-107">**жаурналпаже**</span><span class="sxs-lookup"><span data-stu-id="ef44d-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="ef44d-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="ef44d-108">Child Elements</span></span>

[<span data-ttu-id="ef44d-109">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="ef44d-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="ef44d-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="ef44d-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="ef44d-111">**Рисование**</span><span class="sxs-lookup"><span data-stu-id="ef44d-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="ef44d-112">**Полнотекстовым**</span><span class="sxs-lookup"><span data-stu-id="ef44d-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="ef44d-113">**Образ**</span><span class="sxs-lookup"><span data-stu-id="ef44d-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="ef44d-114">**Flag**</span><span class="sxs-lookup"><span data-stu-id="ef44d-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="ef44d-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="ef44d-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ef44d-116">attribute</span><span class="sxs-lookup"><span data-stu-id="ef44d-116">Attribute</span></span></th>
<th><span data-ttu-id="ef44d-117">Тип</span><span class="sxs-lookup"><span data-stu-id="ef44d-117">Type</span></span></th>
<th><span data-ttu-id="ef44d-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ef44d-118">Required</span></span></th>
<th><span data-ttu-id="ef44d-119">Описание</span><span class="sxs-lookup"><span data-stu-id="ef44d-119">Description</span></span></th>
<th><span data-ttu-id="ef44d-120">поссиблевалуес</span><span class="sxs-lookup"><span data-stu-id="ef44d-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ef44d-121"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="ef44d-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="ef44d-122"><a href="contenttype-complex-type.md"><strong>ContentType, complexType</strong></a></span><span class="sxs-lookup"><span data-stu-id="ef44d-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="ef44d-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="ef44d-123">Required</span></span></td>
<td><span data-ttu-id="ef44d-124">Если тип — &quot; инерт &quot; , содержимое изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="ef44d-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="ef44d-125">Норм.</span><span class="sxs-lookup"><span data-stu-id="ef44d-125">Normal</span></span></li>
<li><span data-ttu-id="ef44d-126">инерт</span><span class="sxs-lookup"><span data-stu-id="ef44d-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="ef44d-127">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="ef44d-127">Element Information</span></span>



|              |                                                             |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="ef44d-128">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="ef44d-128">Element type</span></span> | <span data-ttu-id="ef44d-129">[**ContentType**](contenttype-complex-type.md) , complexType</span><span class="sxs-lookup"><span data-stu-id="ef44d-129">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="ef44d-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="ef44d-130">Namespace</span></span>    | <span data-ttu-id="ef44d-131">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="ef44d-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="ef44d-132">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="ef44d-132">Schema name</span></span>  | <span data-ttu-id="ef44d-133">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="ef44d-133">Journal Reader</span></span>                                              |



 

 

 




