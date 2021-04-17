---
description: Необязательный <author> элемент указывает автора библиотеки. Этот элемент не имеет дочерних элементов и не имеет атрибутов.
ms.assetid: c91042d5-9564-463a-9104-97b927027fc9
title: Элемент Author (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74a2facbf4e3fa743b4dbe56a1c83eb57509c067
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105710901"
---
# <a name="author-element-search-connector-schema"></a><span data-ttu-id="f938f-104">Элемент Author (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="f938f-104">author Element (Search Connector Schema)</span></span>

<span data-ttu-id="f938f-105">Необязательный <author> элемент указывает автора библиотеки.</span><span class="sxs-lookup"><span data-stu-id="f938f-105">The optional <author> element specifies the author of this library.</span></span> <span data-ttu-id="f938f-106">Этот элемент не имеет дочерних элементов и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="f938f-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="f938f-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f938f-107">Syntax</span></span>


```
<!-- author -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="author" type="xs:string" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="f938f-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="f938f-108">Element Information</span></span>



| <span data-ttu-id="f938f-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="f938f-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="f938f-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="f938f-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="f938f-111">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="f938f-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="f938f-112">Пример</span><span class="sxs-lookup"><span data-stu-id="f938f-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <author>Joe Smith</author>
    ...
</searchConnectionDescription>
```



 

 



