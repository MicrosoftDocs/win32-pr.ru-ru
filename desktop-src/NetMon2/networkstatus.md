---
description: Структура NETWORKSTATUS описывает текущее состояние НПП.
ms.assetid: e5e07480-cfc3-408f-9ca2-48a697e4b875
title: Структура NETWORKSTATUS (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- NETWORKSTATUS
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 067a57dabfb5222deb27de44c60c6eb121cd8c36
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104546994"
---
# <a name="networkstatus-structure"></a><span data-ttu-id="022cc-103">Структура NETWORKSTATUS</span><span class="sxs-lookup"><span data-stu-id="022cc-103">NETWORKSTATUS structure</span></span>

<span data-ttu-id="022cc-104">Структура **NETWORKSTATUS** описывает текущее состояние НПП.</span><span class="sxs-lookup"><span data-stu-id="022cc-104">The **NETWORKSTATUS** structure describes the current status of the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="022cc-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="022cc-105">Syntax</span></span>


```C++
typedef struct _NETWORKSTATUS {
  DWORD State;
  DWORD Flags;
} NETWORKSTATUS, *LPNETWORKSTATUS;
```



## <a name="members"></a><span data-ttu-id="022cc-106">Члены</span><span class="sxs-lookup"><span data-stu-id="022cc-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="022cc-107">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="022cc-107">**State**</span></span>
</dt> <dd>

<span data-ttu-id="022cc-108">Указывает текущее состояние НПП.</span><span class="sxs-lookup"><span data-stu-id="022cc-108">Indicates the current state of the NPP.</span></span>



| <span data-ttu-id="022cc-109">Значение</span><span class="sxs-lookup"><span data-stu-id="022cc-109">Value</span></span>                                                                                                                                                                                                          | <span data-ttu-id="022cc-110">Значение</span><span class="sxs-lookup"><span data-stu-id="022cc-110">Meaning</span></span>                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span id="NETWORKSTATUS_STATE_VOID"></span><span id="networkstatus_state_void"></span><dl> <span data-ttu-id="022cc-111"><dt>**NETWORKSTATUS, \_ состояние \_ void**</dt></span><span class="sxs-lookup"><span data-stu-id="022cc-111"><dt>**NETWORKSTATUS\_STATE\_VOID**</dt></span></span> </dl>                | <span data-ttu-id="022cc-112">НПП не подключен, или он подключен, а запись не запущена.</span><span class="sxs-lookup"><span data-stu-id="022cc-112">The NPP is not connected, or it is connected and the capture is not started.</span></span><br/> |
| <span id="NETWORKSTATUS_STATE_CAPTURING"></span><span id="networkstatus_state_capturing"></span><dl> <span data-ttu-id="022cc-113"><dt>**\_захват состояния \_ NETWORKSTATUS**</dt></span><span class="sxs-lookup"><span data-stu-id="022cc-113"><dt>**NETWORKSTATUS\_STATE\_CAPTURING**</dt></span></span> </dl> | <span data-ttu-id="022cc-114">НПП захватывает данные.</span><span class="sxs-lookup"><span data-stu-id="022cc-114">The NPP is capturing data.</span></span><br/>                                                   |
| <span id="NETWORKSTATUS_STATE_PAUSED"></span><span id="networkstatus_state_paused"></span><dl> <span data-ttu-id="022cc-115"><dt>**\_ \_ приостановлено состояние NETWORKSTATUS**</dt></span><span class="sxs-lookup"><span data-stu-id="022cc-115"><dt>**NETWORKSTATUS\_STATE\_PAUSED**</dt></span></span> </dl>          | <span data-ttu-id="022cc-116">НПП приостановлен во время записи данных.</span><span class="sxs-lookup"><span data-stu-id="022cc-116">The NPP has paused while capturing data.</span></span><br/>                                     |



 

</dd> <dt>

<span data-ttu-id="022cc-117">**Флаги**</span><span class="sxs-lookup"><span data-stu-id="022cc-117">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="022cc-118">Флаги, описывающие текущее состояние НПП.</span><span class="sxs-lookup"><span data-stu-id="022cc-118">Flags that describe the current state of the NPP.</span></span>



| <span data-ttu-id="022cc-119">Значение</span><span class="sxs-lookup"><span data-stu-id="022cc-119">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="022cc-120">Значение</span><span class="sxs-lookup"><span data-stu-id="022cc-120">Meaning</span></span>                                            |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <span id="NETWORKSTATUS_FLAGS_TRIGGER_PENDING"></span><span id="networkstatus_flags_trigger_pending"></span><dl> <span data-ttu-id="022cc-121"><dt>**\_ \_ Ожидание триггера NETWORKSTATUS flags \_**</dt></span><span class="sxs-lookup"><span data-stu-id="022cc-121"><dt>**NETWORKSTATUS\_FLAGS\_TRIGGER\_PENDING**</dt></span></span> </dl> | <span data-ttu-id="022cc-122">Ожидается триггер для НПП.</span><span class="sxs-lookup"><span data-stu-id="022cc-122">There is a trigger pending for the NPP.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="022cc-123">Комментарии</span><span class="sxs-lookup"><span data-stu-id="022cc-123">Remarks</span></span>

<span data-ttu-id="022cc-124">При использовании этой структуры необходимо выделить память для структуры, прежде чем ее можно будет использовать, и освободить память, когда структура больше не нужна.</span><span class="sxs-lookup"><span data-stu-id="022cc-124">When using this structure, you must allocate the memory for the structure before it can be used and free the memory when the structure is no longer needed.</span></span>

<span data-ttu-id="022cc-125">В списке см. также в нижней части этого раздела перечислены все методы, использующие эту структуру.</span><span class="sxs-lookup"><span data-stu-id="022cc-125">The See Also list at the bottom of this topic lists all the methods that use this structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="022cc-126">Требования</span><span class="sxs-lookup"><span data-stu-id="022cc-126">Requirements</span></span>



| <span data-ttu-id="022cc-127">Требование</span><span class="sxs-lookup"><span data-stu-id="022cc-127">Requirement</span></span> | <span data-ttu-id="022cc-128">Значение</span><span class="sxs-lookup"><span data-stu-id="022cc-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="022cc-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="022cc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="022cc-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="022cc-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="022cc-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="022cc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="022cc-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="022cc-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="022cc-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="022cc-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="022cc-134"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="022cc-134"><dt>Netmon.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="022cc-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="022cc-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="022cc-136">Иделайдк:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="022cc-136">IDelaydC::QueryStatus</span></span>](idelaydc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="022cc-137">ИЕСП:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="022cc-137">IESP::QueryStatus</span></span>](iesp-querystatus.md)
</dt> <dt>

[<span data-ttu-id="022cc-138">ИРТК:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="022cc-138">IRTC::QueryStatus</span></span>](irtc-querystatus.md)
</dt> <dt>

[<span data-ttu-id="022cc-139">Истатс:: QueryStatus</span><span class="sxs-lookup"><span data-stu-id="022cc-139">IStats::QueryStatus</span></span>](istats-querystatus.md)
</dt> </dl>

 

 




