---
description: Используются для определения MAC-адреса, используемого для управления доступом к носителю.
ms.assetid: c1335127-a2d2-4f44-a895-1abbc5eaf98d
title: DOT11_MAC_ADDRESS (Windot11. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- kbSyntax
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 77b43635462c4b48890599512cc1a413461de72e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910659"
---
# <a name="dot11_mac_address"></a><span data-ttu-id="0091d-103">\_Mac- \_ адрес DOT11</span><span class="sxs-lookup"><span data-stu-id="0091d-103">DOT11\_MAC\_ADDRESS</span></span>

<span data-ttu-id="0091d-104">Типы **\_ Mac- \_ адресов DOT11** используются для определения MAC-адреса стандарта IEEE.</span><span class="sxs-lookup"><span data-stu-id="0091d-104">The **DOT11\_MAC\_ADDRESS** types are used to define an IEEE media access control (MAC) address.</span></span>


```C++
typedef UCHAR DOT11_MAC_ADDRESS[6];
typedef DOT11_MAC_ADDRESS* PDOT11_MAC_ADDRESS;
```



<dl> <dt>

<span data-ttu-id="0091d-105">**DOT11 \_ Mac- \_ адрес \[ 6\]**</span><span class="sxs-lookup"><span data-stu-id="0091d-105">**DOT11\_MAC\_ADDRESS\[6\]**</span></span>
</dt> <dd>

<span data-ttu-id="0091d-106">MAC-адрес в формате одноадресной рассылки, многоадресной рассылки или вещания.</span><span class="sxs-lookup"><span data-stu-id="0091d-106">A MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> <dt>

<span data-ttu-id="0091d-107">**PDOT11 \_ Mac- \_ адрес**</span><span class="sxs-lookup"><span data-stu-id="0091d-107">**PDOT11\_MAC\_ADDRESS**</span></span>
</dt> <dd>

<span data-ttu-id="0091d-108">Указатель на MAC-адрес в формате одноадресной рассылки, многоадресной рассылки или вещания.</span><span class="sxs-lookup"><span data-stu-id="0091d-108">Pointer to a MAC address in unicast, multicast, or broadcast format.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0091d-109">Требования</span><span class="sxs-lookup"><span data-stu-id="0091d-109">Requirements</span></span>



| <span data-ttu-id="0091d-110">Требование</span><span class="sxs-lookup"><span data-stu-id="0091d-110">Requirement</span></span> | <span data-ttu-id="0091d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="0091d-111">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0091d-112">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0091d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0091d-113">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0091d-113">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0091d-114">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0091d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0091d-115">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0091d-115">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="0091d-116">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="0091d-116">Redistributable</span></span><br/>          | <span data-ttu-id="0091d-117">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="0091d-117">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                        |
| <span data-ttu-id="0091d-118">Header</span><span class="sxs-lookup"><span data-stu-id="0091d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="0091d-119"><dt>Windot11. h (включение Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0091d-119"><dt>Windot11.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0091d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0091d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0091d-121">**DOT11 \_ BSSID, \_ список**</span><span class="sxs-lookup"><span data-stu-id="0091d-121">**DOT11\_BSSID\_LIST**</span></span>](dot11-bssid-list.md)
</dt> <dt>

[<span data-ttu-id="0091d-122">**\_атрибуты связи \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="0091d-122">**WLAN\_ASSOCIATION\_ATTRIBUTES**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_association_attributes)
</dt> <dt>

[<span data-ttu-id="0091d-123">**\_запись сети BSS \_**</span><span class="sxs-lookup"><span data-stu-id="0091d-123">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> </dl>

 

 




