---
description: 'Указывает, как Ипропертидескриптион:: Форматфордисплай должен форматировать значение свойства в виде строки.'
ms.assetid: 49ba57b8-3e08-425f-98b2-52ed2c41a488
title: енумератедлист
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d098b47463b65c483be68eb7750da929df43cee7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702254"
---
# <a name="enumeratedlist"></a><span data-ttu-id="36cbf-103">енумератедлист</span><span class="sxs-lookup"><span data-stu-id="36cbf-103">enumeratedList</span></span>

<span data-ttu-id="36cbf-104">Указывает, как [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) должен форматировать значение свойства в виде строки.</span><span class="sxs-lookup"><span data-stu-id="36cbf-104">Specifies how [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) should format the property's value as a string.</span></span> <span data-ttu-id="36cbf-105">Он также влияет на то, как свойство может быть сгруппировано, или какие значения должны отображаться в списке, если "Едитконтрол" является листблокс.</span><span class="sxs-lookup"><span data-stu-id="36cbf-105">It also influences how the property may be grouped, or what values to show in the list if the "editControl" is a listblox.</span></span> <span data-ttu-id="36cbf-106">Это применимо только в том случае <displayInfo displayType="Enumerated"> , если.</span><span class="sxs-lookup"><span data-stu-id="36cbf-106">This is applicable only if <displayInfo displayType="Enumerated">.</span></span> <span data-ttu-id="36cbf-107">Для каждого элемента [displayInfo](./propdesc-schema-displayinfo.md) должен быть только один элемент [енумератедлист]() .</span><span class="sxs-lookup"><span data-stu-id="36cbf-107">There should be only one [enumeratedList]() element for each [displayInfo](./propdesc-schema-displayinfo.md) element.</span></span>

<span data-ttu-id="36cbf-108">При наличии нескольких элементов используется последний из них.</span><span class="sxs-lookup"><span data-stu-id="36cbf-108">If there are multiple elements, the last one is used.</span></span> <span data-ttu-id="36cbf-109">Если элемент [енумератедлист]() не указан, к описанию свойства применяются параметры атрибута по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="36cbf-109">If no [enumeratedList]() element is provided, then the default attribute settings are applied to the property description.</span></span>

## <a name="syntax"></a><span data-ttu-id="36cbf-110">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36cbf-110">Syntax</span></span>


```
<!-- enumeratedList -->
<xs:element name="enumeratedList"  minOccurs="0" maxOccurs="1">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enum" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="value" type="xs:string" use="required"/>
                    <xs:attribute name="text" type="xs:string" use="required"/>
                </xs:complexType>
            </xs:element>
            <xs:element name="enumRange" minOccurs="0" maxOccurs="unbounded">
                <xs:complexType>
                    <xs:attribute name="minValue" type="xs:integer" use="required"/>
                    <xs:attribute name="setValue" type="xs:integer"/>
                    <xs:attribute name="text" type="xs:string"/>
                </xs:complexType>
            </xs:element>
        </xs:sequence>
        <xs:attribute name="defaultText" type="xs:string"/>
        <xs:attribute name="useValueForDefault" type="xs:boolean"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="36cbf-111">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="36cbf-111">Element Information</span></span>



| <span data-ttu-id="36cbf-112">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="36cbf-112">Parent Element</span></span>                                   | <span data-ttu-id="36cbf-113">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="36cbf-113">Child Elements</span></span>                               |
|--------------------------------------------------|----------------------------------------------|
| [<span data-ttu-id="36cbf-114">displayInfo</span><span class="sxs-lookup"><span data-stu-id="36cbf-114">displayInfo</span></span>](./propdesc-schema-displayinfo.md) | [<span data-ttu-id="36cbf-115">enum</span><span class="sxs-lookup"><span data-stu-id="36cbf-115">enum</span></span>](./propdesc-schema-enum.md)           |
|                                                  | [<span data-ttu-id="36cbf-116">енумранже</span><span class="sxs-lookup"><span data-stu-id="36cbf-116">enumRange</span></span>](./propdesc-schema-enumrange.md) |



 

## <a name="attributes"></a><span data-ttu-id="36cbf-117">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="36cbf-117">Attributes</span></span>



| <span data-ttu-id="36cbf-118">Атрибут</span><span class="sxs-lookup"><span data-stu-id="36cbf-118">Attribute</span></span>          | <span data-ttu-id="36cbf-119">Описание</span><span class="sxs-lookup"><span data-stu-id="36cbf-119">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36cbf-120">defaultText</span><span class="sxs-lookup"><span data-stu-id="36cbf-120">defaultText</span></span>        | <span data-ttu-id="36cbf-121">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="36cbf-121">Public.</span></span> <span data-ttu-id="36cbf-122">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="36cbf-122">Optional.</span></span> <span data-ttu-id="36cbf-123">Укажите текст по умолчанию, который будет использоваться при присвоении значения [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) , не сопоставляемого с одним из перечисляемых элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="36cbf-123">Specify default text to use if a value is given to [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) that does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="36cbf-124">Синтаксис допускает прямую отображаемую строку или ссылку на непрямо отображаемую строку; Используйте ссылку, чтобы ее можно было локализовать.</span><span class="sxs-lookup"><span data-stu-id="36cbf-124">The syntax allows for a direct display string or an indirect display string reference; use the reference, so it can be localized.</span></span>                              |
| <span data-ttu-id="36cbf-125">усевалуефордефаулт</span><span class="sxs-lookup"><span data-stu-id="36cbf-125">useValueForDefault</span></span> | <span data-ttu-id="36cbf-126">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="36cbf-126">Public.</span></span> <span data-ttu-id="36cbf-127">Необязательный элемент.</span><span class="sxs-lookup"><span data-stu-id="36cbf-127">Optional.</span></span> <span data-ttu-id="36cbf-128">Если задать для этого параметра значение "true", [**ипропертидескриптион:: форматфордисплай**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) будет использовать значение "как есть", если оно не соответствует одному из перечисляемых элементов в списке.</span><span class="sxs-lookup"><span data-stu-id="36cbf-128">Setting this to "true" will inform [**IPropertyDescription::FormatForDisplay**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-formatfordisplay) to use the value as-is if the value does not map to one of the enumerated elements in the list.</span></span> <span data-ttu-id="36cbf-129">Для **ипропертидескриптион:: форматфордисплай** присвоение этому параметру значения "true" имеет приоритет над заданием "defaultText".</span><span class="sxs-lookup"><span data-stu-id="36cbf-129">For **IPropertyDescription::FormatForDisplay**, setting this to "true" takes precedence over setting the "defaultText".</span></span> <span data-ttu-id="36cbf-130">Значение по умолчанию — «false».</span><span class="sxs-lookup"><span data-stu-id="36cbf-130">The default is "false".</span></span> |



 

 

 
