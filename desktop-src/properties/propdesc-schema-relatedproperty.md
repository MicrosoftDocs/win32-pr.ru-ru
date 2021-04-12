---
description: Новые для Windows 7. Определяет свойство, связанное со свойством, определенным в файле описания свойства.
ms.assetid: 30167942-141A-4f37-B019-0811BA654124
title: relatedProperty
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cabde093a47a25834598659d3ad38e0847c1351d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344802"
---
# <a name="relatedproperty"></a><span data-ttu-id="0381d-104">relatedProperty</span><span class="sxs-lookup"><span data-stu-id="0381d-104">relatedProperty</span></span>

<span data-ttu-id="0381d-105">Новые для Windows 7.</span><span class="sxs-lookup"><span data-stu-id="0381d-105">New for Windows 7.</span></span> <span data-ttu-id="0381d-106">Определяет свойство, связанное со свойством, определенным в файле описания свойства.</span><span class="sxs-lookup"><span data-stu-id="0381d-106">Identifies a property that is related to the property defined in the property description file.</span></span> <span data-ttu-id="0381d-107">В [релатедпропертинфо](./propdesc-schema-relatedpropertyinfo.md) может быть столько элементов [relatedProperty]() , сколько необходимо.</span><span class="sxs-lookup"><span data-stu-id="0381d-107">There can be as many [relatedProperty]() elements within a [relatedPropertyInfo](./propdesc-schema-relatedpropertyinfo.md) as needed.</span></span>

## <a name="syntax"></a><span data-ttu-id="0381d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0381d-108">Syntax</span></span>


```
<!-- relatedPropertyInfo -->
<xs:element name="relatedProperty" minOccurs="0" maxOccurs="unbounded">
    <xs:complexType>
        <xs:attribute name="relationshipName" type="canonical-name" use="required"/>
        <xs:attribute name="propertyName" type="canonical-name" use="required"/>
    </xs:complexType>
</xs:element>
```



## <a name="element-information"></a><span data-ttu-id="0381d-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="0381d-109">Element Information</span></span>



| <span data-ttu-id="0381d-110">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="0381d-110">Parent Element</span></span>                                                   | <span data-ttu-id="0381d-111">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="0381d-111">Child Elements</span></span> |
|------------------------------------------------------------------|----------------|
| [<span data-ttu-id="0381d-112">релатедпропертинфо</span><span class="sxs-lookup"><span data-stu-id="0381d-112">relatedPropertyInfo</span></span>](./propdesc-schema-relatedpropertyinfo.md) | <span data-ttu-id="0381d-113">Нет</span><span class="sxs-lookup"><span data-stu-id="0381d-113">None</span></span>           |



 

## <a name="attributes"></a><span data-ttu-id="0381d-114">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="0381d-114">Attributes</span></span>



| <span data-ttu-id="0381d-115">Атрибут</span><span class="sxs-lookup"><span data-stu-id="0381d-115">Attribute</span></span>        | <span data-ttu-id="0381d-116">Описание</span><span class="sxs-lookup"><span data-stu-id="0381d-116">Description</span></span>                                                        |
|------------------|--------------------------------------------------------------------|
| <span data-ttu-id="0381d-117">relationshipName</span><span class="sxs-lookup"><span data-stu-id="0381d-117">relationshipName</span></span> | <span data-ttu-id="0381d-118">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="0381d-118">Public.</span></span> <span data-ttu-id="0381d-119">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="0381d-119">Required.</span></span> <span data-ttu-id="0381d-120">Каноническое имя связи свойств.</span><span class="sxs-lookup"><span data-stu-id="0381d-120">The canonical name of the property relationship.</span></span> |
| <span data-ttu-id="0381d-121">propertyName</span><span class="sxs-lookup"><span data-stu-id="0381d-121">propertyName</span></span>     | <span data-ttu-id="0381d-122">Общедоступный.</span><span class="sxs-lookup"><span data-stu-id="0381d-122">Public.</span></span> <span data-ttu-id="0381d-123">Обязательный.</span><span class="sxs-lookup"><span data-stu-id="0381d-123">Required.</span></span> <span data-ttu-id="0381d-124">Каноническое имя связанного свойства.</span><span class="sxs-lookup"><span data-stu-id="0381d-124">The canonical name of the related property.</span></span>      |



 

## <a name="remarks"></a><span data-ttu-id="0381d-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0381d-125">Remarks</span></span>

<span data-ttu-id="0381d-126">Этот элемент позволяет сопоставлять одно свойство с другим.</span><span class="sxs-lookup"><span data-stu-id="0381d-126">This element enables you to map one property to another.</span></span> <span data-ttu-id="0381d-127">Например, можно сопоставлять текст пользовательского свойства, fabrikam. СторажекапаЦити, с System. Capacity:</span><span class="sxs-lookup"><span data-stu-id="0381d-127">For example, you can map the text of your custom property, Fabrikam.StorageCapacity, to System.Capacity:</span></span>


```
<!-- relatedPropertyInfo -->
<propertyDescription name="Fabrikam.StorageCapacity" ... >
    ...
    <relatedPropertyInfo>
        <relatedProperty relationshipName="System.RelatedProperty.Text" propertyName="System.Capacity"/>
    </relatedPropertyInfo>
</propertyDescription>
```



 

 
