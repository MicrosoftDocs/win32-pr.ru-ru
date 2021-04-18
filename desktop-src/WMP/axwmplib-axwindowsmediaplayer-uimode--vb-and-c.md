---
title: Аксвиндовсмедиаплайер. uiMode, свойство
description: Свойство uiMode получает или задает значение, указывающее, какие элементы управления отображаются в пользовательском интерфейсе.
ms.assetid: 01034418-be70-44f3-8812-e529c747c9e4
keywords:
- Проигрыватель Windows Media для свойства uiMode
- uiMode свойства проигрывателя Windows Media Player, класс Аксвиндовсмедиаплайер
- Класс Аксвиндовсмедиаплайер Windows Media Player, свойство uiMode
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.uiMode
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33edcf6bdff9e1587269df9eb49c3729099d091e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698850"
---
# <a name="axwindowsmediaplayeruimode-property"></a><span data-ttu-id="e1b9d-106">Аксвиндовсмедиаплайер. uiMode, свойство</span><span class="sxs-lookup"><span data-stu-id="e1b9d-106">AxWindowsMediaPlayer.uiMode property</span></span>

<span data-ttu-id="e1b9d-107">Свойство uiMode получает или задает значение, указывающее, какие элементы управления отображаются в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-107">The uiMode property gets or sets a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1b9d-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="e1b9d-108">Syntax</span></span>


```CSharp
public System.String uiMode {get; set;}
```


```VB

Public Property uiMode As System.String
```





## <a name="property-value"></a><span data-ttu-id="e1b9d-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="e1b9d-109">Property value</span></span>

<span data-ttu-id="e1b9d-110">Строка System. String, которая является одним из следующих значений.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-110">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="e1b9d-111">Значение</span><span class="sxs-lookup"><span data-stu-id="e1b9d-111">Value</span></span>     | <span data-ttu-id="e1b9d-112">Описание</span><span class="sxs-lookup"><span data-stu-id="e1b9d-112">Description</span></span>                                                                                                                                                                                                     | <span data-ttu-id="e1b9d-113">Пример звука</span><span class="sxs-lookup"><span data-stu-id="e1b9d-113">Audio example</span></span>                                                   | <span data-ttu-id="e1b9d-114">Пример видео</span><span class="sxs-lookup"><span data-stu-id="e1b9d-114">Video example</span></span>                                                   |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="e1b9d-115">невидимые</span><span class="sxs-lookup"><span data-stu-id="e1b9d-115">invisible</span></span> | <span data-ttu-id="e1b9d-116">Проигрыватель Windows Media внедряется без видимого пользовательского интерфейса (окна "элементы управления", "видео" или "Визуализация").</span><span class="sxs-lookup"><span data-stu-id="e1b9d-116">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                  | <span data-ttu-id="e1b9d-117">(Ничего не отображается.)</span><span class="sxs-lookup"><span data-stu-id="e1b9d-117">(Nothing is displayed.)</span></span>                                         | <span data-ttu-id="e1b9d-118">(Ничего не отображается.)</span><span class="sxs-lookup"><span data-stu-id="e1b9d-118">(Nothing is displayed.)</span></span>                                         |
| <span data-ttu-id="e1b9d-119">нет</span><span class="sxs-lookup"><span data-stu-id="e1b9d-119">none</span></span>      | <span data-ttu-id="e1b9d-120">Проигрыватель Windows Media внедряется без элементов управления и отображается только в окне видео или визуализация.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-120">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                   | ![UIMODE = "нет" с аудио](images/uimode-none-audio-v11.png) | ![UIMODE = "нет" с видео](images/uimode-none-video-v11.png) |
| <span data-ttu-id="e1b9d-123">Mini</span><span class="sxs-lookup"><span data-stu-id="e1b9d-123">mini</span></span>      | <span data-ttu-id="e1b9d-124">Проигрыватель Windows Media внедряется в окно состояния: воспроизведение/пауза, остановка, отключение звука, а также элементы управления громкостью, отображаемые в дополнение к окну видео или визуализации.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-124">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                    | ![UIMODE = ' Мини ' с аудио](images/uimode-mini-audio-v11.png) | ![UIMODE = ' Мини ' с видео](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="e1b9d-127">переполненные</span><span class="sxs-lookup"><span data-stu-id="e1b9d-127">full</span></span>      | <span data-ttu-id="e1b9d-128">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-128">Default.</span></span> <span data-ttu-id="e1b9d-129">Проигрыватель Windows Media внедряется в окно состояния, строку поиска, воспроизведение/пауза, остановить, выключить звук, далее, предыдущее, быстро перемотка вперед, назад и элементы управления громкостью в дополнение к окну видео или визуализации.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-129">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, rewind, and volume controls in addition to the video or visualization window.</span></span> | ![UIMODE = ' Full ' с аудио](images/uimode-full-audio-v11.png) | ![UIMODE = ' Full ' с видео](images/uimode-full-video-v11.png) |
| <span data-ttu-id="e1b9d-132">пользовательский</span><span class="sxs-lookup"><span data-stu-id="e1b9d-132">custom</span></span>    | <span data-ttu-id="e1b9d-133">Проигрыватель Windows Media внедряется с настраиваемым пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-133">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="e1b9d-134">Может использоваться только в программах на C++.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-134">Can only be used in C++ programs.</span></span>                                                                                                                | <span data-ttu-id="e1b9d-135">(Отображается настраиваемый пользовательский интерфейс.)</span><span class="sxs-lookup"><span data-stu-id="e1b9d-135">(Custom user interface is displayed.)</span></span>                           | <span data-ttu-id="e1b9d-136">(Отображается настраиваемый пользовательский интерфейс.)</span><span class="sxs-lookup"><span data-stu-id="e1b9d-136">(Custom user interface is displayed.)</span></span>                           |



 

## <a name="remarks"></a><span data-ttu-id="e1b9d-137">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e1b9d-137">Remarks</span></span>

<span data-ttu-id="e1b9d-138">Это свойство определяет внешний вид встроенного проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-138">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="e1b9d-139">Если для **uiMode** задано значение "нет", "Мини-" или "полная", то для отображения видеороликов и визуализаций звука имеется окно.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-139">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="e1b9d-140">Это окно можно скрыть в свернутом или полном режиме, установив атрибут **Height** тега **объекта** равным 40, который измеряется снизу, и оставляет часть элементов управления видимой.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-140">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="e1b9d-141">Если внедренный интерфейс не нужен, задайте для атрибутов **Width** и **Height** нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-141">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="e1b9d-142">Если для **uiMode** задано значение "Невидимый", Пользовательский интерфейс не отображается, но пространство на странице все еще зарезервировано, как указано **шириной** и **высотой**.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-142">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="e1b9d-143">Это полезно для того, чтобы хранить макет страницы, когда **uiMode** может измениться.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-143">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="e1b9d-144">Кроме того, зарезервированное пространство прозрачно, поэтому все элементы, расположенные позади элемента управления, будут видимы.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-144">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="e1b9d-145">Если для **uiMode** задано значение Full или Mini, проигрыватель Windows Media отображает элементы управления для передачи данных в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-145">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="e1b9d-146">Если для **uiMode** задано значение "нет", никакие элементы управления не отображаются в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-146">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="e1b9d-147">Если окно является видимым и воспроизводится звуковое содержимое, отображаемая визуализация будет использоваться в проигрывателе Windows Media Player недавно.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-147">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="e1b9d-148">Если для **uiMode** задано значение Custom в программе C++, которая реализует **ивмпремотемедиасервицес**, отображается файл обложки, указанный в **ивмпремотемедиасервицес. жеткустомуимоде** .</span><span class="sxs-lookup"><span data-stu-id="e1b9d-148">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices.GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="e1b9d-149">Во время воспроизведения в полноэкранном режиме проигрыватель Windows Media скрывает курсор мыши, когда **енаблеконтекстмену** равняется false, а **uiMode** равно «None».</span><span class="sxs-lookup"><span data-stu-id="e1b9d-149">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="e1b9d-150">Примеры</span><span class="sxs-lookup"><span data-stu-id="e1b9d-150">Examples</span></span>

<span data-ttu-id="e1b9d-151">В следующем примере создается список, позволяющий пользователю изменить режим пользовательского интерфейса для внедренного объекта проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-151">The following example creates a list box that allows the user to change the user interface mode for an embedded Windows Media Player object.</span></span> <span data-ttu-id="e1b9d-152">Объект Аксвмплиб. Аксвиндовсмедиаплайер представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-152">The AxWMPLib.AxWindowsMediaPlayer object is represented by the variable named player.</span></span>


```CSharp
// Load the list box with the four UI mode options.
uiModeOptions.Items.Add("invisible");
uiModeOptions.Items.Add("none");
uiModeOptions.Items.Add("mini");
uiModeOptions.Items.Add("full");


private void uiModeOptions_OnSelectedIndexChanged(object sender, System.EventArgs e)
{
    // Get the selected UI mode in the list box as a string.
    string newMode = (string)(((System.Windows.Forms.ListBox)sender).SelectedItem);
     
    // Set the UI mode that the user selected.
    player.uiMode = newMode;            
}
```


```VB

' Load the list box with the four UI mode options.
uiModeOptions.Items.Add(&quot;invisible&quot;)
uiModeOptions.Items.Add(&quot;none&quot;)
uiModeOptions.Items.Add(&quot;mini&quot;)
uiModeOptions.Items.Add(&quot;full&quot;)


Public Sub uiModeOptions_OnSelectedIndexChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles uiModeOptions.SelectedIndexChanged

    &#39; Get the selected UI mode in the list box as a string.
    Dim lb As System.Windows.Forms.ListBox = sender
    Dim newMode As String = lb.SelectedItem

    &#39; Set the UI mode that the user selected.
    player.uiMode = newMode

End Sub
```





## <a name="requirements"></a><span data-ttu-id="e1b9d-153">Требования</span><span class="sxs-lookup"><span data-stu-id="e1b9d-153">Requirements</span></span>



| <span data-ttu-id="e1b9d-154">Требование</span><span class="sxs-lookup"><span data-stu-id="e1b9d-154">Requirement</span></span> | <span data-ttu-id="e1b9d-155">Значение</span><span class="sxs-lookup"><span data-stu-id="e1b9d-155">Value</span></span> |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1b9d-156">Версия</span><span class="sxs-lookup"><span data-stu-id="e1b9d-156">Version</span></span><br/>   | <span data-ttu-id="e1b9d-157">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="e1b9d-157">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="e1b9d-158">Проигрыватель Windows Media 9 Series или более поздней версии для "невидимых" или "настраиваемых"</span><span class="sxs-lookup"><span data-stu-id="e1b9d-158">Windows Media Player 9 Series or later for "invisible" or "custom"</span></span><br/>   |
| <span data-ttu-id="e1b9d-159">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="e1b9d-159">Namespace</span></span><br/> | <span data-ttu-id="e1b9d-160">**аксвмплиб**</span><span class="sxs-lookup"><span data-stu-id="e1b9d-160">**AxWMPLib**</span></span><br/>                                                                                                    |
| <span data-ttu-id="e1b9d-161">Сборка</span><span class="sxs-lookup"><span data-stu-id="e1b9d-161">Assembly</span></span><br/>  | <dl> <span data-ttu-id="e1b9d-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="e1b9d-162"><dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1b9d-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e1b9d-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1b9d-164">**Объект Аксвиндовсмедиаплайер (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e1b9d-164">**AxWindowsMediaPlayer Object (VB and C#)**</span></span>](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="e1b9d-165">**Аксвиндовсмедиаплайер. Енаблеконтекстмену (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="e1b9d-165">**AxWindowsMediaPlayer.enableContextMenu (VB and C#)**</span></span>](axwmplib-axwindowsmediaplayer-enablecontextmenu--vb-and-c.md)
</dt> </dl>

 

 





