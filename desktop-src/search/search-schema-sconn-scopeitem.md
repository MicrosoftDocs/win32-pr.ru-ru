---
description: <scopeItem>Элемент представляет отдельную запись в таблице область исключения/включения.
ms.assetid: 18a58b3b-771c-4829-b3d4-253383b4bee8
title: Элемент Скопеитем (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2033202be6d904880ec9c4efa1c60db4bb7e50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104144014"
---
# <a name="scopeitem-element-search-connector-schema"></a><span data-ttu-id="34ab8-103">Элемент Скопеитем (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="34ab8-103">scopeItem Element (Search Connector Schema)</span></span>

<span data-ttu-id="34ab8-104"><scopeItem>Элемент представляет отдельную запись в таблице область исключения/включения.</span><span class="sxs-lookup"><span data-stu-id="34ab8-104">The <scopeItem> element represents a single entry in the exclusion/inclusion scope table.</span></span> <span data-ttu-id="34ab8-105"><scopeItem> расширяет стандартный тип Шелллинктипе, добавляя три новых элемента, управляющих включением и исключением папок, контролируя глубину результатов и задающее расположение области.</span><span class="sxs-lookup"><span data-stu-id="34ab8-105"><scopeItem> extends the standard shellLinkType type by adding three new elements that control inclusion and exclusion of folders, control the depth of results, and specify the location of the scope.</span></span> <span data-ttu-id="34ab8-106">Если <scope> элемент существует, этот элемент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="34ab8-106">If the <scope> element exists, this element is required.</span></span> <span data-ttu-id="34ab8-107">Он имеет три дочерних элемента и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="34ab8-107">It has three child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="34ab8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="34ab8-108">Syntax</span></span>


```
<!-- scopeItem -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                <xs:element name="mode" default="Include">
                                    ...
                                </xs:element>
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    ...
                                </xs:element>
                                <xs:element name="url" type="xs:anyURI"/>
                            </xs:all>
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="34ab8-109">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="34ab8-109">Element Information</span></span>



| <span data-ttu-id="34ab8-110">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="34ab8-110">Parent Element</span></span>                                                           | <span data-ttu-id="34ab8-111">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="34ab8-111">Child Elements</span></span>                                                                        |
|--------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| [<span data-ttu-id="34ab8-112">Элемент Scope (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="34ab8-112">scope Element (Search Connector Schema)</span></span>](search-schema-sconn-scope.md) | <span data-ttu-id="34ab8-113">[элемент Scope (схема соединителя поиска)](search-schema-sconn-scope-mode.md).</span><span class="sxs-lookup"><span data-stu-id="34ab8-113">[scope Element (Search Connector Schema)](search-schema-sconn-scope-mode.md).</span></span>        |
|                                                                          | <span data-ttu-id="34ab8-114">[элемент Scope (схема соединителя поиска)](search-schema-sconn-scope-depth.md).</span><span class="sxs-lookup"><span data-stu-id="34ab8-114">[scope Element (Search Connector Schema)](search-schema-sconn-scope-depth.md).</span></span>       |
|                                                                          | <span data-ttu-id="34ab8-115">[элемент URL скопеитем (схема соединителя поиска)](search-schema-sconn-scope-url.md).</span><span class="sxs-lookup"><span data-stu-id="34ab8-115">[scopeItem url Element (Search Connector Schema)](search-schema-sconn-scope-url.md).</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="34ab8-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34ab8-116">Remarks</span></span>

<span data-ttu-id="34ab8-117">Используйте <scope> элементы и, <scopeItem> чтобы указать, какие расположения следует искать, и какие расположения следует исключить из поиска.</span><span class="sxs-lookup"><span data-stu-id="34ab8-117">Use the <scope> and <scopeItem> elements to identify which locations should be searched and which locations should be excluded from searching.</span></span>

## <a name="example"></a><span data-ttu-id="34ab8-118">Пример</span><span class="sxs-lookup"><span data-stu-id="34ab8-118">Example</span></span>

<span data-ttu-id="34ab8-119">В следующем примере показана область поиска, включающая в себя C: \\ ексамплефолдер и все ее дочерние папки, кроме c: \\ ексамплефолдер \\ ексклудеме.</span><span class="sxs-lookup"><span data-stu-id="34ab8-119">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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



 

 



