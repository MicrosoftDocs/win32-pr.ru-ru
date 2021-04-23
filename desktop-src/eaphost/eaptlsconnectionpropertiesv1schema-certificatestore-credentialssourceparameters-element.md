---
title: CertificateStore (Кредентиалссаурцепараметерс), элемент
description: Указывает, что EAP-TLS должен прочитать сертификат из моего хранилища пользователя или проверить подлинность компьютера.
ms.assetid: 6b15c7cc-b686-4419-a962-e3dd6b4b84a6
keywords:
- Элемент CertificateStore EAPHost
topic_type:
- apiref
api_name:
- CertificateStore
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc7c8841fe275d19752f8b774de5766b95824339
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534718"
---
# <a name="certificatestore-credentialssourceparameters-element"></a><span data-ttu-id="cd037-104">CertificateStore (Кредентиалссаурцепараметерс), элемент</span><span class="sxs-lookup"><span data-stu-id="cd037-104">CertificateStore (CredentialsSourceParameters) Element</span></span>

<span data-ttu-id="cd037-105">Элемент **CertificateStore (кредентиалссаурцепараметерс)** указывает, что EAP-TLS должен прочитать сертификат из моего хранилища пользователя или проверить подлинность компьютера.</span><span class="sxs-lookup"><span data-stu-id="cd037-105">The **CertificateStore (CredentialsSourceParameters)** element indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span>

``` syntax
<xs:element name="CertificateStore"
    type="CertSelection"
 />
```

<span data-ttu-id="cd037-106">Элемент **CertificateStore** определяется сложным типом [**кредентиалссаурцепараметерс**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="cd037-106">The **CertificateStore** element is defined by the [**CredentialsSourceParameters**](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md) complex type.</span></span>

## <a name="remarks"></a><span data-ttu-id="cd037-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="cd037-107">Remarks</span></span>

<span data-ttu-id="cd037-108">Элементы **CertificateStore** и [**смарт-карты**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) не могут одновременно использоваться одновременно.</span><span class="sxs-lookup"><span data-stu-id="cd037-108">The **CertificateStore** and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="cd037-109">Требования</span><span class="sxs-lookup"><span data-stu-id="cd037-109">Requirements</span></span>



| <span data-ttu-id="cd037-110">Требование</span><span class="sxs-lookup"><span data-stu-id="cd037-110">Requirement</span></span> | <span data-ttu-id="cd037-111">Значение</span><span class="sxs-lookup"><span data-stu-id="cd037-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cd037-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="cd037-112">Minimum supported client</span></span><br/> | <span data-ttu-id="cd037-113">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="cd037-113">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="cd037-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="cd037-114">Minimum supported server</span></span><br/> | <span data-ttu-id="cd037-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="cd037-115">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cd037-116">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="cd037-116">See also</span></span>

<dl> <dt>

<span data-ttu-id="cd037-117">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="cd037-117">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="cd037-118">**кредентиалссаурцепараметерс**</span><span class="sxs-lookup"><span data-stu-id="cd037-118">**CredentialsSourceParameters**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssourceparameters-complextype.md)
</dt> <dt>

<span data-ttu-id="cd037-119">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="cd037-119">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="cd037-120">**Кредентиалссаурце (Еаптипе)**</span><span class="sxs-lookup"><span data-stu-id="cd037-120">**CredentialsSource (EapType)**</span></span>](eaptlsconnectionpropertiesv1schema-credentialssource-eaptype-element.md)
<span data-ttu-id="cd037-121"></dt> <dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="cd037-121"></dt> <dt>


</dt> <dt></span></span>

[<span data-ttu-id="cd037-122">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="cd037-122">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="cd037-123">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cd037-123">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="cd037-124">Элементы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="cd037-124">eaptlsconnectionpropertiesv1 Schema Elements</span></span>](eaptlsconnectionpropertiesv1schema-elements.md)
</dt> </dl>

 

 





