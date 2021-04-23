---
description: <url>Элемент указывает URL-адрес эскиза для соединителя поиска. Если <imageLink> существует, этот элемент является обязательным. У него нет дочерних элементов и атрибутов.
ms.assetid: addb2614-9f4f-4cab-a678-b6020b8c4648
title: Элемент URL-адреса Имажелинк (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c97daaafcbf6336dd4d88c3c92315e656d137b1f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692175"
---
# <a name="imagelink-url-element-search-connector-schema"></a><span data-ttu-id="a5ddf-105">Элемент URL-адреса Имажелинк (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="a5ddf-105">imageLink url Element (Search Connector Schema)</span></span>

<span data-ttu-id="a5ddf-106"><url>Элемент указывает URL-адрес эскиза для соединителя поиска.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-106">The <url> element specifies a URL to the thumbnail for this search connector.</span></span> <span data-ttu-id="a5ddf-107">Если <imageLink> существует, этот элемент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-107">If <imageLink> exists, this element is required.</span></span> <span data-ttu-id="a5ddf-108">У него нет дочерних элементов и атрибутов.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-108">It has no child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5ddf-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a5ddf-109">Syntax</span></span>


```
<!-- url -->
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



## <a name="element-information"></a><span data-ttu-id="a5ddf-110">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="a5ddf-110">Element Information</span></span>



| <span data-ttu-id="a5ddf-111">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="a5ddf-111">Parent Element</span></span>                                                                   | <span data-ttu-id="a5ddf-112">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="a5ddf-112">Child Elements</span></span> |
|----------------------------------------------------------------------------------|----------------|
| [<span data-ttu-id="a5ddf-113">Элемент Имажелинк (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="a5ddf-113">imageLink Element (Search Connector Schema)</span></span>](search-schema-sconn-imagelink.md) |                |



 

## <a name="remarks"></a><span data-ttu-id="a5ddf-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a5ddf-114">Remarks</span></span>

<span data-ttu-id="a5ddf-115">Значением может быть путь к локальной файловой системе или URL-адрес.</span><span class="sxs-lookup"><span data-stu-id="a5ddf-115">The value can be a local file system path or a URL.</span></span> <span data-ttu-id="a5ddf-116">Файл образа может быть любым из базовых типов образов, поддерживаемых Windows 7 (PNG, BMP, JPG, GIF).</span><span class="sxs-lookup"><span data-stu-id="a5ddf-116">The image file can be any of the basic image types supported by Windows 7 (PNG, BMP, JPG, GIF).</span></span>

## <a name="example-of-an-imagelinkurl-element"></a><span data-ttu-id="a5ddf-117">Пример элемента Имажелинкурл</span><span class="sxs-lookup"><span data-stu-id="a5ddf-117">Example of an imageLinkurl Element</span></span>


```
<imageLink>
    <imageLinkurl>%ProgramFiles%\Example\examplethumbnail.jpg</imageLinkurl>
</imageLink>
```



 

 



