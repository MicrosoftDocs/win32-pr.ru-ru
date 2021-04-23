---
description: Указывает способ отображения меток свойства.
ms.assetid: 9317aff9-abdd-46c2-aaff-62861925713b
title: лабелинфо
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b1cc0cfc417fae49527bcee50ac5043b1f07f309
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662767"
---
# <a name="labelinfo"></a><span data-ttu-id="5b900-103">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="5b900-103">labelInfo</span></span>

<span data-ttu-id="5b900-104">Указывает способ отображения меток свойства.</span><span class="sxs-lookup"><span data-stu-id="5b900-104">Specifies how the property's labels are displayed.</span></span> <span data-ttu-id="5b900-105">Для каждого элемента [пропертидескриптион](./propdesc-schema-propertydescription.md) должен быть только один элемент [лабелинфо]() .</span><span class="sxs-lookup"><span data-stu-id="5b900-105">There should be only one [labelInfo]() element for each [propertyDescription](./propdesc-schema-propertydescription.md) element.</span></span>

<span data-ttu-id="5b900-106">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="5b900-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="5b900-107">Если элемент [лабелинфо]() не указан, метка свойства не отображается; Однако это обычно является дефектом.</span><span class="sxs-lookup"><span data-stu-id="5b900-107">If no [labelInfo]() element is provided, then the property's label is not displayed; however, this would typically be a defect.</span></span>

## <a name="syntax"></a><span data-ttu-id="5b900-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="5b900-108">Syntax</span></span>


```
<!-- labelInfo -->
<xs:element name="labelInfo">
    <xs:complexType>
        <xs:attribute name="label" type="xs:string"/>
        <xs:attribute name="sortDescription">
            <xs:simpleType>
                <xs:restriction base="xs:string">
                    <xs:enumeration value="General"/>
                    <xs:enumeration value="AToZ"/>
                    <xs:enumeration value="LowestHighest"/>
                    <xs:enumeration value="OldestNewest"/>
                    <xs:enumeration value="SmallestLargest"/>
                </xs:restriction>
            </xs:simpleType>
        </xs:attribute>
        <xs:attribute name="invitationText" type="xs:string"/>
        <xs:attribute name="hideLabel" type="xs:boolean" default="false"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="5b900-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="5b900-109">Element Information</span></span>



| <span data-ttu-id="5b900-110">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="5b900-110">Parent Element</span></span>                                                   | <span data-ttu-id="5b900-111">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5b900-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="5b900-112">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="5b900-112">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) | <span data-ttu-id="5b900-113">Нет</span><span class="sxs-lookup"><span data-stu-id="5b900-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="5b900-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="5b900-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5b900-115">Атрибут</span><span class="sxs-lookup"><span data-stu-id="5b900-115">Attribute</span></span></th>
<th><span data-ttu-id="5b900-116">Описание</span><span class="sxs-lookup"><span data-stu-id="5b900-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5b900-117">метка</span><span class="sxs-lookup"><span data-stu-id="5b900-117">label</span></span></td>
<td><span data-ttu-id="5b900-118">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="5b900-118">Public.</span></span> <span data-ttu-id="5b900-119">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5b900-119">Optional.</span></span> <span data-ttu-id="5b900-120">Метка, отображаемая в пользовательском интерфейсе (например, метка столбца сведений или панель предварительного просмотра).</span><span class="sxs-lookup"><span data-stu-id="5b900-120">The label as it is displayed in the UI (for example, the details column label or preview pane).</span></span> <span data-ttu-id="5b900-121">Синтаксис позволяет получить прямую отображаемую строку или ссылку на непрямо отображаемую строку.</span><span class="sxs-lookup"><span data-stu-id="5b900-121">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="5b900-122">Используйте строку с косвенным отображением, так как она может быть локализована.</span><span class="sxs-lookup"><span data-stu-id="5b900-122">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="5b900-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>Ипропертидескриптион::</strong></a> Возвращает разрешенное отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="5b900-123"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getdisplayname"><strong>IPropertyDescription::GetDisplayName</strong></a> returns the resolved display name.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b900-124">сортдескриптион</span><span class="sxs-lookup"><span data-stu-id="5b900-124">sortDescription</span></span></td>
<td><span data-ttu-id="5b900-125">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5b900-125">Optional.</span></span> <span data-ttu-id="5b900-126">Указывает строки, предлагаемые в качестве параметров сортировки.</span><span class="sxs-lookup"><span data-stu-id="5b900-126">Specifies the strings offered as sort options.</span></span> <span data-ttu-id="5b900-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>Ипропертидескриптион:: жетсортдескриптион</strong></a> возвращает это описание сортировки.</span><span class="sxs-lookup"><span data-stu-id="5b900-127"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-getsortdescription"><strong>IPropertyDescription::GetSortDescription</strong></a> returns this sort description.</span></span> <span data-ttu-id="5b900-128">Следующие значения предоставляют соответствующие строки пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="5b900-128">The following values provide the corresponding UI strings.</span></span>
<ul>
<li><span data-ttu-id="5b900-129">Общие: Сортировка по мере &quot; &quot;  /  &quot; уменьшения&quot;</span><span class="sxs-lookup"><span data-stu-id="5b900-129">General: &quot;Sort going up&quot; / &quot;Sort going down&quot;</span></span></li>
<li><span data-ttu-id="5b900-130">Атоз: по &quot; верхнему &quot;  /  &quot; Z-поверх&quot;</span><span class="sxs-lookup"><span data-stu-id="5b900-130">AToZ: &quot;A on top&quot; / &quot;Z on top&quot;</span></span></li>
<li><span data-ttu-id="5b900-131">Ловессигхест: &quot; самый низкий на &quot; высшем верху  /  &quot;&quot;</span><span class="sxs-lookup"><span data-stu-id="5b900-131">LowestHighest: &quot;Lowest on top&quot; / &quot;Highest on top&quot;</span></span></li>
<li><span data-ttu-id="5b900-132">Олдестневест: &quot; самые старые самые &quot;  /  &quot; новые в начале&quot;</span><span class="sxs-lookup"><span data-stu-id="5b900-132">OldestNewest: &quot;Oldest on top&quot; / &quot;Newest on top&quot;</span></span></li>
<li><span data-ttu-id="5b900-133">Смаллестларжест: &quot; самый маленький на самый &quot;  /  &quot; крупный сверху&quot;</span><span class="sxs-lookup"><span data-stu-id="5b900-133">SmallestLargest: &quot;Smallest on top&quot; / &quot;Largest on top&quot;</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5b900-134">инвитатионтекст</span><span class="sxs-lookup"><span data-stu-id="5b900-134">invitationText</span></span></td>
<td><span data-ttu-id="5b900-135">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5b900-135">Optional.</span></span> <span data-ttu-id="5b900-136">Текст строки справки, отображаемый в качестве инструкции пользователю для элемента управления или подсказки (например, &quot; введите имя автора &quot; ).</span><span class="sxs-lookup"><span data-stu-id="5b900-136">The Help string text that is displayed as an instruction to the user for the control or ToolTip (for instance, &quot;Enter author name.&quot;).</span></span> <span data-ttu-id="5b900-137">Синтаксис позволяет получить прямую отображаемую строку или ссылку на непрямо отображаемую строку.</span><span class="sxs-lookup"><span data-stu-id="5b900-137">The syntax allows for a direct display string or an indirect display string reference.</span></span> <span data-ttu-id="5b900-138">Используйте строку с косвенным отображением, так как она может быть локализована.</span><span class="sxs-lookup"><span data-stu-id="5b900-138">Use the indirect display string because it can be localized.</span></span> <span data-ttu-id="5b900-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>Ипропертидескриптион:: жетедитинвитатион</strong></a> возвращает Разрешенный текст приглашения.</span><span class="sxs-lookup"><span data-stu-id="5b900-139"><a href="/windows/win32/api/propsys/nf-propsys-ipropertydescription-geteditinvitation"><strong>IPropertyDescription::GetEditInvitation</strong></a> returns the resolved invitation text.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5b900-140">хиделабел</span><span class="sxs-lookup"><span data-stu-id="5b900-140">hideLabel</span></span></td>
<td><span data-ttu-id="5b900-141">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="5b900-141">Optional.</span></span> <span data-ttu-id="5b900-142">Значение по умолчанию — &quot;false&quot;.</span><span class="sxs-lookup"><span data-stu-id="5b900-142">The default is &quot;false&quot;.</span></span> <span data-ttu-id="5b900-143">Указывает, скрыта ли метка.</span><span class="sxs-lookup"><span data-stu-id="5b900-143">Indicates whether the label is hidden.</span></span></td>
</tr>
</tbody>
</table>



 

 

 
