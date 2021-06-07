---
description: Содержит содержимое для страницы журнала.
ms.assetid: 1df78a17-1cd4-4e98-aed1-b09d2b357703
title: Элемент Content [средство чтения журнала]
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fec59601a91d63b09c703557b7c6cd28fd11620
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432156"
---
# <a name="content-element-journal-reader"></a><span data-ttu-id="43ff8-103">\[Средство чтения журнала элементов содержимого\]</span><span class="sxs-lookup"><span data-stu-id="43ff8-103">Content Element \[Journal Reader\]</span></span>

<span data-ttu-id="43ff8-104">Содержит содержимое для страницы журнала.</span><span class="sxs-lookup"><span data-stu-id="43ff8-104">Contains the content for a Journal page.</span></span>

## <a name="definition"></a><span data-ttu-id="43ff8-105">Определение</span><span class="sxs-lookup"><span data-stu-id="43ff8-105">Definition</span></span>

``` syntax
<xs:element name="Content" type="ContentType" minOccurs="0" maxOccurs="unbounded" />
```

## <a name="parent-elements"></a><span data-ttu-id="43ff8-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="43ff8-106">Parent Elements</span></span>

[<span data-ttu-id="43ff8-107">**жаурналпаже**</span><span class="sxs-lookup"><span data-stu-id="43ff8-107">**JournalPage**</span></span>](journalpage-element.md)

## <a name="child-elements"></a><span data-ttu-id="43ff8-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="43ff8-108">Child Elements</span></span>

[<span data-ttu-id="43ff8-109">**граупноде**</span><span class="sxs-lookup"><span data-stu-id="43ff8-109">**GroupNode**</span></span>](groupnode-element.md)

[<span data-ttu-id="43ff8-110">**Paragraph**</span><span class="sxs-lookup"><span data-stu-id="43ff8-110">**Paragraph**</span></span>](paragraph-element.md)

[<span data-ttu-id="43ff8-111">**Рисование**</span><span class="sxs-lookup"><span data-stu-id="43ff8-111">**Drawing**</span></span>](drawing-element.md)

[<span data-ttu-id="43ff8-112">**Полнотекстовым**</span><span class="sxs-lookup"><span data-stu-id="43ff8-112">**Text**</span></span>](text-element.md)

[<span data-ttu-id="43ff8-113">**Изображение**</span><span class="sxs-lookup"><span data-stu-id="43ff8-113">**Image**</span></span>](image-element.md)

[<span data-ttu-id="43ff8-114">**Flag**</span><span class="sxs-lookup"><span data-stu-id="43ff8-114">**Flag**</span></span>](flag-element.md)

## <a name="attributes"></a><span data-ttu-id="43ff8-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="43ff8-115">Attributes</span></span>



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
<th><span data-ttu-id="43ff8-116">attribute</span><span class="sxs-lookup"><span data-stu-id="43ff8-116">Attribute</span></span></th>
<th><span data-ttu-id="43ff8-117">Тип</span><span class="sxs-lookup"><span data-stu-id="43ff8-117">Type</span></span></th>
<th><span data-ttu-id="43ff8-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="43ff8-118">Required</span></span></th>
<th><span data-ttu-id="43ff8-119">Описание</span><span class="sxs-lookup"><span data-stu-id="43ff8-119">Description</span></span></th>
<th><span data-ttu-id="43ff8-120">поссиблевалуес</span><span class="sxs-lookup"><span data-stu-id="43ff8-120">PossibleValues</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="43ff8-121"><strong>Тип</strong></span><span class="sxs-lookup"><span data-stu-id="43ff8-121"><strong>Type</strong></span></span></td>
<td><span data-ttu-id="43ff8-122"><a href="contenttype-complex-type.md"><strong>ContentType, complexType</strong></a></span><span class="sxs-lookup"><span data-stu-id="43ff8-122"><a href="contenttype-complex-type.md"><strong>ContentType complexType</strong></a></span></span></td>
<td><span data-ttu-id="43ff8-123">Обязательно</span><span class="sxs-lookup"><span data-stu-id="43ff8-123">Required</span></span></td>
<td><span data-ttu-id="43ff8-124">Если тип — &quot; инерт &quot; , содержимое изменить нельзя.</span><span class="sxs-lookup"><span data-stu-id="43ff8-124">If the type is &quot;Inert&quot;, then the content cannot be modified.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="43ff8-125">Нормальный</span><span class="sxs-lookup"><span data-stu-id="43ff8-125">Normal</span></span></li>
<li><span data-ttu-id="43ff8-126">инерт</span><span class="sxs-lookup"><span data-stu-id="43ff8-126">Inert</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="43ff8-127">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="43ff8-127">Element Information</span></span>



|  <span data-ttu-id="43ff8-128">Элемент</span><span class="sxs-lookup"><span data-stu-id="43ff8-128">Element</span></span>     | <span data-ttu-id="43ff8-129">Значение</span><span class="sxs-lookup"><span data-stu-id="43ff8-129">Value</span></span>                                                     |
|--------------|-------------------------------------------------------------|
| <span data-ttu-id="43ff8-130">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="43ff8-130">Element type</span></span> | <span data-ttu-id="43ff8-131">[**ContentType**](contenttype-complex-type.md) , complexType</span><span class="sxs-lookup"><span data-stu-id="43ff8-131">[**ContentType**](contenttype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="43ff8-132">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="43ff8-132">Namespace</span></span>    | <span data-ttu-id="43ff8-133">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="43ff8-133">urn:schemas-microsoft-com:tabletpc:richink</span></span>                  |
| <span data-ttu-id="43ff8-134">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="43ff8-134">Schema name</span></span>  | <span data-ttu-id="43ff8-135">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="43ff8-135">Journal Reader</span></span>                                              |



 

 

 




