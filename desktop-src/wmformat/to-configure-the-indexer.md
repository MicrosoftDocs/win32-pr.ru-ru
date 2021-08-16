---
title: Настройка индексатора
description: Настройка индексатора
ms.assetid: 0e28e8dd-1586-45e6-8a08-5245d465d068
keywords:
- Windows Пакет SDK для формата мультимедиа, Настройка индексаторов
- Расширенный системный формат (ASF), Настройка индексаторов
- ASF (Расширенный системный формат), Настройка индексаторов
- индексы, Настройка индексаторов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da5a624a4ed9ae749559a1908e3809500bf8aece2b29b8ad406769c5f639e547
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117845629"
---
# <a name="to-configure-the-indexer"></a>Настройка индексатора

Вы можете настроить индексатор перед его использованием для индексирования файла ASF. Каждый поток в файле может быть настроен отдельно или же можно задать одинаковую конфигурацию для всех потоков.

Если вы настраиваете несколько потоков для индексирования в файле, необходимо настроить их все, а затем начать индексирование. Если вы настраиваете и индексируете поток, а затем настраиваете другой поток в том же файле, повторный запуск индексатора приведет к удалению первого индекса. Это соответствует формату ASF-файлов.

В следующем коде показано, как настроить индексатор. В коде предполагается, что индексируемый файл имеет два потока: Первый — это звуковой поток, который не нужно индексировать, а второй — видеопоток. В этом коде показано, как настроить индексатор. Чтобы индексировать файл, необходимо выполнить действия, описанные в разделе [для индексирования ASF-файла](to-index-an-asf-file.md).


```C++
IWMIndexer*  pBaseIndexer = NULL;
IWMIndexer2* pMyIndexer   = NULL;

DWORD          dwInterval;
HRESULT hr = S_OK;

// Initialize COM.
hr = CoInitialize(NULL);

// Create an indexer.
hr = WMCreateIndexer(&pBaseIndexer);

// Retrieve an IWMIndexer2 interface pointer for the indexer just created.
hr = pBaseIndexer->QueryInterface(IID_IWMIndexer2, (void**)&pMyIndexer);

// Release the base indexer.
pBaseIndexer->Release();
pBaseIndexer = NULL;

// Set the index interval to 5 frames.
dwInterval = 5;

// Configure the indexer to create a frame-based index.
hr = pMyIndexer->Configure(2,                    // Stream Number.
                           WMT_IT_FRAME_NUMBERS, // Indexer type.
                           (void *)&dwInterval,  // Index interval.
                           NULL;        // Index type, use default.

// TODO: Index the file. See To Index an ASF File.

// Release the remaining interface.
pMyIndexer->Release();
pMyIndexer = NULL;

```



> [!Note]  
> Тип индекса по умолчанию — ВМТ \_ его \_ ближайшую \_ чистую \_ точку. Хотя можно задать тип индекса другие значения, это приведет к снижению производительности.

 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[**IWMIndexer2:: Configure**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer2-configure)
</dt> <dt>

[**Индексирование файла ASF**](to-index-an-asf-file.md)
</dt> <dt>

[**вмкреатеиндексер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Работа с индексами**](working-with-indexes.md)
</dt> </dl>

 

 




