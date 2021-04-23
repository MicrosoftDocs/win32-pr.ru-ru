---
description: Указывает список беспроводных ЛОКАЛЬНЫХ сетей, к которым может подключаться любой компьютер.
ms.assetid: e24557d8-dedf-4381-bba0-cdb7ea26083b
title: Разрешенных (Нетворкфилтер), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowList
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 5488f962a1ba526b34ca2d10144a150d7c1417d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682398"
---
# <a name="allowlist-networkfilter-element"></a><span data-ttu-id="c7587-103">Разрешенных (Нетворкфилтер), элемент</span><span class="sxs-lookup"><span data-stu-id="c7587-103">allowList (networkFilter) Element</span></span>

<span data-ttu-id="c7587-104">Элемент разрешенных (Нетворкфилтер) указывает список беспроводных ЛОКАЛЬНЫХ сетей, к которым может подключаться любой компьютер.</span><span class="sxs-lookup"><span data-stu-id="c7587-104">The allowList (networkFilter) element specifies the list of wireless LAN networks to which any machine must be allowed to connect.</span></span>

``` syntax
<xs:element name="allowList">
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

<span data-ttu-id="c7587-105">Элемент **разрешенных** определяется элементом [**нетворкфилтер**](wlan-policyschema-networkfilter-wlanpolicy-element.md) .</span><span class="sxs-lookup"><span data-stu-id="c7587-105">The **allowList** element is defined by the [**networkFilter**](wlan-policyschema-networkfilter-wlanpolicy-element.md) element.</span></span>

## <a name="child-elements"></a><span data-ttu-id="c7587-106">Дочерние элементы</span><span class="sxs-lookup"><span data-stu-id="c7587-106">Child elements</span></span>



| <span data-ttu-id="c7587-107">Элемент</span><span class="sxs-lookup"><span data-stu-id="c7587-107">Element</span></span>                                                        | <span data-ttu-id="c7587-108">Тип</span><span class="sxs-lookup"><span data-stu-id="c7587-108">Type</span></span>                                                                     | <span data-ttu-id="c7587-109">Описание</span><span class="sxs-lookup"><span data-stu-id="c7587-109">Description</span></span>                                              |
|----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="c7587-110">**сети**</span><span class="sxs-lookup"><span data-stu-id="c7587-110">**network**</span></span>](wlan-policyschema-network-allowlist-element.md) | [<span data-ttu-id="c7587-111">**нетворкитемтипе**</span><span class="sxs-lookup"><span data-stu-id="c7587-111">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md) | <span data-ttu-id="c7587-112">Сеть, к которой может подключаться компьютер.</span><span class="sxs-lookup"><span data-stu-id="c7587-112">The network to which the machine can connect.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="c7587-113">Требования</span><span class="sxs-lookup"><span data-stu-id="c7587-113">Requirements</span></span>



| <span data-ttu-id="c7587-114">Требование</span><span class="sxs-lookup"><span data-stu-id="c7587-114">Requirement</span></span> | <span data-ttu-id="c7587-115">Значение</span><span class="sxs-lookup"><span data-stu-id="c7587-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c7587-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="c7587-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c7587-117">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c7587-117">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c7587-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="c7587-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c7587-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c7587-119">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7587-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="c7587-120">See also</span></span>

<dl> <dt>

<span data-ttu-id="c7587-121">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="c7587-121">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="c7587-122">**нетворкфилтер**</span><span class="sxs-lookup"><span data-stu-id="c7587-122">**networkFilter**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="c7587-123">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="c7587-123">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="c7587-124">**Нетворкфилтер (Вланполици)**</span><span class="sxs-lookup"><span data-stu-id="c7587-124">**networkFilter (WLANPolicy)**</span></span>](wlan-policyschema-networkfilter-wlanpolicy-element.md)
</dt> </dl>

 

 




