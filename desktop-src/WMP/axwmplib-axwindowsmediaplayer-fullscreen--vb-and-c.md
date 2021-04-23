---
title: Аксвиндовсмедиаплайер. полноэкранное свойство
description: Свойство «во весь экран» получает или задает значение, указывающее, воспроизводится ли видео в полноэкранном режиме.
ms.assetid: 6c48a54a-e0f1-4bf5-8a53-7ccc78fc76ad
keywords:
- Полноэкранное свойство проигрывателя Windows Media Player
- свойство "Полноэкранный" проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство полноэкранного режима
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.fullScreen
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23bfb1a2c67ecfa3ba7cced6f0ccb564bb387b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105694449"
---
# <a name="axwindowsmediaplayerfullscreen-property"></a><span data-ttu-id="2138a-106">Аксвиндовсмедиаплайер. полноэкранное свойство</span><span class="sxs-lookup"><span data-stu-id="2138a-106">AxWindowsMediaPlayer.fullScreen property</span></span>

<span data-ttu-id="2138a-107">Свойство «во весь экран» получает или задает значение, указывающее, воспроизводится ли видео в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="2138a-107">The fullScreen property gets or sets a value indicating whether video content is played in full-screen mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="2138a-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="2138a-108">Syntax</span></span>


```CSharp
public System.Boolean fullScreen {get; set;}
```


```VB

Public Property fullScreen As System.Boolean
```





## <a name="property-value"></a><span data-ttu-id="2138a-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="2138a-109">Property value</span></span>

<span data-ttu-id="2138a-110">Значение System. Boolean, указывающее, воспроизводится ли содержимое в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="2138a-110">A System.Boolean value that indicates whether content is played in full-screen mode.</span></span> <span data-ttu-id="2138a-111">Значением по умолчанию является false.</span><span class="sxs-lookup"><span data-stu-id="2138a-111">The default value is false.</span></span>

## <a name="remarks"></a><span data-ttu-id="2138a-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2138a-112">Remarks</span></span>

<span data-ttu-id="2138a-113">Чтобы полноэкранный режим работал правильно при внедрении элемента управления проигрывателя Windows Media, область отображения видео должна иметь высоту и ширину по крайней мере на один пиксель.</span><span class="sxs-lookup"><span data-stu-id="2138a-113">For full-screen mode to work properly when embedding the Windows Media Player control, the video display area must have a height and width of at least one pixel.</span></span> <span data-ttu-id="2138a-114">Если для **uiMode** задано значение "Mini" или "Full", то высота самого элемента управления должна быть 65 или больше для размещения видеообласти в дополнение к пользовательскому интерфейсу.</span><span class="sxs-lookup"><span data-stu-id="2138a-114">If **uiMode** is set to "mini" or "full", the height of the control itself must be 65 or greater to accommodate the video display area in addition to the user interface.</span></span>

<span data-ttu-id="2138a-115">Если для **uiMode** задано значение "Невидимый", то установка этого свойства в значение true вызовет ошибку и не влияет на поведение элемента управления.</span><span class="sxs-lookup"><span data-stu-id="2138a-115">If **uiMode** is set to "invisible", then setting this property to true raises an error and does not affect the behavior of the control.</span></span>

<span data-ttu-id="2138a-116">Во время воспроизведения в полноэкранном режиме проигрыватель Windows Media скрывает курсор мыши, когда [енаблеконтекстмену](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) равняется false, а **uiMode** равно «None».</span><span class="sxs-lookup"><span data-stu-id="2138a-116">During full-screen playback, Windows Media Player hides the mouse cursor when [enableContextMenu](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md) equals false and **uiMode** equals "none".</span></span>

<span data-ttu-id="2138a-117">Если для **uiMode** задано значение Full или Mini, проигрыватель Windows Media отображает элементы управления движением в полноэкранном режиме при перемещении курсора мыши.</span><span class="sxs-lookup"><span data-stu-id="2138a-117">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode when the mouse cursor moves.</span></span> <span data-ttu-id="2138a-118">По истечении короткого интервала перемещения мыши элементы управления транспорта скрываются.</span><span class="sxs-lookup"><span data-stu-id="2138a-118">After a brief interval of no mouse movement, the transport controls are hidden.</span></span> <span data-ttu-id="2138a-119">Если для **uiMode** задано значение "нет", никакие элементы управления не отображаются в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="2138a-119">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

> [!Note]  
> <span data-ttu-id="2138a-120">Для отображения элементов управления транспорта в полноэкранном режиме требуется операционная система Windows XP.</span><span class="sxs-lookup"><span data-stu-id="2138a-120">Displaying transport controls in full-screen mode requires the Windows XP operating system.</span></span>

 

<span data-ttu-id="2138a-121">Если элементы управления передачей не отображаются в полноэкранном режиме, проигрыватель Windows Media автоматически выходит из полноэкранного режима при остановке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="2138a-121">If transport controls are not displayed in full-screen mode, then Windows Media Player automatically exits full-screen mode when playback stops.</span></span>

## <a name="examples"></a><span data-ttu-id="2138a-122">Примеры</span><span class="sxs-lookup"><span data-stu-id="2138a-122">Examples</span></span>

<span data-ttu-id="2138a-123">В следующем примере создается кнопка, которая использует свойство "полноэкранное" для переключения внедренного объекта проигрывателя в полноэкранный режим.</span><span class="sxs-lookup"><span data-stu-id="2138a-123">The following example creates a button that uses the fullScreen property to switch an embedded player object to full-screen mode.</span></span> <span data-ttu-id="2138a-124">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="2138a-124">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
private void fullScreen_Click(object sender, System.EventArgs e)
{
    // If the player is playing, switch to full screen. 
    if (player.playState == WMPLib.WMPPlayState.wmppsPlaying)
    {
        player.fullScreen = true;
    }
}
```


```VB

Public Sub fullScreen_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles fullScreen.Click

    &#39; If the player is playing, switch to full screen. 
    If (player.playState = WMPLib.WMPPlayState.wmppsPlaying) Then

        player.fullScreen = True

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="2138a-125">Требования</span><span class="sxs-lookup"><span data-stu-id="2138a-125">Requirements</span></span>



| <span data-ttu-id="2138a-126">Требование</span><span class="sxs-lookup"><span data-stu-id="2138a-126">Requirement</span></span> | <span data-ttu-id="2138a-127">Значение</span><span class="sxs-lookup"><span data-stu-id="2138a-127">Value</span></span> |
|----------------------|--------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2138a-128">Версия</span><span class="sxs-lookup"><span data-stu-id="2138a-128">Version</span></span><br/>   | <span data-ttu-id="2138a-129">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="2138a-129">Windows Media Player 9 Series or later</span></span><br/>                                                                  |
| <span data-ttu-id="2138a-130">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="2138a-130">Namespace</span></span><br/> | <span data-ttu-id="2138a-131">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="2138a-131">**AxWMPLib**</span></span><br/>                                                                                            |
| <span data-ttu-id="2138a-132">Сборка</span><span class="sxs-lookup"><span data-stu-id="2138a-132">Assembly</span></span><br/>  | <dl> <span data-ttu-id="2138a-133"><dt>Аксинтероп. Вмплиб (AxInterop.WMPLib.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="2138a-133"><dt>AxInterop.WMPLib (AxInterop.WMPLib.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2138a-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2138a-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2138a-135">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2138a-135">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="2138a-136">**Аксвиндовсмедиаплайер. uiMode (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="2138a-136">**AxWindowsMediaPlayer.uiMode (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-uimode--vb-and-c.md)
</dt> </dl>

 

 





