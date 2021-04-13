---
description: Уведомление СПФИЛЕНОТИФИ \_ ренамиррор отправляется в подпрограммы обратного вызова при возникновении ошибки во время операции переименования файла.
ms.assetid: b7016cbe-2987-477f-958b-52b7a31c54c2
title: Сообщение SPFILENOTIFY_RENAMEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 79a45658153980d7cfd5cb99b76fb344fcdb4bd8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347245"
---
# <a name="spfilenotify_renameerror-message"></a><span data-ttu-id="f142d-103">\_Сообщение спфиленотифи ренамиррор</span><span class="sxs-lookup"><span data-stu-id="f142d-103">SPFILENOTIFY\_RENAMEERROR message</span></span>

<span data-ttu-id="f142d-104">Уведомление **спфиленотифи \_ ренамиррор** отправляется в подпрограммы обратного вызова при возникновении ошибки во время операции переименования файла.</span><span class="sxs-lookup"><span data-stu-id="f142d-104">The **SPFILENOTIFY\_RENAMEERROR** notification is sent to the callback routine if an error occurs during a file rename operation.</span></span>


```C++
SPFILENOTIFY_RENAMEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="f142d-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="f142d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f142d-106">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="f142d-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="f142d-107">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="f142d-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="f142d-108">Элемент **Win32Error** структуры **filePaths** указывает ошибку, которая произошла во время операции переименования.</span><span class="sxs-lookup"><span data-stu-id="f142d-108">The **Win32Error** member of the **FILEPATHS** structure specifies the error that occurred during the rename operation.</span></span>

</dd> <dt>

<span data-ttu-id="f142d-109">*Param2*</span><span class="sxs-lookup"><span data-stu-id="f142d-109">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="f142d-110">Не используется.</span><span class="sxs-lookup"><span data-stu-id="f142d-110">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f142d-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f142d-111">Return value</span></span>

<span data-ttu-id="f142d-112">Подпрограммы обратного вызова должны возвращать один из следующих элементов.</span><span class="sxs-lookup"><span data-stu-id="f142d-112">The callback routine should return one of the following.</span></span>



| <span data-ttu-id="f142d-113">Код возврата</span><span class="sxs-lookup"><span data-stu-id="f142d-113">Return code</span></span>                                                                                  | <span data-ttu-id="f142d-114">Описание</span><span class="sxs-lookup"><span data-stu-id="f142d-114">Description</span></span>                                                                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f142d-115"><dt>**ФИЛЕОП \_ Повтор**</dt></span><span class="sxs-lookup"><span data-stu-id="f142d-115"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="f142d-116">Пользователь выбрал попытку повторного выполнения операции переименования.</span><span class="sxs-lookup"><span data-stu-id="f142d-116">The user chose to attempt the rename operation again.</span></span><br/>                                                                                                                                                                                                  |
| <dl> <span data-ttu-id="f142d-117"><dt>**ФИЛЕОП \_ пропустить**</dt></span><span class="sxs-lookup"><span data-stu-id="f142d-117"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="f142d-118">Пользователь решил пропустить операцию переименования файла.</span><span class="sxs-lookup"><span data-stu-id="f142d-118">The user chose to skip the file rename operation.</span></span><br/>                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="f142d-119"><dt>**прервать ФИЛЕОП \_**</dt></span><span class="sxs-lookup"><span data-stu-id="f142d-119"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="f142d-120">Останавливает фиксацию очереди.</span><span class="sxs-lookup"><span data-stu-id="f142d-120">Stop the queue commit.</span></span> <span data-ttu-id="f142d-121">[**Сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) возвращает **значение false**.</span><span class="sxs-lookup"><span data-stu-id="f142d-121">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns **FALSE**.</span></span> <span data-ttu-id="f142d-122">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) Возвращает расширенные сведения об ошибке, такие как ошибка \_ отмены (если пользователь был отменен) или ошибка \_ не \_ хватает \_ памяти.</span><span class="sxs-lookup"><span data-stu-id="f142d-122">[**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="f142d-123">Требования</span><span class="sxs-lookup"><span data-stu-id="f142d-123">Requirements</span></span>



| <span data-ttu-id="f142d-124">Требование</span><span class="sxs-lookup"><span data-stu-id="f142d-124">Requirement</span></span> | <span data-ttu-id="f142d-125">Значение</span><span class="sxs-lookup"><span data-stu-id="f142d-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f142d-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f142d-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f142d-127">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="f142d-127">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f142d-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f142d-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f142d-129">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="f142d-129">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f142d-130">Header</span><span class="sxs-lookup"><span data-stu-id="f142d-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f142d-131"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="f142d-131"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f142d-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f142d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f142d-133">Обзор</span><span class="sxs-lookup"><span data-stu-id="f142d-133">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="f142d-134">Уведомления</span><span class="sxs-lookup"><span data-stu-id="f142d-134">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="f142d-135">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="f142d-135">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="f142d-136">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="f142d-136">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="f142d-137">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="f142d-137">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

