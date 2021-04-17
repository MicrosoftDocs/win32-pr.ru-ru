---
title: Еаптипе, элемент
description: Является производным типом элемента Еаптипе из схемы baseeapuserpropertiesv1. | Еаптипе, элемент
ms.assetid: 7bd8fb5b-ceff-4d82-a979-b01229f8863a
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
ms.openlocfilehash: b2d4ff105b71e19b27f1a5cf975fb740b9f1a5fd
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/09/2021
ms.locfileid: "105703581"
---
# <a name="eaptype-element"></a><span data-ttu-id="43e75-105">Еаптипе, элемент</span><span class="sxs-lookup"><span data-stu-id="43e75-105">EapType Element</span></span>

<span data-ttu-id="43e75-106">Элемент **еаптипе** является производным типом элемента [**еаптипе**](baseeapuserpropertiesv1schema-eaptype-element.md) из схемы [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="43e75-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

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
                        minOccurs="0"
                        ref="Username"
                     />
                    <xs:element name="Password"
                        type="string"
                        minOccurs="0"
                     />
                    <xs:element name="LogonDomain"
                        type="string"
                        minOccurs="0"
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

## <a name="child-elements"></a><span data-ttu-id="43e75-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="43e75-107">Child elements</span></span>



| <span data-ttu-id="43e75-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="43e75-108">Element</span></span>                                                                           | <span data-ttu-id="43e75-109">Тип</span><span class="sxs-lookup"><span data-stu-id="43e75-109">Type</span></span>   | <span data-ttu-id="43e75-110">Описание</span><span class="sxs-lookup"><span data-stu-id="43e75-110">Description</span></span>                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="43e75-111">**Имен**</span><span class="sxs-lookup"><span data-stu-id="43e75-111">**Username**</span></span>](mschapv2userpropertiesv1schema-username-element.md)               |        | <span data-ttu-id="43e75-112">Указывает пользователя, для которого выполняется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="43e75-112">Identifies the user being authenticated.</span></span> <span data-ttu-id="43e75-113">Если этот элемент отсутствует, имя пользователя получается из Winlogon.</span><span class="sxs-lookup"><span data-stu-id="43e75-113">If this element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="43e75-114">Элемент [**username**](mschapv2userpropertiesv1schema-username-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="43e75-114">The [**Username**](mschapv2userpropertiesv1schema-username-element.md) element is optional.</span></span><br/>                                        |
| [<span data-ttu-id="43e75-115">**LogonDomain**</span><span class="sxs-lookup"><span data-stu-id="43e75-115">**LogonDomain**</span></span>](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | <span data-ttu-id="43e75-116">строка</span><span class="sxs-lookup"><span data-stu-id="43e75-116">string</span></span> | <span data-ttu-id="43e75-117">Определяет домен пользователя или компьютера, для которого выполняется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="43e75-117">Identifies the domain of the user or machine being authenticated.</span></span> <span data-ttu-id="43e75-118">Если этот элемент отсутствует, используется домен из Winlogon.</span><span class="sxs-lookup"><span data-stu-id="43e75-118">If this element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="43e75-119">Элемент [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="43e75-119">The [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) element is optional.</span></span><br/>        |
| [<span data-ttu-id="43e75-120">**Пароль**</span><span class="sxs-lookup"><span data-stu-id="43e75-120">**Password**</span></span>](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | <span data-ttu-id="43e75-121">строка</span><span class="sxs-lookup"><span data-stu-id="43e75-121">string</span></span> | <span data-ttu-id="43e75-122">Указывает пароль пользователя или компьютера, для которого выполняется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="43e75-122">Identifies the password of the user or machine being authenticated.</span></span> <span data-ttu-id="43e75-123">Если этот элемент отсутствует, хэш пароля получается из Winlogon.</span><span class="sxs-lookup"><span data-stu-id="43e75-123">If this element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="43e75-124">Элемент [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="43e75-124">The [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="43e75-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="43e75-125">Remarks</span></span>

<span data-ttu-id="43e75-126">Элемент **processContents** обеспечивает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="43e75-126">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="43e75-127">Элемент **processContents** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="43e75-127">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="43e75-128">Требования</span><span class="sxs-lookup"><span data-stu-id="43e75-128">Requirements</span></span>



| <span data-ttu-id="43e75-129">Требование</span><span class="sxs-lookup"><span data-stu-id="43e75-129">Requirement</span></span> | <span data-ttu-id="43e75-130">Значение</span><span class="sxs-lookup"><span data-stu-id="43e75-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="43e75-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="43e75-131">Minimum supported client</span></span><br/> | <span data-ttu-id="43e75-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="43e75-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="43e75-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="43e75-133">Minimum supported server</span></span><br/> | <span data-ttu-id="43e75-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="43e75-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43e75-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="43e75-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43e75-136">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="43e75-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="43e75-137">Схема mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="43e75-137">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





