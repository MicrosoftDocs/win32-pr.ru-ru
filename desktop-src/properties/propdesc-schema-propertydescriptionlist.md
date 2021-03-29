---
description: Контейнер для одного или нескольких отдельных элементов Пропертидескриптион.
ms.assetid: b54aaa85-6928-470e-9630-44b094205106
title: пропертидескриптионлист
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2cd0beaf4dbbd8b71c7f4b3335c169754c704d9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105647263"
---
# <a name="propertydescriptionlist"></a><span data-ttu-id="36766-103">пропертидескриптионлист</span><span class="sxs-lookup"><span data-stu-id="36766-103">propertyDescriptionList</span></span>

<span data-ttu-id="36766-104">Контейнер для одного или нескольких отдельных элементов [пропертидескриптион](./propdesc-schema-propertydescription.md) .</span><span class="sxs-lookup"><span data-stu-id="36766-104">Container for one or many individual [propertyDescription](./propdesc-schema-propertydescription.md) elements.</span></span> <span data-ttu-id="36766-105">Файл схемы описания свойства. пропдеск должен содержать хотя бы один элемент [пропертидескриптионлист]() .</span><span class="sxs-lookup"><span data-stu-id="36766-105">A .propdesc property description schema file should contain at least one [propertyDescriptionList]() element.</span></span>

## <a name="syntax"></a><span data-ttu-id="36766-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36766-106">Syntax</span></span>


```
<!-- propertyDescriptionList -->
<xs:element name="propertyDescriptionList">
    <xs:complexType>
        <xs:sequence>
            <xs:element ref="s:propertyDescription" minOccurs="1" maxOccurs="unbounded"/>
        </xs:sequence>
        <xs:attribute name="publisher" type="xs:string" use="required"/>
        <xs:attribute name="product"   type="xs:string" use="required"/>
    </xs:complexType>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_formatid_and_propid">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@formatID"/>
        <xs:field    xpath="@propID"/>
    </xs:unique>

    <xs:unique name="No_two_propertyDescriptions_can_have_the_same_canonical_name">
        <xs:selector xpath="s:propertyDescription"/>
        <xs:field    xpath="@name"/>
    </xs:unique>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="36766-107">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="36766-107">Element Information</span></span>



| <span data-ttu-id="36766-108">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="36766-108">Parent Element</span></span>                        | <span data-ttu-id="36766-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="36766-109">Child Elements</span></span>                                                   |
|---------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="36766-110">schema</span><span class="sxs-lookup"><span data-stu-id="36766-110">schema</span></span>](./propdesc-schema-entry.md) | [<span data-ttu-id="36766-111">пропертидескриптион</span><span class="sxs-lookup"><span data-stu-id="36766-111">propertyDescription</span></span>](./propdesc-schema-propertydescription.md) |



 

## <a name="attributes"></a><span data-ttu-id="36766-112">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="36766-112">Attributes</span></span>



| <span data-ttu-id="36766-113">Атрибут</span><span class="sxs-lookup"><span data-stu-id="36766-113">Attribute</span></span> | <span data-ttu-id="36766-114">Описание</span><span class="sxs-lookup"><span data-stu-id="36766-114">Description</span></span>                                                               |
|-----------|---------------------------------------------------------------------------|
| <span data-ttu-id="36766-115">publisher</span><span class="sxs-lookup"><span data-stu-id="36766-115">publisher</span></span> | <span data-ttu-id="36766-116">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="36766-116">Public.</span></span> <span data-ttu-id="36766-117">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="36766-117">Required.</span></span> <span data-ttu-id="36766-118">Отображаемое имя издателя, предоставляющего схему.</span><span class="sxs-lookup"><span data-stu-id="36766-118">The display name of the publisher providing the schema.</span></span> |
| <span data-ttu-id="36766-119">product</span><span class="sxs-lookup"><span data-stu-id="36766-119">product</span></span>   | <span data-ttu-id="36766-120">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="36766-120">Public.</span></span> <span data-ttu-id="36766-121">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="36766-121">Required.</span></span> <span data-ttu-id="36766-122">Отображаемое имя продукта, предоставляющего схему.</span><span class="sxs-lookup"><span data-stu-id="36766-122">The display name of the product providing the schema.</span></span>   |



 

## <a name="remarks"></a><span data-ttu-id="36766-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="36766-123">Remarks</span></span>

<span data-ttu-id="36766-124">[Пропертидескриптионлист]() не следует путать с "списками свойств" и [**ипропертидескриптионлист**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), которые полностью отделены друг от друга.</span><span class="sxs-lookup"><span data-stu-id="36766-124">The [propertyDescriptionList]() should not be confused with "property lists" and [**IPropertyDescriptionList**](/windows/win32/api/propsys/nn-propsys-ipropertydescriptionlist), which are completely separate.</span></span>

 

 
