---
title: Получение примеров мультимедиа с помощью синхронного модуля чтения
description: Получение примеров мультимедиа с помощью синхронного модуля чтения
ms.assetid: 7e228a0b-e29d-485e-b2ef-81c0311ca828
keywords:
- Расширенный формат систем (ASF), получение примеров мультимедиа
- ASF (Расширенный системный формат), получение примеров мультимедиа
- Расширенный формат систем (ASF), синхронные средства чтения
- ASF (Расширенный системный формат), синхронные средства чтения
- синхронные читатели, получение примеров мультимедиа
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1fd341ea9616b18a5e65cfa8c1134e0f1be44b5
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/19/2020
ms.locfileid: "104412516"
---
# <a name="to-retrieve-media-samples-with-the-synchronous-reader"></a><span data-ttu-id="b5ea3-108">Получение примеров мультимедиа с помощью синхронного модуля чтения</span><span class="sxs-lookup"><span data-stu-id="b5ea3-108">To Retrieve Media Samples with the Synchronous Reader</span></span>

<span data-ttu-id="b5ea3-109">Необходимо запросить каждый из примеров по одному за раз из синхронного модуля чтения.</span><span class="sxs-lookup"><span data-stu-id="b5ea3-109">You must request each sample one at a time from the synchronous reader.</span></span> <span data-ttu-id="b5ea3-110">Это обеспечивает более полный контроль над полученными примерами и их получением.</span><span class="sxs-lookup"><span data-stu-id="b5ea3-110">This gives you more control over the samples you receive and when you receive them.</span></span>

<span data-ttu-id="b5ea3-111">Чтобы получить пример, используйте метод [**ивмсинкреадер:: жетнекстсампле**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) .</span><span class="sxs-lookup"><span data-stu-id="b5ea3-111">Use the [**IWMSyncReader::GetNextSample**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-getnextsample) method to retrieve a sample.</span></span> <span data-ttu-id="b5ea3-112">Необходимо передавать в основном указатели на переменные, которые будут заполнены сведениями о примере, извлеченном в качестве параметров.</span><span class="sxs-lookup"><span data-stu-id="b5ea3-112">You need to pass mostly pointers to variables that will be filled with information about the sample retrieved as parameters.</span></span> <span data-ttu-id="b5ea3-113">Единственным входным параметром является *встреамнум*.</span><span class="sxs-lookup"><span data-stu-id="b5ea3-113">The only input parameter is *wStreamNum*.</span></span> <span data-ttu-id="b5ea3-114">Если передать номер потока, **жетнекстсампле** получит следующую выборку с указанным номером потока.</span><span class="sxs-lookup"><span data-stu-id="b5ea3-114">If you pass a stream number, **GetNextSample** will retrieve the next sample with the specified stream number.</span></span> <span data-ttu-id="b5ea3-115">При передаче нулевого значения для *встреамнум* в файл извлекается следующий пример, который выполняется в хронологическом порядке в файле.</span><span class="sxs-lookup"><span data-stu-id="b5ea3-115">If you pass zero for *wStreamNum*, the next sample that occurs chronologically in the file is retrieved.</span></span>

<span data-ttu-id="b5ea3-116">По умолчанию синхронный читатель получает все образцы из выходных данных в файле в хронологическом порядке.</span><span class="sxs-lookup"><span data-stu-id="b5ea3-116">By default, the synchronous reader retrieves all of the samples from the outputs in a file in chronological order.</span></span> <span data-ttu-id="b5ea3-117">Если вы вызовите **жетнекстсампле** и больше нет примеров для получения, он вернет NS \_ E \_ без \_ дополнительных \_ примеров, что является неудачным кодом ошибки.</span><span class="sxs-lookup"><span data-stu-id="b5ea3-117">If you call **GetNextSample** and there are no more samples to get, it will return NS\_E\_NO\_MORE\_SAMPLES, which is a failed error code.</span></span> <span data-ttu-id="b5ea3-118">Поэтому при программировании можно просто прокручивать выборку, пока не завершится выполнение метода.</span><span class="sxs-lookup"><span data-stu-id="b5ea3-118">When coding therefore, you can simply loop through samples until the method fails.</span></span>

> [!Note]  
> <span data-ttu-id="b5ea3-119">Чтобы гарантировать, что синхронный читатель доставляет правильную длительность выборки для видеопотоков, необходимо сначала настроить выходные данные потока.</span><span class="sxs-lookup"><span data-stu-id="b5ea3-119">To ensure that the synchronous reader delivers correct sample durations for video streams, you must first configure the stream output.</span></span> <span data-ttu-id="b5ea3-120">Вызовите метод [**ивмсинкреадер:: сетаутпутсеттинг**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) , чтобы установить \_ для параметра g всзвидеосампледуратионс значение **true**.</span><span class="sxs-lookup"><span data-stu-id="b5ea3-120">Call the [**IWMSyncReader::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmsyncreader-setoutputsetting) method to set the g\_wszVideoSampleDurations setting to **TRUE**.</span></span>

 

<span data-ttu-id="b5ea3-121">Пример кода</span><span class="sxs-lookup"><span data-stu-id="b5ea3-121">Example Code</span></span>

<span data-ttu-id="b5ea3-122">В следующем примере кода показано, как использовать **жетнекстсампле** для получения всех примеров в файле.</span><span class="sxs-lookup"><span data-stu-id="b5ea3-122">The following example code shows how to use **GetNextSample** to retrieve all samples in a file.</span></span>


```C++
// Loop through all the samples in the file.
do
{
   // Get the next sample.
   hr = pSyncReader->GetNextSample(0,
                                   &pMyBuffer,
                                   &cnsSampleTime,
                                   &cnsSampleDuration,
                                   &dwFlags,
                                   &dwOutputNumber,
                                   NULL);

   if(SUCCEEDED(hr))
   {
      // TODO: Process the sample in whatever way is appropriate 
      // to your application. When finished, clean up.
      pMyBuffer->Release();
      pMyBuffer = NULL;
      cnsSampleTime     = 0;
      cnsSampleDuration = 0;
      dwFlags           = 0;
      dwOutputNumber    = 0;
   }
} 
while (SUCCEEDED(hr));

```



## <a name="related-topics"></a><span data-ttu-id="b5ea3-123">См. также</span><span class="sxs-lookup"><span data-stu-id="b5ea3-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b5ea3-124">**Интерфейс Ивмсинкреадер**</span><span class="sxs-lookup"><span data-stu-id="b5ea3-124">**IWMSyncReader Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmsyncreader)
</dt> <dt>

[<span data-ttu-id="b5ea3-125">**Чтение файлов с помощью синхронного модуля чтения**</span><span class="sxs-lookup"><span data-stu-id="b5ea3-125">**Reading Files with the Synchronous Reader**</span></span>](reading-files-with-the-synchronous-reader.md)
</dt> </dl>

 

 




