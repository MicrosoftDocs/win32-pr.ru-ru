---
title: Свойство Ивмпсеттингс Rate
description: Свойство Rate Возвращает или задает текущую скорость воспроизведения видео.
ms.assetid: 7baa667b-52e5-4419-8e12-c3627a417b20
keywords:
- Проигрыватель Windows Media для свойства Rate
- свойство "частота" проигрывателя Windows Media Player, интерфейс Ивмпсеттингс
- Интерфейс Ивмпсеттингс Windows Media Player, свойство Rate
topic_type:
- apiref
api_name:
- IWMPSettings.rate
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f502bebdbd22523858637f8abccbe203db104cbe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105717847"
---
# <a name="iwmpsettingsrate-property"></a><span data-ttu-id="d96c8-106">Свойство Ивмпсеттингс:: Rate</span><span class="sxs-lookup"><span data-stu-id="d96c8-106">IWMPSettings::rate property</span></span>

<span data-ttu-id="d96c8-107">Свойство **Rate** Возвращает или задает текущую скорость воспроизведения видео.</span><span class="sxs-lookup"><span data-stu-id="d96c8-107">The **rate** property gets or sets the current playback rate for video.</span></span>

## <a name="syntax"></a><span data-ttu-id="d96c8-108">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="d96c8-108">Syntax</span></span>


```CSharp
public System.Double rate {get; set;}
```


```VB

Public Property rate As System.Double
```





## <a name="property-value"></a><span data-ttu-id="d96c8-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="d96c8-109">Property value</span></span>

<span data-ttu-id="d96c8-110">Значение **System. Double** , которое является скоростью воспроизведения и значением по умолчанию 1,0.</span><span class="sxs-lookup"><span data-stu-id="d96c8-110">A **System.Double** that is the playback rate, with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="d96c8-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d96c8-111">Remarks</span></span>

<span data-ttu-id="d96c8-112">Значение, полученное этим свойством, выступает в качестве значения множителя, которое позволяет воспроизводить элемент мультимедиа с более высокой или низкой скоростью.</span><span class="sxs-lookup"><span data-stu-id="d96c8-112">The value retrieved by this property acts as a multiplier value that enables you to play a media item at a faster or slower rate.</span></span> <span data-ttu-id="d96c8-113">Значение по умолчанию 1,0 указывает на созданную скорость.</span><span class="sxs-lookup"><span data-stu-id="d96c8-113">The default value of 1.0 indicates the authored speed.</span></span>

<span data-ttu-id="d96c8-114">Обратите внимание, что звуковая дорожка будет трудной для понимания на скорости ниже 0,5 или выше 1,5.</span><span class="sxs-lookup"><span data-stu-id="d96c8-114">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="d96c8-115">Скорость воспроизведения 2 означает удвоенную нормальную скорость воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d96c8-115">A playback rate of 2 indicates twice the normal playback speed.</span></span>

<span data-ttu-id="d96c8-116">Проигрыватель Windows Media попытается использовать наиболее эффективный из следующих четырех режимов воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d96c8-116">Windows Media Player will attempt to use the most effective of the following four different playback modes</span></span>

-   <span data-ttu-id="d96c8-117">Плавное воспроизведение видео с пошаговым сопровождением</span><span class="sxs-lookup"><span data-stu-id="d96c8-117">Smooth video playback with audio pitch maintained</span></span>
-   <span data-ttu-id="d96c8-118">Плавное воспроизведение видео с пошаговой звука не поддерживается</span><span class="sxs-lookup"><span data-stu-id="d96c8-118">Smooth video playback with audio pitch not maintained</span></span>
-   <span data-ttu-id="d96c8-119">Плавное воспроизведение видео без звука</span><span class="sxs-lookup"><span data-stu-id="d96c8-119">Smooth video playback with no audio</span></span>
-   <span data-ttu-id="d96c8-120">Воспроизведение видео опорного кадра без звука</span><span class="sxs-lookup"><span data-stu-id="d96c8-120">Keyframe video playback with no audio</span></span>

<span data-ttu-id="d96c8-121">Режим, выбранный проигрывателем Windows Media, зависит от множества факторов, включая тип файла и расположение, операционную систему, сеть и сервер.</span><span class="sxs-lookup"><span data-stu-id="d96c8-121">The mode chosen by Windows Media Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="d96c8-122">Кроме того, в зависимости от формата цифрового мультимедиа, используемого для создания содержимого, также применяются и другие соображения.</span><span class="sxs-lookup"><span data-stu-id="d96c8-122">Other considerations apply as well, depending on the digital media format used to create the content:</span></span>

-   <span data-ttu-id="d96c8-123">**Windows Media Video (WMV) и ASF.**</span><span class="sxs-lookup"><span data-stu-id="d96c8-123">**Windows Media Video (WMV) and ASF.**</span></span> <span data-ttu-id="d96c8-124">Оптимальные значения для свойства **Rate** : от 1 до 10 или от 1 до 10 для обратного воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d96c8-124">Optimal values for the **rate** property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="d96c8-125">Значения от 0,5 до 1,0 или от-0,5 до-1,0 могут также работать в случаях, когда может поддерживаться тон звука, например при воспроизведении файлов, расположенных на локальном компьютере.</span><span class="sxs-lookup"><span data-stu-id="d96c8-125">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, such as when playing files located on the local computer.</span></span> <span data-ttu-id="d96c8-126">Значения с абсолютной величиной больше 10 допускаются, но не очень важны.</span><span class="sxs-lookup"><span data-stu-id="d96c8-126">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="d96c8-127">**Другие форматы видео.**</span><span class="sxs-lookup"><span data-stu-id="d96c8-127">**Other video formats.**</span></span> <span data-ttu-id="d96c8-128">Свойство **Rate** может принимать значения от 0 до 9.</span><span class="sxs-lookup"><span data-stu-id="d96c8-128">The **rate** property can range from 0 to 9.</span></span> <span data-ttu-id="d96c8-129">Отрицательные значения не допускаются.</span><span class="sxs-lookup"><span data-stu-id="d96c8-129">Negative values are not allowed.</span></span> <span data-ttu-id="d96c8-130">Значения меньше 1 представляют медленное движение.</span><span class="sxs-lookup"><span data-stu-id="d96c8-130">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="d96c8-131">Значения, указанные выше 9, разрешены, но не очень важны.</span><span class="sxs-lookup"><span data-stu-id="d96c8-131">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="d96c8-132">Метод **ивмпконтролс. фастфорвард** изменяет значение **Rate** на 5,0, а метод **ивмпконтролс. фастреверсе** изменяет значение **Rate** на 5,0.</span><span class="sxs-lookup"><span data-stu-id="d96c8-132">The **IWMPControls.fastForward** method changes the value of **rate** to 5.0, while the **IWMPControls.fastReverse** method changes the value of **rate** to  5.0.</span></span>

<span data-ttu-id="d96c8-133">Скорость воспроизведения некоторых форматов мультимедиа не может быть изменена.</span><span class="sxs-lookup"><span data-stu-id="d96c8-133">The playback rate of some digital media formats cannot be altered.</span></span> <span data-ttu-id="d96c8-134">Используйте свойство **ивмпсеттингс.** Ивмпсеттингс (в C# метод **. Get- \_ Available** ), чтобы определить, можно ли указать это свойство для конкретного элемента мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="d96c8-134">Use the **IWMPSettings.isAvailable** property (In C# the **IWMPSettings.get\_isAvailable** method) to discover whether this property can be specified for a particular media item.</span></span>

## <a name="examples"></a><span data-ttu-id="d96c8-135">Примеры</span><span class="sxs-lookup"><span data-stu-id="d96c8-135">Examples</span></span>

<span data-ttu-id="d96c8-136">В следующем примере используется числовой элемент управления, который позволяет пользователю изменить скорость воспроизведения текущего носителя.</span><span class="sxs-lookup"><span data-stu-id="d96c8-136">The following example uses a numeric updown control that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="d96c8-137">Когда пользователь нажимает стрелки вверх или вниз элемента управления, свойству **Rate** присваивается новое значение.</span><span class="sxs-lookup"><span data-stu-id="d96c8-137">When the user clicks the up or down arrows of the control, the **rate** property is set to the new value.</span></span> <span data-ttu-id="d96c8-138">Возможный диапазон значений в элементе управления — 0,5 (половинная скорость) 2,0 (двойная скорость).</span><span class="sxs-lookup"><span data-stu-id="d96c8-138">The possible range of values in the control are 0.5 (half-speed) to 2.0 (double-speed).</span></span> <span data-ttu-id="d96c8-139">Объект **аксвмплиб. аксвиндовсмедиаплайер** представлен переменной с именем Player.</span><span class="sxs-lookup"><span data-stu-id="d96c8-139">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void playbackRate_Click(object sender, System.EventArgs e)
{
    // Get the new value of the control, and cast it from decimal to double.
    double newRate = (double)((System.Windows.Forms.NumericUpDown)sender).Value;

    // Test whether playback rate can be set. 
    if( player.settings.get_isAvailable("Rate") )
    {
        // Set the playback rate to the new value.
        player.settings.rate = newRate;
    }
}
```


```VB

Public Sub playbackRate_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles playbackRate.Click

    &#39;  Get the new value of the control as a double.
    Dim nUpDown As System.Windows.Forms.NumericUpDown = sender
    Dim newRate As Double = nUpDown.Value

    &#39;  Test whether playback rate can be set. 
    If (player.settings.isAvailable(&quot;Rate&quot;)) Then

        &#39;  Set the playback rate to the new value.
        player.settings.rate = newRate

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="d96c8-140">Требования</span><span class="sxs-lookup"><span data-stu-id="d96c8-140">Requirements</span></span>



| <span data-ttu-id="d96c8-141">Требование</span><span class="sxs-lookup"><span data-stu-id="d96c8-141">Requirement</span></span> | <span data-ttu-id="d96c8-142">Значение</span><span class="sxs-lookup"><span data-stu-id="d96c8-142">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d96c8-143">Версия</span><span class="sxs-lookup"><span data-stu-id="d96c8-143">Version</span></span><br/>   | <span data-ttu-id="d96c8-144">Проигрыватель Windows Media 9 Series или более поздней версии</span><span class="sxs-lookup"><span data-stu-id="d96c8-144">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="d96c8-145">Пространство имен</span><span class="sxs-lookup"><span data-stu-id="d96c8-145">Namespace</span></span><br/> | <span data-ttu-id="d96c8-146">**вмплиб**</span><span class="sxs-lookup"><span data-stu-id="d96c8-146">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="d96c8-147">Сборка</span><span class="sxs-lookup"><span data-stu-id="d96c8-147">Assembly</span></span><br/>  | <dl> <span data-ttu-id="d96c8-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="d96c8-148"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d96c8-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d96c8-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d96c8-150">**Ивмпконтролс. Фастфорвард (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d96c8-150">**IWMPControls.fastForward (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastforward--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d96c8-151">**Ивмпконтролс. Фастреверсе (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d96c8-151">**IWMPControls.fastReverse (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-fastreverse--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d96c8-152">**Интерфейс Ивмпсеттингс (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d96c8-152">**IWMPSettings Interface (VB and C#)**</span></span>](iwmpsettings--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d96c8-153">**Ивмпсеттингс. доступ (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d96c8-153">**IWMPSettings.isAvailable (VB and C#)**</span></span>](iwmpsettings-isavailable--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="d96c8-154">**Ивмпсеттингс. выкл. (VB и C#)**</span><span class="sxs-lookup"><span data-stu-id="d96c8-154">**IWMPSettings.mute (VB and C#)**</span></span>](wmplibiwmpsettings-iwmpsettings-mute--vb-and-c.md)
</dt> </dl>

 

 





