---
title: Ивмпнетворк Рецептионкуалити, свойство
description: Свойство Рецептионкуалити Возвращает процент пакетов, которые не были потеряны за последние 30 секунд.
ms.assetid: 103e6b8f-e029-4f53-93ac-b516896a7594
keywords:
- Проигрыватель Windows Media для свойства Рецептионкуалити
- Рецептионкуалити свойство проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство Рецептионкуалити
topic_type:
- apiref
api_name:
- IWMPNetwork.receptionQuality
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a3703ffa29183937874c40053bd3c7ae3c85d75d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699192"
---
# <a name="iwmpnetworkreceptionquality-property"></a><span data-ttu-id="e9294-106">Свойство Ивмпнетворк:: Рецептионкуалити</span><span class="sxs-lookup"><span data-stu-id="e9294-106">IWMPNetwork::receptionQuality property</span></span>

<span data-ttu-id="e9294-107">Свойство **рецептионкуалити** Возвращает процент пакетов, которые не были потеряны за последние 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="e9294-107">The **receptionQuality** property gets the percentage of packets not lost in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9294-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e9294-108">Syntax</span></span>


```CSharp
public System.Int32 receptionQuality {get; set;}
```


```VB

Public ReadOnly Property receptionQuality As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="e9294-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e9294-109">Property value</span></span>

<span data-ttu-id="e9294-110">Значение **System. Int32** , которое является качеством приема.</span><span class="sxs-lookup"><span data-stu-id="e9294-110">A **System.Int32** that is the reception quality.</span></span>

## <a name="remarks"></a><span data-ttu-id="e9294-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e9294-111">Remarks</span></span>

<span data-ttu-id="e9294-112">Количество пакетов, полученных, потерянных и восстановленных во время потоковой передачи, отслеживается каждую секунду.</span><span class="sxs-lookup"><span data-stu-id="e9294-112">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="e9294-113">Свойство **рецептионкуалити** Возвращает процент пакетов, которые не были потеряны за последние 30 секунд.</span><span class="sxs-lookup"><span data-stu-id="e9294-113">The **receptionQuality** property gets the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="e9294-114">Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство сбрасывается до нуля.</span><span class="sxs-lookup"><span data-stu-id="e9294-114">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="e9294-115">Значение не сбрасывается, если воспроизведение приостановлено.</span><span class="sxs-lookup"><span data-stu-id="e9294-115">The value is not reset if playback is paused.</span></span>

<span data-ttu-id="e9294-116">Это свойство получает действительные сведения только во время выполнения, когда URL-адрес для воспроизведения задается с помощью свойства **аксвиндовсмедиаплайер. URL** .</span><span class="sxs-lookup"><span data-stu-id="e9294-116">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="e9294-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="e9294-117">Examples</span></span>

<span data-ttu-id="e9294-118">В следующем примере используется **рецептионкуалити** , чтобы отобразить процент пакетов, полученных в метке, в ответ на событие **плайстатечанже** .</span><span class="sxs-lookup"><span data-stu-id="e9294-118">The following example uses **receptionQuality** to display the percentage of packets received in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="e9294-119">В примере для обновления экрана используется таймер с интервалом в 1 секунду.</span><span class="sxs-lookup"><span data-stu-id="e9294-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="e9294-120">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="e9294-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


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

private void UpdateReceptionQuality(object sender, EventArgs e)
{
    receptionQualityLabel.Text = ("Packets recovered: " + player.network.receptionQuality.ToString() + "%");
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

Public Sub UpdateReceptionQuality(ByVal sender As Object, ByVal e As System.EventArgs) Handles timer.Tick

    receptionQualityLabel.Text = (&quot;Packets recovered: &quot; + player.network.receptionQuality.ToString() + &quot;%&quot;)

End Sub
```





## <a name="requirements"></a><span data-ttu-id="e9294-121">Требования</span><span class="sxs-lookup"><span data-stu-id="e9294-121">Requirements</span></span>



| <span data-ttu-id="e9294-122">Требование</span><span class="sxs-lookup"><span data-stu-id="e9294-122">Requirement</span></span> | <span data-ttu-id="e9294-123">Значение</span><span class="sxs-lookup"><span data-stu-id="e9294-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9294-124">Версия</span><span class="sxs-lookup"><span data-stu-id="e9294-124">Version</span></span><br/>   | <span data-ttu-id="e9294-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="e9294-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="e9294-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e9294-126">Namespace</span></span><br/> | <span data-ttu-id="e9294-127">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="e9294-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="e9294-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="e9294-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e9294-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e9294-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9294-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e9294-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9294-131">**Аксвиндовсмедиаплайер. URL (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e9294-131">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e9294-132">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e9294-132">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





