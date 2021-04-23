---
description: Необязательный <imageLink> элемент указывает эскиз для этого соединителя поиска. Этот элемент имеет один обязательный дочерний элемент и не имеет атрибутов.
ms.assetid: 71078d83-72f4-41f9-b80c-7ba0139206fb
title: Элемент Имажелинк (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d84b2e5cbbfc8bbd98557ebd0405a09cf998e6ca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692174"
---
# <a name="imagelink-element-search-connector-schema"></a><span data-ttu-id="e9399-104">Элемент Имажелинк (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="e9399-104">imageLink Element (Search Connector Schema)</span></span>

<span data-ttu-id="e9399-105">Необязательный <imageLink> элемент указывает эскиз для этого соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="e9399-105">The optional <imageLink> element specifies a thumbnail for this search connector.</span></span> <span data-ttu-id="e9399-106">Этот элемент имеет один обязательный дочерний элемент и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="e9399-106">This element has one mandatory child element and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9399-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9399-107">Syntax</span></span>


```
<!-- imageLink -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="imageLink" minOccurs="0">
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="url" type="xs:anyURI"/>
                    </xs:sequence>
                </xs:complexType>
            </xs:element>            
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="e9399-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="e9399-108">Element Information</span></span>



| <span data-ttu-id="e9399-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="e9399-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="e9399-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e9399-110">Child Elements</span></span>                                                                           |
|------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e9399-111">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="e9399-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="e9399-112">Элемент URL-адреса Имажелинк (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="e9399-112">imageLink url Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink-url.md) |



 

## <a name="remarks"></a><span data-ttu-id="e9399-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9399-113">Remarks</span></span>

<span data-ttu-id="e9399-114">Значение Имажелинк может быть локальным путем файловой системы или URL-адресом.</span><span class="sxs-lookup"><span data-stu-id="e9399-114">The imageLink value can be a local file system path or a URL.</span></span> <span data-ttu-id="e9399-115">Файл образа может быть любым из базовых типов образов, поддерживаемых Windows 7 (PNG, BMP, JPG, GIF).</span><span class="sxs-lookup"><span data-stu-id="e9399-115">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelink-element"></a><span data-ttu-id="e9399-116">Пример элемента Имажелинк</span><span class="sxs-lookup"><span data-stu-id="e9399-116">Example of an imageLink Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



