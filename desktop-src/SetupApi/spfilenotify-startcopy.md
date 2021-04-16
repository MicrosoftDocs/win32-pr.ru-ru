---
description: Уведомление СПФИЛЕНОТИФИ \_ старткопи отправляется в функцию обратного вызова, когда очередь начинает операцию копирования файла.
ms.assetid: 01a7d9d4-b548-4e72-b1c9-7116e67c023b
title: Сообщение SPFILENOTIFY_STARTCOPY (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6693938a2f67530e7e3c906c5105d2c98a915a32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664079"
---
# <a name="spfilenotify_startcopy-message"></a><span data-ttu-id="aae4d-103">\_Сообщение спфиленотифи старткопи</span><span class="sxs-lookup"><span data-stu-id="aae4d-103">SPFILENOTIFY\_STARTCOPY message</span></span>

<span data-ttu-id="aae4d-104">Уведомление **спфиленотифи \_ старткопи** отправляется в функцию обратного вызова, когда очередь начинает операцию копирования файла.</span><span class="sxs-lookup"><span data-stu-id="aae4d-104">The **SPFILENOTIFY\_STARTCOPY** notification is sent to the callback function when the queue starts a file copy operation.</span></span>


```C++
SPFILENOTIFY_STARTCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) Operation;
            
```



## <a name="parameters"></a><span data-ttu-id="aae4d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="aae4d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aae4d-106">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="aae4d-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="aae4d-107">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="aae4d-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="aae4d-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="aae4d-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="aae4d-109">Всегда имеет значение ФИЛЕОП \_ Copy.</span><span class="sxs-lookup"><span data-stu-id="aae4d-109">Always has the value FILEOP\_COPY.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aae4d-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="aae4d-110">Return value</span></span>

<span data-ttu-id="aae4d-111">Подпрограммы обратного вызова должны возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="aae4d-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="aae4d-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="aae4d-112">Return code</span></span>                                                                                  | <span data-ttu-id="aae4d-113">Описание</span><span class="sxs-lookup"><span data-stu-id="aae4d-113">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="aae4d-114"><dt>**прервать ФИЛЕОП \_**</dt></span><span class="sxs-lookup"><span data-stu-id="aae4d-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="aae4d-115">Прервать процесс фиксации очереди.</span><span class="sxs-lookup"><span data-stu-id="aae4d-115">Abort the queue commit process.</span></span> <span data-ttu-id="aae4d-116">Подпрограммы обратного вызова должны вызывать [**сетластеррор**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) для указания причины завершения.</span><span class="sxs-lookup"><span data-stu-id="aae4d-116">The callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror) to indicate the reason for termination.</span></span> <span data-ttu-id="aae4d-117">Функция [**сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) возвращает **значение false** , и последующий вызов [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) возвращает код ошибки, заданный подпрограммой обратного вызова во время вызова **сетластеррор**.</span><span class="sxs-lookup"><span data-stu-id="aae4d-117">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function returns **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns the error code set by the callback routine during the call to **SetLastError**.</span></span><br/> |
| <dl> <span data-ttu-id="aae4d-118"><dt>**ФИЛЕОП \_ доит**</dt></span><span class="sxs-lookup"><span data-stu-id="aae4d-118"><dt>**FILEOP\_DOIT**</dt></span></span> </dl>  | <span data-ttu-id="aae4d-119">Выполните операцию копирования файлов.</span><span class="sxs-lookup"><span data-stu-id="aae4d-119">Perform the file copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |
| <dl> <span data-ttu-id="aae4d-120"><dt>**ФИЛЕОП \_ пропустить**</dt></span><span class="sxs-lookup"><span data-stu-id="aae4d-120"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="aae4d-121">Пропустить текущую операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="aae4d-121">Skip the current copy operation.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="aae4d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="aae4d-122">Requirements</span></span>



| <span data-ttu-id="aae4d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="aae4d-123">Requirement</span></span> | <span data-ttu-id="aae4d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="aae4d-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aae4d-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="aae4d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="aae4d-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="aae4d-126">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aae4d-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="aae4d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="aae4d-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="aae4d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="aae4d-129">Header</span><span class="sxs-lookup"><span data-stu-id="aae4d-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="aae4d-130"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aae4d-130"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aae4d-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aae4d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aae4d-132">Обзор</span><span class="sxs-lookup"><span data-stu-id="aae4d-132">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="aae4d-133">Уведомления</span><span class="sxs-lookup"><span data-stu-id="aae4d-133">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="aae4d-134">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="aae4d-134">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="aae4d-135">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="aae4d-135">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="aae4d-136">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="aae4d-136">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

