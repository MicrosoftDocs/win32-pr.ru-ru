---
title: Тлсекстенсионс (схема v1)
description: Сведения об элементе Тлсекстенсионс (Еаптипе). Этот элемент обеспечивает будущие улучшения схемы.
ms.assetid: f968d91d-e226-44a9-98db-347cbedfa201
keywords:
- элемент EAPHost
topic_type:
- apiref
api_name:
- TLSExtensions
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 886f1ab2a6f00a4a8a9d530fa41865b2fd0cf0b8
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/21/2020
ms.locfileid: "105672419"
---
# <a name="tlsextensions-v1-schema"></a><span data-ttu-id="2557a-105">Тлсекстенсионс (схема v1)</span><span class="sxs-lookup"><span data-stu-id="2557a-105">TLSExtensions (v1 schema)</span></span>

<span data-ttu-id="2557a-106">Элемент **тлсекстенсионс (еаптипе)** обеспечивает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="2557a-106">The **TLSExtensions (EapType)** element enables future enhancements to the schema.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: TLSExtensions"
 />
```

<span data-ttu-id="2557a-107">Элемент определяется элементом [**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="2557a-107">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="2557a-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2557a-108">Remarks</span></span>

<span data-ttu-id="2557a-109">Элемент **тлсекстенсионс** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="2557a-109">The **TLSExtensions** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="2557a-110">Требования</span><span class="sxs-lookup"><span data-stu-id="2557a-110">Requirements</span></span>



| <span data-ttu-id="2557a-111">Роль</span><span class="sxs-lookup"><span data-stu-id="2557a-111">Role</span></span> | <span data-ttu-id="2557a-112">Минимальная поддерживаемая версия ОС</span><span class="sxs-lookup"><span data-stu-id="2557a-112">Minimum supported OS version</span></span> |
|------|------------------------------|
| <span data-ttu-id="2557a-113">Клиент</span><span class="sxs-lookup"><span data-stu-id="2557a-113">Client</span></span><br/> | <span data-ttu-id="2557a-114">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="2557a-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="2557a-115">Сервер</span><span class="sxs-lookup"><span data-stu-id="2557a-115">Server</span></span><br/> | <span data-ttu-id="2557a-116">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="2557a-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2557a-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2557a-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="2557a-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="2557a-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="2557a-119">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="2557a-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="2557a-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="2557a-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="2557a-121">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="2557a-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="2557a-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="2557a-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="2557a-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="2557a-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="2557a-124">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2557a-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="2557a-125">Элементы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="2557a-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="2557a-126">**Тлсекстенсионс (Тлсекстенсионстипе)**</span><span class="sxs-lookup"><span data-stu-id="2557a-126">**TLSExtensions (TLSExtensionsType)**</span></span>](eaptlsconnectionpropertiesv2schema-performservervalidation-eaptype-element.md)
</dt> </dl>

 

 





