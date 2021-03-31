---
title: Еаптипе, элемент
description: Является производным типом элемента Еаптипе из схемы baseeapuserpropertiesv1. | Еаптипе, элемент
ms.assetid: c9117803-dbf0-498d-8f86-f44ac2e6b2dc
keywords:
- Элемент Еаптипе EAPHost
topic_type:
- apiref
api_name:
- EapType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: be2fd00cde752cae1ae8af0fa0305cbed2cdfe7c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "104273418"
---
# <a name="eaptype-element"></a><span data-ttu-id="adda9-105">Еаптипе, элемент</span><span class="sxs-lookup"><span data-stu-id="adda9-105">EapType Element</span></span>

<span data-ttu-id="adda9-106">Элемент **еаптипе** является производным типом элемента [**еаптипе**](baseeapuserpropertiesv1schema-eaptype-element.md) из схемы [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="adda9-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

``` syntax
<xs:element name="EapType"
    substitutionGroup="EapType"
>
    <xs:complexType>
        <xs:complexContent>
            <xs:extension
                base="BaseEapTypeParameters"
            >
                <xs:sequence>
                    <xs:element
                        ref="Username"
                     />
                    <xs:element name="UserCert"
                        type="hexBinary"
                     />
                    <xs:any
                        processContents="lax"
                        minOccurs="0"
                        maxOccurs="unbounded"
                        namespace="##other"
                     />
                </xs:sequence>
            </xs:extension>
        </xs:complexContent>
    </xs:complexType>
</xs:element>
```

## <a name="child-elements"></a><span data-ttu-id="adda9-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="adda9-107">Child elements</span></span>



| <span data-ttu-id="adda9-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="adda9-108">Element</span></span>                                                                   | <span data-ttu-id="adda9-109">Тип</span><span class="sxs-lookup"><span data-stu-id="adda9-109">Type</span></span>      | <span data-ttu-id="adda9-110">Описание</span><span class="sxs-lookup"><span data-stu-id="adda9-110">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="adda9-111">**Имен**</span><span class="sxs-lookup"><span data-stu-id="adda9-111">**Username**</span></span>](eaptlsuserpropertiesv1schema-username-element.md)         |           | <span data-ttu-id="adda9-112">Захватывает имя пользователя для отправки в ответе EAP-Identity.</span><span class="sxs-lookup"><span data-stu-id="adda9-112">Captures the user name to be sent in the EAP-Identity response.</span></span> <span data-ttu-id="adda9-113">Если элемент [**username**](eaptlsuserpropertiesv1schema-username-element.md) отсутствует, то EAP-TLS использует имя в сертификате, на который ссылается элемент [**усерцерт**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="adda9-113">If the [**Username**](eaptlsuserpropertiesv1schema-username-element.md) element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span><br/> |
| [<span data-ttu-id="adda9-114">**усерцерт**</span><span class="sxs-lookup"><span data-stu-id="adda9-114">**UserCert**</span></span>](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | <span data-ttu-id="adda9-115">hexBinary</span><span class="sxs-lookup"><span data-stu-id="adda9-115">hexBinary</span></span> | <span data-ttu-id="adda9-116">Ссылается на хэш SHA-1 сертификата, который следует использовать для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="adda9-116">Refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span><br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a><span data-ttu-id="adda9-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="adda9-117">Remarks</span></span>

<span data-ttu-id="adda9-118">Элемент **processContents** обеспечивает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="adda9-118">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="adda9-119">Элемент **processContents** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="adda9-119">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="adda9-120">Требования</span><span class="sxs-lookup"><span data-stu-id="adda9-120">Requirements</span></span>



| <span data-ttu-id="adda9-121">Требование</span><span class="sxs-lookup"><span data-stu-id="adda9-121">Requirement</span></span> | <span data-ttu-id="adda9-122">Значение</span><span class="sxs-lookup"><span data-stu-id="adda9-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="adda9-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="adda9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="adda9-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="adda9-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="adda9-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="adda9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="adda9-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="adda9-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="adda9-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="adda9-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="adda9-128">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="adda9-128">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="adda9-129">Схема eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="adda9-129">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





