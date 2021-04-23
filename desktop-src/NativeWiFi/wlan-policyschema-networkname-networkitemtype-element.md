---
description: Указывает идентификатор набора служб (SSID) беспроводной сети.
ms.assetid: 103808f2-9e5f-4605-b42a-337a13455294
title: networkName (Нетворкитемтипе), элемент
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- networkName
api_type:
- Schema
api_location: ''
ms.openlocfilehash: da635c392a29419e7b151cc2c4fb080ff7d3fca9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912527"
---
# <a name="networkname-networkitemtype-element"></a><span data-ttu-id="a8961-103">networkName (Нетворкитемтипе), элемент</span><span class="sxs-lookup"><span data-stu-id="a8961-103">networkName (networkItemType) Element</span></span>

<span data-ttu-id="a8961-104">Элемент networkName (Нетворкитемтипе) указывает идентификатор набора служб (SSID) беспроводной сети.</span><span class="sxs-lookup"><span data-stu-id="a8961-104">The networkName (networkItemType) element specifies the service set identifier (SSID) of a wireless network.</span></span>

``` syntax
<xs:element name="networkName"
    type="networkNameType"
 />
```

<span data-ttu-id="a8961-105">Элемент **networkName** определяется сложным типом [**нетворкитемтипе**](wlan-policyschema-networkitemtype-complextype.md) .</span><span class="sxs-lookup"><span data-stu-id="a8961-105">The **networkName** element is defined by the [**networkItemType**](wlan-policyschema-networkitemtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="a8961-106">Требования</span><span class="sxs-lookup"><span data-stu-id="a8961-106">Requirements</span></span>



| <span data-ttu-id="a8961-107">Требование</span><span class="sxs-lookup"><span data-stu-id="a8961-107">Requirement</span></span> | <span data-ttu-id="a8961-108">Значение</span><span class="sxs-lookup"><span data-stu-id="a8961-108">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a8961-109">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a8961-109">Minimum supported client</span></span><br/> | <span data-ttu-id="a8961-110">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a8961-110">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a8961-111">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a8961-111">Minimum supported server</span></span><br/> | <span data-ttu-id="a8961-112">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a8961-112">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8961-113">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a8961-113">See also</span></span>

<dl> <dt>

<span data-ttu-id="a8961-114">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="a8961-114">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="a8961-115">**нетворкитемтипе**</span><span class="sxs-lookup"><span data-stu-id="a8961-115">**networkItemType**</span></span>](wlan-policyschema-networkitemtype-complextype.md)
</dt> <dt>

<span data-ttu-id="a8961-116">**Возможные непосредственные родительские элементы в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="a8961-116">**Possible immediate parent elements in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="a8961-117">**сеть (разрешенных)**</span><span class="sxs-lookup"><span data-stu-id="a8961-117">**network (allowList)**</span></span>](wlan-policyschema-network-allowlist-element.md)
</dt> <dt>

[<span data-ttu-id="a8961-118">**сеть (списка блокировки)**</span><span class="sxs-lookup"><span data-stu-id="a8961-118">**network (blockList)**</span></span>](wlan-policyschema-network-blocklist-element.md)
</dt> </dl>

 

 




