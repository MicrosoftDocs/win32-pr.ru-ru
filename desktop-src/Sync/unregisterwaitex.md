---
description: Отменяет зарегистрированную операцию ожидания, выданную функцией RegisterWaitForSingleObject.
ms.assetid: ea700e55-fce7-46cd-bb96-0c129b429d46
title: Функция UnregisterWaitEx (Среадпуллегациаписет. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- UnregisterWaitEx
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-threadpool-l1-1-0.dll
- KernelBase.dll
- API-MS-Win-Core-threadpool-legacy-l1-1-0.dll
- API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
- MinKernelBase.dll
ms.openlocfilehash: 30f5ad5f88bec9eb7eebff5a73d8f84f633cb249
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910023"
---
# <a name="unregisterwaitex-function"></a><span data-ttu-id="038ac-103">Функция UnregisterWaitEx</span><span class="sxs-lookup"><span data-stu-id="038ac-103">UnregisterWaitEx function</span></span>

<span data-ttu-id="038ac-104">Отменяет зарегистрированную операцию ожидания, выданную функцией [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="038ac-104">Cancels a registered wait operation issued by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

## <a name="syntax"></a><span data-ttu-id="038ac-105">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="038ac-105">Syntax</span></span>


```C++
BOOL WINAPI UnregisterWaitEx(
  _In_     HANDLE WaitHandle,
  _In_opt_ HANDLE CompletionEvent
);
```



## <a name="parameters"></a><span data-ttu-id="038ac-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="038ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="038ac-107">*WaitHandle* \[ окне\]</span><span class="sxs-lookup"><span data-stu-id="038ac-107">*WaitHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="038ac-108">Дескриптор ожидания.</span><span class="sxs-lookup"><span data-stu-id="038ac-108">The wait handle.</span></span> <span data-ttu-id="038ac-109">Этот маркер возвращается функцией [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) .</span><span class="sxs-lookup"><span data-stu-id="038ac-109">This handle is returned by the [**RegisterWaitForSingleObject**](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject) function.</span></span>

</dd> <dt>

<span data-ttu-id="038ac-110">*Комплетионевент* \[ в необязательное\]</span><span class="sxs-lookup"><span data-stu-id="038ac-110">*CompletionEvent* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="038ac-111">Дескриптор объекта события, который должен быть сигнальным при отмене регистрации операции ожидания.</span><span class="sxs-lookup"><span data-stu-id="038ac-111">A handle to the event object to be signaled when the wait operation has been unregistered.</span></span> <span data-ttu-id="038ac-112">Этот параметр может принимать значение **NULL**.</span><span class="sxs-lookup"><span data-stu-id="038ac-112">This parameter can be **NULL**.</span></span>

<span data-ttu-id="038ac-113">Если этот параметр имеет **недопустимое \_ \_ значение Handle**, функция ожидает завершения всех функций обратного вызова перед возвратом.</span><span class="sxs-lookup"><span data-stu-id="038ac-113">If this parameter is **INVALID\_HANDLE\_VALUE**, the function waits for all callback functions to complete before returning.</span></span>

<span data-ttu-id="038ac-114">Если этот параметр имеет **значение NULL**, функция помечает таймер для удаления и сразу же возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="038ac-114">If this parameter is **NULL**, the function marks the timer for deletion and returns immediately.</span></span> <span data-ttu-id="038ac-115">Однако большинство вызывающих объектов должны ждать завершения функции обратного вызова, чтобы они могли выполнить необходимую очистку.</span><span class="sxs-lookup"><span data-stu-id="038ac-115">However, most callers should wait for the callback function to complete so they can perform any needed cleanup.</span></span>

<span data-ttu-id="038ac-116">Если вызывающий объект предоставляет это событие, функция завершается успешно или функция завершается с **ошибкой ввода-вывода с ошибками \_ \_**, не закрывайте событие до тех пор, пока не будет получен сигнал.</span><span class="sxs-lookup"><span data-stu-id="038ac-116">If the caller provides this event and the function succeeds or the function fails with **ERROR\_IO\_PENDING**, do not close the event until it is signaled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="038ac-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="038ac-117">Return value</span></span>

<span data-ttu-id="038ac-118">Если функция выполняется успешно, возвращается ненулевое значение.</span><span class="sxs-lookup"><span data-stu-id="038ac-118">If the function succeeds, the return value is nonzero.</span></span>

<span data-ttu-id="038ac-119">Если функция выполняется неудачно, возвращается нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="038ac-119">If the function fails, the return value is zero.</span></span> <span data-ttu-id="038ac-120">Дополнительные сведения об ошибке можно получить, вызвав [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span><span class="sxs-lookup"><span data-stu-id="038ac-120">To get extended error information, call [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).</span></span>

## <a name="remarks"></a><span data-ttu-id="038ac-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="038ac-121">Remarks</span></span>

<span data-ttu-id="038ac-122">Невозможно сделать блокирующий вызов **UnregisterWaitEx** из функции обратного вызова для той же операции ожидания.</span><span class="sxs-lookup"><span data-stu-id="038ac-122">You cannot make a blocking call to **UnregisterWaitEx** from within a callback function for the same wait operation.</span></span> <span data-ttu-id="038ac-123">В противном случае обратный вызов будет ожидать завершения.</span><span class="sxs-lookup"><span data-stu-id="038ac-123">Otherwise, the callback will be waiting for itself to finish.</span></span> <span data-ttu-id="038ac-124">Как правило, при блокирующем вызове **UnregisterWaitEx** создается зависимость между текущим потоком и обратным вызовом, поэтому для блокирования вызова отмены регистрации в другой операции ожидания необходимо убедиться, что функции обратного вызова не зависят друг от друга и что вторая операция ожидания не выполняет блокирование вызова отмены регистрации для первой операции.</span><span class="sxs-lookup"><span data-stu-id="038ac-124">In general, a blocking call to **UnregisterWaitEx** creates a dependency between the current thread and the callback, so to make a blocking unregister call on another wait operation, you must ensure that the callback functions do not depend on one another and that the second wait operation does not also perform a blocking unregister call on the first operation.</span></span>

<span data-ttu-id="038ac-125">Будьте внимательны при выполнении блокирующего вызова **UnregisterWaitEx** в постоянном потоке.</span><span class="sxs-lookup"><span data-stu-id="038ac-125">Be careful when making a blocking **UnregisterWaitEx** call on a persistent thread.</span></span> <span data-ttu-id="038ac-126">Если операция ожидания, для которой выполняется отмена регистрации, была создана с помощью **WT \_ ексекутеинперсистентсреад**, может возникнуть взаимоблокировка.</span><span class="sxs-lookup"><span data-stu-id="038ac-126">If the wait operation being unregistered was created with **WT\_EXECUTEINPERSISTENTTHREAD**, a deadlock may occur.</span></span>

<span data-ttu-id="038ac-127">После выполнения неблокирующего вызова **UnregisterWaitEx** никакие новые функции обратного вызова, связанные с *WaitHandle* , не могут быть поставлены в очередь.</span><span class="sxs-lookup"><span data-stu-id="038ac-127">After making non-blocking call to **UnregisterWaitEx**, no new callback functions associated with *WaitHandle* can be queued.</span></span> <span data-ttu-id="038ac-128">Однако могут существовать ожидающие функции обратного вызова, уже поставленные в очередь рабочим потокам.</span><span class="sxs-lookup"><span data-stu-id="038ac-128">However, there may be pending callback functions already queued to worker threads.</span></span>

<span data-ttu-id="038ac-129">В некоторых случаях функция завершится с **ошибкой ввода- \_ вывода \_** , если *комплетионевент* имеет **значение NULL**.</span><span class="sxs-lookup"><span data-stu-id="038ac-129">Under some conditions, the function will fail with **ERROR\_IO\_PENDING** if *CompletionEvent* is **NULL**.</span></span> <span data-ttu-id="038ac-130">Это означает, что существуют необработанные функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="038ac-130">This indicates that there are outstanding callback functions.</span></span> <span data-ttu-id="038ac-131">Эти обратные вызовы будут выполняться или находиться в процессе выполнения.</span><span class="sxs-lookup"><span data-stu-id="038ac-131">Those callbacks either will execute or are in the middle of executing.</span></span>

<span data-ttu-id="038ac-132">Если *комплетионевент* является обработчиком события, предоставленного вызывающим объектом, функция может завершиться успешно, завершиться с **ошибкой ввода- \_ вывода \_ с ошибками** или завершиться с другим кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="038ac-132">If *CompletionEvent* is a handle to an event provided by the caller, it is possible for the function to succeed, fail with **ERROR\_IO\_PENDING**, or fail with a different error code.</span></span> <span data-ttu-id="038ac-133">Если функция завершается успешно или если функция завершается с **ошибкой \_ ввода-вывода в режиме \_ ожидания**, вызывающий объект всегда должен ждать, пока событие не закроет событие.</span><span class="sxs-lookup"><span data-stu-id="038ac-133">If the function succeeds, or if the function fails with **ERROR\_IO\_PENDING**, the caller should always wait until the event is signaled to close the event.</span></span> <span data-ttu-id="038ac-134">Если функция завершается с другим кодом ошибки, нет необходимости ждать, пока событие не будет сигнальным, чтобы закрыть событие.</span><span class="sxs-lookup"><span data-stu-id="038ac-134">If the function fails with a different error code, it is not necessary to wait until the event is signaled to close the event.</span></span>

<span data-ttu-id="038ac-135">**Windows XP:** Если *комплетионевент* является дескриптором события, предоставленного вызывающим объектом, и функция завершается с **ошибкой ввода-вывода с ошибками \_ \_**, вызывающий объект должен подождать, пока событие не закроет событие.</span><span class="sxs-lookup"><span data-stu-id="038ac-135">**Windows XP:** If *CompletionEvent* is a handle to an event provided by the caller and the function fails with **ERROR\_IO\_PENDING**, the caller should wait until the event is signaled to close the event.</span></span> <span data-ttu-id="038ac-136">Это поведение изменилось, начиная с Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="038ac-136">This behavior changed starting with Windows Vista.</span></span>

<span data-ttu-id="038ac-137">Чтобы скомпилировать приложение, использующее эту функцию, определите **\_ Win32 \_ WinNT** как 0x0500 или более поздней версии.</span><span class="sxs-lookup"><span data-stu-id="038ac-137">To compile an application that uses this function, define **\_WIN32\_WINNT** as 0x0500 or later.</span></span> <span data-ttu-id="038ac-138">Дополнительные сведения см. [в разделе Использование заголовков Windows](../winprog/using-the-windows-headers.md).</span><span class="sxs-lookup"><span data-stu-id="038ac-138">For more information, see [Using the Windows Headers](../winprog/using-the-windows-headers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="038ac-139">Требования</span><span class="sxs-lookup"><span data-stu-id="038ac-139">Requirements</span></span>



| <span data-ttu-id="038ac-140">Требование</span><span class="sxs-lookup"><span data-stu-id="038ac-140">Requirement</span></span> | <span data-ttu-id="038ac-141">Значение</span><span class="sxs-lookup"><span data-stu-id="038ac-141">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="038ac-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="038ac-142">Minimum supported client</span></span><br/> | <span data-ttu-id="038ac-143">Только для \[ классических приложений Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="038ac-143">Windows XP \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="038ac-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="038ac-144">Minimum supported server</span></span><br/> | <span data-ttu-id="038ac-145">\[Только для настольных приложений Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="038ac-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="038ac-146">Header</span><span class="sxs-lookup"><span data-stu-id="038ac-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="038ac-147"><dt>Среадпуллегациаписет. h в Windows 8 и Windows Server 2012 (Включите Windows. h); </dt> <dt>Винбасе. h в Windows 7, Windows server 2008 R2, Windows Vista, Windows server 2008, Windows XP и Windows server 2003 (включая Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="038ac-147"><dt>Threadpoollegacyapiset.h on Windows 8 and Windows Server 2012 (include Windows.h); </dt> <dt>WinBase.h on Windows 7, Windows Server 2008 R2, Windows Vista, Windows Server 2008, Windows XP and Windows Server 2003 (include Windows.h)</dt></span></span> </dl> |
| <span data-ttu-id="038ac-148">Библиотека</span><span class="sxs-lookup"><span data-stu-id="038ac-148">Library</span></span><br/>                  | <dl> <span data-ttu-id="038ac-149"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="038ac-149"><dt>Kernel32.lib</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="038ac-150">DLL</span><span class="sxs-lookup"><span data-stu-id="038ac-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="038ac-151"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="038ac-151"><dt>Kernel32.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                        |



## <a name="see-also"></a><span data-ttu-id="038ac-152">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="038ac-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="038ac-153">**RegisterWaitForSingleObject**</span><span class="sxs-lookup"><span data-stu-id="038ac-153">**RegisterWaitForSingleObject**</span></span>](/windows/desktop/api/WinBase/nf-winbase-registerwaitforsingleobject)
</dt> <dt>

[<span data-ttu-id="038ac-154">Функции синхронизации</span><span class="sxs-lookup"><span data-stu-id="038ac-154">Synchronization Functions</span></span>](synchronization-functions.md)
</dt> <dt>

[<span data-ttu-id="038ac-155">Группировка потоков в пул</span><span class="sxs-lookup"><span data-stu-id="038ac-155">Thread Pooling</span></span>](../procthread/thread-pooling.md)
</dt> </dl>

 

 
