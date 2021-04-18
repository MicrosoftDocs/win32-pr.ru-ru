---
title: Кредентиалссаурце (Еаптипе), элемент
description: Сведения об элементе Кредентиалссаурце (Еаптипе). Этот элемент содержит сведения о расположении сертификата EAP-TLS.
ms.assetid: 6ef48e5e-7c71-472f-ab01-0a43a97ecd96
keywords:
- Элемент Кредентиалссаурце EAPHost
topic_type:
- apiref
api_name:
- CredentialsSource
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d68eccf44b7e2c248e366d8e3d8f05f4e7dd4774
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105700935"
---
# <a name="credentialssource-eaptype-element"></a><span data-ttu-id="9e2a2-105">Кредентиалссаурце (Еаптипе), элемент</span><span class="sxs-lookup"><span data-stu-id="9e2a2-105">CredentialsSource (EapType) Element</span></span>

<span data-ttu-id="9e2a2-106">Элемент **кредентиалссаурце (еаптипе)** содержит сведения о расположении сертификата EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="9e2a2-106">The **CredentialsSource (EapType)** element contains information about the location of the EAP-TLS certificate.</span></span>

``` syntax
<xs:element name="CredentialsSource"
    type="CredentialsSourceParameters"
 />
```

<span data-ttu-id="9e2a2-107">Элемент **кредентиалссаурце** определяется элементом [**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9e2a2-107">The **CredentialsSource** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e2a2-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9e2a2-108">Remarks</span></span>

<span data-ttu-id="9e2a2-109">Элемент **CredentialSource** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9e2a2-109">The **CredentialSource** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e2a2-110">Требования</span><span class="sxs-lookup"><span data-stu-id="9e2a2-110">Requirements</span></span>



| <span data-ttu-id="9e2a2-111">Роль</span><span class="sxs-lookup"><span data-stu-id="9e2a2-111">Role</span></span> | <span data-ttu-id="9e2a2-112">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="9e2a2-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="9e2a2-113">Клиент</span><span class="sxs-lookup"><span data-stu-id="9e2a2-113">Client</span></span><br/> | <span data-ttu-id="9e2a2-114">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9e2a2-114">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="9e2a2-115">Сервер</span><span class="sxs-lookup"><span data-stu-id="9e2a2-115">Server</span></span><br/> | <span data-ttu-id="9e2a2-116">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9e2a2-116">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9e2a2-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9e2a2-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="9e2a2-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="9e2a2-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9e2a2-119">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="9e2a2-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="9e2a2-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="9e2a2-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9e2a2-121">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="9e2a2-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="9e2a2-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="9e2a2-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="9e2a2-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="9e2a2-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="9e2a2-124">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="9e2a2-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="9e2a2-125">Элементы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="9e2a2-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





