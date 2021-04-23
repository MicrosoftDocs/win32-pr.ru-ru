---
description: <simpleLocation>Элемент указывает расположение соединителей поиска, основанных на файловой системе или обработчике протоколов. Этот элемент имеет два дочерних элемента и не имеет атрибутов.
ms.assetid: 04ffc178-0a76-4870-a075-a2ecd31937a1
title: Элемент Симплелокатион (схема соединителя поиска)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d12c17ace36314ceb180f14b6de0eb7a890a385b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342902"
---
# <a name="simplelocation-element-search-connector-schema"></a><span data-ttu-id="444cf-104">Элемент Симплелокатион (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="444cf-104">simpleLocation Element (Search Connector Schema)</span></span>

<span data-ttu-id="444cf-105"><simpleLocation>Элемент указывает расположение соединителей поиска, основанных на файловой системе или обработчике протоколов.</span><span class="sxs-lookup"><span data-stu-id="444cf-105">The <simpleLocation> element specifies the location for search connectors that are file-system based or protocol-handler based.</span></span> <span data-ttu-id="444cf-106">Этот элемент имеет два дочерних элемента и не имеет атрибутов.</span><span class="sxs-lookup"><span data-stu-id="444cf-106">This element has two child elements and no attributes.</span></span>

## <a name="syntax"></a><span data-ttu-id="444cf-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="444cf-107">Syntax</span></span>


```
<!-- simpleLocation -->
    <xs:complexType name="searchConnectorDescriptionType">
        <xs:all>
            ...
            <xs:element name="simpleLocation" type="shellLinkType" minOccurs="0">
                <xs:all>
                    <xs:element name="url" type="xs:anyURI"/>
                    <xs:element name="serialized" minOccurs="0"/>
                </xs:all>
                
            </xs:element>
            ...
        </xs:all>
        <xs:attribute name="publisher" type="xs:string"/>
        <xs:attribute name="product" type="xs:string"/>
    </xs:complexType>
```



## <a name="element-information"></a><span data-ttu-id="444cf-108">Сведения об элементе</span><span class="sxs-lookup"><span data-stu-id="444cf-108">Element Information</span></span>



| <span data-ttu-id="444cf-109">Родительский элемент</span><span class="sxs-lookup"><span data-stu-id="444cf-109">Parent Element</span></span>                                                                                                   | <span data-ttu-id="444cf-110">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="444cf-110">Child Elements</span></span>                                                                                                                                                                                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="444cf-111">Элемент Сеарчконнектордескриптионтипе (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="444cf-111">searchConnectorDescriptionType Element (Search Connector Schema)</span></span>](search-schema-searchconnectordescription.md) | [<span data-ttu-id="444cf-112">Элемент URL-адреса Симплелокатион (схема соединителя поиска)</span><span class="sxs-lookup"><span data-stu-id="444cf-112">simpleLocation url Element (Search Connector Schema)</span></span>](search-schema-sconn-url.md)                                                                                                                                                                                                                                |
|                                                                                                                  | <span data-ttu-id="444cf-113">сериализовано: этот элемент содержит Шелллинк в кодировке Base64, указывающий на расположение, определенное в <url> элементе.</span><span class="sxs-lookup"><span data-stu-id="444cf-113">serialized: This element contains the base64-encoded ShellLink pointing to the location defined in the <url> element.</span></span> <span data-ttu-id="444cf-114">Windows 7 создает Шелллинк из значения <url> элемента и соответствующим образом обновляет это поле при первой загрузке этой библиотеки, поэтому автор должен оставить его пустым.</span><span class="sxs-lookup"><span data-stu-id="444cf-114">Windows 7 creates the ShellLink from the value of the <url> element and properly updates this field on the first load of this library, so it should be left empty by the author.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="444cf-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="444cf-115">Remarks</span></span>

<span data-ttu-id="444cf-116">Этот элемент можно использовать вместо, <locationProvider> Если расположение находится в файловой системе или если соединитель является известным обработчиком протокола (например, MAPI:).</span><span class="sxs-lookup"><span data-stu-id="444cf-116">This element can be used instead of <locationProvider> when the location is on the file system or the connector is a known protocol handler (like mapi:).</span></span> <span data-ttu-id="444cf-117">Если <simpleLocation> присутствует, то не должен быть <locationProvider> элементом.</span><span class="sxs-lookup"><span data-stu-id="444cf-117">If <simpleLocation> is present, there MUST NOT be a <locationProvider> element.</span></span> <span data-ttu-id="444cf-118">Для соединителей поиска поставщика веб-служб используйте [<locationProvider>](search-schema-sconn-locationprovider.md) элемент.</span><span class="sxs-lookup"><span data-stu-id="444cf-118">For web service provider search connectors, use the [<locationProvider>](search-schema-sconn-locationprovider.md) element instead.</span></span>

## <a name="examples"></a><span data-ttu-id="444cf-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="444cf-119">Examples</span></span>


```
<?xml version="1.0" encoding="UTF-8"?>
<searchConnectorDescription xmlns="http://schemas.microsoft.com/windows/2009/searchConnector">
    ...
    <simpleLocation>
        <url>mapi://{S-1-5-21-2127521184-1604012920-1887927527-2779359}/</url>
    </simpleLocation>
    ...
</searchConnectionDescription>
```



 

 



