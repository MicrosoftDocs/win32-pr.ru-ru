---
description: Элемент логического типа <isSearchOnlyItem> определяет, поддерживает ли поставщик поиска режим просмотра в дополнение к режиму поиска. Этот элемент является необязательным и не имеет дочерних элементов и атрибутов.
ms.assetid: eec1b735-ae78-48ef-8ebf-05b9fd038963
title: Элемент Иссеарчонлитем (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ded7b62cde5cf813603d5cc87c41fe2c443b42d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540631"
---
# <a name="issearchonlyitem-element-search-connector-schema"></a><span data-ttu-id="af56a-104">Элемент Иссеарчонлитем (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="af56a-104">isSearchOnlyItem Element (Search Connector Schema)</span></span>

<span data-ttu-id="af56a-105">Элемент логического типа <isSearchOnlyItem> определяет, поддерживает ли поставщик поиска режим просмотра в дополнение к режиму поиска.</span><span class="sxs-lookup"><span data-stu-id="af56a-105">The Boolean <isSearchOnlyItem> element specifies whether the search provider supports browse mode in addition to search mode.</span></span> <span data-ttu-id="af56a-106">Этот элемент является необязательным и не имеет дочерних элементов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="af56a-106">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="af56a-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="af56a-107">Syntax</span></span>


```
<!-- isSearchOnlyItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            <xs:element name="isSearchOnlyItem" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="af56a-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="af56a-108">Element Information</span></span>



| <span data-ttu-id="af56a-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="af56a-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="af56a-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="af56a-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="af56a-111">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="af56a-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="af56a-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="af56a-112">Remarks</span></span>

<span data-ttu-id="af56a-113">Значение `true` указывает, что пользователи не могут просматривать расположение соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="af56a-113">The value `true` indicates that the search connector location cannot be browsed by users.</span></span> <span data-ttu-id="af56a-114">Значение `false` указывает, что пользователи могут просматривать расположение соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="af56a-114">The value `false` indicates that users can browse the search connector location.</span></span>

## <a name="example"></a><span data-ttu-id="af56a-115">Пример</span><span class="sxs-lookup"><span data-stu-id="af56a-115">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <isSearchOnlyItem>true</isSearchOnlyItem>
    ...
</searchConnectionDescription>
```



 

 



