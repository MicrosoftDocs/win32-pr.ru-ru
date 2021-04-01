---
description: Уведомление СПФИЛЕНОТИФИ \_ делетиррор отправляется в подпрограммы обратного вызова при возникновении ошибки во время операции удаления файла.
ms.assetid: b98b62f0-0b59-430e-966d-c1447026b696
title: Сообщение SPFILENOTIFY_DELETEERROR (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 035b61120bd1343b43c9b6f6d74246eab33cb430
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081528"
---
# <a name="spfilenotify_deleteerror-message"></a><span data-ttu-id="e12e4-103">\_Сообщение спфиленотифи делетиррор</span><span class="sxs-lookup"><span data-stu-id="e12e4-103">SPFILENOTIFY\_DELETEERROR message</span></span>

<span data-ttu-id="e12e4-104">Уведомление **спфиленотифи \_ делетиррор** отправляется в подпрограммы обратного вызова при возникновении ошибки во время операции удаления файла.</span><span class="sxs-lookup"><span data-stu-id="e12e4-104">The **SPFILENOTIFY\_DELETEERROR** notification is sent to the callback routine if an error occurs during a file delete operation.</span></span>


```C++
SPFILENOTIFY_DELETEERROR
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="e12e4-105">Параметры</span><span class="sxs-lookup"><span data-stu-id="e12e4-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e12e4-106">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="e12e4-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="e12e4-107">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="e12e4-107">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span>

</dd> <dt>

<span data-ttu-id="e12e4-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="e12e4-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="e12e4-109">Не используется.</span><span class="sxs-lookup"><span data-stu-id="e12e4-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e12e4-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e12e4-110">Return value</span></span>

<span data-ttu-id="e12e4-111">Подпрограммы обратного вызова должны возвращать одно из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e12e4-111">The callback routine should return one of the following values.</span></span>



| <span data-ttu-id="e12e4-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="e12e4-112">Return code</span></span>                                                                                  | <span data-ttu-id="e12e4-113">Описание</span><span class="sxs-lookup"><span data-stu-id="e12e4-113">Description</span></span>                                                                                                                                                                                                                                                                   |
|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e12e4-114"><dt>**прервать ФИЛЕОП \_**</dt></span><span class="sxs-lookup"><span data-stu-id="e12e4-114"><dt>**FILEOP\_ABORT**</dt></span></span> </dl> | <span data-ttu-id="e12e4-115">Обработка очереди должна быть отменена.</span><span class="sxs-lookup"><span data-stu-id="e12e4-115">Queue processing should be canceled.</span></span> <span data-ttu-id="e12e4-116">[**Сетупкоммитфилекуеуе**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) возвращает ноль, а [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) Возвращает расширенные сведения об ошибке, такие как ошибка \_ отмены (если пользователь был отменен) или ошибка \_ не \_ хватает \_ памяти.</span><span class="sxs-lookup"><span data-stu-id="e12e4-116">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) returns zero and [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns extended error information such as ERROR\_CANCELLED (if the user canceled) or ERROR\_NOT\_ENOUGH\_MEMORY.</span></span><br/> |
| <dl> <span data-ttu-id="e12e4-117"><dt>**ФИЛЕОП \_ Повтор**</dt></span><span class="sxs-lookup"><span data-stu-id="e12e4-117"><dt>**FILEOP\_RETRY**</dt></span></span> </dl> | <span data-ttu-id="e12e4-118">Пользователь пытается выполнить операцию удаления еще раз.</span><span class="sxs-lookup"><span data-stu-id="e12e4-118">The user is attempting the delete operation again.</span></span><br/>                                                                                                                                                                                                                 |
| <dl> <span data-ttu-id="e12e4-119"><dt>**ФИЛЕОП \_ пропустить**</dt></span><span class="sxs-lookup"><span data-stu-id="e12e4-119"><dt>**FILEOP\_SKIP**</dt></span></span> </dl>  | <span data-ttu-id="e12e4-120">Пользователь пропускает операцию удаления файла.</span><span class="sxs-lookup"><span data-stu-id="e12e4-120">The user is skipping the file delete operation.</span></span><br/>                                                                                                                                                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="e12e4-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e12e4-121">Requirements</span></span>



| <span data-ttu-id="e12e4-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e12e4-122">Requirement</span></span> | <span data-ttu-id="e12e4-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e12e4-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="e12e4-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e12e4-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e12e4-125">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="e12e4-125">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e12e4-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e12e4-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e12e4-127">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="e12e4-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="e12e4-128">Header</span><span class="sxs-lookup"><span data-stu-id="e12e4-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e12e4-129"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="e12e4-129"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e12e4-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e12e4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e12e4-131">Обзор</span><span class="sxs-lookup"><span data-stu-id="e12e4-131">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="e12e4-132">Уведомления</span><span class="sxs-lookup"><span data-stu-id="e12e4-132">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="e12e4-133">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="e12e4-133">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="e12e4-134">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="e12e4-134">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="e12e4-135">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="e12e4-135">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

