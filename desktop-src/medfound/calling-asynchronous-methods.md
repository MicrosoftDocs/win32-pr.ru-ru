---
description: Вызов асинхронных методов
ms.assetid: 1d8688a5-d476-457d-a0ad-e4f106ac3484
title: Вызов асинхронных методов
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bdd6e272aeb3203706f0c621b4634cf3e6c0562
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539635"
---
# <a name="calling-asynchronous-methods"></a>Вызов асинхронных методов

В Media Foundation многие операции выполняются асинхронно. Асинхронные операции могут повысить производительность, так как они не блокируют вызывающий поток. Асинхронная операция в Media Foundation определяется парой методов с соглашением об именовании **Begin..** . и **End...**. Вместе эти два метода определяют асинхронную операцию чтения в потоке.

Чтобы запустить асинхронную операцию, вызовите метод **Begin** . Метод **Begin** всегда содержит по крайней мере два параметра:

-   Указатель на интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) . Приложение должно реализовать этот интерфейс.
-   Указатель на необязательный объект состояния.

Интерфейс [**имфасинккаллбакк**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasynccallback) уведомляет приложение о завершении операции. Пример реализации этого интерфейса см. [в разделе Реализация асинхронного обратного вызова](implementing-the-asynchronous-callback.md). Объект состояния является необязательным. Если он указан, он должен реализовать интерфейс **IUnknown** . Объект состояния можно использовать для хранения любых сведений о состоянии, необходимых для обратного вызова. Если сведения о состоянии не нужны, можно присвоить этому параметру **значение NULL**. Метод **Begin** может содержать дополнительные параметры, характерные для этого метода.

Если метод **Begin** возвращает код ошибки, это означает, что операция была выполнена неудачно, а обратный вызов не будет вызываться. Если метод **Begin** завершается удачно, это означает, что операция находится в состоянии ожидания, а обратный вызов будет вызываться после завершения операции.

Например, метод [**имфбитестреам:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) запускает асинхронную операцию чтения для потока байтов:


```C++
    BYTE data[DATA_SIZE];
    ULONG cbRead = 0;

    CMyCallback *pCB = new (std::nothrow) CMyCallback(pStream, &hr);

    if (pCB == NULL)
    {
        hr = E_OUTOFMEMORY;
    }

    // Start an asynchronous request to read data.
    if (SUCCEEDED(hr))
    {
        hr = pStream->BeginRead(data, DATA_SIZE, pCB, NULL);
    }
```



Метод обратного вызова — [**имфасинккаллбакк:: Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke). Он имеет единственный параметр *пасинкресулт*, который является указателем на интерфейс [**имфасинкресулт**](/windows/desktop/api/mfobjects/nn-mfobjects-imfasyncresult) . Чтобы завершить асинхронную операцию, вызовите метод **End** , соответствующий асинхронному методу **Begin** . Метод **End** всегда принимает указатель **имфасинкресулт** . Всегда передавайте тот же указатель, который был получен в методе **Invoke** . Асинхронная операция не завершается, пока не будет вызван метод **End** . Вы можете вызвать метод **End** из метода **Invoke** или вызвать его из другого потока.

Например, чтобы выполнить [**имфбитестреам:: BeginRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-beginread) в байтовом потоке, вызовите [**Имфбитестреам:: EndRead**](/windows/desktop/api/mfobjects/nf-mfobjects-imfbytestream-endread):


```C++
    STDMETHODIMP Invoke(IMFAsyncResult* pResult)
    {
        m_hrStatus = m_pStream->EndRead(pResult, &m_cbRead);

        SetEvent(m_hEvent);

        return S_OK;
    }
```



Возвращаемое значение метода **End** указывает состояние асинхронной операции. В большинстве случаев приложение будет выполнять некоторую работу после завершения асинхронной операции, независимо от того, завершается ли она успешно. Доступно несколько параметров.

-   Выполните работу внутри метода [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) . Этот подход приемлем, если приложение никогда не блокирует вызывающий поток или ожидает чего-либо внутри метода **Invoke** . При блокировке вызывающего потока поток потоковой передачи можно заблокировать. Например, можно обновить некоторые переменные состояния, но не выполнять синхронную операцию чтения или ожидание объекта мьютекса.
-   В методе [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Задайте событие и немедленно возвратите значение. Вызывающий поток приложения ожидает события и выполняет работу при сигнале события.
-   В методе [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) Опубликуйте сообщение частного окна в окне приложения и немедленно возвратите значение. Приложение выполняет работу над циклом обработки сообщений. (Не забудьте опубликовать сообщение, вызвав **сообщение**, а не **SendMessage**, так как **SendMessage** может блокировать поток обратного вызова.)

Важно помнить, что [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) вызывается из другого потока. Приложение отвечает за то, чтобы любая работа, выполняемая внутри **вызова** , была потокобезопасной.

По умолчанию поток, вызывающий [**Invoke**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-invoke) , не делает никаких предположений о поведении объекта обратного вызова. При необходимости можно реализовать метод [**имфасинккаллбакк:: Parameters**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasynccallback-getparameters) , чтобы получить сведения о реализации обратного вызова. В противном случае этот метод может возвращать **E \_ нотимпл**:


```C++
    STDMETHODIMP GetParameters(DWORD* pdwFlags, DWORD* pdwQueue)
    {
        // Implementation of this method is optional.
        return E_NOTIMPL;
    }
```



Если в методе **Begin** указан объект состояния, его можно извлечь из метода обратного вызова, вызвав [**имфасинкресулт::**](/windows/desktop/api/mfobjects/nf-mfobjects-imfasyncresult-getstate)GetObject.

## <a name="related-topics"></a>См. также

<dl> <dt>

[Асинхронные методы обратного вызова](asynchronous-callback-methods.md)
</dt> </dl>

 

 



