---
title: Player. uiMode
description: Свойство uiMode указывает или получает значение, указывающее, какие элементы управления отображаются в пользовательском интерфейсе.
ms.assetid: 6297d22b-e8ed-4f28-83f6-b74d3265c520
keywords:
- Проигрыватель проигрывателя Windows Media Player. uiMode
topic_type:
- apiref
api_name:
- Player.uiMode
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b1fd2e8e3a2ac6314255cd6ebc350b2ace8cb63
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105704343"
---
# <a name="playeruimode"></a><span data-ttu-id="bcb27-104">Player. uiMode</span><span class="sxs-lookup"><span data-stu-id="bcb27-104">Player.uiMode</span></span>

<span data-ttu-id="bcb27-105">Свойство **uiMode** указывает или получает значение, указывающее, какие элементы управления отображаются в пользовательском интерфейсе.</span><span class="sxs-lookup"><span data-stu-id="bcb27-105">The **uiMode** property specifies or retrieves a value indicating which controls are shown in the user interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcb27-106">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="bcb27-106">Syntax</span></span>

<span data-ttu-id="bcb27-107">*проигрыватель* . **uiMode**</span><span class="sxs-lookup"><span data-stu-id="bcb27-107">*player* .**uiMode**</span></span>

## <a name="possible-values"></a><span data-ttu-id="bcb27-108">Возможные значения</span><span class="sxs-lookup"><span data-stu-id="bcb27-108">Possible Values</span></span>

<span data-ttu-id="bcb27-109">Это свойство является **строкой** для чтения и записи.</span><span class="sxs-lookup"><span data-stu-id="bcb27-109">This property is a read/write **String**.</span></span>



| <span data-ttu-id="bcb27-110">Значение</span><span class="sxs-lookup"><span data-stu-id="bcb27-110">Value</span></span>     | <span data-ttu-id="bcb27-111">Описание</span><span class="sxs-lookup"><span data-stu-id="bcb27-111">Description</span></span>                                                                                                                                                                                                           | <span data-ttu-id="bcb27-112">Пример звука</span><span class="sxs-lookup"><span data-stu-id="bcb27-112">Audio Example</span></span>                                          | <span data-ttu-id="bcb27-113">Пример видео</span><span class="sxs-lookup"><span data-stu-id="bcb27-113">Video Example</span></span>                                          |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|--------------------------------------------------------|
| <span data-ttu-id="bcb27-114">невидимые</span><span class="sxs-lookup"><span data-stu-id="bcb27-114">invisible</span></span> | <span data-ttu-id="bcb27-115">Проигрыватель Windows Media внедряется без видимого пользовательского интерфейса (окна "элементы управления", "видео" или "Визуализация").</span><span class="sxs-lookup"><span data-stu-id="bcb27-115">Windows Media Player is embedded without any visible user interface (controls, video or visualization window).</span></span>                                                                                                        | <span data-ttu-id="bcb27-116">(Ничего не отображается.)</span><span class="sxs-lookup"><span data-stu-id="bcb27-116">(Nothing is displayed.)</span></span>                                | <span data-ttu-id="bcb27-117">(Ничего не отображается.)</span><span class="sxs-lookup"><span data-stu-id="bcb27-117">(Nothing is displayed.)</span></span>                                |
| <span data-ttu-id="bcb27-118">нет</span><span class="sxs-lookup"><span data-stu-id="bcb27-118">none</span></span>      | <span data-ttu-id="bcb27-119">Проигрыватель Windows Media внедряется без элементов управления и отображается только в окне видео или визуализация.</span><span class="sxs-lookup"><span data-stu-id="bcb27-119">Windows Media Player is embedded without controls, and with only the video or visualization window displayed.</span></span>                                                                                                         | !["нет" с аудио](images/uimode-none-audio-v11.png) | !["нет" с видео](images/uimode-none-video-v11.png) |
| <span data-ttu-id="bcb27-122">Mini</span><span class="sxs-lookup"><span data-stu-id="bcb27-122">mini</span></span>      | <span data-ttu-id="bcb27-123">Проигрыватель Windows Media внедряется в окно состояния: воспроизведение/пауза, остановка, отключение звука, а также элементы управления громкостью, отображаемые в дополнение к окну видео или визуализации.</span><span class="sxs-lookup"><span data-stu-id="bcb27-123">Windows Media Player is embedded with the status window, play/pause, stop, mute, and volume controls shown in addition to the video or visualization window.</span></span>                                                          | !["Мини" с аудио](images/uimode-mini-audio-v11.png) | !["Мини" с видео](images/uimode-mini-video-v11.png) |
| <span data-ttu-id="bcb27-126">переполненные</span><span class="sxs-lookup"><span data-stu-id="bcb27-126">full</span></span>      | <span data-ttu-id="bcb27-127">По умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bcb27-127">Default.</span></span> <span data-ttu-id="bcb27-128">Проигрыватель Windows Media внедряется с окном состояния, панелью поиска, воспроизведением, паузой, остановкой, микрофоном, следующим, предыдущим, быстрым пересылкой, быстрым обратным вызовом и элементами управления громкостью в дополнение к окну видео или визуализации.</span><span class="sxs-lookup"><span data-stu-id="bcb27-128">Windows Media Player is embedded with the status window, seek bar, play/pause, stop, mute, next, previous, fast forward, fast reverse, and volume controls in addition to the video or visualization window.</span></span> | !["Full" с аудио](images/uimode-full-audio-v11.png) | !["полная" с видео](images/uimode-full-video-v11.png) |
| <span data-ttu-id="bcb27-131">пользовательский</span><span class="sxs-lookup"><span data-stu-id="bcb27-131">custom</span></span>    | <span data-ttu-id="bcb27-132">Проигрыватель Windows Media внедряется с настраиваемым пользовательским интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="bcb27-132">Windows Media Player is embedded with a custom user interface.</span></span> <span data-ttu-id="bcb27-133">Может использоваться только в программах на C++.</span><span class="sxs-lookup"><span data-stu-id="bcb27-133">Can only be used in C++ programs.</span></span>                                                                                                                      | <span data-ttu-id="bcb27-134">(Отображается настраиваемый пользовательский интерфейс.)</span><span class="sxs-lookup"><span data-stu-id="bcb27-134">(Custom user interface is displayed.)</span></span>                  | <span data-ttu-id="bcb27-135">(Отображается настраиваемый пользовательский интерфейс.)</span><span class="sxs-lookup"><span data-stu-id="bcb27-135">(Custom user interface is displayed.)</span></span>                  |



 

## <a name="remarks"></a><span data-ttu-id="bcb27-136">Комментарии</span><span class="sxs-lookup"><span data-stu-id="bcb27-136">Remarks</span></span>

<span data-ttu-id="bcb27-137">Это свойство определяет внешний вид встроенного проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="bcb27-137">This property specifies the appearance of the embedded Windows Media Player.</span></span> <span data-ttu-id="bcb27-138">Если для **uiMode** задано значение "нет", "Мини-" или "полная", то для отображения видеороликов и визуализаций звука имеется окно.</span><span class="sxs-lookup"><span data-stu-id="bcb27-138">When **uiMode** is set to "none", "mini", or "full", a window is present for the display of video clips and audio visualizations.</span></span> <span data-ttu-id="bcb27-139">Это окно можно скрыть в свернутом или полном режиме, установив атрибут **Height** тега **объекта** равным 40, который измеряется снизу, и оставляет часть элементов управления видимой.</span><span class="sxs-lookup"><span data-stu-id="bcb27-139">This window can be hidden in mini or full mode by setting the **height** attribute of the **OBJECT** tag to 40, which is measured from the bottom, and leaves the controls portion of the user interface visible.</span></span> <span data-ttu-id="bcb27-140">Если внедренный интерфейс не нужен, задайте для атрибутов **Width** и **Height** нулевое значение.</span><span class="sxs-lookup"><span data-stu-id="bcb27-140">If no embedded interface is desired, set both the **width** and **height** attributes to zero.</span></span>

<span data-ttu-id="bcb27-141">Если для **uiMode** задано значение "Невидимый", Пользовательский интерфейс не отображается, но пространство на странице все еще зарезервировано, как указано **шириной** и **высотой**.</span><span class="sxs-lookup"><span data-stu-id="bcb27-141">If **uiMode** is set to "invisible", no user interface is displayed, but space is still reserved on the page as specified by **width** and **height**.</span></span> <span data-ttu-id="bcb27-142">Это полезно для того, чтобы хранить макет страницы, когда **uiMode** может измениться.</span><span class="sxs-lookup"><span data-stu-id="bcb27-142">This is useful for retaining page layout when **uiMode** can change.</span></span> <span data-ttu-id="bcb27-143">Кроме того, зарезервированное пространство прозрачно, поэтому все элементы, расположенные позади элемента управления, будут видимы.</span><span class="sxs-lookup"><span data-stu-id="bcb27-143">Additionally, the reserved space is transparent, so any elements layered behind the control will be visible.</span></span>

<span data-ttu-id="bcb27-144">Если для **uiMode** задано значение Full или Mini, проигрыватель Windows Media отображает элементы управления для передачи данных в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="bcb27-144">If **uiMode** is set to "full" or "mini", Windows Media Player displays transport controls in full-screen mode.</span></span> <span data-ttu-id="bcb27-145">Если для **uiMode** задано значение "нет", никакие элементы управления не отображаются в полноэкранном режиме.</span><span class="sxs-lookup"><span data-stu-id="bcb27-145">If **uiMode** is set to "none", no controls are displayed in full-screen mode.</span></span>

<span data-ttu-id="bcb27-146">Если окно является видимым и воспроизводится звуковое содержимое, отображаемая визуализация будет использоваться в проигрывателе Windows Media Player недавно.</span><span class="sxs-lookup"><span data-stu-id="bcb27-146">If the window is visible and audio content is being played, the visualization displayed will be the one most recently used in Windows Media Player.</span></span>

<span data-ttu-id="bcb27-147">Если для **uiMode** задано значение "Custom" в программе C++, которая реализует **ивмпремотемедиасервицес**, отображается файл обложки, указанный в **ивмпремотемедиасервицес:: жеткустомуимоде** .</span><span class="sxs-lookup"><span data-stu-id="bcb27-147">If **uiMode** is set to "custom" in a C++ program that implements **IWMPRemoteMediaServices**, the skin file indicated by **IWMPRemoteMediaServices::GetCustomUIMode** is displayed.</span></span>

<span data-ttu-id="bcb27-148">Во время воспроизведения в полноэкранном режиме проигрыватель Windows Media скрывает курсор мыши, когда **енаблеконтекстмену** равняется false, а **uiMode** равно «None».</span><span class="sxs-lookup"><span data-stu-id="bcb27-148">During full-screen playback, Windows Media Player hides the mouse cursor when **enableContextMenu** equals false and **uiMode** equals "none".</span></span>

## <a name="examples"></a><span data-ttu-id="bcb27-149">Примеры</span><span class="sxs-lookup"><span data-stu-id="bcb27-149">Examples</span></span>

<span data-ttu-id="bcb27-150">В следующем примере создается HTML-элемент SELECT, который позволяет пользователю изменить пользовательский интерфейс для внедренного объекта **Player** .</span><span class="sxs-lookup"><span data-stu-id="bcb27-150">The following example creates an HTML SELECT element that allows the user to change the user interface for an embedded **Player** object.</span></span> <span data-ttu-id="bcb27-151">Объект **Player** создан с идентификатором "Player".</span><span class="sxs-lookup"><span data-stu-id="bcb27-151">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create an HTML SELECT element. -->
<SELECT  ID = UI  LANGUAGE="JScript"

         /* Specify the UI mode the user selects. */
         onChange = "Player.uiMode = UI.value">

/* These are the four UI mode options. */
<OPTION VALUE="invisible">Invisible
<OPTION VALUE="none">No Controls
<OPTION VALUE="mini">Mini Player
<OPTION VALUE="full">Full Player
</SELECT>

```



<span data-ttu-id="bcb27-152">Проигрыватель Windows Media 10 Mobile: это свойство принимает или возвращает значения "None" или "Full".</span><span class="sxs-lookup"><span data-stu-id="bcb27-152">Windows Media Player 10 Mobile: This property only accepts or returns values of "none" or "full".</span></span> <span data-ttu-id="bcb27-153">На смартфонах устройства отображается только состояние воспроизведения и счетчик, если для *uiMode* задано значение Full.</span><span class="sxs-lookup"><span data-stu-id="bcb27-153">On Smartphone devices, only playback status and a counter are displayed when *uiMode* is set to "full".</span></span>

## <a name="requirements"></a><span data-ttu-id="bcb27-154">Требования</span><span class="sxs-lookup"><span data-stu-id="bcb27-154">Requirements</span></span>



| <span data-ttu-id="bcb27-155">Требование</span><span class="sxs-lookup"><span data-stu-id="bcb27-155">Requirement</span></span> | <span data-ttu-id="bcb27-156">Значение</span><span class="sxs-lookup"><span data-stu-id="bcb27-156">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcb27-157">Версия</span><span class="sxs-lookup"><span data-stu-id="bcb27-157">Version</span></span><br/> | <span data-ttu-id="bcb27-158">Проигрыватель Windows Media версии 7,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="bcb27-158">Windows Media Player version 7.0 or later.</span></span> <span data-ttu-id="bcb27-159">Проигрыватель Windows Media 9 Series или более поздней версии для «невидимых» или «пользовательских».</span><span class="sxs-lookup"><span data-stu-id="bcb27-159">Windows Media Player 9 Series or later for "invisible" or "custom".</span></span><br/> |
| <span data-ttu-id="bcb27-160">DLL</span><span class="sxs-lookup"><span data-stu-id="bcb27-160">DLL</span></span><br/>     | <dl> <span data-ttu-id="bcb27-161"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bcb27-161"><dt>Wmp.dll</dt></span></span> </dl>                                        |



## <a name="see-also"></a><span data-ttu-id="bcb27-162">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="bcb27-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcb27-163">**Интерфейс Ивмпремотемедиасервицес**</span><span class="sxs-lookup"><span data-stu-id="bcb27-163">**IWMPRemoteMediaServices Interface**</span></span>](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices)
</dt> <dt>

[<span data-ttu-id="bcb27-164">**Ивмпремотемедиасервицес:: Жеткустомуимоде**</span><span class="sxs-lookup"><span data-stu-id="bcb27-164">**IWMPRemoteMediaServices::GetCustomUIMode**</span></span>](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getcustomuimode)
</dt> <dt>

[<span data-ttu-id="bcb27-165">**Объект Player**</span><span class="sxs-lookup"><span data-stu-id="bcb27-165">**Player Object**</span></span>](player-object.md)
</dt> </dl>

 

 





