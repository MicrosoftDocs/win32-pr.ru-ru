---
description: '<mode>Элемент указывает, следует ли включать или исключать URL-адрес из области соединителя поиска. Допустимые значения: include и Exclude. Этот элемент не имеет дочерних элементов и не имеет атрибутов.'
ms.assetid: 7654c04a-31c4-4260-a51c-0600804e62a9
title: Элемент Mode (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec8c09b4c6de138e6e390d2c31a82fe5d1f56566
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808896"
---
# <a name="mode-element-search-connector-schema"></a><span data-ttu-id="51250-105">Элемент Mode (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="51250-105">mode Element (Search Connector Schema)</span></span>

<span data-ttu-id="51250-106"><mode>Элемент указывает, следует ли включать или исключать URL-адрес из области соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="51250-106">The <mode> element specifies whether the URL should be included or excluded from the scope of the search connector.</span></span> <span data-ttu-id="51250-107">Допустимые значения: `Include` и `Exclude`.</span><span class="sxs-lookup"><span data-stu-id="51250-107">The allowed values are `Include` and `Exclude`.</span></span> <span data-ttu-id="51250-108">Этот элемент не имеет дочерних элементов и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="51250-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="51250-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="51250-109">Syntax</span></span>


```
<!-- mode -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
        ...
        <xs:element name="scope" minOccurs="0">
            <xs:complexType>
                <xs:sequence minOccurs="0">
                    <xs:element name="scopeItem" maxOccurs="unbounded">
                        <xs:complexType>
                            <xs:all>
                                ...
                                <xs:element name="mode" default="Include">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Include"/>
                                            <xs:enumeration value="Exclude"/>
                                        </xs:restriction>
                                    </xs:simpleType>
                                </xs:element>
                                ...
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



## <a name="element-information"></a><span data-ttu-id="51250-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="51250-110">Element Information</span></span>



| <span data-ttu-id="51250-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="51250-111">Parent Element</span></span>                                                                   | <span data-ttu-id="51250-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="51250-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="51250-113">Элемент Скопеитем (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="51250-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="51250-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51250-114">Remarks</span></span>

<span data-ttu-id="51250-115">Невозможно выполнить поиск или просмотр исключенной области.</span><span class="sxs-lookup"><span data-stu-id="51250-115">An excluded scope cannot be searched or browsed.</span></span> <span data-ttu-id="51250-116">URL-адреса Скопеитем можно вкладывать.</span><span class="sxs-lookup"><span data-stu-id="51250-116">You can nest scopeItem URLs.</span></span> <span data-ttu-id="51250-117">Например, можно включить родительскую область и все ее дочерние элементы, кроме одной, добавив родительский URL-адрес как включенный, со значением глубины Deep и исключая дочерний URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="51250-117">For example, you can include a parent scope and all its children except one by adding the parent URL as included, with depth value of Deep, and excluding the child URL.</span></span>

## <a name="example"></a><span data-ttu-id="51250-118">Пример</span><span class="sxs-lookup"><span data-stu-id="51250-118">Example</span></span>

<span data-ttu-id="51250-119">В следующем примере показана область поиска, включающая в себя C: \\ ексамплефолдер и все ее дочерние папки, кроме c: \\ ексамплефолдер \\ ексклудеме.</span><span class="sxs-lookup"><span data-stu-id="51250-119">The following example shows a search scope that includes C:\\ExampleFolder and all its child folders except C:\\ExampleFolder\\ExcludeMe.</span></span>


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
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\ExampleFolder\ExcludeMe</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



