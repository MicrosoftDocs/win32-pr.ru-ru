---
title: TimeCreated (Системпропертиестипе), элемент
description: Метка времени, определяющая время записи события в журнал.
ms.assetid: 16b2b71b-078e-4862-b1be-ef7cec315bc5
keywords:
- Журнал событий элемента TimeCreated
topic_type:
- apiref
api_name:
- TimeCreated
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 998bb03601f0ecbe87c571daa94b1f33e307d6af
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988841"
---
# <a name="timecreated-systempropertiestype-element"></a><span data-ttu-id="7324a-104">TimeCreated (Системпропертиестипе), элемент</span><span class="sxs-lookup"><span data-stu-id="7324a-104">TimeCreated (SystemPropertiesType) Element</span></span>

<span data-ttu-id="7324a-105">Метка времени, определяющая время записи события в журнал.</span><span class="sxs-lookup"><span data-stu-id="7324a-105">The time stamp that identifies when the event was logged.</span></span>

``` syntax
<xs:element name="TimeCreated">
    <xs:complexType>
        <xs:attribute name="SystemTime"
            type="dateTime"
            use="required"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="7324a-106">Элемент **TimeCreated** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="7324a-106">The **TimeCreated** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="7324a-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="7324a-107">Attributes</span></span>



| <span data-ttu-id="7324a-108">Имя</span><span class="sxs-lookup"><span data-stu-id="7324a-108">Name</span></span>       | <span data-ttu-id="7324a-109">Тип</span><span class="sxs-lookup"><span data-stu-id="7324a-109">Type</span></span>     | <span data-ttu-id="7324a-110">Описание</span><span class="sxs-lookup"><span data-stu-id="7324a-110">Description</span></span>                                              |
|------------|----------|----------------------------------------------------------|
| <span data-ttu-id="7324a-111">SystemTime</span><span class="sxs-lookup"><span data-stu-id="7324a-111">SystemTime</span></span> | <span data-ttu-id="7324a-112">dateTime</span><span class="sxs-lookup"><span data-stu-id="7324a-112">dateTime</span></span> | <span data-ttu-id="7324a-113">Системное время, когда событие было зарегистрировано.</span><span class="sxs-lookup"><span data-stu-id="7324a-113">The system time of when the event was logged.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="7324a-114">Требования</span><span class="sxs-lookup"><span data-stu-id="7324a-114">Requirements</span></span>



| <span data-ttu-id="7324a-115">Требование</span><span class="sxs-lookup"><span data-stu-id="7324a-115">Requirement</span></span> | <span data-ttu-id="7324a-116">Значение</span><span class="sxs-lookup"><span data-stu-id="7324a-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="7324a-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7324a-117">Minimum supported client</span></span><br/> | <span data-ttu-id="7324a-118">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="7324a-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="7324a-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7324a-119">Minimum supported server</span></span><br/> | <span data-ttu-id="7324a-120">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="7324a-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7324a-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7324a-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="7324a-122">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="7324a-122">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="7324a-123">**Система (EventType)**</span><span class="sxs-lookup"><span data-stu-id="7324a-123">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





