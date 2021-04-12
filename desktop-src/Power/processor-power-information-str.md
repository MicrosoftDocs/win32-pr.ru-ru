---
description: Содержит сведения о процессоре.
ms.assetid: fa8c533c-3a54-4eb5-893f-649dfd8b4609
title: Структура PROCESSOR_POWER_INFORMATION
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PROCESSOR_POWER_INFORMATION
api_type:
- NA
api_location: ''
ms.openlocfilehash: 500a346080d7bf0c44d392a63a71310db74225a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345485"
---
# <a name="processor_power_information-structure"></a><span data-ttu-id="1a6f8-103">\_ \_ Структура сведений о ПИТАНИи процессора</span><span class="sxs-lookup"><span data-stu-id="1a6f8-103">PROCESSOR\_POWER\_INFORMATION structure</span></span>

<span data-ttu-id="1a6f8-104">Содержит сведения о процессоре.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-104">Contains information about a processor.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a6f8-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1a6f8-105">Syntax</span></span>


```C++
typedef struct _PROCESSOR_POWER_INFORMATION {
  ULONG Number;
  ULONG MaxMhz;
  ULONG CurrentMhz;
  ULONG MhzLimit;
  ULONG MaxIdleState;
  ULONG CurrentIdleState;
} PROCESSOR_POWER_INFORMATION, *PPROCESSOR_POWER_INFORMATION;
```



## <a name="members"></a><span data-ttu-id="1a6f8-106">Члены</span><span class="sxs-lookup"><span data-stu-id="1a6f8-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="1a6f8-107">**Число**</span><span class="sxs-lookup"><span data-stu-id="1a6f8-107">**Number**</span></span>
</dt> <dd>

<span data-ttu-id="1a6f8-108">Номер системного процессора.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-108">The system processor number.</span></span>

</dd> <dt>

<span data-ttu-id="1a6f8-109">**максмхз**</span><span class="sxs-lookup"><span data-stu-id="1a6f8-109">**MaxMhz**</span></span>
</dt> <dd>

<span data-ttu-id="1a6f8-110">Максимальная заданная частота таймера системного процессора в мегагерцах.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-110">The maximum specified clock frequency of the system processor, in megahertz.</span></span>

</dd> <dt>

<span data-ttu-id="1a6f8-111">**куррентмхз**</span><span class="sxs-lookup"><span data-stu-id="1a6f8-111">**CurrentMhz**</span></span>
</dt> <dd>

<span data-ttu-id="1a6f8-112">Тактовая частота процессора в мегагерцах.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-112">The processor clock frequency, in megahertz.</span></span> <span data-ttu-id="1a6f8-113">Это число — это максимально заданная частота такта процессора, умноженная на текущее регулирование процессора.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-113">This number is the maximum specified processor clock frequency multiplied by the current processor throttle.</span></span>

</dd> <dt>

<span data-ttu-id="1a6f8-114">**мхзлимит**</span><span class="sxs-lookup"><span data-stu-id="1a6f8-114">**MhzLimit**</span></span>
</dt> <dd>

<span data-ttu-id="1a6f8-115">Ограничение тактовой частоты процессора в мегагерцах.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-115">The limit on the processor clock frequency, in megahertz.</span></span> <span data-ttu-id="1a6f8-116">Это число является максимальной тактовой частотой процессора, умноженной на текущий предел регулирования температуры процессора.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-116">This number is the maximum specified processor clock frequency multiplied by the current processor thermal throttle limit.</span></span>

</dd> <dt>

<span data-ttu-id="1a6f8-117">**максидлестате**</span><span class="sxs-lookup"><span data-stu-id="1a6f8-117">**MaxIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="1a6f8-118">Максимальное состояние простоя этого процессора.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-118">The maximum idle state of this processor.</span></span>

</dd> <dt>

<span data-ttu-id="1a6f8-119">**куррентидлестате**</span><span class="sxs-lookup"><span data-stu-id="1a6f8-119">**CurrentIdleState**</span></span>
</dt> <dd>

<span data-ttu-id="1a6f8-120">Текущее состояние простоя этого процессора.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-120">The current idle state of this processor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1a6f8-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1a6f8-121">Remarks</span></span>

<span data-ttu-id="1a6f8-122">Обратите внимание, что это определение структуры было случайно опущено в WinNT. h.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-122">Note that this structure definition was accidentally omitted from WinNT.h.</span></span> <span data-ttu-id="1a6f8-123">Эта ошибка будет исправлена в будущем.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-123">This error will be corrected in the future.</span></span> <span data-ttu-id="1a6f8-124">Тем временем, чтобы скомпилировать приложение, включите в исходный код определение структуры, содержащееся в этом разделе.</span><span class="sxs-lookup"><span data-stu-id="1a6f8-124">In the meantime, to compile your application, include the structure definition contained in this topic in your source code.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a6f8-125">Требования</span><span class="sxs-lookup"><span data-stu-id="1a6f8-125">Requirements</span></span>



| <span data-ttu-id="1a6f8-126">Требование</span><span class="sxs-lookup"><span data-stu-id="1a6f8-126">Requirement</span></span> | <span data-ttu-id="1a6f8-127">Значение</span><span class="sxs-lookup"><span data-stu-id="1a6f8-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1a6f8-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="1a6f8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1a6f8-129">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1a6f8-129">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="1a6f8-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="1a6f8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1a6f8-131">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1a6f8-131">Windows Server 2003 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1a6f8-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1a6f8-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a6f8-133">**каллнтповеринформатион**</span><span class="sxs-lookup"><span data-stu-id="1a6f8-133">**CallNtPowerInformation**</span></span>](/windows/desktop/api/Powerbase/nf-powerbase-callntpowerinformation)
</dt> </dl>

 

 




