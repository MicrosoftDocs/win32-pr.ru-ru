---
description: В этом разделе описывается воспроизведение последовательности аудио-и видеофайлов с помощью Мфплай.
ms.assetid: ee16eaa3-0506-4444-b139-f8a8498d6597
title: Как воспроизвести последовательность файлов
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58dc4d1523be4cc6cc09416096af260c9eae736c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105650688"
---
# <a name="how-to-play-a-sequence-of-files"></a><span data-ttu-id="ed017-103">Как воспроизвести последовательность файлов</span><span class="sxs-lookup"><span data-stu-id="ed017-103">How to Play a Sequence of Files</span></span>

<span data-ttu-id="ed017-104">\[Мфплай доступен для использования в операционных системах, указанных в разделе требования.</span><span class="sxs-lookup"><span data-stu-id="ed017-104">\[MFPlay is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="ed017-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="ed017-105">It may be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="ed017-106">\]</span><span class="sxs-lookup"><span data-stu-id="ed017-106">\]</span></span>

<span data-ttu-id="ed017-107">В этом разделе описывается воспроизведение последовательности аудио-и видеофайлов с помощью Мфплай.</span><span class="sxs-lookup"><span data-stu-id="ed017-107">This topic describes how to play a sequence of audio/video files using MFPlay.</span></span>


<span data-ttu-id="ed017-108">В разделе [Начало работы with мфплай](getting-started-with-mfplay.md) показано, как воспроизвести один файл мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ed017-108">The topic [Getting Started with MFPlay](getting-started-with-mfplay.md) shows how to play a single media file.</span></span> <span data-ttu-id="ed017-109">Можно также использовать Мфплай для воспроизведения последовательности файлов.</span><span class="sxs-lookup"><span data-stu-id="ed017-109">You can also use MFPlay to play a sequence of files.</span></span>

### <a name="synchronous-blocking-method"></a><span data-ttu-id="ed017-110">Синхронный (блокирующий) метод</span><span class="sxs-lookup"><span data-stu-id="ed017-110">Synchronous (Blocking) Method</span></span>

1.  <span data-ttu-id="ed017-111">Вызовите метод [**имфпмедиаплайер:: креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) .</span><span class="sxs-lookup"><span data-stu-id="ed017-111">Call the [**IMFPMediaPlayer::CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method.</span></span> <span data-ttu-id="ed017-112">Метод создает элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ed017-112">The method creates a media item.</span></span>
2.  <span data-ttu-id="ed017-113">Вызовите [**имфпмедиаплайер:: сетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) , чтобы поставить в очередь элемент мультимедиа для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ed017-113">Call [**IMFPMediaPlayer::SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) to queue the media item for playback.</span></span>
3.  <span data-ttu-id="ed017-114">Вызовите [**имфпмедиаплайер::P**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) , чтобы начать воспроизведение.</span><span class="sxs-lookup"><span data-stu-id="ed017-114">Call [**IMFPMediaPlayer::Play**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play) to start playback.</span></span>

<span data-ttu-id="ed017-115">Эти действия показаны в следующем коде.</span><span class="sxs-lookup"><span data-stu-id="ed017-115">These steps are shown in the following code.</span></span>


```C++
HRESULT OpenMediaFile(IMFPMediaPlayer *pPlayer, PCWSTR pwszURL)
{
    HRESULT hr = S_OK;
    
    IMFPMediaItem *pItem = NULL;

    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        TRUE,  // Blocking call
        0,     // User data.
        &pItem
        );

    if (SUCCEEDED(hr))
    {
        hr = pPlayer->SetMediaItem(pItem);
    }

    if (SUCCEEDED(hr))
    {
       hr = pPlayer->Play();
    }

    if (pItem)
    {
        pItem->Release();
    }
    return hr;
}
```



<span data-ttu-id="ed017-116">Метод [**креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) принимает следующие параметры:</span><span class="sxs-lookup"><span data-stu-id="ed017-116">The [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) method takes the following parameters:</span></span>

-   <span data-ttu-id="ed017-117">Первый параметр — это URL-адрес файла.</span><span class="sxs-lookup"><span data-stu-id="ed017-117">The first parameter is the URL of the file.</span></span>
-   <span data-ttu-id="ed017-118">Второй параметр указывает, блокируется ли метод.</span><span class="sxs-lookup"><span data-stu-id="ed017-118">The second parameter specifies whether the method blocks.</span></span> <span data-ttu-id="ed017-119">Указание значения **true**, как показано здесь, приводит к тому, что метод блокируется до создания элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ed017-119">Specifying the value **TRUE**, as shown here, causes the method to block until the media item is created.</span></span>
-   <span data-ttu-id="ed017-120">Третий параметр связывает произвольное значение **типа \_ DWORD** с элементом мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ed017-120">The third parameter associates an arbitrary **DWORD\_PTR** value with the media item.</span></span> <span data-ttu-id="ed017-121">Это значение можно получить позже, вызвав [**имфпмедиаитем:: UserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).</span><span class="sxs-lookup"><span data-stu-id="ed017-121">You can get this value later by calling [**IMFPMediaItem::GetUserData**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata).</span></span>
-   <span data-ttu-id="ed017-122">Четвертый параметр получает указатель на интерфейс [**имфпмедиаитем**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ed017-122">The fourth parameter receives a pointer to the [**IMFPMediaItem**](/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem) interface of the media item.</span></span>

### <a name="asynchronous-non-blocking-method"></a><span data-ttu-id="ed017-123">Асинхронный (не блокирующий) метод</span><span class="sxs-lookup"><span data-stu-id="ed017-123">Asynchronous (Non-Blocking) Method</span></span>

<span data-ttu-id="ed017-124">Избегайте параметра блокировки при вызове [**креатемедиаитемфромурл**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) из потока пользовательского интерфейса, так как для выполнения может потребоваться значительное время.</span><span class="sxs-lookup"><span data-stu-id="ed017-124">Avoid the blocking option if you call [**CreateMediaItemFromURL**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl) from your UI thread, because it can take a noticeable amount of time to complete.</span></span> <span data-ttu-id="ed017-125">Метод обычно открывает файл или сетевое подключение и считывает достаточно данных для анализа заголовков файлов, все из которых может занять некоторое время.</span><span class="sxs-lookup"><span data-stu-id="ed017-125">The method typically opens a file or network connection and reads enough data to parse the file headers, all of which can take time.</span></span> <span data-ttu-id="ed017-126">Поэтому, как правило, лучше установить для второго параметра значение **false**.</span><span class="sxs-lookup"><span data-stu-id="ed017-126">Therefore, it is generally better to set the second parameter to **FALSE**.</span></span> <span data-ttu-id="ed017-127">Этот параметр приводит к асинхронному выполнению метода.</span><span class="sxs-lookup"><span data-stu-id="ed017-127">This option causes the method to perform asynchronously.</span></span> <span data-ttu-id="ed017-128">При использовании асинхронного параметра последний параметр должен иметь **значение NULL**:</span><span class="sxs-lookup"><span data-stu-id="ed017-128">When the asynchronous option is used, the last parameter must be **NULL**:</span></span>


```C++
    hr = pPlayer->CreateMediaItemFromURL(
        sURL, 
        FALSE,  // Non-blocking call.
        0,      // User data.
        NULL    // Must be NULL for the non-blocking call.
        );
```



<span data-ttu-id="ed017-129">При создании элемента мультимедиа приложение получает событие **МФП \_ event \_ Type \_ MEDIAITEM \_ Created** .</span><span class="sxs-lookup"><span data-stu-id="ed017-129">When the media item is created, your application receives an **MFP\_EVENT\_TYPE\_MEDIAITEM\_CREATED** event.</span></span> <span data-ttu-id="ed017-130">Структура данных для этого события содержит указатель на элемент мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ed017-130">The data structure for this event contains a pointer to the media item.</span></span> <span data-ttu-id="ed017-131">Передайте этот указатель методу [**сетмедиаитем**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) , чтобы поставить в очередь элемент для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="ed017-131">Pass this pointer to the [**SetMediaItem**](/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem) method to queue the item for playback.</span></span>


```C++
void OnMediaItemCreated(MFP_MEDIAITEM_CREATED_EVENT *pEvent)
{
    HRESULT hr = S_OK;
    if (FAILED(pEvent->header.hrEvent))
    {
        // Handle error. (Not shown.)
    }
    else
    {
        hr = g_pPlayer->SetMediaItem(pEvent->pMediaItem);
    }
}
```



## <a name="requirements"></a><span data-ttu-id="ed017-132">Требования</span><span class="sxs-lookup"><span data-stu-id="ed017-132">Requirements</span></span>

<span data-ttu-id="ed017-133">Для Мфплай требуется Windows 7.</span><span class="sxs-lookup"><span data-stu-id="ed017-133">MFPlay requires Windows 7.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ed017-134">См. также</span><span class="sxs-lookup"><span data-stu-id="ed017-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ed017-135">Использование Мфплай для воспроизведения звука и видео</span><span class="sxs-lookup"><span data-stu-id="ed017-135">Using MFPlay for Audio/Video Playback</span></span>](using-mfplay-for-audio-video-playback.md)
</dt> </dl>

 

 



