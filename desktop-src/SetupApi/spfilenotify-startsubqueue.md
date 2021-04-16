---
description: Уведомление СПФИЛЕНОТИФИ \_ стартсубкуеуе отправляется в функцию обратного вызова, когда очередь начинает обработку операций в подочереди DELETE, Rename или Copy.
ms.assetid: 4f971549-8f79-4995-9796-1177c3a3c416
title: Сообщение SPFILENOTIFY_STARTSUBQUEUE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30e4f20440c12e7fcd1900cd9762a504a26b907f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664455"
---
# <a name="spfilenotify_startsubqueue-message"></a><span data-ttu-id="3c859-103">\_Сообщение спфиленотифи стартсубкуеуе</span><span class="sxs-lookup"><span data-stu-id="3c859-103">SPFILENOTIFY\_STARTSUBQUEUE message</span></span>

<span data-ttu-id="3c859-104">Уведомление **спфиленотифи \_ стартсубкуеуе** отправляется в функцию обратного вызова, когда очередь начинает обработку операций в подочереди DELETE, Rename или Copy.</span><span class="sxs-lookup"><span data-stu-id="3c859-104">The **SPFILENOTIFY\_STARTSUBQUEUE** notification is sent to the callback function when the queue starts to process the operations in the delete, rename, or copy subqueue.</span></span>


```C++
SPFILENOTIFY_STARTSUBQUEUE
  Param1 = (UINT) SubQueue;
  Param2 = (UINT) NumOperations;
            
```



## <a name="parameters"></a><span data-ttu-id="3c859-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="3c859-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c859-106">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="3c859-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="3c859-107">Подочередь, которая была запущена.</span><span class="sxs-lookup"><span data-stu-id="3c859-107">Subqueue that has been started.</span></span> <span data-ttu-id="3c859-108">Этот параметр может иметь одно из значений ФИЛЕОП \_ DELETE, филеоп \_ Rename или филеоп \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="3c859-108">This parameter can be any one of the values FILEOP\_DELETE, FILEOP\_RENAME, or FILEOP\_COPY.</span></span>

</dd> <dt>

<span data-ttu-id="3c859-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="3c859-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="3c859-110">Число операций копирования, переименования или удаления файлов во вложенной очереди.</span><span class="sxs-lookup"><span data-stu-id="3c859-110">Number of file copy, rename, or delete operations in the subqueue.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c859-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3c859-111">Return value</span></span>

<span data-ttu-id="3c859-112">При возникновении ошибки подпрограммы обратного вызова должны вызвать [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), указав ошибку, а затем вернуть ноль.</span><span class="sxs-lookup"><span data-stu-id="3c859-112">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="3c859-113">Функция [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) вернет **значение false** , а последующий вызов [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвратит код ошибки, заданный подпрограммой обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="3c859-113">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="3c859-114">Если ошибка не возникает, подпрограммы обратного вызова должны возвращать ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="3c859-114">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c859-115">Требования</span><span class="sxs-lookup"><span data-stu-id="3c859-115">Requirements</span></span>



| <span data-ttu-id="3c859-116">Требование</span><span class="sxs-lookup"><span data-stu-id="3c859-116">Requirement</span></span> | <span data-ttu-id="3c859-117">Значение</span><span class="sxs-lookup"><span data-stu-id="3c859-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c859-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c859-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3c859-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="3c859-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="3c859-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c859-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3c859-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="3c859-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3c859-122">Header</span><span class="sxs-lookup"><span data-stu-id="3c859-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c859-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c859-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c859-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c859-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c859-125">Обзор</span><span class="sxs-lookup"><span data-stu-id="3c859-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="3c859-126">Уведомления</span><span class="sxs-lookup"><span data-stu-id="3c859-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="3c859-127">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="3c859-127">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="3c859-128">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="3c859-128">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

