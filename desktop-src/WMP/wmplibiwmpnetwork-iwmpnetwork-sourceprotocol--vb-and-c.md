---
title: Ивмпнетворк Саурцепротокол, свойство
description: Свойство Саурцепротокол получает исходный протокол, используемый для получения данных.
ms.assetid: db1d7651-3f25-4ac9-a3e1-dc3a8ddf8c40
keywords:
- Проигрыватель Windows Media для свойства Саурцепротокол
- Саурцепротокол свойство проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство Саурцепротокол
topic_type:
- apiref
api_name:
- IWMPNetwork.sourceProtocol
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5017e1a053c124a1f7f50668c6f392eb541d57f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105708588"
---
# <a name="iwmpnetworksourceprotocol-property"></a><span data-ttu-id="b037c-106">Свойство Ивмпнетворк:: Саурцепротокол</span><span class="sxs-lookup"><span data-stu-id="b037c-106">IWMPNetwork::sourceProtocol property</span></span>

<span data-ttu-id="b037c-107">Свойство **саурцепротокол** получает исходный протокол, используемый для получения данных.</span><span class="sxs-lookup"><span data-stu-id="b037c-107">The **sourceProtocol** property gets the source protocol used to receive data.</span></span>

## <a name="syntax"></a><span data-ttu-id="b037c-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b037c-108">Syntax</span></span>


```CSharp
public System.String sourceProtocol {get; set;}
```


```VB

Public ReadOnly Property sourceProtocol As System.String
```





## <a name="property-value"></a><span data-ttu-id="b037c-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="b037c-109">Property value</span></span>

<span data-ttu-id="b037c-110">**Строка System. String** , которая является именем исходного протокола.</span><span class="sxs-lookup"><span data-stu-id="b037c-110">A **System.String** that is the name of the source protocol.</span></span>

## <a name="remarks"></a><span data-ttu-id="b037c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b037c-111">Remarks</span></span>

<span data-ttu-id="b037c-112">Это свойство получает строку нулевой длины ("") при воспроизведении компакт-диска или DVD-диска.</span><span class="sxs-lookup"><span data-stu-id="b037c-112">This property gets a zero-length string ("") when playing a CD or DVD.</span></span>

## <a name="examples"></a><span data-ttu-id="b037c-113">Примеры</span><span class="sxs-lookup"><span data-stu-id="b037c-113">Examples</span></span>

<span data-ttu-id="b037c-114">В следующем примере кода используется **саурцепротокол** для вывода исходного протокола, используемого для получения данных.</span><span class="sxs-lookup"><span data-stu-id="b037c-114">The following code example uses **sourceProtocol** to display the source protocol used to receive data.</span></span> <span data-ttu-id="b037c-115">Сведения отображаются в метке в ответ на событие **плайстатечанже** .</span><span class="sxs-lookup"><span data-stu-id="b037c-115">The information is displayed in a label, in response to the **PlayStateChange** Event.</span></span> <span data-ttu-id="b037c-116">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="b037c-116">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the PlayStateChange event.
player.PlayStateChange += new AxWMPLib._WMPOCXEvents_PlayStateChangeEventHandler(player_PlayStateChange);

// Create an event handler for the PlayStateChange event.
private void player_PlayStateChange(object sender, AxWMPLib._WMPOCXEvents_PlayStateChangeEvent e)
{
    // Display the network source protocol when the player is playing by testing for a 
    // play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3. 
    if (e.newState == 3) 
    {
        sourceProtocolLabel.Text = ("Source protocol: " + player.network.sourceProtocol);
    } 
}
```


```VB

' Create an event handler for the PlayStateChange event.
Public Sub player_PlayStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_PlayStateChangeEvent) Handles player.PlayStateChange

    &#39; Display the network source protocol when the player is playing by testing for a 
    &#39; play state enum value of WMPLib.WMPPlayState.wmppsPlaying which equals 3.
    If (e.newState = 3) Then

        sourceProtocolLabel.Text = (&quot;Source protocol: &quot; + player.network.sourceProtocol)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b037c-117">Требования</span><span class="sxs-lookup"><span data-stu-id="b037c-117">Requirements</span></span>



| <span data-ttu-id="b037c-118">Требование</span><span class="sxs-lookup"><span data-stu-id="b037c-118">Requirement</span></span> | <span data-ttu-id="b037c-119">Значение</span><span class="sxs-lookup"><span data-stu-id="b037c-119">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b037c-120">Версия</span><span class="sxs-lookup"><span data-stu-id="b037c-120">Version</span></span><br/>   | <span data-ttu-id="b037c-121">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b037c-121">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b037c-122">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b037c-122">Namespace</span></span><br/> | <span data-ttu-id="b037c-123">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="b037c-123">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b037c-124">Сборка</span><span class="sxs-lookup"><span data-stu-id="b037c-124">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b037c-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b037c-125"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b037c-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b037c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b037c-127">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b037c-127">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





