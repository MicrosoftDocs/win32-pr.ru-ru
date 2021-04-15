---
title: Ивмпконтролс Фастфорвард, метод
description: Метод Фастфорвард запускает быстрое воспроизведение элемента мультимедиа в прямом направлении. | Ивмпконтролс Фастфорвард, метод
ms.assetid: 44609d63-1d1a-489c-ac17-60b6d3ddc588
keywords:
- Фастфорвард метод Windows Media Player
- Фастфорвард метод проигрывателя Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, метод Фастфорвард
topic_type:
- apiref
api_name:
- IWMPControls.fastForward
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1d99307a7b188b238157af62833273b8c724eab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689309"
---
# <a name="iwmpcontrolsfastforward-method"></a><span data-ttu-id="3f3ee-107">Метод Ивмпконтролс:: Фастфорвард</span><span class="sxs-lookup"><span data-stu-id="3f3ee-107">IWMPControls::fastForward method</span></span>

<span data-ttu-id="3f3ee-108">Метод **фастфорвард** запускает быстрое воспроизведение элемента мультимедиа в прямом направлении.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-108">The **fastForward** method starts fast play of the media item in the forward direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f3ee-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="3f3ee-109">Syntax</span></span>


```CSharp
public void fastForward();
```


```VB

Public Sub fastForward()
Implements IWMPControls.fastForward
```





## <a name="parameters"></a><span data-ttu-id="3f3ee-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f3ee-110">Parameters</span></span>

<span data-ttu-id="3f3ee-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3f3ee-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f3ee-112">Return value</span></span>

<span data-ttu-id="3f3ee-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f3ee-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f3ee-114">Remarks</span></span>

<span data-ttu-id="3f3ee-115">Метод **фастфорвард** воспроизводит клип в пять раз после обычной скорости.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-115">The **fastForward** method plays the clip at five times the normal speed.</span></span> <span data-ttu-id="3f3ee-116">Вызов **фастфорвард** эквивалентен указанию 5,0 для скорости путем установки свойства **ивмпсеттингс. rate** .</span><span class="sxs-lookup"><span data-stu-id="3f3ee-116">Calling **fastForward** is equivalent to specifying 5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="3f3ee-117">Если частота впоследствии изменилась или если вызывается **ивмпконтролс. Play** или **ивмпконтролс. остановка** , проигрыватель Windows Media прекратит быструю пересылку.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-117">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast forwarding.</span></span>

<span data-ttu-id="3f3ee-118">Метод **фастфорвард** не работает для широковещательных трансляций и определенных типов носителей.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-118">The **fastForward** method does not work for live broadcasts and certain media types.</span></span> <span data-ttu-id="3f3ee-119">Чтобы определить, можно ли выполнить быструю пересылку клипа, передайте значение **System. String** "фастфорвард" в свойство **ивмпконтролс. Available** (метод **ивмпконтролс. Get- \_ Available** в C#).</span><span class="sxs-lookup"><span data-stu-id="3f3ee-119">To determine whether you can fast forward in a clip, pass the **System.String** value "FastForward" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="3f3ee-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="3f3ee-120">Examples</span></span>

<span data-ttu-id="3f3ee-121">В следующем примере **фастфорвард** используется для перемотки текущего элемента мультимедиа в ответ на событие щелчка кнопки.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-121">The following example uses **fastForward** to fast-forward the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="3f3ee-122">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="3f3ee-122">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastForwardButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastForward"))
    {
        controls.fastForward();
    }
}
```


```VB

Public Sub fastForwardButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastForwardButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface. 
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastForward&quot;)) Then

        controls.fastForward()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="3f3ee-123">Требования</span><span class="sxs-lookup"><span data-stu-id="3f3ee-123">Requirements</span></span>



| <span data-ttu-id="3f3ee-124">Требование</span><span class="sxs-lookup"><span data-stu-id="3f3ee-124">Requirement</span></span> | <span data-ttu-id="3f3ee-125">Значение</span><span class="sxs-lookup"><span data-stu-id="3f3ee-125">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f3ee-126">Версия</span><span class="sxs-lookup"><span data-stu-id="3f3ee-126">Version</span></span><br/>   | <span data-ttu-id="3f3ee-127">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="3f3ee-127">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="3f3ee-128">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="3f3ee-128">Namespace</span></span><br/> | <span data-ttu-id="3f3ee-129">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="3f3ee-129">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="3f3ee-130">Сборка</span><span class="sxs-lookup"><span data-stu-id="3f3ee-130">Assembly</span></span><br/>  | <dl> <span data-ttu-id="3f3ee-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="3f3ee-131"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f3ee-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f3ee-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f3ee-133">**Интерфейс Ивмпконтролс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3f3ee-133">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3f3ee-134">**Ивмпконтролс. доступ (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3f3ee-134">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3f3ee-135">**Ивмпконтролс. Play (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3f3ee-135">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3f3ee-136">**Ивмпконтролс. останавливаться (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3f3ee-136">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="3f3ee-137">**Ивмпсеттингс. rate (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="3f3ee-137">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





