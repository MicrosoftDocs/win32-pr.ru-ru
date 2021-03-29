---
description: '<depth>Элемент указывает, должен ли диапазон соединителя поиска включать дочерние URL-адреса. Допустимые значения: глубокий и поверхностный. Этот элемент не имеет дочерних элементов и не имеет атрибутов.'
ms.assetid: 859decab-cbe3-4cec-b37c-6d0e7c353876
title: Элемент Depth (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bf68bcbc96b6d1beb2c381f0a17532272b8d397e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990967"
---
# <a name="depth-element-search-connector-schema"></a><span data-ttu-id="7d20f-105">Элемент Depth (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="7d20f-105">depth Element (Search Connector Schema)</span></span>

<span data-ttu-id="7d20f-106"><depth>Элемент указывает, должен ли диапазон соединителя поиска включать дочерние URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="7d20f-106">The <depth> element specifies whether the search connector's scope should include child URLs.</span></span> <span data-ttu-id="7d20f-107">Допустимые значения: `Deep` и `Shallow`.</span><span class="sxs-lookup"><span data-stu-id="7d20f-107">The allowed values are `Deep` and `Shallow`.</span></span> <span data-ttu-id="7d20f-108">Этот элемент не имеет дочерних элементов и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="7d20f-108">This element has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="7d20f-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="7d20f-109">Syntax</span></span>


```
<!-- depth -->
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
                                <xs:element name="depth" default="Shallow" minOccurs="0">
                                    <xs:simpleType>
                                        <xs:restriction base="xs:string">
                                            <xs:enumeration value="Shallow"/>
                                            <xs:enumeration value="Deep"/>
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



## <a name="element-information"></a><span data-ttu-id="7d20f-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="7d20f-110">Element Information</span></span>



| <span data-ttu-id="7d20f-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="7d20f-111">Parent Element</span></span>                                                                   | <span data-ttu-id="7d20f-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="7d20f-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="7d20f-113">Элемент Скопеитем (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="7d20f-113">scopeItem Element (Search Connector Schema)</span></span>](search-schema-sconn-scopeitem.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="7d20f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d20f-114">Remarks</span></span>

<span data-ttu-id="7d20f-115">Если глубина имеет глубину, пользователи могут просматривать или искать элементы на уровне URL-адреса Скопеитем или в любых дочерних URL-адресах.</span><span class="sxs-lookup"><span data-stu-id="7d20f-115">If the depth is deep, users can browse or search items in the scopeItem's URL level or within any child URLs.</span></span>

## <a name="example"></a><span data-ttu-id="7d20f-116">Пример</span><span class="sxs-lookup"><span data-stu-id="7d20f-116">Example</span></span>

<span data-ttu-id="7d20f-117">В следующем примере показана область поиска, включающая в себя C: \\ Folder а и все ее дочерние папки и C: \\ фолдерб, но не все ее дочерние папки.</span><span class="sxs-lookup"><span data-stu-id="7d20f-117">The following example shows a search scope that includes C:\\FolderA and all its child folders and C:\\FolderB but none of its child folders.</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <scope>
        <scopeItem>
            <mode>Include</mode>
            <depth>Deep</depth>
            <url>C:\FolderA</url>
        </scopeItem>
        <scopeItem>
            <mode>Include</mode>
            <depth>Shallow</depth>
            <url>C:\FolderB</url>
        </scopeItem>
    </scope>
    ...
</searchConnectionDescription>
```



 

 



