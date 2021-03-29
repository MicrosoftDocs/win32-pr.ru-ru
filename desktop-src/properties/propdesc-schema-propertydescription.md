---
description: Описывает одно уникальное каноническое свойство.
ms.assetid: 1a36ec83-5d8a-4fc5-be3d-a8c2f0983057
title: пропертидескриптион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 233f6d9b1242a9f02b2edbb2bb29cefaef625c7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103991544"
---
# <a name="propertydescription"></a><span data-ttu-id="31ced-103">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="31ced-103">propertyDescription</span></span>

<span data-ttu-id="31ced-104">Описывает одно уникальное каноническое свойство.</span><span class="sxs-lookup"><span data-stu-id="31ced-104">Describes a single unique canonical property.</span></span> <span data-ttu-id="31ced-105">Каждое такое свойство, предназначенное для доступа в системе, должно иметь соответствующий элемент [пропертидескриптион]() .</span><span class="sxs-lookup"><span data-stu-id="31ced-105">Every such property intended to be available in the system must have a corresponding [propertyDescription]() element.</span></span>

## <a name="syntax-for-windows-7"></a><span data-ttu-id="31ced-106">Синтаксис для Windows 7</span><span class="sxs-lookup"><span data-stu-id="31ced-106">Syntax for Windows 7</span></span>


```
<!-- propertyDescription for Windows 7-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
            <xs:element ref="relatedPropertyInfo" minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="propid" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="syntax-for-vista"></a><span data-ttu-id="31ced-107">Синтаксис для Vista</span><span class="sxs-lookup"><span data-stu-id="31ced-107">Syntax for Vista</span></span>


```
<!-- propertyDescription for Windows Vista-->
<xs:element name="propertyDescription">
    <xs:complexType>
        <xs:all>
            <xs:element ref="searchInfo"          minOccurs="0" maxOccurs="1"/>
            <xs:element ref="labelInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="typeInfo"            minOccurs="0" maxOccurs="1"/>
            <xs:element ref="aliasInfo"           minOccurs="0" maxOccurs="1"/>
            <xs:element ref="displayInfo"         minOccurs="0" maxOccurs="1"/>
        </xs:all>

        <xs:attribute name="formatID"  type="uuid" use="required"/>
        <xs:attribute name="propID"    type="xs:nonNegativeInteger" use="required"/>
        <xs:attribute name="name"      type="canonical-name"        use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="31ced-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="31ced-108">Element Information</span></span>



| <span data-ttu-id="31ced-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="31ced-109">Parent Element</span></span>                                                           | <span data-ttu-id="31ced-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="31ced-110">Child Elements</span></span>                                                   |
|--------------------------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="31ced-111">пропертидескриптионлист</span><span class="sxs-lookup"><span data-stu-id="31ced-111">propertyDescriptionList</span></span>](./propdesc-schema-propertydescriptionlist.md) | [<span data-ttu-id="31ced-112">сеарчинфо</span><span class="sxs-lookup"><span data-stu-id="31ced-112">searchInfo</span></span>](./propdesc-schema-searchinfo.md)                   |
|                                                                          | [<span data-ttu-id="31ced-113">лабелинфо</span><span class="sxs-lookup"><span data-stu-id="31ced-113">labelInfo</span></span>](./propdesc-schema-labelinfo.md)                     |
|                                                                          | [<span data-ttu-id="31ced-114">typeInfo</span><span class="sxs-lookup"><span data-stu-id="31ced-114">typeInfo</span></span>](./propdesc-schema-typeinfo.md)                       |
|                                                                          | [<span data-ttu-id="31ced-115">aliasInfo</span><span class="sxs-lookup"><span data-stu-id="31ced-115">aliasInfo</span></span>](./propdesc-schema-aliasinfo.md)                     |
|                                                                          | [<span data-ttu-id="31ced-116">displayInfo</span><span class="sxs-lookup"><span data-stu-id="31ced-116">displayInfo</span></span>](./propdesc-schema-displayinfo.md)                 |
|                                                                          | [<span data-ttu-id="31ced-117">релатедпропертинфо</span><span class="sxs-lookup"><span data-stu-id="31ced-117">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) |



 

## <a name="attributes"></a><span data-ttu-id="31ced-118">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="31ced-118">Attributes</span></span>



| <span data-ttu-id="31ced-119">Атрибут</span><span class="sxs-lookup"><span data-stu-id="31ced-119">Attribute</span></span> | <span data-ttu-id="31ced-120">Описание</span><span class="sxs-lookup"><span data-stu-id="31ced-120">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                         |
|-----------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="31ced-121">name</span><span class="sxs-lookup"><span data-stu-id="31ced-121">name</span></span>      | <span data-ttu-id="31ced-122">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="31ced-122">Required.</span></span> <span data-ttu-id="31ced-123">Каноническое имя свойства, уникальное для системы; Например, `System.Rating` .</span><span class="sxs-lookup"><span data-stu-id="31ced-123">The canonical property name, unique to the system; for example, `System.Rating`.</span></span> <span data-ttu-id="31ced-124">Эта строка имеет тип канонического типа и ограничена 64 символами.</span><span class="sxs-lookup"><span data-stu-id="31ced-124">This string is of type canonical-type and is limited to 64 characters.</span></span> <span data-ttu-id="31ced-125">Имя чувствительно к регистру и должно использовать следующий синтаксис: Publisher. Application. PropertyName.</span><span class="sxs-lookup"><span data-stu-id="31ced-125">The name is case-sensitive and should use the following syntax: Publisher.Application.PropertyName.</span></span> <span data-ttu-id="31ced-126">[**Ипропертидескриптион:: жетканоникалнаме**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) возвращает это значение.</span><span class="sxs-lookup"><span data-stu-id="31ced-126">[**IPropertyDescription::GetCanonicalName**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getcanonicalname) returns this value.</span></span> |
| <span data-ttu-id="31ced-127">форматид</span><span class="sxs-lookup"><span data-stu-id="31ced-127">formatID</span></span>  | <span data-ttu-id="31ced-128">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="31ced-128">Required.</span></span> <span data-ttu-id="31ced-129">Идентификатор формата свойства (FMTID).</span><span class="sxs-lookup"><span data-stu-id="31ced-129">The property's format identifier (FMTID).</span></span> <span data-ttu-id="31ced-130">Значение должно включать заключенные в фигурные скобки. Например, `{64440492-4C8B-11D1-8B70-080036B11A03}` .</span><span class="sxs-lookup"><span data-stu-id="31ced-130">The value must include enclosing braces; for example, `{64440492-4C8B-11D1-8B70-080036B11A03}`.</span></span> <span data-ttu-id="31ced-131">[**Ипропертидескриптион:: жетпропертикэй**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) возвращает это значение.</span><span class="sxs-lookup"><span data-stu-id="31ced-131">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span>                                                                                                                       |
| <span data-ttu-id="31ced-132">propID</span><span class="sxs-lookup"><span data-stu-id="31ced-132">propID</span></span>    | <span data-ttu-id="31ced-133">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="31ced-133">Required.</span></span> <span data-ttu-id="31ced-134">Идентификатор свойства (PID); Например, `9` .</span><span class="sxs-lookup"><span data-stu-id="31ced-134">The property identifier (PID); for example, `9`.</span></span> <span data-ttu-id="31ced-135">[**Ипропертидескриптион:: жетпропертикэй**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) возвращает это значение.</span><span class="sxs-lookup"><span data-stu-id="31ced-135">[**IPropertyDescription::GetPropertyKey**](/windows/win32/api/propsys/nf-propsys-ipropertydescription-getpropertykey) returns this value.</span></span> <span data-ttu-id="31ced-136">Это значение должно быть больше или равно 2.</span><span class="sxs-lookup"><span data-stu-id="31ced-136">This value must be greater than or equal to 2.</span></span> <span data-ttu-id="31ced-137">Значения 0 и 1 зарезервированы системой.</span><span class="sxs-lookup"><span data-stu-id="31ced-137">The values 0 and 1 are reserved by the system.</span></span>                                                                                                                  |



 

 

 
