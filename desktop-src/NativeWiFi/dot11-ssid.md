---
description: Содержит идентификатор SSID интерфейса.
ms.assetid: f2b15ef9-99ee-4505-8575-224112024d7a
title: Структура DOT11_SSID (Влантипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_SSID
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: e319d22db33a627be631f9b6b0ee36591bc7a5bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910651"
---
# <a name="dot11_ssid-structure"></a><span data-ttu-id="ead41-103">\_Структура SSID по идентификатору DOT11</span><span class="sxs-lookup"><span data-stu-id="ead41-103">DOT11\_SSID structure</span></span>

<span data-ttu-id="ead41-104">Структура **\_ SSID DOT11** содержит идентификатор SSID интерфейса.</span><span class="sxs-lookup"><span data-stu-id="ead41-104">A **DOT11\_SSID** structure contains the SSID of an interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="ead41-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ead41-105">Syntax</span></span>


```C++
typedef struct _DOT11_SSID {
  ULONG uSSIDLength;
  UCHAR ucSSID[DOT11_SSID_MAX_LENGTH];
} DOT11_SSID, *PDOT11_SSID;
```



## <a name="members"></a><span data-ttu-id="ead41-106">Члены</span><span class="sxs-lookup"><span data-stu-id="ead41-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="ead41-107">**уссидленгс**</span><span class="sxs-lookup"><span data-stu-id="ead41-107">**uSSIDLength**</span></span>
</dt> <dd>

<span data-ttu-id="ead41-108">Длина массива **укссид** в байтах.</span><span class="sxs-lookup"><span data-stu-id="ead41-108">The length, in bytes, of the **ucSSID** array.</span></span>

</dd> <dt>

<span data-ttu-id="ead41-109">**укссид**</span><span class="sxs-lookup"><span data-stu-id="ead41-109">**ucSSID**</span></span>
</dt> <dd>

<span data-ttu-id="ead41-110">Идентификатор SSID.</span><span class="sxs-lookup"><span data-stu-id="ead41-110">The SSID.</span></span> <span data-ttu-id="ead41-111">\_Максимальная длина DOT11 SSID равна \_ \_ 32.</span><span class="sxs-lookup"><span data-stu-id="ead41-111">DOT11\_SSID\_MAX\_LENGTH is set to 32.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ead41-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ead41-112">Remarks</span></span>

<span data-ttu-id="ead41-113">Идентификатор SSID, заданный членом **укссид** , не является строкой ASCII, завершающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="ead41-113">The SSID that is specified by the **ucSSID** member is not a null-terminated ASCII string.</span></span> <span data-ttu-id="ead41-114">Длина идентификатора SSID определяется членом **уссидленгс** .</span><span class="sxs-lookup"><span data-stu-id="ead41-114">The length of the SSID is determined by the **uSSIDLength** member.</span></span>

<span data-ttu-id="ead41-115">Подстановочный знак SSID — это идентификатор SSID, для элемента **уссидленгс** которого установлено значение 0.</span><span class="sxs-lookup"><span data-stu-id="ead41-115">A wildcard SSID is an SSID whose **uSSIDLength** member is set to zero.</span></span> <span data-ttu-id="ead41-116">Если для нужного идентификатора SSID задан подстановочный знак SSID, станция 802,11 может подключаться к любой сети "базовый набор служб (BSS)".</span><span class="sxs-lookup"><span data-stu-id="ead41-116">When the desired SSID is set to the wildcard SSID, the 802.11 station can connect to any basic service set (BSS) network.</span></span>

## <a name="requirements"></a><span data-ttu-id="ead41-117">Требования</span><span class="sxs-lookup"><span data-stu-id="ead41-117">Requirements</span></span>



| <span data-ttu-id="ead41-118">Требование</span><span class="sxs-lookup"><span data-stu-id="ead41-118">Requirement</span></span> | <span data-ttu-id="ead41-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ead41-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ead41-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ead41-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ead41-121">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ead41-121">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ead41-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ead41-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ead41-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ead41-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="ead41-124">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="ead41-124">Redistributable</span></span><br/>          | <span data-ttu-id="ead41-125">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ead41-125">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="ead41-126">Header</span><span class="sxs-lookup"><span data-stu-id="ead41-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ead41-127"><dt>Влантипес. h (включение Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ead41-127"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ead41-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ead41-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ead41-129">**\_Параметры подключения \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="ead41-129">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[<span data-ttu-id="ead41-130">**вланжетнетворкбсслист**</span><span class="sxs-lookup"><span data-stu-id="ead41-130">**WlanGetNetworkBssList**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> <dt>

[<span data-ttu-id="ead41-131">**вланскан**</span><span class="sxs-lookup"><span data-stu-id="ead41-131">**WlanScan**</span></span>](/windows/desktop/api/wlanapi/nf-wlanapi-wlanscan)
</dt> </dl>

 

 




