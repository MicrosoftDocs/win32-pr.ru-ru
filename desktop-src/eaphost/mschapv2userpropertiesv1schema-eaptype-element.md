---
title: Элемент Еаптипе (mschapv2userpropertiesv1schema)
description: Этот элемент является производным типом элемента Еаптипе из схемы baseeapuserpropertiesv1. Для mschapv2userpropertiesv1schema.
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
ms.openlocfilehash: d5985123a4679fe9b2524f9338b9181daa11282d
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/02/2021
ms.locfileid: "106187749"
---
# <a name="eaptype-element-mschapv2userpropertiesv1schema"></a><span data-ttu-id="05b69-105">Элемент Еаптипе (mschapv2userpropertiesv1schema)</span><span class="sxs-lookup"><span data-stu-id="05b69-105">EapType element (mschapv2userpropertiesv1schema)</span></span>

<span data-ttu-id="05b69-106">Элемент **еаптипе** является производным типом элемента [**еаптипе**](baseeapuserpropertiesv1schema-eaptype-element.md) из схемы [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) .</span><span class="sxs-lookup"><span data-stu-id="05b69-106">The **EapType** element is a derived type of the [**EapType**](baseeapuserpropertiesv1schema-eaptype-element.md) element from the [baseeapuserpropertiesv1](baseeapuserpropertiesv1schema-schema.md) schema.</span></span>

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

## <a name="child-elements"></a><span data-ttu-id="05b69-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="05b69-107">Child elements</span></span>



| <span data-ttu-id="05b69-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="05b69-108">Element</span></span>                                                                           | <span data-ttu-id="05b69-109">Тип</span><span class="sxs-lookup"><span data-stu-id="05b69-109">Type</span></span>   | <span data-ttu-id="05b69-110">Описание</span><span class="sxs-lookup"><span data-stu-id="05b69-110">Description</span></span>                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|--------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="05b69-111">**Имен**</span><span class="sxs-lookup"><span data-stu-id="05b69-111">**Username**</span></span>](mschapv2userpropertiesv1schema-username-element.md)               |        | <span data-ttu-id="05b69-112">Указывает пользователя, для которого выполняется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="05b69-112">Identifies the user being authenticated.</span></span> <span data-ttu-id="05b69-113">Если этот элемент отсутствует, имя пользователя получается из Winlogon.</span><span class="sxs-lookup"><span data-stu-id="05b69-113">If this element is not present, the user name is obtained from winlogon.</span></span> <span data-ttu-id="05b69-114">Элемент [**username**](mschapv2userpropertiesv1schema-username-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="05b69-114">The [**Username**](mschapv2userpropertiesv1schema-username-element.md) element is optional.</span></span><br/>                                        |
| [<span data-ttu-id="05b69-115">**LogonDomain**</span><span class="sxs-lookup"><span data-stu-id="05b69-115">**LogonDomain**</span></span>](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) | <span data-ttu-id="05b69-116">строка</span><span class="sxs-lookup"><span data-stu-id="05b69-116">string</span></span> | <span data-ttu-id="05b69-117">Определяет домен пользователя или компьютера, для которого выполняется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="05b69-117">Identifies the domain of the user or machine being authenticated.</span></span> <span data-ttu-id="05b69-118">Если этот элемент отсутствует, используется домен из Winlogon.</span><span class="sxs-lookup"><span data-stu-id="05b69-118">If this element is not present, the domain from winlogon is used.</span></span> <span data-ttu-id="05b69-119">Элемент [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="05b69-119">The [**LogonDomain**](mschapv2userpropertiesv1schema-logondomain-eaptype-element.md) element is optional.</span></span><br/>        |
| [<span data-ttu-id="05b69-120">**Пароль**</span><span class="sxs-lookup"><span data-stu-id="05b69-120">**Password**</span></span>](mschapv2userpropertiesv1schema-password-eaptype-element.md)       | <span data-ttu-id="05b69-121">строка</span><span class="sxs-lookup"><span data-stu-id="05b69-121">string</span></span> | <span data-ttu-id="05b69-122">Указывает пароль пользователя или компьютера, для которого выполняется проверка подлинности.</span><span class="sxs-lookup"><span data-stu-id="05b69-122">Identifies the password of the user or machine being authenticated.</span></span> <span data-ttu-id="05b69-123">Если этот элемент отсутствует, хэш пароля получается из Winlogon.</span><span class="sxs-lookup"><span data-stu-id="05b69-123">If this element is not present, the password hash is obtained from winlogon.</span></span> <span data-ttu-id="05b69-124">Элемент [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) является необязательным.</span><span class="sxs-lookup"><span data-stu-id="05b69-124">The [**Password**](mschapv2userpropertiesv1schema-password-eaptype-element.md) element is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="05b69-125">Remarks</span><span class="sxs-lookup"><span data-stu-id="05b69-125">Remarks</span></span>

<span data-ttu-id="05b69-126">Элемент **processContents** обеспечивает будущие улучшения схемы.</span><span class="sxs-lookup"><span data-stu-id="05b69-126">The **processContents** element enables future enhancements to the schema.</span></span> <span data-ttu-id="05b69-127">Элемент **processContents** является необязательным.</span><span class="sxs-lookup"><span data-stu-id="05b69-127">The **processContents** element is optional.</span></span>

## <a name="requirements"></a><span data-ttu-id="05b69-128">Требования</span><span class="sxs-lookup"><span data-stu-id="05b69-128">Requirements</span></span>



| <span data-ttu-id="05b69-129">Требование</span><span class="sxs-lookup"><span data-stu-id="05b69-129">Requirement</span></span> | <span data-ttu-id="05b69-130">Значение</span><span class="sxs-lookup"><span data-stu-id="05b69-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="05b69-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="05b69-131">Minimum supported client</span></span><br/> | <span data-ttu-id="05b69-132">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="05b69-132">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="05b69-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="05b69-133">Minimum supported server</span></span><br/> | <span data-ttu-id="05b69-134">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="05b69-134">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="05b69-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="05b69-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="05b69-136">EAPHost и схема прежних версий</span><span class="sxs-lookup"><span data-stu-id="05b69-136">EAPHost and Legacy Schema</span></span>](eaphost-schemas.md)
</dt> <dt>

[<span data-ttu-id="05b69-137">Схема mschapv2userpropertiesv1</span><span class="sxs-lookup"><span data-stu-id="05b69-137">mschapv2userpropertiesv1 Schema</span></span>](mschapv2userpropertiesv1schema-schema.md)
</dt> </dl>

 

 





