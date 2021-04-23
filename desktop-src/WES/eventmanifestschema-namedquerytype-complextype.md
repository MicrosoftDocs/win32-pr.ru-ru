---
title: Сложный тип Намедкуеритипе
description: Не используется. Определяет список именованных запросов, которые запрашивают строку сообщения о событии для значения и выполняют указанное действие, если оно найдено. | Сложный тип Намедкуеритипе
ms.assetid: 2606094d-ae1b-4a3f-a78f-30659fa141ab
keywords:
- Журнал событий сложных типов Намедкуеритипе
topic_type:
- apiref
api_name:
- NamedQueryType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e296847cbed635d88f4fa58efa53fda030affffe
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105694031"
---
# <a name="namedquerytype-complex-type"></a><span data-ttu-id="97b9a-106">Сложный тип Намедкуеритипе</span><span class="sxs-lookup"><span data-stu-id="97b9a-106">NamedQueryType Complex Type</span></span>

<span data-ttu-id="97b9a-107">Не используется.</span><span class="sxs-lookup"><span data-stu-id="97b9a-107">Not used.</span></span> <span data-ttu-id="97b9a-108">Определяет список именованных запросов, которые запрашивают строку сообщения о событии для значения и выполняют указанное действие, если оно найдено.</span><span class="sxs-lookup"><span data-stu-id="97b9a-108">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span>

``` syntax
<xs:complexType name="NamedQueryType">
    <xs:sequence
        minOccurs="0"
    >
        <xs:element name="patternMaps"
            type="PatternMapListType"
         />
        <xs:any
            processContents="lax"
            maxOccurs="unbounded"
            minOccurs="0"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="97b9a-109">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="97b9a-109">Child elements</span></span>



| <span data-ttu-id="97b9a-110">Элемент</span><span class="sxs-lookup"><span data-stu-id="97b9a-110">Element</span></span>                                                                       | <span data-ttu-id="97b9a-111">Тип</span><span class="sxs-lookup"><span data-stu-id="97b9a-111">Type</span></span>                                                                             | <span data-ttu-id="97b9a-112">Описание</span><span class="sxs-lookup"><span data-stu-id="97b9a-112">Description</span></span>                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97b9a-113">**паттернмапс**</span><span class="sxs-lookup"><span data-stu-id="97b9a-113">**patternMaps**</span></span>](eventmanifestschema-patternmaps-namedquerytype-element.md) | [<span data-ttu-id="97b9a-114">**паттернмаплисттипе**</span><span class="sxs-lookup"><span data-stu-id="97b9a-114">**PatternMapListType**</span></span>](eventmanifestschema-patternmaplisttype-complextype.md) | <span data-ttu-id="97b9a-115">Определяет список пар регулярных выражений, которые используются для изменения строки сообщения.</span><span class="sxs-lookup"><span data-stu-id="97b9a-115">Defines a list of regular expression pairs that are used to alter the message string.</span></span><br/> |



## <a name="examples"></a><span data-ttu-id="97b9a-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="97b9a-116">Examples</span></span>

<span data-ttu-id="97b9a-117">В следующем примере показано, как использовать элемент [**намедкуериес**](eventmanifestschema-namedqueries-metadatatype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="97b9a-117">The following example shows how to use the [**namedQueries**](eventmanifestschema-namedqueries-metadatatype-element.md) element.</span></span> <span data-ttu-id="97b9a-118">Этот пример принимает содержимое строки сообщения и вставляет его в строку https://www .*мессажестринг*. com.</span><span class="sxs-lookup"><span data-stu-id="97b9a-118">This example takes the contents of the message string and inserts it into the string https://www.*messagestring*.com.</span></span> <span data-ttu-id="97b9a-119">Затем она заменяет строку сообщения на результат.</span><span class="sxs-lookup"><span data-stu-id="97b9a-119">It then replaces the message string with the result.</span></span> <span data-ttu-id="97b9a-120">Например, если строка сообщения содержит Microsoft, запрос заменит строку сообщения Майкрософт на https://www.Microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="97b9a-120">For example, if the message string contained Microsoft, the query would replace the Microsoft message string with https://www.Microsoft.com.</span></span>


```XML
<namedqueries>
   <patternmap name="SearchStrings" format="winrxv1">
       <map name="/${1}/" value="/http:\/\/www\.*\.com\/"/>
   </patternmap>
</namedqueries>
```



## <a name="requirements"></a><span data-ttu-id="97b9a-121">Требования</span><span class="sxs-lookup"><span data-stu-id="97b9a-121">Requirements</span></span>



| <span data-ttu-id="97b9a-122">Требование</span><span class="sxs-lookup"><span data-stu-id="97b9a-122">Requirement</span></span> | <span data-ttu-id="97b9a-123">Значение</span><span class="sxs-lookup"><span data-stu-id="97b9a-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="97b9a-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="97b9a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="97b9a-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="97b9a-125">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="97b9a-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="97b9a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="97b9a-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="97b9a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





