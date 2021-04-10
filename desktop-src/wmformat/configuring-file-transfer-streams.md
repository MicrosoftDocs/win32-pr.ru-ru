---
title: Настройка потоков обмена файлами
description: Настройка потоков обмена файлами
ms.assetid: faed54ae-9e80-492a-9602-e726bdb3b54a
keywords:
- потоки, Настройка потоков для обмена файлами
- кодеки, Настройка потоков для обмена файлами
- потоки для перемещения файлов
- потоки, расширения модулей данных
- кодеки, расширения модулей данных
- расширения модулей данных, потоки обмена файлами
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75fac7d2270da82f1f9e82ed9123611ae608dd3c
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104069605"
---
# <a name="configuring-file-transfer-streams"></a><span data-ttu-id="b88bf-109">Настройка потоков обмена файлами</span><span class="sxs-lookup"><span data-stu-id="b88bf-109">Configuring File Transfer Streams</span></span>

<span data-ttu-id="b88bf-110">Для потоков передачи файлов не требуются специальные параметры в структуре [**\_ \_ типа мультимедиа WM**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) .</span><span class="sxs-lookup"><span data-stu-id="b88bf-110">File transfer streams do not require any special settings in the [**WM\_MEDIA\_TYPE**](/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type) structure.</span></span> <span data-ttu-id="b88bf-111">Им требуется расширение единицы данных, чтобы связать имя файла с каждым образцом.</span><span class="sxs-lookup"><span data-stu-id="b88bf-111">They do require a data unit extension to associate a file name with each sample.</span></span> <span data-ttu-id="b88bf-112">Чтобы отправить имя с примерами передачи файлов, необходимо реализовать систему расширения единиц обработки данных для потока.</span><span class="sxs-lookup"><span data-stu-id="b88bf-112">To send a name with file transfer samples, you must implement a data unit extension system for the stream.</span></span>

<span data-ttu-id="b88bf-113">Чтобы задать расширение единицы данных для потока, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="b88bf-113">To set a data unit extension for the stream, perform the following steps:</span></span>

1.  <span data-ttu-id="b88bf-114">Получите указатель на интерфейс [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) объекта конфигурации потока, вызвав **Ивмстреамконфиг:: QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="b88bf-114">Obtain a pointer to the [**IWMStreamConfig2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig2) interface of the stream configuration object by calling **IWMStreamConfig::QueryInterface**.</span></span>
2.  <span data-ttu-id="b88bf-115">Добавьте расширение единицы данных для потока, вызвав [**IWMStreamConfig2:: адддатаунитекстенсион**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) следующим образом:</span><span class="sxs-lookup"><span data-stu-id="b88bf-115">Add a data unit extension for the stream by calling [**IWMStreamConfig2::AddDataUnitExtension**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig2-adddataunitextension) as follows:</span></span>
    ```C++
    hr = pStreamConfig2->AddDataUnitExtension(CLSID_WMTPropertyFileName,
                                              -1, NULL, 0);
    ```

    

## <a name="related-topics"></a><span data-ttu-id="b88bf-116">См. также</span><span class="sxs-lookup"><span data-stu-id="b88bf-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b88bf-117">**Общая конфигурация для всех потоков**</span><span class="sxs-lookup"><span data-stu-id="b88bf-117">**Configuration Common to All Streams**</span></span>](configuration-common-to-all-streams.md)
</dt> <dt>

[<span data-ttu-id="b88bf-118">**Настройка произвольных типов потоков**</span><span class="sxs-lookup"><span data-stu-id="b88bf-118">**Configuring Arbitrary Stream Types**</span></span>](configuring-arbitrary-stream-types.md)
</dt> <dt>

[<span data-ttu-id="b88bf-119">**Файловые потоки**</span><span class="sxs-lookup"><span data-stu-id="b88bf-119">**File Streams**</span></span>](file-streams.md)
</dt> </dl>

 

 




