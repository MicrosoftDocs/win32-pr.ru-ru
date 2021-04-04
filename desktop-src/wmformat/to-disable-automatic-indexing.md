---
title: Отключение автоматического индексирования
description: Отключение автоматического индексирования
ms.assetid: 41fe18de-3a94-4001-83ce-0bb5dd086995
keywords:
- Windows Media Format SDK, отключение автоматического индексирования
- Windows Media Format SDK, автоматическое индексирование
- Расширенный формат систем (ASF), отключение автоматического индексирования
- ASF (Расширенный системный формат), отключение автоматического индексирования
- Расширенный формат систем (ASF), автоматическое индексирование
- ASF (Расширенный системный формат), автоматическое индексирование
- индексы, отключение автоматического индексирования
- индексы, автоматическое индексирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0235ddac8093d9b1c6d40fde341ee32d078b84b7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "103987203"
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



## <a name="related-topics"></a>См. также

<dl> <dt>

[**IWMWriterFileSink3:: Жетаутоиндексинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmwriterfilesink3-getautoindexing)
</dt> <dt>

[**вмкреатевритерфилесинк**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreatewriterfilesink)
</dt> <dt>

[**Работа с индексами**](working-with-indexes.md)
</dt> </dl>

 

 




