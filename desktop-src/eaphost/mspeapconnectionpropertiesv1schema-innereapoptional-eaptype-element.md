---
title: Иннереапоптионал (Еаптипе), элемент
description: Сведения об элементе Иннереапоптионал (Еаптипе). Этот элемент указывает, следует ли выполнять гостевой доступ.
ms.assetid: 2d314c89-5415-407f-84c3-c4c5c8957b39
keywords:
- Элемент Иннереапоптионал EAPHost
topic_type:
- apiref
api_name:
- InnerEapOptional
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be63845f389936656172b4cbb4e42de659bbf0e1
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "104134567"
---
# <a name="innereapoptional-eaptype-element"></a><span data-ttu-id="990cb-105">Иннереапоптионал (Еаптипе), элемент</span><span class="sxs-lookup"><span data-stu-id="990cb-105">InnerEapOptional (EapType) Element</span></span>

<span data-ttu-id="990cb-106">Элемент **иннереапоптионал (еаптипе)** указывает, следует ли выполнять гостевой доступ.</span><span class="sxs-lookup"><span data-stu-id="990cb-106">The **InnerEapOptional (EapType)** element indicates whether to perform GUEST access.</span></span>

``` syntax
<xs:element name="InnerEapOptional"
    type="boolean"
 />
```

<span data-ttu-id="990cb-107">Элемент **иннереапоптионал** определяется элементом [**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="990cb-107">The **InnerEapOptional** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="990cb-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="990cb-108">Remarks</span></span>

<span data-ttu-id="990cb-109">Если элемент **иннереапоптионал** имеет значение true, то должен присутствовать элемент [**EAP**](baseeapconnectionpropertiesv1schema-eap-element.md) , описывающий внутренний метод и его конфигурацию. Если задано значение FALSE, PEAP выполняет гостевой доступ.</span><span class="sxs-lookup"><span data-stu-id="990cb-109">If the **InnerEapOptional** element is TRUE, then the [**Eap**](baseeapconnectionpropertiesv1schema-eap-element.md) element must be present and describe the inner method and it's configuration; if FALSE, then PEAP will perform GUEST access.</span></span> <span data-ttu-id="990cb-110">Элемент **иннереапоптионал** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="990cb-110">The **InnerEapOptional** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="990cb-111">Требования</span><span class="sxs-lookup"><span data-stu-id="990cb-111">Requirements</span></span>



| <span data-ttu-id="990cb-112">Роль</span><span class="sxs-lookup"><span data-stu-id="990cb-112">Role</span></span> | <span data-ttu-id="990cb-113">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="990cb-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="990cb-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="990cb-114">Client</span></span><br/> | <span data-ttu-id="990cb-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="990cb-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="990cb-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="990cb-116">Server</span></span><br/> | <span data-ttu-id="990cb-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="990cb-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="990cb-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="990cb-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="990cb-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="990cb-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="990cb-120">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="990cb-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="990cb-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="990cb-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="990cb-122">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="990cb-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="990cb-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="990cb-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="990cb-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="990cb-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="990cb-125">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="990cb-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="990cb-126">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="990cb-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





