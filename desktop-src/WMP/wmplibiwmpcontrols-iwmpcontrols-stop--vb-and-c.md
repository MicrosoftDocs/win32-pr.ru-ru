---
title: Метод завершения Ивмпконтролс
description: Метод Stop останавливает воспроизведение элемента мультимедиа. | Метод завершения Ивмпконтролс
ms.assetid: 4be601af-6321-4115-a94d-cfc9228991cb
keywords:
- метод завершения проигрывателя Windows Media Player
- метод завершения проигрывателя Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, метод завершения
topic_type:
- apiref
api_name:
- IWMPControls.stop
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a73271098340ea0cf0a645472b5ef6333ae0f4b2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689294"
---
# <a name="iwmpcontrolsstop-method"></a><span data-ttu-id="3a0dd-107">Метод Ивмпконтролс:: останавливаться</span><span class="sxs-lookup"><span data-stu-id="3a0dd-107">IWMPControls::stop method</span></span>

<span data-ttu-id="3a0dd-108">Метод **Stop** останавливает воспроизведение элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3a0dd-108">The **stop** method stops playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a0dd-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3a0dd-109">Syntax</span></span>


```CSharp
public void stop();
```


```VB

Public Sub stop()
Implements IWMPControls.stop
```





## <a name="parameters"></a><span data-ttu-id="3a0dd-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3a0dd-110">Parameters</span></span>

<span data-ttu-id="3a0dd-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3a0dd-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a0dd-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3a0dd-112">Return value</span></span>

<span data-ttu-id="3a0dd-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3a0dd-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a0dd-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3a0dd-114">Remarks</span></span>

<span data-ttu-id="3a0dd-115">Этот метод заставляет проигрыватель Windows Media освобождать любые системные ресурсы, которые он использует, например звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="3a0dd-115">This method causes Windows Media Player to release any system resources it is using, such as the audio device.</span></span> <span data-ttu-id="3a0dd-116">Однако текущий элемент мультимедиа не освобожден.</span><span class="sxs-lookup"><span data-stu-id="3a0dd-116">The current media item, however, is not released.</span></span>

<span data-ttu-id="3a0dd-117">Когда проигрыватель Windows Media остановлен, текущая позиция воспроизведения в элементе мультимедиа сбрасывается до начала элемента.</span><span class="sxs-lookup"><span data-stu-id="3a0dd-117">When Windows Media Player is stopped, the current playback position in the media item is reset to the beginning of the item.</span></span> <span data-ttu-id="3a0dd-118">При последующем вызове **ивмпконтролс. Play** начнет воспроизведение с начала элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="3a0dd-118">Subsequently calling **IWMPControls.play** will start playback from the beginning of the media item.</span></span> <span data-ttu-id="3a0dd-119">Чтобы остановить операцию воспроизведения без изменения текущей позицией, используйте метод **ивмпконтролс. Pause** .</span><span class="sxs-lookup"><span data-stu-id="3a0dd-119">To halt a play operation without changing the current position, use the **IWMPControls.pause** method.</span></span>

## <a name="examples"></a><span data-ttu-id="3a0dd-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="3a0dd-120">Examples</span></span>

<span data-ttu-id="3a0dd-121">В следующем примере используется функция " **Отключить** " для завершения текущего элемента мультимедиа в ответ на событие щелчка кнопки.</span><span class="sxs-lookup"><span data-stu-id="3a0dd-121">The following example uses **stop** to stop the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="3a0dd-122">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="3a0dd-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void stopButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("stop"))
    {
        controls.stop();
    }
}
```


```VB

Public Sub stopButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles stopButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;stop&quot;)) Then

        controls.stop()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3a0dd-123">Требования</span><span class="sxs-lookup"><span data-stu-id="3a0dd-123">Requirements</span></span>



| <span data-ttu-id="3a0dd-124">Требование</span><span class="sxs-lookup"><span data-stu-id="3a0dd-124">Requirement</span></span> | <span data-ttu-id="3a0dd-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3a0dd-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0dd-126">Версия</span><span class="sxs-lookup"><span data-stu-id="3a0dd-126">Version</span></span><br/>   | <span data-ttu-id="3a0dd-127">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3a0dd-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3a0dd-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3a0dd-128">Namespace</span></span><br/> | <span data-ttu-id="3a0dd-129">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="3a0dd-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3a0dd-130">Сборка</span><span class="sxs-lookup"><span data-stu-id="3a0dd-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3a0dd-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3a0dd-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a0dd-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3a0dd-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a0dd-133">**Интерфейс Ивмпконтролс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3a0dd-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3a0dd-134">**Ивмпконтролс. Next (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3a0dd-134">**IWMPControls.next (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-next--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3a0dd-135">**Ивмпконтролс. Pause (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3a0dd-135">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3a0dd-136">**Ивмпконтролс. Play (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3a0dd-136">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3a0dd-137">**Ивмпконтролс. Previous (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3a0dd-137">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> </dl>

 

 





