---
description: Уведомление СПФИЛЕНОТИФИ \_ ендсубкуеуе отправляется в функцию обратного вызова, когда очередь завершает все операции в подочереди DELETE, Rename или Copy.
ms.assetid: 76bd027a-0f00-46e3-b502-0c97827308a8
title: Сообщение SPFILENOTIFY_ENDSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7eadc7546487b308313b7cb31088a22420e27af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081526"
---
# <a name="spfilenotify_endsubqueue-message"></a><span data-ttu-id="d002b-103">\_Сообщение спфиленотифи ендсубкуеуе</span><span class="sxs-lookup"><span data-stu-id="d002b-103">SPFILENOTIFY\_ENDSUBQUEUE message</span></span>

<span data-ttu-id="d002b-104">Уведомление **спфиленотифи \_ ендсубкуеуе** отправляется в функцию обратного вызова, когда очередь завершает все операции в подочереди DELETE, Rename или Copy.</span><span class="sxs-lookup"><span data-stu-id="d002b-104">The **SPFILENOTIFY\_ENDSUBQUEUE** notification is sent to the callback function when the queue completes all the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_ENDSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="d002b-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="d002b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d002b-106">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="d002b-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="d002b-107">Подочередь, которая была завершена.</span><span class="sxs-lookup"><span data-stu-id="d002b-107">Subqueue that has been completed.</span></span> <span data-ttu-id="d002b-108">Этот параметр может принимать одно из следующих значений: ФИЛЕОП \_ DELETE, филеоп \_ Rename или филеоп \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="d002b-108">This parameter can be one of the following values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="d002b-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="d002b-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="d002b-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="d002b-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d002b-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d002b-111">Return value</span></span>

<span data-ttu-id="d002b-112">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="d002b-112">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="d002b-113">Требования</span><span class="sxs-lookup"><span data-stu-id="d002b-113">Requirements</span></span>



| <span data-ttu-id="d002b-114">Требование</span><span class="sxs-lookup"><span data-stu-id="d002b-114">Requirement</span></span> | <span data-ttu-id="d002b-115">Значение</span><span class="sxs-lookup"><span data-stu-id="d002b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d002b-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d002b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="d002b-117">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="d002b-117">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d002b-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d002b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="d002b-119">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d002b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d002b-120">Header</span><span class="sxs-lookup"><span data-stu-id="d002b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="d002b-121"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="d002b-121"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d002b-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d002b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d002b-123">Обзор</span><span class="sxs-lookup"><span data-stu-id="d002b-123">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="d002b-124">Уведомления</span><span class="sxs-lookup"><span data-stu-id="d002b-124">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="d002b-125">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="d002b-125">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="d002b-126">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="d002b-126">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




