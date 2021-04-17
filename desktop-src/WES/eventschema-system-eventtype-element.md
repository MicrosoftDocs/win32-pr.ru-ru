---
title: Элемент System (EventType)
description: Содержит сведения, определяющие поставщик и способ его включения, событие, канал, на который было написано событие, а также системные сведения, такие как идентификатор процесса и потока.
ms.assetid: c532cfa3-b722-4227-a403-5c050d62a92c
keywords:
- Журнал событий системного элемента
topic_type:
- apiref
api_name:
- System
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4fef0f9f9e24a855564a8d3df2f94610ff9a8248
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105691770"
---
# <a name="system-eventtype-element"></a><span data-ttu-id="75c81-104">Элемент System (EventType)</span><span class="sxs-lookup"><span data-stu-id="75c81-104">System (EventType) Element</span></span>

<span data-ttu-id="75c81-105">Содержит сведения, определяющие поставщик и способ его включения, событие, канал, на который было написано событие, а также системные сведения, такие как идентификатор процесса и потока.</span><span class="sxs-lookup"><span data-stu-id="75c81-105">Contains information that identifies the provider and how it was enabled, the event, the channel to which the event was written, and system information such as the process and thread IDs.</span></span>

``` syntax
<xs:element name="System"
    type="SystemPropertiesType"
 />
```

<span data-ttu-id="75c81-106">Элемент **System** определяется сложным типом [**EventType**](eventschema-eventtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="75c81-106">The **System** element is defined by the [**EventType**](eventschema-eventtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="75c81-107">Требования</span><span class="sxs-lookup"><span data-stu-id="75c81-107">Requirements</span></span>



| <span data-ttu-id="75c81-108">Требование</span><span class="sxs-lookup"><span data-stu-id="75c81-108">Requirement</span></span> | <span data-ttu-id="75c81-109">Значение</span><span class="sxs-lookup"><span data-stu-id="75c81-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="75c81-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="75c81-110">Minimum supported client</span></span><br/> | <span data-ttu-id="75c81-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="75c81-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="75c81-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="75c81-112">Minimum supported server</span></span><br/> | <span data-ttu-id="75c81-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="75c81-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75c81-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="75c81-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="75c81-115">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="75c81-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="75c81-116">**Журнале**</span><span class="sxs-lookup"><span data-stu-id="75c81-116">**Event**</span></span>](eventschema-event-element.md)
</dt> </dl>

 

 





