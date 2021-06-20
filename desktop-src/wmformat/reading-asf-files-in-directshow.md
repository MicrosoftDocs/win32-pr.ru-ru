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
# <a name="reading-asf-files-in-directshow-windows-media-format-11-sdk"></a><span data-ttu-id="34902-121">Чтение файлов ASF в DirectShow (пакет SDK для Windows Media Format 11)</span><span class="sxs-lookup"><span data-stu-id="34902-121">Reading ASF Files in DirectShow (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="34902-122">Воспроизведение файлов ASF обрабатывается фильтром [чтения WM ASF](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="34902-122">Playback of ASF files is handled by the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="34902-123">Когда средство чтения WM ASF считывает файл, он автоматически создает выходной ПИН-код для каждого потока, включая веб-потоки, потоки команд скрипта и любой другой тип произвольного потока.</span><span class="sxs-lookup"><span data-stu-id="34902-123">When the WM ASF Reader reads a file, it automatically creates an output pin for each stream, including Web streams, script command streams, and any other type of arbitrary stream.</span></span> <span data-ttu-id="34902-124">В случае нескольких файлов скорости передачи ПИН-коды создаются только для выбранных в данный момент потоков.</span><span class="sxs-lookup"><span data-stu-id="34902-124">In the case of multiple bit rate files, pins are created only for the currently selected streams.</span></span>

<span data-ttu-id="34902-125">Модуль чтения WM ASF поддерживает интерфейс DirectShow **имедиасикинг** , позволяющий приложениям выполнять временное Поиск в файле.</span><span class="sxs-lookup"><span data-stu-id="34902-125">The WM ASF Reader supports the DirectShow **IMediaSeeking** interface, which enables applications to perform temporal seeking within the file.</span></span> <span data-ttu-id="34902-126">Однако воспроизведение с тактовой частотой, отличной от 1,0 (как указано в **имедиасикинг:: сетрате**), не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="34902-126">However, playback at speeds other than 1.0 (as specified in **IMediaSeeking::SetRate**) is not supported.</span></span>

<span data-ttu-id="34902-127">Фильтр также предоставляет несколько интерфейсов пакета SDK Windows Media Format, как описано в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="34902-127">The filter also exposes several Windows Media Format SDK interfaces as described in the following table.</span></span>



| <span data-ttu-id="34902-128">Интерфейс</span><span class="sxs-lookup"><span data-stu-id="34902-128">Interface</span></span>                                        | <span data-ttu-id="34902-129">Как предоставлено</span><span class="sxs-lookup"><span data-stu-id="34902-129">How exposed</span></span>                            | <span data-ttu-id="34902-130">Комментарии</span><span class="sxs-lookup"><span data-stu-id="34902-130">Comments</span></span>                                                                                                                                                                                    |
|--------------------------------------------------|----------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="34902-131">**ивмдрмреадер**</span><span class="sxs-lookup"><span data-stu-id="34902-131">**IWMDRMReader**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmdrmreader)             | <span data-ttu-id="34902-132">Через **IServiceProvider** по фильтру</span><span class="sxs-lookup"><span data-stu-id="34902-132">Through **IServiceProvider** on filter</span></span> | <span data-ttu-id="34902-133">Предоставляется для приложений, которым требуется воспроизведение содержимого, защищенного цифровыми Rights Management (DRM).</span><span class="sxs-lookup"><span data-stu-id="34902-133">Provided for applications that need to play content protected by Digital Rights Management (DRM).</span></span> <span data-ttu-id="34902-134">Этот интерфейс также можно использовать для непосредственного получения других интерфейсов в объекте Reader.</span><span class="sxs-lookup"><span data-stu-id="34902-134">This interface can also be used to obtain other interfaces on the Reader Object directly.</span></span> |
| [<span data-ttu-id="34902-135">**ивмхеадеринфо**</span><span class="sxs-lookup"><span data-stu-id="34902-135">**IWMHeaderInfo**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo)           | <span data-ttu-id="34902-136">**QueryInterface** в фильтре</span><span class="sxs-lookup"><span data-stu-id="34902-136">**QueryInterface** on filter</span></span>           | <span data-ttu-id="34902-137">Предоставляется, чтобы приложения могли считывать атрибуты файлов и содержимого, а также сведения о маркерах и скриптах и метаданные.</span><span class="sxs-lookup"><span data-stu-id="34902-137">Provided so that applications can read file and content attributes, as well as marker and script information and metadata.</span></span>                                                                  |
| [<span data-ttu-id="34902-138">**ивмреадерадванцед**</span><span class="sxs-lookup"><span data-stu-id="34902-138">**IWMReaderAdvanced**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced)   | <span data-ttu-id="34902-139">**QueryInterface** в фильтре</span><span class="sxs-lookup"><span data-stu-id="34902-139">**QueryInterface** on filter</span></span>           | <span data-ttu-id="34902-140">Частично Реализовано на фильтре, чтобы приложения могли обращаться к информационным методам объекта WM Reader.</span><span class="sxs-lookup"><span data-stu-id="34902-140">Partially implemented on the filter so that applications can access the informational methods on the WM Reader object.</span></span>                                                                      |
| [<span data-ttu-id="34902-141">**IWMReaderAdvanced2**</span><span class="sxs-lookup"><span data-stu-id="34902-141">**IWMReaderAdvanced2**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2) | <span data-ttu-id="34902-142">**QueryInterface** в фильтре</span><span class="sxs-lookup"><span data-stu-id="34902-142">**QueryInterface** on filter</span></span>           | <span data-ttu-id="34902-143">Частично Реализовано на фильтре, чтобы приложения могли обращаться к информационным методам объекта Reader.</span><span class="sxs-lookup"><span data-stu-id="34902-143">Partially implemented on the filter so that applications can access the informational methods on the Reader Object.</span></span>                                                                         |



 

<span data-ttu-id="34902-144">Фильтр [чтения WM ASF](wm-asf-reader-filter.md) был впервые сделан доступным в DirectShow 8,0.</span><span class="sxs-lookup"><span data-stu-id="34902-144">The [WM ASF Reader](wm-asf-reader-filter.md) filter was first made available in DirectShow 8.0.</span></span> <span data-ttu-id="34902-145">Версия фильтра, поставляемого с DirectShow 8,1 и 9,0, поддерживает версию 7. *x* пакета SDK Windows Media Format.</span><span class="sxs-lookup"><span data-stu-id="34902-145">The version of the filter that ships with DirectShow 8.1 and 9.0 supports version 7.*x* of the Windows Media Format SDK.</span></span> <span data-ttu-id="34902-146">Последняя версия фильтра, вместе с другими компонентами КАСФ, поставляется с и поддерживает пакет SDK для Windows Media Format 9 Series и более поздних версий, а также заменяет фильтр в DirectX 9,0.</span><span class="sxs-lookup"><span data-stu-id="34902-146">The most recent version of the filter, along with the other QASF components, ships with and supports the Windows Media Format 9 Series SDK, and later versions, and it supersedes the filter in DirectX 9.0.</span></span> <span data-ttu-id="34902-147">При установке пакета SDK для формата Windows Media после установки DirectX 8. *x* или 9. *пакет SDK* для версии DirectX, вы перезапишете версию для qasf.dll с версией 9 Series.</span><span class="sxs-lookup"><span data-stu-id="34902-147">If you install the Windows Media Format SDK after installing the DirectX 8.*x* or 9.*x* SDK, you will overwrite the DirectX version of qasf.dll with the 9 Series version.</span></span> <span data-ttu-id="34902-148">Это не должно представлять проблемы, за исключением случаев, когда в одном сценарии это приведет к различным поведению в методе DirectShow **играфбуилдер:: renderFile** .</span><span class="sxs-lookup"><span data-stu-id="34902-148">This should not present any problems except possibly in one scenario where it will result in different behavior in the DirectShow **IGraphBuilder::RenderFile** method.</span></span> <span data-ttu-id="34902-149">Версия пакета SDK для Windows Media 9 Series для модуля чтения WM ASF является фильтром источников по умолчанию для расширений файлов ASF, WMV и WMA.</span><span class="sxs-lookup"><span data-stu-id="34902-149">The Windows Media Format 9 Series SDK version of the WM ASF Reader is the default source filter for the .asf, .wmv, and .wma file name extensions.</span></span> <span data-ttu-id="34902-150">Это означает, что модуль чтения WM ASF автоматически создается и добавляется в граф фильтра диспетчером графа фильтров в таких методах, как **играфбуилдер:: renderFile** или **Играфбуилдер:: аддсаурцефилтер** , если указан файл этого типа.</span><span class="sxs-lookup"><span data-stu-id="34902-150">This means that the WM ASF Reader is automatically created and added to the filter graph by the Filter Graph Manager in methods such as **IGraphBuilder::RenderFile** or **IGraphBuilder::AddSourceFilter** when a file of this type is specified.</span></span> <span data-ttu-id="34902-151">В DirectX 9,0 и более ранних версиях и Windows XP с пакетом обновления 1 (SP1) и более ранних версиях метод **RenderFile** использует старый фильтр источника Windows Media.</span><span class="sxs-lookup"><span data-stu-id="34902-151">In DirectX 9.0 and earlier, and Windows XP Service Pack 1 and earlier, the **RenderFile** method uses the older Windows Media Source Filter.</span></span> <span data-ttu-id="34902-152">Это поведение поддерживалось для обеспечения обратной совместимости с приложениями, использующими проигрыватель Windows Media 6,4.</span><span class="sxs-lookup"><span data-stu-id="34902-152">This behavior was maintained to ensure backward compatibility with applications that used the Windows Media Player 6.4.</span></span> <span data-ttu-id="34902-153">Дополнительные сведения о устаревшем фильтре исходного кода Windows Media см. в документации по пакету SDK для DirectShow.</span><span class="sxs-lookup"><span data-stu-id="34902-153">For more information about the legacy Windows Media Source Filter, see the DirectShow SDK Documentation.</span></span>

<span data-ttu-id="34902-154">Чтобы воспроизвести ASF-файл с содержимым на основе Windows Media с помощью средства чтения WM ASF, необходимо создать экземпляр диспетчера графа фильтров, вызвать **играфбуилдер:: renderFile** для создания графа, а затем вызвать **Имедиаконтрол:: Run** для воспроизведения файла.</span><span class="sxs-lookup"><span data-stu-id="34902-154">To play an ASF file with Windows Media–based content using the WM ASF Reader, the three primary steps are to create an instance of the Filter Graph Manager, call **IGraphBuilder::RenderFile** to create the graph, and then call **IMediaControl::Run** to play the file.</span></span> <span data-ttu-id="34902-155">Следующий пример кода представляет собой полную программу, которая воспроизводит файл ASF с помощью DirectShow.</span><span class="sxs-lookup"><span data-stu-id="34902-155">The following code example is a complete program that plays an ASF file using DirectShow.</span></span> <span data-ttu-id="34902-156">Для выполнения этого примера необходимо, чтобы пакет SDK для DirectX был установлен, а среда сборки должна быть настроена в соответствии с инструкциями в документации по пакету SDK для DirectShow "Настройка среды сборки".</span><span class="sxs-lookup"><span data-stu-id="34902-156">To run this example, you must have the DirectX SDK installed and your build environment must be configured according to the instructions in the DirectShow SDK documentation topic "Setting Up the Build Environment."</span></span> <span data-ttu-id="34902-157">Кроме того, необходимо указать файл на компьютере при вызове функции **RenderFile**.</span><span class="sxs-lookup"><span data-stu-id="34902-157">Also, you must specify a file on your computer in the call to **RenderFile**.</span></span>


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



<span data-ttu-id="34902-158">Обратите внимание, что код приложения для этого простого примера никогда не ссылается на модуль чтения WM ASF специально.</span><span class="sxs-lookup"><span data-stu-id="34902-158">Note that the application code for this simple example never references the WM ASF Reader specifically.</span></span> <span data-ttu-id="34902-159">Этот фильтр создается, подключается, запускается и в конечном итоге освобождается диспетчером графа фильтров.</span><span class="sxs-lookup"><span data-stu-id="34902-159">That filter is created, connected, run, and eventually released by the Filter Graph Manager.</span></span> <span data-ttu-id="34902-160">Однако во многих случаях может потребоваться настроить средство чтения WM ASF перед началом воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="34902-160">In many scenarios, however, you may want to configure the WM ASF Reader before beginning playback.</span></span>

 

 




