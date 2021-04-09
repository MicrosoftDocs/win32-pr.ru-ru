---
description: Необязательный логический <isIndexed> элемент указывает, индексируется ли расположение, описываемое соединителем поиска (локально или удаленно с помощью Windows Search 4 или более поздней версии).
ms.assetid: e72b5614-454c-481f-bc31-897d2dea8042
title: Элемент с индексом (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f658f6b932f6241b7af84e763d564ca0a8f1b5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144020"
---
# <a name="isindexed-element-search-connector-schema"></a><span data-ttu-id="24a12-103">Элемент с индексом (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="24a12-103">isIndexed Element (Search Connector Schema)</span></span>

<span data-ttu-id="24a12-104">Необязательный логический <isIndexed> элемент указывает, индексируется ли расположение, описываемое соединителем поиска (локально или удаленно с помощью Windows Search 4 или более поздней версии).</span><span class="sxs-lookup"><span data-stu-id="24a12-104">The optional Boolean <isIndexed> element specifies whether the location described by the search connector is indexed (either locally or remotely using Windows Search 4 or higher).</span></span> <span data-ttu-id="24a12-105">Значение по умолчанию — true для локальных папок.</span><span class="sxs-lookup"><span data-stu-id="24a12-105">The default value is true for local folders.</span></span> <span data-ttu-id="24a12-106">Этот элемент не имеет дочерних элементов и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="24a12-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="24a12-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="24a12-107">Syntax</span></span>


```
<!-- isIndexed -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="isIndexed" type="xsIboolean" minOccurs="0"/>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="24a12-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="24a12-108">Element Information</span></span>



| <span data-ttu-id="24a12-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="24a12-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="24a12-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="24a12-110">Child Elements</span></span> |
|------------------------------------------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="24a12-111">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="24a12-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) |                |



 

## <a name="example"></a><span data-ttu-id="24a12-112">Пример</span><span class="sxs-lookup"><span data-stu-id="24a12-112">Example</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="https://schemas.adventureworks.com/searchConnector">
    ...
    <isIndexed>false</isIndexed>
    ...
</searchConnectionDescription>
```



 

 



