---
title: Ивмпнетворк Енкодедфрамерате, свойство
description: Свойство Енкодедфрамерате возвращает частоту кадров видео, указанную автором содержимого.
ms.assetid: 4faf5675-5bf3-485d-802f-a1f900ddae63
keywords:
- Проигрыватель Windows Media для свойства Енкодедфрамерате
- Енкодедфрамерате свойство проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство Енкодедфрамерате
topic_type:
- apiref
api_name:
- IWMPNetwork.encodedFrameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b4176a9c2492d0ce34ffd0936c48dbdef065d1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665131"
---
# <a name="iwmpnetworkencodedframerate-property"></a><span data-ttu-id="36e15-106">Свойство Ивмпнетворк:: Енкодедфрамерате</span><span class="sxs-lookup"><span data-stu-id="36e15-106">IWMPNetwork::encodedFrameRate property</span></span>

<span data-ttu-id="36e15-107">Свойство **енкодедфрамерате** возвращает частоту кадров видео, указанную автором содержимого.</span><span class="sxs-lookup"><span data-stu-id="36e15-107">The **encodedFrameRate** property gets the video frame rate specified by the content author.</span></span>

## <a name="syntax"></a><span data-ttu-id="36e15-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="36e15-108">Syntax</span></span>


```CSharp
public System.Int32 encodedFrameRate {get; set;}
```


```VB

Public ReadOnly Property encodedFrameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="36e15-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="36e15-109">Property value</span></span>

<span data-ttu-id="36e15-110">Значение **System. Int32** , которое является закодированной частотой кадров в кадрах в секунду (кадров/с).</span><span class="sxs-lookup"><span data-stu-id="36e15-110">A **System.Int32** that is the encoded frame rate in frames per second (fps).</span></span>

> [!Note]  
> <span data-ttu-id="36e15-111">Несмотря на то, что свойство **енкодедфрамерате** измеряет частоту закодированных кадров в кадрах в секунду, свойство **Частота** кадров измеряет текущую частоту кадров в кадрах за сотни секунд.</span><span class="sxs-lookup"><span data-stu-id="36e15-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span>

 

## <a name="examples"></a><span data-ttu-id="36e15-112">Примеры</span><span class="sxs-lookup"><span data-stu-id="36e15-112">Examples</span></span>

<span data-ttu-id="36e15-113">В следующем примере кода используется **енкодедфрамерате** для вывода частоты кадров, указанной при кодировании файла.</span><span class="sxs-lookup"><span data-stu-id="36e15-113">The following code example uses **encodedFrameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="36e15-114">Сведения отображаются в метке в ответ на событие **плайстатечанже** .</span><span class="sxs-lookup"><span data-stu-id="36e15-114">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="36e15-115">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="36e15-115">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the encodedFrameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.encodedFrameRate != 0)
            {
                encodedFrameRateLabel.Text = "Current Encoded Frame Rate: " + player.network.encodedFrameRate + " K bits/second";
            }
            break;

        default:
            break;
    }
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the encodedFrameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.encodedFrameRate <> 0) Then

                encodedFrameRateLabel.Text = &quot;Current Encoded Frame Rate: &quot; + player.network.encodedFrameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="36e15-116">Требования</span><span class="sxs-lookup"><span data-stu-id="36e15-116">Requirements</span></span>



| <span data-ttu-id="36e15-117">Требование</span><span class="sxs-lookup"><span data-stu-id="36e15-117">Requirement</span></span> | <span data-ttu-id="36e15-118">Значение</span><span class="sxs-lookup"><span data-stu-id="36e15-118">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36e15-119">Версия</span><span class="sxs-lookup"><span data-stu-id="36e15-119">Version</span></span><br/>   | <span data-ttu-id="36e15-120">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="36e15-120">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="36e15-121">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="36e15-121">Namespace</span></span><br/> | <span data-ttu-id="36e15-122">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="36e15-122">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="36e15-123">Сборка</span><span class="sxs-lookup"><span data-stu-id="36e15-123">Assembly</span></span><br/>  | <dl> <span data-ttu-id="36e15-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="36e15-124"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36e15-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="36e15-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36e15-126">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="36e15-126">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="36e15-127">**Ивмпнетворк. частота (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="36e15-127">**IWMPNetwork.frameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-framerate--vb-and-c.md)
</dt> </dl>

 

 





