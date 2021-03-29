---
description: Воспроизведение файла
ms.assetid: 3d8c5d06-8690-4298-a1d1-f21af35bcfd4
title: Воспроизведение файла
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc84ef751db318354da36454e6a30fd2ce4bd8e7
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423085"
---
# <a name="how-to-play-a-file"></a>Воспроизведение файла

Эта статья призвана предоставить вам версию программирования DirectShow. Он представляет простое консольное приложение, которое воспроизводит аудио-или видеофайл. Программа состоит всего из нескольких строк, но она демонстрирует некоторые возможности программирования DirectShow.

Как описано в статье [Введение в программирование приложений DirectShow](introduction-to-directshow-application-programming.md) , приложение DirectShow всегда выполняет те же основные действия:

1.  Создайте экземпляр [диспетчера графа фильтров](filter-graph-manager.md).
2.  Используйте диспетчер графа фильтров для создания графа фильтра.
3.  Запустите граф, что приведет к перемещению данных по фильтрам.

Чтобы скомпилировать и связать код в этом разделе, включите заголовочный файл DShow. h и укажите ссылку на файл статической библиотеки стрмиидс. lib. Дополнительные сведения см. в разделе [Создание приложений DirectShow](setting-up-the-build-environment.md).

Начните [**с вызова CoInitialize**](/windows/desktop/api/objbase/nf-objbase-coinitialize) или [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) для инициализации библиотеки COM:


```C++
HRESULT hr = CoInitialize(NULL);
if (FAILED(hr))
{
    // Add error-handling code here. (Omitted for clarity.)
}
```



Для простоты в этом примере игнорируется возвращаемое значение, но всегда следует проверять значение **HRESULT** из любого вызова метода.

Затем вызовите [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) для создания диспетчера графа фильтров:


```C++
IGraphBuilder *pGraph;
HRESULT hr = CoCreateInstance(CLSID_FilterGraph, NULL, 
    CLSCTX_INPROC_SERVER, IID_IGraphBuilder, (void **)&pGraph);
```



Как показано, идентификатором класса является CLSID \_ филтерграф. Диспетчер графов фильтров предоставляется внутри внутрипроцессного DLL, поэтому контекст выполнения — **КЛСКТКС \_ INPROC \_ Server**. DirectShow поддерживает модель свободной потоковой модели, поэтому можно также вызвать [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) с флагом **\_ многопотоковой инициализации** .

Вызов [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) возвращает интерфейс [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) , который в основном содержит методы для построения графа фильтра. Для этого примера необходимы два других интерфейса:

-   [**Имедиаконтрол**](/windows/desktop/api/Control/nn-control-imediacontrol) управляет потоковой передачей. Он содержит методы для остановки и запуска графа.
-   [**Имедиаевент**](/windows/desktop/api/Control/nn-control-imediaevent) имеет методы для получения событий из диспетчера графа фильтров. В этом примере интерфейс используется для ожидания завершения воспроизведения.

Оба этих интерфейса предоставляются диспетчером графа фильтров. Используйте возвращенный указатель [**играфбуилдер**](/windows/desktop/api/Strmif/nn-strmif-igraphbuilder) для запроса этих запросов:


```C++
IMediaControl *pControl;
IMediaEvent   *pEvent;
hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);
```



Теперь можно построить граф фильтра. Для воспроизведения файла это делается одним вызовом метода:


```C++
hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
```



Метод [**играфбуилдер:: renderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) создает граф фильтра, который может воспроизвести указанный файл. Первый параметр — это имя файла, представленное в виде строки расширенных символов (2 байта). Второй параметр зарезервирован и должен равняться **null**.

Этот метод может завершиться ошибкой, если указанный файл не существует или формат файла не распознан. При условии, что метод выполнен правильно, граф фильтра теперь готов к воспроизведению. Чтобы запустить граф, вызовите метод [**имедиаконтрол:: Run**](/windows/desktop/api/Control/nf-control-imediacontrol-run) :


```C++
hr = pControl->Run();
```



При выполнении графа фильтра данные перемещаются по фильтрам и подготавливаются к просмотру как видео и аудио. Воспроизведение выполняется в отдельном потоке. Можно подождать завершения воспроизведения, вызвав метод [**имедиаевент:: ваитфоркомплетион**](/windows/desktop/api/Control/nf-control-imediaevent-waitforcompletion) :


```C++
long evCode = 0;
pEvent->WaitForCompletion(INFINITE, &evCode);
```



Этот метод блокируется до окончания воспроизведения файла или до истечения заданного интервала времени ожидания. Значение INFINITE означает, что приложение блокируется на неограниченное время до завершения воспроизведения файла. Более реалистичный пример обработки событий см. в разделе [реагирование на события](responding-to-events.md).

После завершения работы приложения Освободите указатели интерфейса и закройте библиотеку COM:


```C++
pControl->Release();
pEvent->Release();
pGraph->Release();
CoUninitialize();
```



## <a name="example-code"></a>Пример кода

Ниже приведен полный код для примера, описанного в этой статье:


```C++
#include <dshow.h>
void main(void)
{
    IGraphBuilder *pGraph = NULL;
    IMediaControl *pControl = NULL;
    IMediaEvent   *pEvent = NULL;

    // Initialize the COM library.
    HRESULT hr = CoInitialize(NULL);
    if (FAILED(hr))
    {
        printf("ERROR - Could not initialize COM library");
        return;
    }

    // Create the filter graph manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file on your system.
    hr = pGraph->RenderFile(L"C:\\Example.avi", NULL);
    if (SUCCEEDED(hr))
    {
        // Run the graph.
        hr = pControl->Run();
        if (SUCCEEDED(hr))
        {
            // Wait for completion.
            long evCode;
            pEvent->WaitForCompletion(INFINITE, &evCode);

            // Note: Do not use INFINITE in a real application, because it
            // can block indefinitely.
        }
    }
    pControl->Release();
    pEvent->Release();
    pGraph->Release();
    CoUninitialize();
}
```



## <a name="related-topics"></a>См. также

<dl> <dt>

[Основные задачи DirectShow](basic-directshow-tasks.md)
</dt> </dl>

 

 
