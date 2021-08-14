---
title: Отключение автоматического индексирования
description: Отключение автоматического индексирования
ms.assetid: 41fe18de-3a94-4001-83ce-0bb5dd086995
keywords:
- Windows Пакет SDK для формата мультимедиа, отключение автоматического индексирования
- Windows Пакет SDK для формата мультимедиа, автоматическое индексирование
- Расширенный формат систем (ASF), отключение автоматического индексирования
- ASF (Расширенный системный формат), отключение автоматического индексирования
- Расширенный формат систем (ASF), автоматическое индексирование
- ASF (Расширенный системный формат), автоматическое индексирование
- индексы, отключение автоматического индексирования
- индексы, автоматическое индексирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61f3b63d58b8f9a0fbbdff88369832b67abca7d9f11a39c56613c6e5d867d6a7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118699915"
---
# <a name="to-disable-automatic-indexing"></a>Отключение автоматического индексирования

При записи файла ASF не всегда требуется создавать индекс по умолчанию. Вы можете отключить автоматическое индексирование с помощью метода [**IWMWriterFileSink3:: сетаутоиндексинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-setautoindexing) .

В следующем примере кода показано, как отключить автоматическое индексирование с помощью модуля записи.


```C++
IWMWriterFileSink*  pBaseFileSink = NULL;
IWMWriterFileSink3* pMySink       = NULL;

BOOL    fAutoIndex;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create a writer file sink.
hr = WMCreateWriterFileSink(&pBaseFileSink);

// Retrieve an IWMWriterFileSink3 interface pointer for the new sink.
hr = pBaseFileSink->QueryInterface(IID_IWMWriterFileSink3,
                                    (void**)&pMySink);

// Release the base file sink.
pBaseFileSink->Release();
pBaseFileSink = NULL;

// Check the state of automatic indexing.
hr = pMySink->GetAutoIndexing(&fAutoIndex);

// If auto indexing is enabled, turn it off.
if(fAutoIndex)
   pMySink->SetAutoIndexing(FALSE);

// You can now write to this sink and the file will not have an index.

// Release the remaining interface.
pMySink->Release();
pMySink = NULL;

```



## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IWMWriterFileSink3:: Жетаутоиндексинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getautoindexing)
</dt> <dt>

[**вмкреатевритерфилесинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)
</dt> <dt>

[**Работа с индексами**](working-with-indexes.md)
</dt> </dl>

 

 




