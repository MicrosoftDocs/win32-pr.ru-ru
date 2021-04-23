---
title: Команда размещения
description: Команда размещения определяет область исходного изображения и окно назначения, используемые для вывода. Эта команда распознает цифровые видеоролики и устройства наложения видео.
ms.assetid: 55fb7192-2083-45e7-a0bf-0d72a6320f91
keywords:
- размещение команды мультимедиа Windows
topic_type:
- apiref
api_name:
- put
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d22fb7c74c1ed469e609e7dcfdd3d36ba355cc5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137250"
---
# <a name="put-command"></a><span data-ttu-id="fdd77-105">Команда размещения</span><span class="sxs-lookup"><span data-stu-id="fdd77-105">put command</span></span>

<span data-ttu-id="fdd77-106">Команда размещения определяет область исходного изображения и окно назначения, используемые для вывода.</span><span class="sxs-lookup"><span data-stu-id="fdd77-106">The put command defines the area of the source image and destination window used for display.</span></span> <span data-ttu-id="fdd77-107">Эта команда распознает цифровые видеоролики и устройства наложения видео.</span><span class="sxs-lookup"><span data-stu-id="fdd77-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="fdd77-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="fdd77-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("put %s %s %s"), 
  lpszDeviceID, 
  lpszRegions, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="fdd77-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="fdd77-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fdd77-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="fdd77-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="fdd77-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="fdd77-111">Identifier of an MCI device.</span></span> <span data-ttu-id="fdd77-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="fdd77-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="fdd77-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*лпсзрегионс*</span><span class="sxs-lookup"><span data-stu-id="fdd77-113"><span id="lpszRegions"></span><span id="lpszregions"></span><span id="LPSZREGIONS"></span>*lpszRegions*</span></span>
</dt> <dd>

<span data-ttu-id="fdd77-114">Флаг для определения области.</span><span class="sxs-lookup"><span data-stu-id="fdd77-114">Flag for defining the area.</span></span> <span data-ttu-id="fdd77-115">В следующей таблице перечислены типы устройств, которые распознают команду размещения и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="fdd77-115">The following table lists device types that recognize the put command and the flags used by each type.</span></span>



| <span data-ttu-id="fdd77-116">Значение</span><span class="sxs-lookup"><span data-stu-id="fdd77-116">Value</span></span>        | <span data-ttu-id="fdd77-117">Значение</span><span class="sxs-lookup"><span data-stu-id="fdd77-117">Meaning</span></span>                                                                                      | <span data-ttu-id="fdd77-118">Значение</span><span class="sxs-lookup"><span data-stu-id="fdd77-118">Meaning</span></span>                                                                                          |
|--------------|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd77-119">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="fdd77-119">digitalvideo</span></span> | <span data-ttu-id="fdd77-120">Целевое назначение в *прямоугольной* рамке прямоугольника *исходного исходного* *кода в* прямоугольнике</span><span class="sxs-lookup"><span data-stu-id="fdd77-120">destination destination at *rectangle* frame frame at *rectangle* source source at *rectangle*</span></span> | <span data-ttu-id="fdd77-121">видео видео в окне *прямоугольного* окна в окне *прямоугольника* клиент окна клиента в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="fdd77-121">video video at *rectangle* window window at *rectangle* window client window client at *rectangle*</span></span> |
| <span data-ttu-id="fdd77-122">overlay</span><span class="sxs-lookup"><span data-stu-id="fdd77-122">overlay</span></span>      | <span data-ttu-id="fdd77-123">Целевое назначение в *прямоугольной* рамке фрейма в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="fdd77-123">destination destination at *rectangle* frame frame at *rectangle*</span></span>                             | <span data-ttu-id="fdd77-124">источник исходного кода в видеоролике  *в прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="fdd77-124">source source at *rectangle* video video at *rectangle*</span></span>                                           |



 

<span data-ttu-id="fdd77-125">В следующей таблице перечислены флаги, которые могут быть указаны в параметре **лпсзрегионс** , и их значения.</span><span class="sxs-lookup"><span data-stu-id="fdd77-125">The following table lists the flags that can be specified in the **lpszRegions** parameter and their meanings.</span></span>



| <span data-ttu-id="fdd77-126">Значение</span><span class="sxs-lookup"><span data-stu-id="fdd77-126">Value</span></span>                        | <span data-ttu-id="fdd77-127">Значение</span><span class="sxs-lookup"><span data-stu-id="fdd77-127">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                               |
|------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fdd77-128">ресурс destination</span><span class="sxs-lookup"><span data-stu-id="fdd77-128">destination</span></span>                  | <span data-ttu-id="fdd77-129">Выбирает всю клиентскую область окна назначения для вывода данных.</span><span class="sxs-lookup"><span data-stu-id="fdd77-129">Selects the entire client area of the destination window to display the data.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="fdd77-130">назначение в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="fdd77-130">destination at *rectangle*</span></span>   | <span data-ttu-id="fdd77-131">Выбирает часть клиентской области окна назначения, используемую для вывода изображения.</span><span class="sxs-lookup"><span data-stu-id="fdd77-131">Selects a portion of the client area of the destination window used to display the image.</span></span> <span data-ttu-id="fdd77-132">Если область окна просмотра задана и устройство поддерживает растяжение, исходное изображение растягивается до смещения и экстента назначения.</span><span class="sxs-lookup"><span data-stu-id="fdd77-132">When an area of the display window is specified and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                     |
| <span data-ttu-id="fdd77-133">frame</span><span class="sxs-lookup"><span data-stu-id="fdd77-133">frame</span></span>                        | <span data-ttu-id="fdd77-134">Выбирает весь буфер кадров для получения входящих видеороликов.</span><span class="sxs-lookup"><span data-stu-id="fdd77-134">Selects the entire frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="fdd77-135">рамка в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="fdd77-135">frame at *rectangle*</span></span>         | <span data-ttu-id="fdd77-136">Выбирает часть буфера кадров для получения входящих видео-изображений.</span><span class="sxs-lookup"><span data-stu-id="fdd77-136">Selects a portion of the frame buffer to receive the incoming video images.</span></span>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="fdd77-137">source</span><span class="sxs-lookup"><span data-stu-id="fdd77-137">source</span></span>                       | <span data-ttu-id="fdd77-138">Выделяет все изображение для вывода в окне назначения.</span><span class="sxs-lookup"><span data-stu-id="fdd77-138">Selects the entire image for display in the destination window.</span></span>                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="fdd77-139">Источник в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="fdd77-139">source at *rectangle*</span></span>        | <span data-ttu-id="fdd77-140">Выбирает часть изображения, которая будет отображаться в окне назначения.</span><span class="sxs-lookup"><span data-stu-id="fdd77-140">Selects a portion of the image to display in the destination window.</span></span> <span data-ttu-id="fdd77-141">Если задана область исходного изображения и устройство поддерживает растяжение, исходное изображение растягивается до смещения и экстента назначения.</span><span class="sxs-lookup"><span data-stu-id="fdd77-141">When an area of the source image is specified, and the device supports stretching, the source image is stretched to the destination offset and extent.</span></span>                                                                                                                           |
| <span data-ttu-id="fdd77-142">видео</span><span class="sxs-lookup"><span data-stu-id="fdd77-142">video</span></span>                        | <span data-ttu-id="fdd77-143">Выбирает весь входящий видеообраз для записи в буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="fdd77-143">Selects the entire incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="fdd77-144">видео в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="fdd77-144">video at *rectangle*</span></span>         | <span data-ttu-id="fdd77-145">Выбирает часть входящего изображения видео для записи в буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="fdd77-145">Selects a portion of the incoming video image to capture in the frame buffer.</span></span>                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="fdd77-146">window</span><span class="sxs-lookup"><span data-stu-id="fdd77-146">window</span></span>                       | <span data-ttu-id="fdd77-147">Восстанавливает исходный размер окна на экране.</span><span class="sxs-lookup"><span data-stu-id="fdd77-147">Restores the initial window size on the display.</span></span> <span data-ttu-id="fdd77-148">Эта команда также отображает окно.</span><span class="sxs-lookup"><span data-stu-id="fdd77-148">This command also displays the window.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="fdd77-149">окно в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="fdd77-149">window at *rectangle*</span></span>        | <span data-ttu-id="fdd77-150">Изменяет размер и расположение окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="fdd77-150">Changes the size and location of the display window.</span></span> <span data-ttu-id="fdd77-151">Указанный прямоугольник задается относительно родительского окна окна просмотра (обычно настольного компьютера), если для команды [Open](open.md) был использован флаг "дочерний стиль".</span><span class="sxs-lookup"><span data-stu-id="fdd77-151">The specified rectangle is relative to the parent window of the display window (usually the desktop) if the "style child" flag has been used for the [open](open.md) command.</span></span> <span data-ttu-id="fdd77-152">Чтобы изменить расположение окна без изменения его высоты или ширины, укажите нулевые значения для высоты и ширины.</span><span class="sxs-lookup"><span data-stu-id="fdd77-152">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span> |
| <span data-ttu-id="fdd77-153">Клиент окна</span><span class="sxs-lookup"><span data-stu-id="fdd77-153">window client</span></span>                | <span data-ttu-id="fdd77-154">Восстанавливает клиентскую область окна.</span><span class="sxs-lookup"><span data-stu-id="fdd77-154">Restores the client area of the window.</span></span>                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="fdd77-155">Клиент окна в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="fdd77-155">window client at *rectangle*</span></span> | <span data-ttu-id="fdd77-156">Изменяет размер и расположение клиентской области окна.</span><span class="sxs-lookup"><span data-stu-id="fdd77-156">Changes the size and location of the client area of the window.</span></span> <span data-ttu-id="fdd77-157">Указанный прямоугольник задается относительно родительского окна окна клиента.</span><span class="sxs-lookup"><span data-stu-id="fdd77-157">The specified rectangle is relative to the parent window of the client window.</span></span> <span data-ttu-id="fdd77-158">Чтобы изменить расположение окна без изменения его высоты или ширины, укажите нулевые значения для высоты и ширины.</span><span class="sxs-lookup"><span data-stu-id="fdd77-158">To change the location of the window without changing its height or width, specify zero for the height and width.</span></span>                                                                                      |



 

<span data-ttu-id="fdd77-159">Если флаг включает прямоугольник, то координаты прямоугольника зависят от исходного расположения окна или от источника изображения, и задаются как **x1 Y1 x2 Y2**.</span><span class="sxs-lookup"><span data-stu-id="fdd77-159">When a flag includes a rectangle, the rectangle coordinates are relative to the window origin or the image origin, as appropriate, and are specified as **X1 Y1 X2 Y2**.</span></span> <span data-ttu-id="fdd77-160">Координаты **X1Y1** задают верхний левый угол, а координаты **X2Y2** задают ширину и высоту прямоугольника.</span><span class="sxs-lookup"><span data-stu-id="fdd77-160">The coordinates **X1Y1** specify the upper left corner, and the coordinates **X2Y2** specify the width and height of the rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="fdd77-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="fdd77-161"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="fdd77-162">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="fdd77-162">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="fdd77-163">Для устройств Digital-Video также можно указать "Test".</span><span class="sxs-lookup"><span data-stu-id="fdd77-163">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="fdd77-164">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="fdd77-164">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fdd77-165">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fdd77-165">Return Value</span></span>

<span data-ttu-id="fdd77-166">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="fdd77-166">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="fdd77-167">Комментарии</span><span class="sxs-lookup"><span data-stu-id="fdd77-167">Remarks</span></span>

<span data-ttu-id="fdd77-168">Команда размещения определяет один или несколько следующих прямоугольников при работе с устройствами наложения видео:</span><span class="sxs-lookup"><span data-stu-id="fdd77-168">The put command defines one or more of the following rectangles when working with video-overlay devices:</span></span>

-   <span data-ttu-id="fdd77-169">Прямоугольник видео определяет регион входящего видеоизображения для записи.</span><span class="sxs-lookup"><span data-stu-id="fdd77-169">The video rectangle defines the region of the incoming video image to capture.</span></span>
-   <span data-ttu-id="fdd77-170">Прямоугольник фрейма определяет область буфера кадров, которая получает изображение для входящего видео.</span><span class="sxs-lookup"><span data-stu-id="fdd77-170">The frame rectangle defines the region of the frame buffer that receives the incoming video image.</span></span>
-   <span data-ttu-id="fdd77-171">Исходный прямоугольник определяет, какой регион буфера фрейма копируется в прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="fdd77-171">The source rectangle defines which region of the frame buffer is copied to the destination rectangle.</span></span>
-   <span data-ttu-id="fdd77-172">Прямоугольник назначения определяет область клиентской области окна просмотра, которая получает изображение видео.</span><span class="sxs-lookup"><span data-stu-id="fdd77-172">The destination rectangle defines the region of the display window client area that receives the video image.</span></span>

<span data-ttu-id="fdd77-173">Прямоугольник видео связан с прямоугольником фрейма так же, как исходный прямоугольник связан с прямоугольником назначения.</span><span class="sxs-lookup"><span data-stu-id="fdd77-173">The video rectangle is related to the frame rectangle in the same way the source rectangle is related to the destination rectangle.</span></span> <span data-ttu-id="fdd77-174">Растяжение может происходить от прямоугольника видео до прямоугольника фрейма и из исходного прямоугольника в прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="fdd77-174">Stretching can occur from the video rectangle to the frame rectangle and from the source rectangle to the destination rectangle.</span></span> <span data-ttu-id="fdd77-175">Не все устройства поддерживают растяжение, и растяжение должно быть включено (с помощью команды [Set](set.md) ).</span><span class="sxs-lookup"><span data-stu-id="fdd77-175">Not all devices support stretching, and stretching must be enabled (by using the [set](set.md) command).</span></span>

<span data-ttu-id="fdd77-176">Следующая команда определяет три региона для видео, кадра и источника.</span><span class="sxs-lookup"><span data-stu-id="fdd77-176">The following command defines three regions for the video, frame, and source.</span></span>

``` syntax
put vboard video 120 120 200 200 frame 0 0 200 200 source 0 0 200 200
```

<span data-ttu-id="fdd77-177">Регионы в этом примере определяются следующим образом:</span><span class="sxs-lookup"><span data-stu-id="fdd77-177">The regions in this example are defined as follows:</span></span>

-   <span data-ttu-id="fdd77-178">В буфер кадров захватывается регион с размером 200 в 200 пикселей для входных данных видео, начиная с точки с координатами 120 пикселов, из верхнего левого угла.</span><span class="sxs-lookup"><span data-stu-id="fdd77-178">A 200- by 200-pixel region of the incoming video data, starting at an origin 120 pixels from the upper left corner, will be captured to the frame buffer.</span></span>
-   <span data-ttu-id="fdd77-179">Данные видео будут помещены в область размером 200 в 200 пикселей в левом верхнем углу буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="fdd77-179">The video data will be placed in a 200- by 200-pixel region at the upper left corner of the frame buffer.</span></span>
-   <span data-ttu-id="fdd77-180">Передача выполняется из области 200 – 200-пиксель в левом верхнем углу буфера кадров в конечное окно.</span><span class="sxs-lookup"><span data-stu-id="fdd77-180">Transfers are made from the 200- by 200-pixel region at the upper left corner of the frame buffer to the destination window.</span></span>

## <a name="requirements"></a><span data-ttu-id="fdd77-181">Требования</span><span class="sxs-lookup"><span data-stu-id="fdd77-181">Requirements</span></span>



| <span data-ttu-id="fdd77-182">Требование</span><span class="sxs-lookup"><span data-stu-id="fdd77-182">Requirement</span></span> | <span data-ttu-id="fdd77-183">Значение</span><span class="sxs-lookup"><span data-stu-id="fdd77-183">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="fdd77-184">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="fdd77-184">Minimum supported client</span></span><br/> | <span data-ttu-id="fdd77-185">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fdd77-185">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fdd77-186">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="fdd77-186">Minimum supported server</span></span><br/> | <span data-ttu-id="fdd77-187">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="fdd77-187">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="fdd77-188">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="fdd77-188">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fdd77-189">MCI</span><span class="sxs-lookup"><span data-stu-id="fdd77-189">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="fdd77-190">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="fdd77-190">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="fdd77-191">open</span><span class="sxs-lookup"><span data-stu-id="fdd77-191">open</span></span>](open.md)
</dt> <dt>

[<span data-ttu-id="fdd77-192">set</span><span class="sxs-lookup"><span data-stu-id="fdd77-192">set</span></span>](set.md)
</dt> </dl>

 

