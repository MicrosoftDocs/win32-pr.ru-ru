---
description: Необязательный параметр <description> элемент задает описание для соединителя поиска. Этот элемент не имеет дочерних элементов и не имеет атрибутов.
ms.assetid: 0e9d806c-7dfd-4e7f-8843-15a4e22f317f
title: Элемент Description (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9d82fd6ad3ae45c4a8c3700c4822387a81880d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342922"
---
# <a name="description-element-search-connector-schema"></a><span data-ttu-id="dc24e-105">Элемент Description (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="dc24e-105">description Element (Search Connector Schema)</span></span>

<span data-ttu-id="dc24e-106">Необязательный параметр</span><span class="sxs-lookup"><span data-stu-id="dc24e-106">The optional</span></span> <description> <span data-ttu-id="dc24e-107">элемент задает описание для соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="dc24e-107">element specifies a description for this search connector.</span></span> <span data-ttu-id="dc24e-108">Этот элемент не имеет дочерних элементов и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="dc24e-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="dc24e-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="dc24e-109">Syntax</span></span>


```
<!-- description -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="description" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="dc24e-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="dc24e-110">Element Information</span></span>



| <span data-ttu-id="dc24e-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="dc24e-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="dc24e-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="dc24e-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="dc24e-113">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="dc24e-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="dc24e-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dc24e-114">Remarks</span></span>

<span data-ttu-id="dc24e-115">Описание должно быть понятным для пользователя, так как оно может использоваться во всплывающих подсказках.</span><span class="sxs-lookup"><span data-stu-id="dc24e-115">The description should be user-friendly as it may be used in tooltips.</span></span>

## <a name="example"></a><span data-ttu-id="dc24e-116">Пример</span><span class="sxs-lookup"><span data-stu-id="dc24e-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <description>Search AdventureWorks.com</description>
    ...
</searchConnectionDescription>
```



 

 



