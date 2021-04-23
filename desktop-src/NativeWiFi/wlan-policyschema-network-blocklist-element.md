---
description: Определяет Заблокированную сеть.
ms.assetid: ccf24d45-cae0-4eb7-951a-004a5f71e04a
title: Элемент Network (списка блокировки)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- network
api_type:
- Schema
api_location: ''
ms.openlocfilehash: f58948573db281aacb00e227ff0fbc2f1cdf82b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674294"
---
# <a name="network-blocklist-element"></a><span data-ttu-id="55ae4-103">Элемент Network (списка блокировки)</span><span class="sxs-lookup"><span data-stu-id="55ae4-103">network (blockList) Element</span></span>

<span data-ttu-id="55ae4-104">Элемент Network (списка блокировки) определяет Заблокированную сеть.</span><span class="sxs-lookup"><span data-stu-id="55ae4-104">The network (blockList) element defines a blocked network.</span></span> <span data-ttu-id="55ae4-105">Компьютеру не удается подключиться к заблокированной сети.</span><span class="sxs-lookup"><span data-stu-id="55ae4-105">A machine cannot connect to a blocked network.</span></span>

``` syntax
<xs:element name="network"
    type="networkItemType"
 />
```

<span data-ttu-id="55ae4-106">Элемент **Network** определяется элементом [**списка блокировки**](wlan-policyschema-blocklist-networkfilter-element.md) .</span><span class="sxs-lookup"><span data-stu-id="55ae4-106">The **network** element is defined by the [**blockList**](wlan-policyschema-blocklist-networkfilter-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="55ae4-107">Требования</span><span class="sxs-lookup"><span data-stu-id="55ae4-107">Requirements</span></span>



| <span data-ttu-id="55ae4-108">Требование</span><span class="sxs-lookup"><span data-stu-id="55ae4-108">Requirement</span></span> | <span data-ttu-id="55ae4-109">Значение</span><span class="sxs-lookup"><span data-stu-id="55ae4-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="55ae4-110">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="55ae4-110">Minimum supported client</span></span><br/> | <span data-ttu-id="55ae4-111">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="55ae4-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="55ae4-112">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="55ae4-112">Minimum supported server</span></span><br/> | <span data-ttu-id="55ae4-113">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="55ae4-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="55ae4-114">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="55ae4-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="55ae4-115">**Контекст определения элемента в схеме**</span><span class="sxs-lookup"><span data-stu-id="55ae4-115">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="55ae4-116">**Списка блокировки**</span><span class="sxs-lookup"><span data-stu-id="55ae4-116">**blockList**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> <dt>

<span data-ttu-id="55ae4-117">**Возможный непосредственный родительский элемент в экземпляре схемы**</span><span class="sxs-lookup"><span data-stu-id="55ae4-117">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="55ae4-118">**Списка блокировки (Нетворкфилтер)**</span><span class="sxs-lookup"><span data-stu-id="55ae4-118">**blockList (networkFilter)**</span></span>](wlan-policyschema-blocklist-networkfilter-element.md)
</dt> </dl>

 

 




