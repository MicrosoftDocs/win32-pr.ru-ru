---
description: Уведомление СПФИЛЕНОТИФИ \_ ендкуеуе отправляется в подпрограммы обратного вызова после завершения всех операций, поставленных в очередь.
ms.assetid: f4540ab6-edea-4f84-b7eb-4ab3f774068b
title: Сообщение SPFILENOTIFY_ENDQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0f3ed2ca896f91ec09cb49f89731b41c5d099465
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103999507"
---
# <a name="spfilenotify_endqueue-message"></a><span data-ttu-id="0bdb7-103">\_Сообщение спфиленотифи ендкуеуе</span><span class="sxs-lookup"><span data-stu-id="0bdb7-103">SPFILENOTIFY\_ENDQUEUE message</span></span>

<span data-ttu-id="0bdb7-104">Уведомление **спфиленотифи \_ ендкуеуе** отправляется в подпрограммы обратного вызова после завершения всех операций, поставленных в очередь.</span><span class="sxs-lookup"><span data-stu-id="0bdb7-104">The **SPFILENOTIFY\_ENDQUEUE** notification is sent to the callback routine when all of the queued operations have been completed.</span></span>


```C++
SPFILENOTIFY_ENDQUEUE
  Param1 = (UINT) Result;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="0bdb7-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="0bdb7-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0bdb7-106">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="0bdb7-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="0bdb7-107">**Значение true** , если очередь успешно обработана; в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="0bdb7-107">**TRUE** if the queue was processed successfully, **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="0bdb7-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="0bdb7-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="0bdb7-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="0bdb7-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0bdb7-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0bdb7-110">Return value</span></span>

<span data-ttu-id="0bdb7-111">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="0bdb7-111">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="0bdb7-112">Требования</span><span class="sxs-lookup"><span data-stu-id="0bdb7-112">Requirements</span></span>



| <span data-ttu-id="0bdb7-113">Требование</span><span class="sxs-lookup"><span data-stu-id="0bdb7-113">Requirement</span></span> | <span data-ttu-id="0bdb7-114">Значение</span><span class="sxs-lookup"><span data-stu-id="0bdb7-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0bdb7-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0bdb7-115">Minimum supported client</span></span><br/> | <span data-ttu-id="0bdb7-116">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="0bdb7-116">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0bdb7-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0bdb7-117">Minimum supported server</span></span><br/> | <span data-ttu-id="0bdb7-118">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="0bdb7-118">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0bdb7-119">Header</span><span class="sxs-lookup"><span data-stu-id="0bdb7-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="0bdb7-120"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="0bdb7-120"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0bdb7-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0bdb7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0bdb7-122">Обзор</span><span class="sxs-lookup"><span data-stu-id="0bdb7-122">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="0bdb7-123">Уведомления</span><span class="sxs-lookup"><span data-stu-id="0bdb7-123">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="0bdb7-124">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="0bdb7-124">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="0bdb7-125">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="0bdb7-125">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




