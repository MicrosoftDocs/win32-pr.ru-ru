---
description: Функции прототипа обработчика событий используются для всех функций, которые обрабатывают события уведомлений Winlogon.
ms.assetid: 99b91e80-5e4e-4119-89aa-c0a80fce69e3
title: Функция обратного вызова прототипа функции обработчика событий
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Event_Handler_Function_Name
api_type:
- UserDefined
api_location: ''
ms.openlocfilehash: 935ddac5660c814b898be17218d879678f2135ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105651103"
---
# <a name="event-handler-function-prototype-callback-function"></a><span data-ttu-id="a459d-103">Функция обратного вызова прототипа функции обработчика событий</span><span class="sxs-lookup"><span data-stu-id="a459d-103">Event Handler Function Prototype callback function</span></span>

<span data-ttu-id="a459d-104">\[Функции прототипа обработчика событий больше не доступны для использования в Windows Server 2008 и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="a459d-104">\[Event Handler Prototype functions are no longer available for use as of Windows Server 2008 and Windows Vista.</span></span> <span data-ttu-id="a459d-105">\]</span><span class="sxs-lookup"><span data-stu-id="a459d-105">\]</span></span>

<span data-ttu-id="a459d-106">Функции прототипа обработчика событий используются для всех функций, которые обрабатывают события уведомлений [*Winlogon*](/windows/desktop/SecGloss/w-gly) .</span><span class="sxs-lookup"><span data-stu-id="a459d-106">Event Handler Prototype functions are used for all functions that handle [*Winlogon*](/windows/desktop/SecGloss/w-gly) notification events.</span></span> <span data-ttu-id="a459d-107">Имя функции, представленное ниже *\_ \_ \_ имени функции обработчика событий* заполнителя, обычно отражает имя события, обрабатываемого функцией.</span><span class="sxs-lookup"><span data-stu-id="a459d-107">The name of the function, represented below by the place holder *Event\_Handler\_Function\_Name*, typically reflects the name of the event that the function handles.</span></span> <span data-ttu-id="a459d-108">Например, функция, обрабатывающая события входа в систему, может называться: **влевентлогон**.</span><span class="sxs-lookup"><span data-stu-id="a459d-108">For example, the function that handles logon events might be named: **WLEventLogon**.</span></span>

## <a name="syntax"></a><span data-ttu-id="a459d-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="a459d-109">Syntax</span></span>


```C++
void Event_Handler_Function_Name(
  _In_ PWLX_NOTIFICATION_INFO pInfo
);
```



## <a name="parameters"></a><span data-ttu-id="a459d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a459d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a459d-111">*пинфо* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="a459d-111">*pInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a459d-112">Указатель на структуру [**\_ \_ сведений об уведомлении влкс**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) , которая содержит подробные сведения о событии.</span><span class="sxs-lookup"><span data-stu-id="a459d-112">A pointer to a [**WLX\_NOTIFICATION\_INFO**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_notification_info) structure that contains the details of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a459d-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a459d-113">Return value</span></span>

<span data-ttu-id="a459d-114">Эта функция обратного вызова не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="a459d-114">This callback function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a459d-115">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a459d-115">Remarks</span></span>

<span data-ttu-id="a459d-116">Если обработчику событий необходимо создать дочерние процессы, он должен вызвать функцию [**параметр CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) .</span><span class="sxs-lookup"><span data-stu-id="a459d-116">If your event handler needs to create child processes, it should call the [**CreateProcessAsUser**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessasusera) function.</span></span> <span data-ttu-id="a459d-117">В противном случае новый процесс будет создан на рабочем столе Winlogon, а не на рабочем столе пользователя.</span><span class="sxs-lookup"><span data-stu-id="a459d-117">Otherwise, the new process will be created on the Winlogon desktop, not the user's desktop.</span></span>

## <a name="examples"></a><span data-ttu-id="a459d-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="a459d-118">Examples</span></span>

<span data-ttu-id="a459d-119">В следующем примере показано, как реализовать обработчики событий для событий Winlogon.</span><span class="sxs-lookup"><span data-stu-id="a459d-119">The following sample shows how to implement event handlers for Winlogon events.</span></span> <span data-ttu-id="a459d-120">Для простоты отображаются только реализации обработчиков событий входа и выхода из системы.</span><span class="sxs-lookup"><span data-stu-id="a459d-120">For simplicity, only the implementations of the Logon and Logoff event handlers are shown.</span></span> <span data-ttu-id="a459d-121">Обработчики для остальных событий можно реализовать точно таким же образом.</span><span class="sxs-lookup"><span data-stu-id="a459d-121">You can implement handlers for the rest of the events in exactly the same manner.</span></span>


```C++
// Copyright (C) Microsoft. All rights reserved. 
#include <windows.h>

// Here is the entrance function for the DLL.
BOOL WINAPI LibMain(HINSTANCE hInstance, DWORD dwReason, LPVOID lpReserved)
{
    switch (dwReason)
    {
        case DLL_PROCESS_ATTACH:
            {

             // Disable DLL_THREAD_ATTACH & DLL_THREAD_DETACH
             // notification calls. This is a performance optimization
             // for multithreaded applications that do not need 
             // thread-level notifications of attachment or
             // detachment.

            DisableThreadLibraryCalls (hInstance);
            }
            break;
    }

    return TRUE;
}

// Here is the event handler for the Winlogon Logon event.
void WLEventLogon (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogon.\r\n"));
}

// Here is the event handler for the Winlogon Logoff event.
void WLEventLogoff (PWLX_NOTIFICATION_INFO pInfo)
{

    // Print the name of the handler to debug output.
    // You can replace this with more useful functionality.
    OutputDebugString (TEXT("NOTIFY:  Entering WLEventLogff.\r\n"));
}
```



## <a name="requirements"></a><span data-ttu-id="a459d-122">Требования</span><span class="sxs-lookup"><span data-stu-id="a459d-122">Requirements</span></span>



| <span data-ttu-id="a459d-123">Требование</span><span class="sxs-lookup"><span data-stu-id="a459d-123">Requirement</span></span> | <span data-ttu-id="a459d-124">Значение</span><span class="sxs-lookup"><span data-stu-id="a459d-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a459d-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a459d-125">Minimum supported client</span></span><br/> | <span data-ttu-id="a459d-126">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="a459d-126">Windows XP \[desktop apps only\]</span></span><br/>          |
| <span data-ttu-id="a459d-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a459d-127">Minimum supported server</span></span><br/> | <span data-ttu-id="a459d-128">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="a459d-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a459d-129">Окончание поддержки клиента</span><span class="sxs-lookup"><span data-stu-id="a459d-129">End of client support</span></span><br/>    | <span data-ttu-id="a459d-130">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a459d-130">Windows XP</span></span><br/>                                |
| <span data-ttu-id="a459d-131">Поддержка конца сервера</span><span class="sxs-lookup"><span data-stu-id="a459d-131">End of server support</span></span><br/>    | <span data-ttu-id="a459d-132">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="a459d-132">Windows Server 2003</span></span><br/>                       |



 

