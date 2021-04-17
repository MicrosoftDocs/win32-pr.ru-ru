---
title: Индексирование файла ASF
description: Индексирование файла ASF
ms.assetid: 33175444-365c-4b94-8b91-07198431062f
keywords:
- Windows Media Format SDK, индексирование файлов ASF
- Расширенный системный формат (ASF), индексирование файлов
- ASF (Расширенный системный формат), индексирование файлов
- индексы, индексирование файлов ASF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7206e1856abb9705e18e885ba06cb8253a93c84b
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "105681583"
---
# <a name="to-index-an-asf-file"></a>Индексирование файла ASF

Процесс индексирования ASF-файла очень прост. Выполните вызов [**ивминдексер:: startIndex**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmindexer-startindexing) и передайте имя файла. Индексатор выполняет остальные. Вызов **startIndex** является асинхронным, поэтому состояние должно отслеживаться с помощью обратного вызова **OnStatus** .

В следующем коде показано, как индексировать ASF файл. Если необходимо настроить индексатор перед индексацией файла, необходимо включить код из примера, включенного в, [для настройки индексатора](to-configure-the-indexer.md).

В этом примере маркер, указывающий на событие, должен быть создан как глобальная переменная, поэтому он будет доступен для обратного вызова. Следующее объявление должно отображаться в глобальной области видимости.


```C++
HANDLE g_hEvent = NULL;

```



В более реалистичном сценарии обработчик событий должен быть элементом данных класса, который содержит как обратный вызов, так и логику для запуска индексатора.

Индексатор отправляет несколько событий обратному вызову **OnStatus** после вызова **Ивминдексер:: startIndex**. При необходимости их можно перехватить для приложения. Как минимум необходимо выполнить треппинг ВМТ \_ Closed, который отправляется после завершения индексирования. Используйте следующую логику в параметре message в реализации обратного вызова **OnStatus** .


```C++
// Inside the status switch statement.
case WMT_CLOSED:
   // You may want to deal with the HRESULT value passed with the status.
   // If you do, you should do it here.

   // Signal the event.
   SetEvent(g_hEvent);
   break;

```



В этом примере предполагается, что реализация обратного вызова **OnStatus** осуществляется через объект с именем микаллбакк. Дополнительные сведения об использовании событий и обратных вызовов с помощью этого пакета SDK см. [в разделе Использование методов обратного вызова](using-the-callback-methods.md).


```C++
IWMIndexer* pMyIndexer     = NULL;
HRESULT     hr             = S_OK;
WCHAR       pwszFileName[] = L"C:\SomeFile.wmv";

// Initialize COM.
hr = CoInitialize(NULL);

// Create an event for asynchronous calls.
g_hEvent = CreateEvent(NULL, TRUE, FALSE, NULL);

// Create an indexer.
hr = WMCreateIndexer(&pMyIndexer);

// TODO: Configure the indexer if needed. See To Configure the Indexer.

// Start the indexer.
hr = pMyIndexer->StartIndexing(pwszFileName, &MyCallback, NULL);

// Wait for the indexer to finish.
WaitForSingleObject(g_hEvent, INFINITE);

// Clean up.
pMyIndexer->Release();
pMyIndexer = NULL

CloseHandle(g_hEvent);
g_hEvent = NULL;

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**Интерфейс Ивминдексер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmindexer)
</dt> <dt>

[**Настройка индексатора**](to-configure-the-indexer.md)
</dt> <dt>

[**вмкреатеиндексер**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-wmcreateindexer)
</dt> <dt>

[**Работа с индексами**](working-with-indexes.md)
</dt> </dl>

 

 




