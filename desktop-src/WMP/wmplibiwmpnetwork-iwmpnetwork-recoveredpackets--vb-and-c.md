---
title: Ивмпнетворк Рековередпаккетс, свойство
description: Свойство Рековередпаккетс возвращает количество восстановленных пакетов.
ms.assetid: 90fcefcd-2bd7-4fb5-8337-36bec5d44e60
keywords:
- Проигрыватель Windows Media для свойства Рековередпаккетс
- Рековередпаккетс свойство проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство Рековередпаккетс
topic_type:
- apiref
api_name:
- IWMPNetwork.recoveredPackets
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fe9fb8b44249be30289abb2f8922343285ca074
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105652267"
---
# <a name="iwmpnetworkrecoveredpackets-property"></a><span data-ttu-id="f92ab-106">Свойство Ивмпнетворк:: Рековередпаккетс</span><span class="sxs-lookup"><span data-stu-id="f92ab-106">IWMPNetwork::recoveredPackets property</span></span>

<span data-ttu-id="f92ab-107">Свойство **рековередпаккетс** возвращает количество восстановленных пакетов.</span><span class="sxs-lookup"><span data-stu-id="f92ab-107">The **recoveredPackets** property gets the number of recovered packets.</span></span>

## <a name="syntax"></a><span data-ttu-id="f92ab-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="f92ab-108">Syntax</span></span>


```CSharp
public System.Int32 recoveredPackets {get; set;}
```


```VB

Public ReadOnly Property recoveredPackets As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="f92ab-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f92ab-109">Property value</span></span>

<span data-ttu-id="f92ab-110">Значение **System. Int32** , которое является числом восстановленных пакетов.</span><span class="sxs-lookup"><span data-stu-id="f92ab-110">A **System.Int32** that is the number of recovered packets.</span></span>

## <a name="remarks"></a><span data-ttu-id="f92ab-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f92ab-111">Remarks</span></span>

<span data-ttu-id="f92ab-112">Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство сбрасывается до нуля.</span><span class="sxs-lookup"><span data-stu-id="f92ab-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="f92ab-113">Значение не сбрасывается, если воспроизведение приостановлено.</span><span class="sxs-lookup"><span data-stu-id="f92ab-113">The value is not reset if playback is paused.</span></span>

<span data-ttu-id="f92ab-114">Это свойство получает действительные сведения только во время выполнения, когда URL-адрес для воспроизведения задается с помощью свойства **аксвиндовсмедиаплайер. URL** .</span><span class="sxs-lookup"><span data-stu-id="f92ab-114">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span> <span data-ttu-id="f92ab-115">При использовании протокола HTTP значение будет равно нулю, что не выполняется без потерь.</span><span class="sxs-lookup"><span data-stu-id="f92ab-115">The value will be zero when using the HTTP protocol, which is lossless.</span></span>

## <a name="examples"></a><span data-ttu-id="f92ab-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="f92ab-116">Examples</span></span>

<span data-ttu-id="f92ab-117">В следующем примере используется **рековередпаккетс** для вывода числа восстановленных пакетов в метке в ответ на событие **плайстатечанже** .</span><span class="sxs-lookup"><span data-stu-id="f92ab-117">The following example uses **recoveredPackets** to display the number of recovered packets in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="f92ab-118">В примере для обновления экрана используется таймер с интервалом в 1 секунду.</span><span class="sxs-lookup"><span data-stu-id="f92ab-118">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="f92ab-119">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="f92ab-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Test whether content is playing. 
    if (e.newState == 3)
    {
        // Start the timer. Update the display every 10 seconds.
        timer.Interval = 10000;
        timer.Start();
    }
    else
    {
        // Not playing; stop the timer.
        timer.Stop();
    }
}

private void UpdateRecoveredPackets(object sender, EventArgs e)
{
    recoveredPacketsLabel.Text = ("Packets recovered: " + player.network.recoveredPackets.ToString());
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

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

Public Sub UpdateRecoveredPackets(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    recoveredPacketsLabel.Text = (&quot;Packets recovered: &quot; + player.network.recoveredPackets.ToString())

End Sub
```





## <a name="requirements"></a><span data-ttu-id="f92ab-120">Требования</span><span class="sxs-lookup"><span data-stu-id="f92ab-120">Requirements</span></span>



| <span data-ttu-id="f92ab-121">Требование</span><span class="sxs-lookup"><span data-stu-id="f92ab-121">Requirement</span></span> | <span data-ttu-id="f92ab-122">Значение</span><span class="sxs-lookup"><span data-stu-id="f92ab-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f92ab-123">Версия</span><span class="sxs-lookup"><span data-stu-id="f92ab-123">Version</span></span><br/>   | <span data-ttu-id="f92ab-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="f92ab-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="f92ab-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="f92ab-125">Namespace</span></span><br/> | <span data-ttu-id="f92ab-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="f92ab-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="f92ab-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="f92ab-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="f92ab-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="f92ab-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f92ab-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f92ab-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f92ab-130">**Аксвиндовсмедиаплайер. URL (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f92ab-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="f92ab-131">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="f92ab-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





