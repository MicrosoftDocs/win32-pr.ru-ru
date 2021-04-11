---
title: Команда MCI_PUT (Ммсистем. h)
description: Команда MCI « \_ разместить» задает прямоугольники источника, назначения и фрейма. Эта команда распознает цифровые видеоролики и устройства наложения видео.
ms.assetid: 9d81682b-6546-4e6d-a6df-e2de8c013b66
keywords:
- MCI_PUT команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_PUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c8fa4af30aa2b3aa6f7cdd50f453bc8edca83334
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137803"
---
# <a name="mci_put-command"></a><span data-ttu-id="acec9-105">Команда MCI « \_ разместить»</span><span class="sxs-lookup"><span data-stu-id="acec9-105">MCI\_PUT command</span></span>

<span data-ttu-id="acec9-106">Команда MCI « \_ разместить» задает прямоугольники источника, назначения и фрейма.</span><span class="sxs-lookup"><span data-stu-id="acec9-106">The MCI\_PUT command sets the source, destination, and frame rectangles.</span></span> <span data-ttu-id="acec9-107">Эта команда распознает цифровые видеоролики и устройства наложения видео.</span><span class="sxs-lookup"><span data-stu-id="acec9-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="acec9-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="acec9-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_PUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpDest
);
```



## <a name="parameters"></a><span data-ttu-id="acec9-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="acec9-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="acec9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="acec9-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="acec9-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="acec9-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="acec9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="acec9-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="acec9-113">\_Уведомление MCI, \_ Ожидание MCI или, для устройств с цифровыми видео, \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="acec9-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="acec9-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="acec9-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="acec9-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*лпдест*</span><span class="sxs-lookup"><span data-stu-id="acec9-115"><span id="lpDest"></span><span id="lpdest"></span><span id="LPDEST"></span>*lpDest*</span></span>
</dt> <dd>

<span data-ttu-id="acec9-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="acec9-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="acec9-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="acec9-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="acec9-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="acec9-118">Return Value</span></span>

<span data-ttu-id="acec9-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="acec9-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="acec9-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="acec9-120">Remarks</span></span>

<span data-ttu-id="acec9-121">С типом устройства **дигиталвидео** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="acec9-121">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="acec9-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>MCI \_ ДГВ \_ Размещение \_ клиента</span><span class="sxs-lookup"><span data-stu-id="acec9-122"><span id="MCI_DGV_PUT_CLIENT"></span><span id="mci_dgv_put_client"></span>MCI\_DGV\_PUT\_CLIENT</span></span>
</dt> <dd>

<span data-ttu-id="acec9-123">Прямоугольник, определенный для MCI \_ ДГВ \_ Rect, применяется к положению клиентского окна.</span><span class="sxs-lookup"><span data-stu-id="acec9-123">The rectangle defined for MCI\_DGV\_RECT applies to the position of the client window.</span></span> <span data-ttu-id="acec9-124">Указанный прямоугольник задается относительно родительского окна окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="acec9-124">The rectangle specified is relative to the parent window of the display window.</span></span> <span data-ttu-id="acec9-125">\_ \_ \_ Этот флаг должен быть установлен одновременно для окна размещения MCI ДГВ.</span><span class="sxs-lookup"><span data-stu-id="acec9-125">MCI\_DGV\_PUT\_WINDOW must be set concurrently with this flag.</span></span>

</dd> <dt>

<span data-ttu-id="acec9-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>\_ДГВ \_ размещения MCI \_</span><span class="sxs-lookup"><span data-stu-id="acec9-126"><span id="MCI_DGV_PUT_DESTINATION"></span><span id="mci_dgv_put_destination"></span>MCI\_DGV\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="acec9-127">Прямоугольник, определенный для MCI \_ ДГВ \_ Rect, задает прямоугольник назначения.</span><span class="sxs-lookup"><span data-stu-id="acec9-127">The rectangle defined for MCI\_DGV\_RECT specifies a destination rectangle.</span></span> <span data-ttu-id="acec9-128">Прямоугольник назначения определяет часть окна клиента, связанную с этим экземпляром драйвера устройства, которая показывает изображение или видео.</span><span class="sxs-lookup"><span data-stu-id="acec9-128">The destination rectangle specifies the portion of the client window associated with this device driver instance that shows the image or video.</span></span>

</dd> <dt>

<span data-ttu-id="acec9-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>MCI \_ ДГВ \_ Размещение \_ фрейма</span><span class="sxs-lookup"><span data-stu-id="acec9-129"><span id="MCI_DGV_PUT_FRAME"></span><span id="mci_dgv_put_frame"></span>MCI\_DGV\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="acec9-130">Прямоугольник, определенный для MCI \_ ДГВ \_ Rect, применяется к прямоугольнику фрейма.</span><span class="sxs-lookup"><span data-stu-id="acec9-130">The rectangle defined for MCI\_DGV\_RECT applies to the frame rectangle.</span></span> <span data-ttu-id="acec9-131">Прямоугольник фрейма указывает часть буфера фрейма, используемую в качестве места назначения видеороликов, полученных из прямоугольника видео.</span><span class="sxs-lookup"><span data-stu-id="acec9-131">The frame rectangle specifies the portion of the frame buffer used as the destination of the video images obtained from the video rectangle.</span></span> <span data-ttu-id="acec9-132">Видео должно масштабироваться в соответствии с прямоугольником буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="acec9-132">The video should be scaled to fit within the frame buffer rectangle.</span></span>

<span data-ttu-id="acec9-133">Прямоугольник задается в координатах буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="acec9-133">The rectangle is specified in frame buffer coordinates.</span></span> <span data-ttu-id="acec9-134">Прямоугольником по умолчанию является полный буфер кадра.</span><span class="sxs-lookup"><span data-stu-id="acec9-134">The default rectangle is the full frame buffer.</span></span> <span data-ttu-id="acec9-135">Указание этого прямоугольника позволяет устройству масштабировать изображение, когда оно поддерживает эти данные.</span><span class="sxs-lookup"><span data-stu-id="acec9-135">Specifying this rectangle lets the device scale the image as it digitizes the data.</span></span> <span data-ttu-id="acec9-136">Устройства, которые не могут масштабировать образ, отклоняют эту команду с помощью \_ НЕподдерживаемой \_ функции мЦиерр.</span><span class="sxs-lookup"><span data-stu-id="acec9-136">Devices that cannot scale the image reject this command with MCIERR\_UNSUPPORTED\_FUNCTION.</span></span> <span data-ttu-id="acec9-137">Вы можете использовать \_ флаг ЖЕТДЕВКАПС MCI \_ , \_ чтобы определить, масштабируется ли устройство с помощью команды [MCI \_ жетдевкапс](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="acec9-137">You can use the MCI\_GETDEVCAPS\_CAN\_STRETCH flag with the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command to determine if a device scales the image.</span></span> <span data-ttu-id="acec9-138">Устройство возвращает **значение false** , если оно не может масштабировать изображение.</span><span class="sxs-lookup"><span data-stu-id="acec9-138">A device returns **FALSE** if it cannot scale the image.</span></span>

</dd> <dt>

<span data-ttu-id="acec9-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>\_источник MCI \_ ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="acec9-139"><span id="MCI_DGV_PUT_SOURCE"></span><span id="mci_dgv_put_source"></span>MCI\_DGV\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="acec9-140">Прямоугольник, определенный для MCI \_ ДГВ \_ Rect, указывает исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="acec9-140">The rectangle defined for MCI\_DGV\_RECT specifies a source rectangle.</span></span> <span data-ttu-id="acec9-141">Исходный прямоугольник указывает, какая часть буфера фрейма должна масштабироваться для размещения в прямоугольнике назначения.</span><span class="sxs-lookup"><span data-stu-id="acec9-141">The source rectangle specifies which portion of the frame buffer is to be scaled to fit into the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="acec9-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>\_видео о \_ размещении MCI ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="acec9-142"><span id="MCI_DGV_PUT_VIDEO"></span><span id="mci_dgv_put_video"></span>MCI\_DGV\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="acec9-143">Прямоугольник, определенный для MCI \_ ДГВ \_ Rect, применяется к прямоугольнику видео.</span><span class="sxs-lookup"><span data-stu-id="acec9-143">The rectangle defined for MCI\_DGV\_RECT applies to the video rectangle.</span></span> <span data-ttu-id="acec9-144">В прямоугольнике видео указывается, какая часть текущего источника презентации хранится в буфере кадров.</span><span class="sxs-lookup"><span data-stu-id="acec9-144">The video rectangle specifies which portion of the current presentation source is stored in the frame buffer.</span></span> <span data-ttu-id="acec9-145">Прямоугольник задается с помощью естественных координат источника представления.</span><span class="sxs-lookup"><span data-stu-id="acec9-145">The rectangle is specified using the natural coordinates of the presentation source.</span></span> <span data-ttu-id="acec9-146">Он позволяет определить кадрирование, которое происходит до сохранения изображений и видео в буфере кадров.</span><span class="sxs-lookup"><span data-stu-id="acec9-146">It allows the specification of cropping that occurs prior to storing images and video in the frame buffer.</span></span> <span data-ttu-id="acec9-147">Прямоугольником по умолчанию является полная активная область сканирования или полные распакованные изображения и видео.</span><span class="sxs-lookup"><span data-stu-id="acec9-147">The default rectangle is the full active scan area or the full decompressed images and video.</span></span>

</dd> <dt>

<span data-ttu-id="acec9-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>\_ \_ окно размещения MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="acec9-148"><span id="MCI_DGV_PUT_WINDOW"></span><span id="mci_dgv_put_window"></span>MCI\_DGV\_PUT\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="acec9-149">Прямоугольник, определенный для MCI \_ ДГВ \_ Rect, применяется к окну просмотра.</span><span class="sxs-lookup"><span data-stu-id="acec9-149">The rectangle defined for MCI\_DGV\_RECT applies to the display window.</span></span> <span data-ttu-id="acec9-150">Этот прямоугольник относится к родительскому окну окна просмотра (обычно это рабочий стол).</span><span class="sxs-lookup"><span data-stu-id="acec9-150">This rectangle is relative to the parent window of the display window (usually the desktop).</span></span> <span data-ttu-id="acec9-151">Если окно не указано, по умолчанию используется исходный размер и расположение окна.</span><span class="sxs-lookup"><span data-stu-id="acec9-151">If the window is not specified, it defaults to the initial window size and position.</span></span>

</dd> <dt>

<span data-ttu-id="acec9-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI \_ ДГВ \_ Rect</span><span class="sxs-lookup"><span data-stu-id="acec9-152"><span id="MCI_DGV_RECT"></span><span id="mci_dgv_rect"></span>MCI\_DGV\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="acec9-153">Элемент **RC** структуры, идентифицируемой *лпдест* , содержит допустимый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="acec9-153">The **rc** member of the structure identified by *lpDest* contains a valid rectangle.</span></span>

</dd> </dl>

<span data-ttu-id="acec9-154">Для устройств с цифровыми видео *лпдест* указывает на структуру [**MCI \_ ДГВ \_ \_ пармс**](/previous-versions//dd743397(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="acec9-154">For digital-video devices, *lpDest* points to an [**MCI\_DGV\_PUT\_PARMS**](/previous-versions//dd743397(v=vs.85)) structure.</span></span>

<span data-ttu-id="acec9-155">Для типа устройства **наложения** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="acec9-155">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="acec9-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>\_овли \_ размещения MCI \_</span><span class="sxs-lookup"><span data-stu-id="acec9-156"><span id="MCI_OVLY_PUT_DESTINATION"></span><span id="mci_ovly_put_destination"></span>MCI\_OVLY\_PUT\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="acec9-157">Прямоугольник, определенный для MCI \_ овли \_ Rect, указывает область окна клиента, используемую для вывода изображения.</span><span class="sxs-lookup"><span data-stu-id="acec9-157">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the client window used to display an image.</span></span> <span data-ttu-id="acec9-158">Прямоугольник содержит смещение и видимую область изображения относительно начала координат окна.</span><span class="sxs-lookup"><span data-stu-id="acec9-158">The rectangle contains the offset and visible extent of the image relative to the window origin.</span></span> <span data-ttu-id="acec9-159">Если кадр растягивается, источник растягивается до прямоугольника назначения.</span><span class="sxs-lookup"><span data-stu-id="acec9-159">If the frame is being stretched, the source is stretched to the destination rectangle.</span></span>

</dd> <dt>

<span data-ttu-id="acec9-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>MCI \_ овли \_ Размещение \_ фрейма</span><span class="sxs-lookup"><span data-stu-id="acec9-160"><span id="MCI_OVLY_PUT_FRAME"></span><span id="mci_ovly_put_frame"></span>MCI\_OVLY\_PUT\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="acec9-161">Прямоугольник, определенный для MCI \_ овли \_ Rect, указывает область видеобуфера, используемую для получения видеоизображения.</span><span class="sxs-lookup"><span data-stu-id="acec9-161">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used to receive the video image.</span></span> <span data-ttu-id="acec9-162">Прямоугольник содержит смещение и экстент области буфера относительно источника видеобуфера.</span><span class="sxs-lookup"><span data-stu-id="acec9-162">The rectangle contains the offset and extent of the buffer area relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="acec9-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>\_источник MCI \_ овли \_</span><span class="sxs-lookup"><span data-stu-id="acec9-163"><span id="MCI_OVLY_PUT_SOURCE"></span><span id="mci_ovly_put_source"></span>MCI\_OVLY\_PUT\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="acec9-164">Прямоугольник, определенный для MCI \_ овли \_ Rect, указывает область видеобуфера, используемую в качестве источника цифрового изображения.</span><span class="sxs-lookup"><span data-stu-id="acec9-164">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video buffer used as the source of the digital image.</span></span> <span data-ttu-id="acec9-165">Прямоугольник содержит смещение и экстент прямоугольника обрезки для видеобуфера относительно его источника.</span><span class="sxs-lookup"><span data-stu-id="acec9-165">The rectangle contains the offset and extent of the clipping rectangle for the video buffer relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="acec9-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>\_видео о \_ размещении MCI овли \_</span><span class="sxs-lookup"><span data-stu-id="acec9-166"><span id="MCI_OVLY_PUT_VIDEO"></span><span id="mci_ovly_put_video"></span>MCI\_OVLY\_PUT\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="acec9-167">Прямоугольник, определенный для MCI \_ овли \_ Rect, определяет область видеозаписи видеобуфера.</span><span class="sxs-lookup"><span data-stu-id="acec9-167">The rectangle defined for MCI\_OVLY\_RECT specifies the area of the video source capture by the video buffer.</span></span> <span data-ttu-id="acec9-168">Прямоугольник содержит смещение и экстент прямоугольника обрезки для источника видео относительно его происхождения.</span><span class="sxs-lookup"><span data-stu-id="acec9-168">The rectangle contains the offset and extent of the clipping rectangle for the video source relative to its origin.</span></span>

</dd> <dt>

<span data-ttu-id="acec9-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI \_ овли \_ Rect</span><span class="sxs-lookup"><span data-stu-id="acec9-169"><span id="MCI_OVLY_RECT"></span><span id="mci_ovly_rect"></span>MCI\_OVLY\_RECT</span></span>
</dt> <dd>

<span data-ttu-id="acec9-170">Элемент **RC** структуры, идентифицируемой *лпдест* , содержит допустимый отображаемый прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="acec9-170">The **rc** member of the structure identified by *lpDest* contains a valid display rectangle.</span></span> <span data-ttu-id="acec9-171">Если этот флаг не указан, то прямоугольник по умолчанию соответствует координатам видеобуфера или окна, на которое выполняется усечение.</span><span class="sxs-lookup"><span data-stu-id="acec9-171">If this flag is not specified, the default rectangle matches the coordinates of the video buffer or window being clipped.</span></span>

</dd> </dl>

<span data-ttu-id="acec9-172">Для устройств с наложением видео *лпдест* указывает на структуру [**MCI \_ овли \_ Rect \_ пармс**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="acec9-172">For video-overlay devices, *lpDest* points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="acec9-173">Требования</span><span class="sxs-lookup"><span data-stu-id="acec9-173">Requirements</span></span>



| <span data-ttu-id="acec9-174">Требование</span><span class="sxs-lookup"><span data-stu-id="acec9-174">Requirement</span></span> | <span data-ttu-id="acec9-175">Значение</span><span class="sxs-lookup"><span data-stu-id="acec9-175">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="acec9-176">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="acec9-176">Minimum supported client</span></span><br/> | <span data-ttu-id="acec9-177">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="acec9-177">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="acec9-178">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="acec9-178">Minimum supported server</span></span><br/> | <span data-ttu-id="acec9-179">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="acec9-179">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="acec9-180">Заголовок</span><span class="sxs-lookup"><span data-stu-id="acec9-180">Header</span></span><br/>                   | <dl> <span data-ttu-id="acec9-181"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="acec9-181"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="acec9-182">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="acec9-182">See also</span></span>

<dl> <dt>

[<span data-ttu-id="acec9-183">MCI</span><span class="sxs-lookup"><span data-stu-id="acec9-183">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="acec9-184">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="acec9-184">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

