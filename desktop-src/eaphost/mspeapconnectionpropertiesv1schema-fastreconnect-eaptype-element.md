---
title: FastReconnect (Еаптипе), элемент
description: Сведения об элементе FastReconnect (Еаптипе). Этот элемент указывает, следует ли выполнять быстрое повторное подключение.
ms.assetid: 075285b0-7b1b-4d3c-af27-a718f3c20394
keywords:
- Элемент FastReconnect EAPHost
topic_type:
- apiref
api_name:
- FastReconnect
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2214519db68b8c95b0e0efa91d68a7cd667b5f87
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105691660"
---
# <a name="fastreconnect-eaptype-element"></a><span data-ttu-id="f35a1-105">FastReconnect (Еаптипе), элемент</span><span class="sxs-lookup"><span data-stu-id="f35a1-105">FastReconnect (EapType) Element</span></span>

<span data-ttu-id="f35a1-106">Элемент **FastReconnect (еаптипе)** указывает, нужно ли выполнять быстрое повторное подключение.</span><span class="sxs-lookup"><span data-stu-id="f35a1-106">The **FastReconnect (EapType)** element indicates whether to perform a fast reconnect.</span></span>

``` syntax
<xs:element name="FastReconnect"
    type="boolean"
 />
```

<span data-ttu-id="f35a1-107">Элемент **FastReconnect** определяется элементом [**еаптипе**](mspeapconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="f35a1-107">The **FastReconnect** element is defined by the [**EapType**](mspeapconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="f35a1-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f35a1-108">Remarks</span></span>

<span data-ttu-id="f35a1-109">Если элемент **FastReconnect** имеет значение true, то PEAP пытается выполнить быстрое повторное подключение. Если значение равно FALSE, PEAP выполняет полную проверку подлинности.</span><span class="sxs-lookup"><span data-stu-id="f35a1-109">If the **FastReconnect** element is TRUE, then PEAP attempts to perform a fast reconnect; if FALSE, PEAP performs the full authentication.</span></span> <span data-ttu-id="f35a1-110">Элемент **FastReconnect** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="f35a1-110">The **FastReconnect** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="f35a1-111">Требования</span><span class="sxs-lookup"><span data-stu-id="f35a1-111">Requirements</span></span>



| <span data-ttu-id="f35a1-112">Роль</span><span class="sxs-lookup"><span data-stu-id="f35a1-112">Role</span></span> | <span data-ttu-id="f35a1-113">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="f35a1-113">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="f35a1-114">Клиент</span><span class="sxs-lookup"><span data-stu-id="f35a1-114">Client</span></span><br/> | <span data-ttu-id="f35a1-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="f35a1-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f35a1-116">Сервер</span><span class="sxs-lookup"><span data-stu-id="f35a1-116">Server</span></span><br/> | <span data-ttu-id="f35a1-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="f35a1-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f35a1-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f35a1-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="f35a1-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="f35a1-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="f35a1-120">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="f35a1-120">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="f35a1-121">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="f35a1-121">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="f35a1-122">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="f35a1-122">**EapType**</span></span>](mspeapconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="f35a1-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="f35a1-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="f35a1-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="f35a1-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="f35a1-125">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f35a1-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="f35a1-126">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="f35a1-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





