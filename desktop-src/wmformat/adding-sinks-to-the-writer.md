---
title: Добавление приемников в модуль записи
description: Добавление приемников в модуль записи
ms.assetid: 714b84f0-5ad8-4e00-aa77-e866e65b43b0
keywords:
- Расширенный системный формат (ASF), Добавление приемников в модуль записи
- ASF (Расширенный системный формат), Добавление приемников в модуль записи
- Расширенный формат систем (ASF), приемники
- ASF (Расширенный системный формат), приемники
- Расширенный формат систем (ASF), приемники записи
- ASF (Расширенный системный формат), приемники записи
- приемники, добавление в модуль записи
- Приемники модуля записи, добавление
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aca64b412dd83e9bbba1d8de66b2aef335573c9e50073c2afe898fed0c34761b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119810024"
---
# <a name="adding-sinks-to-the-writer"></a>Добавление приемников в модуль записи

Приемники модуля записи — это отдельные объекты из модуля записи, которые необходимо добавить в модуль записи для использования. При записи в файл можно просто вызвать [**ивмвритер:: сетаутпутфиленаме**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriter-setoutputfilename), который автоматически настроит приемник файла. В противном случае для добавления приемника в модуль записи вызовите метод [**ивмвритерадванцед:: аддсинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-addsink) . **Аддсинк** требует указатель на интерфейс [**ивмвритерсинк**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwritersink) приемника.

По завершении использования приемника его необходимо закрыть, вызвав соответствующий метод, в зависимости от типа приемника, а затем удалить его из модуля записи, вызвав [**ивмвритерадванцед:: ремовесинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriteradvanced-removesink).

В следующем примере кода показано, как создать приемник файла модуля записи и добавить его в модуль записи. Дополнительные сведения об использовании этого кода см. [в разделе Использование примеров кода](using-the-code-examples.md).


```C++
HRESULT AddFileSink(IWMWriterFileSink** ppFileSink, IWMWriter* pWriter)
{
    HRESULT hr = S_OK;
    IWMWriterSink*     pSinkBase       = NULL;
    IWMWriterAdvanced* pWriterAdvanced = NULL;

    hr = CreateWriterFileSink(ppFileSink);
    GOTO_EXIT_IF_FAILED(hr);

    hr = *ppFileSink->QueryInterface(IID_IWMWriterSink, 
                                     (void**) &pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriter->QueryInterface(IID_IWMWriterAdvanced,
                                 (void**) &pWriterAdvanced);
    GOTO_EXIT_IF_FAILED(hr);

    hr = pWriterAdvanced->AddSink(pSinkBase);
    GOTO_EXIT_IF_FAILED(hr);

Exit:
    SAFE_RELEASE(pSinkBase);
    SAFE_RELEASE(pWriterAdvanced);
    return hr;
}

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**Получение сообщений об ошибках из приемника**](getting-error-messages-from-a-sink.md)
</dt> <dt>

[**Интерфейс Ивмвритерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmwriteradvanced)
</dt> <dt>

[**Работа с приемниками модуля записи**](working-with-writer-sinks.md)
</dt> </dl>

 

 




