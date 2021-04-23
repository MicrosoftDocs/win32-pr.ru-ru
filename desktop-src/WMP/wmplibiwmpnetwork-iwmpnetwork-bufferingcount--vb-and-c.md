---
title: Ивмпнетворк Буфферингкаунт, свойство
description: Свойство Буфферингкаунт возвращает количество попыток буферизации во время воспроизведения.
ms.assetid: 2e3a2914-fc38-4477-8c4c-15b4a2e424dc
keywords:
- Проигрыватель Windows Media для свойства Буфферингкаунт
- Буфферингкаунт свойство проигрывателя Windows Media Player, интерфейс Ивмпнетворк
- Интерфейс Ивмпнетворк Windows Media Player, свойство Буфферингкаунт
topic_type:
- apiref
api_name:
- IWMPNetwork.bufferingCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4958892dd9784ee72b51adfedbbcdee81817b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694682"
---
# <a name="iwmpnetworkbufferingcount-property"></a><span data-ttu-id="6d0be-106">Свойство Ивмпнетворк:: Буфферингкаунт</span><span class="sxs-lookup"><span data-stu-id="6d0be-106">IWMPNetwork::bufferingCount property</span></span>

<span data-ttu-id="6d0be-107">Свойство **буфферингкаунт** возвращает количество попыток буферизации во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6d0be-107">The **bufferingCount** property gets the number of times buffering occurred during playback.</span></span>

## <a name="syntax"></a><span data-ttu-id="6d0be-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="6d0be-108">Syntax</span></span>


```CSharp
public System.Int32 bufferingCount {get; set;}
```


```VB

Public ReadOnly Property bufferingCount As System.Int32
```





## <a name="property-value"></a><span data-ttu-id="6d0be-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="6d0be-109">Property value</span></span>

<span data-ttu-id="6d0be-110">Значение **System. Int32** , которое является счетчиком буферизации.</span><span class="sxs-lookup"><span data-stu-id="6d0be-110">A **System.Int32** that is the buffering count.</span></span>

## <a name="remarks"></a><span data-ttu-id="6d0be-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6d0be-111">Remarks</span></span>

<span data-ttu-id="6d0be-112">Каждый раз, когда воспроизведение останавливается и перезапускается, это свойство сбрасывается до нуля.</span><span class="sxs-lookup"><span data-stu-id="6d0be-112">Each time playback is stopped and restarted, this property is reset to zero.</span></span> <span data-ttu-id="6d0be-113">Если воспроизведение приостановлено, оно не сбрасывается.</span><span class="sxs-lookup"><span data-stu-id="6d0be-113">It is not reset if playback is paused.</span></span>

<span data-ttu-id="6d0be-114">Буферизация применяется только к потоковой передаче содержимого.</span><span class="sxs-lookup"><span data-stu-id="6d0be-114">Buffering applies only to streaming content.</span></span> <span data-ttu-id="6d0be-115">Это свойство получает действительные сведения только во время выполнения, когда URL-адрес для воспроизведения задается с помощью свойства **аксвиндовсмедиаплайер. URL** .</span><span class="sxs-lookup"><span data-stu-id="6d0be-115">This property gets valid information only during run time when the URL for playback is set by using the **AxWindowsMediaPlayer.URL** property.</span></span>

## <a name="examples"></a><span data-ttu-id="6d0be-116">Примеры</span><span class="sxs-lookup"><span data-stu-id="6d0be-116">Examples</span></span>

<span data-ttu-id="6d0be-117">В следующем примере *буфферингкаунт* используется для вывода количества попыток буферизации во время воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="6d0be-117">The following example uses *bufferingCount* to display the number of times buffering occurs during playback.</span></span> <span data-ttu-id="6d0be-118">Сведения отображаются в метке в ответ на событие буферизации.</span><span class="sxs-lookup"><span data-stu-id="6d0be-118">The information is displayed in a label in response to the Buffering Event.</span></span> <span data-ttu-id="6d0be-119">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="6d0be-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// Add a delegate for the Buffering event.
player.Buffering += new AxWMPLib._WMPOCXEvents_BufferingEventHandler(player_Buffering);

// Create an event handler for the Buffering event.
private void player_Buffering(object sender, AxWMPLib._WMPOCXEvents_BufferingEvent e)
{
    // Display the bufferingCount when buffering has started.
    if (e.start == true)
    {
        bufferingCountLabel.Text = ("Buffering count: " + player.network.bufferingCount);
    }  
}
```


```VB

' Create an event handler for the Buffering event.
Public Sub player_Buffering(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_BufferingEvent) Handles player.Buffering

    &#39; Display the bufferingCount when buffering has started.
    If (e.start = True) Then

        bufferingCountLabel.Text = (&quot;Buffering count: &quot; + player.network.bufferingCount)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="6d0be-120">Требования</span><span class="sxs-lookup"><span data-stu-id="6d0be-120">Requirements</span></span>



| <span data-ttu-id="6d0be-121">Требование</span><span class="sxs-lookup"><span data-stu-id="6d0be-121">Requirement</span></span> | <span data-ttu-id="6d0be-122">Значение</span><span class="sxs-lookup"><span data-stu-id="6d0be-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d0be-123">Версия</span><span class="sxs-lookup"><span data-stu-id="6d0be-123">Version</span></span><br/>   | <span data-ttu-id="6d0be-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="6d0be-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="6d0be-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="6d0be-125">Namespace</span></span><br/> | <span data-ttu-id="6d0be-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="6d0be-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="6d0be-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="6d0be-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="6d0be-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="6d0be-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6d0be-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6d0be-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6d0be-130">**Аксвиндовсмедиаплайер. URL (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6d0be-130">**AxWindowsMediaPlayer.URL (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-url--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="6d0be-131">**Интерфейс Ивмпнетворк (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="6d0be-131">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> </dl>

 

 





