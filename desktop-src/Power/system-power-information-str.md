---
description: Содержит сведения о время простояе системы.
ms.assetid: f6349b7c-1835-4492-95e3-9ce142628804
title: Структура SYSTEM_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SYSTEM_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: c32a8ad86b71ea680bd2961c9196a0896b055e5e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998494"
---
# <a name="system_power_information-structure"></a><span data-ttu-id="fca8b-103">\_Структура системной \_ информации о питании</span><span class="sxs-lookup"><span data-stu-id="fca8b-103">SYSTEM\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="fca8b-104">Содержит сведения о время простояе системы.</span><span class="sxs-lookup"><span data-stu-id="fca8b-104">Contains information about the idleness of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="fca8b-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="fca8b-105">Syntax</span></span>


```C++
typedef struct _SYSTEM_POWER_INFORMATION {
  ULONG MaxIdlenessAllowed;
  ULONG Idleness;
  ULONG TimeRemaining;
  UCHAR CoolingMode;
} SYSTEM_POWER_INFORMATION, *PSYSTEM_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="fca8b-106">Члены</span><span class="sxs-lookup"><span data-stu-id="fca8b-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="fca8b-107">**максидленессалловед**</span><span class="sxs-lookup"><span data-stu-id="fca8b-107">**MaxIdlenessAllowed**</span></span>
</dt> <dd>

<span data-ttu-id="fca8b-108">Время простоя, в котором система считается бездействующей, а время ожидания простоя начинается с учета, выраженное в процентах.</span><span class="sxs-lookup"><span data-stu-id="fca8b-108">The idleness at which the system is considered idle and the idle time-out begins counting, expressed as a percentage.</span></span> <span data-ttu-id="fca8b-109">Удаление ниже этого номера приводит к отмене таймера.</span><span class="sxs-lookup"><span data-stu-id="fca8b-109">Dropping below this number causes the timer to be canceled.</span></span>

</dd> <dt>

<span data-ttu-id="fca8b-110">**Неактивность**</span><span class="sxs-lookup"><span data-stu-id="fca8b-110">**Idleness**</span></span>
</dt> <dd>

<span data-ttu-id="fca8b-111">Текущий уровень простоя, выраженный в процентах.</span><span class="sxs-lookup"><span data-stu-id="fca8b-111">The current idle level, expressed as a percentage.</span></span>

</dd> <dt>

<span data-ttu-id="fca8b-112">**TimeRemaining**</span><span class="sxs-lookup"><span data-stu-id="fca8b-112">**TimeRemaining**</span></span>
</dt> <dd>

<span data-ttu-id="fca8b-113">Время, оставшееся до времени простоя в секундах.</span><span class="sxs-lookup"><span data-stu-id="fca8b-113">The time remaining in the idle timer, in seconds.</span></span>

</dd> <dt>

<span data-ttu-id="fca8b-114">**кулингмоде**</span><span class="sxs-lookup"><span data-stu-id="fca8b-114">**CoolingMode**</span></span>
</dt> <dd>

<span data-ttu-id="fca8b-115">Текущий режим охлаждения системы.</span><span class="sxs-lookup"><span data-stu-id="fca8b-115">The current system cooling mode.</span></span> <span data-ttu-id="fca8b-116">Этот элемент должен иметь одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="fca8b-116">This member must one of the following values.</span></span>



| <span data-ttu-id="fca8b-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fca8b-117">Value</span></span>                                                                                                                                                                                                                                 | <span data-ttu-id="fca8b-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fca8b-118">Meaning</span></span>                                                                                                   |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span id="PO_TZ_ACTIVE"></span><span id="po_tz_active"></span><dl> <span data-ttu-id="fca8b-119"><dt>**PO \_ \_Неактивное**</dt> значение <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="fca8b-119"><dt>**PO\_TZ\_ACTIVE**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="fca8b-120">Сейчас система находится в активном режиме охлаждения.</span><span class="sxs-lookup"><span data-stu-id="fca8b-120">The system is currently in Active cooling mode.</span></span><br/>                                                |
| <span id="PO_TZ_INVALID_MODE"></span><span id="po_tz_invalid_mode"></span><dl> <span data-ttu-id="fca8b-121"><dt>**PO \_ \_Недопустимый \_ режим**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="fca8b-121"><dt>**PO\_TZ\_INVALID\_MODE**</dt> <dt>2</dt></span></span> </dl> | <span data-ttu-id="fca8b-122">Система не поддерживает регулирование использования ЦП, или в системе не определена тепловая зона.</span><span class="sxs-lookup"><span data-stu-id="fca8b-122">The system does not support CPU throttling, or there is no thermal zone defined in the system.</span></span><br/> |
| <span id="PO_TZ_PASSIVE"></span><span id="po_tz_passive"></span><dl> <span data-ttu-id="fca8b-123"><dt>**PO \_ Режим \_ passive**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="fca8b-123"><dt>**PO\_TZ\_PASSIVE**</dt> <dt>1</dt></span></span> </dl>                 | <span data-ttu-id="fca8b-124">В настоящее время система находится в режиме пассивного охлаждения.</span><span class="sxs-lookup"><span data-stu-id="fca8b-124">The system is currently in Passive cooling mode.</span></span><br/>                                               |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fca8b-125">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fca8b-125">Remarks</span></span>

<span data-ttu-id="fca8b-126">Обратите внимание, что это определение структуры было случайно опущено в WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="fca8b-126">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="fca8b-127">Эта ошибка будет исправлена в будущем.</span><span class="sxs-lookup"><span data-stu-id="fca8b-127">This error will be corrected in the future.</span></span> <span data-ttu-id="fca8b-128">Тем временем, чтобы скомпилировать приложение, включите в исходный код определение структуры, содержащееся в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="fca8b-128">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="fca8b-129">Требования</span><span class="sxs-lookup"><span data-stu-id="fca8b-129">Requirements</span></span>



| <span data-ttu-id="fca8b-130">Требование</span><span class="sxs-lookup"><span data-stu-id="fca8b-130">Requirement</span></span> | <span data-ttu-id="fca8b-131">Значение</span><span class="sxs-lookup"><span data-stu-id="fca8b-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fca8b-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fca8b-132">Minimum supported client</span></span><br/> | <span data-ttu-id="fca8b-133">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="fca8b-133">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="fca8b-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fca8b-134">Minimum supported server</span></span><br/> | <span data-ttu-id="fca8b-135">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="fca8b-135">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="fca8b-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fca8b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fca8b-137">**каллнтповеринформатион**</span><span class="sxs-lookup"><span data-stu-id="fca8b-137">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




