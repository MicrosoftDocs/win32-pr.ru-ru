---
description: Описывает режимы защищенного режима (S) для устройства Windows.
ms.assetid: CE50AC56-0295-477C-93CB-ABAB92482A59
title: Перечисление WLDP_WINDOWS_LOCKDOWN_MODE (Wldp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_WINDOWS_LOCKDOWN_MODE
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: 438a44bec0745ea67b2b40c3f8aa9c0dd6bd0072
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105657936"
---
# <a name="wldp_windows_lockdown_mode-enumeration"></a><span data-ttu-id="0ee6f-103">\_ \_ Перечисление в режиме блокировки Windows \_ WLDP</span><span class="sxs-lookup"><span data-stu-id="0ee6f-103">WLDP\_WINDOWS\_LOCKDOWN\_MODE enumeration</span></span>

<span data-ttu-id="0ee6f-104">Описывает режимы защищенного режима (S) для устройства Windows.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-104">Describes the secure modes (S modes) for a Windows device.</span></span> <span data-ttu-id="0ee6f-105">Используется в основном в [**влдпкуеривиндовслоккдовнмоде**](wldpquerywindowslockdownmode.md).</span><span class="sxs-lookup"><span data-stu-id="0ee6f-105">Used primarily in [**WldpQueryWindowsLockdownMode**](wldpquerywindowslockdownmode.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee6f-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ee6f-106">Syntax</span></span>


```C++
typedef enum _WLDP_WINDOWS_LOCKDOWN_MODE { 
  WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED  = 0,
  WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL     = 1,
  WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED    = 2,
  WLDP_WINDOWS_LOCKDOWN_MODE_MAX       = 3
} WLDP_WINDOWS_LOCKDOWN_MODE, *PWLDP_WINDOWS_LOCKDOWN_MODE;
```



## <a name="constants"></a><span data-ttu-id="0ee6f-107">Константы</span><span class="sxs-lookup"><span data-stu-id="0ee6f-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0ee6f-108"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**WLDP \_ \_ режим блокировки \_ Windows \_ разблокирован**</span><span class="sxs-lookup"><span data-stu-id="0ee6f-108"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_UNLOCKED"></span><span id="wldp_windows_lockdown_mode_unlocked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_UNLOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="0ee6f-109">Разблокирован.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-109">Unlocked.</span></span> <span data-ttu-id="0ee6f-110">Используется в основном для устройств Windows без режима S.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-110">Used primarily for Windows devices without the S mode.</span></span>

</dd> <dt>

<span data-ttu-id="0ee6f-111"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**\_ \_ \_ \_ пробная версия режима блокировки Windows WLDP**</span><span class="sxs-lookup"><span data-stu-id="0ee6f-111"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_TRIAL"></span><span id="wldp_windows_lockdown_mode_trial"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_TRIAL**</span></span>
</dt> <dd>

<span data-ttu-id="0ee6f-112">ПК.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-112">Trial.</span></span> <span data-ttu-id="0ee6f-113">Используется в основном для пробного устройства Windows 10 с режимом S.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-113">Used primarily for a Windows 10 trial device with the S mode.</span></span> <span data-ttu-id="0ee6f-114">Режим пробной версии — особый случай для устройств Windows 10 с режимом S: политики применяются принудительно, но защита от отката для принудительной установки политики отсутствует.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-114">Trial mode is a special case for Windows 10 devices with the S mode: policies are enforced, but there is no anti-rollback protection for the enforcement of the policy.</span></span>

</dd> <dt>

<span data-ttu-id="0ee6f-115"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP \_ \_ режим блокировки \_ Windows \_ заблокирован**</span><span class="sxs-lookup"><span data-stu-id="0ee6f-115"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_LOCKED"></span><span id="wldp_windows_lockdown_mode_locked"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_LOCKED**</span></span>
</dt> <dd>

<span data-ttu-id="0ee6f-116">Блокирован.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-116">Locked.</span></span> <span data-ttu-id="0ee6f-117">Используется в основном для устройства Windows 10 с режимом S.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-117">Used primarily for a Windows 10 device with the S mode.</span></span> <span data-ttu-id="0ee6f-118">Заблокированное устройство будет принудительно применять подписанные политики Device Guard, поставляемые с образом ОС Windows 10 с режимом S.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-118">A device that is locked will enforce the signed Device Guard policies shipped with the Windows 10 OS image with the S mode.</span></span>

</dd> <dt>

<span data-ttu-id="0ee6f-119"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**\_ \_ \_ максимальный режим блокировки Windows \_ WLDP**</span><span class="sxs-lookup"><span data-stu-id="0ee6f-119"><span id="WLDP_WINDOWS_LOCKDOWN_MODE_MAX"></span><span id="wldp_windows_lockdown_mode_max"></span>**WLDP\_WINDOWS\_LOCKDOWN\_MODE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="0ee6f-120">Максимальное значение перечисления.</span><span class="sxs-lookup"><span data-stu-id="0ee6f-120">The maximum enumeration value.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0ee6f-121">Требования</span><span class="sxs-lookup"><span data-stu-id="0ee6f-121">Requirements</span></span>



| <span data-ttu-id="0ee6f-122">Требование</span><span class="sxs-lookup"><span data-stu-id="0ee6f-122">Requirement</span></span> | <span data-ttu-id="0ee6f-123">Значение</span><span class="sxs-lookup"><span data-stu-id="0ee6f-123">Value</span></span> |
|-------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="0ee6f-124">Header</span><span class="sxs-lookup"><span data-stu-id="0ee6f-124">Header</span></span><br/> | <dl> <span data-ttu-id="0ee6f-125"><dt>Wldp. h</dt></span><span class="sxs-lookup"><span data-stu-id="0ee6f-125"><dt>Wldp.h</dt></span></span> </dl> |



 

 




