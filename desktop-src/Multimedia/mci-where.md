---
title: Команда MCI_WHERE (Ммсистем. h)
description: Команда MCI, \_ которая получает прямоугольник обрезки для видеоустройства.
ms.assetid: f64a7e49-4ee1-4836-ba9a-0bbdc47626b3
keywords:
- MCI_WHERE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_WHERE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6619131319863d1159a3bdb8bb85d366243544a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988713"
---
# <a name="mci_where-command"></a><span data-ttu-id="335f2-104">\_Команда MCI WHERE</span><span class="sxs-lookup"><span data-stu-id="335f2-104">MCI\_WHERE command</span></span>

<span data-ttu-id="335f2-105">Команда MCI, \_ которая получает прямоугольник обрезки для видеоустройства.</span><span class="sxs-lookup"><span data-stu-id="335f2-105">The MCI\_WHERE command obtains the clipping rectangle for the video device.</span></span> <span data-ttu-id="335f2-106">Эта команда распознает цифровые видеоролики и устройства наложения видео.</span><span class="sxs-lookup"><span data-stu-id="335f2-106">Digital-video, and video-overlay devices recognize this command.</span></span> <span data-ttu-id="335f2-107">**Верхний** и **левый** элементы возвращенного [Rect](/previous-versions//ms536136(v=vs.85)) содержат источник прямоугольника обрезки, а **правый** и **Нижний** элементы содержат ширину и высоту прямоугольника обрезки.</span><span class="sxs-lookup"><span data-stu-id="335f2-107">The **top** and **left** members of the returned [RECT](/previous-versions//ms536136(v=vs.85)) contain the origin of the clipping rectangle, and the **right** and **bottom** members contain the width and height of the clipping rectangle.</span></span> <span data-ttu-id="335f2-108">(Это не стандартное использование **правых** и **нижних** элементов.)</span><span class="sxs-lookup"><span data-stu-id="335f2-108">(This is not the standard use of the **right** and **bottom** members.)</span></span>

<span data-ttu-id="335f2-109">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="335f2-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_WHERE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpQuery
);
```



## <a name="parameters"></a><span data-ttu-id="335f2-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="335f2-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="335f2-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="335f2-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="335f2-112">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="335f2-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="335f2-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="335f2-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="335f2-114">\_Уведомление MCI, \_ Ожидание MCI или, для устройств с цифровыми видео, \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="335f2-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video devices, MCI\_TEST.</span></span> <span data-ttu-id="335f2-115">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="335f2-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="335f2-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*лпкуери*</span><span class="sxs-lookup"><span data-stu-id="335f2-116"><span id="lpQuery"></span><span id="lpquery"></span><span id="LPQUERY"></span>*lpQuery*</span></span>
</dt> <dd>

<span data-ttu-id="335f2-117">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="335f2-117">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="335f2-118">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="335f2-118">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="335f2-119">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="335f2-119">Return Value</span></span>

<span data-ttu-id="335f2-120">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="335f2-120">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="335f2-121">Комментарии</span><span class="sxs-lookup"><span data-stu-id="335f2-121">Remarks</span></span>

<span data-ttu-id="335f2-122">С типом устройства **дигиталвидео** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="335f2-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="335f2-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI \_ ДГВ, \_ где \_ Destination</span><span class="sxs-lookup"><span data-stu-id="335f2-123"><span id="MCI_DGV_WHERE_DESTINATION"></span><span id="mci_dgv_where_destination"></span>MCI\_DGV\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="335f2-124">Получает описание прямоугольной области, используемой для вывода видео и изображений в клиентской области текущего окна.</span><span class="sxs-lookup"><span data-stu-id="335f2-124">Obtains a description of the rectangular region used to display video and images in the client area of the current window.</span></span>

</dd> <dt>

<span data-ttu-id="335f2-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI \_ ДГВ, \_ где \_ Frame</span><span class="sxs-lookup"><span data-stu-id="335f2-125"><span id="MCI_DGV_WHERE_FRAME"></span><span id="mci_dgv_where_frame"></span>MCI\_DGV\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="335f2-126">Получает описание прямоугольной области буфера кадров, в которой масштабируются изображения из прямоугольника видео.</span><span class="sxs-lookup"><span data-stu-id="335f2-126">Obtains a description of the rectangular region of the frame buffer into which images from the video rectangle are scaled.</span></span> <span data-ttu-id="335f2-127">Координаты прямоугольника помещаются в элемент **RC** структуры, идентифицируемой *лпкуери*.</span><span class="sxs-lookup"><span data-stu-id="335f2-127">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="335f2-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI \_ ДГВ, \_ где \_ Max</span><span class="sxs-lookup"><span data-stu-id="335f2-128"><span id="MCI_DGV_WHERE_MAX"></span><span id="mci_dgv_where_max"></span>MCI\_DGV\_WHERE\_MAX</span></span>
</dt> <dd>

<span data-ttu-id="335f2-129">При использовании с MCI \_ ДГВ \_ \_ , где Destination или \_ MCI \_ ДГВ \_ , где Source, возвращаемый прямоугольник указывает максимальную ширину и высоту указанной области.</span><span class="sxs-lookup"><span data-stu-id="335f2-129">When used with MCI\_DGV\_WHERE\_DESTINATION or MCI\_DGV\_WHERE\_SOURCE, the rectangle returned indicates the maximum width and height of the specified region.</span></span> <span data-ttu-id="335f2-130">При использовании с MCI \_ ДГВ \_ \_ , где Window, возвращаемый прямоугольник указывает размер всего экрана.</span><span class="sxs-lookup"><span data-stu-id="335f2-130">When used with MCI\_DGV\_WHERE\_WINDOW, the rectangle returned indicates the size of the entire display.</span></span>

</dd> <dt>

<span data-ttu-id="335f2-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI \_ ДГВ, \_ где \_ Source</span><span class="sxs-lookup"><span data-stu-id="335f2-131"><span id="MCI_DGV_WHERE_SOURCE"></span><span id="mci_dgv_where_source"></span>MCI\_DGV\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="335f2-132">Получает описание прямоугольной области (обрезанной из буфера кадров), которая растягивается в соответствии с прямоугольником назначения на экране.</span><span class="sxs-lookup"><span data-stu-id="335f2-132">Obtains a description of the rectangular region (cropped from the frame buffer) that is stretched to fit the destination rectangle on the display.</span></span>

</dd> <dt>

<span data-ttu-id="335f2-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI \_ ДГВ, \_ где \_ видео</span><span class="sxs-lookup"><span data-stu-id="335f2-133"><span id="MCI_DGV_WHERE_VIDEO"></span><span id="mci_dgv_where_video"></span>MCI\_DGV\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="335f2-134">Получает описание прямоугольной области, обрезанной от источника презентации, для заполнения прямоугольника фрейма в буфере кадров.</span><span class="sxs-lookup"><span data-stu-id="335f2-134">Obtains a description of the rectangular region cropped from the presentation source to fill the frame rectangle in the frame buffer.</span></span> <span data-ttu-id="335f2-135">Координаты прямоугольника помещаются в элемент **RC** структуры, идентифицируемой *лпкуери*.</span><span class="sxs-lookup"><span data-stu-id="335f2-135">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="335f2-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI \_ ДГВ, \_ где \_ окно</span><span class="sxs-lookup"><span data-stu-id="335f2-136"><span id="MCI_DGV_WHERE_WINDOW"></span><span id="mci_dgv_where_window"></span>MCI\_DGV\_WHERE\_WINDOW</span></span>
</dt> <dd>

<span data-ttu-id="335f2-137">Получает описание рамки для окна просмотра.</span><span class="sxs-lookup"><span data-stu-id="335f2-137">Obtains a description of the display-window frame.</span></span>

</dd> <dt>


</dt> <dd></dd> </dl>

<span data-ttu-id="335f2-138">Для устройств с цифровыми видео параметр *лпкуери* указывает на **ДГВ MCI, где \_ Структура \_ \_ пармс** .</span><span class="sxs-lookup"><span data-stu-id="335f2-138">For digital-video devices, the *lpQuery* parameter points to an **MCI\_DGV\_WHERE\_PARMS** structure.</span></span> <span data-ttu-id="335f2-139">**ДГВ MCI \_ , \_ где структура \_ Пармс** идентична структуре [**MCI \_ ДГВ \_ Rect \_ пармс**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) .</span><span class="sxs-lookup"><span data-stu-id="335f2-139">The **MCI\_DGV\_WHERE\_PARMS** structure is identical to the [**MCI\_DGV\_RECT\_PARMS**](/windows/win32/api/digitalv/ns-digitalv-mci_dgv_rect_parms) structure.</span></span>

<span data-ttu-id="335f2-140">Для типа устройства **наложения** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="335f2-140">The following additional flags are used with the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="335f2-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI \_ овли, \_ где \_ Destination</span><span class="sxs-lookup"><span data-stu-id="335f2-141"><span id="MCI_OVLY_WHERE_DESTINATION"></span><span id="mci_ovly_where_destination"></span>MCI\_OVLY\_WHERE\_DESTINATION</span></span>
</dt> <dd>

<span data-ttu-id="335f2-142">Получает конечный прямоугольник для вывода.</span><span class="sxs-lookup"><span data-stu-id="335f2-142">Obtains the destination display rectangle.</span></span> <span data-ttu-id="335f2-143">Координаты прямоугольника помещаются в элемент **RC** структуры, идентифицируемой *лпкуери*.</span><span class="sxs-lookup"><span data-stu-id="335f2-143">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="335f2-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI \_ овли, \_ где \_ Frame</span><span class="sxs-lookup"><span data-stu-id="335f2-144"><span id="MCI_OVLY_WHERE_FRAME"></span><span id="mci_ovly_where_frame"></span>MCI\_OVLY\_WHERE\_FRAME</span></span>
</dt> <dd>

<span data-ttu-id="335f2-145">Получает прямоугольник наложенного фрейма.</span><span class="sxs-lookup"><span data-stu-id="335f2-145">Obtains the overlay frame rectangle.</span></span> <span data-ttu-id="335f2-146">Координаты прямоугольника помещаются в элемент **RC** структуры, идентифицируемой *лпкуери*.</span><span class="sxs-lookup"><span data-stu-id="335f2-146">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="335f2-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI \_ овли, \_ где \_ Source</span><span class="sxs-lookup"><span data-stu-id="335f2-147"><span id="MCI_OVLY_WHERE_SOURCE"></span><span id="mci_ovly_where_source"></span>MCI\_OVLY\_WHERE\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="335f2-148">Получает исходный прямоугольник.</span><span class="sxs-lookup"><span data-stu-id="335f2-148">Obtains the source rectangle.</span></span> <span data-ttu-id="335f2-149">Координаты прямоугольника помещаются в элемент **RC** структуры, идентифицируемой *лпкуери*.</span><span class="sxs-lookup"><span data-stu-id="335f2-149">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> <dt>

<span data-ttu-id="335f2-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI \_ овли, \_ где \_ видео</span><span class="sxs-lookup"><span data-stu-id="335f2-150"><span id="MCI_OVLY_WHERE_VIDEO"></span><span id="mci_ovly_where_video"></span>MCI\_OVLY\_WHERE\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="335f2-151">Получает прямоугольник видео.</span><span class="sxs-lookup"><span data-stu-id="335f2-151">Obtains the video rectangle.</span></span> <span data-ttu-id="335f2-152">Координаты прямоугольника помещаются в элемент **RC** структуры, идентифицируемой *лпкуери*.</span><span class="sxs-lookup"><span data-stu-id="335f2-152">The rectangle coordinates are placed in the **rc** member of the structure identified by *lpQuery*.</span></span>

</dd> </dl>

<span data-ttu-id="335f2-153">Для устройств с наложением параметр *лпкуери* указывает на структуру [**MCI \_ овли \_ Rect \_ пармс**](mci-ovly-rect-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="335f2-153">For video-overlay devices, the *lpQuery* parameter points to an [**MCI\_OVLY\_RECT\_PARMS**](mci-ovly-rect-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="335f2-154">Требования</span><span class="sxs-lookup"><span data-stu-id="335f2-154">Requirements</span></span>



| <span data-ttu-id="335f2-155">Требование</span><span class="sxs-lookup"><span data-stu-id="335f2-155">Requirement</span></span> | <span data-ttu-id="335f2-156">Значение</span><span class="sxs-lookup"><span data-stu-id="335f2-156">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="335f2-157">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="335f2-157">Minimum supported client</span></span><br/> | <span data-ttu-id="335f2-158">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="335f2-158">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="335f2-159">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="335f2-159">Minimum supported server</span></span><br/> | <span data-ttu-id="335f2-160">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="335f2-160">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="335f2-161">Заголовок</span><span class="sxs-lookup"><span data-stu-id="335f2-161">Header</span></span><br/>                   | <dl> <span data-ttu-id="335f2-162"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="335f2-162"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="335f2-163">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="335f2-163">See also</span></span>

<dl> <dt>

[<span data-ttu-id="335f2-164">MCI</span><span class="sxs-lookup"><span data-stu-id="335f2-164">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="335f2-165">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="335f2-165">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

