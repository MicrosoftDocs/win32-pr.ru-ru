---
title: Binary (Евентдататипе), элемент
description: Двоичный BLOB-объект данных для событий, записываемых с помощью ведения журнала событий.
ms.assetid: aec2557f-6d63-48e7-b4d7-584e99dfcce3
keywords:
- Журнал событий двоичного элемента
topic_type:
- apiref
api_name:
- Binary
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: cdfd00e2d25f3178ab44081f76725b3189f1010b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071134"
---
# <a name="binary-eventdatatype-element"></a><span data-ttu-id="4394a-104">Binary (Евентдататипе), элемент</span><span class="sxs-lookup"><span data-stu-id="4394a-104">Binary (EventDataType) Element</span></span>

<span data-ttu-id="4394a-105">Двоичный BLOB-объект данных для событий, записываемых с помощью [ведения журнала событий](/windows/desktop/EventLog/event-logging).</span><span class="sxs-lookup"><span data-stu-id="4394a-105">A binary data blob for events that are written using [Event Logging](/windows/desktop/EventLog/event-logging).</span></span>

``` syntax
<xs:element name="Binary"
    type="hexBinary"
 />
```

<span data-ttu-id="4394a-106">Элемент **binary** определяется сложным типом [**евентдататипе**](eventschema-eventdatatype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="4394a-106">The **Binary** element is defined by the [**EventDataType**](eventschema-eventdatatype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="4394a-107">Требования</span><span class="sxs-lookup"><span data-stu-id="4394a-107">Requirements</span></span>



| <span data-ttu-id="4394a-108">Требование</span><span class="sxs-lookup"><span data-stu-id="4394a-108">Requirement</span></span> | <span data-ttu-id="4394a-109">Значение</span><span class="sxs-lookup"><span data-stu-id="4394a-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4394a-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4394a-110">Minimum supported client</span></span><br/> | <span data-ttu-id="4394a-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4394a-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4394a-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4394a-112">Minimum supported server</span></span><br/> | <span data-ttu-id="4394a-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4394a-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4394a-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4394a-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="4394a-115">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="4394a-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="4394a-116">**EventData (EventType)**</span><span class="sxs-lookup"><span data-stu-id="4394a-116">**EventData (EventType)**</span></span>](eventschema-eventdata-eventtype-element.md)
</dt> </dl>

 

