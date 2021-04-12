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
# <a name="asynchronous-contexts"></a>Асинхронные контексты

Контексты безопасности асинхронного SSPI позволяют вызывающим объектам продолжать работу, не блокируя и не выполняя получение уведомлений после завершения вызова. В настоящее время асинхронные контексты поддерживаются только для клиентов и серверов TLS в режиме ядра. Следующие асинхронные функции SSPI работают с асинхронными контекстами безопасности:

## <a name="async-context-management-types"></a>Типы асинхронного управления контекстом

| Имени объекта | Описание |
|-------------|--------------|
| [сспиасинкнотификаллбакк](/windows/win32/api/sspi/nc-sspi-sspiasyncnotifycallback) | Обратный вызов, используемый для уведомления о завершении асинхронного вызова SSPI. |


## <a name="async-context-management-functions"></a>Функции асинхронного управления контекстом

| Имя API | Описание |
|-------------|--------------|
| [сспикреатеасинкконтекст](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext) | Создает экземпляр класса Сспиасинкконтекст, который используется для контроля асинхронного вызова. |
| [сспиреинитасинкконтекст](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext) | Помечает асинхронный контекст для повторного использования. |
| [ссписетасинкнотификаллбакк](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) | Регистрирует обратный вызов, уведомляющий о завершении асинхронного вызова. |
| [сспиасинкконтекстрекуиреснотифи](/windows/win32/api/sspi/nf-sspi-sspiasynccontextrequiresnotify) | Определяет, требует ли данный асинхронный контекст уведомления о завершении вызова. |
| [сспижетасинккаллстатус](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus) | Возвращает текущее состояние асинхронного вызова, связанного с предоставленным контекстом.  |
| [сспифриасинкконтекст](/windows/win32/api/sspi/nf-sspi-sspifreeasynccontext) | Освобождает контекст, созданный при вызове функции Сспикреатеасинкконтекст. |

## <a name="async-sspi-functions"></a>Асинхронные функции SSPI

Следующие функции принимают асинхронный контекст в дополнение к тем же параметрам, что и их синхронные аналоги.

| Имя API | Описание |
|-------------|--------------|
| [сспиаккуирекредентиалшандлеасинк](/windows/win32/api/sspi/nf-sspi-sspiacquirecredentialshandleasynca) | Асинхронно получает маркер для существующих учетных данных субъекта безопасности. |
| [сспиакцептсекуритиконтекстасинк](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync) | Позволяет серверному компоненту транспортного приложения асинхронно устанавливать контекст безопасности между сервером и удаленным клиентом. |
| [сспиинитиализесекуритиконтекстасинк](/windows/win32/api/sspi/nf-sspi-sspiinitializesecuritycontextasynca) | Инициализирует асинхронный контекст безопасности. |
| [сспиделетесекуритиконтекстасинк](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync) | Удаляет локальные структуры данных, связанные с указанным контекстом безопасности, инициированный предыдущим вызовом функции Сспиинитиализесекуритиконтекстасинк или Сспиакцептсекуритиконтекстасинк. |
| [сспифрикредентиалшандлеасинк](/windows/win32/api/sspi/nf-sspi-sspifreecredentialshandleasync) | Освобождает маркер учетных данных. |

## <a name="api-sample"></a>Пример API

Типичный поток вызова работает следующим образом:
1) Создание контекста Сспиасинкконтекст для трассировки вызова с помощью [сспикреатеасинкконтекст](/windows/win32/api/sspi/nf-sspi-sspicreateasynccontext)
2) Регистрация [сспиасинкнотификаллбакк](/windows/win32/api/sspi/nf-sspi-sspisetasyncnotifycallback) для контекста
3) Сделать асинхронный вызов с помощью [сспиакцептсекуритиконтекстасинк](/windows/win32/api/sspi/nf-sspi-sspiacceptsecuritycontextasync)
4) Получение результата при обратном вызове с помощью [сспижетасинккаллстатус](/windows/win32/api/sspi/nf-sspi-sspigetasynccallstatus)
5) Удалите Сспиасинкконтекст с помощью [сспиделетесекуритиконтекстасинк](/windows/win32/api/sspi/nf-sspi-sspideletesecuritycontextasync). Если вы повторно используете контекст с [сспиреинитасинкконтекст](/windows/win32/api/sspi/nf-sspi-sspireinitasynccontext), вернитесь к шагу 2.

В приведенном ниже примере демонстрируется вызов Сспиакцептсекуритиконтекстасинк. Пример ожидает завершения вызова и получает результат.

При полном подтверждении SSPI Сспиакцептсекуритиконтекстасинк и Сспиинитиализесекуритиконтекстасинк будут вызываться несколько раз до тех пор, пока не будет возвращено SEC_E_OK. Сспиреинитасинкконтекст был предоставлен для простоты использования и для упрощения производительности в этом случае.

Утверждения используются для выделения предполагаемого результата успеха.

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

## <a name="see-also"></a>См. также:

[заголовок SSPI. h](/windows/win32/api/sspi/)

[Функции SSPI](/windows/win32/api/sspi/#functions)

[Структуры SSPI](/windows/win32/api/sspi/#structures)


