---
description: 'Указывает, как Ипропертидескриптион:: Форматфордисплай должен форматировать значение свойства Булеанформат в виде строки.'
ms.assetid: f6384910-4411-4ac2-884d-3476c1b6ff96
title: булеанформат
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 528458d9c31d54ef43eca8325b1daeef4eee1195
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405967"
---
# <a name="booleanformat"></a><span data-ttu-id="807b8-103">булеанформат</span><span class="sxs-lookup"><span data-stu-id="807b8-103">booleanFormat</span></span>

<span data-ttu-id="807b8-104">Указывает, как [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) должен форматировать значение свойства в виде строки.</span><span class="sxs-lookup"><span data-stu-id="807b8-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="807b8-105">Это применимо только в том случае <displayInfo displayType="String"> , если.</span><span class="sxs-lookup"><span data-stu-id="807b8-105">This is applicable only if <displayInfo displayType="String">.</span></span> <span data-ttu-id="807b8-106">Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [булеанформат]() .</span><span class="sxs-lookup"><span data-stu-id="807b8-106">There should be only one [booleanFormat]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="807b8-107">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="807b8-107">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="807b8-108">Если элемент [булеанформат]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="807b8-108">If no [booleanFormat]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="807b8-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="807b8-109">Syntax</span></span>


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



## <a name="element-information"></a><span data-ttu-id="807b8-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="807b8-110">Element Information</span></span>



| <span data-ttu-id="807b8-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="807b8-111">Parent Element</span></span>                                   | <span data-ttu-id="807b8-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="807b8-112">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="807b8-113">displayInfo</span><span class="sxs-lookup"><span data-stu-id="807b8-113">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="807b8-114">Нет</span><span class="sxs-lookup"><span data-stu-id="807b8-114">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="807b8-115">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="807b8-115">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="807b8-116">Атрибут</span><span class="sxs-lookup"><span data-stu-id="807b8-116">Attribute</span></span></th>
<th><span data-ttu-id="807b8-117">Описание</span><span class="sxs-lookup"><span data-stu-id="807b8-117">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="807b8-118">форматас</span><span class="sxs-lookup"><span data-stu-id="807b8-118">formatAs</span></span></td>
<td><span data-ttu-id="807b8-119">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="807b8-119">Public.</span></span> <span data-ttu-id="807b8-120">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="807b8-120">Optional.</span></span> <span data-ttu-id="807b8-121">Значение по умолчанию — &quot; Данет &quot; .</span><span class="sxs-lookup"><span data-stu-id="807b8-121">Default is &quot;YesNo&quot;.</span></span> <span data-ttu-id="807b8-122">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="807b8-122">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="807b8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="807b8-123">Value</span></span></th>
<th><span data-ttu-id="807b8-124">Значение</span><span class="sxs-lookup"><span data-stu-id="807b8-124">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="807b8-125">Данет</span><span class="sxs-lookup"><span data-stu-id="807b8-125">YesNo</span></span></td>
<td><span data-ttu-id="807b8-126">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="807b8-126">Default.</span></span> <span data-ttu-id="807b8-127">Форматирует значение как « &quot; Да &quot; » или « &quot; нет &quot; ».</span><span class="sxs-lookup"><span data-stu-id="807b8-127">Formats the value as either &quot;Yes&quot; or &quot;No&quot;.</span></span> <span data-ttu-id="807b8-128">Необходимо, чтобы тип свойства был логическим.</span><span class="sxs-lookup"><span data-stu-id="807b8-128">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="807b8-129">онофф</span><span class="sxs-lookup"><span data-stu-id="807b8-129">OnOff</span></span></td>
<td><span data-ttu-id="807b8-130">Форматирует значение как on, &quot; так &quot; и &quot; Off &quot; .</span><span class="sxs-lookup"><span data-stu-id="807b8-130">Formats the value as either &quot;On&quot; or &quot;Off&quot;.</span></span> <span data-ttu-id="807b8-131">Необходимо, чтобы тип свойства был логическим.</span><span class="sxs-lookup"><span data-stu-id="807b8-131">Requires the property type to be Boolean.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="807b8-132">труефалсе</span><span class="sxs-lookup"><span data-stu-id="807b8-132">TrueFalse</span></span></td>
<td><span data-ttu-id="807b8-133">Форматирует значение как &quot; true &quot; или &quot; false &quot; .</span><span class="sxs-lookup"><span data-stu-id="807b8-133">Formats the value as either &quot;True&quot; or &quot;False&quot;.</span></span> <span data-ttu-id="807b8-134">Необходимо, чтобы тип свойства был логическим.</span><span class="sxs-lookup"><span data-stu-id="807b8-134">Requires the property type to be Boolean.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
