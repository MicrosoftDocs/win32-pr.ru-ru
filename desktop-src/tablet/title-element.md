---
description: Содержит сведения о названии заметки журнала.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Элемент Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2362e286482b329c50788b8eae4b4a30cbd1a125
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105693658"
---
# <a name="title-element"></a><span data-ttu-id="d1a0e-103">Элемент Title</span><span class="sxs-lookup"><span data-stu-id="d1a0e-103">Title Element</span></span>

<span data-ttu-id="d1a0e-104">Содержит сведения о названии заметки журнала.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="d1a0e-105">Определение</span><span class="sxs-lookup"><span data-stu-id="d1a0e-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="d1a0e-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="d1a0e-106">Parent Elements</span></span>

[<span data-ttu-id="d1a0e-107">**Stationery**</span><span class="sxs-lookup"><span data-stu-id="d1a0e-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="d1a0e-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d1a0e-108">Child Elements</span></span>

[<span data-ttu-id="d1a0e-109">**титлеареа**</span><span class="sxs-lookup"><span data-stu-id="d1a0e-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="d1a0e-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d1a0e-110">Attributes</span></span>



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
<th><span data-ttu-id="d1a0e-111">attribute</span><span class="sxs-lookup"><span data-stu-id="d1a0e-111">Attribute</span></span></th>
<th><span data-ttu-id="d1a0e-112">Тип</span><span class="sxs-lookup"><span data-stu-id="d1a0e-112">Type</span></span></th>
<th><span data-ttu-id="d1a0e-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d1a0e-113">Required</span></span></th>
<th><span data-ttu-id="d1a0e-114">Описание</span><span class="sxs-lookup"><span data-stu-id="d1a0e-114">Description</span></span></th>
<th><span data-ttu-id="d1a0e-115">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="d1a0e-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d1a0e-116"><strong>Style</strong></span><span class="sxs-lookup"><span data-stu-id="d1a0e-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="d1a0e-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="d1a0e-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="d1a0e-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d1a0e-118">Required</span></span></td>
<td><span data-ttu-id="d1a0e-119">Задает тип границы, окружающей заголовок примечания.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="d1a0e-120">Нет</span><span class="sxs-lookup"><span data-stu-id="d1a0e-120">None</span></span></li>
<li><span data-ttu-id="d1a0e-121">солидскуаре</span><span class="sxs-lookup"><span data-stu-id="d1a0e-121">SolidSquare</span></span></li>
<li><span data-ttu-id="d1a0e-122">аутлинескуаре</span><span class="sxs-lookup"><span data-stu-id="d1a0e-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="d1a0e-123">солидраундрект</span><span class="sxs-lookup"><span data-stu-id="d1a0e-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="d1a0e-124">аутлинераундрект</span><span class="sxs-lookup"><span data-stu-id="d1a0e-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="d1a0e-125">солидраундректдоттедбаселине</span><span class="sxs-lookup"><span data-stu-id="d1a0e-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d1a0e-126"><strong>датестиле</strong></span><span class="sxs-lookup"><span data-stu-id="d1a0e-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="d1a0e-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="d1a0e-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="d1a0e-128">Обязательно</span><span class="sxs-lookup"><span data-stu-id="d1a0e-128">Required</span></span></td>
<td><span data-ttu-id="d1a0e-129">Определяет, содержит ли заголовок дату или нет.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="d1a0e-130">Нет</span><span class="sxs-lookup"><span data-stu-id="d1a0e-130">None</span></span></li>
<li><span data-ttu-id="d1a0e-131">Short</span><span class="sxs-lookup"><span data-stu-id="d1a0e-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d1a0e-132"><strong>Цвет</strong></span><span class="sxs-lookup"><span data-stu-id="d1a0e-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="d1a0e-133"><a href="colortype-simple-type.md"><strong>Колортипе simpleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="d1a0e-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="d1a0e-134">Необязательно</span><span class="sxs-lookup"><span data-stu-id="d1a0e-134">Optional</span></span></td>
<td><span data-ttu-id="d1a0e-135">Указывает цвет фона.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="d1a0e-136">См. <a href="colortype-simple-type.md"><strong>Колортипе simpleType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d1a0e-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="d1a0e-137">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d1a0e-137">Element Information</span></span>



|              |                                                         |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="d1a0e-138">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="d1a0e-138">Element type</span></span> | <span data-ttu-id="d1a0e-139">[**Титлетипе**](titletype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="d1a0e-139">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="d1a0e-140">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d1a0e-140">Namespace</span></span>    | <span data-ttu-id="d1a0e-141">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="d1a0e-141">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="d1a0e-142">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="d1a0e-142">Schema name</span></span>  | <span data-ttu-id="d1a0e-143">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="d1a0e-143">Journal Reader</span></span>                                          |



 

 

 



