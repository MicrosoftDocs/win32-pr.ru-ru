---
title: Енаблекуарантинечеккс (Еаптипе), элемент
description: Сведения об элементе Енаблекуарантинечеккс (Еаптипе). Этот элемент указывает, следует ли выполнять проверки защиты доступа к сети (NAP).
ms.assetid: bd5c7efc-f857-4e21-9cd8-0a1cbe5a87d8
keywords:
- Элемент Енаблекуарантинечеккс EAPHost
topic_type:
- apiref
api_name:
- EnableQuarantineChecks
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0becd1add038bb91307095eaf5cd0743d383632b
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "103987902"
---
# <a name="enablequarantinechecks-eaptype-element"></a><span data-ttu-id="2ed22-105">Енаблекуарантинечеккс (Еаптипе), элемент</span><span class="sxs-lookup"><span data-stu-id="2ed22-105">EnableQuarantineChecks (EapType) Element</span></span>

<span data-ttu-id="2ed22-106">Элемент **енаблекуарантинечеккс (еаптипе)** указывает, следует ли выполнять проверки защиты доступа к сети (NAP).</span><span class="sxs-lookup"><span data-stu-id="2ed22-106">The **EnableQuarantineChecks (EapType)** element indicates whether to perform Network Access Protection (NAP) checks.</span></span>

``` syntax
<xs:element name="EnableQuarantineChecks"
    type="boolean"
 />
```

<span data-ttu-id="2ed22-107">Элемент **енаблекуарантинечеккс** определяется элементом [**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2ed22-107">The **EnableQuarantineChecks** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ed22-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2ed22-108">Remarks</span></span>

<span data-ttu-id="2ed22-109">Если элемент **енаблекуарантинечеккс** имеет значение true, PEAP ВЫПОЛНЯЕТ проверки NAP; Если значение равно FALSE, PEAP не будет выполнять проверки защиты доступа к сети.</span><span class="sxs-lookup"><span data-stu-id="2ed22-109">If the **EnableQuarantineChecks** element is TRUE, then PEAP will perform NAP checks; if FALSE, PEAP will not perform NAP checks.</span></span> <span data-ttu-id="2ed22-110">Элемент **енаблекуарантинечеккс** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="2ed22-110">The **EnableQuarantineChecks** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ed22-111">Требования</span><span class="sxs-lookup"><span data-stu-id="2ed22-111">Requirements</span></span>



| <span data-ttu-id="2ed22-112">Роль</span><span class="sxs-lookup"><span data-stu-id="2ed22-112">Role</span></span> | <span data-ttu-id="2ed22-113">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="2ed22-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="2ed22-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="2ed22-114">Client</span></span><br/> | <span data-ttu-id="2ed22-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2ed22-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2ed22-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="2ed22-116">Server</span></span><br/> | <span data-ttu-id="2ed22-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2ed22-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2ed22-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2ed22-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="2ed22-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="2ed22-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2ed22-120">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="2ed22-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="2ed22-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="2ed22-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2ed22-122">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="2ed22-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="2ed22-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="2ed22-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="2ed22-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="2ed22-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2ed22-125">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2ed22-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="2ed22-126">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2ed22-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





