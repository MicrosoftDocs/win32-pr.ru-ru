---
title: акцептсервернаме
description: Указывает, проверяется ли имя сервера на соответствие строке имени, указанной в элементе ServerName (Сервервалидатионпараметерс). | акцептсервернаме
ms.assetid: 440a46ae-7fef-4e97-9fd7-cbd20143597b
keywords:
- элемент EAPHost
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
ms.openlocfilehash: beb12da9897cc0e77480f609edee632c135b5c5d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273528"
---
# <a name="acceptservername"></a><span data-ttu-id="9714f-105">акцептсервернаме</span><span class="sxs-lookup"><span data-stu-id="9714f-105">AcceptServerName</span></span>

<span data-ttu-id="9714f-106">Элемент **акцептсервернаме (еаптипе)** указывает, проверяется ли имя сервера на соответствие строке имени, указанной в элементе [**ServerName (сервервалидатионпараметерс)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9714f-106">The **AcceptServerName (EapType)** element indicates whether the server name is validated against the name string specified in the [**ServerNames (ServerValidationParameters)**](eaptlsconnectionpropertiesv1schema-servernames-servervalidationparameters-element.md) element.</span></span>

``` syntax
<xs:element
    minOccurs="0"
    maxOccurs="1"
    ref="extendedTLS: AcceptServerName"
 />
```

<span data-ttu-id="9714f-107">Элемент определяется элементом [**еаптипе**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="9714f-107">The element is defined by the [**EapType**](eaptlsconnectionpropertiesv1schema-eaptype-element.md) element.</span></span>

## <a name="remarks"></a><span data-ttu-id="9714f-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9714f-108">Remarks</span></span>

<span data-ttu-id="9714f-109">Элемент **акцептсервернаме** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="9714f-109">The **AcceptServerName** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="9714f-110">Требования</span><span class="sxs-lookup"><span data-stu-id="9714f-110">Requirements</span></span>



| <span data-ttu-id="9714f-111">Требование</span><span class="sxs-lookup"><span data-stu-id="9714f-111">Requirement</span></span> | <span data-ttu-id="9714f-112">Значение</span><span class="sxs-lookup"><span data-stu-id="9714f-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="9714f-113">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9714f-113">Minimum supported client</span></span><br/> | <span data-ttu-id="9714f-114">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="9714f-114">Windows 7 \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="9714f-115">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9714f-115">Minimum supported server</span></span><br/> | <span data-ttu-id="9714f-116">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="9714f-116">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9714f-117">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9714f-117">See also</span></span>

<dl> <dt>

<span data-ttu-id="9714f-118">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="9714f-118">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="9714f-119">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="9714f-119">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
</dt> <dt>

<span data-ttu-id="9714f-120">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="9714f-120">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="9714f-121">**еаптипе**</span><span class="sxs-lookup"><span data-stu-id="9714f-121">**EapType**</span></span>](eaptlsconnectionpropertiesv1schema-eaptype-element.md)
<span data-ttu-id="9714f-122"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="9714f-122"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="9714f-123">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="9714f-123">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="9714f-124">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="9714f-124">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="9714f-125">Элементы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="9714f-125">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> <dt>

[<span data-ttu-id="9714f-126">**Акцептсервернаме (Еаптипе)**</span><span class="sxs-lookup"><span data-stu-id="9714f-126">**AcceptServerName (EapType)**</span></span>](eaptlsconnectionpropertiesv2schema-acceptservername-eaptype-element.md)
</dt> </dl>

 

 





