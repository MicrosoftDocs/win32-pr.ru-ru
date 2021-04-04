---
description: Указывает, какой элемент управления следует использовать при изменении свойства.
ms.assetid: cef6d76f-664a-4808-a224-e82a5adb2d70
title: едитконтрол
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 966f9742082fd6b5f939941a956eaae1ac4e427a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998592"
---
# <a name="editcontrol"></a><span data-ttu-id="e1f69-103">едитконтрол</span><span class="sxs-lookup"><span data-stu-id="e1f69-103">editControl</span></span>

<span data-ttu-id="e1f69-104">Указывает, какой элемент управления следует использовать при изменении свойства.</span><span class="sxs-lookup"><span data-stu-id="e1f69-104">Specifies what control to use when editing the property.</span></span> <span data-ttu-id="e1f69-105">Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [едитконтрол]() .</span><span class="sxs-lookup"><span data-stu-id="e1f69-105">There should be only one [editControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="e1f69-106">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="e1f69-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="e1f69-107">Если элемент [едитконтрол]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1f69-107">If no [editControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="e1f69-108">Если <typeInfo isInnate="true"> значение равно, этот элемент игнорируется, так как свойство присущей не может быть изменено.</span><span class="sxs-lookup"><span data-stu-id="e1f69-108">If <typeInfo isInnate="true">, this element is ignored because an innate property cannot be edited.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1f69-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1f69-109">Syntax</span></span>


```
<!-- editControl -->
<xs:element name="editControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="Calendar"/>
                    <xs:enumeration value="CheckboxDropList"/>
                    <xs:enumeration value="DropList"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="Text"/>
                    <xs:enumeration value="IconList"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="e1f69-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e1f69-110">Element Information</span></span>



| <span data-ttu-id="e1f69-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="e1f69-111">Parent Element</span></span>                                   | <span data-ttu-id="e1f69-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e1f69-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="e1f69-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e1f69-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="e1f69-114">Нет</span><span class="sxs-lookup"><span data-stu-id="e1f69-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="e1f69-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e1f69-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1f69-116">Атрибут</span><span class="sxs-lookup"><span data-stu-id="e1f69-116">Attribute</span></span></th>
<th><span data-ttu-id="e1f69-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e1f69-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1f69-118">управляющие</span><span class="sxs-lookup"><span data-stu-id="e1f69-118">control</span></span></td>
<td><span data-ttu-id="e1f69-119">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="e1f69-119">Public.</span></span> <span data-ttu-id="e1f69-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e1f69-120">Optional.</span></span> <span data-ttu-id="e1f69-121">Значение по умолчанию — &quot; Default &quot; .</span><span class="sxs-lookup"><span data-stu-id="e1f69-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="e1f69-122">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="e1f69-122">The following are valid values.</span></span> 
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e1f69-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e1f69-123">Value</span></span></th>
<th><span data-ttu-id="e1f69-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e1f69-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1f69-125">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e1f69-125">Default</span></span></td>
<td><span data-ttu-id="e1f69-126">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1f69-126">Default.</span></span> <span data-ttu-id="e1f69-127">Использует элемент управления по умолчанию, основанный на <typeInfo type=&quot;&quot;> атрибуте.</span><span class="sxs-lookup"><span data-stu-id="e1f69-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="e1f69-128">Типы по умолчанию перечислены ниже.</span><span class="sxs-lookup"><span data-stu-id="e1f69-128">The default types are listed below.</span></span> <span data-ttu-id="e1f69-129">Любой другой тип приводит к использованию &quot; &quot; элемента управления Text.</span><span class="sxs-lookup"><span data-stu-id="e1f69-129">Any other type results in using the &quot;Text&quot; control.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e1f69-130">Тип</span><span class="sxs-lookup"><span data-stu-id="e1f69-130">Type</span></span></th>
<th><span data-ttu-id="e1f69-131">Control</span><span class="sxs-lookup"><span data-stu-id="e1f69-131">Control</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e1f69-132">Строка</span><span class="sxs-lookup"><span data-stu-id="e1f69-132">String</span></span></td>
<td><span data-ttu-id="e1f69-133">Текст</span><span class="sxs-lookup"><span data-stu-id="e1f69-133">Text</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1f69-134">Строка (с несколькими значениями)</span><span class="sxs-lookup"><span data-stu-id="e1f69-134">String (multi-value)</span></span></td>
<td><span data-ttu-id="e1f69-135">мултивалуетекст</span><span class="sxs-lookup"><span data-stu-id="e1f69-135">MultiValueText</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1f69-136">Дата/время</span><span class="sxs-lookup"><span data-stu-id="e1f69-136">DateTime</span></span></td>
<td><span data-ttu-id="e1f69-137">Календарь</span><span class="sxs-lookup"><span data-stu-id="e1f69-137">Calendar</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1f69-138">Календарь</span><span class="sxs-lookup"><span data-stu-id="e1f69-138">Calendar</span></span></td>
<td><span data-ttu-id="e1f69-139">Использует элемент управления Calendar.</span><span class="sxs-lookup"><span data-stu-id="e1f69-139">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1f69-140">чеккбоксдроплист</span><span class="sxs-lookup"><span data-stu-id="e1f69-140">CheckboxDropList</span></span></td>
<td><span data-ttu-id="e1f69-141">Использует элемент управления "список" с флажками.</span><span class="sxs-lookup"><span data-stu-id="e1f69-141">Uses the list control with checkboxes.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1f69-142">дроплист</span><span class="sxs-lookup"><span data-stu-id="e1f69-142">DropList</span></span></td>
<td><span data-ttu-id="e1f69-143">Использует элемент управления "раскрывающийся список".</span><span class="sxs-lookup"><span data-stu-id="e1f69-143">Uses the dropdown list control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1f69-144">мултилинетекст</span><span class="sxs-lookup"><span data-stu-id="e1f69-144">MultiLineText</span></span></td>
<td><span data-ttu-id="e1f69-145">Использует многострочный элемент управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="e1f69-145">Uses the multi-line text edit control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1f69-146">мултивалуетекст</span><span class="sxs-lookup"><span data-stu-id="e1f69-146">MultiValueText</span></span></td>
<td><span data-ttu-id="e1f69-147">Использует многозначный элемент управления "поле ввода".</span><span class="sxs-lookup"><span data-stu-id="e1f69-147">Uses the multi-value text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1f69-148">Рейтинг</span><span class="sxs-lookup"><span data-stu-id="e1f69-148">Rating</span></span></td>
<td><span data-ttu-id="e1f69-149">Использует элемент управления рейтингом «5 звезд».</span><span class="sxs-lookup"><span data-stu-id="e1f69-149">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e1f69-150">Текст</span><span class="sxs-lookup"><span data-stu-id="e1f69-150">Text</span></span></td>
<td><span data-ttu-id="e1f69-151">Использует элемент управления редактированием текста.</span><span class="sxs-lookup"><span data-stu-id="e1f69-151">Uses the text edit control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e1f69-152">иконлист</span><span class="sxs-lookup"><span data-stu-id="e1f69-152">IconList</span></span></td>
<td><span data-ttu-id="e1f69-153"><strong>Windows 7 и более поздние версии.</strong></span><span class="sxs-lookup"><span data-stu-id="e1f69-153"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
