---
title: Ивмпнетворк Довнлоадпрогресс, свойство
description: Свойство Довнлоадпрогресс Возвращает процент завершенной загрузки.
ms.assetid: 40568c81-5bb5-45d9-b654-31072608663d
keywords:
- Проигрыватель Windows Media для свойства Довнлоадпрогресс
- Довнлоадпрогресс свойство проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство Довнлоадпрогресс
topic_type:
- apiref
api_name:
- IWMPNetwork.downloadProgress
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b10b767845ac951e1364e15c7f6f1d729882e0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694478"
---
# <a name="iwmpnetworkdownloadprogress-property"></a><span data-ttu-id="2b13f-106">Ивмпнетворк: свойство Овнлоадпрогресс:d</span><span class="sxs-lookup"><span data-stu-id="2b13f-106">IWMPNetwork::downloadProgress property</span></span>

<span data-ttu-id="2b13f-107">Свойство **довнлоадпрогресс** Возвращает процент завершенной загрузки.</span><span class="sxs-lookup"><span data-stu-id="2b13f-107">The **downloadProgress** property gets the percentage of downloading completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b13f-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2b13f-108">Syntax</span></span>


```CSharp
public System.Int32 downloadProgress {get; set;}
```


```VB

Public ReadOnly Property downloadProgress As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="2b13f-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2b13f-109">Property value</span></span>

<span data-ttu-id="2b13f-110">Объект **System. Int32** , который является процессом загрузки, выраженный в процентах.</span><span class="sxs-lookup"><span data-stu-id="2b13f-110">A **System.Int32** that is the download progress expressed as a percentage.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b13f-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2b13f-111">Remarks</span></span>

<span data-ttu-id="2b13f-112">Если элемент управления проигрывателя Windows Media подключен к цифровому файлу мультимедиа, который можно воспроизвести и скачать одновременно, свойство **довнлоадпрогресс** Возвращает процент общего файла, который был скачан.</span><span class="sxs-lookup"><span data-stu-id="2b13f-112">When the Windows Media Player control is connected to a digital media file that can be played and downloaded at the same time, the **downloadProgress** property gets the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="2b13f-113">В настоящее время эта функция поддерживается только для цифровых файлов мультимедиа, скачанных с веб-серверов.</span><span class="sxs-lookup"><span data-stu-id="2b13f-113">This feature is currently supported only for digital media files downloaded from web servers.</span></span> <span data-ttu-id="2b13f-114">Файл любого из следующих форматов можно скачать и воспроизвести одновременно:</span><span class="sxs-lookup"><span data-stu-id="2b13f-114">A file of any of the following formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="2b13f-115">Advanced Systems Format (ASF)</span><span class="sxs-lookup"><span data-stu-id="2b13f-115">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="2b13f-116">Звуковые файлы в формате WMA</span><span class="sxs-lookup"><span data-stu-id="2b13f-116">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="2b13f-117">Видеофайлы в формате WMV</span><span class="sxs-lookup"><span data-stu-id="2b13f-117">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="2b13f-118">MP3</span><span class="sxs-lookup"><span data-stu-id="2b13f-118">MP3</span></span>
-   <span data-ttu-id="2b13f-119">КОДИРОВЩИК</span><span class="sxs-lookup"><span data-stu-id="2b13f-119">MPEG</span></span>
-   <span data-ttu-id="2b13f-120">WAV</span><span class="sxs-lookup"><span data-stu-id="2b13f-120">WAV</span></span>

<span data-ttu-id="2b13f-121">Кроме того, некоторые файлы AVI можно загружать и воспроизводить одновременно.</span><span class="sxs-lookup"><span data-stu-id="2b13f-121">In addition, some AVI files can be downloaded and played simultaneously.</span></span>

<span data-ttu-id="2b13f-122">Используйте **аксвиндовсмедиаплайер. \_ Вмпокксевентс \_ буфферинжевент** , чтобы определить, когда буферизация начинается или останавливается.</span><span class="sxs-lookup"><span data-stu-id="2b13f-122">Use the **AxWindowsMediaPlayer.\_WMPOCXEvents\_BufferingEvent** to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="2b13f-123">Примеры</span><span class="sxs-lookup"><span data-stu-id="2b13f-123">Examples</span></span>

<span data-ttu-id="2b13f-124">В следующем примере кода используется **довнлоадпрогресс** для показа процента завершенной загрузки.</span><span class="sxs-lookup"><span data-stu-id="2b13f-124">The following code example uses **downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="2b13f-125">Сведения отображаются в метке в ответ на событие **буферизации** .</span><span class="sxs-lookup"><span data-stu-id="2b13f-125">The information is displayed in a label, in response to the **Buffering** Event.</span></span> <span data-ttu-id="2b13f-126">В примере для обновления экрана используется таймер с интервалом в 1 секунду.</span><span class="sxs-lookup"><span data-stu-id="2b13f-126">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="2b13f-127">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="2b13f-127">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Determine whether buffering has started or stopped.
    if (e.start == true)
    {
        // Set the timer interval at one second (1000 miliseconds).
        timer.Interval = 1000;
        
        // Start the timer.
        timer.Start();
    }
    else
    {
        // Buffering is complete. Stop the timer.
        timer.Stop();
    }
}

// Update the download progress in a timer event handler.
private void UpdateDownloadProgress(object sender, EventArgs e)
{
    downloadProgressLabel.Text = ("Download progress: " + player.network.downloadProgress + " percent complete");
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Test whether packets may be arriving.
    Select Case e.newState

    &#39; If WMPPlayState is Stopped, Paused, ScanForward, ScanReverse, Waiting, MediaEnded
    &#39; or Transitioning then stop the timer. 
        Case 1
        Case 2
        Case 4
        Case 5
        Case 7
        Case 8
        Case 9
            timer.Stop()

        &#39; If WMPPlayState is Playing or Buffering then set the timer interval and start the timer.
        Case Else
            timer.Interval = 1000
            timer.Start()

    End Select

End Sub

&#39; Update the download progress in a timer event handler.
Public Sub UpdateDownloadProgress(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    downloadProgressLabel.Text = (&quot;Download progress: &quot; + player.network.downloadProgress + &quot; percent complete&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2b13f-128">Требования</span><span class="sxs-lookup"><span data-stu-id="2b13f-128">Requirements</span></span>



| <span data-ttu-id="2b13f-129">Требование</span><span class="sxs-lookup"><span data-stu-id="2b13f-129">Requirement</span></span> | <span data-ttu-id="2b13f-130">Значение</span><span class="sxs-lookup"><span data-stu-id="2b13f-130">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b13f-131">Версия</span><span class="sxs-lookup"><span data-stu-id="2b13f-131">Version</span></span><br/>   | <span data-ttu-id="2b13f-132">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2b13f-132">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2b13f-133">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2b13f-133">Namespace</span></span><br/> | <span data-ttu-id="2b13f-134">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="2b13f-134">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2b13f-135">Сборка</span><span class="sxs-lookup"><span data-stu-id="2b13f-135">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2b13f-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2b13f-136"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b13f-137">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2b13f-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b13f-138">**Событие Аксвиндовсмедиаплайер. Buffering (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2b13f-138">**AxWindowsMediaPlayer.Buffering Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-buffering.md)
</dt> <dt>

[<span data-ttu-id="2b13f-139">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2b13f-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





