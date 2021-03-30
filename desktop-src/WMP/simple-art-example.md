---
title: Пример простой иллюстрации
description: Пример простой иллюстрации
ms.assetid: e17c29c3-3bc6-43f5-83e1-94005218417f
keywords:
- Обложки проигрывателя Windows Media, графические файлы
- обложки, файлы Art
- файлы для обложек, изображений
- графические файлы для обложек, примеры
- Обложки проигрывателя Windows Media, примеры
- обложки, примеры
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cab7b25dc33da70a627f8b0e126d6797b1bcdd9f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103775545"
---
# <a name="simple-art-example"></a><span data-ttu-id="dc367-109">Пример простой иллюстрации</span><span class="sxs-lookup"><span data-stu-id="dc367-109">Simple Art Example</span></span>

<span data-ttu-id="dc367-110">Для создания простой обложки с двумя кнопками необходимы три рисунка.</span><span class="sxs-lookup"><span data-stu-id="dc367-110">Three art files are needed to create a simple skin with two buttons.</span></span> <span data-ttu-id="dc367-111">Требуется основной образ и изображение сопоставления, а альтернативное изображение предоставляет пользователю визуальную подсказку о том, что кнопка может быть нажата.</span><span class="sxs-lookup"><span data-stu-id="dc367-111">A primary image and a mapping image are required, and an alternate image provides a visual cue to the user that a button is clickable.</span></span>

<span data-ttu-id="dc367-112">Эти графические файлы были созданы в художественной программе, использующей слои.</span><span class="sxs-lookup"><span data-stu-id="dc367-112">These art files were created in an art program that uses layers.</span></span> <span data-ttu-id="dc367-113">Использование слоев упрощает обеспечение того, что основной, сопоставленный и альтернативный изображения имеют одинаковый размер и построчно.</span><span class="sxs-lookup"><span data-stu-id="dc367-113">Using layers makes it easier to make sure that your primary, mapping, and alternate images are all the same size and line up with each other.</span></span>

<span data-ttu-id="dc367-114">Подробные инструкции по созданию картинок см. в статье [Создание обложки](skin-creation-guide.md).</span><span class="sxs-lookup"><span data-stu-id="dc367-114">The detailed instructions on creating the art are in the [Skin Creation Guide](skin-creation-guide.md).</span></span>

## <a name="primary-image"></a><span data-ttu-id="dc367-115">Основной образ</span><span class="sxs-lookup"><span data-stu-id="dc367-115">Primary Image</span></span>

<span data-ttu-id="dc367-116">Основной образ — это простой желтый овал с двумя кнопками, розовый один для запуска проигрывателя Windows Media и фиолетовая кнопка для ее отмены.</span><span class="sxs-lookup"><span data-stu-id="dc367-116">The primary image is a simple yellow oval with two buttons, a pink one to start Windows Media Player and purple button to stop it.</span></span> <span data-ttu-id="dc367-117">Фон немного темнее, чем овал.</span><span class="sxs-lookup"><span data-stu-id="dc367-117">The background is a slightly darker yellow than the oval.</span></span> <span data-ttu-id="dc367-118">Это изображение показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="dc367-118">This image is shown in the following illustration.</span></span>

![основной образ](images/absam01b.png)

<span data-ttu-id="dc367-120">Основной образ находился на следующих изображениях, каждый в отдельном слое.</span><span class="sxs-lookup"><span data-stu-id="dc367-120">The primary image was from the following images, each in a separate layer.</span></span> <span data-ttu-id="dc367-121">Первый овал был создан с эффектом выпуклости и рельефности слоя.</span><span class="sxs-lookup"><span data-stu-id="dc367-121">First an oval was created with a layer bevel and emboss effect.</span></span> <span data-ttu-id="dc367-122">Это изображение показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="dc367-122">This image is shown in the following illustration.</span></span>

![изображение овала](images/absam01s.png)

<span data-ttu-id="dc367-124">Затем создаются две кнопки, а также эффекты рельефа и рельефа слоя.</span><span class="sxs-lookup"><span data-stu-id="dc367-124">Then the two buttons were created, also with layer bevel and emboss effects.</span></span> <span data-ttu-id="dc367-125">Это показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="dc367-125">This is shown in the following illustration.</span></span>

![две кнопки](images/absam01p.png)

<span data-ttu-id="dc367-127">После создания фона изображения.</span><span class="sxs-lookup"><span data-stu-id="dc367-127">Next the image background was created.</span></span> <span data-ttu-id="dc367-128">Был выбран немного более темный желтый цвет, чтобы не было замечено сглаживание между овалом и фоном.</span><span class="sxs-lookup"><span data-stu-id="dc367-128">A slightly darker yellow was chosen so that any anti-aliasing between the oval and the background will not be noticed.</span></span> <span data-ttu-id="dc367-129">Значение цвета — \# CCCC00.</span><span class="sxs-lookup"><span data-stu-id="dc367-129">The color value is \#CCCC00.</span></span> <span data-ttu-id="dc367-130">Это изображение показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="dc367-130">This image is shown in the following illustration.</span></span>

![фоновое изображение](images/absam01y.png)

<span data-ttu-id="dc367-132">Слои, содержащие эти изображения, были сделаны видимыми и сохранены в виде копии в растровом формате, создавая первичный образ.</span><span class="sxs-lookup"><span data-stu-id="dc367-132">The layers that contained these images were made visible and saved as a copy in bitmap format, creating the primary image.</span></span> <span data-ttu-id="dc367-133">Основной составной образ будет использоваться атрибутом **backgroundImage** элемента **View** .</span><span class="sxs-lookup"><span data-stu-id="dc367-133">The primary composite image will be used by the **backgroundImage** attribute of the **VIEW** element.</span></span>

## <a name="mapping-image"></a><span data-ttu-id="dc367-134">Изображение сопоставления</span><span class="sxs-lookup"><span data-stu-id="dc367-134">Mapping Image</span></span>

<span data-ttu-id="dc367-135">Изображение сопоставления необходимо для указания времени и места щелчка обложки.</span><span class="sxs-lookup"><span data-stu-id="dc367-135">A mapping image is needed to specify when and where a skin is clicked.</span></span> <span data-ttu-id="dc367-136">Изображение сопоставления было создано с красной областью и зеленой областью.</span><span class="sxs-lookup"><span data-stu-id="dc367-136">A mapping image was created with a red area and a green area.</span></span> <span data-ttu-id="dc367-137">Это изображение показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="dc367-137">This image is shown in the following illustration.</span></span>

![изображение сопоставления](images/absam01m.png)

<span data-ttu-id="dc367-139">Зеленая область будет использоваться для задания области обложки, которая запускает проигрыватель Windows Media, и будет использоваться красная область для ее отмены.</span><span class="sxs-lookup"><span data-stu-id="dc367-139">The green area will be used to identify the area on the skin that will start Windows Media Player and the red area will be used to stop it.</span></span> <span data-ttu-id="dc367-140">Изображение сопоставления имеет тот же размер, что и основной образ.</span><span class="sxs-lookup"><span data-stu-id="dc367-140">The mapping image is the same size as the primary image.</span></span>

<span data-ttu-id="dc367-141">Изображение сопоставления было создано путем копирования слоя кнопок в новый слой и отключения эффекта рельефа и рельефа.</span><span class="sxs-lookup"><span data-stu-id="dc367-141">The mapping image was created by copying the button layer to a new layer and turning off the bevel and emboss effect.</span></span> <span data-ttu-id="dc367-142">Для сопоставления требуются плоские образы, так как проигрыватель Windows Media ищет в каждой области отдельные значения цвета.</span><span class="sxs-lookup"><span data-stu-id="dc367-142">Flat images are needed for mapping because Windows Media Player will be looking for single color values in each area.</span></span> <span data-ttu-id="dc367-143">Он может искать только определенный цвет, например красный ( \# FF0000).</span><span class="sxs-lookup"><span data-stu-id="dc367-143">It can only search for a color you define, such as red (\#FF0000).</span></span> <span data-ttu-id="dc367-144">Если изображение имеет багетную рамку или другой результат, не все из них будут полностью красными.</span><span class="sxs-lookup"><span data-stu-id="dc367-144">If your image has a bevel or other effect, not all of it will be the exact red you need.</span></span>

<span data-ttu-id="dc367-145">Чтобы запомнить кнопки сопоставления, изображения были заполнены красным и зеленым цветом, но можно использовать любой цвет.</span><span class="sxs-lookup"><span data-stu-id="dc367-145">To make the mapping buttons an easy color to remember, the images were filled with pure red and pure green, but any color can be used.</span></span> <span data-ttu-id="dc367-146">Необходимо запомнить цветовые номера на карте, чтобы их можно было указать в файле определения обложки XML.</span><span class="sxs-lookup"><span data-stu-id="dc367-146">You will need to remember the color numbers in your map so that they can be entered in the XML skin definition file.</span></span> <span data-ttu-id="dc367-147">В этом случае красный цвет — \# FF0000, а зеленый — \# 00FF00.</span><span class="sxs-lookup"><span data-stu-id="dc367-147">In this case, red is \#FF0000 and green is \#00FF00.</span></span>

<span data-ttu-id="dc367-148">Затем, если виден только новый слой, образ был сохранен как копия в файл BMP.</span><span class="sxs-lookup"><span data-stu-id="dc367-148">Then, with only the new layer visible, the image was saved as a copy to a BMP file.</span></span> <span data-ttu-id="dc367-149">Он будет вызываться атрибутом **маппингимаже** элемента **BUTTONGROUP** .</span><span class="sxs-lookup"><span data-stu-id="dc367-149">It will be called by the **mappingImage** attribute of the **BUTTONGROUP** element.</span></span>

## <a name="alternate-image"></a><span data-ttu-id="dc367-150">Альтернативное изображение</span><span class="sxs-lookup"><span data-stu-id="dc367-150">Alternate Image</span></span>

<span data-ttu-id="dc367-151">Альтернативные образы не требуются, но очень полезны для предоставления пользователю визуальных подсказок.</span><span class="sxs-lookup"><span data-stu-id="dc367-151">Alternate images are not required but are very useful to give visual cues to the user.</span></span> <span data-ttu-id="dc367-152">В этом случае рекомендуется использовать изображение для наведения, чтобы пользователь знал, на какие области можно щелкнуть.</span><span class="sxs-lookup"><span data-stu-id="dc367-152">In this case, a hover image is recommended so that the user knows what areas can be clicked on.</span></span>

<span data-ttu-id="dc367-153">Был создан альтернативный образ с двумя желтыми кнопками.</span><span class="sxs-lookup"><span data-stu-id="dc367-153">An alternate image was created with two yellow buttons.</span></span> <span data-ttu-id="dc367-154">Это показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="dc367-154">This is shown in the following illustration.</span></span>

![изображение при наведении](images/absam01h.png)

<span data-ttu-id="dc367-156">Альтернативный образ был создан путем копирования исходного слоя кнопки на новый слой и последующего изменения цвета заливки на желтый.</span><span class="sxs-lookup"><span data-stu-id="dc367-156">The alternate image was created by copying the original button layer to a new layer and then changing the fill color to yellow.</span></span> <span data-ttu-id="dc367-157">Эффект рельефа и выпуклости сохранен.</span><span class="sxs-lookup"><span data-stu-id="dc367-157">The bevel and emboss effect was kept.</span></span> <span data-ttu-id="dc367-158">После этого создается новый слой и добавляются изображения: стрелка указывает "Воспроизвести", а квадрат — "останавливаться".</span><span class="sxs-lookup"><span data-stu-id="dc367-158">Then a new layer was created and images were added: the arrow indicates "play" and the square indicates "stop".</span></span> <span data-ttu-id="dc367-159">Затем, если видны только новые желтые кнопки и слои типа, изображение сохраняется как копия в файл точечного рисунка.</span><span class="sxs-lookup"><span data-stu-id="dc367-159">Then, with only the new yellow button and type layers visible, the image was saved as a copy to a bitmap file.</span></span>

<span data-ttu-id="dc367-160">Результат заключается в том, что при наведении указателя мыши на область, определенную изображением сопоставления, отображается изображение для наведения, которое предупреждает читателя о том, что, если щелкнуть это место, они могут воспроизвести или закрыть проигрыватель Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dc367-160">The result is that when the mouse hovers over an area defined by the mapping image, the hover image will be displayed, alerting the reader that if they click on that spot, they can play or stop Windows Media Player.</span></span>

## <a name="final-image"></a><span data-ttu-id="dc367-161">Окончательный образ</span><span class="sxs-lookup"><span data-stu-id="dc367-161">Final Image</span></span>

<span data-ttu-id="dc367-162">Ниже приведен окончательный образ обложки.</span><span class="sxs-lookup"><span data-stu-id="dc367-162">Here is the final image of the skin.</span></span>

![окончательный образ](images/absam01f.png)

<span data-ttu-id="dc367-164">И это изображение, которое будет отображаться при наведении указателя мыши на розовую кнопку справа.</span><span class="sxs-lookup"><span data-stu-id="dc367-164">And this is the image you will see if you hover over the pink button on the right.</span></span>

![навести указатель на правую кнопку](images/absam01r.png)

## <a name="xml-code-for-the-art-example"></a><span data-ttu-id="dc367-166">XML-код для примера рисунка</span><span class="sxs-lookup"><span data-stu-id="dc367-166">XML Code for the Art Example</span></span>

<span data-ttu-id="dc367-167">Сведения о том, как писать код XML, приведены в разделе [руководство по созданию обложки](skin-creation-guide.md), но чтобы продемонстрировать, как небольшой код необходим для создания рабочей обложки, здесь приведен код для иллюстрации в этом примере.</span><span class="sxs-lookup"><span data-stu-id="dc367-167">The details of how to write XML code are given in the [Skin Creation Guide](skin-creation-guide.md), but to show how little code is needed to create a working skin, here is the code for the artwork in this example.</span></span>

<span data-ttu-id="dc367-168">Для функций Play и останавливают используются стандартные кнопки.</span><span class="sxs-lookup"><span data-stu-id="dc367-168">Predefined buttons are used for the play and stop functions.</span></span> <span data-ttu-id="dc367-169">Необходимо загрузить файл или список воспроизведения из привязки Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dc367-169">You must load a file or playlist from the Windows Media anchor.</span></span> <span data-ttu-id="dc367-170">Когда проигрыватель Windows Media переходит в режим обложки, в правом нижнем углу экрана появляется небольшое поле.</span><span class="sxs-lookup"><span data-stu-id="dc367-170">When Windows Media Player changes to skin mode, a small box appears in the lower-right corner of the screen.</span></span> <span data-ttu-id="dc367-171">Это поле называется "привязка".</span><span class="sxs-lookup"><span data-stu-id="dc367-171">This box is called the "anchor".</span></span> <span data-ttu-id="dc367-172">Если щелкнуть привязку, вы получите требуемую минимальную функциональность, в случае если Обложка не предоставляет способа вернуться в полноэкранный режим проигрывателя Windows Media.</span><span class="sxs-lookup"><span data-stu-id="dc367-172">Clicking the anchor gives you the minimum functionality needed, in case a skin does not provide a way to return to the full mode of Windows Media Player.</span></span> <span data-ttu-id="dc367-173">Пользователь может переключаться между режимами с помощью меню **вид** в полном режиме или путем щелчка привязки в режиме обложки.</span><span class="sxs-lookup"><span data-stu-id="dc367-173">The user can switch between modes by using the **View** menu if in full mode, or by clicking the anchor if in skin mode.</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp">
                
        <PLAYELEMENT
            mappingColor = "#00FF00"/>

        <STOPELEMENT
            mappingColor = "#FF0000"/>
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



## <a name="related-topics"></a><span data-ttu-id="dc367-174">См. также</span><span class="sxs-lookup"><span data-stu-id="dc367-174">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc367-175">**Файлы изображений**</span><span class="sxs-lookup"><span data-stu-id="dc367-175">**Art Files**</span></span>](art-files.md)
</dt> </dl>

 

 




