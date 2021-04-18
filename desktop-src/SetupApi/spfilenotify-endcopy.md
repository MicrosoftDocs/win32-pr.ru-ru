---
description: Уведомление СПФИЛЕНОТИФИ \_ ендкопи передается функции обратного вызова, когда очередь завершает операцию копирования. Это уведомление отправляется, даже если пользователь отменяет или возникает ошибка.
ms.assetid: d58dc397-8803-466c-9069-728faf2c2030
title: Сообщение SPFILENOTIFY_ENDCOPY (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75dba56c4a38ac87003a3b59b594135e55a462f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664725"
---
# <a name="spfilenotify_endcopy-message"></a><span data-ttu-id="82ccd-104">\_Сообщение спфиленотифи ендкопи</span><span class="sxs-lookup"><span data-stu-id="82ccd-104">SPFILENOTIFY\_ENDCOPY message</span></span>

<span data-ttu-id="82ccd-105">Уведомление **спфиленотифи \_ ендкопи** передается функции обратного вызова, когда очередь завершает операцию копирования.</span><span class="sxs-lookup"><span data-stu-id="82ccd-105">The **SPFILENOTIFY\_ENDCOPY** notification is passed to the callback function when the queue completes a copy operation.</span></span> <span data-ttu-id="82ccd-106">Это уведомление отправляется, даже если пользователь отменяет или возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="82ccd-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDCOPY
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="82ccd-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="82ccd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="82ccd-108">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="82ccd-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="82ccd-109">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="82ccd-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="82ccd-110">Элемент **Win32Error** структуры **filePaths** указывает результат операции копирования.</span><span class="sxs-lookup"><span data-stu-id="82ccd-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="82ccd-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="82ccd-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="82ccd-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="82ccd-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="82ccd-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="82ccd-113">Return value</span></span>

<span data-ttu-id="82ccd-114">Код возврата игнорируется.</span><span class="sxs-lookup"><span data-stu-id="82ccd-114">The return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="82ccd-115">Требования</span><span class="sxs-lookup"><span data-stu-id="82ccd-115">Requirements</span></span>



| <span data-ttu-id="82ccd-116">Требование</span><span class="sxs-lookup"><span data-stu-id="82ccd-116">Requirement</span></span> | <span data-ttu-id="82ccd-117">Значение</span><span class="sxs-lookup"><span data-stu-id="82ccd-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="82ccd-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="82ccd-118">Minimum supported client</span></span><br/> | <span data-ttu-id="82ccd-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="82ccd-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="82ccd-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="82ccd-120">Minimum supported server</span></span><br/> | <span data-ttu-id="82ccd-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="82ccd-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="82ccd-122">Header</span><span class="sxs-lookup"><span data-stu-id="82ccd-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="82ccd-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="82ccd-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82ccd-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="82ccd-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82ccd-125">Обзор</span><span class="sxs-lookup"><span data-stu-id="82ccd-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="82ccd-126">Уведомления</span><span class="sxs-lookup"><span data-stu-id="82ccd-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="82ccd-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="82ccd-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="82ccd-128">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="82ccd-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="82ccd-129">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="82ccd-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




