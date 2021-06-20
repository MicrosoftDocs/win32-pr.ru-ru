---
title: Чтение файлов ASF в DirectShow (пакет SDK для Windows Media Format 11)
description: Воспроизведение файлов ASF обрабатывается фильтром чтения WM ASF. Узнайте о чтении файлов ASF в DirectShow в пакете SDK для Windows Media Format 11.
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Пакет SDK для Windows Media Format, DirectShow
- Windows Media Format SDK, чтение файлов ASF
- Windows Media Format SDK, фильтр чтения WM ASF
- Windows Media Format SDK, интерфейс Имедиасикинг
- Расширенный системный формат (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный формат систем (ASF), чтение файлов
- ASF (Расширенный системный формат), чтение файлов
- Расширенный формат систем (ASF), фильтр чтения WM ASF
- ASF (Расширенный системный формат), фильтр чтения WM ASF
- Расширенный системный формат (ASF), интерфейс Имедиасикинг
- ASF (Расширенный системный формат), интерфейс Имедиасикинг
- DirectShow, чтение файлов ASF
- DirectShow, фильтр чтения WM ASF
- DirectShow, интерфейс Имедиасикинг
- Фильтр чтения WM ASF
- имедиасикинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4aaab64798011eb21edbe43f49438db99d0bae6b
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/19/2021
ms.locfileid: "112404327"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a>Чтение файлов ASF в DirectShow (пакет SDK для Windows Media Format 11)

Воспроизведение файлов ASF обрабатывается фильтром [чтения WM ASF](wm-asf-reader-filter.md) . Когда средство чтения WM ASF считывает файл, он автоматически создает выходной ПИН-код для каждого потока, включая веб-потоки, потоки команд скрипта и любой другой тип произвольного потока. В случае нескольких файлов скорости передачи ПИН-коды создаются только для выбранных в данный момент потоков.

Модуль чтения WM ASF поддерживает интерфейс DirectShow **имедиасикинг** , позволяющий приложениям выполнять временное Поиск в файле. Однако воспроизведение с тактовой частотой, отличной от 1,0 (как указано в **имедиасикинг:: сетрате**), не поддерживается.

Фильтр также предоставляет несколько интерфейсов пакета SDK Windows Media Format, как описано в следующей таблице.



| Интерфейс                                        | Как предоставлено                            | Комментарии                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Через **IServiceProvider** по фильтру | Предоставляется для приложений, которым требуется воспроизведение содержимого, защищенного цифровыми Rights Management (DRM). Этот интерфейс также можно использовать для непосредственного получения других интерфейсов в объекте Reader. |
| [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** в фильтре           | Предоставляется, чтобы приложения могли считывать атрибуты файлов и содержимого, а также сведения о маркерах и скриптах и метаданные.                                                                  |
| [**ивмреадерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** в фильтре           | Частично Реализовано на фильтре, чтобы приложения могли обращаться к информационным методам объекта WM Reader.                                                                      |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** в фильтре           | Частично Реализовано на фильтре, чтобы приложения могли обращаться к информационным методам объекта Reader.                                                                         |



 

Фильтр [чтения WM ASF](wm-asf-reader-filter.md) был впервые сделан доступным в DirectShow 8,0. Версия фильтра, поставляемого с DirectShow 8,1 и 9,0, поддерживает версию 7. *x* пакета SDK Windows Media Format. Последняя версия фильтра, вместе с другими компонентами КАСФ, поставляется с и поддерживает пакет SDK для Windows Media Format 9 Series и более поздних версий, а также заменяет фильтр в DirectX 9,0. При установке пакета SDK для формата Windows Media после установки DirectX 8. *x* или 9. *пакет SDK* для версии DirectX, вы перезапишете версию для qasf.dll с версией 9 Series. Это не должно представлять проблемы, за исключением случаев, когда в одном сценарии это приведет к различным поведению в методе DirectShow **играфбуилдер:: renderFile** . Версия пакета SDK для Windows Media 9 Series для модуля чтения WM ASF является фильтром источников по умолчанию для расширений файлов ASF, WMV и WMA. Это означает, что модуль чтения WM ASF автоматически создается и добавляется в граф фильтра диспетчером графа фильтров в таких методах, как **играфбуилдер:: renderFile** или **Играфбуилдер:: аддсаурцефилтер** , если указан файл этого типа. В DirectX 9,0 и более ранних версиях и Windows XP с пакетом обновления 1 (SP1) и более ранних версиях метод **RenderFile** использует старый фильтр источника Windows Media. Это поведение поддерживалось для обеспечения обратной совместимости с приложениями, использующими проигрыватель Windows Media 6,4. Дополнительные сведения о устаревшем фильтре исходного кода Windows Media см. в документации по пакету SDK для DirectShow.

Чтобы воспроизвести ASF-файл с содержимым на основе Windows Media с помощью средства чтения WM ASF, необходимо создать экземпляр диспетчера графа фильтров, вызвать **играфбуилдер:: renderFile** для создания графа, а затем вызвать **Имедиаконтрол:: Run** для воспроизведения файла. Следующий пример кода представляет собой полную программу, которая воспроизводит файл ASF с помощью DirectShow. Для выполнения этого примера необходимо, чтобы пакет SDK для DirectX был установлен, а среда сборки должна быть настроена в соответствии с инструкциями в документации по пакету SDK для DirectShow "Настройка среды сборки". Кроме того, необходимо указать файл на компьютере при вызове функции **RenderFile**.


```C++
#include <dshow.h>
#include <stdio.h>

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

    // Create the Filter Graph Manager and query for interfaces.
    hr = CoCreateInstance(CLSID_FilterGraph, NULL, CLSCTX_INPROC_SERVER, 
                        IID_IGraphBuilder, (void **)&pGraph);
    if (FAILED(hr))
    {
        printf("ERROR - Could not create the Filter Graph Manager.");
        return;
    }

    hr = pGraph->QueryInterface(IID_IMediaControl, (void **)&pControl);
    hr = pGraph->QueryInterface(IID_IMediaEvent, (void **)&pEvent);

    // Build the graph. IMPORTANT: Change this string to a file
    // on your system.
    hr = pGraph->RenderFile(L"test.wmv", NULL);
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



Обратите внимание, что код приложения для этого простого примера никогда не ссылается на модуль чтения WM ASF специально. Этот фильтр создается, подключается, запускается и в конечном итоге освобождается диспетчером графа фильтров. Однако во многих случаях может потребоваться настроить средство чтения WM ASF перед началом воспроизведения.

 

 




