---
title: Ивмпконтролс следующий метод
description: Следующий метод задает следующий элемент списка воспроизведения в качестве текущего элемента.
ms.assetid: 3f82ef25-a1e0-4845-b0ed-dd6463719577
keywords:
- Следующий метод проигрывателя Windows Media
- Следующий метод проигрывателя Windows Media Player, интерфейс Ивмпконтролс
- Интерфейс Ивмпконтролс Windows Media Player, метод Next
topic_type:
- apiref
api_name:
- IWMPControls.next
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8444ba7d9209759cb64c4b582e1af9d074332ae
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689299"
---
# <a name="iwmpcontrolsnext-method"></a><span data-ttu-id="2683e-106">Метод Ивмпконтролс:: Next</span><span class="sxs-lookup"><span data-stu-id="2683e-106">IWMPControls::next method</span></span>

<span data-ttu-id="2683e-107">**Следующий** метод задает следующий элемент списка воспроизведения в качестве текущего элемента.</span><span class="sxs-lookup"><span data-stu-id="2683e-107">The **next** method sets the next item in the playlist as the current item.</span></span>

## <a name="syntax"></a><span data-ttu-id="2683e-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2683e-108">Syntax</span></span>


```CSharp
public void next();
```


```VB

Public Sub next()
Implements IWMPControls.next
```





## <a name="parameters"></a><span data-ttu-id="2683e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="2683e-109">Parameters</span></span>

<span data-ttu-id="2683e-110">Этот метод не имеет параметров.</span><span class="sxs-lookup"><span data-stu-id="2683e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2683e-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2683e-111">Return value</span></span>

<span data-ttu-id="2683e-112">Этот метод не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="2683e-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2683e-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2683e-113">Remarks</span></span>

<span data-ttu-id="2683e-114">Если список воспроизведения находится в последней записи при вызове **Next** , первая запись списка воспроизведения станет текущей.</span><span class="sxs-lookup"><span data-stu-id="2683e-114">If the playlist is on the last entry when **next** is invoked, the first entry in the playlist will become the current one.</span></span>

<span data-ttu-id="2683e-115">Для списков воспроизведения на стороне сервера этот метод пропускает следующий элемент в списке воспроизведения на стороне сервера, а не в списке воспроизведения клиента.</span><span class="sxs-lookup"><span data-stu-id="2683e-115">For server-side playlists, this method skips to the next item in the server-side playlist, not the client playlist.</span></span>

<span data-ttu-id="2683e-116">При воспроизведении DVD этот метод пропускает следующую логическую главу в последовательности воспроизведения, которая может не быть следующей главой в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="2683e-116">When playing a DVD, this method skips to the next logical chapter in the playback sequence, which may not be the next chapter in the playlist.</span></span> <span data-ttu-id="2683e-117">При воспроизведении изображений DVD-образов этот метод переходит к следующему изображению.</span><span class="sxs-lookup"><span data-stu-id="2683e-117">When playing DVD still images, this method skips to the next image.</span></span>

## <a name="examples"></a><span data-ttu-id="2683e-118">Примеры</span><span class="sxs-lookup"><span data-stu-id="2683e-118">Examples</span></span>

<span data-ttu-id="2683e-119">В следующем примере функция **Next** используется для перехода к следующему элементу в текущем списке воспроизведения в ответ на событие щелчка кнопки.</span><span class="sxs-lookup"><span data-stu-id="2683e-119">The following example uses **next** to move to the next item in the current playlist in response to the Click event of a button.</span></span> <span data-ttu-id="2683e-120">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="2683e-120">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void nextButton_Click(object o, System.EventArgs args)
{
    // To get all of the available functionality of the player controls, cast the
    // value returned by player.Ctlcontrols to a WMPLib.IWMPControls3 interface. 
    WMPLib.IWMPControls3 controls = (WMPLib.IWMPControls3)player.Ctlcontrols;

    // Check first to be sure the operation is valid.
    if (controls.get_isAvailable("next"))
    {
        controls.next();
    }
}
```


```VB

Public Sub nextButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles nextButton.Click

    &#39; To get all of the available functionality of the player controls, Dim the
    &#39; value returned by player.Ctlcontrols as a WMPLib.IWMPControls3 interface.
    Dim controls As WMPLib.IWMPControls3 = player.Ctlcontrols

    &#39; Check first to be sure the operation is valid.
    If (controls.isAvailable(&quot;next&quot;)) Then

        controls.next()

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2683e-121">Требования</span><span class="sxs-lookup"><span data-stu-id="2683e-121">Requirements</span></span>



| <span data-ttu-id="2683e-122">Требование</span><span class="sxs-lookup"><span data-stu-id="2683e-122">Requirement</span></span> | <span data-ttu-id="2683e-123">Значение</span><span class="sxs-lookup"><span data-stu-id="2683e-123">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2683e-124">Версия</span><span class="sxs-lookup"><span data-stu-id="2683e-124">Version</span></span><br/>   | <span data-ttu-id="2683e-125">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2683e-125">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="2683e-126">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2683e-126">Namespace</span></span><br/> | <span data-ttu-id="2683e-127">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="2683e-127">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="2683e-128">Сборка</span><span class="sxs-lookup"><span data-stu-id="2683e-128">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2683e-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2683e-129"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2683e-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2683e-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2683e-131">**Интерфейс Ивмпконтролс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2683e-131">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2683e-132">**Ивмпконтролс. Previous (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2683e-132">**IWMPControls.previous (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-previous--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2683e-133">**Ивмпконтролс. останавливаться (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2683e-133">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> </dl>

 

 





