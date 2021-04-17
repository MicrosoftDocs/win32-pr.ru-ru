---
description: Содержит фон элемента Жаурналдокумент или элемента Жаурналпаже.
ms.assetid: 48527c4e-50fb-4800-ac87-1646234783ba
title: Элемент Background
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e58a836c7cfd13130779c1cd6b017105bcaa6321
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712497"
---
# <a name="background-element"></a><span data-ttu-id="70fb2-103">Элемент Background</span><span class="sxs-lookup"><span data-stu-id="70fb2-103">Background Element</span></span>

<span data-ttu-id="70fb2-104">Содержит фон элемента [**жаурналдокумент**](journaldocument-element.md) или элемента [**жаурналпаже**](journalpage-element.md) .</span><span class="sxs-lookup"><span data-stu-id="70fb2-104">Contains the background for a [**JournalDocument**](journaldocument-element.md) element or [**JournalPage**](journalpage-element.md) element.</span></span>

## <a name="definition"></a><span data-ttu-id="70fb2-105">Определение</span><span class="sxs-lookup"><span data-stu-id="70fb2-105">Definition</span></span>

``` syntax
<xs:element name="Background" type="BackgroundType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="70fb2-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="70fb2-106">Parent Elements</span></span>

[<span data-ttu-id="70fb2-107">**Stationery**</span><span class="sxs-lookup"><span data-stu-id="70fb2-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="70fb2-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="70fb2-108">Child Elements</span></span>

[<span data-ttu-id="70fb2-109">**Образ**</span><span class="sxs-lookup"><span data-stu-id="70fb2-109">**Image**</span></span>](image-element.md)

## <a name="attributes"></a><span data-ttu-id="70fb2-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="70fb2-110">Attributes</span></span>



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
<th><span data-ttu-id="70fb2-111">attribute</span><span class="sxs-lookup"><span data-stu-id="70fb2-111">Attribute</span></span></th>
<th><span data-ttu-id="70fb2-112">Тип</span><span class="sxs-lookup"><span data-stu-id="70fb2-112">Type</span></span></th>
<th><span data-ttu-id="70fb2-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="70fb2-113">Required</span></span></th>
<th><span data-ttu-id="70fb2-114">Описание</span><span class="sxs-lookup"><span data-stu-id="70fb2-114">Description</span></span></th>
<th><span data-ttu-id="70fb2-115">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="70fb2-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="70fb2-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="70fb2-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="70fb2-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="70fb2-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="70fb2-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="70fb2-118">Required</span></span></td>
<td><span data-ttu-id="70fb2-119">Задает стиль фона.</span><span class="sxs-lookup"><span data-stu-id="70fb2-119">Specifies the style of the background.</span></span></td>
<td><ul>
<li><span data-ttu-id="70fb2-120">Нет</span><span class="sxs-lookup"><span data-stu-id="70fb2-120">None</span></span></li>
<li><span data-ttu-id="70fb2-121">Сплошная</span><span class="sxs-lookup"><span data-stu-id="70fb2-121">Solid</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="70fb2-122"><strong>Цвет</strong></span><span class="sxs-lookup"><span data-stu-id="70fb2-122"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="70fb2-123"><a href="colortype-simple-type.md"><strong>Колортипе</strong></a> simpleType</span><span class="sxs-lookup"><span data-stu-id="70fb2-123"><a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType</span></span></td>
<td><span data-ttu-id="70fb2-124">Необязательно</span><span class="sxs-lookup"><span data-stu-id="70fb2-124">Optional</span></span></td>
<td><span data-ttu-id="70fb2-125">Указывает цвет фона.</span><span class="sxs-lookup"><span data-stu-id="70fb2-125">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="70fb2-126">См. <a href="colortype-simple-type.md"><strong>колортипе</strong></a> simpleType.</span><span class="sxs-lookup"><span data-stu-id="70fb2-126">See <a href="colortype-simple-type.md"><strong>ColorType</strong></a> simpleType.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="70fb2-127">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="70fb2-127">Element Information</span></span>



|              |                                                                   |
|--------------|-------------------------------------------------------------------|
| <span data-ttu-id="70fb2-128">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="70fb2-128">Element type</span></span> | <span data-ttu-id="70fb2-129">[**Баккграундтипе**](backgroundtype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="70fb2-129">[**BackgroundType**](backgroundtype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="70fb2-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="70fb2-130">Namespace</span></span>    | <span data-ttu-id="70fb2-131">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="70fb2-131">urn:schemas-microsoft-com:tabletpc:richink</span></span>                        |
| <span data-ttu-id="70fb2-132">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="70fb2-132">Schema name</span></span>  | <span data-ttu-id="70fb2-133">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="70fb2-133">Journal Reader</span></span>                                                    |



 

 

 



