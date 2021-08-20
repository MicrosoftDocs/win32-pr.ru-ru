---
title: чтение файлов ASF в DirectShow (пакет SDK для Windows Media Format 11)
description: Воспроизведение файлов ASF обрабатывается фильтром чтения WM ASF. сведения о чтении файлов ASF в DirectShow в пакете SDK для Windows Media Format 11.
ms.assetid: eec2c91f-1762-4798-91d0-d68ec2160d6a
keywords:
- Windows Пакет SDK для формата мультимедиа, DirectShow
- Windows Пакет SDK для формата мультимедиа, чтение файлов ASF
- Windows Пакет SDK для формата мультимедиа, фильтр чтения WM ASF
- Windows Пакет SDK для формата мультимедиа, интерфейс Имедиасикинг
- Расширенный формат систем (ASF), DirectShow
- ASF (Расширенный системный формат), DirectShow
- Расширенный формат систем (ASF), чтение файлов
- ASF (Расширенный системный формат), чтение файлов
- Расширенный формат систем (ASF), фильтр чтения WM ASF
- ASF (Расширенный системный формат), фильтр чтения WM ASF
- Расширенный системный формат (ASF), интерфейс Имедиасикинг
- ASF (Расширенный системный формат), интерфейс Имедиасикинг
- DirectShow чтение файлов ASF
- DirectShow, фильтр чтения WM ASF
- DirectShow, интерфейс имедиасикинг
- Фильтр чтения WM ASF
- имедиасикинг
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eef3c492be93d4197609689165785f7483d926f092e25ddbe579caf2bd84031f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117654365"
---
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a>чтение файлов ASF в DirectShow (пакет SDK для Windows Media Format 11)

Воспроизведение файлов ASF обрабатывается фильтром [чтения WM ASF](wm-asf-reader-filter.md) . Когда средство чтения WM ASF считывает файл, он автоматически создает выходной ПИН-код для каждого потока, включая веб-потоки, потоки команд скрипта и любой другой тип произвольного потока. В случае нескольких файлов скорости передачи ПИН-коды создаются только для выбранных в данный момент потоков.

модуль чтения WM ASF поддерживает интерфейс DirectShow **имедиасикинг** , позволяющий приложениям выполнять временное поиск в файле. Однако воспроизведение с тактовой частотой, отличной от 1,0 (как указано в **имедиасикинг:: сетрате**), не поддерживается.

фильтр также предоставляет несколько Windows интерфейсов пакета SDK для формата мультимедиа, как описано в следующей таблице.



| Интерфейс                                        | Как предоставлено                            | Примечания                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ивмдрмреадер**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | Через **IServiceProvider** по фильтру | Предоставляется для приложений, которым требуется воспроизведение содержимого, защищенного цифровыми Rights Management (DRM). Этот интерфейс также можно использовать для непосредственного получения других интерфейсов в объекте Reader. |
| [**ивмхеадеринфо**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | **QueryInterface** в фильтре           | Предоставляется, чтобы приложения могли считывать атрибуты файлов и содержимого, а также сведения о маркерах и скриптах и метаданные.                                                                  |
| [**ивмреадерадванцед**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | **QueryInterface** в фильтре           | Частично Реализовано на фильтре, чтобы приложения могли обращаться к информационным методам объекта WM Reader.                                                                      |
| [**IWMReaderAdvanced2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | **QueryInterface** в фильтре           | Частично Реализовано на фильтре, чтобы приложения могли обращаться к информационным методам объекта Reader.                                                                         |



 

фильтр [чтения WM ASF](wm-asf-reader-filter.md) был впервые сделан доступным в DirectShow 8,0. версия фильтра, поставляемого с DirectShow 8,1 и 9,0, поддерживает версию 7. *x* пакета SDK для Windows Media Format. последняя версия фильтра, вместе с другими компонентами касф, поставляется с и поддерживает пакет SDK для Windows Media Format 9 серии и более поздних версий, а также заменяет фильтр в DirectX 9,0. если вы устанавливаете пакет SDK Windows Media Format после установки DirectX 8. *x* или 9. *пакет SDK* для версии DirectX, вы перезапишете версию для qasf.dll с версией 9 Series. это не должно представлять проблемы, за исключением случаев, когда в одном сценарии это приведет к различным результатам в методе DirectShow **играфбуилдер:: RenderFile** . версия пакета SDK для модуля чтения WM asf в формате Windows Media 9 является фильтром источников по умолчанию для расширений файлов ASF, wmv и wma. это означает, что модуль чтения WM ASF автоматически создается и добавляется в граф фильтра с помощью фильтра Graph Manager в таких методах, как **играфбуилдер:: RenderFile** или **играфбуилдер:: аддсаурцефилтер** , если указан файл этого типа. в DirectX 9,0 и более ранних версиях и Windows XP с пакетом обновления 1 (sp1) и более ранних версиях метод **RenderFile** использует старый фильтр источника носителей Windows. это поведение поддерживалось для обеспечения обратной совместимости с приложениями, которые использовали проигрыватель Windows Media 6,4. дополнительные сведения об устаревшем Windows фильтре источников мультимедиа см. в документации по пакету SDK для DirectShow.

чтобы воспроизвести ASF-файл с Windows содержимым на основе носителя с помощью средства чтения WM ASF, необходимо создать экземпляр фильтра Graph Manager, вызвать **играфбуилдер:: RenderFile** для создания графа, а затем вызвать **имедиаконтрол:: Run** для воспроизведения файла. Следующий пример кода представляет собой полную программу, которая воспроизводит файл ASF с помощью DirectShow. для выполнения этого примера необходимо, чтобы пакет SDK для DirectX был установлен, а среда сборки должна быть настроена в соответствии с инструкциями в разделе документации по DirectShow SDK "настройка среды сборки". Кроме того, необходимо указать файл на компьютере при вызове функции **RenderFile**.


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



Обратите внимание, что код приложения для этого простого примера никогда не ссылается на модуль чтения WM ASF специально. этот фильтр создается, подключается, выполняется и в конечном итоге освобождается диспетчером Graph Manager. Однако во многих случаях может потребоваться настроить средство чтения WM ASF перед началом воспроизведения.

 

 




