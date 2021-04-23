---
title: Перечисление BG_ERROR_CONTEXT (Deliveryoptimization. h)
description: Перечисление BG_ERROR_CONTEXT определяет постоянные значения, указывающие контекст, в котором произошла ошибка.
ms.assetid: 86202343-5B5B-4A2E-A58D-7634BCB41E1C
keywords:
- Перечисление BG_ERROR_CONTEXT
topic_type:
- apiref
api_name:
- BG_ERROR_CONTEXT
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cf6c68c20a5117e6cd8a02f8b4608b494c0ea93f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490068"
---
# <a name="bg_error_context-enumeration"></a><span data-ttu-id="ebe05-104">Перечисление BG_ERROR_CONTEXT</span><span class="sxs-lookup"><span data-stu-id="ebe05-104">BG_ERROR_CONTEXT enumeration</span></span>

<span data-ttu-id="ebe05-105">Перечисление **BG_ERROR_CONTEXT** определяет постоянные значения, указывающие контекст, в котором произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="ebe05-105">The **BG_ERROR_CONTEXT** enumeration defines the constant values that specify the context in which the error occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe05-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="ebe05-106">Syntax</span></span>


```C++
typedef enum  { 
  BG_ERROR_CONTEXT_NONE                        = 0,
  BG_ERROR_CONTEXT_UNKNOWN                     = 1,
  BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER       = 2,
  BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION  = 3,
  BG_ERROR_CONTEXT_LOCAL_FILE                  = 4,
  BG_ERROR_CONTEXT_REMOTE_FILE                 = 5,
  BG_ERROR_CONTEXT_GENERAL_TRANSPORT           = 6,
  BG_ERROR_CONTEXT_REMOTE_APPLICATION          = 7
} BG_ERROR_CONTEXT;
```



## <a name="constants"></a><span data-ttu-id="ebe05-107">Константы</span><span class="sxs-lookup"><span data-stu-id="ebe05-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="ebe05-108"><span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**</span><span class="sxs-lookup"><span data-stu-id="ebe05-108"><span id="BG_ERROR_CONTEXT_NONE"></span><span id="bg_error_context_none"></span>**BG_ERROR_CONTEXT_NONE**</span></span>
</dt> <dd>

<span data-ttu-id="ebe05-109">Произошла ошибка.</span><span class="sxs-lookup"><span data-stu-id="ebe05-109">An error has not occurred.</span></span>

</dd> <dt>

<span data-ttu-id="ebe05-110"><span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**</span><span class="sxs-lookup"><span data-stu-id="ebe05-110"><span id="BG_ERROR_CONTEXT_UNKNOWN"></span><span id="bg_error_context_unknown"></span>**BG_ERROR_CONTEXT_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="ebe05-111">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ebe05-111">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ebe05-112"><span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**</span><span class="sxs-lookup"><span data-stu-id="ebe05-112"><span id="BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER"></span><span id="bg_error_context_general_queue_manager"></span>**BG_ERROR_CONTEXT_GENERAL_QUEUE_MANAGER**</span></span>
</dt> <dd>

<span data-ttu-id="ebe05-113">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ebe05-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ebe05-114"><span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**</span><span class="sxs-lookup"><span data-stu-id="ebe05-114"><span id="BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION"></span><span id="bg_error_context_queue_manager_notification"></span>**BG_ERROR_CONTEXT_QUEUE_MANAGER_NOTIFICATION**</span></span>
</dt> <dd>

<span data-ttu-id="ebe05-115">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ebe05-115">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ebe05-116"><span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**</span><span class="sxs-lookup"><span data-stu-id="ebe05-116"><span id="BG_ERROR_CONTEXT_LOCAL_FILE"></span><span id="bg_error_context_local_file"></span>**BG_ERROR_CONTEXT_LOCAL_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ebe05-117">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ebe05-117">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ebe05-118"><span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**</span><span class="sxs-lookup"><span data-stu-id="ebe05-118"><span id="BG_ERROR_CONTEXT_REMOTE_FILE"></span><span id="bg_error_context_remote_file"></span>**BG_ERROR_CONTEXT_REMOTE_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="ebe05-119">Ошибка связана с указанным удаленным файлом.</span><span class="sxs-lookup"><span data-stu-id="ebe05-119">The error was related to the specified remote file.</span></span> <span data-ttu-id="ebe05-120">Например, URL-адрес недоступен.</span><span class="sxs-lookup"><span data-stu-id="ebe05-120">For example, the URL was not accessible.</span></span>

</dd> <dt>

<span data-ttu-id="ebe05-121"><span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**</span><span class="sxs-lookup"><span data-stu-id="ebe05-121"><span id="BG_ERROR_CONTEXT_GENERAL_TRANSPORT"></span><span id="bg_error_context_general_transport"></span>**BG_ERROR_CONTEXT_GENERAL_TRANSPORT**</span></span>
</dt> <dd>

<span data-ttu-id="ebe05-122">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ebe05-122">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="ebe05-123"><span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**</span><span class="sxs-lookup"><span data-stu-id="ebe05-123"><span id="BG_ERROR_CONTEXT_REMOTE_APPLICATION"></span><span id="bg_error_context_remote_application"></span>**BG_ERROR_CONTEXT_REMOTE_APPLICATION**</span></span>
</dt> <dd>

<span data-ttu-id="ebe05-124">Не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ebe05-124">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ebe05-125">Требования</span><span class="sxs-lookup"><span data-stu-id="ebe05-125">Requirements</span></span>



| <span data-ttu-id="ebe05-126">Требование</span><span class="sxs-lookup"><span data-stu-id="ebe05-126">Requirement</span></span> | <span data-ttu-id="ebe05-127">Значение</span><span class="sxs-lookup"><span data-stu-id="ebe05-127">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe05-128">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ebe05-128">Minimum supported client</span></span><br/> | <span data-ttu-id="ebe05-129">\[Только для настольных приложений Windows 10 версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="ebe05-129">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ebe05-130">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ebe05-130">Minimum supported server</span></span><br/> | <span data-ttu-id="ebe05-131">\[Только для настольных приложений Windows Server версии 1709\]</span><span class="sxs-lookup"><span data-stu-id="ebe05-131">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ebe05-132">Header</span><span class="sxs-lookup"><span data-stu-id="ebe05-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="ebe05-133"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="ebe05-133"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ebe05-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ebe05-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe05-135">**Ибаккграундкоперрор:: возникла ошибка**</span><span class="sxs-lookup"><span data-stu-id="ebe05-135">**IBackgroundCopyError::GetError**</span></span>](ibackgroundcopyerror-geterror-method.md)
</dt> </dl>

 

 





