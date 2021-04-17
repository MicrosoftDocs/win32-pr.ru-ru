---
title: Акцептсервернаме, элемент
description: Указывает, проверяется ли имя сервера на соответствие строке имени, указанной в элементе ServerName (Сервервалидатионпараметерс). | Акцептсервернаме, элемент
ms.assetid: 307b2d2a-1678-4aa9-82ed-46d401cf0e0f
keywords:
- Элемент Акцептсервернаме EAPHost
topic_type:
- apiref
api_name:
- AcceptServerName
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: b48c43bce2bd71f4d761ea58fcdf5e0632107f87
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105693982"
---
# <a name="acceptservername-element"></a><span data-ttu-id="899c6-105">Акцептсервернаме, элемент</span><span class="sxs-lookup"><span data-stu-id="899c6-105">AcceptServerName element</span></span>

<span data-ttu-id="899c6-106">Элемент **акцептсервернаме (еаптипе)** указывает, проверяется ли имя сервера на соответствие строке имени, указанной в элементе [**ServerName (сервервалидатионпараметерс)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="899c6-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element name="AcceptServerName"
    type="xs:boolean"
 />
```

<span data-ttu-id="899c6-107">Элемент **акцептсервернаме** определяется элементом [**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="899c6-107">The **AcceptServerName** element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="899c6-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="899c6-108">Remarks</span></span>

<span data-ttu-id="899c6-109">Элемент **акцептсервернаме** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="899c6-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="899c6-110">Требования</span><span class="sxs-lookup"><span data-stu-id="899c6-110">Requirements</span></span>



| <span data-ttu-id="899c6-111">Требование</span><span class="sxs-lookup"><span data-stu-id="899c6-111">Requirement</span></span> | <span data-ttu-id="899c6-112">Значение</span><span class="sxs-lookup"><span data-stu-id="899c6-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="899c6-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="899c6-113">Minimum supported client</span></span><br/> | <span data-ttu-id="899c6-114">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="899c6-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="899c6-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="899c6-115">Minimum supported server</span></span><br/> | <span data-ttu-id="899c6-116">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="899c6-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="899c6-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="899c6-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="899c6-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="899c6-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="899c6-119">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="899c6-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="899c6-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="899c6-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="899c6-121">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="899c6-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="899c6-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="899c6-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="899c6-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="899c6-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="899c6-124">eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="899c6-124">eaptlsconnectionpropertiesv2</span></span>](eaptlsconnectionpropertiesv2schema-schema.md)
</dt> <dt>

[<span data-ttu-id="899c6-125">Элементы схемы eaptlsconnectionpropertiesv2</span><span class="sxs-lookup"><span data-stu-id="899c6-125">eaptlsconnectionpropertiesv2 Schema Elements</span></span>](eaptlsconnectionpropertiesv2schema-elements.md)
</dt> <dt>

[<span data-ttu-id="899c6-126">**Акцептсервернаме (Еаптипе)**</span><span class="sxs-lookup"><span data-stu-id="899c6-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-tlsextensionstype-peapextensionstype-element.md)
</dt> </dl>

 

 





