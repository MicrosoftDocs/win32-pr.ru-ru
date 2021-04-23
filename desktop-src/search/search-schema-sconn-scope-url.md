---
description: <url>Элемент указывает URL-адрес, представляющий область соединителя поиска. Этот элемент не имеет дочерних элементов и не имеет атрибутов.
ms.assetid: 5afd84aa-98e3-4118-845a-d4efad19a488
title: Элемент URL-адреса Скопеитем (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c573308fe406fe4500f6bb8e88b3762fa0bbac05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896910"
---
# <a name="scopeitem-url-element-search-connector-schema"></a><span data-ttu-id="2cf88-104">Элемент URL-адреса Скопеитем (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="2cf88-104">scopeItem url Element (Search Connector Schema)</span></span>

<span data-ttu-id="2cf88-105"><url>Элемент указывает URL-адрес, представляющий область соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="2cf88-105">The <url> element specifies a URL that represents the scope of the search connector.</span></span> <span data-ttu-id="2cf88-106">Этот элемент не имеет дочерних элементов и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="2cf88-106">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="2cf88-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2cf88-107">Syntax</span></span>


```
<!-- url -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0"><xs:all>
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence></xs:all>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="2cf88-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="2cf88-108">Element Information</span></span>



| <span data-ttu-id="2cf88-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="2cf88-109">Parent Element</span></span>                                                                   | <span data-ttu-id="2cf88-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="2cf88-110">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="2cf88-111">Элемент Скопеитем (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="2cf88-111">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="2cf88-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2cf88-112">Remarks</span></span>

<span data-ttu-id="2cf88-113">Значением может быть путь к локальной файловой системе или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="2cf88-113">The value can be a local file system path or a URL.</span></span>

## <a name="example"></a><span data-ttu-id="2cf88-114">Пример</span><span class="sxs-lookup"><span data-stu-id="2cf88-114">Example</span></span>

<span data-ttu-id="2cf88-115">В следующем примере показана область поиска, включающая в себя C: \\ ексамплефолдер и все ее дочерние папки, кроме c: \\ ексамплефолдер \\ ексклудеме.</span><span class="sxs-lookup"><span data-stu-id="2cf88-115">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder</url>
        </scopeItem>
        <scopeItem>
            <mode>Exclude</mode>
            <depth>Deep</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



