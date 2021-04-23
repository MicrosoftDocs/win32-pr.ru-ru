---
title: Ивмпконтролс Фастреверсе, метод
description: Метод Фастреверсе запускает быстрое воспроизведение элемента мультимедиа в обратном направлении.
ms.assetid: 5c872e8d-2ffc-425f-a4dd-938ddd1426e0
keywords:
- Фастреверсе метод Windows Media Player
- Фастреверсе метод проигрывателя Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, метод Фастреверсе
topic_type:
- apiref
api_name:
- IWMPControls.fastReverse
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7061481aea13b0ed83c3a3d0eb47ca24b940358b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689306"
---
# <a name="iwmpcontrolsfastreverse-method"></a><span data-ttu-id="0ed31-106">Метод Ивмпконтролс:: Фастреверсе</span><span class="sxs-lookup"><span data-stu-id="0ed31-106">IWMPControls::fastReverse method</span></span>

<span data-ttu-id="0ed31-107">Метод **фастреверсе** запускает быстрое воспроизведение элемента мультимедиа в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="0ed31-107">The **fastReverse** method starts fast play of the media item in the reverse direction.</span></span>

## <a name="syntax"></a><span data-ttu-id="0ed31-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0ed31-108">Syntax</span></span>


```CSharp
public void fastReverse();
```


```VB

Public Sub fastReverse()
Implements IWMPControls.fastReverse
```





## <a name="parameters"></a><span data-ttu-id="0ed31-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0ed31-109">Parameters</span></span>

<span data-ttu-id="0ed31-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="0ed31-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0ed31-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0ed31-111">Return value</span></span>

<span data-ttu-id="0ed31-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="0ed31-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0ed31-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0ed31-113">Remarks</span></span>

<span data-ttu-id="0ed31-114">Метод **фастреверсе** просматривает клип в обратную, в пять раз превышающую нормальную скорость, отображая только ключевые кадры, если это видеофайл.</span><span class="sxs-lookup"><span data-stu-id="0ed31-114">The **fastReverse** method scans the clip in reverse at five times the normal speed, displaying only the key frames if it is a video file.</span></span> <span data-ttu-id="0ed31-115">Вызов **фастреверсе** эквивалентен указанию-5,0 для ставки путем установки свойства **ивмпсеттингс. rate** .</span><span class="sxs-lookup"><span data-stu-id="0ed31-115">Calling **fastReverse** is equivalent to specifying -5.0 for the rate by setting the **IWMPSettings.rate** property.</span></span> <span data-ttu-id="0ed31-116">Если частота впоследствии изменилась или при вызове **ивмпконтролс. Play** или **ивмпконтролс. останавливают** , проигрыватель Windows Media прекратит обратный.</span><span class="sxs-lookup"><span data-stu-id="0ed31-116">If the rate is subsequently changed, or if **IWMPControls.play** or **IWMPControls.stop** is called, Windows Media Player will cease fast reverse.</span></span>

<span data-ttu-id="0ed31-117">Если элемент является частью списка воспроизведения, **фастреверсе** останавливается в начале текущей записи. Например, если параметр Track 3 находится в **фастреверсе**, то при достижении начала Track 3 проигрыватель Windows Media не будет переходить к разделу Track 2.</span><span class="sxs-lookup"><span data-stu-id="0ed31-117">If the item is part of a playlist, **fastReverse** stops at the beginning of the current track. For instance, if track 3 is in **fastReverse**, when the beginning of track 3 is reached, Windows Media Player will not go to track 2.</span></span> <span data-ttu-id="0ed31-118">При вызове **фастреверсе** Счетчик воспроизведения не увеличивается.</span><span class="sxs-lookup"><span data-stu-id="0ed31-118">The play count is not incremented when calling **fastReverse**.</span></span>

<span data-ttu-id="0ed31-119">При вызове **ивмпконтролс. фастфорвард** во время выполнения **фастреверсе** **фастреверсе** будет остановлен и **ивмпконтролс. фастфорвард** начнется.</span><span class="sxs-lookup"><span data-stu-id="0ed31-119">If you call **IWMPControls.fastForward** while **fastReverse** is running, **fastReverse** will be stopped and **IWMPControls.fastForward** will begin.</span></span>

<span data-ttu-id="0ed31-120">Этот метод не работает для широковещательных трансляций и определенных типов цифровых носителей.</span><span class="sxs-lookup"><span data-stu-id="0ed31-120">This method does not work for live broadcasts and certain digital media types.</span></span> <span data-ttu-id="0ed31-121">Чтобы определить, можно ли использовать параметр "Быстрый обратный" в картинке, передайте значение **System. String** "фастреверсе" в свойство **ивмпконтролс. Available** (метод **ивмпконтролс. Get, \_ доступный** в C#).</span><span class="sxs-lookup"><span data-stu-id="0ed31-121">To determine whether you can use fast reverse in a clip, pass the **System.String** value "FastReverse" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="0ed31-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="0ed31-122">Examples</span></span>

<span data-ttu-id="0ed31-123">В следующем примере **фастреверсе** используется для отмены текущего элемента мультимедиа в ответ на событие щелчка кнопки.</span><span class="sxs-lookup"><span data-stu-id="0ed31-123">The following example uses **fastReverse** to reverse the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="0ed31-124">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="0ed31-124">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void fastReverseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("fastReverse"))
    {
        controls.fastReverse();
    }
}
```


```VB

Public Sub fastReverseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fastReverseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;fastReverse&quot;)) Then

        controls.fastReverse()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="0ed31-125">Требования</span><span class="sxs-lookup"><span data-stu-id="0ed31-125">Requirements</span></span>



| <span data-ttu-id="0ed31-126">Требование</span><span class="sxs-lookup"><span data-stu-id="0ed31-126">Requirement</span></span> | <span data-ttu-id="0ed31-127">Значение</span><span class="sxs-lookup"><span data-stu-id="0ed31-127">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0ed31-128">Версия</span><span class="sxs-lookup"><span data-stu-id="0ed31-128">Version</span></span><br/>   | <span data-ttu-id="0ed31-129">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="0ed31-129">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="0ed31-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="0ed31-130">Namespace</span></span><br/> | <span data-ttu-id="0ed31-131">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="0ed31-131">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="0ed31-132">Сборка</span><span class="sxs-lookup"><span data-stu-id="0ed31-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="0ed31-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="0ed31-133"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ed31-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0ed31-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ed31-135">**Интерфейс Ивмпконтролс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="0ed31-135">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ed31-136">**Ивмпконтролс. Фастфорвард (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="0ed31-136">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ed31-137">**Ивмпконтролс. доступ (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="0ed31-137">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ed31-138">**Ивмпконтролс. Play (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="0ed31-138">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ed31-139">**Ивмпконтролс. останавливаться (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="0ed31-139">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="0ed31-140">**Ивмпсеттингс. rate (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="0ed31-140">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





