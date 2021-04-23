---
description: Элемент логического типа <supportsAdvancedQuerySyntax> определяет, поддерживает ли поставщик поиска расширенный синтаксис запроса. Значение по умолчанию – false. Этот элемент является необязательным и не имеет дочерних элементов и атрибутов.
ms.assetid: d4aef1f1-63c8-4e9a-9e22-5efbb8c523b2
title: Элемент Суппортсадванцедкуерисинтакс (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39d31eb96615c952f703729fd9d22f2e5d27f38b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692165"
---
# <a name="supportsadvancedquerysyntax-element-search-connector-schema"></a><span data-ttu-id="8ab36-105">Элемент Суппортсадванцедкуерисинтакс (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="8ab36-105">supportsAdvancedQuerySyntax Element (Search Connector Schema)</span></span>

<span data-ttu-id="8ab36-106">Элемент логического типа <supportsAdvancedQuerySyntax> определяет, поддерживает ли поставщик поиска [Расширенный синтаксис запроса](-search-3x-advancedquerysyntax.md).</span><span class="sxs-lookup"><span data-stu-id="8ab36-106">The Boolean <supportsAdvancedQuerySyntax> element specifies whether the search provider supports the [Advanced Query Syntax](-search-3x-advancedquerysyntax.md).</span></span> <span data-ttu-id="8ab36-107">Значение по умолчанию – false.</span><span class="sxs-lookup"><span data-stu-id="8ab36-107">The default is false.</span></span> <span data-ttu-id="8ab36-108">Этот элемент является необязательным и не имеет дочерних элементов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="8ab36-108">This element is optional and has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ab36-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="8ab36-109">Syntax</span></span>


```
<!-- supportsAdvancedQuerySyntax -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="supportsAdvancedQuerySyntax" type="xs:boolean" default="false" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="8ab36-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="8ab36-110">Element Information</span></span>



| <span data-ttu-id="8ab36-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="8ab36-111">Parent Element</span></span>                                                                                                   | <span data-ttu-id="8ab36-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8ab36-112">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="8ab36-113">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="8ab36-113">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="8ab36-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8ab36-114">Remarks</span></span>

<span data-ttu-id="8ab36-115">Значение `true` указывает, что поставщик поиска поддерживает расширенный синтаксис запроса, отправленный в поисковых запросах.</span><span class="sxs-lookup"><span data-stu-id="8ab36-115">The value `true` indicates that the search provider supports Advanced Query Syntax sent in search queries.</span></span>

## <a name="example"></a><span data-ttu-id="8ab36-116">Пример</span><span class="sxs-lookup"><span data-stu-id="8ab36-116">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <supportsAdvancedQuerySyntax>true</supportsAdvancedQuerySyntax>
    ...
</searchConnectionDescription>
```



 

 



