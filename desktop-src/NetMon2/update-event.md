---
description: Обновление \_ структуры событий обновляет события. Эта структура передается обратно вызывающему приложению через процедуру обратного вызова состояния события НПП.
ms.assetid: 6896be5a-f986-44ff-a18b-010f7b9858aa
title: Структура UPDATE_EVENT (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UPDATE_EVENT
api_type:
- HeaderDef
api_location:
- Netmon.h
ms.openlocfilehash: 3da45020a68114182a71b25ff9bba380d3f89eee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105673576"
---
# <a name="update_event-structure"></a><span data-ttu-id="f9108-104">ОБНОВИТЬ \_ структуру событий</span><span class="sxs-lookup"><span data-stu-id="f9108-104">UPDATE\_EVENT structure</span></span>

<span data-ttu-id="f9108-105">**Обновление структуры \_ событий** обновляет события.</span><span class="sxs-lookup"><span data-stu-id="f9108-105">The **UPDATE\_EVENT** structure updates events.</span></span> <span data-ttu-id="f9108-106">Эта структура передается обратно вызывающему приложению через процедуру обратного вызова состояния события НПП.</span><span class="sxs-lookup"><span data-stu-id="f9108-106">This structure is passed back to the calling application via the event status callback procedure by the NPP.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9108-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f9108-107">Syntax</span></span>


```C++
typedef struct _UPDATE_EVENT {
  USHORT       Event;
  DWORD        Action;
  DWORD        Status;
  DWORD        Value;
  __int64      TimeStamp;
  DWORD_PTR    lpUserContext;
  DWORD_PTR    lpReserved;
  UINT         FramesDropped;
  union {
    DWORD                        Reserved;
    LPFRAMETABLE                 lpFrameTable;
    DWORD_PTR                    lpPacketQueue;
    SECURITY_PERMISSION_RESPONSE SecurityResponse;
  };
  LPSTATISTICS lpFinalStats;
} UPDATE_EVENT, *PUPDATE_EVENT;
```



## <a name="members"></a><span data-ttu-id="f9108-108">Члены</span><span class="sxs-lookup"><span data-stu-id="f9108-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f9108-109">**Событие**</span><span class="sxs-lookup"><span data-stu-id="f9108-109">**Event**</span></span>
</dt> <dd>

<span data-ttu-id="f9108-110">Регистрируется фактическое событие.</span><span class="sxs-lookup"><span data-stu-id="f9108-110">Actual event being recorded.</span></span>

</dd> <dt>

<span data-ttu-id="f9108-111">**Действие**</span><span class="sxs-lookup"><span data-stu-id="f9108-111">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="f9108-112">Предпринимаемое действие.</span><span class="sxs-lookup"><span data-stu-id="f9108-112">The action taken.</span></span>

</dd> <dt>

<span data-ttu-id="f9108-113">**Состояние**</span><span class="sxs-lookup"><span data-stu-id="f9108-113">**Status**</span></span>
</dt> <dd>

<span data-ttu-id="f9108-114">Указание состояния сети.</span><span class="sxs-lookup"><span data-stu-id="f9108-114">Network status indication.</span></span>

</dd> <dt>

<span data-ttu-id="f9108-115">**Значение**</span><span class="sxs-lookup"><span data-stu-id="f9108-115">**Value**</span></span>
</dt> <dd>

<span data-ttu-id="f9108-116">Вспомогательная переменная счетчика.</span><span class="sxs-lookup"><span data-stu-id="f9108-116">Auxiliary counter variable.</span></span>

</dd> <dt>

<span data-ttu-id="f9108-117">**TimeStamp**</span><span class="sxs-lookup"><span data-stu-id="f9108-117">**TimeStamp**</span></span>
</dt> <dd>

<span data-ttu-id="f9108-118">Помеченные события в микросекундах.</span><span class="sxs-lookup"><span data-stu-id="f9108-118">The marked events, in microseconds.</span></span>

</dd> <dt>

<span data-ttu-id="f9108-119">**лпусерконтекст**</span><span class="sxs-lookup"><span data-stu-id="f9108-119">**lpUserContext**</span></span>
</dt> <dd>

<span data-ttu-id="f9108-120">Контекст пользователя, заданный приложением.</span><span class="sxs-lookup"><span data-stu-id="f9108-120">User context given by the application.</span></span>

</dd> <dt>

<span data-ttu-id="f9108-121">**lpReserved**</span><span class="sxs-lookup"><span data-stu-id="f9108-121">**lpReserved**</span></span>
</dt> <dd>

<span data-ttu-id="f9108-122">Использование драйвера или NAL.</span><span class="sxs-lookup"><span data-stu-id="f9108-122">Driver or NAL use.</span></span>

</dd> <dt>

<span data-ttu-id="f9108-123">**фрамесдроппед**</span><span class="sxs-lookup"><span data-stu-id="f9108-123">**FramesDropped**</span></span>
</dt> <dd>

<span data-ttu-id="f9108-124">Кадры RTF отброшены в указанном буфере.</span><span class="sxs-lookup"><span data-stu-id="f9108-124">RTF frames dropped in the specified buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f9108-125">**Reserved**</span><span class="sxs-lookup"><span data-stu-id="f9108-125">**Reserved**</span></span>
</dt> <dd>

<span data-ttu-id="f9108-126">Данные не возвращаются с помощью этого параметра.</span><span class="sxs-lookup"><span data-stu-id="f9108-126">No data comes back with this switch option.</span></span>

</dd> <dt>

<span data-ttu-id="f9108-127">**лпфраметабле**</span><span class="sxs-lookup"><span data-stu-id="f9108-127">**lpFrameTable**</span></span>
</dt> <dd>

<span data-ttu-id="f9108-128">Только RTF.</span><span class="sxs-lookup"><span data-stu-id="f9108-128">RTF only.</span></span>

</dd> <dt>

<span data-ttu-id="f9108-129">**лппаккеткуеуе**</span><span class="sxs-lookup"><span data-stu-id="f9108-129">**lpPacketQueue**</span></span>
</dt> <dd>

<span data-ttu-id="f9108-130">Для передачи.</span><span class="sxs-lookup"><span data-stu-id="f9108-130">For transmits.</span></span>

</dd> <dt>

<span data-ttu-id="f9108-131">**секуритиреспонсе**</span><span class="sxs-lookup"><span data-stu-id="f9108-131">**SecurityResponse**</span></span>
</dt> <dd>

<span data-ttu-id="f9108-132">Ответ монитора удаленной безопасности.</span><span class="sxs-lookup"><span data-stu-id="f9108-132">Remote security monitor response.</span></span>

</dd> <dt>

<span data-ttu-id="f9108-133">**лпфиналстатс**</span><span class="sxs-lookup"><span data-stu-id="f9108-133">**lpFinalStats**</span></span>
</dt> <dd>

<span data-ttu-id="f9108-134">Этот параметр заполняется только для остановок, не связанных с безопасностью (например, триггеров).</span><span class="sxs-lookup"><span data-stu-id="f9108-134">This is only filled in on non-security related stops (for example, triggers).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f9108-135">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f9108-135">Remarks</span></span>

<span data-ttu-id="f9108-136">Пользователи C++ должны отметить, что объявление для этого обратного вызова должно находиться в открытой части файла заголовка:</span><span class="sxs-lookup"><span data-stu-id="f9108-136">C++ users should note that the declaration for this callback should be in the public part of the header file:</span></span>

``` syntax
static WINAPI DWORD NetworkCallback( UPDATE_EVENT events);
```

<span data-ttu-id="f9108-137">Реализация должна находиться в защищенном разделе CPP файла:</span><span class="sxs-lookup"><span data-stu-id="f9108-137">The implementation should be in the protected section of the .cpp file:</span></span>

``` syntax
DWORD WINAPI ClassName::NetworkCallback( UPDATE_EVENT events) {};
```

## <a name="requirements"></a><span data-ttu-id="f9108-138">Требования</span><span class="sxs-lookup"><span data-stu-id="f9108-138">Requirements</span></span>



| <span data-ttu-id="f9108-139">Требование</span><span class="sxs-lookup"><span data-stu-id="f9108-139">Requirement</span></span> | <span data-ttu-id="f9108-140">Значение</span><span class="sxs-lookup"><span data-stu-id="f9108-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f9108-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f9108-141">Minimum supported client</span></span><br/> | <span data-ttu-id="f9108-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f9108-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f9108-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f9108-143">Minimum supported server</span></span><br/> | <span data-ttu-id="f9108-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="f9108-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f9108-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="f9108-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="f9108-146"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="f9108-146"><dt>Netmon.h</dt></span></span> </dl> |



 

 




