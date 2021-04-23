---
title: Элемент Трустедрутка (Сервервалидатионпараметерс) — подключение
description: Записывает отпечатки для корневых центров сертификации (CAs), которые являются доверенными для клиента. | Трустедрутка (Сервервалидатионпараметерс), элемент
ms.assetid: 81e3b6ca-6360-42dc-bfd3-298e81e66c1a
keywords:
- Элемент Трустедрутка EAPHost
topic_type:
- apiref
api_name:
- TrustedRootCA
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: e6f91816ba90300a76545a7a22cea6d037b4e897
ms.sourcegitcommit: 168d11879cb9fd89d26f826482725c0a626be00f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/16/2021
ms.locfileid: "105694366"
---
# <a name="trustedrootca-servervalidationparameters-element-for-connection-properties"></a><span data-ttu-id="6bc35-105">Элемент Трустедрутка (Сервервалидатионпараметерс) для свойств соединения</span><span class="sxs-lookup"><span data-stu-id="6bc35-105">TrustedRootCA (ServerValidationParameters) Element for connection properties</span></span>

<span data-ttu-id="6bc35-106">Элемент **трустедрутка (сервервалидатионпараметерс)** захватывает отпечатки для корневых центров сертификации (CAS), которые являются доверенными для клиента.</span><span class="sxs-lookup"><span data-stu-id="6bc35-106">The **TrustedRootCA (ServerValidationParameters)** element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="6bc35-107">Элемент **трустедрутка** определяется сложным типом [**сервервалидатионпараметерс**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="6bc35-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="6bc35-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6bc35-108">Remarks</span></span>

<span data-ttu-id="6bc35-109">Thumb Print — это шестнадцатеричная строка, которая содержит хэш SHA-1 сертификата.</span><span class="sxs-lookup"><span data-stu-id="6bc35-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="6bc35-110">Элемент **трустедрутка** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="6bc35-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="6bc35-111">Требования</span><span class="sxs-lookup"><span data-stu-id="6bc35-111">Requirements</span></span>



| <span data-ttu-id="6bc35-112">Требование</span><span class="sxs-lookup"><span data-stu-id="6bc35-112">Requirement</span></span> | <span data-ttu-id="6bc35-113">Значение</span><span class="sxs-lookup"><span data-stu-id="6bc35-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="6bc35-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6bc35-114">Minimum supported client</span></span><br/> | <span data-ttu-id="6bc35-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="6bc35-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="6bc35-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6bc35-116">Minimum supported server</span></span><br/> | <span data-ttu-id="6bc35-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="6bc35-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6bc35-118">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6bc35-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="6bc35-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="6bc35-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="6bc35-120">**сервервалидатионпараметерс**</span><span class="sxs-lookup"><span data-stu-id="6bc35-120">**ServerValidationParameters**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="6bc35-121">**Возможные непосредственные родительские элементы в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="6bc35-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="6bc35-122">**Сервервалидатион (Еаптипе)**</span><span class="sxs-lookup"><span data-stu-id="6bc35-122">**ServerValidation (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="6bc35-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="6bc35-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="6bc35-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="6bc35-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="6bc35-125">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="6bc35-125">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="6bc35-126">Элементы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="6bc35-126">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





