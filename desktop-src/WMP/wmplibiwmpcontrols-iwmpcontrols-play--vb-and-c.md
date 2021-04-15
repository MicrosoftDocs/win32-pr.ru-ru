---
title: Метод Play Ивмпконтролс
description: Метод Play начинает воспроизведение текущего элемента мультимедиа или возобновляет воспроизведение приостановленного элемента.
ms.assetid: 02e00df6-4dc1-44bb-9826-e69e8298ccaa
keywords:
- воспроизвести метод проигрыватель Windows Media
- метод Play проигрыватель Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, метод Play
topic_type:
- apiref
api_name:
- IWMPControls.play
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fd87a2e2ba3d53b119df328fa68668c91c78d6d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689297"
---
# <a name="iwmpcontrolsplay-method"></a><span data-ttu-id="b72b0-106">Ивмпконтролс: метод макетирования:p</span><span class="sxs-lookup"><span data-stu-id="b72b0-106">IWMPControls::play method</span></span>

<span data-ttu-id="b72b0-107">Метод **Play** начинает воспроизведение текущего элемента мультимедиа или возобновляет воспроизведение приостановленного элемента.</span><span class="sxs-lookup"><span data-stu-id="b72b0-107">The **play** method begins playback of the current media item, or resumes playback of a paused item.</span></span>

## <a name="syntax"></a><span data-ttu-id="b72b0-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="b72b0-108">Syntax</span></span>


```CSharp
public void play();
```


```VB

Public Sub play()
Implements IWMPControls.play
```





## <a name="parameters"></a><span data-ttu-id="b72b0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="b72b0-109">Parameters</span></span>

<span data-ttu-id="b72b0-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="b72b0-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b72b0-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b72b0-111">Return value</span></span>

<span data-ttu-id="b72b0-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="b72b0-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b72b0-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b72b0-113">Remarks</span></span>

<span data-ttu-id="b72b0-114">Если этот метод вызывается во время быстрой пересылки или перемотки, скорость воспроизведения (значение **ивмпсеттингс. rate**) устанавливается равным 1,0.</span><span class="sxs-lookup"><span data-stu-id="b72b0-114">If this method is called while fast-forwarding or rewinding, the rate of playback (the value of **IWMPSettings.rate**) is set to 1.0.</span></span>

## <a name="examples"></a><span data-ttu-id="b72b0-115">Примеры</span><span class="sxs-lookup"><span data-stu-id="b72b0-115">Examples</span></span>

<span data-ttu-id="b72b0-116">В следующем примере функция **Play** используется для воспроизведения текущего элемента мультимедиа в ответ на событие щелчка кнопки.</span><span class="sxs-lookup"><span data-stu-id="b72b0-116">The following example uses **play** to play the current media item in response to the Click event of a button.</span></span> <span data-ttu-id="b72b0-117">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="b72b0-117">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid. 
    if (controls.get_isAvailable("play"))
    {
        controls.play();
    }
}
```


```VB

Public Sub playButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid. 
    If (controls.isAvailable(&quot;play&quot;)) Then

        controls.play()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="b72b0-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b72b0-118">Requirements</span></span>



| <span data-ttu-id="b72b0-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b72b0-119">Requirement</span></span> | <span data-ttu-id="b72b0-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b72b0-120">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b72b0-121">Версия</span><span class="sxs-lookup"><span data-stu-id="b72b0-121">Version</span></span><br/>   | <span data-ttu-id="b72b0-122">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="b72b0-122">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="b72b0-123">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="b72b0-123">Namespace</span></span><br/> | <span data-ttu-id="b72b0-124">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="b72b0-124">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="b72b0-125">Сборка</span><span class="sxs-lookup"><span data-stu-id="b72b0-125">Assembly</span></span><br/>  | <dl> <span data-ttu-id="b72b0-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="b72b0-126"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b72b0-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b72b0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b72b0-128">**Интерфейс Ивмпконтролс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b72b0-128">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b72b0-129">**Ивмпконтролс. Плайитем (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b72b0-129">**IWMPControls.playItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-playitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="b72b0-130">**Ивмпсеттингс. rate (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="b72b0-130">**IWMPSettings.rate (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





