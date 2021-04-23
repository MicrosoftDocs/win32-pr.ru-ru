---
description: Определяет список разрешенных и запрещенных сетей для компьютеров.
ms.assetid: 21502c97-36a4-4cd6-9dd0-ee44c4cc522f
title: Нетворкфилтер (Вланполици), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkFilter
api_type:
- Schema
api_location: ''
ms.openlocfilehash: d78a23ba1a456f1ad45745fcc25580c27de148c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684234"
---
# <a name="networkfilter-wlanpolicy-element"></a><span data-ttu-id="8a2c5-103">Нетворкфилтер (Вланполици), элемент</span><span class="sxs-lookup"><span data-stu-id="8a2c5-103">networkFilter (WLANPolicy) Element</span></span>

<span data-ttu-id="8a2c5-104">Элемент Нетворкфилтер (Вланполици) определяет список разрешенных и запрещенных сетей для компьютеров.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-104">The networkFilter (WLANPolicy) element defines the list of allowed and denied networks for machines.</span></span>

``` syntax
<xs:element name="networkFilter">
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
```

<span data-ttu-id="8a2c5-105">Элемент **нетворкфилтер** определяется элементом [**вланполици**](wlan-policyschema-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="8a2c5-105">The **networkFilter** element is defined by the [**WLANPolicy**](wlan-policyschema-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="8a2c5-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="8a2c5-106">Child elements</span></span>



| <span data-ttu-id="8a2c5-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="8a2c5-107">Element</span></span>                                                                    | <span data-ttu-id="8a2c5-108">Тип</span><span class="sxs-lookup"><span data-stu-id="8a2c5-108">Type</span></span>                                                                     | <span data-ttu-id="8a2c5-109">Описание</span><span class="sxs-lookup"><span data-stu-id="8a2c5-109">Description</span></span>                                                                                    |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8a2c5-110">**Разрешенных**</span><span class="sxs-lookup"><span data-stu-id="8a2c5-110">**allowList**</span></span>](wlan-policyschema-allowlist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="8a2c5-111">Список беспроводных ЛОКАЛЬНЫХ сетей, к которым может подключаться любой компьютер.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-111">The list of wireless LAN networks to which any machine must be allowed to connect.</span></span> <br/> |
| [<span data-ttu-id="8a2c5-112">**Списка блокировки**</span><span class="sxs-lookup"><span data-stu-id="8a2c5-112">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)     |                                                                          | <span data-ttu-id="8a2c5-113">Список беспроводных ЛОКАЛЬНЫХ сетей, к которым компьютер не должен подключаться.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-113">The list of wireless LAN networks to which a machine must not connect.</span></span><br/>              |
| [<span data-ttu-id="8a2c5-114">**деняллесс**</span><span class="sxs-lookup"><span data-stu-id="8a2c5-114">**denyAllESS**</span></span>](wlan-policyschema-denyalless-networkfilter-element.md)   | <span data-ttu-id="8a2c5-115">Логическое</span><span class="sxs-lookup"><span data-stu-id="8a2c5-115">boolean</span></span>                                                                  | <span data-ttu-id="8a2c5-116">Указывает, заблокирован ли доступ ко всем сетям инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-116">Specifies if access to all infrastructure networks is blocked.</span></span> <br/>                     |
| [<span data-ttu-id="8a2c5-117">**деняллибсс**</span><span class="sxs-lookup"><span data-stu-id="8a2c5-117">**denyAllIBSS**</span></span>](wlan-policyschema-denyallibss-networkfilter-element.md) | <span data-ttu-id="8a2c5-118">Логическое</span><span class="sxs-lookup"><span data-stu-id="8a2c5-118">boolean</span></span>                                                                  | <span data-ttu-id="8a2c5-119">Указывает, заблокирован ли доступ ко всем компьютерным сетям.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-119">Specifies if access to all ad-hoc networks is blocked.</span></span> <br/>                             |
| [<span data-ttu-id="8a2c5-120">**сети**</span><span class="sxs-lookup"><span data-stu-id="8a2c5-120">**network**</span></span>](wlan-policyschema-network-allowlist-element.md)             | [<span data-ttu-id="8a2c5-121">**нетворкитемтипе**</span><span class="sxs-lookup"><span data-stu-id="8a2c5-121">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="8a2c5-122">Разрешенная сеть.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-122">An allowed network.</span></span> <br/>                                                                |
| [<span data-ttu-id="8a2c5-123">**сети**</span><span class="sxs-lookup"><span data-stu-id="8a2c5-123">**network**</span></span>](wlan-policyschema-network-blocklist-element.md)             | [<span data-ttu-id="8a2c5-124">**нетворкитемтипе**</span><span class="sxs-lookup"><span data-stu-id="8a2c5-124">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="8a2c5-125">Заблокированная сеть.</span><span class="sxs-lookup"><span data-stu-id="8a2c5-125">A blocked network.</span></span> <br/>                                                                 |



## <a name="requirements"></a><span data-ttu-id="8a2c5-126">Требования</span><span class="sxs-lookup"><span data-stu-id="8a2c5-126">Requirements</span></span>



| <span data-ttu-id="8a2c5-127">Требование</span><span class="sxs-lookup"><span data-stu-id="8a2c5-127">Requirement</span></span> | <span data-ttu-id="8a2c5-128">Значение</span><span class="sxs-lookup"><span data-stu-id="8a2c5-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8a2c5-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8a2c5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8a2c5-130">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="8a2c5-130">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8a2c5-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8a2c5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8a2c5-132">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="8a2c5-132">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8a2c5-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8a2c5-133">See also</span></span>

<dl> <dt>

<span data-ttu-id="8a2c5-134">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="8a2c5-134">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="8a2c5-135">**вланполици**</span><span class="sxs-lookup"><span data-stu-id="8a2c5-135">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="8a2c5-136">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="8a2c5-136">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="8a2c5-137">**вланполици**</span><span class="sxs-lookup"><span data-stu-id="8a2c5-137">**WLANPolicy**</span></span>](wlan-policyschema-wlanpolicy-element.md)
</dt> </dl>

 

 




