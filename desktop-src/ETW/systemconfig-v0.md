---
description: Этот класс является родительским классом для событий конфигурации оборудования. Следующий синтаксис упрощен из MOF-кода.
ms.assetid: 9da1a7ec-89b5-462b-a336-544e4b7adf96
title: Класс SystemConfig_V0
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SystemConfig_V0
api_type:
- NA
api_location: ''
ms.openlocfilehash: 92d77d1ad3effdd2bf22a7df8112187b27666238
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908868"
---
# <a name="systemconfig_v0-class"></a><span data-ttu-id="48b31-104">\_Класс системконфиг v0</span><span class="sxs-lookup"><span data-stu-id="48b31-104">SystemConfig\_V0 class</span></span>

<span data-ttu-id="48b31-105">Этот класс является родительским классом для событий конфигурации оборудования.</span><span class="sxs-lookup"><span data-stu-id="48b31-105">This class is the parent class for hardware configuration events.</span></span>

<span data-ttu-id="48b31-106">Следующий синтаксис упрощен из MOF-кода.</span><span class="sxs-lookup"><span data-stu-id="48b31-106">The following syntax is simplified from MOF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="48b31-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="48b31-107">Syntax</span></span>

``` syntax
[Guid("{01853a65-418f-4f36-aefc-dc0f1d2fd235}"), EventVersion(0)]
class SystemConfig_V0 : MSNT_SystemTrace
{
};
```

## <a name="members"></a><span data-ttu-id="48b31-108">Участники</span><span class="sxs-lookup"><span data-stu-id="48b31-108">Members</span></span>

<span data-ttu-id="48b31-109">Класс **системконфиг \_ v0** не определяет никаких членов.</span><span class="sxs-lookup"><span data-stu-id="48b31-109">The **SystemConfig\_V0** class does not define any members.</span></span>

## <a name="remarks"></a><span data-ttu-id="48b31-110">Примечания</span><span class="sxs-lookup"><span data-stu-id="48b31-110">Remarks</span></span>

<span data-ttu-id="48b31-111">Сведения о событиях конфигурации оборудования в Windows XP см. в разделе класс [**хвконфиг**](hwconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="48b31-111">For hardware configuration events on Windows XP, see the [**HWConfig**](hwconfig.md) class.</span></span>

## <a name="requirements"></a><span data-ttu-id="48b31-112">Требования</span><span class="sxs-lookup"><span data-stu-id="48b31-112">Requirements</span></span>



| <span data-ttu-id="48b31-113">Требование</span><span class="sxs-lookup"><span data-stu-id="48b31-113">Requirement</span></span> | <span data-ttu-id="48b31-114">Значение</span><span class="sxs-lookup"><span data-stu-id="48b31-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="48b31-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="48b31-115">Minimum supported client</span></span><br/> | <span data-ttu-id="48b31-116">Ни одна версия не поддерживается</span><span class="sxs-lookup"><span data-stu-id="48b31-116">None supported</span></span><br/>                            |
| <span data-ttu-id="48b31-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="48b31-117">Minimum supported server</span></span><br/> | <span data-ttu-id="48b31-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="48b31-118">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="48b31-119">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="48b31-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48b31-120">**МСНТ \_ системтраце**</span><span class="sxs-lookup"><span data-stu-id="48b31-120">**MSNT\_SystemTrace**</span></span>](msnt-systemtrace.md)
</dt> <dt>

[<span data-ttu-id="48b31-121">**системконфиг**</span><span class="sxs-lookup"><span data-stu-id="48b31-121">**SystemConfig**</span></span>](systemconfig.md)
</dt> <dt>

[<span data-ttu-id="48b31-122">**\_ЦП системконфиг v0 \_**</span><span class="sxs-lookup"><span data-stu-id="48b31-122">**SystemConfig\_V0\_CPU**</span></span>](systemconfig-v0-cpu.md)
</dt> <dt>

[<span data-ttu-id="48b31-123">**Системконфиг \_ v0 \_ логдиск**</span><span class="sxs-lookup"><span data-stu-id="48b31-123">**SystemConfig\_V0\_LogDisk**</span></span>](systemconfig-v0-logdisk.md)
</dt> <dt>

[<span data-ttu-id="48b31-124">**\_ \_ Сетевой адаптер системконфиг v0**</span><span class="sxs-lookup"><span data-stu-id="48b31-124">**SystemConfig\_V0\_NIC**</span></span>](systemconfig-v0-nic.md)
</dt> <dt>

[<span data-ttu-id="48b31-125">**Системконфиг \_ v0 \_ фидиск**</span><span class="sxs-lookup"><span data-stu-id="48b31-125">**SystemConfig\_V0\_PhyDisk**</span></span>](systemconfig-v0-phydisk.md)
</dt> <dt>

[<span data-ttu-id="48b31-126">**Системконфиг \_ v0 \_**</span><span class="sxs-lookup"><span data-stu-id="48b31-126">**SystemConfig\_V0\_Power**</span></span>](systemconfig-v0-power.md)
</dt> <dt>

[<span data-ttu-id="48b31-127">**Системконфиг \_ v0 \_ Services**</span><span class="sxs-lookup"><span data-stu-id="48b31-127">**SystemConfig\_V0\_Services**</span></span>](systemconfig-v0-services.md)
</dt> <dt>

[<span data-ttu-id="48b31-128">**\_Видео системконфиг v0 \_**</span><span class="sxs-lookup"><span data-stu-id="48b31-128">**SystemConfig\_V0\_Video**</span></span>](systemconfig-v0-video.md)
</dt> </dl>

 

 




