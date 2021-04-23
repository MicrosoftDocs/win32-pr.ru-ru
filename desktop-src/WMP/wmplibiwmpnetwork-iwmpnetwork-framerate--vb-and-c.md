---
title: Свойство частоты кадров Ивмпнетворк
description: Свойство частота кадров возвращает текущую частоту кадров видео.
ms.assetid: 800ecf3d-3b2c-48f9-8fc4-c7c32757749a
keywords:
- Свойство частоты кадров Windows Media Player
- Свойство частоты кадров Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство частоты кадров
topic_type:
- apiref
api_name:
- IWMPNetwork.frameRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c338a116588fa9f1c552feff15f220e08b0f66e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105665241"
---
# <a name="iwmpnetworkframerate-property"></a><span data-ttu-id="44c9e-106">Свойство Ивмпнетворк:: частота кадров</span><span class="sxs-lookup"><span data-stu-id="44c9e-106">IWMPNetwork::frameRate property</span></span>

<span data-ttu-id="44c9e-107">Свойство **Частота** кадров возвращает текущую частоту кадров видео.</span><span class="sxs-lookup"><span data-stu-id="44c9e-107">The **frameRate** property gets the current video frame rate.</span></span>

## <a name="syntax"></a><span data-ttu-id="44c9e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="44c9e-108">Syntax</span></span>


```CSharp
public System.Int32 frameRate {get; set;}
```


```VB

Public ReadOnly Property frameRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="44c9e-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="44c9e-109">Property value</span></span>

<span data-ttu-id="44c9e-110">Объект **System. Int32** , который является текущей частотой кадров в кадрах за сотни секунд.</span><span class="sxs-lookup"><span data-stu-id="44c9e-110">A **System.Int32** that is the current frame rate in frames per hundred seconds.</span></span>

> [!Note]  
> <span data-ttu-id="44c9e-111">Несмотря на то, что свойство **енкодедфрамерате** измеряет частоту закодированных кадров в кадрах в секунду, свойство **Частота** кадров измеряет текущую частоту кадров в кадрах за сотни секунд.</span><span class="sxs-lookup"><span data-stu-id="44c9e-111">Although the **encodedFrameRate** property measures the encoded frame rate in frames per second, the **frameRate** property measures the current frame rate in frames per hundred seconds.</span></span> <span data-ttu-id="44c9e-112">См. заметки.</span><span class="sxs-lookup"><span data-stu-id="44c9e-112">See Remarks.</span></span>

 

## <a name="remarks"></a><span data-ttu-id="44c9e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44c9e-113">Remarks</span></span>

<span data-ttu-id="44c9e-114">Текущее значение частоты кадров возвращается в кадрах за сотни секунд.</span><span class="sxs-lookup"><span data-stu-id="44c9e-114">The current frame rate value is returned in frames per hundred seconds.</span></span> <span data-ttu-id="44c9e-115">Например, значение 2998 означает 29,98 кадров в секунду (кадров/с).</span><span class="sxs-lookup"><span data-stu-id="44c9e-115">For example, a value of 2998 indicates 29.98 frames per second (fps).</span></span>

## <a name="examples"></a><span data-ttu-id="44c9e-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="44c9e-116">Examples</span></span>

<span data-ttu-id="44c9e-117">В приведенном ниже примере кода **используется частота кадров для вывода** частотного кадра, указанного при кодировании файла.</span><span class="sxs-lookup"><span data-stu-id="44c9e-117">The following code example uses **frameRate** to display the frame rate specified when the file was encoded.</span></span> <span data-ttu-id="44c9e-118">Сведения отображаются в метке в ответ на событие **плайстатечанже** .</span><span class="sxs-lookup"><span data-stu-id="44c9e-118">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="44c9e-119">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="44c9e-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the frameRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.frameRate != 0)
            {
                frameRateLabel.Text = "Current Frame Rate: " + player.network.frameRate + " K bits/second";
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

    &#39; Display the frameRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.frameRate <> 0) Then

                frameRateLabel.Text = &quot;Current Frame Rate: &quot; + player.network.frameRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="44c9e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="44c9e-120">Requirements</span></span>



| <span data-ttu-id="44c9e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="44c9e-121">Requirement</span></span> | <span data-ttu-id="44c9e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="44c9e-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44c9e-123">Версия</span><span class="sxs-lookup"><span data-stu-id="44c9e-123">Version</span></span><br/>   | <span data-ttu-id="44c9e-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="44c9e-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="44c9e-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="44c9e-125">Namespace</span></span><br/> | <span data-ttu-id="44c9e-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="44c9e-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="44c9e-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="44c9e-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="44c9e-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="44c9e-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44c9e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44c9e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44c9e-130">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="44c9e-130">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="44c9e-131">**Ивмпнетворк. Енкодедфрамерате (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="44c9e-131">**IWMPNetwork.encodedFrameRate (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-encodedframerate--vb-and-c.md)
</dt> </dl>

 

 





