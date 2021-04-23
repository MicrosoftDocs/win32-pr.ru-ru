---
description: Указывает список беспроводных ЛОКАЛЬНЫХ сетей, к которым компьютер не должен подключаться.
ms.assetid: 01db3f7e-1e27-4378-9c42-bc38192f9507
title: Списка блокировки (Нетворкфилтер), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- blockList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: e852286d00d93904bd185fef6c2f3444bb5987f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990866"
---
# <a name="blocklist-networkfilter-element"></a><span data-ttu-id="3675f-103">Списка блокировки (Нетворкфилтер), элемент</span><span class="sxs-lookup"><span data-stu-id="3675f-103">blockList (networkFilter) Element</span></span>

<span data-ttu-id="3675f-104">Элемент списка блокировки (Нетворкфилтер) указывает список беспроводных ЛОКАЛЬНЫХ сетей, к которым компьютер не должен подключаться.</span><span class="sxs-lookup"><span data-stu-id="3675f-104">The blockList (networkFilter) element specifies the list of wireless LAN networks to which a machine must not connect.</span></span>

``` syntax
<xs:element name="blockList">
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
```

<span data-ttu-id="3675f-105">Элемент **списка блокировки** определяется элементом [**нетворкфилтер**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="3675f-105">The **blockList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="3675f-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="3675f-106">Child elements</span></span>



| <span data-ttu-id="3675f-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="3675f-107">Element</span></span>                                                        | <span data-ttu-id="3675f-108">Тип</span><span class="sxs-lookup"><span data-stu-id="3675f-108">Type</span></span>                                                                     | <span data-ttu-id="3675f-109">Описание</span><span class="sxs-lookup"><span data-stu-id="3675f-109">Description</span></span>                      |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------|
| [<span data-ttu-id="3675f-110">**сети**</span><span class="sxs-lookup"><span data-stu-id="3675f-110">**network**</span></span>](wlan-policyschema-network-blocklist-element.md) | [<span data-ttu-id="3675f-111">**нетворкитемтипе**</span><span class="sxs-lookup"><span data-stu-id="3675f-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="3675f-112">Заблокированная сеть.</span><span class="sxs-lookup"><span data-stu-id="3675f-112">The blocked network.</span></span> <br/> |



## <a name="requirements"></a><span data-ttu-id="3675f-113">Требования</span><span class="sxs-lookup"><span data-stu-id="3675f-113">Requirements</span></span>



| <span data-ttu-id="3675f-114">Требование</span><span class="sxs-lookup"><span data-stu-id="3675f-114">Requirement</span></span> | <span data-ttu-id="3675f-115">Значение</span><span class="sxs-lookup"><span data-stu-id="3675f-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3675f-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3675f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3675f-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3675f-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3675f-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3675f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3675f-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3675f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3675f-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3675f-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="3675f-121">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="3675f-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="3675f-122">**нетворкфилтер**</span><span class="sxs-lookup"><span data-stu-id="3675f-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="3675f-123">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="3675f-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="3675f-124">**Нетворкфилтер (Вланполици)**</span><span class="sxs-lookup"><span data-stu-id="3675f-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




