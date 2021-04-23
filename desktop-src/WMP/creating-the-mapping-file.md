---
title: Создание файла сопоставления
description: Создание файла сопоставления
ms.assetid: d882cd5b-1404-4dfd-8b51-a61e1505fae1
keywords:
- Создание обложек, файлы сопоставлений
- Обложки проигрывателя Windows Media, графические файлы
- обложки, файлы Art
- файлы для обложек, изображений
- графические файлы для обложек, изображения сопоставления
- Обложки проигрывателя Windows Media, сопоставление изображений
- обложки, сопоставление изображений
- Сопоставление изображений в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b71682f48ecdba098f76a9e27f656b27d5fe8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410628"
---
# <a name="creating-the-mapping-file"></a><span data-ttu-id="59555-111">Создание файла сопоставления</span><span class="sxs-lookup"><span data-stu-id="59555-111">Creating the Mapping File</span></span>

<span data-ttu-id="59555-112">После создания фрагментов основного файла рисунка сравнительно легко создать файл сопоставления.</span><span class="sxs-lookup"><span data-stu-id="59555-112">Once you have created the pieces of your primary art file, it is relatively easy to create a mapping file.</span></span> <span data-ttu-id="59555-113">Вы создадите новый файл сопоставления, объединив рисунок из двух уже созданных слоев кнопок.</span><span class="sxs-lookup"><span data-stu-id="59555-113">You will create the new mapping file by combining the art from the two button layers you already created.</span></span>

1.  <span data-ttu-id="59555-114">Вам потребуется сделать две кнопки, созданные для основного файла рисунка, и скопировать их на новый слой.</span><span class="sxs-lookup"><span data-stu-id="59555-114">You will need to take the two buttons you created for the primary art file and copy them to a new layer.</span></span> <span data-ttu-id="59555-115">Выполните следующие действия. Скопируйте слой кнопки "Закрыть", удалите все эффекты слоя и переименуйте его "закрыть карту".</span><span class="sxs-lookup"><span data-stu-id="59555-115">Use the following steps: Copy the Close button layer, remove any Layer effects, and rename it "Close map".</span></span> <span data-ttu-id="59555-116">Картинка должна выглядеть плоской, без рельефов.</span><span class="sxs-lookup"><span data-stu-id="59555-116">The art should look flat, with no bevels.</span></span>
2.  <span data-ttu-id="59555-117">Используйте палитру цветов, чтобы создать цвет переднего плана чистого красного цвета.</span><span class="sxs-lookup"><span data-stu-id="59555-117">Use the Color Picker to create a foreground color of pure red.</span></span> <span data-ttu-id="59555-118">Убедитесь, что для номера цвета задано значение " \# FF0000".</span><span class="sxs-lookup"><span data-stu-id="59555-118">Be sure the color number value is "\#FF0000".</span></span> <span data-ttu-id="59555-119">Затем с помощью средства заливка заполните часть окружности слоя "закрыть карту".</span><span class="sxs-lookup"><span data-stu-id="59555-119">Then use the Paint Bucket tool to fill the inside of the circle of the Close map layer.</span></span>
3.  <span data-ttu-id="59555-120">Скопируйте слой кнопки воспроизведения, удалите все эффекты слоя и переименуйте его "Map гиперкарта" (воспроизвести карту).</span><span class="sxs-lookup"><span data-stu-id="59555-120">Copy the Play button layer, remove any Layer effects, and rename it "Play map".</span></span> <span data-ttu-id="59555-121">Опять же, картинка должна выглядеть плоской.</span><span class="sxs-lookup"><span data-stu-id="59555-121">Again, the art should look flat.</span></span> <span data-ttu-id="59555-122">Вы не хотите вносить какие-либо эффекты на уровне сопоставления, так как вы просто определяете области точечного рисунка, которые проигрыватель Windows Media будет использовать для определения места, в котором мышь выполняет действие и что вы хотите сделать с ним.</span><span class="sxs-lookup"><span data-stu-id="59555-122">You do not want any effects in the mapping layer because you are just defining regions of the bitmap that Windows Media Player will use to determine where the mouse performs an action and what you want to do with it.</span></span>
4.  <span data-ttu-id="59555-123">Используйте палитру цветов, чтобы создать цвет переднего плана чистого зеленого цвета.</span><span class="sxs-lookup"><span data-stu-id="59555-123">Use the Color Picker to create a foreground color of pure green.</span></span> <span data-ttu-id="59555-124">Убедитесь, что для номера цвета задано значение " \# 00FF00".</span><span class="sxs-lookup"><span data-stu-id="59555-124">Be sure the color number value is "\#00FF00".</span></span> <span data-ttu-id="59555-125">Затем используйте инструмент заливка для заполнения внутри круга слоя карт воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="59555-125">Then use the Paint Bucket tool to fill the inside of the circle of the Play map layer.</span></span>

<span data-ttu-id="59555-126">Теперь все готово для создания файла сопоставлений.</span><span class="sxs-lookup"><span data-stu-id="59555-126">You are now ready to create the mapping art file.</span></span> <span data-ttu-id="59555-127">Скрыть все слои, а затем показать только следующие слои в указанном порядке (сверху вниз):</span><span class="sxs-lookup"><span data-stu-id="59555-127">Hide all layers, and then show only the following layers, in this order (top to bottom):</span></span>

<span data-ttu-id="59555-128">Воспроизвести карту</span><span class="sxs-lookup"><span data-stu-id="59555-128">Play map</span></span>

<span data-ttu-id="59555-129">Закрыть карту</span><span class="sxs-lookup"><span data-stu-id="59555-129">Close map</span></span>

<span data-ttu-id="59555-130">Сохраните в новый файл с помощью команды сохранить копию в меню файл.</span><span class="sxs-lookup"><span data-stu-id="59555-130">Save to a new file using the Save a Copy command from the File menu.</span></span> <span data-ttu-id="59555-131">Выберите параметр BMP в части сохранить как диалогового окна Сохранить копию и введите имя файла, который будет ссылаться позже в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="59555-131">Select the BMP option in the Save As portion of the Save a Copy dialog box and type a file name that you will refer to later in your skin definition file.</span></span> <span data-ttu-id="59555-132">В идеале он должен находиться в том же каталоге, что и файл определения обложки.</span><span class="sxs-lookup"><span data-stu-id="59555-132">Ideally it should be in the same directory as your skin definition file.</span></span> <span data-ttu-id="59555-133">Например, можно вызвать этот файл map.bmp.</span><span class="sxs-lookup"><span data-stu-id="59555-133">For example, you could call this file map.bmp.</span></span> <span data-ttu-id="59555-134">Выберите параметры по умолчанию и сохраните файл.</span><span class="sxs-lookup"><span data-stu-id="59555-134">Choose the default settings and save the file.</span></span>

<span data-ttu-id="59555-135">Файл сопоставления должен выглядеть, как показано на следующем рисунке.</span><span class="sxs-lookup"><span data-stu-id="59555-135">Your mapping file should look like the following illustration.</span></span>

![mapping file](images/g01map.png)

<span data-ttu-id="59555-137">Как можно предположить, Зеленая область будет использоваться для определения того, когда следует начать проигрыватель Windows Media, а красная область — для ее отмены.</span><span class="sxs-lookup"><span data-stu-id="59555-137">As you might guess, the green area will be used to determine when to make Windows Media Player start and the red area is for telling it to stop.</span></span> <span data-ttu-id="59555-138">Можно использовать любые два цвета, если вы используете цветовые номера при настройке файла определения обложки.</span><span class="sxs-lookup"><span data-stu-id="59555-138">Any two colors can be used, as long as you use the color numbers when you set up the skin definition file.</span></span> <span data-ttu-id="59555-139">Убедитесь, что цвета на карте являются чистыми цветами для региона, который вы хотите использовать, и различающиеся края.</span><span class="sxs-lookup"><span data-stu-id="59555-139">Be sure the colors in the map are pure colors for the region you want to use and have distinct edges.</span></span> <span data-ttu-id="59555-140">Чистый цвет будет одним, где каждый одиночный пиксель в области имеет одинаковое значение цвета.</span><span class="sxs-lookup"><span data-stu-id="59555-140">A pure color would be one where every single pixel in the area has the same color value.</span></span> <span data-ttu-id="59555-141">Использование этого действия может размытие или искажение границы, тем самым слегка изменяя цвета некоторых пикселов.</span><span class="sxs-lookup"><span data-stu-id="59555-141">Using an effect may blur or distort the edge, thereby slightly modifying the colors of some of the pixels.</span></span> <span data-ttu-id="59555-142">Файл сопоставления виден только для мыши, а не для человека, поэтому не следует заполнять его и удалять все эффекты слоев, которые могли быть перенесены из других слоев.</span><span class="sxs-lookup"><span data-stu-id="59555-142">The mapping file is only seen by the mouse, not a human, so do not bother decorating it, and remove any layer effects you may have carried over from other layers.</span></span>

<span data-ttu-id="59555-143">При сохранении файла выбранное имя файла будет впоследствии использоваться в качестве значения атрибута **маппингимаже** элемента **BUTTONGROUP** в файле определения обложки.</span><span class="sxs-lookup"><span data-stu-id="59555-143">When you save your file, the file name you choose will later be used as the value for the **mappingImage** attribute of the **BUTTONGROUP** element in your skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59555-144">См. также</span><span class="sxs-lookup"><span data-stu-id="59555-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59555-145">**Создание первой обложки**</span><span class="sxs-lookup"><span data-stu-id="59555-145">**Building Your First Skin**</span></span>](building-your-first-skin.md)
</dt> </dl>

 

 




