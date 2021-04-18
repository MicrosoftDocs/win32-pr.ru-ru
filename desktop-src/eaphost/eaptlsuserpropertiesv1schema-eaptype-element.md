---
title: Элемент Еаптипе (eaptlsuserpropertiesv1schema)
description: Этот элемент является производным типом элемента Еаптипе из схемы baseeapuserpropertiesv1. Для eaptlsuserpropertiesv1schema.
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
ms.openlocfilehash: 53e5c1404c70542f3604b94aa6cae9c8fc39fd21
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187757"
---
# <a name="eaptype-element-eaptlsuserpropertiesv1schema"></a><span data-ttu-id="1c6be-105">Элемент Еаптипе (eaptlsuserpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="1c6be-105">EapType element (eaptlsuserpropertiesv1schema)</span></span>

<span data-ttu-id="1c6be-106">Элемент **еаптипе** является производным типом элемента [**еаптипе**](baseeapuserpropertiesv1schema-eaptype-element.md) из схемы [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="1c6be-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="1c6be-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="1c6be-107">Child elements</span></span>



| <span data-ttu-id="1c6be-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="1c6be-108">Element</span></span>                                                                   | <span data-ttu-id="1c6be-109">Тип</span><span class="sxs-lookup"><span data-stu-id="1c6be-109">Type</span></span>      | <span data-ttu-id="1c6be-110">Описание</span><span class="sxs-lookup"><span data-stu-id="1c6be-110">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|---------------------------------------------------------------------------|-----------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1c6be-111">**Имен**</span><span class="sxs-lookup"><span data-stu-id="1c6be-111">**Username**</span></span>](eaptlsuserpropertiesv1schema-username-element.md)         |           | <span data-ttu-id="1c6be-112">Захватывает имя пользователя для отправки в ответе EAP-Identity.</span><span class="sxs-lookup"><span data-stu-id="1c6be-112">Captures the user name to be sent in the EAP-Identity response.</span></span> <span data-ttu-id="1c6be-113">Если элемент [**username**](eaptlsuserpropertiesv1schema-username-element.md) отсутствует, то EAP-TLS использует имя в сертификате, на который ссылается элемент [**усерцерт**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) .</span><span class="sxs-lookup"><span data-stu-id="1c6be-113">If the [**Username**](eaptlsuserpropertiesv1schema-username-element.md) element is absent, then EAP-TLS uses the name in the certificate referred to in the [**UserCert**](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) element.</span></span><br/> |
| [<span data-ttu-id="1c6be-114">**усерцерт**</span><span class="sxs-lookup"><span data-stu-id="1c6be-114">**UserCert**</span></span>](eaptlsuserpropertiesv1schema-usercert-eaptype-element.md) | <span data-ttu-id="1c6be-115">hexBinary</span><span class="sxs-lookup"><span data-stu-id="1c6be-115">hexBinary</span></span> | <span data-ttu-id="1c6be-116">Ссылается на хэш SHA-1 сертификата, который следует использовать для проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="1c6be-116">Refers to the SHA-1 hash of the certificate that should be used for authentication.</span></span><br/>                                                                                                                                                                                                                             |



## <a name="remarks"></a><span data-ttu-id="1c6be-117">Remarks</span><span class="sxs-lookup"><span data-stu-id="1c6be-117">Remarks</span></span>

<span data-ttu-id="1c6be-118">Элемент **processContents** обеспечивает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="1c6be-118">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="1c6be-119">Элемент **processContents** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="1c6be-119">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="1c6be-120">Требования</span><span class="sxs-lookup"><span data-stu-id="1c6be-120">Requirements</span></span>



| <span data-ttu-id="1c6be-121">Требование</span><span class="sxs-lookup"><span data-stu-id="1c6be-121">Requirement</span></span> | <span data-ttu-id="1c6be-122">Значение</span><span class="sxs-lookup"><span data-stu-id="1c6be-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1c6be-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1c6be-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1c6be-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="1c6be-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1c6be-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1c6be-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1c6be-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="1c6be-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1c6be-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1c6be-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c6be-128">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="1c6be-128">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="1c6be-129">Схема eaptlsuserpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="1c6be-129">eaptlsuserpropertiesv1 Schema</span></span>](eaptlsuserpropertiesv1schema-schema.md)
</dt> </dl>

 

 





