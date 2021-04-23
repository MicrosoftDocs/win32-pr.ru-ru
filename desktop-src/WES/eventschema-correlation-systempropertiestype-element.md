---
title: Элемент Correlation (Системпропертиестипе)
description: Идентификаторы действий, которые потребители могут использовать для группирования связанных событий.
ms.assetid: 63982f37-3581-4b11-ac14-b95bc52541cb
keywords:
- Журнал событий элемента корреляции
topic_type:
- apiref
api_name:
- Correlation
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 91baca47479fe19988f3bfb23d573b8d92583d79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989104"
---
# <a name="correlation-systempropertiestype-element"></a><span data-ttu-id="a715d-104">Элемент Correlation (Системпропертиестипе)</span><span class="sxs-lookup"><span data-stu-id="a715d-104">Correlation (SystemPropertiesType) Element</span></span>

<span data-ttu-id="a715d-105">Идентификаторы действий, которые потребители могут использовать для группирования связанных событий.</span><span class="sxs-lookup"><span data-stu-id="a715d-105">The activity identifiers that consumers can use to group related events together.</span></span>

``` syntax
<xs:element name="Correlation">
    <xs:complexType>
        <xs:attribute name="ActivityID"
            type="GUIDType"
            use="optional"
         />
        <xs:attribute name="RelatedActivityID"
            type="GUIDType"
            use="optional"
         />
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="a715d-106">Элемент **Correlation** определяется сложным типом [**системпропертиестипе**](eventschema-systempropertiestype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a715d-106">The **Correlation** element is defined by the [**SystemPropertiesType**](eventschema-systempropertiestype-complextype.md) complex type.</span></span>

## <a name="attributes"></a><span data-ttu-id="a715d-107">Атрибуты</span><span class="sxs-lookup"><span data-stu-id="a715d-107">Attributes</span></span>



| <span data-ttu-id="a715d-108">Имя</span><span class="sxs-lookup"><span data-stu-id="a715d-108">Name</span></span>              | <span data-ttu-id="a715d-109">Тип</span><span class="sxs-lookup"><span data-stu-id="a715d-109">Type</span></span>                                                | <span data-ttu-id="a715d-110">Описание</span><span class="sxs-lookup"><span data-stu-id="a715d-110">Description</span></span>                                                                                                                                                                                  |
|-------------------|-----------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a715d-111">Идентификатор действия</span><span class="sxs-lookup"><span data-stu-id="a715d-111">ActivityID</span></span>        | [<span data-ttu-id="a715d-112">**гуидтипе**</span><span class="sxs-lookup"><span data-stu-id="a715d-112">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="a715d-113">Глобальный уникальный идентификатор, определяющий текущее действие.</span><span class="sxs-lookup"><span data-stu-id="a715d-113">A globally unique identifier that identifies the current activity.</span></span> <span data-ttu-id="a715d-114">События, опубликованные с помощью этого идентификатора, являются частью одного действия.</span><span class="sxs-lookup"><span data-stu-id="a715d-114">The events that are published with this identifier are part of the same activity.</span></span><br/>                              |
| <span data-ttu-id="a715d-115">RelatedActivityID</span><span class="sxs-lookup"><span data-stu-id="a715d-115">RelatedActivityID</span></span> | [<span data-ttu-id="a715d-116">**гуидтипе**</span><span class="sxs-lookup"><span data-stu-id="a715d-116">**GUIDType**</span></span>](eventschema-guidtype-simpletype.md) | <span data-ttu-id="a715d-117">Глобальный уникальный идентификатор, определяющий действие, в которое был передан элемент управления.</span><span class="sxs-lookup"><span data-stu-id="a715d-117">A globally unique identifier that identifies the activity to which control was transferred to.</span></span> <span data-ttu-id="a715d-118">Затем связанные события будут иметь этот идентификатор в качестве идентификатора ActivityID.</span><span class="sxs-lookup"><span data-stu-id="a715d-118">The related events would then have this identifier as their ActivityID identifier.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a715d-119">Требования</span><span class="sxs-lookup"><span data-stu-id="a715d-119">Requirements</span></span>



| <span data-ttu-id="a715d-120">Требование</span><span class="sxs-lookup"><span data-stu-id="a715d-120">Requirement</span></span> | <span data-ttu-id="a715d-121">Значение</span><span class="sxs-lookup"><span data-stu-id="a715d-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a715d-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a715d-122">Minimum supported client</span></span><br/> | <span data-ttu-id="a715d-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a715d-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a715d-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a715d-124">Minimum supported server</span></span><br/> | <span data-ttu-id="a715d-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a715d-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a715d-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a715d-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="a715d-127">**Родительский элемент**</span><span class="sxs-lookup"><span data-stu-id="a715d-127">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="a715d-128">**Система (EventType)**</span><span class="sxs-lookup"><span data-stu-id="a715d-128">**System (EventType)**</span></span>](eventschema-system-eventtype-element.md)
</dt> </dl>

 

 





