---
description: 'Указывает, как Ипропертидескриптион:: Форматфордисплай должен форматировать значение свойства в виде строки. Это применимо только в том случае <displayInfo displayType=&\#0034;String&\#0034;> , если.'
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: булеанформат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d91332f0cc062e7ee4a83e3584776ecf09c5c4b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998593"
---
# <a name="booleanformat"></a><span data-ttu-id="b822b-104">булеанформат</span><span class="sxs-lookup"><span data-stu-id="b822b-104">booleanFormat</span></span>

<span data-ttu-id="b822b-105">Указывает, как [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) должен форматировать значение свойства в виде строки.</span><span class="sxs-lookup"><span data-stu-id="b822b-105">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="b822b-106">Это применимо только в том случае <displayInfo displayType="String"> , если.</span><span class="sxs-lookup"><span data-stu-id="b822b-106">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="b822b-107">Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [булеанформат]() .</span><span class="sxs-lookup"><span data-stu-id="b822b-107">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="b822b-108">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="b822b-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="b822b-109">Если элемент [булеанформат]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b822b-109">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="b822b-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b822b-110">Syntax</span></span>


```
      <!-- booleanFormat -->
      <xs:element name="booleanFormat"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="formatAs">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="YesNo"/>
                <xs:enumeration value="OnOff"/>
                <xs:enumeration value="TrueFalse"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="b822b-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="b822b-111">Element Information</span></span>



| <span data-ttu-id="b822b-112">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="b822b-112">Parent Element</span></span>                                   | <span data-ttu-id="b822b-113">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="b822b-113">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="b822b-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="b822b-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="b822b-115">Нет</span><span class="sxs-lookup"><span data-stu-id="b822b-115">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="b822b-116">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="b822b-116">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b822b-117">Атрибут</span><span class="sxs-lookup"><span data-stu-id="b822b-117">Attribute</span></span></th>
<th><span data-ttu-id="b822b-118">Описание</span><span class="sxs-lookup"><span data-stu-id="b822b-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b822b-119">форматас</span><span class="sxs-lookup"><span data-stu-id="b822b-119">formatAs</span></span></td>
<td><span data-ttu-id="b822b-120">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="b822b-120">Public.</span></span> <span data-ttu-id="b822b-121">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="b822b-121">Optional.</span></span> <span data-ttu-id="b822b-122">Значение по умолчанию — &quot; Данет &quot; .</span><span class="sxs-lookup"><span data-stu-id="b822b-122">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="b822b-123">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="b822b-123">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b822b-124">Значение</span><span class="sxs-lookup"><span data-stu-id="b822b-124">Value</span></span></th>
<th><span data-ttu-id="b822b-125">Значение</span><span class="sxs-lookup"><span data-stu-id="b822b-125">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b822b-126">Данет</span><span class="sxs-lookup"><span data-stu-id="b822b-126">YesNo</span></span></td>
<td><span data-ttu-id="b822b-127">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="b822b-127">Default.</span></span> <span data-ttu-id="b822b-128">Форматирует значение как « &quot; Да &quot; » или « &quot; нет &quot; ».</span><span class="sxs-lookup"><span data-stu-id="b822b-128">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="b822b-129">Необходимо, чтобы тип свойства был логическим.</span><span class="sxs-lookup"><span data-stu-id="b822b-129">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b822b-130">онофф</span><span class="sxs-lookup"><span data-stu-id="b822b-130">OnOff</span></span></td>
<td><span data-ttu-id="b822b-131">Форматирует значение как on, &quot; так &quot; и &quot; Off &quot; .</span><span class="sxs-lookup"><span data-stu-id="b822b-131">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="b822b-132">Необходимо, чтобы тип свойства был логическим.</span><span class="sxs-lookup"><span data-stu-id="b822b-132">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b822b-133">труефалсе</span><span class="sxs-lookup"><span data-stu-id="b822b-133">TrueFalse</span></span></td>
<td><span data-ttu-id="b822b-134">Форматирует значение как &quot; true &quot; или &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="b822b-134">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="b822b-135">Необходимо, чтобы тип свойства был логическим.</span><span class="sxs-lookup"><span data-stu-id="b822b-135">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
