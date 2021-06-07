---
description: Содержит сведения о названии заметки журнала.
ms.assetid: efeed3a6-de5e-4698-9dc3-d0acb3d13dee
title: Элемент Title
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef687f809aae5c3722cdad84ee63d79c7bfcfb21
ms.sourcegitcommit: c3f669dc1d52278432bf75ad9fddba3257d26aa2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/04/2021
ms.locfileid: "111432226"
---
# <a name="title-element"></a><span data-ttu-id="6f1e4-103">Элемент Title</span><span class="sxs-lookup"><span data-stu-id="6f1e4-103">Title Element</span></span>

<span data-ttu-id="6f1e4-104">Содержит сведения о названии заметки журнала.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-104">Contains title information about the Journal note.</span></span>

## <a name="definition"></a><span data-ttu-id="6f1e4-105">Определение</span><span class="sxs-lookup"><span data-stu-id="6f1e4-105">Definition</span></span>

``` syntax
<xs:element name="Title" type="TitleType" minOccurs="0" />
```

## <a name="parent-elements"></a><span data-ttu-id="6f1e4-106">Родительские элементы</span><span class="sxs-lookup"><span data-stu-id="6f1e4-106">Parent Elements</span></span>

[<span data-ttu-id="6f1e4-107">**Stationery**</span><span class="sxs-lookup"><span data-stu-id="6f1e4-107">**Stationery**</span></span>](stationery-element.md)

## <a name="child-elements"></a><span data-ttu-id="6f1e4-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="6f1e4-108">Child Elements</span></span>

[<span data-ttu-id="6f1e4-109">**титлеареа**</span><span class="sxs-lookup"><span data-stu-id="6f1e4-109">**TitleArea**</span></span>](titlearea-element.md)

## <a name="attributes"></a><span data-ttu-id="6f1e4-110">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="6f1e4-110">Attributes</span></span>



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
<th><span data-ttu-id="6f1e4-111">attribute</span><span class="sxs-lookup"><span data-stu-id="6f1e4-111">Attribute</span></span></th>
<th><span data-ttu-id="6f1e4-112">Тип</span><span class="sxs-lookup"><span data-stu-id="6f1e4-112">Type</span></span></th>
<th><span data-ttu-id="6f1e4-113">Обязательно</span><span class="sxs-lookup"><span data-stu-id="6f1e4-113">Required</span></span></th>
<th><span data-ttu-id="6f1e4-114">Описание</span><span class="sxs-lookup"><span data-stu-id="6f1e4-114">Description</span></span></th>
<th><span data-ttu-id="6f1e4-115">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="6f1e4-115">Possible Values</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6f1e4-116"><strong>Стиль</strong></span><span class="sxs-lookup"><span data-stu-id="6f1e4-116"><strong>Style</strong></span></span></td>
<td><span data-ttu-id="6f1e4-117"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="6f1e4-117"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="6f1e4-118">Обязательно</span><span class="sxs-lookup"><span data-stu-id="6f1e4-118">Required</span></span></td>
<td><span data-ttu-id="6f1e4-119">Задает тип границы, окружающей заголовок примечания.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-119">Specifies the type of border surrounding the title of the note.</span></span></td>
<td><ul>
<li><span data-ttu-id="6f1e4-120">Нет</span><span class="sxs-lookup"><span data-stu-id="6f1e4-120">None</span></span></li>
<li><span data-ttu-id="6f1e4-121">солидскуаре</span><span class="sxs-lookup"><span data-stu-id="6f1e4-121">SolidSquare</span></span></li>
<li><span data-ttu-id="6f1e4-122">аутлинескуаре</span><span class="sxs-lookup"><span data-stu-id="6f1e4-122">OutlineSquare</span></span></li>
<li><span data-ttu-id="6f1e4-123">солидраундрект</span><span class="sxs-lookup"><span data-stu-id="6f1e4-123">SolidRoundRect</span></span></li>
<li><span data-ttu-id="6f1e4-124">аутлинераундрект</span><span class="sxs-lookup"><span data-stu-id="6f1e4-124">OutlineRoundRect</span></span></li>
<li><span data-ttu-id="6f1e4-125">солидраундректдоттедбаселине</span><span class="sxs-lookup"><span data-stu-id="6f1e4-125">SolidRoundRectDottedBaseline</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6f1e4-126"><strong>датестиле</strong></span><span class="sxs-lookup"><span data-stu-id="6f1e4-126"><strong>DateStyle</strong></span></span></td>
<td><span data-ttu-id="6f1e4-127"><strong>xs:string</strong></span><span class="sxs-lookup"><span data-stu-id="6f1e4-127"><strong>xs:string</strong></span></span></td>
<td><span data-ttu-id="6f1e4-128">Обязательно</span><span class="sxs-lookup"><span data-stu-id="6f1e4-128">Required</span></span></td>
<td><span data-ttu-id="6f1e4-129">Определяет, содержит ли заголовок дату или нет.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-129">Defines whether the title includes a date or not.</span></span></td>
<td><ul>
<li><span data-ttu-id="6f1e4-130">Нет</span><span class="sxs-lookup"><span data-stu-id="6f1e4-130">None</span></span></li>
<li><span data-ttu-id="6f1e4-131">Short</span><span class="sxs-lookup"><span data-stu-id="6f1e4-131">Short</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="6f1e4-132"><strong>Цвет</strong></span><span class="sxs-lookup"><span data-stu-id="6f1e4-132"><strong>Color</strong></span></span></td>
<td><span data-ttu-id="6f1e4-133"><a href="colortype-simple-type.md"><strong>Колортипе simpleType</strong></a></span><span class="sxs-lookup"><span data-stu-id="6f1e4-133"><a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a></span></span></td>
<td><span data-ttu-id="6f1e4-134">Необязательно</span><span class="sxs-lookup"><span data-stu-id="6f1e4-134">Optional</span></span></td>
<td><span data-ttu-id="6f1e4-135">Указывает цвет фона.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-135">Specifies the color of the background.</span></span></td>
<td><span data-ttu-id="6f1e4-136">См. <a href="colortype-simple-type.md"><strong>Колортипе simpleType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="6f1e4-136">See <a href="colortype-simple-type.md"><strong>ColorType simpleType</strong></a>.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="element-information"></a><span data-ttu-id="6f1e4-137">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="6f1e4-137">Element Information</span></span>



| <span data-ttu-id="6f1e4-138">Элемент</span><span class="sxs-lookup"><span data-stu-id="6f1e4-138">Element</span></span>      | <span data-ttu-id="6f1e4-139">Значение</span><span class="sxs-lookup"><span data-stu-id="6f1e4-139">Value</span></span>                                                   |
|--------------|---------------------------------------------------------|
| <span data-ttu-id="6f1e4-140">Тип элемента</span><span class="sxs-lookup"><span data-stu-id="6f1e4-140">Element type</span></span> | <span data-ttu-id="6f1e4-141">[**Титлетипе**](titletype-complex-type.md) complexType</span><span class="sxs-lookup"><span data-stu-id="6f1e4-141">[**TitleType**](titletype-complex-type.md) complexType</span></span> |
| <span data-ttu-id="6f1e4-142">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6f1e4-142">Namespace</span></span>    | <span data-ttu-id="6f1e4-143">urn: schemas-microsoft-com: TabletPC: ричинк</span><span class="sxs-lookup"><span data-stu-id="6f1e4-143">urn:schemas-microsoft-com:tabletpc:richink</span></span>              |
| <span data-ttu-id="6f1e4-144">Имя схемы</span><span class="sxs-lookup"><span data-stu-id="6f1e4-144">Schema name</span></span>  | <span data-ttu-id="6f1e4-145">Средство чтения журнала</span><span class="sxs-lookup"><span data-stu-id="6f1e4-145">Journal Reader</span></span>                                          |



 

 

 



