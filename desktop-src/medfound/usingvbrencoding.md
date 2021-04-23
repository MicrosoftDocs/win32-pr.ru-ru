---
description: В этом разделе описывается настройка потоков VBR.
ms.assetid: 9dd3ff5b-4c7c-41a8-b1b9-7ea380175193
title: Использование кодирования VBR (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cdd1f317308d79c696e26a8671cc9d84ca8effa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104263481"
---
# <a name="using-vbr-encoding-microsoft-media-foundation"></a><span data-ttu-id="97c4f-103">Использование кодирования VBR (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="97c4f-103">Using VBR Encoding (Microsoft Media Foundation)</span></span>

<span data-ttu-id="97c4f-104">Как описано в разделе [методы кодирования](encodingmethods.md) , для повышения согласованности качества содержимого используется кодирование с переменной СКОРОСТЬЮ (VBR).</span><span class="sxs-lookup"><span data-stu-id="97c4f-104">As detailed in the [Encoding Methods](encodingmethods.md) topic, variable bit rate (VBR) encoding is used to improve the consistency of content quality.</span></span> <span data-ttu-id="97c4f-105">Потоки VBR настраиваются точно так же, как потоки с постоянными скоростями (CBR), за исключением параметров буфера (скорость потока и окно буфера).</span><span class="sxs-lookup"><span data-stu-id="97c4f-105">You configure VBR streams in the same way that you encode constant bit rate (CBR) streams, except for the buffer parameters (bit rate and buffer window).</span></span> <span data-ttu-id="97c4f-106">В этом разделе описывается настройка потоков VBR.</span><span class="sxs-lookup"><span data-stu-id="97c4f-106">This section describes how to configure VBR streams.</span></span>

## <a name="configuring-quality-based-vbr"></a><span data-ttu-id="97c4f-107">Настройка качества VBR</span><span class="sxs-lookup"><span data-stu-id="97c4f-107">Configuring Quality Based VBR</span></span>

<span data-ttu-id="97c4f-108">Для кодирования, использующего метод VBR на основе метода Quality, не требуются стандартные параметры буфера.</span><span class="sxs-lookup"><span data-stu-id="97c4f-108">Encoding using the quality based VBR method does not require any predefined buffer parameters.</span></span> <span data-ttu-id="97c4f-109">Вместо этого указывается уровень качества (от 0 до 100), используемый кодировщиком для динамического определения соответствующих параметров буфера.</span><span class="sxs-lookup"><span data-stu-id="97c4f-109">Instead, you specify a quality level (from 0 to 100) which the encoder uses to determine the appropriate buffer parameters dynamically.</span></span> <span data-ttu-id="97c4f-110">Этот режим кодирования использует только один проход кодирования.</span><span class="sxs-lookup"><span data-stu-id="97c4f-110">This encoding mode uses only one encoding pass.</span></span>

<span data-ttu-id="97c4f-111">Вы можете перечислить Поддерживаемые типы выходных данных VBR на основе качества для аудиокодеков.</span><span class="sxs-lookup"><span data-stu-id="97c4f-111">You can enumerate the supported quality-based VBR output types for the audio codecs.</span></span> <span data-ttu-id="97c4f-112">При задании типа выходных данных необходимо использовать один из типов, возвращаемых DMO.</span><span class="sxs-lookup"><span data-stu-id="97c4f-112">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="97c4f-113">Дополнительные сведения см. в разделе [Перечисление типов аудио для конкретных режимов кодирования](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="97c4f-113">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="97c4f-114">Чтобы настроить поток видео VBR с учетом качества, необходимо задать свойства, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="97c4f-114">To configure a quality-based VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="97c4f-115">Свойство</span><span class="sxs-lookup"><span data-stu-id="97c4f-115">Property</span></span>                                            | <span data-ttu-id="97c4f-116">Описание</span><span class="sxs-lookup"><span data-stu-id="97c4f-116">Description</span></span>                                                                                                                                             |
|-----------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="97c4f-117">МФПКЭЙ \_ вбренаблед</span><span class="sxs-lookup"><span data-stu-id="97c4f-117">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="97c4f-118">Установите значение \_ true.</span><span class="sxs-lookup"><span data-stu-id="97c4f-118">Set to VARIANT\_TRUE.</span></span>                                                                                                                                   |
| [<span data-ttu-id="97c4f-119">МФПКЭЙ \_ вбркуалити</span><span class="sxs-lookup"><span data-stu-id="97c4f-119">MFPKEY\_VBRQUALITY</span></span>](mfpkey-vbrqualityproperty.md) | <span data-ttu-id="97c4f-120">Задайте нужное значение качества от 0 до 100.</span><span class="sxs-lookup"><span data-stu-id="97c4f-120">Set to the desired quality value, from 0 to 100.</span></span> <span data-ttu-id="97c4f-121">Не все значения качества представляют дискретные параметры.</span><span class="sxs-lookup"><span data-stu-id="97c4f-121">Not all quality values represent discrete settings.</span></span> <span data-ttu-id="97c4f-122">Дополнительные сведения см. в описании свойства.</span><span class="sxs-lookup"><span data-stu-id="97c4f-122">See the property description for more information.</span></span> |



 

## <a name="configuring-unconstrained-vbr"></a><span data-ttu-id="97c4f-123">Настройка неограниченных VBR</span><span class="sxs-lookup"><span data-stu-id="97c4f-123">Configuring Unconstrained VBR</span></span>

<span data-ttu-id="97c4f-124">Неограниченная кодировка VBR позволяет кодировщику изменять размер отдельных выборок без явных ограничений буфера.</span><span class="sxs-lookup"><span data-stu-id="97c4f-124">Unconstrained VBR encoding enables the encoder to vary the size of individual samples without any explicit buffer limits.</span></span> <span data-ttu-id="97c4f-125">Однако средняя скорость потока на протяжении полученного содержимого должна быть меньше или равна указанному значению.</span><span class="sxs-lookup"><span data-stu-id="97c4f-125">However, the average bit rate over the duration of the resulting content must be less than or equal to the specified value.</span></span> <span data-ttu-id="97c4f-126">Для неограниченной VBR требуется два прохода кодирования.</span><span class="sxs-lookup"><span data-stu-id="97c4f-126">Unconstrained VBR requires two encoding passes.</span></span>

<span data-ttu-id="97c4f-127">Можно перечислить Поддерживаемые типы выходных данных VBR с двумя проходами для аудиокодеков.</span><span class="sxs-lookup"><span data-stu-id="97c4f-127">You can enumerate the supported two-pass VBR output types for the audio codecs.</span></span> <span data-ttu-id="97c4f-128">При задании типа выходных данных необходимо использовать один из типов, возвращаемых DMO.</span><span class="sxs-lookup"><span data-stu-id="97c4f-128">You must use one of the types returned by the DMO when setting the output type.</span></span> <span data-ttu-id="97c4f-129">Дополнительные сведения см. в разделе [Перечисление типов аудио для конкретных режимов кодирования](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="97c4f-129">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="97c4f-130">Для настройки видеопотока с неограниченным каналом VBR необходимо задать свойства, перечисленные в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="97c4f-130">To configure an unconstrained VBR video stream, you must set the properties that are listed in the following table.</span></span>



| <span data-ttu-id="97c4f-131">Свойство</span><span class="sxs-lookup"><span data-stu-id="97c4f-131">Property</span></span>                                            | <span data-ttu-id="97c4f-132">Описание</span><span class="sxs-lookup"><span data-stu-id="97c4f-132">Description</span></span>                          |
|-----------------------------------------------------|--------------------------------------|
| [<span data-ttu-id="97c4f-133">МФПКЭЙ \_ вбренаблед</span><span class="sxs-lookup"><span data-stu-id="97c4f-133">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="97c4f-134">Установите значение \_ true.</span><span class="sxs-lookup"><span data-stu-id="97c4f-134">Set to VARIANT\_TRUE.</span></span>                |
| [<span data-ttu-id="97c4f-135">МФПКЭЙ \_ пассесусед</span><span class="sxs-lookup"><span data-stu-id="97c4f-135">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="97c4f-136">Задайте значение 2.</span><span class="sxs-lookup"><span data-stu-id="97c4f-136">Set to 2.</span></span>                            |
| [<span data-ttu-id="97c4f-137">МФПКЭЙ \_ равг</span><span class="sxs-lookup"><span data-stu-id="97c4f-137">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="97c4f-138">Задайте требуемую среднюю скорость.</span><span class="sxs-lookup"><span data-stu-id="97c4f-138">Set to the desired average bit rate.</span></span> |



 

## <a name="configuring-peak-constrained-vbr"></a><span data-ttu-id="97c4f-139">Настройка Peak-Constrained VBR</span><span class="sxs-lookup"><span data-stu-id="97c4f-139">Configuring Peak-Constrained VBR</span></span>

<span data-ttu-id="97c4f-140">Пиковая частота VBR похожа на "неограниченное число VBR", так как она ограничена средним битом скорости в течение потока.</span><span class="sxs-lookup"><span data-stu-id="97c4f-140">Peak-constrained VBR is like unconstrained VBR in that it is confined to an average bit rate over the duration of the stream.</span></span> <span data-ttu-id="97c4f-141">Кроме того, Пиковая нагрузка соответствует пиковому буферу.</span><span class="sxs-lookup"><span data-stu-id="97c4f-141">In addition, peak-constrained VBR conforms to a peak buffer.</span></span> <span data-ttu-id="97c4f-142">Этот буфер описывается с использованием пиковой скорости потока и пикового окна буфера, точно так же, как буфер CBR описывается средним битом скорости и окном буфера.</span><span class="sxs-lookup"><span data-stu-id="97c4f-142">This buffer is described using a peak bit rate and a peak buffer window, just as a CBR buffer is described by an average bit rate and a buffer window.</span></span> <span data-ttu-id="97c4f-143">Этот режим обеспечивает гибкость кодировщика при кодировании отдельных выборок с соблюдением пиковых ограничений.</span><span class="sxs-lookup"><span data-stu-id="97c4f-143">This mode gives the encoder flexibility in how it encodes individual samples while adhering to the peak limitations.</span></span> <span data-ttu-id="97c4f-144">Это особенно полезно при декодировании с помощью микросхемы устройства, например проигрывателя DVD, при этом необходимо учитывать ограничения по оборудованию.</span><span class="sxs-lookup"><span data-stu-id="97c4f-144">This is particularly useful when decoding is performed by a chip in a device, like a DVD player, where there are hardware limitations that must be considered.</span></span>

<span data-ttu-id="97c4f-145">Поддерживаемые выходные типы выходных кодировщика VBR с ограничением пиковой нагрузки — это те же типы, которые перечислены для неограниченных VBR.</span><span class="sxs-lookup"><span data-stu-id="97c4f-145">The supported peak-constrained, VBR audio encoder output types are the same types enumerated for unconstrained VBR.</span></span> <span data-ttu-id="97c4f-146">Установите пиковые значения для DMO и используйте доставленный тип.</span><span class="sxs-lookup"><span data-stu-id="97c4f-146">Set the peak values on the DMO and use the delivered type.</span></span> <span data-ttu-id="97c4f-147">Дополнительные сведения см. в разделе [Перечисление типов аудио для конкретных режимов кодирования](enumeratingaudiotypesforspecificencodingmodes.md).</span><span class="sxs-lookup"><span data-stu-id="97c4f-147">For more information, see [Enumerating Audio Types for Specific Encoding Modes](enumeratingaudiotypesforspecificencodingmodes.md).</span></span>

<span data-ttu-id="97c4f-148">Чтобы настроить поток видео с пиковым ограничением VBR, необходимо задать свойства, перечисленные в следующей таблице, с помощью метода **ипропертибаг:: Write** .</span><span class="sxs-lookup"><span data-stu-id="97c4f-148">To configure a peak-constrained VBR video stream, you must set the properties that are listed in the following table using the **IPropertyBag::Write** method.</span></span>



| <span data-ttu-id="97c4f-149">Свойство</span><span class="sxs-lookup"><span data-stu-id="97c4f-149">Property</span></span>                                            | <span data-ttu-id="97c4f-150">Описание</span><span class="sxs-lookup"><span data-stu-id="97c4f-150">Description</span></span>                                                     |
|-----------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="97c4f-151">МФПКЭЙ \_ вбренаблед</span><span class="sxs-lookup"><span data-stu-id="97c4f-151">MFPKEY\_VBRENABLED</span></span>](mfpkey-vbrenabledproperty.md) | <span data-ttu-id="97c4f-152">Установите значение \_ true.</span><span class="sxs-lookup"><span data-stu-id="97c4f-152">Set to VARIANT\_TRUE.</span></span>                                           |
| [<span data-ttu-id="97c4f-153">МФПКЭЙ \_ пассесусед</span><span class="sxs-lookup"><span data-stu-id="97c4f-153">MFPKEY\_PASSESUSED</span></span>](mfpkey-passesusedproperty.md) | <span data-ttu-id="97c4f-154">Задайте значение 2.</span><span class="sxs-lookup"><span data-stu-id="97c4f-154">Set to 2.</span></span>                                                       |
| [<span data-ttu-id="97c4f-155">МФПКЭЙ \_ равг</span><span class="sxs-lookup"><span data-stu-id="97c4f-155">MFPKEY\_RAVG</span></span>](mfpkey-ravgproperty.md)             | <span data-ttu-id="97c4f-156">Задайте требуемую среднюю скорость.</span><span class="sxs-lookup"><span data-stu-id="97c4f-156">Set to the desired average bit rate.</span></span>                            |
| [<span data-ttu-id="97c4f-157">МФПКЭЙ \_ рмакс</span><span class="sxs-lookup"><span data-stu-id="97c4f-157">MFPKEY\_RMAX</span></span>](mfpkey-rmaxproperty.md)             | <span data-ttu-id="97c4f-158">Задайте желаемую пиковую скорость.</span><span class="sxs-lookup"><span data-stu-id="97c4f-158">Set to the desired peak bit rate.</span></span>                               |
| [<span data-ttu-id="97c4f-159">МФПКЭЙ \_ бмакс</span><span class="sxs-lookup"><span data-stu-id="97c4f-159">MFPKEY\_BMAX</span></span>](mfpkey-bmaxproperty.md)             | <span data-ttu-id="97c4f-160">Задайте для параметра окно буфера, соответствующее пиковой скорости.</span><span class="sxs-lookup"><span data-stu-id="97c4f-160">Set to the buffer window that corresponds to the peak bit rate.</span></span> |



 

> [!Note]  
> <span data-ttu-id="97c4f-161">Рекомендуется установить пиковую скорость по крайней мере вдвое в два раза выше средней скорости.</span><span class="sxs-lookup"><span data-stu-id="97c4f-161">It is recommended that you set the peak bit rate to at least twice the average bit rate.</span></span> <span data-ttu-id="97c4f-162">Если задать для пиковой скорости более низкое значение, то кодек может кодировать содержимое как CBR, а не Пиковое ограничение VBR.</span><span class="sxs-lookup"><span data-stu-id="97c4f-162">Setting the peak rate to a lower value may cause the codec to encode the content as two-pass CBR instead of peak-constrained VBR.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="97c4f-163">См. также</span><span class="sxs-lookup"><span data-stu-id="97c4f-163">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97c4f-164">Кодеки Windows Media</span><span class="sxs-lookup"><span data-stu-id="97c4f-164">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> <dt>

[<span data-ttu-id="97c4f-165">Использование кодировки Two-Pass</span><span class="sxs-lookup"><span data-stu-id="97c4f-165">Using Two-Pass Encoding</span></span>](usingtwoencodingpasses.md)
</dt> <dt>

[<span data-ttu-id="97c4f-166">Работа с аудио</span><span class="sxs-lookup"><span data-stu-id="97c4f-166">Working with Audio</span></span>](workingwithaudio.md)
</dt> <dt>

[<span data-ttu-id="97c4f-167">Работа с видео</span><span class="sxs-lookup"><span data-stu-id="97c4f-167">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



