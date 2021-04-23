---
description: Уведомление СПФИЛЕНОТИФИ \_ ендренаме отправляется в подпрограммы обратного вызова, когда очередь завершает операцию переименования. Это уведомление отправляется, даже если пользователь отменяет или возникает ошибка.
ms.assetid: 8d5a8d17-de4f-4100-aa72-dfefeb8d4db9
title: Сообщение SPFILENOTIFY_ENDRENAME (Setupapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a316d4dfe72ee9eb7d85fdb70eb90e1cf3d3f463
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664525"
---
# <a name="spfilenotify_endrename-message"></a><span data-ttu-id="806b3-104">\_Сообщение спфиленотифи ендренаме</span><span class="sxs-lookup"><span data-stu-id="806b3-104">SPFILENOTIFY\_ENDRENAME message</span></span>

<span data-ttu-id="806b3-105">Уведомление **спфиленотифи \_ ендренаме** отправляется в подпрограммы обратного вызова, когда очередь завершает операцию переименования.</span><span class="sxs-lookup"><span data-stu-id="806b3-105">The **SPFILENOTIFY\_ENDRENAME** notification is sent to the callback routine when the queue completes a rename operation.</span></span> <span data-ttu-id="806b3-106">Это уведомление отправляется, даже если пользователь отменяет или возникает ошибка.</span><span class="sxs-lookup"><span data-stu-id="806b3-106">This notification is sent even if the user cancels or if an error occurs.</span></span>


```C++
SPFILENOTIFY_ENDRENAME
  Param1 = (UINT) FilePathInfo;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="806b3-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="806b3-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="806b3-108">*Параметр1*</span><span class="sxs-lookup"><span data-stu-id="806b3-108">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="806b3-109">Указатель на структуру [**FilePath**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) .</span><span class="sxs-lookup"><span data-stu-id="806b3-109">Pointer to a [**FILEPATHS**](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a) structure.</span></span> <span data-ttu-id="806b3-110">Элемент **Win32Error** структуры **filePaths** указывает результат операции копирования.</span><span class="sxs-lookup"><span data-stu-id="806b3-110">The **Win32Error** member of the **FILEPATHS** structure indicates the outcome of the copy operation.</span></span>

</dd> <dt>

<span data-ttu-id="806b3-111">*Param2*</span><span class="sxs-lookup"><span data-stu-id="806b3-111">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="806b3-112">Не используется.</span><span class="sxs-lookup"><span data-stu-id="806b3-112">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="806b3-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="806b3-113">Return value</span></span>

<span data-ttu-id="806b3-114">Возвращаемое значение игнорируется.</span><span class="sxs-lookup"><span data-stu-id="806b3-114">The return value is ignored.</span></span>

## <a name="requirements"></a><span data-ttu-id="806b3-115">Требования</span><span class="sxs-lookup"><span data-stu-id="806b3-115">Requirements</span></span>



| <span data-ttu-id="806b3-116">Требование</span><span class="sxs-lookup"><span data-stu-id="806b3-116">Requirement</span></span> | <span data-ttu-id="806b3-117">Значение</span><span class="sxs-lookup"><span data-stu-id="806b3-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="806b3-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="806b3-118">Minimum supported client</span></span><br/> | <span data-ttu-id="806b3-119">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="806b3-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="806b3-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="806b3-120">Minimum supported server</span></span><br/> | <span data-ttu-id="806b3-121">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="806b3-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="806b3-122">Header</span><span class="sxs-lookup"><span data-stu-id="806b3-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="806b3-123"><dt>Setupapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="806b3-123"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="806b3-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="806b3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="806b3-125">Обзор</span><span class="sxs-lookup"><span data-stu-id="806b3-125">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="806b3-126">Уведомления</span><span class="sxs-lookup"><span data-stu-id="806b3-126">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="806b3-127">**FILEPATHS**</span><span class="sxs-lookup"><span data-stu-id="806b3-127">**FILEPATHS**</span></span>](/windows/desktop/api/Setupapi/ns-setupapi-filepaths_a)
</dt> <dt>

[<span data-ttu-id="806b3-128">**сетупкоммитфилекуеуе**</span><span class="sxs-lookup"><span data-stu-id="806b3-128">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="806b3-129">**сетупдефаулткуеуекаллбакк**</span><span class="sxs-lookup"><span data-stu-id="806b3-129">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




