---
title: Дифферентусернаме (Еаптипе), элемент
description: Сведения об элементе Дифферентусернаме (Еаптипе). Этот элемент определяет, какое имя пользователя использует EAP-TLS.
ms.assetid: f0ce41a9-c774-4d12-8a5a-a8eb1eb84cb0
keywords:
- Элемент Дифферентусернаме EAPHost
topic_type:
- apiref
api_name:
- DifferentUsername
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 505e23c74d4c1c8c74a50906809d0acc9ce06c42
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105700931"
---
# <a name="differentusername-eaptype-element"></a><span data-ttu-id="4db97-105">Дифферентусернаме (Еаптипе), элемент</span><span class="sxs-lookup"><span data-stu-id="4db97-105">DifferentUsername (EapType) Element</span></span>

<span data-ttu-id="4db97-106">Элемент **дифферентусернаме (еаптипе)** определяет, какое имя пользователя использует EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="4db97-106">The **DifferentUsername (EapType)** element determines which user name EAP-TLS is to use.</span></span>

``` syntax
<xs:element name="DifferentUsername"
    type="boolean"
 />
```

<span data-ttu-id="4db97-107">Элемент **дифферентусернаме** определяется элементом [**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="4db97-107">The **DifferentUsername** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="4db97-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4db97-108">Remarks</span></span>

<span data-ttu-id="4db97-109">Если элемент **дифферентусернаме** имеет значение true, то EAP-TLS должен использовать имя пользователя, отличное от имени, которое отображается в сертификате.</span><span class="sxs-lookup"><span data-stu-id="4db97-109">If the **DifferentUserName** element is TRUE, EAP-TLS should use a user name other than the name that appears on the certificate.</span></span> <span data-ttu-id="4db97-110">Если элемент **дифферентусернаме** имеет значение false, то EAP-TLS использует имя пользователя, которое отображается в сертификате.</span><span class="sxs-lookup"><span data-stu-id="4db97-110">If the **DifferentUserName** element is FALSE, EAP-TLS uses the user name that appears on the certificate.</span></span>

<span data-ttu-id="4db97-111">Элемент **дифферентусернаме** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="4db97-111">The **DifferentUserName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="4db97-112">Требования</span><span class="sxs-lookup"><span data-stu-id="4db97-112">Requirements</span></span>



| <span data-ttu-id="4db97-113">Роль</span><span class="sxs-lookup"><span data-stu-id="4db97-113">Role</span></span> | <span data-ttu-id="4db97-114">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="4db97-114">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="4db97-115">Клиент</span><span class="sxs-lookup"><span data-stu-id="4db97-115">Client</span></span><br/> | <span data-ttu-id="4db97-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="4db97-116">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4db97-117">Сервер</span><span class="sxs-lookup"><span data-stu-id="4db97-117">Server</span></span><br/> | <span data-ttu-id="4db97-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="4db97-118">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4db97-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4db97-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="4db97-120">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="4db97-120">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4db97-121">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="4db97-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="4db97-122">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="4db97-122">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4db97-123">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="4db97-123">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="4db97-124"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="4db97-124"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="4db97-125">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="4db97-125">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="4db97-126">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="4db97-126">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="4db97-127">Элементы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="4db97-127">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





