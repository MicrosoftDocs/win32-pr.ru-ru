---
title: Получение сообщений об ошибках из приемника
description: Получение сообщений об ошибках из приемника
ms.assetid: c948d06f-7728-4d89-8dc4-40d192c94099
keywords:
- Расширенный формат систем (ASF), сообщения об ошибках из приемников
- ASF (Расширенный системный формат), сообщения об ошибках из приемников
- Расширенный формат систем (ASF), приемники
- ASF (Расширенный системный формат), приемники
- приемники, сообщения об ошибках
- сообщения об ошибках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e432f805b5e33de0e830a2f319713bccec328d429f8eb04064d87edc56bf375c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930874"
---
# <a name="getting-error-messages-from-a-sink"></a>Получение сообщений об ошибках из приемника

Объект модуля записи не отправляет сообщения в метод обратного вызова [**ивмстатускаллбакк:: OnStatus**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstatuscallback-onstatus) . Однако можно настроить приемники записи для отправки сообщений в OnStatus. Каждый приемник должен быть настроен для доставки состояния отдельно, но все приемники могут передавать данные в один и тот же обратный вызов.

Чтобы настроить приемник для доставки сообщений о состоянии в **OnStatus**, вызовите метод [**Ивмрегистеркаллбакк:: Advise**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmregistercallback-advise) .

В следующем примере кода показано, как настроить все приемники для доставки сообщений о состоянии обратному вызову **OnStatus** . В этом примере индекс каждого приемника будет использоваться в качестве параметра контекста, чтобы метод **OnStatus** мог отличать сообщения от разных приемников. Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).


```C++
HRESULT SetSinksForStatus (IWMWriter* pWriter, IWMStatusCallback* pStatus)
{
    HRESULT hr          = S_OK;
    DWORD   cSinks      = 0;
    DWORD   dwSinkIndex = 0;

    IWMWriterAdvanced*   pWriterAdvanced = NULL;
    IWMWriterSink*       pSink           = NULL;
    IWMRegisterCallback* pRegisterCallbk = NULL;

    // Get the advanced writer interface.
    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced, 
                                 (void**)&pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    // Get the number of sinks that are added to the writer object.
    hr = pWriterAdvanced->GetSinkCount(&cSinks);
    GOTO_EXIT_IF_FAILED(hr);

    // Loop through all of the sinks.
    for(dwSinkIndex = 0; dwSinkIndex < cSinks; dwSinkIndex++)
    {
        // Get the base interface for the next sink.
        hr = pWriterAdvanced->GetSink(dwSinkIndex, &pSink);
        GOTO_EXIT_IF_FAILED(hr);

        // Get the callback registration interface for the sink.
        hr = pSink->QueryInterface(IID_IWMRegisterCallback,
                                   (void**)&pRegisterCallbk);
        GOTO_EXIT_IF_FAILED(hr);

        // Register the OnStatus callback.
        hr = pRegisterCallbk->Advise(pStatus, (void*) &dwSinkIndex);
        GOTO_EXIT_IF_FAILED(hr);

        // Release for the next iteration.
        SAFE_RELEASE(pSink);
        SAFE_RELEASE(pRegisterCallbk);
    } // end for dwSinkIndex

Exit:
    SAFE_RELEASE(pSink);
    SAFE_RELEASE(pRegisterCallbk);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Интерфейс Ивмрегистеркаллбакк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmregistercallback)
</dt> <dt>

[**Работа с приемниками модуля записи**](working-with-writer-sinks.md)
</dt> </dl>

 

 




