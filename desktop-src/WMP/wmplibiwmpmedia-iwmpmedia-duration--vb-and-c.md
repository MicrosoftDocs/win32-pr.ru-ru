---
title: Ивмпмедиа, свойство длительности
description: Свойство Duration возвращает продолжительность текущего элемента мультимедиа в секундах.
ms.assetid: f8a0bf3e-eeaf-46f5-90c8-d3b11ce4eb39
keywords:
- Проигрыватель Windows Media, свойство Duration
- свойство Duration проигрыватель Windows Media Player, интерфейс Ивмпмедиа
- Интерфейс Ивмпмедиа Windows Media Player, свойство Duration
topic_type:
- apiref
api_name:
- IWMPMedia.duration
- IWMPMedia.get_duration
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f796cab042713082ce2066659f62736855e62787
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105669261"
---
# <a name="iwmpmediaduration-property"></a><span data-ttu-id="3b51c-106">Ивмпмедиа: свойство фигурации:d</span><span class="sxs-lookup"><span data-stu-id="3b51c-106">IWMPMedia::duration property</span></span>

<span data-ttu-id="3b51c-107">Свойство **Duration** Возвращает продолжительность текущего элемента мультимедиа в секундах.</span><span class="sxs-lookup"><span data-stu-id="3b51c-107">The **duration** property gets the duration in seconds of the current media item.</span></span>

<span data-ttu-id="3b51c-108">Это свойство доступно только для чтения.</span><span class="sxs-lookup"><span data-stu-id="3b51c-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b51c-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3b51c-109">Syntax</span></span>


```CSharp
public System.Double duration {get;}
```


```VB

Public ReadOnly Property duration As System.Double
```





## <a name="property-value"></a><span data-ttu-id="3b51c-110">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="3b51c-110">Property value</span></span>

<span data-ttu-id="3b51c-111">Значение **System. Double** , которое является длительностью в секундах.</span><span class="sxs-lookup"><span data-stu-id="3b51c-111">A **System.Double** that is the duration in seconds.</span></span>

## <a name="remarks"></a><span data-ttu-id="3b51c-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3b51c-112">Remarks</span></span>

<span data-ttu-id="3b51c-113">Если это свойство используется с элементом мультимедиа, отличным от указанного в Аксвиндовсмедиаплайер. Куррентмедиа, он может не содержать допустимого значения.</span><span class="sxs-lookup"><span data-stu-id="3b51c-113">If this property is used with a media item other than the one specified in AxWindowsMediaPlayer.currentMedia, it may not contain a valid value.</span></span>

<span data-ttu-id="3b51c-114">Чтобы получить длительность для файлов, которые не находятся в библиотеке пользователя, необходимо подождать, пока проигрыватель Windows Media откроет этот файл. то есть текущий **опенстате** должен равняться **медиаопен**.</span><span class="sxs-lookup"><span data-stu-id="3b51c-114">To retrieve the duration for files that are not in the user's library, you must wait for Windows Media Player to open the file; that is, the current **OpenState** must equal **MediaOpen**.</span></span> <span data-ttu-id="3b51c-115">Это можно проверить, обрабатывая **аксвиндовсмедиаплайер. \_ Вмпокксевентс \_ опенстатечанже** или путем периодической проверки значения **аксвиндовсмедиаплайер. опенстате**.</span><span class="sxs-lookup"><span data-stu-id="3b51c-115">You can verify this by handling the **AxWindowsMediaPlayer.\_WMPOCXEvents\_OpenStateChange** event or by periodically checking the value of **AxWindowsMediaPlayer.openState**.</span></span>

<span data-ttu-id="3b51c-116">Для списков воспроизведения продолжительность каждого элемента мультимедиа может быть получена при открытии отдельного элемента мультимедиа, а не при открытии списка воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="3b51c-116">For playlists, the duration of each media item can be retrieved when the individual media item is opened, rather than the when the playlist is opened.</span></span>

<span data-ttu-id="3b51c-117">Перед использованием этого свойства необходимо иметь доступ на чтение к библиотеке.</span><span class="sxs-lookup"><span data-stu-id="3b51c-117">Before using this property, you must have read access to the library.</span></span> <span data-ttu-id="3b51c-118">Дополнительные сведения см. в разделе [доступ к библиотеке](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="3b51c-118">For more information, see [Library Access](library-access.md).</span></span>

## <a name="examples"></a><span data-ttu-id="3b51c-119">Примеры</span><span class="sxs-lookup"><span data-stu-id="3b51c-119">Examples</span></span>

<span data-ttu-id="3b51c-120">В следующем примере используется **Длительность** для вывода времени, оставшегося в текущем элементе мультимедиа в метке.</span><span class="sxs-lookup"><span data-stu-id="3b51c-120">The following example uses **duration** to display the time remaining in the current media item in a label.</span></span> <span data-ttu-id="3b51c-121">Таймер обновляет текст метки каждую секунду.</span><span class="sxs-lookup"><span data-stu-id="3b51c-121">A timer updates the text in the label every second.</span></span>


```CSharp
// Set the timer to fire an event every second and start the timer.
timer.Interval = 1000;
timer.Start();

// Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a switch statement to
// determine when to start and stop the timer. 

private void TimerEventProcessor(object sender, System.EventArgs e)
{
    // Subtract the current position from the duration of the current media to get
    // the time remaining. Use the Math.floor method to round the result down to the
    // nearest whole number.
    double t = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition);

    // Display the time remaining in the current media.
    timeRemaining.Text = ("Seconds remaining: " + t.ToString());        
}
```


```VB

' Set the timer to fire an event every second and start the timer.
Timer.Interval = 1000
Timer.Start()

&#39; Note:  Use the AxWindowsMediaPlayer.PlayStateChange event with a Select Case statement to
&#39; determine when to start and stop the timer. 

Public Sub TimerEventProcessor(ByVal sender As Object, ByVal e As System.EventArgs) Handles Timer.Tick

    &#39; Subtract the current position from the duration of the current media to get
    &#39; the time remaining. Use the Math.Floor method to round the result down to the
    &#39; nearest whole number.
    Dim t As Double = Math.Floor(player.currentMedia.duration - player.Ctlcontrols.currentPosition)

    &#39; Display the time remaining in the current media.
    timeRemaining.Text = (&quot;Seconds remaining: &quot; + t.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3b51c-122">Требования</span><span class="sxs-lookup"><span data-stu-id="3b51c-122">Requirements</span></span>



| <span data-ttu-id="3b51c-123">Требование</span><span class="sxs-lookup"><span data-stu-id="3b51c-123">Requirement</span></span> | <span data-ttu-id="3b51c-124">Значение</span><span class="sxs-lookup"><span data-stu-id="3b51c-124">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b51c-125">Версия</span><span class="sxs-lookup"><span data-stu-id="3b51c-125">Version</span></span><br/>   | <span data-ttu-id="3b51c-126">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3b51c-126">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3b51c-127">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3b51c-127">Namespace</span></span><br/> | <span data-ttu-id="3b51c-128">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="3b51c-128">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3b51c-129">Сборка</span><span class="sxs-lookup"><span data-stu-id="3b51c-129">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3b51c-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3b51c-130"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3b51c-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3b51c-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b51c-132">**Аксвиндовсмедиаплайер. Куррентмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3b51c-132">**AxWindowsMediaPlayer.currentMedia (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b51c-133">**Аксвиндовсмедиаплайер. Опенстате (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3b51c-133">**AxWindowsMediaPlayer.openState (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstate--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b51c-134">**Событие Аксвиндовсмедиаплайер. Опенстатечанже (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3b51c-134">**AxWindowsMediaPlayer.OpenStateChange Event (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[<span data-ttu-id="3b51c-135">**Интерфейс Ивмпмедиа (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3b51c-135">**IWMPMedia Interface (VB and C#)**</span></span>](iwmpmedia--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3b51c-136">**Ивмпмедиа. Дуратионстринг (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3b51c-136">**IWMPMedia.durationString (VB and C#)**</span></span>](wmplibiwmpmedia-iwmpmedia-durationstring--vb-and-c.md)
</dt> </dl>

 

 





