---
title: Элемент смарт-карты (Кредентиалссаурцепараметерс)
description: Указывает, что EAP-TLS должен считывать сертификат из смарт-карты.
ms.assetid: 0755b0bf-520a-4ae6-a8fc-2f69ae12b066
keywords:
- Элемент смарт-карты EAPHost
topic_type:
- apiref
api_name:
- SmartCard
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 14581a06064a242a0f66e763e0b848d7d74bce50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105710509"
---
# <a name="smartcard-credentialssourceparameters-element"></a><span data-ttu-id="0d015-104">Элемент смарт-карты (Кредентиалссаурцепараметерс)</span><span class="sxs-lookup"><span data-stu-id="0d015-104">SmartCard (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="0d015-105">Элемент Smart Card **(кредентиалссаурцепараметерс)** указывает, что EAP-TLS должен прочитать сертификат из смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="0d015-105">The **SmartCard (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the Smart Card.</span></span>

``` syntax
<xs:element name="SmartCard"
    type="emptyString"
 />
```

<span data-ttu-id="0d015-106">Элемент **смарт-карты** определяется сложным типом [**кредентиалссаурцепараметерс**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="0d015-106">The **SmartCard** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d015-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d015-107">Remarks</span></span>

<span data-ttu-id="0d015-108">Элементы [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) и **смарт-карты** не могут одновременно использоваться одновременно.</span><span class="sxs-lookup"><span data-stu-id="0d015-108">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and **SmartCard** elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d015-109">Требования</span><span class="sxs-lookup"><span data-stu-id="0d015-109">Requirements</span></span>



| <span data-ttu-id="0d015-110">Требование</span><span class="sxs-lookup"><span data-stu-id="0d015-110">Requirement</span></span> | <span data-ttu-id="0d015-111">Значение</span><span class="sxs-lookup"><span data-stu-id="0d015-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0d015-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d015-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0d015-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0d015-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="0d015-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d015-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0d015-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0d015-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d015-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d015-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="0d015-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="0d015-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="0d015-118">**кредентиалссаурцепараметерс**</span><span class="sxs-lookup"><span data-stu-id="0d015-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="0d015-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="0d015-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="0d015-120">**Кредентиалссаурце (Еаптипе)**</span><span class="sxs-lookup"><span data-stu-id="0d015-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="0d015-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="0d015-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="0d015-122">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="0d015-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="0d015-123">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="0d015-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="0d015-124">Элементы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="0d015-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





