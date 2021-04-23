---
title: Сложный тип Паттернмаплисттипе
description: Не используется. Определяет список пар регулярных выражений, которые используются для изменения строки сообщения.
ms.assetid: f7b92821-a959-4b91-9e7e-47d0136ee61f
keywords:
- Журнал событий сложных типов Паттернмаплисттипе
topic_type:
- apiref
api_name:
- PatternMapListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5d1bb655dcf13c70fb989756cb9f5716301934c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340305"
---
# <a name="patternmaplisttype-complex-type"></a><span data-ttu-id="bbfd2-105">Сложный тип Паттернмаплисттипе</span><span class="sxs-lookup"><span data-stu-id="bbfd2-105">PatternMapListType Complex Type</span></span>

<span data-ttu-id="bbfd2-106">Не используется.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-106">Not used.</span></span> <span data-ttu-id="bbfd2-107">Определяет список пар регулярных выражений, которые используются для изменения строки сообщения.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-107">Defines a list of regular expression pairs that are used to alter the message string.</span></span>

``` syntax
<xs:complexType name="PatternMapListType">
    <xs:sequence>
        <xs:element name="patternMap"
            type="PatternMapType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="bbfd2-108">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="bbfd2-108">Child elements</span></span>



| <span data-ttu-id="bbfd2-109">Элемент</span><span class="sxs-lookup"><span data-stu-id="bbfd2-109">Element</span></span>                                                                         | <span data-ttu-id="bbfd2-110">Тип</span><span class="sxs-lookup"><span data-stu-id="bbfd2-110">Type</span></span>                                                                     | <span data-ttu-id="bbfd2-111">Описание</span><span class="sxs-lookup"><span data-stu-id="bbfd2-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bbfd2-112">**паттернмап**</span><span class="sxs-lookup"><span data-stu-id="bbfd2-112">**patternMap**</span></span>](eventmanifestschema-patternmap-patternmaplisttype-element.md) | [<span data-ttu-id="bbfd2-113">**паттернмаптипе**</span><span class="sxs-lookup"><span data-stu-id="bbfd2-113">**PatternMapType**</span></span>](eventmanifestschema-patternmaptype-complextype.md) | <span data-ttu-id="bbfd2-114">Определяет сопоставление между двумя регулярными выражениями.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-114">Defines a mapping between two regular expressions.</span></span> <span data-ttu-id="bbfd2-115">Одно выражение используется для поиска соответствующей строки в строке сообщения, а другая — для изменения строки перед тем, как служба снова поместит ее в строку сообщения.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-115">One expression is used to find a matching string in the message string and the other is used to alter the string before the service places it back in the message string.</span></span> <span data-ttu-id="bbfd2-116">Используется первое сопоставление шаблонов, которое соответствует, и другие шаблоны не используются.</span><span class="sxs-lookup"><span data-stu-id="bbfd2-116">The first pattern mapping that matches is used and other patterns are not tried.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bbfd2-117">Требования</span><span class="sxs-lookup"><span data-stu-id="bbfd2-117">Requirements</span></span>



| <span data-ttu-id="bbfd2-118">Требование</span><span class="sxs-lookup"><span data-stu-id="bbfd2-118">Requirement</span></span> | <span data-ttu-id="bbfd2-119">Значение</span><span class="sxs-lookup"><span data-stu-id="bbfd2-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bbfd2-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="bbfd2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bbfd2-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="bbfd2-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bbfd2-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="bbfd2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bbfd2-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="bbfd2-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





