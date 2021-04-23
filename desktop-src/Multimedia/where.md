---
title: команда Where
description: Команда Where извлекает прямоугольник, указывающий исходную или целевую область. Этот прямоугольник был указан с помощью команды размещения. Эта команда распознает цифровые видеоролики и устройства наложения видео.
ms.assetid: 85c68ded-bd3e-4a48-9af7-58478615a7f0
keywords:
- размещение команд мультимедиа Windows
topic_type:
- apiref
api_name:
- where
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22c499eae8f0209c1ef93efb9677ae438dcf0e86
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989213"
---
# <a name="where-command"></a><span data-ttu-id="ecc90-106">команда Where</span><span class="sxs-lookup"><span data-stu-id="ecc90-106">where command</span></span>

<span data-ttu-id="ecc90-107">Команда Where извлекает прямоугольник, указывающий исходную или целевую область.</span><span class="sxs-lookup"><span data-stu-id="ecc90-107">The where command retrieves the rectangle specifying the source or destination area.</span></span> <span data-ttu-id="ecc90-108">Этот прямоугольник был указан с помощью команды [размещения](put.md) .</span><span class="sxs-lookup"><span data-stu-id="ecc90-108">This rectangle was specified using the [put](put.md) command.</span></span> <span data-ttu-id="ecc90-109">Эта команда распознает цифровые видеоролики и устройства наложения видео.</span><span class="sxs-lookup"><span data-stu-id="ecc90-109">Digital-video, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="ecc90-110">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ecc90-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("where %s %s %s"), 
  lpszDeviceID, 
  lpszRequestRect, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="ecc90-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="ecc90-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ecc90-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="ecc90-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ecc90-113">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="ecc90-113">Identifier of an MCI device.</span></span> <span data-ttu-id="ecc90-114">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="ecc90-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="ecc90-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*лпсзрекуестрект*</span><span class="sxs-lookup"><span data-stu-id="ecc90-115"><span id="lpszRequestRect"></span><span id="lpszrequestrect"></span><span id="LPSZREQUESTRECT"></span>*lpszRequestRect*</span></span>
</dt> <dd>

<span data-ttu-id="ecc90-116">Флаг, определяющий прямоугольник, измерения которого извлекаются.</span><span class="sxs-lookup"><span data-stu-id="ecc90-116">Flag that identifies the rectangle whose dimensions are retrieved.</span></span> <span data-ttu-id="ecc90-117">В следующей таблице перечислены типы устройств, которые распознают команду **WHERE** и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="ecc90-117">The following table lists device types that recognize the **where** command and the flags used by each type.</span></span>



| <span data-ttu-id="ecc90-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ecc90-118">Value</span></span>        | <span data-ttu-id="ecc90-119">Значение</span><span class="sxs-lookup"><span data-stu-id="ecc90-119">Meaning</span></span>                                                       | <span data-ttu-id="ecc90-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ecc90-120">Meaning</span></span>                                  |
|--------------|---------------------------------------------------------------|------------------------------------------|
| <span data-ttu-id="ecc90-121">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="ecc90-121">digitalvideo</span></span> | <span data-ttu-id="ecc90-122">дестинатиондестинатион [**Max**](max.md)фрамефраме макссаурце</span><span class="sxs-lookup"><span data-stu-id="ecc90-122">destinationdestination [**max**](max.md)frameframe maxsource</span></span> | <span data-ttu-id="ecc90-123">Source максвидеовидео максвиндоввиндов Max</span><span class="sxs-lookup"><span data-stu-id="ecc90-123">source maxvideovideo maxwindowwindow max</span></span> |
| <span data-ttu-id="ecc90-124">overlay</span><span class="sxs-lookup"><span data-stu-id="ecc90-124">overlay</span></span>      | <span data-ttu-id="ecc90-125">дестинатионфраме</span><span class="sxs-lookup"><span data-stu-id="ecc90-125">destinationframe</span></span>                                              | <span data-ttu-id="ecc90-126">sourcevideoprofile</span><span class="sxs-lookup"><span data-stu-id="ecc90-126">sourcevideo</span></span>                              |



 

<span data-ttu-id="ecc90-127">В следующей таблице перечислены флаги, которые могут быть указаны в параметре **лпсзрекуестрект** , и их значения.</span><span class="sxs-lookup"><span data-stu-id="ecc90-127">The following table lists the flags that can be specified in the **lpszRequestRect** parameter and their meanings.</span></span>



| <span data-ttu-id="ecc90-128">Значение</span><span class="sxs-lookup"><span data-stu-id="ecc90-128">Value</span></span>                          | <span data-ttu-id="ecc90-129">Значение</span><span class="sxs-lookup"><span data-stu-id="ecc90-129">Meaning</span></span>                                                                                                                                                                                                                                                                                              |
|--------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ecc90-130">ресурс destination</span><span class="sxs-lookup"><span data-stu-id="ecc90-130">destination</span></span>                    | <span data-ttu-id="ecc90-131">Извлекает смещение и экстент назначения.</span><span class="sxs-lookup"><span data-stu-id="ecc90-131">Retrieves the destination offset and extent.</span></span> <span data-ttu-id="ecc90-132">Для устройств наложения видео прямоугольник назначения определяет область клиентской области окна отображения, в которой отображаются данные изображения из буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="ecc90-132">For video-overlay devices, the destination rectangle defines the area of the display window client area that displays the image data from the frame buffer.</span></span>                                                                                             |
| <span data-ttu-id="ecc90-133">[ **Максимальное** значение назначения](max.md)</span><span class="sxs-lookup"><span data-stu-id="ecc90-133">destination [**max**](max.md)</span></span> | <span data-ttu-id="ecc90-134">Извлекает текущий размер прямоугольника клиента.</span><span class="sxs-lookup"><span data-stu-id="ecc90-134">Retrieves the current size of the client rectangle.</span></span>                                                                                                                                                                                                                                                  |
| <span data-ttu-id="ecc90-135">frame</span><span class="sxs-lookup"><span data-stu-id="ecc90-135">frame</span></span>                          | <span data-ttu-id="ecc90-136">Извлекает смещение и экстент прямоугольника буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="ecc90-136">Retrieves the offset and extent of the frame buffer rectangle.</span></span> <span data-ttu-id="ecc90-137">Прямоугольник буфера фрейма определяет область буфера кадров, которая получает входящие данные видео.</span><span class="sxs-lookup"><span data-stu-id="ecc90-137">The frame buffer rectangle defines the area of the frame buffer that receives incoming video data.</span></span> <span data-ttu-id="ecc90-138">Изображения из прямоугольника "видео" масштабируются в этот регион.</span><span class="sxs-lookup"><span data-stu-id="ecc90-138">Images from the "video" rectangle are scaled into this region.</span></span>                                                                     |
| <span data-ttu-id="ecc90-139">[ **максимальный размер** рамки](max.md)</span><span class="sxs-lookup"><span data-stu-id="ecc90-139">frame [**max**](max.md)</span></span>       | <span data-ttu-id="ecc90-140">Возвращает максимальный размер буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="ecc90-140">Returns the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="ecc90-141">source</span><span class="sxs-lookup"><span data-stu-id="ecc90-141">source</span></span>                         | <span data-ttu-id="ecc90-142">Извлекает исходное смещение и экстент.</span><span class="sxs-lookup"><span data-stu-id="ecc90-142">Retrieves the source offset and extent.</span></span> <span data-ttu-id="ecc90-143">Для устройств наложения видео исходный прямоугольник определяет область буфера кадров, которая отображается в окне назначения.</span><span class="sxs-lookup"><span data-stu-id="ecc90-143">For video-overlay devices, the source rectangle defines the region of the frame buffer that is displayed in the destination window.</span></span> <span data-ttu-id="ecc90-144">Устройство использует этот прямоугольник для обрезки изображения перед его растяжением, чтобы он соответствовал прямоугольнику назначения на экране.</span><span class="sxs-lookup"><span data-stu-id="ecc90-144">The device uses this rectangle to crop the image before it is stretched to fit the destination rectangle on the display.</span></span> |
| <span data-ttu-id="ecc90-145">[ **максимальный** источник](max.md)</span><span class="sxs-lookup"><span data-stu-id="ecc90-145">source [**max**](max.md)</span></span>      | <span data-ttu-id="ecc90-146">Возвращает максимальный размер буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="ecc90-146">Retrieves the maximum size of the frame buffer.</span></span>                                                                                                                                                                                                                                                      |
| <span data-ttu-id="ecc90-147">видео</span><span class="sxs-lookup"><span data-stu-id="ecc90-147">video</span></span>                          | <span data-ttu-id="ecc90-148">Извлекает смещение и экстент видеопрямоугольника.</span><span class="sxs-lookup"><span data-stu-id="ecc90-148">Retrieves the offset and extent of the video rectangle.</span></span> <span data-ttu-id="ecc90-149">Прямоугольник видео определяет регион входящих видеоданных, которые передаются в буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="ecc90-149">The video rectangle defines the region of the incoming video data that is transferred to the frame buffer.</span></span>                                                                                                                                   |
| <span data-ttu-id="ecc90-150">[ **Макс** . видео](max.md)</span><span class="sxs-lookup"><span data-stu-id="ecc90-150">video [**max**](max.md)</span></span>       | <span data-ttu-id="ecc90-151">Возвращает максимальный размер входных данных.</span><span class="sxs-lookup"><span data-stu-id="ecc90-151">Returns the maximum size of the input.</span></span>                                                                                                                                                                                                                                                               |
| <span data-ttu-id="ecc90-152">window</span><span class="sxs-lookup"><span data-stu-id="ecc90-152">window</span></span>                         | <span data-ttu-id="ecc90-153">Извлекает текущий размер и расположение рамки окна монитора.</span><span class="sxs-lookup"><span data-stu-id="ecc90-153">Retrieves the current size and position of the display-window frame.</span></span>                                                                                                                                                                                                                                 |
| <span data-ttu-id="ecc90-154">[ **максимальный размер** окна](max.md)</span><span class="sxs-lookup"><span data-stu-id="ecc90-154">window [**max**](max.md)</span></span>      | <span data-ttu-id="ecc90-155">Возвращает размер всего экрана.</span><span class="sxs-lookup"><span data-stu-id="ecc90-155">Retrieves the size of the entire display.</span></span>                                                                                                                                                                                                                                                            |



 

</dd> <dt>

<span data-ttu-id="ecc90-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="ecc90-156"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ecc90-157">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="ecc90-157">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="ecc90-158">Для устройств Digital-Video также можно указать "Test".</span><span class="sxs-lookup"><span data-stu-id="ecc90-158">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="ecc90-159">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ecc90-159">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ecc90-160">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ecc90-160">Return Value</span></span>

<span data-ttu-id="ecc90-161">Возвращает прямоугольник в параметре *лпсзретурнстринг* функции [**mciSendString**](/previous-versions//dd757161(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="ecc90-161">Returns a rectangle in the *lpszReturnString* parameter of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function.</span></span> <span data-ttu-id="ecc90-162">Прямоугольник описывает область, указанную в параметре *лпсзрекуестрект* этой команды.</span><span class="sxs-lookup"><span data-stu-id="ecc90-162">The rectangle describes the area specified in the *lpszRequestRect* parameter of this command.</span></span> <span data-ttu-id="ecc90-163">Прямоугольник задается как *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="ecc90-163">The rectangle is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="ecc90-164">Координаты *x1 Y1* определяют левый верхний угол прямоугольника, а координаты *x2 Y2* определяют ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="ecc90-164">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span>

## <a name="examples"></a><span data-ttu-id="ecc90-165">Примеры</span><span class="sxs-lookup"><span data-stu-id="ecc90-165">Examples</span></span>

<span data-ttu-id="ecc90-166">Следующая команда возвращает отображаемый прямоугольник устройства "Movie".</span><span class="sxs-lookup"><span data-stu-id="ecc90-166">The following command returns the display rectangle of the "movie" device.</span></span>

``` syntax
where movie destination
```

## <a name="requirements"></a><span data-ttu-id="ecc90-167">Требования</span><span class="sxs-lookup"><span data-stu-id="ecc90-167">Requirements</span></span>



| <span data-ttu-id="ecc90-168">Требование</span><span class="sxs-lookup"><span data-stu-id="ecc90-168">Requirement</span></span> | <span data-ttu-id="ecc90-169">Значение</span><span class="sxs-lookup"><span data-stu-id="ecc90-169">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ecc90-170">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ecc90-170">Minimum supported client</span></span><br/> | <span data-ttu-id="ecc90-171">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ecc90-171">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ecc90-172">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ecc90-172">Minimum supported server</span></span><br/> | <span data-ttu-id="ecc90-173">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ecc90-173">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ecc90-174">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ecc90-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ecc90-175">MCI</span><span class="sxs-lookup"><span data-stu-id="ecc90-175">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ecc90-176">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="ecc90-176">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="ecc90-177">PUT</span><span class="sxs-lookup"><span data-stu-id="ecc90-177">put</span></span>](put.md)
</dt> </dl>

 

