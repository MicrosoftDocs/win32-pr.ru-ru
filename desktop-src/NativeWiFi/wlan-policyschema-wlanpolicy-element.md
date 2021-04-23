---
description: Содержит политику беспроводной локальной сети.
ms.assetid: 16ffb682-f88b-4ca1-a902-d2db5e347975
title: Вланполици, элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLANPolicy
api_type:
- Schema
api_location: ''
ms.openlocfilehash: ec26a3cab15014deabca4e9332c1fbef7a788b17
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155279"
---
# <a name="wlanpolicy-element"></a><span data-ttu-id="583f2-103">Вланполици, элемент</span><span class="sxs-lookup"><span data-stu-id="583f2-103">WLANPolicy Element</span></span>

<span data-ttu-id="583f2-104">Элемент **вланполици** содержит политику беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="583f2-104">The **WLANPolicy** element contains a wireless LAN policy.</span></span> <span data-ttu-id="583f2-105">Этот элемент является уникальным корневым элементом для профиля политики беспроводной связи.</span><span class="sxs-lookup"><span data-stu-id="583f2-105">This element is the unique root element for a wireless policy profile.</span></span>

<span data-ttu-id="583f2-106">Целевое пространство имен для элемента **вланполици** — `https://www.microsoft.com/networking/WLAN/policy/v1` .</span><span class="sxs-lookup"><span data-stu-id="583f2-106">The target namespace for the **WLANPolicy** element is `https://www.microsoft.com/networking/WLAN/policy/v1`.</span></span>

``` syntax
<xs:element name="WLANPolicy">
    <xs:complexType>
        <xs:sequence>
            <xs:element name="name"
                type="nameType"
             />
            <xs:element name="description"
                type="nameType"
                minOccurs="0"
             />
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
            <xs:element name="networkFilter"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:element name="allowList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
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
                        <xs:element name="blockList"
                            minOccurs="0"
                        >
                            <xs:complexType>
                                <xs:sequence>
                                    <xs:element name="network"
                                        type="networkItemType"
                                        maxOccurs="unbounded"
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
                        <xs:element name="denyAllIBSS"
                            type="boolean"
                            minOccurs="0"
                         />
                        <xs:element name="denyAllESS"
                            type="boolean"
                            minOccurs="0"
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
            <xs:element name="profileList"
                minOccurs="0"
            >
                <xs:complexType>
                    <xs:sequence>
                        <xs:any
                            processContents="lax"
                            maxOccurs="unbounded"
                            namespace="##other"
                         />
                    </xs:sequence>
                </xs:complexType>
            </xs:element>
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

## <a name="child-elements"></a><span data-ttu-id="583f2-107">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="583f2-107">Child elements</span></span>



| <span data-ttu-id="583f2-108">Элемент</span><span class="sxs-lookup"><span data-stu-id="583f2-108">Element</span></span>                                                                                                                    | <span data-ttu-id="583f2-109">Тип</span><span class="sxs-lookup"><span data-stu-id="583f2-109">Type</span></span>                                                                     | <span data-ttu-id="583f2-110">Описание</span><span class="sxs-lookup"><span data-stu-id="583f2-110">Description</span></span>                                                                                                                          |
|----------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="583f2-111">**алловеверйонетокреатеаллусерпрофилес**</span><span class="sxs-lookup"><span data-stu-id="583f2-111">**allowEveryoneToCreateAllUserProfiles**</span></span>](wlan-policyschema-alloweveryonetocreatealluserprofiles-globalflags-element.md) | <span data-ttu-id="583f2-112">Логическое</span><span class="sxs-lookup"><span data-stu-id="583f2-112">boolean</span></span>                                                                  | <span data-ttu-id="583f2-113">Указывает, может ли любой пользователь создать профиль для всех пользователей.</span><span class="sxs-lookup"><span data-stu-id="583f2-113">Specifies whether any user can create an all-user profile.</span></span> <br/>                                                               |
| [<span data-ttu-id="583f2-114">**Разрешенных**</span><span class="sxs-lookup"><span data-stu-id="583f2-114">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="583f2-115">Список беспроводных ЛОКАЛЬНЫХ сетей, к которым может подключаться любой компьютер.</span><span class="sxs-lookup"><span data-stu-id="583f2-115">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/>                                       |
| [<span data-ttu-id="583f2-116">**Списка блокировки**</span><span class="sxs-lookup"><span data-stu-id="583f2-116">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)                                                     |                                                                          | <span data-ttu-id="583f2-117">Список беспроводных ЛОКАЛЬНЫХ сетей, к которым компьютер не должен подключаться.</span><span class="sxs-lookup"><span data-stu-id="583f2-117">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>                                                    |
| [<span data-ttu-id="583f2-118">**деняллесс**</span><span class="sxs-lookup"><span data-stu-id="583f2-118">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)                                                   | <span data-ttu-id="583f2-119">Логическое</span><span class="sxs-lookup"><span data-stu-id="583f2-119">boolean</span></span>                                                                  | <span data-ttu-id="583f2-120">Указывает, заблокирован ли доступ ко всем сетям инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="583f2-120">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                                                           |
| [<span data-ttu-id="583f2-121">**деняллибсс**</span><span class="sxs-lookup"><span data-stu-id="583f2-121">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md)                                                 | <span data-ttu-id="583f2-122">Логическое</span><span class="sxs-lookup"><span data-stu-id="583f2-122">boolean</span></span>                                                                  | <span data-ttu-id="583f2-123">Указывает, заблокирован ли доступ ко всем компьютерным сетям.</span><span class="sxs-lookup"><span data-stu-id="583f2-123">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                                                                   |
| [<span data-ttu-id="583f2-124">**nописание**</span><span class="sxs-lookup"><span data-stu-id="583f2-124">**description**</span></span>](wlan-policyschema-description-wlanpolicy-element.md)                                                    | [<span data-ttu-id="583f2-125">**наметипе**</span><span class="sxs-lookup"><span data-stu-id="583f2-125">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="583f2-126">Описание политики беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="583f2-126">The description of a wireless LAN policy.</span></span> <br/>                                                                                |
| [<span data-ttu-id="583f2-127">**енаблеаутоконфиг**</span><span class="sxs-lookup"><span data-stu-id="583f2-127">**enableAutoConfig**</span></span>](wlan-policyschema-enableautoconfig-globalflags-element.md)                                         | <span data-ttu-id="583f2-128">Логическое</span><span class="sxs-lookup"><span data-stu-id="583f2-128">boolean</span></span>                                                                  | <span data-ttu-id="583f2-129">Указывает, используют ли компьютеры встроенную службу автоматической настройки (автоконфигурации) для управления беспроводными подключениями.</span><span class="sxs-lookup"><span data-stu-id="583f2-129">Specifies whether machines use the built-in automatic configuration (AutoConfig) service to manage wireless connections.</span></span> <br/> |
| [<span data-ttu-id="583f2-130">**глобалфлагс**</span><span class="sxs-lookup"><span data-stu-id="583f2-130">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="583f2-131">Содержит глобальные параметры для модуля автоматической настройки (ACM).</span><span class="sxs-lookup"><span data-stu-id="583f2-131">Contains the global settings for the Auto Configuration Module (ACM).</span></span> <br/>                                                    |
| [<span data-ttu-id="583f2-132">**безымян**</span><span class="sxs-lookup"><span data-stu-id="583f2-132">**name**</span></span>](wlan-policyschema-name-wlanpolicy-element.md)                                                                  | [<span data-ttu-id="583f2-133">**наметипе**</span><span class="sxs-lookup"><span data-stu-id="583f2-133">**nameType**</span></span>](wlan-policyschema-nametype-simpletype.md)                | <span data-ttu-id="583f2-134">Имя политики беспроводной локальной сети.</span><span class="sxs-lookup"><span data-stu-id="583f2-134">The name of a wireless LAN policy.</span></span> <br/>                                                                                       |
| [<span data-ttu-id="583f2-135">**сети**</span><span class="sxs-lookup"><span data-stu-id="583f2-135">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)                                                             | [<span data-ttu-id="583f2-136">**нетворкитемтипе**</span><span class="sxs-lookup"><span data-stu-id="583f2-136">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="583f2-137">Разрешенная сеть.</span><span class="sxs-lookup"><span data-stu-id="583f2-137">An allowed network.</span></span> <br/>                                                                                                      |
| [<span data-ttu-id="583f2-138">**сети**</span><span class="sxs-lookup"><span data-stu-id="583f2-138">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)                                                             | [<span data-ttu-id="583f2-139">**нетворкитемтипе**</span><span class="sxs-lookup"><span data-stu-id="583f2-139">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="583f2-140">Заблокированная сеть.</span><span class="sxs-lookup"><span data-stu-id="583f2-140">A blocked network.</span></span> <br/>                                                                                                       |
| [<span data-ttu-id="583f2-141">**нетворкфилтер**</span><span class="sxs-lookup"><span data-stu-id="583f2-141">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)                                                |                                                                          | <span data-ttu-id="583f2-142">Список разрешенных и запрещенных сетей.</span><span class="sxs-lookup"><span data-stu-id="583f2-142">The list of allowed and denied networks.</span></span><br/>                                                                                  |
| [<span data-ttu-id="583f2-143">**профилелист**</span><span class="sxs-lookup"><span data-stu-id="583f2-143">**profileList**</span></span>](wlan-policyschema-profilelist-wlanpolicy-element.md)                                                    |                                                                          | <span data-ttu-id="583f2-144">Содержит список профилей, применяемых на уровне домена или компьютера.</span><span class="sxs-lookup"><span data-stu-id="583f2-144">Contains a list of profiles to be applied at the domain or machine level.</span></span> <br/>                                                |
| [<span data-ttu-id="583f2-145">**шовдениеднетворк**</span><span class="sxs-lookup"><span data-stu-id="583f2-145">**showDeniedNetwork**</span></span>](wlan-policyschema-showdeniednetwork-globalflags-element.md)                                       | <span data-ttu-id="583f2-146">Логическое</span><span class="sxs-lookup"><span data-stu-id="583f2-146">boolean</span></span>                                                                  | <span data-ttu-id="583f2-147">Указывает, отображаются ли запрещенные сети в мастере **подключения к сети** .</span><span class="sxs-lookup"><span data-stu-id="583f2-147">Specifies whether denied networks appear in the **Connect to a Network** wizard.</span></span> <br/>                                         |



## <a name="remarks"></a><span data-ttu-id="583f2-148">Комментарии</span><span class="sxs-lookup"><span data-stu-id="583f2-148">Remarks</span></span>

<span data-ttu-id="583f2-149">Сведения о просмотре списка дочерних элементов в древовидной структуре см. в разделе [ \_ элементы схемы политики WLAN](wlan-policyschema-elements.md).</span><span class="sxs-lookup"><span data-stu-id="583f2-149">To view the list of child elements in a tree-like structure, see [WLAN\_policy Schema Elements](wlan-policyschema-elements.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="583f2-150">Требования</span><span class="sxs-lookup"><span data-stu-id="583f2-150">Requirements</span></span>



| <span data-ttu-id="583f2-151">Требование</span><span class="sxs-lookup"><span data-stu-id="583f2-151">Requirement</span></span> | <span data-ttu-id="583f2-152">Значение</span><span class="sxs-lookup"><span data-stu-id="583f2-152">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="583f2-153">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="583f2-153">Minimum supported client</span></span><br/> | <span data-ttu-id="583f2-154">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="583f2-154">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="583f2-155">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="583f2-155">Minimum supported server</span></span><br/> | <span data-ttu-id="583f2-156">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="583f2-156">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 




