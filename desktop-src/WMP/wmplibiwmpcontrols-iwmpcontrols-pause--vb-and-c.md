---
title: Метод Pause Ивмпконтролс
description: Метод Pause приостанавливает воспроизведение элемента мультимедиа. | Метод Pause Ивмпконтролс
ms.assetid: 1d9ebaf3-84b4-458d-a393-2b685cd0dbfb
keywords:
- приостановить метод проигрыватель Windows Media Player
- приостановить метод проигрыватель Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, метод Pause
topic_type:
- apiref
api_name:
- IWMPControls.pause
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5cf89cfef66c84be76a529d9c0cef6ec3ae6ac40
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689298"
---
# <a name="iwmpcontrolspause-method"></a><span data-ttu-id="92b04-107">Ивмпконтролс: метод:p Аусе</span><span class="sxs-lookup"><span data-stu-id="92b04-107">IWMPControls::pause method</span></span>

<span data-ttu-id="92b04-108">Метод **Pause** приостанавливает воспроизведение элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="92b04-108">The **pause** method pauses playback of the media item.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b04-109">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="92b04-109">Syntax</span></span>


```CSharp
public void pause();
```


```VB

Public Sub pause()
Implements IWMPControls.pause
```





## <a name="parameters"></a><span data-ttu-id="92b04-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="92b04-110">Parameters</span></span>

<span data-ttu-id="92b04-111">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="92b04-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="92b04-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="92b04-112">Return value</span></span>

<span data-ttu-id="92b04-113">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="92b04-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92b04-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92b04-114">Remarks</span></span>

<span data-ttu-id="92b04-115">При приостановке файла проигрыватель Windows Media не предоставляет никаких системных ресурсов, таких как звуковое устройство.</span><span class="sxs-lookup"><span data-stu-id="92b04-115">When a file is paused, Windows Media Player does not give up any system resources, such as the audio device.</span></span>

<span data-ttu-id="92b04-116">Чтобы определить, можно ли приостановить определенный тип носителя, передайте значение **Свойства** **ивмпконтролс. Available** (метод **ивмпконтролс. Get, \_ доступного** в C#) к свойству "Pause".</span><span class="sxs-lookup"><span data-stu-id="92b04-116">To determine whether a particular media type can be paused, pass the **System.String** value "pause" to the **IWMPControls.isAvailable** property (the **IWMPControls.get\_isAvailable** method in C#).</span></span>

## <a name="examples"></a><span data-ttu-id="92b04-117">Примеры</span><span class="sxs-lookup"><span data-stu-id="92b04-117">Examples</span></span>

<span data-ttu-id="92b04-118">В следующем примере используется **приостановка** для приостановки воспроизведения текущего элемента мультимедиа в ответ на событие щелчка кнопки.</span><span class="sxs-lookup"><span data-stu-id="92b04-118">The following example uses **pause** to pause playback of the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="92b04-119">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="92b04-119">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void pauseButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("pause"))
    {
        controls.pause();
    }
}
```


```VB

Public Sub pauseButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles pauseButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;pause&quot;)) Then

        controls.pause()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="92b04-120">Требования</span><span class="sxs-lookup"><span data-stu-id="92b04-120">Requirements</span></span>



| <span data-ttu-id="92b04-121">Требование</span><span class="sxs-lookup"><span data-stu-id="92b04-121">Requirement</span></span> | <span data-ttu-id="92b04-122">Значение</span><span class="sxs-lookup"><span data-stu-id="92b04-122">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b04-123">Версия</span><span class="sxs-lookup"><span data-stu-id="92b04-123">Version</span></span><br/>   | <span data-ttu-id="92b04-124">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="92b04-124">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="92b04-125">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="92b04-125">Namespace</span></span><br/> | <span data-ttu-id="92b04-126">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="92b04-126">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="92b04-127">Сборка</span><span class="sxs-lookup"><span data-stu-id="92b04-127">Assembly</span></span><br/>  | <dl> <span data-ttu-id="92b04-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="92b04-128"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92b04-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92b04-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b04-130">**Интерфейс Ивмпконтролс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="92b04-130">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="92b04-131">**Ивмпконтролс. доступ (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="92b04-131">**IWMPControls.isAvailable (VB and C#)**</span></span>](iwmpcontrols-isavailable--vb-and-c.md)
</dt> </dl>

 

 





