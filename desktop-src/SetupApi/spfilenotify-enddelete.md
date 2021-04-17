---
description: Уведомление СПФИЛЕНОТИФИ \_ ендделете возвращается в подпрограммы обратного вызова, когда очередь завершает операцию удаления. Это уведомление отправляется, даже если пользователь отменяет или возникает ошибка.
ms.assetid: 78859854-8411-4c51-9c3c-628315cf1c41
title: Сообщение SPFILENOTIFY_ENDDELETE (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4ee4762dc33f8b8ec16a6be273cb42f41aeafce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664528"
---
# <a name="spfilenotify_enddelete-message"></a><span data-ttu-id="83bf2-104">\_Сообщение спфиленотифи ендделете</span><span class="sxs-lookup"><span data-stu-id="83bf2-104">SPFILENOTIFY\_ENDDELETE message</span></span>

<span data-ttu-id="83bf2-105">Уведомление **спфиленотифи \_ ендделете** возвращается в подпрограммы обратного вызова, когда очередь завершает операцию удаления.</span><span class="sxs-lookup"><span data-stu-id="83bf2-105">The **SPFILENOTIFY\_ENDDELETE** notification is returned to the callback routine when a queue completes a delete operation.</span></span> <span data-ttu-id="83bf2-106">Это уведомление отправляется, даже если пользователь отменяет или возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="83bf2-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDDELETE
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="83bf2-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="83bf2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="83bf2-108">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="83bf2-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="83bf2-109">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="83bf2-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="83bf2-110">Элемент **Win32Error** структуры **filePaths** указывает результат операции копирования.</span><span class="sxs-lookup"><span data-stu-id="83bf2-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of a copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="83bf2-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="83bf2-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="83bf2-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="83bf2-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="83bf2-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83bf2-113">Return value</span></span>

<span data-ttu-id="83bf2-114">Код возврата игнорируется.</span><span class="sxs-lookup"><span data-stu-id="83bf2-114">The return code is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="83bf2-115">Требования</span><span class="sxs-lookup"><span data-stu-id="83bf2-115">Requirements</span></span>



| <span data-ttu-id="83bf2-116">Требование</span><span class="sxs-lookup"><span data-stu-id="83bf2-116">Requirement</span></span> | <span data-ttu-id="83bf2-117">Значение</span><span class="sxs-lookup"><span data-stu-id="83bf2-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="83bf2-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="83bf2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="83bf2-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="83bf2-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="83bf2-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="83bf2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="83bf2-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="83bf2-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="83bf2-122">Header</span><span class="sxs-lookup"><span data-stu-id="83bf2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="83bf2-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="83bf2-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="83bf2-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="83bf2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83bf2-125">Обзор</span><span class="sxs-lookup"><span data-stu-id="83bf2-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="83bf2-126">Уведомления</span><span class="sxs-lookup"><span data-stu-id="83bf2-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="83bf2-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="83bf2-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="83bf2-128">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="83bf2-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="83bf2-129">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="83bf2-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




