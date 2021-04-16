---
description: Содержит глобальные параметры для модуля автоматической настройки (ACM).
ms.assetid: fb2b96d0-38cc-44fe-a82a-97e73b6a8f2a
title: Глобалфлагс (Вланполици), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- globalFlags
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 97d0b8ee90407efd94ac46cc1df6b084b9dcc54d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546815"
---
# <a name="globalflags-wlanpolicy-element"></a><span data-ttu-id="e6cc3-103">Глобалфлагс (Вланполици), элемент</span><span class="sxs-lookup"><span data-stu-id="e6cc3-103">globalFlags (WLANPolicy) Element</span></span>

<span data-ttu-id="e6cc3-104">Элемент Глобалфлагс (Вланполици) содержит глобальные параметры для модуля автоматической настройки (ACM).</span><span class="sxs-lookup"><span data-stu-id="e6cc3-104">The globalFlags (WLANPolicy) element contains the global settings for the Auto Configuration Module (ACM).</span></span> <span data-ttu-id="e6cc3-105">Этот элемент является обязательным.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-105">This element is mandatory.</span></span>

``` syntax
<xs:element name="globalFlags">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="enableAutoConfig"
                type="boolean"
             />
            <xs:element name="showDeniedNetwork"
                type="boolean"
             />
            <xs:element name="allowEveryoneToCreateAllUserProfiles"
                type="boolean"
             />
            <xs:any
                processContents="lax"
                minOccurs="0"
                maxOccurs="unbounded"
                namespace="##other"
             />
        </xs:sequence>
    </xs:complexType>
</xs:element>
```

<span data-ttu-id="e6cc3-106">Элемент **глобалфлагс** определяется элементом [**вланполици**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="e6cc3-106">The **globalFlags** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="e6cc3-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="e6cc3-107">Child elements</span></span>



| <span data-ttu-id="e6cc3-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="e6cc3-108">Element</span></span>                                                                                                                    | <span data-ttu-id="e6cc3-109">Тип</span><span class="sxs-lookup"><span data-stu-id="e6cc3-109">Type</span></span>    | <span data-ttu-id="e6cc3-110">Описание</span><span class="sxs-lookup"><span data-stu-id="e6cc3-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|---------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e6cc3-111">**алловеверйонетокреатеаллусерпрофилес**</span><span class="sxs-lookup"><span data-stu-id="e6cc3-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="e6cc3-112">Логическое</span><span class="sxs-lookup"><span data-stu-id="e6cc3-112">boolean</span></span> | <span data-ttu-id="e6cc3-113">Указывает, может ли любой пользователь создать профиль для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="e6cc3-114">**енаблеаутоконфиг**</span><span class="sxs-lookup"><span data-stu-id="e6cc3-114">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="e6cc3-115">Логическое</span><span class="sxs-lookup"><span data-stu-id="e6cc3-115">boolean</span></span> | <span data-ttu-id="e6cc3-116">Указывает, используют ли компьютеры встроенную службу автоматической настройки (автоконфигурации) для управления беспроводными подключениями.</span><span class="sxs-lookup"><span data-stu-id="e6cc3-116">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="e6cc3-117">**шовдениеднетворк**</span><span class="sxs-lookup"><span data-stu-id="e6cc3-117">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="e6cc3-118">Логическое</span><span class="sxs-lookup"><span data-stu-id="e6cc3-118">boolean</span></span> | <span data-ttu-id="e6cc3-119">Указывает, отображаются ли запрещенные сети в мастере **подключения к сети** .</span><span class="sxs-lookup"><span data-stu-id="e6cc3-119">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="requirements"></a><span data-ttu-id="e6cc3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="e6cc3-120">Requirements</span></span>



| <span data-ttu-id="e6cc3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="e6cc3-121">Requirement</span></span> | <span data-ttu-id="e6cc3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="e6cc3-122">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e6cc3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6cc3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6cc3-124">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="e6cc3-124">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e6cc3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6cc3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6cc3-126">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="e6cc3-126">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6cc3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6cc3-127">See also</span></span>

<dl> <dt>

<span data-ttu-id="e6cc3-128">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="e6cc3-128">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="e6cc3-129">**вланполици**</span><span class="sxs-lookup"><span data-stu-id="e6cc3-129">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="e6cc3-130">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="e6cc3-130">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="e6cc3-131">**вланполици**</span><span class="sxs-lookup"><span data-stu-id="e6cc3-131">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




