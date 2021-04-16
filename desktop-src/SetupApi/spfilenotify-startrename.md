---
description: Уведомление СПФИЛЕНОТИФИ \_ стартренаме отправляется в функцию обратного вызова, когда очередь запускает операцию переименования файла.
ms.assetid: 005c1840-6aa9-4e94-bfe7-6a9d53735fd9
title: Сообщение SPFILENOTIFY_STARTRENAME (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 36c17d0c70b49ba00b3b16956e7ede5eda43b35b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664076"
---
# <a name="spfilenotify_startrename-message"></a><span data-ttu-id="09eda-103">\_Сообщение спфиленотифи стартренаме</span><span class="sxs-lookup"><span data-stu-id="09eda-103">SPFILENOTIFY\_STARTRENAME message</span></span>

<span data-ttu-id="09eda-104">Уведомление **спфиленотифи \_ стартренаме** отправляется в функцию обратного вызова, когда очередь запускает операцию переименования файла.</span><span class="sxs-lookup"><span data-stu-id="09eda-104">The **SPFILENOTIFY\_STARTRENAME** notification is sent to the callback function when the queue starts a file rename operation.</span></span>


```C++
SPFILENOTIFY_STARTRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a><span data-ttu-id="09eda-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="09eda-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09eda-106">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="09eda-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="09eda-107">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="09eda-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="09eda-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="09eda-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="09eda-109">Всегда имеет значение ФИЛЕОП \_ Rename.</span><span class="sxs-lookup"><span data-stu-id="09eda-109">Always has the value FILEOP\_RENAME.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="09eda-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="09eda-110">Return value</span></span>

<span data-ttu-id="09eda-111">Подпрограммы обратного вызова должны возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="09eda-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="09eda-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="09eda-112">Return code</span></span>                                                                                  | <span data-ttu-id="09eda-113">Описание</span><span class="sxs-lookup"><span data-stu-id="09eda-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                     |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="09eda-114"><dt>**прервать ФИЛЕОП \_**</dt></span><span class="sxs-lookup"><span data-stu-id="09eda-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="09eda-115">Прервать фиксацию очереди.</span><span class="sxs-lookup"><span data-stu-id="09eda-115">Abort the queue commit.</span></span> <span data-ttu-id="09eda-116">Подпрограммы обратного вызова должны вызывать [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) для указания причины завершения.</span><span class="sxs-lookup"><span data-stu-id="09eda-116">The callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to indicate the reason for termination.</span></span> <span data-ttu-id="09eda-117">[**Сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) возвращает **значение false** , и последующий вызов [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки, заданный подпрограммой обратного вызова во время вызова **сетластеррор**.</span><span class="sxs-lookup"><span data-stu-id="09eda-117">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code set by the callback routine during the call to **SetLastError**.</span></span><br/> |
| <dl> <span data-ttu-id="09eda-118"><dt>**ФИЛЕОП \_ доит**</dt></span><span class="sxs-lookup"><span data-stu-id="09eda-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="09eda-119">Выполните операцию копирования файлов.</span><span class="sxs-lookup"><span data-stu-id="09eda-119">Perform the file copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="09eda-120"><dt>**ФИЛЕОП \_ пропустить**</dt></span><span class="sxs-lookup"><span data-stu-id="09eda-120"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="09eda-121">Пропустить текущую операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="09eda-121">Skip the current copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                     |



 

## <a name="requirements"></a><span data-ttu-id="09eda-122">Требования</span><span class="sxs-lookup"><span data-stu-id="09eda-122">Requirements</span></span>



| <span data-ttu-id="09eda-123">Требование</span><span class="sxs-lookup"><span data-stu-id="09eda-123">Requirement</span></span> | <span data-ttu-id="09eda-124">Значение</span><span class="sxs-lookup"><span data-stu-id="09eda-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="09eda-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="09eda-125">Minimum supported client</span></span><br/> | <span data-ttu-id="09eda-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="09eda-126">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="09eda-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="09eda-127">Minimum supported server</span></span><br/> | <span data-ttu-id="09eda-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="09eda-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="09eda-129">Header</span><span class="sxs-lookup"><span data-stu-id="09eda-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="09eda-130"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="09eda-130"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09eda-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="09eda-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09eda-132">Обзор</span><span class="sxs-lookup"><span data-stu-id="09eda-132">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="09eda-133">Уведомления</span><span class="sxs-lookup"><span data-stu-id="09eda-133">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="09eda-134">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="09eda-134">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="09eda-135">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="09eda-135">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="09eda-136">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="09eda-136">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

