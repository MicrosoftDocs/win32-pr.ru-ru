---
description: Указывает, какой элемент управления следует использовать в меню фильтра заголовка.
ms.assetid: a3117e16-20d0-4637-b726-9fa49516ad5c
title: филтерконтрол
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0c0de28eaa349b9a999ba39c1bad47aa01d43d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662769"
---
# <a name="filtercontrol"></a><span data-ttu-id="793b5-103">филтерконтрол</span><span class="sxs-lookup"><span data-stu-id="793b5-103">filterControl</span></span>

<span data-ttu-id="793b5-104">Указывает, какой элемент управления следует использовать в меню фильтра заголовка.</span><span class="sxs-lookup"><span data-stu-id="793b5-104">Specifies what control to use in the header filter menu.</span></span> <span data-ttu-id="793b5-105">Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [филтерконтрол]() .</span><span class="sxs-lookup"><span data-stu-id="793b5-105">There should be only one [filterControl]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="793b5-106">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="793b5-106">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="793b5-107">Если элемент [филтерконтрол]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="793b5-107">If no [filterControl]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="793b5-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="793b5-108">Syntax</span></span>


```
      <!-- filterControl -->
      <xs:element name="filterControl"  minOccurs="0" maxOccurs="1">
        <xs:complexType>
          <xs:attribute name="control">
            <xs:simpleType>
              <xs:restriction base="xs:string">
                <xs:enumeration value="Default"/>
                <xs:enumeration value="Calendar"/>
                <xs:enumeration value="Rating"/>
              </xs:restriction>
            </xs:simpleType>
          </xs:attribute>
        </xs:complexType>
      </xs:element>
```



## <a name="element-information"></a><span data-ttu-id="793b5-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="793b5-109">Element Information</span></span>



| <span data-ttu-id="793b5-110">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="793b5-110">Parent Element</span></span>                                   | <span data-ttu-id="793b5-111">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="793b5-111">Child Elements</span></span> |
|--------------------------------------------------|----------------|
| [<span data-ttu-id="793b5-112">displayInfo</span><span class="sxs-lookup"><span data-stu-id="793b5-112">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | <span data-ttu-id="793b5-113">Нет</span><span class="sxs-lookup"><span data-stu-id="793b5-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="793b5-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="793b5-114">Attributes</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="793b5-115">Атрибут</span><span class="sxs-lookup"><span data-stu-id="793b5-115">Attribute</span></span></th>
<th><span data-ttu-id="793b5-116">Описание</span><span class="sxs-lookup"><span data-stu-id="793b5-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="793b5-117">управляющие</span><span class="sxs-lookup"><span data-stu-id="793b5-117">control</span></span></td>
<td><span data-ttu-id="793b5-118">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="793b5-118">Public.</span></span> <span data-ttu-id="793b5-119">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="793b5-119">Optional.</span></span> <span data-ttu-id="793b5-120">Значение по умолчанию — &quot; Default &quot; .</span><span class="sxs-lookup"><span data-stu-id="793b5-120">Default is &quot;Default&quot;.</span></span> <span data-ttu-id="793b5-121">Допустимы следующие значения.</span><span class="sxs-lookup"><span data-stu-id="793b5-121">The following are valid values.</span></span> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="793b5-122">Значение</span><span class="sxs-lookup"><span data-stu-id="793b5-122">Value</span></span></th>
<th><span data-ttu-id="793b5-123">Значение</span><span class="sxs-lookup"><span data-stu-id="793b5-123">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="793b5-124">Значение по умолчанию</span><span class="sxs-lookup"><span data-stu-id="793b5-124">Default</span></span></td>
<td><span data-ttu-id="793b5-125">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="793b5-125">Default.</span></span> <span data-ttu-id="793b5-126">Использует элемент управления по умолчанию, основанный на <typeInfo type=&quot;&quot;> атрибуте.</span><span class="sxs-lookup"><span data-stu-id="793b5-126">Uses the default control, based upon the <typeInfo type=&quot;&quot;> attribute.</span></span> <span data-ttu-id="793b5-127">По умолчанию используется тип &quot; DateTime &quot; , а элементом управления по умолчанию является &quot; Calendar &quot; .</span><span class="sxs-lookup"><span data-stu-id="793b5-127">The default type is &quot;DateTime&quot; and the default control is &quot;Calendar&quot;.</span></span> <span data-ttu-id="793b5-128">Любой другой тип приведет к отсутствию специального элемента управления фильтра.</span><span class="sxs-lookup"><span data-stu-id="793b5-128">Any other type results in no special filter control.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="793b5-129">Календарь</span><span class="sxs-lookup"><span data-stu-id="793b5-129">Calendar</span></span></td>
<td><span data-ttu-id="793b5-130">Использует элемент управления Calendar.</span><span class="sxs-lookup"><span data-stu-id="793b5-130">Uses the calendar control.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="793b5-131">Рейтинг</span><span class="sxs-lookup"><span data-stu-id="793b5-131">Rating</span></span></td>
<td><span data-ttu-id="793b5-132">Использует элемент управления рейтингом «5 звезд».</span><span class="sxs-lookup"><span data-stu-id="793b5-132">Uses the 5-star rating control.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
</tbody>
</table>



 

 

 
