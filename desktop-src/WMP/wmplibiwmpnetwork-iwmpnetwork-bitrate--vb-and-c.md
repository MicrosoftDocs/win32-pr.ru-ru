---
title: Свойство Ивмпнетворк скорость
description: Свойство скорость получает текущую скорость получения.
ms.assetid: f7dda557-3954-45ed-9eac-6d27109e2dfa
keywords:
- свойство "скорость" проигрывателя Windows Media Player
- свойство "скорость" проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство "скорость"
topic_type:
- apiref
api_name:
- IWMPNetwork.bitRate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f64039eb960a928f5268643e18d1a01b9034d5d1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694683"
---
# <a name="iwmpnetworkbitrate-property"></a><span data-ttu-id="1daf0-106">Свойство Ивмпнетворк:: скорость</span><span class="sxs-lookup"><span data-stu-id="1daf0-106">IWMPNetwork::bitRate property</span></span>

<span data-ttu-id="1daf0-107">Свойство **скорость** получает текущую скорость получения.</span><span class="sxs-lookup"><span data-stu-id="1daf0-107">The **bitRate** property gets the current bit rate being received.</span></span>

## <a name="syntax"></a><span data-ttu-id="1daf0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="1daf0-108">Syntax</span></span>


```CSharp
public System.Int32 bitRate {get; set;}
```


```VB

Public ReadOnly Property bitRate As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="1daf0-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="1daf0-109">Property value</span></span>

<span data-ttu-id="1daf0-110">Значение **System. Int32** , которое является скоростью потока.</span><span class="sxs-lookup"><span data-stu-id="1daf0-110">A **System.Int32** that is the bit rate.</span></span>

## <a name="remarks"></a><span data-ttu-id="1daf0-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="1daf0-111">Remarks</span></span>

<span data-ttu-id="1daf0-112">Значение этого свойства представляет собой комбинацию скорости потока видео и звуковых потоков.</span><span class="sxs-lookup"><span data-stu-id="1daf0-112">The value of this property is a combination of the bit rates of both video and audio streams.</span></span>

## <a name="examples"></a><span data-ttu-id="1daf0-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="1daf0-113">Examples</span></span>

<span data-ttu-id="1daf0-114">В следующем примере скорость **используется для** показа текущей скорости мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="1daf0-114">The following example uses **bitRate** to display the current media bit rate.</span></span> <span data-ttu-id="1daf0-115">Сведения отображаются в метке в ответ на событие **плайстатечанже** .</span><span class="sxs-lookup"><span data-stu-id="1daf0-115">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="1daf0-116">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="1daf0-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bitRate when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bitRate != 0)
            {
                bitRateLabel.Text = "Current Bit Rate: " + player.network.bitRate + " K bits/second";
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

    &#39; Display the bitRate when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bitRate <> 0) Then

                bitRateLabel.Text = &quot;Current Bit Rate: &quot; + player.network.bitRate + &quot; K bits/second&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="1daf0-117">Требования</span><span class="sxs-lookup"><span data-stu-id="1daf0-117">Requirements</span></span>



| <span data-ttu-id="1daf0-118">Требование</span><span class="sxs-lookup"><span data-stu-id="1daf0-118">Requirement</span></span> | <span data-ttu-id="1daf0-119">Значение</span><span class="sxs-lookup"><span data-stu-id="1daf0-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1daf0-120">Версия</span><span class="sxs-lookup"><span data-stu-id="1daf0-120">Version</span></span><br/>   | <span data-ttu-id="1daf0-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="1daf0-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="1daf0-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="1daf0-122">Namespace</span></span><br/> | <span data-ttu-id="1daf0-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="1daf0-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="1daf0-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="1daf0-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="1daf0-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="1daf0-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1daf0-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="1daf0-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1daf0-127">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="1daf0-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





