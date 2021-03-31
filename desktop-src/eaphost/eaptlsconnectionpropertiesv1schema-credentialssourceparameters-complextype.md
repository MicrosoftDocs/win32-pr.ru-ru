---
title: Сложный тип Кредентиалссаурцепараметерс
description: Определяет элемент, необходимый для указания источника сертификата, используемого с проверкой подлинности EAP-TLS.
ms.assetid: 1482694e-3025-4231-8154-4be0301fe5ce
keywords:
- Кредентиалссаурцепараметерс сложный тип EAPHost
topic_type:
- apiref
api_name:
- CredentialsSourceParameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 912faa4a388d9a57225991959625a978ca0921f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136691"
---
# <a name="credentialssourceparameters-complex-type"></a><span data-ttu-id="652d9-104">Сложный тип Кредентиалссаурцепараметерс</span><span class="sxs-lookup"><span data-stu-id="652d9-104">CredentialsSourceParameters Complex Type</span></span>

<span data-ttu-id="652d9-105">Сложный тип **кредентиалссаурцепараметерс** определяет элемент, необходимый для указания источника сертификата, который будет использоваться с проверкой подлинности EAP-TLS.</span><span class="sxs-lookup"><span data-stu-id="652d9-105">The **CredentialsSourceParameters** complex type defines the element required to specify the source of the certificate to be used with an EAP-TLS authentication.</span></span>

<span data-ttu-id="652d9-106">Существует возможность выбора между элементом [**смарт-карты**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) или элементом [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) .</span><span class="sxs-lookup"><span data-stu-id="652d9-106">There is a choice between the [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) element or [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) element.</span></span>

``` syntax
<xs:complexType name="CredentialsSourceParameters">
    <xs:choice>
        <xs:element name="SmartCard"
            type="emptyString"
         />
        <xs:element name="CertificateStore"
            type="CertSelection"
         />
    </xs:choice>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="652d9-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="652d9-107">Child elements</span></span>



| <span data-ttu-id="652d9-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="652d9-108">Element</span></span>                                                                                                             | <span data-ttu-id="652d9-109">Тип</span><span class="sxs-lookup"><span data-stu-id="652d9-109">Type</span></span>                                                                                  | <span data-ttu-id="652d9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="652d9-110">Description</span></span>                                                                                                                  |
|---------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="652d9-111">**ИмяХранилищаСертификатов**</span><span class="sxs-lookup"><span data-stu-id="652d9-111">**CertificateStore**</span></span>](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) | [<span data-ttu-id="652d9-112">**цертселектион**</span><span class="sxs-lookup"><span data-stu-id="652d9-112">**CertSelection**</span></span>](eaptlsconnectionpropertiesv1schema-certselection-complextype.md) | <span data-ttu-id="652d9-113">Указывает, что EAP-TLS должен прочитать сертификат из моего хранилища пользователя или проверить подлинность компьютера.</span><span class="sxs-lookup"><span data-stu-id="652d9-113">Indicates that EAP-TLS should read the certificate from the user's My Store, or the machine being authenticated.</span></span> <br/> |
| [<span data-ttu-id="652d9-114">**Карте**</span><span class="sxs-lookup"><span data-stu-id="652d9-114">**SmartCard**</span></span>](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md)               | [<span data-ttu-id="652d9-115">**emptyString**</span><span class="sxs-lookup"><span data-stu-id="652d9-115">**emptyString**</span></span>](eaptlsconnectionpropertiesv1schema-emptystring-simpletype.md)      | <span data-ttu-id="652d9-116">Указывает, что EAP-TLS должен считывать сертификат из смарт-карты.</span><span class="sxs-lookup"><span data-stu-id="652d9-116">Indicates that EAP-TLS should read the certificate from the Smart Card.</span></span> <br/>                                          |



## <a name="remarks"></a><span data-ttu-id="652d9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="652d9-117">Remarks</span></span>

<span data-ttu-id="652d9-118">Элементы [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) и [**смарт-карты**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) не могут одновременно использоваться одновременно.</span><span class="sxs-lookup"><span data-stu-id="652d9-118">The [**CertificateStore**](eaptlsconnectionpropertiesv1schema-certificatestore-credentialssourceparameters-element.md) and [**SmartCard**](eaptlsconnectionpropertiesv1schema-smartcard-credentialssourceparameters-element.md) elements cannot both be used simultaneously.</span></span>

## <a name="requirements"></a><span data-ttu-id="652d9-119">Требования</span><span class="sxs-lookup"><span data-stu-id="652d9-119">Requirements</span></span>



| <span data-ttu-id="652d9-120">Требование</span><span class="sxs-lookup"><span data-stu-id="652d9-120">Requirement</span></span> | <span data-ttu-id="652d9-121">Значение</span><span class="sxs-lookup"><span data-stu-id="652d9-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="652d9-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="652d9-122">Minimum supported client</span></span><br/> | <span data-ttu-id="652d9-123">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="652d9-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="652d9-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="652d9-124">Minimum supported server</span></span><br/> | <span data-ttu-id="652d9-125">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="652d9-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="652d9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="652d9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="652d9-127">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="652d9-127">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="652d9-128">Схема eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="652d9-128">eaptlsconnectionpropertiesv1 Schema</span></span>](eaptlsconnectionpropertiesv1schema-schema.md)
</dt> <dt>

[<span data-ttu-id="652d9-129">Сложные типы схемы eaptlsconnectionpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="652d9-129">eaptlsconnectionpropertiesv1 Schema Complex Types</span></span>](eaptlsconnectionpropertiesv1schema-complex-types.md)
</dt> </dl>

 

 





