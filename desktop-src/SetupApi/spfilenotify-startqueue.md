---
description: Уведомление СПФИЛЕНОТИФИ \_ старткуеуе отправляется в подпрограммы обратного вызова при запуске процесса обязательства очереди.
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: Сообщение SPFILENOTIFY_STARTQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090e3f97dceb1843d75934dd99cca500e6f93086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664078"
---
# <a name="spfilenotify_startqueue-message"></a><span data-ttu-id="850c2-103">\_Сообщение спфиленотифи старткуеуе</span><span class="sxs-lookup"><span data-stu-id="850c2-103">SPFILENOTIFY\_STARTQUEUE message</span></span>

<span data-ttu-id="850c2-104">Уведомление **спфиленотифи \_ старткуеуе** отправляется в подпрограммы обратного вызова при запуске процесса обязательства очереди.</span><span class="sxs-lookup"><span data-stu-id="850c2-104">The **SPFILENOTIFY\_STARTQUEUE** notification is sent to the callback routine when the queue commitment process starts.</span></span>


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="850c2-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="850c2-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="850c2-106">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="850c2-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="850c2-107">Обработчик для окна, который должен владеть диалоговыми окнами, создаваемыми подпрограммыми обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="850c2-107">Handle to the window that is to own the dialog boxes that the callback routine generates.</span></span>

</dd> <dt>

<span data-ttu-id="850c2-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="850c2-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="850c2-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="850c2-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="850c2-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="850c2-110">Return value</span></span>

<span data-ttu-id="850c2-111">При возникновении ошибки подпрограммы обратного вызова должны вызвать [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), указав ошибку, а затем вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="850c2-111">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="850c2-112">Функция [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) вернет **значение false** , а последующий вызов [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвратит код ошибки, заданный подпрограммой обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="850c2-112">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="850c2-113">Если ошибка не возникает, подпрограммы обратного вызова должны возвращать ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="850c2-113">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="850c2-114">Требования</span><span class="sxs-lookup"><span data-stu-id="850c2-114">Requirements</span></span>



| <span data-ttu-id="850c2-115">Требование</span><span class="sxs-lookup"><span data-stu-id="850c2-115">Requirement</span></span> | <span data-ttu-id="850c2-116">Значение</span><span class="sxs-lookup"><span data-stu-id="850c2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="850c2-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="850c2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="850c2-118">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="850c2-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="850c2-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="850c2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="850c2-120">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="850c2-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="850c2-121">Header</span><span class="sxs-lookup"><span data-stu-id="850c2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="850c2-122"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="850c2-122"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="850c2-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="850c2-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="850c2-124">Обзор</span><span class="sxs-lookup"><span data-stu-id="850c2-124">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="850c2-125">Уведомления</span><span class="sxs-lookup"><span data-stu-id="850c2-125">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="850c2-126">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="850c2-126">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="850c2-127">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="850c2-127">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

