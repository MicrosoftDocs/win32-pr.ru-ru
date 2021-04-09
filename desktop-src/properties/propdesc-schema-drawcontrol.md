---
description: Указывает, какой элемент управления следует использовать при простом отображении свойства.
ms.assetid: 0fb8afc4-d16b-4c2e-80b3-da9935b11bb5
title: дравконтрол
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5318fdebc995ff45932f75b4000ceda6e74068e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104080560"
---
# <a name="drawcontrol"></a><span data-ttu-id="e6266-103">дравконтрол</span><span class="sxs-lookup"><span data-stu-id="e6266-103">drawControl</span></span>

<span data-ttu-id="e6266-104">Указывает, какой элемент управления следует использовать при простом отображении свойства.</span><span class="sxs-lookup"><span data-stu-id="e6266-104">Specifies what control to use when simply displaying the property.</span></span> <span data-ttu-id="e6266-105">Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [дравконтрол]() .</span><span class="sxs-lookup"><span data-stu-id="e6266-105">There should be only one [drawControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="e6266-106">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="e6266-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="e6266-107">Если элемент [дравконтрол]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e6266-107">If no [drawControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

<span data-ttu-id="e6266-108">Эта форма элемента управления не позволяет изменять свойства.</span><span class="sxs-lookup"><span data-stu-id="e6266-108">This form of the control does not allow for property editing.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6266-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e6266-109">Syntax</span></span>


```
<!-- drawControl -->
<xs:element name="drawControl"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:attribute name="control">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="Default"/>
                    <xs:enumeration value="MultiLineText"/>
                    <xs:enumeration value="MultiValueText"/>
                    <xs:enumeration value="PercentBar"/>
                    <xs:enumeration value="ProgressBar"/>
                    <xs:enumeration value="Rating"/>
                    <xs:enumeration value="StaticText"/>
                    <xs:enumeration value="IconList"/>
                    <xs:enumeration value="BooleanCheckMark"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="e6266-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e6266-110">Element Information</span></span>



| <span data-ttu-id="e6266-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="e6266-111">Parent Element</span></span>                                   | <span data-ttu-id="e6266-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e6266-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="e6266-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="e6266-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="e6266-114">Нет</span><span class="sxs-lookup"><span data-stu-id="e6266-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="e6266-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="e6266-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e6266-116">Атрибут</span><span class="sxs-lookup"><span data-stu-id="e6266-116">Attribute</span></span></th>
<th><span data-ttu-id="e6266-117">Описание</span><span class="sxs-lookup"><span data-stu-id="e6266-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6266-118">управляющие</span><span class="sxs-lookup"><span data-stu-id="e6266-118">control</span></span></td>
<td><span data-ttu-id="e6266-119">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="e6266-119">Public.</span></span> <span data-ttu-id="e6266-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="e6266-120">Optional.</span></span> <span data-ttu-id="e6266-121">Значение по умолчанию — &quot; Default &quot; .</span><span class="sxs-lookup"><span data-stu-id="e6266-121">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="e6266-122">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="e6266-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e6266-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e6266-123">Value</span></span></th>
<th><span data-ttu-id="e6266-124">Значение</span><span class="sxs-lookup"><span data-stu-id="e6266-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e6266-125">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="e6266-125">Default</span></span></td>
<td><span data-ttu-id="e6266-126">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e6266-126">Default.</span></span> <span data-ttu-id="e6266-127">Использует элемент управления по умолчанию, основанный на <typeInfo type=&quot;&quot;> атрибуте.</span><span class="sxs-lookup"><span data-stu-id="e6266-127">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="e6266-128">Тип по умолчанию — &quot; String &quot; (многозначный), а элемент управления по умолчанию — &quot; мултивалуетекст &quot; .</span><span class="sxs-lookup"><span data-stu-id="e6266-128">The default type is &quot;String&quot; (multi-value) and the default control is &quot;MultiValueText&quot;.</span></span> <span data-ttu-id="e6266-129">Любой другой тип приводит к использованию &quot; &quot; элемента управления статиктекст.</span><span class="sxs-lookup"><span data-stu-id="e6266-129">Any other type results in using the &quot;StaticText&quot; control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6266-130">мултилинетекст</span><span class="sxs-lookup"><span data-stu-id="e6266-130">MultiLineText</span></span></td>
<td><span data-ttu-id="e6266-131">Использует многострочный элемент управления Text.</span><span class="sxs-lookup"><span data-stu-id="e6266-131">Uses the multi-line text control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6266-132">мултивалуетекст</span><span class="sxs-lookup"><span data-stu-id="e6266-132">MultiValueText</span></span></td>
<td><span data-ttu-id="e6266-133">Использует многозначный элемент управления Text.</span><span class="sxs-lookup"><span data-stu-id="e6266-133">Uses the multi-value text control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6266-134">перцентбар</span><span class="sxs-lookup"><span data-stu-id="e6266-134">PercentBar</span></span></td>
<td><span data-ttu-id="e6266-135">Использует элемент управления "процентная черта".</span><span class="sxs-lookup"><span data-stu-id="e6266-135">Uses the percent bar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6266-136">ProgressBar</span><span class="sxs-lookup"><span data-stu-id="e6266-136">ProgressBar</span></span></td>
<td><span data-ttu-id="e6266-137">Использует элемент управления "индикатор выполнения".</span><span class="sxs-lookup"><span data-stu-id="e6266-137">Uses the progress bar control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6266-138">Рейтинг</span><span class="sxs-lookup"><span data-stu-id="e6266-138">Rating</span></span></td>
<td><span data-ttu-id="e6266-139">Использует элемент управления рейтингом «5 звезд».</span><span class="sxs-lookup"><span data-stu-id="e6266-139">Uses the 5-star rating control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6266-140">статиктекст</span><span class="sxs-lookup"><span data-stu-id="e6266-140">StaticText</span></span></td>
<td><span data-ttu-id="e6266-141">Использует <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>ипропертидескриптион:: форматфордисплай</strong></a> для вывода значения свойства.</span><span class="sxs-lookup"><span data-stu-id="e6266-141">Uses <a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay"><strong>IPropertyDescription::FormatForDisplay</strong></a> to display the property value.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e6266-142">иконлист</span><span class="sxs-lookup"><span data-stu-id="e6266-142">IconList</span></span></td>
<td><span data-ttu-id="e6266-143"><strong>Windows 7 и более поздние версии.</strong></span><span class="sxs-lookup"><span data-stu-id="e6266-143"><strong>Windows 7 and later.</strong></span></span> <span data-ttu-id="e6266-144">Перечисление значков.</span><span class="sxs-lookup"><span data-stu-id="e6266-144">An enumeration of icons.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e6266-145">булеанчеккмарк</span><span class="sxs-lookup"><span data-stu-id="e6266-145">BooleanCheckMark</span></span></td>
<td><span data-ttu-id="e6266-146"><strong>Windows 7 и более поздние версии.</strong></span><span class="sxs-lookup"><span data-stu-id="e6266-146"><strong>Windows 7 and later.</strong></span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
