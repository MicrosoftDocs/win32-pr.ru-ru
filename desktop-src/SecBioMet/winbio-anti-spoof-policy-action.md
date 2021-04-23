---
title: Перечисление WINBIO_ANTI_SPOOF_POLICY_ACTION (Винбио \_ types. h)
description: Указывает типы действий, выполняемых для политики антиподмены пользователя.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- API биометрическая платформа Windows перечисления WINBIO_ANTI_SPOOF_POLICY_ACTION
- API биометрическая платформа Windows указателя перечисления PWINBIO_ANTI_SPOOF_POLICY
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5905624bad252475cdde12c003f31a734e64dd2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988878"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a><span data-ttu-id="df794-105">\_ \_ \_ \_ Перечисление действий политики антифишинга винбио</span><span class="sxs-lookup"><span data-stu-id="df794-105">WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION enumeration</span></span>

<span data-ttu-id="df794-106">Указывает типы действий, выполняемых для политики антиподмены пользователя.</span><span class="sxs-lookup"><span data-stu-id="df794-106">Specifies the types of actions you take for the antispoofing policy of a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="df794-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="df794-107">Syntax</span></span>


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a><span data-ttu-id="df794-108">Константы</span><span class="sxs-lookup"><span data-stu-id="df794-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="df794-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**\_отключение антифишинга винбио \_ \_**</span><span class="sxs-lookup"><span data-stu-id="df794-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO\_ANTI\_SPOOF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="df794-110">Отключает обнаружение подмены для биометрического фактора.</span><span class="sxs-lookup"><span data-stu-id="df794-110">Turns off the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="df794-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**\_Включение антифишинга винбио \_ \_**</span><span class="sxs-lookup"><span data-stu-id="df794-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO\_ANTI\_SPOOF\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="df794-112">Включает обнаружение подмены для биометрического фактора.</span><span class="sxs-lookup"><span data-stu-id="df794-112">Turns on the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="df794-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**\_Удаление антифишинга винбио \_ \_**</span><span class="sxs-lookup"><span data-stu-id="df794-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**WINBIO\_ANTI\_SPOOF\_REMOVE**</span></span>
</dt> <dd>

<span data-ttu-id="df794-114">Удаляет из учетной записи всю политику антиподмены для биометрического коэффициента.</span><span class="sxs-lookup"><span data-stu-id="df794-114">Removes the entire antispoofing policy for the biometric factor from the account.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df794-115">Требования</span><span class="sxs-lookup"><span data-stu-id="df794-115">Requirements</span></span>



| <span data-ttu-id="df794-116">Требование</span><span class="sxs-lookup"><span data-stu-id="df794-116">Requirement</span></span> | <span data-ttu-id="df794-117">Значение</span><span class="sxs-lookup"><span data-stu-id="df794-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df794-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df794-118">Minimum supported client</span></span><br/> | <span data-ttu-id="df794-119">Только для \[ настольных приложений Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="df794-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="df794-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df794-120">Minimum supported server</span></span><br/> | <span data-ttu-id="df794-121">\[Только для настольных приложений Windows Server 2016\]</span><span class="sxs-lookup"><span data-stu-id="df794-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="df794-122">Header</span><span class="sxs-lookup"><span data-stu-id="df794-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="df794-123"><dt>Винбио \_ types. h (включите винбио. h для клиентских приложений или винбио \_ Adapters. h для адаптеров).</dt></span><span class="sxs-lookup"><span data-stu-id="df794-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df794-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df794-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df794-125">**\_ \_ \_ действие политики АНТИфишинга винбио \_**</span><span class="sxs-lookup"><span data-stu-id="df794-125">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="df794-126">**\_источник политики \_ винбио**</span><span class="sxs-lookup"><span data-stu-id="df794-126">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> </dl>

 

 





