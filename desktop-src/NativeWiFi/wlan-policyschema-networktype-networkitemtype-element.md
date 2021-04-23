---
description: Указывает тип сети.
ms.assetid: fe3044ab-6e93-48f8-b8cb-fdf984987232
title: Нетворктипе (Нетворкитемтипе), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkType
api_type:
- Schema
api_location: ''
ms.openlocfilehash: c63b8afdaf699fde6871c198a8235772c59da1ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674214"
---
# <a name="networktype-networkitemtype-element"></a><span data-ttu-id="fe006-103">Нетворктипе (Нетворкитемтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="fe006-103">networkType (networkItemType) Element</span></span>

<span data-ttu-id="fe006-104">Элемент Нетворктипе (Нетворкитемтипе) указывает тип сети.</span><span class="sxs-lookup"><span data-stu-id="fe006-104">The networkType (networkItemType) element specifies a network type.</span></span> <span data-ttu-id="fe006-105">Существует два типа сетей: сети инфраструктуры (ESS) и ad-hoc Network (ИБСС).</span><span class="sxs-lookup"><span data-stu-id="fe006-105">There are two types of networks: infrastructure networks (ESS) and ad-hoc networks (IBSS).</span></span>

``` syntax
<xs:element name="networkType"
    type="networkTypeType"
 />
```

<span data-ttu-id="fe006-106">Элемент **нетворктипе** определяется сложным типом [**нетворкитемтипе**](wlan-policyschema-networkitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="fe006-106">The **networkType** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe006-107">Требования</span><span class="sxs-lookup"><span data-stu-id="fe006-107">Requirements</span></span>



| <span data-ttu-id="fe006-108">Требование</span><span class="sxs-lookup"><span data-stu-id="fe006-108">Requirement</span></span> | <span data-ttu-id="fe006-109">Значение</span><span class="sxs-lookup"><span data-stu-id="fe006-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fe006-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fe006-110">Minimum supported client</span></span><br/> | <span data-ttu-id="fe006-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="fe006-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="fe006-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fe006-112">Minimum supported server</span></span><br/> | <span data-ttu-id="fe006-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="fe006-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fe006-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fe006-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="fe006-115">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="fe006-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="fe006-116">**нетворкитемтипе**</span><span class="sxs-lookup"><span data-stu-id="fe006-116">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="fe006-117">**Возможные непосредственные родительские элементы в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="fe006-117">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="fe006-118">**сеть (разрешенных)**</span><span class="sxs-lookup"><span data-stu-id="fe006-118">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="fe006-119">**сеть (списка блокировки)**</span><span class="sxs-lookup"><span data-stu-id="fe006-119">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




