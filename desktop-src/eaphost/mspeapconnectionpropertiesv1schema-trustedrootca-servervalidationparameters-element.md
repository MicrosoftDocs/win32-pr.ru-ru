---
title: Элемент Трустедрутка (Сервервалидатионпараметерс) (v1)
description: Записывает отпечатки для корневых центров сертификации (CAs), которые являются доверенными для клиента. | Трустедрутка (Сервервалидатионпараметерс), элемент
ms.assetid: f0485dcc-8610-4c5b-b4db-6f2a77057489
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
ms.openlocfilehash: 17e1b81e080d48ac8fae4f082c3cf4b46bac858e
ms.sourcegitcommit: 4d4a6e9ad5de37e467cd3164276771b71e1f113f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/05/2021
ms.locfileid: "106389081"
---
# <a name="trustedrootca-servervalidationparameters-element"></a><span data-ttu-id="45282-105">Трустедрутка (Сервервалидатионпараметерс), элемент</span><span class="sxs-lookup"><span data-stu-id="45282-105">TrustedRootCA (ServerValidationParameters) Element</span></span>

<span data-ttu-id="45282-106">Элемент **трустедрутка (сервервалидатионпараметерс)** захватывает отпечатки для корневых центров сертификации (CAS), которые являются доверенными для клиента.</span><span class="sxs-lookup"><span data-stu-id="45282-106">The **TrustedRootCA (ServerValidationParameters)** element element captures the thumb print of root certificate authorities (CAs) that are trusted by the client.</span></span>

``` syntax
<xs:element name="TrustedRootCA"
    type="hexBinary"
 />
```

<span data-ttu-id="45282-107">Элемент **трустедрутка** определяется сложным типом [**сервервалидатионпараметерс**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="45282-107">The **TrustedRootCA** element is defined by the [**ServerValidationParameters**](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="45282-108">Remarks</span><span class="sxs-lookup"><span data-stu-id="45282-108">Remarks</span></span>

<span data-ttu-id="45282-109">Thumb Print — это шестнадцатеричная строка, которая содержит хэш SHA-1 сертификата.</span><span class="sxs-lookup"><span data-stu-id="45282-109">The thumb print is a hexadecimal string that contains the SHA-1 hash of the certificate.</span></span> <span data-ttu-id="45282-110">Элемент **трустедрутка** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="45282-110">The **TrustedRootCA** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="45282-111">Требования</span><span class="sxs-lookup"><span data-stu-id="45282-111">Requirements</span></span>



| <span data-ttu-id="45282-112">Требование</span><span class="sxs-lookup"><span data-stu-id="45282-112">Requirement</span></span> | <span data-ttu-id="45282-113">Значение</span><span class="sxs-lookup"><span data-stu-id="45282-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="45282-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="45282-114">Minimum supported client</span></span><br/> | <span data-ttu-id="45282-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="45282-115">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="45282-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="45282-116">Minimum supported server</span></span><br/> | <span data-ttu-id="45282-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="45282-117">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="45282-118">См. также</span><span class="sxs-lookup"><span data-stu-id="45282-118">See also</span></span>

<dl> <dt>

<span data-ttu-id="45282-119">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="45282-119">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="45282-120">**сервервалидатионпараметерс**</span><span class="sxs-lookup"><span data-stu-id="45282-120">**ServerValidationParameters**</span></span>](mspeapconnectionpropertiesv1schema-servervalidationparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="45282-121">**Возможные непосредственные родительские элементы в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="45282-121">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="45282-122">**Сервервалидатион (Еаптипе)**</span><span class="sxs-lookup"><span data-stu-id="45282-122">**ServerValidation (EapType)**</span></span>](mspeapconnectionpropertiesv1schema-servervalidation-eaptype-element.md)
<span data-ttu-id="45282-123"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="45282-123"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="45282-124">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="45282-124">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="45282-125">Схема mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="45282-125">mspeapconnectionpropertiesv1 Schema</span></span>](mspeapconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="45282-126">Элементы схемы mspeapconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="45282-126">mspeapconnectionpropertiesv1 Schema Elements</span></span>](mspeapconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





