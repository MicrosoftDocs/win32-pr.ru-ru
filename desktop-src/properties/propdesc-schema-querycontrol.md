---
description: Не поддерживается в Windows 7 и более поздних версиях. Указывает, какой элемент управления следует использовать в построителе запросов.
ms.assetid: 7d79c2fe-c63d-4ac5-8dd6-1a6103e53245
title: куериконтрол
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 448b47038f82afb9f860209bfe89eb9e6eecb890
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662762"
---
# <a name="querycontrol"></a><span data-ttu-id="d60aa-104">куериконтрол</span><span class="sxs-lookup"><span data-stu-id="d60aa-104">queryControl</span></span>

<span data-ttu-id="d60aa-105">Не поддерживается в Windows 7 и более поздних версиях.</span><span class="sxs-lookup"><span data-stu-id="d60aa-105">Not supported in Windows 7 and later.</span></span> <span data-ttu-id="d60aa-106">Указывает, какой элемент управления следует использовать в построителе запросов.</span><span class="sxs-lookup"><span data-stu-id="d60aa-106">Specifies what control to use in the query builder.</span></span> <span data-ttu-id="d60aa-107">Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [куериконтрол]() .</span><span class="sxs-lookup"><span data-stu-id="d60aa-107">There should be only one [queryControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="d60aa-108">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="d60aa-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="d60aa-109">Если элемент [куериконтрол]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d60aa-109">If no [queryControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="d60aa-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d60aa-110">Syntax</span></span>


```
<!-- queryControl -->
<xs:element name="queryControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Boolean"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="NumericText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="d60aa-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="d60aa-111">Element Information</span></span>



| <span data-ttu-id="d60aa-112">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="d60aa-112">Parent Element</span></span>                                   | <span data-ttu-id="d60aa-113">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="d60aa-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="d60aa-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="d60aa-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="d60aa-115">Нет</span><span class="sxs-lookup"><span data-stu-id="d60aa-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="d60aa-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="d60aa-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d60aa-117">Атрибут</span><span class="sxs-lookup"><span data-stu-id="d60aa-117">Attribute</span></span></th>
<th><span data-ttu-id="d60aa-118">Описание</span><span class="sxs-lookup"><span data-stu-id="d60aa-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d60aa-119">управляющие</span><span class="sxs-lookup"><span data-stu-id="d60aa-119">control</span></span></td>
<td><span data-ttu-id="d60aa-120">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="d60aa-120">Public.</span></span> <span data-ttu-id="d60aa-121">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="d60aa-121">Optional.</span></span> <span data-ttu-id="d60aa-122">Значение по умолчанию — &quot; Default &quot; .</span><span class="sxs-lookup"><span data-stu-id="d60aa-122">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="d60aa-123">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="d60aa-123">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d60aa-124">Значение</span><span class="sxs-lookup"><span data-stu-id="d60aa-124">Value</span></span></th>
<th><span data-ttu-id="d60aa-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d60aa-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d60aa-126">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="d60aa-126">Default</span></span></td>
<td><span data-ttu-id="d60aa-127">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d60aa-127">Default.</span></span> <span data-ttu-id="d60aa-128">Использует элемент управления по умолчанию, основанный на <typeInfo type=&quot;&quot;> атрибуте.</span><span class="sxs-lookup"><span data-stu-id="d60aa-128">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="d60aa-129">Типы по умолчанию перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="d60aa-129">The default types are listed below.</span></span> <span data-ttu-id="d60aa-130">Любой другой тип приводит к использованию &quot; &quot; элемента управления Text.</span><span class="sxs-lookup"><span data-stu-id="d60aa-130">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d60aa-131">Исключением</span><span class="sxs-lookup"><span data-stu-id="d60aa-131">ConditionType</span></span></th>
<th><span data-ttu-id="d60aa-132">Control</span><span class="sxs-lookup"><span data-stu-id="d60aa-132">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d60aa-133">Строка</span><span class="sxs-lookup"><span data-stu-id="d60aa-133">String</span></span></td>
<td><span data-ttu-id="d60aa-134">Текст</span><span class="sxs-lookup"><span data-stu-id="d60aa-134">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d60aa-135">Строка (с несколькими значениями)</span><span class="sxs-lookup"><span data-stu-id="d60aa-135">String (multi-value)</span></span></td>
<td><span data-ttu-id="d60aa-136">мултивалуетекст</span><span class="sxs-lookup"><span data-stu-id="d60aa-136">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d60aa-137">Число или размер</span><span class="sxs-lookup"><span data-stu-id="d60aa-137">Number or Size</span></span></td>
<td><span data-ttu-id="d60aa-138">нумериктекст</span><span class="sxs-lookup"><span data-stu-id="d60aa-138">NumericText</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d60aa-139">Number или size (enum)</span><span class="sxs-lookup"><span data-stu-id="d60aa-139">Number or Size (enum)</span></span></td>
<td><span data-ttu-id="d60aa-140">Список</span><span class="sxs-lookup"><span data-stu-id="d60aa-140">List</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d60aa-141">Дата/время</span><span class="sxs-lookup"><span data-stu-id="d60aa-141">DateTime</span></span></td>
<td><span data-ttu-id="d60aa-142">Календарь</span><span class="sxs-lookup"><span data-stu-id="d60aa-142">Calendar</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d60aa-143">Логический</span><span class="sxs-lookup"><span data-stu-id="d60aa-143">Boolean</span></span></td>
<td><span data-ttu-id="d60aa-144">Логический</span><span class="sxs-lookup"><span data-stu-id="d60aa-144">Boolean</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d60aa-145">Логический</span><span class="sxs-lookup"><span data-stu-id="d60aa-145">Boolean</span></span></td>
<td><span data-ttu-id="d60aa-146">Использует логический элемент управления.</span><span class="sxs-lookup"><span data-stu-id="d60aa-146">Uses the boolean control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d60aa-147">Календарь</span><span class="sxs-lookup"><span data-stu-id="d60aa-147">Calendar</span></span></td>
<td><span data-ttu-id="d60aa-148">Использует элемент управления "Календарь".</span><span class="sxs-lookup"><span data-stu-id="d60aa-148">Uses the dropdown calendar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d60aa-149">чеккбоксдроплист</span><span class="sxs-lookup"><span data-stu-id="d60aa-149">CheckboxDropList</span></span></td>
<td><span data-ttu-id="d60aa-150">Использует элемент управления "список" с флажками.</span><span class="sxs-lookup"><span data-stu-id="d60aa-150">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d60aa-151">дроплист</span><span class="sxs-lookup"><span data-stu-id="d60aa-151">DropList</span></span></td>
<td><span data-ttu-id="d60aa-152">Использует элемент управления "раскрывающийся список".</span><span class="sxs-lookup"><span data-stu-id="d60aa-152">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d60aa-153">мултивалуетекст</span><span class="sxs-lookup"><span data-stu-id="d60aa-153">MultiValueText</span></span></td>
<td><span data-ttu-id="d60aa-154">Использует многозначный элемент управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="d60aa-154">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d60aa-155">нумериктекст</span><span class="sxs-lookup"><span data-stu-id="d60aa-155">NumericText</span></span></td>
<td><span data-ttu-id="d60aa-156">Использует элемент управления числовым текстом.</span><span class="sxs-lookup"><span data-stu-id="d60aa-156">Uses the numeric text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d60aa-157">Рейтинг</span><span class="sxs-lookup"><span data-stu-id="d60aa-157">Rating</span></span></td>
<td><span data-ttu-id="d60aa-158">Использует элемент управления рейтингом «5 звезд».</span><span class="sxs-lookup"><span data-stu-id="d60aa-158">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d60aa-159">Текст</span><span class="sxs-lookup"><span data-stu-id="d60aa-159">Text</span></span></td>
<td><span data-ttu-id="d60aa-160">Использует элемент управления редактированием текста.</span><span class="sxs-lookup"><span data-stu-id="d60aa-160">Uses the text edit control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
