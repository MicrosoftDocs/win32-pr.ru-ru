---
title: Свойство пропускной способности Ивмпнетворк
description: Свойство пропускной способности получает текущую пропускную способность элемента мультимедиа.
ms.assetid: 4355aa14-bca7-4b46-aad5-3e3796a54735
keywords:
- Свойство пропускной способности Windows Media Player
- Свойство пропускной способности проигрыватель Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство пропускной способности
topic_type:
- apiref
api_name:
- IWMPNetwork.bandWidth
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df9a55f9d5c6724c428b75a4171c2e8b7ca13d18
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694914"
---
# <a name="iwmpnetworkbandwidth-property"></a><span data-ttu-id="aba3d-106">Свойство Ивмпнетворк:: пропускная способность</span><span class="sxs-lookup"><span data-stu-id="aba3d-106">IWMPNetwork::bandWidth property</span></span>

<span data-ttu-id="aba3d-107">Свойство **пропускной способности** получает текущую пропускную способность элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="aba3d-107">The **bandWidth** property gets the current bandwidth of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="aba3d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="aba3d-108">Syntax</span></span>


```CSharp
public System.Int32 bandWidth {get; set;}
```


```VB

Public ReadOnly Property bandWidth As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="aba3d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="aba3d-109">Property value</span></span>

<span data-ttu-id="aba3d-110">Объект **System. Int32** , который является пропускной способностью.</span><span class="sxs-lookup"><span data-stu-id="aba3d-110">A **System.Int32** that is the bandwidth.</span></span>

## <a name="remarks"></a><span data-ttu-id="aba3d-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="aba3d-111">Remarks</span></span>

<span data-ttu-id="aba3d-112">Значение, полученное с помощью **аксвиндовсмедиаплайер. URL** , будет равно нулю, если URL-адрес не задан.</span><span class="sxs-lookup"><span data-stu-id="aba3d-112">The value retrieved through **AxWindowsMediaPlayer.URL** will be zero if the URL is not set.</span></span> <span data-ttu-id="aba3d-113">Это свойство допустимо только для потокового мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="aba3d-113">This property is valid only for streaming media.</span></span>

## <a name="examples"></a><span data-ttu-id="aba3d-114">Примеры</span><span class="sxs-lookup"><span data-stu-id="aba3d-114">Examples</span></span>

<span data-ttu-id="aba3d-115">В следующем примере **пропускная способность** используется для вывода текущей пропускной способности мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="aba3d-115">The following example uses **bandWidth** to display the current media bandwidth.</span></span> <span data-ttu-id="aba3d-116">Сведения отображаются в метке в ответ на событие **плайстатечанже** .</span><span class="sxs-lookup"><span data-stu-id="aba3d-116">The information is displayed in a label in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="aba3d-117">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="aba3d-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the bandwidth when the player is playing. 
    switch (e.newState)
    {
        case 3:  // Play State = WMPLib.WMPPlayState.wmppsPlaying = 3
            if (player.network.bandWidth != 0)
            {
                bandWidthLabel.Text = "Current Bandwidth: " + player.network.bandWidth + " K bits/second";
            }
            else
            {
                bandWidthLabel.Text = "Bandwidth is only available for streaming media.";
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

    &#39; Display the bandWidth when the player is playing. 
    Select Case e.newState

        Case 3 &#39; Play State = WMPLib.WMPPlayState.wmppsPlaying = 3

            If (player.network.bandWidth <> 0) Then

                bandWidthLabel.Text = &quot;Current Bandwidth: &quot; + player.network.bandWidth + &quot; K bits/second&quot;

            Else

                bandWidthLabel.Text = &quot;Bandwidth is only available for streaming media.&quot;

            End If

    End Select

End Sub
```





## <a name="requirements"></a><span data-ttu-id="aba3d-118">Требования</span><span class="sxs-lookup"><span data-stu-id="aba3d-118">Requirements</span></span>



| <span data-ttu-id="aba3d-119">Требование</span><span class="sxs-lookup"><span data-stu-id="aba3d-119">Requirement</span></span> | <span data-ttu-id="aba3d-120">Значение</span><span class="sxs-lookup"><span data-stu-id="aba3d-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aba3d-121">Версия</span><span class="sxs-lookup"><span data-stu-id="aba3d-121">Version</span></span><br/>   | <span data-ttu-id="aba3d-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="aba3d-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="aba3d-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="aba3d-123">Namespace</span></span><br/> | <span data-ttu-id="aba3d-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="aba3d-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="aba3d-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="aba3d-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="aba3d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="aba3d-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aba3d-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="aba3d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba3d-128">**Аксвиндовсмедиаплайер. URL (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="aba3d-128">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="aba3d-129">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="aba3d-129">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





