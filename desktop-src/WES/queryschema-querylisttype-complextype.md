---
title: Сложный тип Куерилисттипе
description: Определяет список запросов, которые могут содержать набор селекторов и подавления, которые используются для включения или исключения событий из результирующего набора.
ms.assetid: 3b9944e8-5913-4a77-a8fd-7efa43f3063f
keywords:
- Журнал событий сложных типов Куерилисттипе
topic_type:
- apiref
api_name:
- QueryListType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58cc6e83fb681f6244288088ea217097dd109c23
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691822"
---
# <a name="querylisttype-complex-type"></a><span data-ttu-id="5c7f0-104">Сложный тип Куерилисттипе</span><span class="sxs-lookup"><span data-stu-id="5c7f0-104">QueryListType Complex Type</span></span>

<span data-ttu-id="5c7f0-105">Определяет список запросов, которые могут содержать набор селекторов и подавления, которые используются для включения или исключения событий из результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="5c7f0-105">Defines a list of queries that can contain a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span>

``` syntax
<xs:complexType name="QueryListType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:element name="Query"
            type="QueryType"
         />
    </xs:sequence>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="5c7f0-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="5c7f0-106">Child elements</span></span>



| <span data-ttu-id="5c7f0-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="5c7f0-107">Element</span></span>                                                  | <span data-ttu-id="5c7f0-108">Тип</span><span class="sxs-lookup"><span data-stu-id="5c7f0-108">Type</span></span>                                                   | <span data-ttu-id="5c7f0-109">Описание</span><span class="sxs-lookup"><span data-stu-id="5c7f0-109">Description</span></span>                                                                                                                     |
|----------------------------------------------------------|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5c7f0-110">**Запрос**</span><span class="sxs-lookup"><span data-stu-id="5c7f0-110">**Query**</span></span>](queryschema-query-querylisttype-element.md) | [<span data-ttu-id="5c7f0-111">**QueryType**</span><span class="sxs-lookup"><span data-stu-id="5c7f0-111">**QueryType**</span></span>](queryschema-querytype-complextype.md) | <span data-ttu-id="5c7f0-112">Определяет набор селекторов и подавления, которые используются для включения или исключения событий из результирующего набора.</span><span class="sxs-lookup"><span data-stu-id="5c7f0-112">Defines a set of selectors and suppressors that are used to include events in or exclude events from the result set.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="5c7f0-113">Требования</span><span class="sxs-lookup"><span data-stu-id="5c7f0-113">Requirements</span></span>



| <span data-ttu-id="5c7f0-114">Требование</span><span class="sxs-lookup"><span data-stu-id="5c7f0-114">Requirement</span></span> | <span data-ttu-id="5c7f0-115">Значение</span><span class="sxs-lookup"><span data-stu-id="5c7f0-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5c7f0-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="5c7f0-116">Minimum supported client</span></span><br/> | <span data-ttu-id="5c7f0-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="5c7f0-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5c7f0-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="5c7f0-118">Minimum supported server</span></span><br/> | <span data-ttu-id="5c7f0-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="5c7f0-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





