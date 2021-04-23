---
title: Асинхронные контексты
description: Общие сведения о асинхронных контекстах и заголовке асинхронного SSPI.
ms.topic: article
ms.keywords: SSPI, Asynchronous Contexts, async contexts, Async SSPI, SSPI Async, Asynchronous SSPI, sspi,SspiAcceptSecurityContextAsync, SspiAcquireCredentialsHandleAsync, SspiAsyncContextRequiresNotify, SspiAsyncNotifyCallback, SspiCreateAsyncContext,SspiDeleteSecurityContextAsync, SspiFreeAsyncContext, SspiFreeCredentialsHandleAsync, SspiGetAsyncCallStatus, SspiInitializeSecurityContextAsync, SspiReinitAsyncContext, SspiSetAsyncNotifyCallback
ms.date: 06/23/2020
ms.openlocfilehash: e523112d35e0ddbc38c3374c67e3d81ba74a6dce
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347295"
---
# <a name="asynchronous-contexts"></a><span data-ttu-id="72a12-103">Асинхронные контексты</span><span class="sxs-lookup"><span data-stu-id="72a12-103">Asynchronous Contexts</span></span>

<span data-ttu-id="72a12-104">Контексты безопасности асинхронного SSPI позволяют вызывающим объектам продолжать работу, не блокируя и не выполняя получение уведомлений после завершения вызова.</span><span class="sxs-lookup"><span data-stu-id="72a12-104">Asynchronous SSPI security contexts allow callers to proceed without blocking and receive notifications once the call completes.</span></span> <span data-ttu-id="72a12-105">В настоящее время асинхронные контексты поддерживаются только для клиентов и серверов TLS в режиме ядра.</span><span class="sxs-lookup"><span data-stu-id="72a12-105">Asynchronous contexts are currently only supported for kernel-mode TLS clients and servers.</span></span> <span data-ttu-id="72a12-106">Следующие асинхронные функции SSPI работают с асинхронными контекстами безопасности:</span><span class="sxs-lookup"><span data-stu-id="72a12-106">The following asynchronous SSPI functions operate on asynchronous security contexts:</span></span>

## <a name="async-context-management-types"></a><span data-ttu-id="72a12-107">Типы асинхронного управления контекстом</span><span class="sxs-lookup"><span data-stu-id="72a12-107">Async context management types</span></span>

| <span data-ttu-id="72a12-108">Имени объекта</span><span class="sxs-lookup"><span data-stu-id="72a12-108">Object Name</span></span> | <span data-ttu-id="72a12-109">Описание</span><span class="sxs-lookup"><span data-stu-id="72a12-109">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="72a12-110">сспиасинкнотификаллбакк</span><span class="sxs-lookup"><span data-stu-id="72a12-110">SspiAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | <span data-ttu-id="72a12-111">Обратный вызов, используемый для уведомления о завершении асинхронного вызова SSPI.</span><span class="sxs-lookup"><span data-stu-id="72a12-111">Callback used for notifying completion of an async SSPI call.</span></span> |


## <a name="async-context-management-functions"></a><span data-ttu-id="72a12-112">Функции асинхронного управления контекстом</span><span class="sxs-lookup"><span data-stu-id="72a12-112">Async context management functions</span></span>

| <span data-ttu-id="72a12-113">Имя API</span><span class="sxs-lookup"><span data-stu-id="72a12-113">API Name</span></span> | <span data-ttu-id="72a12-114">Описание</span><span class="sxs-lookup"><span data-stu-id="72a12-114">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="72a12-115">сспикреатеасинкконтекст</span><span class="sxs-lookup"><span data-stu-id="72a12-115">SspiCreateAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | <span data-ttu-id="72a12-116">Создает экземпляр класса Сспиасинкконтекст, который используется для контроля асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="72a12-116">Creates an instance of SspiAsyncContext which is used to track the async call.</span></span> |
| [<span data-ttu-id="72a12-117">сспиреинитасинкконтекст</span><span class="sxs-lookup"><span data-stu-id="72a12-117">SspiReinitAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | <span data-ttu-id="72a12-118">Помечает асинхронный контекст для повторного использования.</span><span class="sxs-lookup"><span data-stu-id="72a12-118">Marks an async context for reuse.</span></span> |
| [<span data-ttu-id="72a12-119">ссписетасинкнотификаллбакк</span><span class="sxs-lookup"><span data-stu-id="72a12-119">SspiSetAsyncNotifyCallback</span></span>](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | <span data-ttu-id="72a12-120">Регистрирует обратный вызов, уведомляющий о завершении асинхронного вызова.</span><span class="sxs-lookup"><span data-stu-id="72a12-120">Registers a callback that is notified on async call completion.</span></span> |
| [<span data-ttu-id="72a12-121">сспиасинкконтекстрекуиреснотифи</span><span class="sxs-lookup"><span data-stu-id="72a12-121">SspiAsyncContextRequiresNotify</span></span>](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | <span data-ttu-id="72a12-122">Определяет, требует ли данный асинхронный контекст уведомления о завершении вызова.</span><span class="sxs-lookup"><span data-stu-id="72a12-122">Determines whether a given async context requires notification on completion of the call.</span></span> |
| [<span data-ttu-id="72a12-123">сспижетасинккаллстатус</span><span class="sxs-lookup"><span data-stu-id="72a12-123">SspiGetAsyncCallStatus</span></span>](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | <span data-ttu-id="72a12-124">Возвращает текущее состояние асинхронного вызова, связанного с предоставленным контекстом.</span><span class="sxs-lookup"><span data-stu-id="72a12-124">Gets the current status of an async call associated with the provided context.</span></span>  |
| [<span data-ttu-id="72a12-125">сспифриасинкконтекст</span><span class="sxs-lookup"><span data-stu-id="72a12-125">SspiFreeAsyncContext</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | <span data-ttu-id="72a12-126">Освобождает контекст, созданный при вызове функции Сспикреатеасинкконтекст.</span><span class="sxs-lookup"><span data-stu-id="72a12-126">Frees up a context created in the call to the SspiCreateAsyncContext function.</span></span> |

## <a name="async-sspi-functions"></a><span data-ttu-id="72a12-127">Асинхронные функции SSPI</span><span class="sxs-lookup"><span data-stu-id="72a12-127">Async SSPI functions</span></span>

<span data-ttu-id="72a12-128">Следующие функции принимают асинхронный контекст в дополнение к тем же параметрам, что и их синхронные аналоги.</span><span class="sxs-lookup"><span data-stu-id="72a12-128">The following functions accept an async context in addition to all the same parameters as their synchronous counterpart.</span></span>

| <span data-ttu-id="72a12-129">Имя API</span><span class="sxs-lookup"><span data-stu-id="72a12-129">API Name</span></span> | <span data-ttu-id="72a12-130">Описание</span><span class="sxs-lookup"><span data-stu-id="72a12-130">Description</span></span> |
|-------------|--------------|
| [<span data-ttu-id="72a12-131">сспиаккуирекредентиалшандлеасинк</span><span class="sxs-lookup"><span data-stu-id="72a12-131">SspiAcquireCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | <span data-ttu-id="72a12-132">Асинхронно получает маркер для существующих учетных данных субъекта безопасности.</span><span class="sxs-lookup"><span data-stu-id="72a12-132">Asynchronously acquires a handle to preexisting credentials of a security principal.</span></span> |
| [<span data-ttu-id="72a12-133">сспиакцептсекуритиконтекстасинк</span><span class="sxs-lookup"><span data-stu-id="72a12-133">SspiAcceptSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | <span data-ttu-id="72a12-134">Позволяет серверному компоненту транспортного приложения асинхронно устанавливать контекст безопасности между сервером и удаленным клиентом.</span><span class="sxs-lookup"><span data-stu-id="72a12-134">Lets the server component of a transport application asynchronously establish a security context between the server and a remote client.</span></span> |
| [<span data-ttu-id="72a12-135">сспиинитиализесекуритиконтекстасинк</span><span class="sxs-lookup"><span data-stu-id="72a12-135">SspiInitializeSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | <span data-ttu-id="72a12-136">Инициализирует асинхронный контекст безопасности.</span><span class="sxs-lookup"><span data-stu-id="72a12-136">Initializes an async security context.</span></span> |
| [<span data-ttu-id="72a12-137">сспиделетесекуритиконтекстасинк</span><span class="sxs-lookup"><span data-stu-id="72a12-137">SspiDeleteSecurityContextAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | <span data-ttu-id="72a12-138">Удаляет локальные структуры данных, связанные с указанным контекстом безопасности, инициированный предыдущим вызовом функции Сспиинитиализесекуритиконтекстасинк или Сспиакцептсекуритиконтекстасинк.</span><span class="sxs-lookup"><span data-stu-id="72a12-138">Deletes the local data structures associated with the specified security context initiated by a previous call to the SspiInitializeSecurityContextAsync function or the SspiAcceptSecurityContextAsync function.</span></span> |
| [<span data-ttu-id="72a12-139">сспифрикредентиалшандлеасинк</span><span class="sxs-lookup"><span data-stu-id="72a12-139">SspiFreeCredentialsHandleAsync</span></span>](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | <span data-ttu-id="72a12-140">Освобождает маркер учетных данных.</span><span class="sxs-lookup"><span data-stu-id="72a12-140">Frees up a credential handle.</span></span> |

## <a name="api-sample"></a><span data-ttu-id="72a12-141">Пример API</span><span class="sxs-lookup"><span data-stu-id="72a12-141">API Sample</span></span>

<span data-ttu-id="72a12-142">Типичный поток вызова работает следующим образом:</span><span class="sxs-lookup"><span data-stu-id="72a12-142">A typical call flow works as follows:</span></span>
1) <span data-ttu-id="72a12-143">Создание контекста Сспиасинкконтекст для трассировки вызова с помощью [сспикреатеасинкконтекст](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span><span class="sxs-lookup"><span data-stu-id="72a12-143">Create SspiAsyncContext context to track call using [SspiCreateAsyncContext](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)</span></span>
2) <span data-ttu-id="72a12-144">Регистрация [сспиасинкнотификаллбакк](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) для контекста</span><span class="sxs-lookup"><span data-stu-id="72a12-144">Register an [SspiAsyncNotifyCallback](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) for the context</span></span>
3) <span data-ttu-id="72a12-145">Сделать асинхронный вызов с помощью [сспиакцептсекуритиконтекстасинк](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span><span class="sxs-lookup"><span data-stu-id="72a12-145">Make the async call using [SspiAcceptSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)</span></span>
4) <span data-ttu-id="72a12-146">Получение результата при обратном вызове с помощью [сспижетасинккаллстатус](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span><span class="sxs-lookup"><span data-stu-id="72a12-146">On callback, retrieve the result using [SspiGetAsyncCallStatus](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)</span></span>
5) <span data-ttu-id="72a12-147">Удалите Сспиасинкконтекст с помощью [сспиделетесекуритиконтекстасинк](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span><span class="sxs-lookup"><span data-stu-id="72a12-147">Delete SspiAsyncContext using [SspiDeleteSecurityContextAsync](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync).</span></span> <span data-ttu-id="72a12-148">Если вы повторно используете контекст с [сспиреинитасинкконтекст](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), вернитесь к шагу 2.</span><span class="sxs-lookup"><span data-stu-id="72a12-148">If reusing the context with [SspiReinitAsyncContext](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), go back to step 2.</span></span>

<span data-ttu-id="72a12-149">В приведенном ниже примере демонстрируется вызов Сспиакцептсекуритиконтекстасинк.</span><span class="sxs-lookup"><span data-stu-id="72a12-149">The sample below demonstrates an invocation of SspiAcceptSecurityContextAsync.</span></span> <span data-ttu-id="72a12-150">Пример ожидает завершения вызова и получает результат.</span><span class="sxs-lookup"><span data-stu-id="72a12-150">The sample waits for the call to complete and retrieves the result.</span></span>

<span data-ttu-id="72a12-151">При полном подтверждении SSPI Сспиакцептсекуритиконтекстасинк и Сспиинитиализесекуритиконтекстасинк будут вызываться несколько раз до тех пор, пока не будет возвращено SEC_E_OK.</span><span class="sxs-lookup"><span data-stu-id="72a12-151">In a full SSPI handshake, SspiAcceptSecurityContextAsync and SspiInitializeSecurityContextAsync would be called multiple times until SEC_E_OK is returned.</span></span> <span data-ttu-id="72a12-152">Сспиреинитасинкконтекст был предоставлен для простоты использования и для упрощения производительности в этом случае.</span><span class="sxs-lookup"><span data-stu-id="72a12-152">SspiReinitAsyncContext has been provided for ease of use and to facilitate performance in this case.</span></span>

<span data-ttu-id="72a12-153">Утверждения используются для выделения предполагаемого результата успеха.</span><span class="sxs-lookup"><span data-stu-id="72a12-153">Asserts are used to highlight what we would expect in the case of success.</span></span>

```cpp
#include <sspi.h>

void AsyncCallCompleted(
    _In_     SspiAsyncContext* AsyncContext,
    _In_opt_ PVOID pCallbackData
)
{
    // Get result.
    SECURITY_STATUS Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_E_OK == Status);

    // *Perform any needed callback actions, use pCallbackData if needed*

    // Clean up async context when done.
    SspiFreeAsyncContext(AsyncContext);
}

void DoASCCall(
    _In_opt_  PCredHandle    phCred,
    _In_opt_  PCtxtHandle    phContext,
    _In_opt_  PSecBufferDesc pInput,
    _In_opt_  PSecBufferDesc pOutput,
    _Out_     unsigned long* pfContextAttr,
    _Out_opt_ PTimeStamp     ptsExpiry
)
{
    // Create context for async call
    SspiAsyncContext* AsyncContext = SspiCreateAsyncContext();

    // Check for out of memory condition
    ASSERT(AsyncContext);

    // Register callback that continues execution upon completion.
    PVOID pCallbackData = … ; // *Setup any state needed for callback.*
    SECURITY_STATUS Status = SspiSetAsyncNotifyCallback(AsyncContext,
                                        AsyncCallCompleted,
                                        pCallbackData);
    ASSERT(SEC_E_OK == Status);

    // Queue asynchronous call.
    Status = SspiAcceptSecurityContextAsync(AsyncContext,
                                            phCred,
                                            phContext,
                                            pInput,
                                            ASC_REQ_CONNECTION,
                                            SECURITY_NATIVE_DREP,
                                            phContext,
                                            pOutput,
                                            pfContextAttr,
                                            ptsExpiry);

    // All async functions return the status of queueing the async call,
    // not the call’s result.
    ASSERT(SEC_E_OK == Status);

    // At this point, the call can be pending or complete.
    // If complete, the result or error is returned.
    // For this example, we assume if it finished, it finished with SEC_E_OK.
    Status = SspiGetAsyncCallStatus(AsyncContext);
    ASSERT(SEC_I_ASYNC_CALL_PENDING == Status ||
           SEC_E_OK == Status);

    // Execution will continue in the callback upon completion
}

```

## <a name="see-also"></a><span data-ttu-id="72a12-154">См. также:</span><span class="sxs-lookup"><span data-stu-id="72a12-154">See Also</span></span>

[<span data-ttu-id="72a12-155">заголовок SSPI. h</span><span class="sxs-lookup"><span data-stu-id="72a12-155">sspi.h header</span></span>](/windows/win32/api/sspi/)

[<span data-ttu-id="72a12-156">Функции SSPI</span><span class="sxs-lookup"><span data-stu-id="72a12-156">SSPI functions</span></span>](/windows/win32/api/sspi/#functions)

[<span data-ttu-id="72a12-157">Структуры SSPI</span><span class="sxs-lookup"><span data-stu-id="72a12-157">SSPI structures</span></span>](/windows/win32/api/sspi/#structures)


