---
description: Определяет тип сети "базовый набор служб (BSS)".
ms.assetid: 13d57339-655e-4978-974e-e7b12a83d18a
title: Перечисление DOT11_BSS_TYPE (Влантипес. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DOT11_BSS_TYPE
api_type:
- HeaderDef
api_location:
- wlantypes.h
ms.openlocfilehash: 7815e75f3ef7ef8d908b7d2b26f2e5f9d3630009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105673922"
---
# <a name="dot11_bss_type-enumeration"></a><span data-ttu-id="ce131-103">\_ \_ Перечисление типов BSS DOT11</span><span class="sxs-lookup"><span data-stu-id="ce131-103">DOT11\_BSS\_TYPE enumeration</span></span>

<span data-ttu-id="ce131-104">Тип **перечисления \_ DOT11 \_ BSS** определяет тип сети "базовый набор служб (BSS)".</span><span class="sxs-lookup"><span data-stu-id="ce131-104">The **DOT11\_BSS\_TYPE** enumerated type defines a basic service set (BSS) network type.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce131-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ce131-105">Syntax</span></span>


```C++
typedef enum _DOT11_BSS_TYPE { 
  dot11_BSS_type_infrastructure  = 1,
  dot11_BSS_type_independent     = 2,
  dot11_BSS_type_any             = 3
} DOT11_BSS_TYPE, *PDOT11_BSS_TYPE;
```



## <a name="constants"></a><span data-ttu-id="ce131-106">Константы</span><span class="sxs-lookup"><span data-stu-id="ce131-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ce131-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**\_ \_ инфраструктура типов Dot11 \_ BSS**</span><span class="sxs-lookup"><span data-stu-id="ce131-107"><span id="dot11_BSS_type_infrastructure"></span><span id="dot11_bss_type_infrastructure"></span><span id="DOT11_BSS_TYPE_INFRASTRUCTURE"></span>**dot11\_BSS\_type\_infrastructure**</span></span>
</dt> <dd>

<span data-ttu-id="ce131-108">Указывает сеть BSS инфраструктуры.</span><span class="sxs-lookup"><span data-stu-id="ce131-108">Specifies an infrastructure BSS network.</span></span>

</dd> <dt>

<span data-ttu-id="ce131-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**\_тип Dot11 BSS не \_ \_ зависит**</span><span class="sxs-lookup"><span data-stu-id="ce131-109"><span id="dot11_BSS_type_independent"></span><span id="dot11_bss_type_independent"></span><span id="DOT11_BSS_TYPE_INDEPENDENT"></span>**dot11\_BSS\_type\_independent**</span></span>
</dt> <dd>

<span data-ttu-id="ce131-110">Указывает независимую сеть BSS (ИБСС).</span><span class="sxs-lookup"><span data-stu-id="ce131-110">Specifies an independent BSS (IBSS) network.</span></span>

</dd> <dt>

<span data-ttu-id="ce131-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**\_тип Dot11 \_ BSS \_ ANY**</span><span class="sxs-lookup"><span data-stu-id="ce131-111"><span id="dot11_BSS_type_any"></span><span id="dot11_bss_type_any"></span><span id="DOT11_BSS_TYPE_ANY"></span>**dot11\_BSS\_type\_any**</span></span>
</dt> <dd>

<span data-ttu-id="ce131-112">Указывает либо инфраструктуру, либо ИБСС сеть.</span><span class="sxs-lookup"><span data-stu-id="ce131-112">Specifies either infrastructure or IBSS network.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ce131-113">Требования</span><span class="sxs-lookup"><span data-stu-id="ce131-113">Requirements</span></span>



| <span data-ttu-id="ce131-114">Требование</span><span class="sxs-lookup"><span data-stu-id="ce131-114">Requirement</span></span> | <span data-ttu-id="ce131-115">Значение</span><span class="sxs-lookup"><span data-stu-id="ce131-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce131-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ce131-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ce131-117">Windows Vista, Windows XP с пакетом обновления 3 (SP3), \[ только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ce131-117">Windows Vista, Windows XP with SP3 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ce131-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ce131-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ce131-119">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ce131-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                        |
| <span data-ttu-id="ce131-120">Распространяемые компоненты</span><span class="sxs-lookup"><span data-stu-id="ce131-120">Redistributable</span></span><br/>          | <span data-ttu-id="ce131-121">Интерфейс API беспроводной локальной сети для Windows XP с пакетом обновления 2 (SP2)</span><span class="sxs-lookup"><span data-stu-id="ce131-121">Wireless LAN API for Windows XP with SP2</span></span><br/>                                                         |
| <span data-ttu-id="ce131-122">Header</span><span class="sxs-lookup"><span data-stu-id="ce131-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce131-123"><dt>Влантипес. h (включение Windot11. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ce131-123"><dt>Wlantypes.h (include Windot11.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ce131-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ce131-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce131-125">**\_запись сети BSS \_**</span><span class="sxs-lookup"><span data-stu-id="ce131-125">**WLAN\_BSS\_ENTRY**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_bss_entry)
</dt> <dt>

[<span data-ttu-id="ce131-126">**\_Параметры подключения \_ WLAN**</span><span class="sxs-lookup"><span data-stu-id="ce131-126">**WLAN\_CONNECTION\_PARAMETERS**</span></span>](/windows/desktop/api/wlanapi/ns-wlanapi-wlan_connection_parameters)
</dt> <dt>

[<span data-ttu-id="ce131-127">**вланжетнетворкбсслист**</span><span class="sxs-lookup"><span data-stu-id="ce131-127">**WlanGetNetworkBssList**</span></span>](/windows/desktop/api/Wlanapi/nf-wlanapi-wlangetnetworkbsslist)
</dt> </dl>

 

 




