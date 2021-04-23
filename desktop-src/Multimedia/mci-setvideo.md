---
title: Команда MCI_SETVIDEO (Ммсистем. h)
description: Команда MCI \_ сетвидео задает значения, связанные с воспроизведением видео. Эта команда распознает устройства цифрового видео и ВИДЕОМАГНИТОФОНА.
ms.assetid: b84956d8-01a0-49f6-a96c-2693a25e6f2a
keywords:
- MCI_SETVIDEO команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SETVIDEO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 83a20e0cc5466ac9ff28a59543543069fa9acd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490773"
---
# <a name="mci_setvideo-command"></a><span data-ttu-id="433fe-105">\_Команда MCI сетвидео</span><span class="sxs-lookup"><span data-stu-id="433fe-105">MCI\_SETVIDEO command</span></span>

<span data-ttu-id="433fe-106">Команда MCI \_ сетвидео задает значения, связанные с воспроизведением видео.</span><span class="sxs-lookup"><span data-stu-id="433fe-106">The MCI\_SETVIDEO command sets values associated with video playback.</span></span> <span data-ttu-id="433fe-107">Эта команда распознает устройства цифрового видео и ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="433fe-107">Digital-video and VCR devices recognize this command.</span></span>

<span data-ttu-id="433fe-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="433fe-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETVIDEO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetVideo
);
```



## <a name="parameters"></a><span data-ttu-id="433fe-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="433fe-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="433fe-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="433fe-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="433fe-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="433fe-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="433fe-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="433fe-113">**MCI \_ УВЕДОМЛЕНИЕ**, **\_ Ожидание MCI** или **\_ тест MCI**.</span><span class="sxs-lookup"><span data-stu-id="433fe-113">**MCI\_NOTIFY**, **MCI\_WAIT**, or **MCI\_TEST**.</span></span> <span data-ttu-id="433fe-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="433fe-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="433fe-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*лпсетвидео*</span><span class="sxs-lookup"><span data-stu-id="433fe-115"><span id="lpSetVideo"></span><span id="lpsetvideo"></span><span id="LPSETVIDEO"></span>*lpSetVideo*</span></span>
</dt> <dd>

<span data-ttu-id="433fe-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="433fe-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="433fe-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="433fe-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="433fe-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="433fe-118">Return Value</span></span>

<span data-ttu-id="433fe-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="433fe-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="433fe-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="433fe-120">Remarks</span></span>

<span data-ttu-id="433fe-121">С типом устройства "дигиталвидео" используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="433fe-121">The following additional flags are used with the "digitalvideo" device type:</span></span>

<dl> <dt>

<span data-ttu-id="433fe-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI \_ ДГВ \_ сетвидео \_ ALG</span><span class="sxs-lookup"><span data-stu-id="433fe-122"><span id="MCI_DGV_SETVIDEO_ALG"></span><span id="mci_dgv_setvideo_alg"></span>MCI\_DGV\_SETVIDEO\_ALG</span></span>
</dt> <dd>

<span data-ttu-id="433fe-123">Элемент **лпстралгорисм** структуры, идентифицируемой *лпсетвидео* , содержит адрес буфера, содержащего имя алгоритма сжатия видео.</span><span class="sxs-lookup"><span data-stu-id="433fe-123">The **lpstrAlgorithm** member of the structure identified by *lpSetVideo* contains an address of a buffer containing the name of a video compression algorithm.</span></span> <span data-ttu-id="433fe-124">Алгоритм сжатия используется последующими командами [ \_ резервирования MCI](mci-reserve.md) или [ \_ записи MCI](mci-record.md) .</span><span class="sxs-lookup"><span data-stu-id="433fe-124">The compression algorithm is used by subsequent [MCI\_RESERVE](mci-reserve.md) or [MCI\_RECORD](mci-record.md) commands.</span></span> <span data-ttu-id="433fe-125">Доступные алгоритмы зависят от устройства.</span><span class="sxs-lookup"><span data-stu-id="433fe-125">The available algorithms are device dependent.</span></span>

<span data-ttu-id="433fe-126">Если указанный алгоритм несовместим с текущим форматом файла, формат файла меняется на формат по умолчанию для алгоритма.</span><span class="sxs-lookup"><span data-stu-id="433fe-126">If the specified algorithm is incompatible with the current file format, the file format is changed to the default format for the algorithm.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI \_ ДГВ \_ сетвидео \_ клокктиме</span><span class="sxs-lookup"><span data-stu-id="433fe-127"><span id="MCI_DGV_SETVIDEO_CLOCKTIME"></span><span id="mci_dgv_setvideo_clocktime"></span>MCI\_DGV\_SETVIDEO\_CLOCKTIME</span></span>
</dt> <dd>

<span data-ttu-id="433fe-128">При использовании с **MCI \_ ДГВ \_ сетвидео \_**, указывает, что время указывается в миллисекундах и является абсолютным временем.</span><span class="sxs-lookup"><span data-stu-id="433fe-128">When used with **MCI\_DGV\_SETVIDEO\_OVER**, indicates time is specified in milliseconds and is absolute time.</span></span> <span data-ttu-id="433fe-129">(На этот раз это не пошаговое воспроизведение рабочей области.)</span><span class="sxs-lookup"><span data-stu-id="433fe-129">(This time is not in step with the playing of the workspace.)</span></span>

</dd> <dt>

<span data-ttu-id="433fe-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>\_ \_ \_ входные данные сетвидео MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="433fe-130"><span id="MCI_DGV_SETVIDEO_INPUT"></span><span id="mci_dgv_setvideo_input"></span>MCI\_DGV\_SETVIDEO\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="433fe-131">Изменяет **\_ \_ \_ яркость MCI ДГВ сетвидео**, **MCI \_ ДГВ \_ сетвидео \_**, MCI **\_ ДГВ \_ сетвидео \_ контраст**, **MCI \_ ДГВ \_ сетвидео \_ гамма**, **MCI \_ ДГВ \_ сетвидео \_**, или **MCI \_ ДГВ \_ сетвидео \_ оттенок** , чтобы он влиял на входной сигнал и изменяет записываемые данные.</span><span class="sxs-lookup"><span data-stu-id="433fe-131">Modifies the **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** so that it affects the input signal and modifies what is recorded.</span></span> <span data-ttu-id="433fe-132">По возможности это значение по умолчанию при мониторинге входных данных.</span><span class="sxs-lookup"><span data-stu-id="433fe-132">If possible, this is the default when monitoring the input.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>\_ \_ элемент сетвидео MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="433fe-133"><span id="MCI_DGV_SETVIDEO_ITEM"></span><span id="mci_dgv_setvideo_item"></span>MCI\_DGV\_SETVIDEO\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="433fe-134">Константа Video указывается в элементе **двитем** структуры, определенной параметром *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-134">A video constant is specified in the **dwItem** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-135">Константа определяет заданное значение.</span><span class="sxs-lookup"><span data-stu-id="433fe-135">The constant identifies the value that is being set.</span></span> <span data-ttu-id="433fe-136">С этим флагом можно указать следующие константы:</span><span class="sxs-lookup"><span data-stu-id="433fe-136">You can specify the following constants with this flag:</span></span>

</dd> <dt>

<span data-ttu-id="433fe-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>Процедура рисования в MCI \_ AVI \_ сетвидео \_ \_</span><span class="sxs-lookup"><span data-stu-id="433fe-137"><span id="MCI_AVI_SETVIDEO_DRAW_PROCEDURE"></span><span id="mci_avi_setvideo_draw_procedure"></span>MCI\_AVI\_SETVIDEO\_DRAW\_PROCEDURE</span></span>
</dt> <dd>

<span data-ttu-id="433fe-138">Новый адрес процедуры рисования задается в элементе **дввалуе** структуры, определенной параметром *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-138">A new drawing procedure address is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-139">Новую процедуру рисования можно указать только в том случае, если устройство бездействует.</span><span class="sxs-lookup"><span data-stu-id="433fe-139">You can specify a new drawing procedure only when the device is idle.</span></span> <span data-ttu-id="433fe-140">Этот флаг распознается только драйвером МЦИАВИ Digital-Video.</span><span class="sxs-lookup"><span data-stu-id="433fe-140">This flag is recognized only by the MCIAVI digital-video driver.</span></span> <span data-ttu-id="433fe-141">Эквивалент этого флага в интерфейсе командной строки не существует.</span><span class="sxs-lookup"><span data-stu-id="433fe-141">There is no equivalent to this flag in the string command interface.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>\_ \_ \_ цвет палитры MCI AVI сетвидео \_</span><span class="sxs-lookup"><span data-stu-id="433fe-142"><span id="MCI_AVI_SETVIDEO_PALETTE_COLOR"></span><span id="mci_avi_setvideo_palette_color"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="433fe-143">Новый цвет палитры указан в элементах **двовер** и **дввалуе** структуры, идентифицируемой *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-143">A new palette color is specified in the **dwOver** and **dwValue** members of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-144">Элемент **двовер** указывает индекс палитры изменяемого цвета, а элемент **дввалуе** задает новый цвет в виде значения RGB.</span><span class="sxs-lookup"><span data-stu-id="433fe-144">The **dwOver** member specifies the palette index of the color to be changed and the **dwValue** member specifies the new color, as an RGB value.</span></span> <span data-ttu-id="433fe-145">При использовании этой константы необходимо также указать флаги **\_ ДГВ MCI \_ сетвидео \_** и **MCI \_ ДГВ \_ сетвидео \_** с **\_ \_ \_ элементом MCI ДГВ сетвидео** .</span><span class="sxs-lookup"><span data-stu-id="433fe-145">You must also specify the **MCI\_DGV\_SETVIDEO\_OVER** and **MCI\_DGV\_SETVIDEO\_VALUE** flags with **MCI\_DGV\_SETVIDEO\_ITEM** when you use this constant.</span></span> <span data-ttu-id="433fe-146">Этот флаг распознается только драйвером МЦИАВИ Digital-Video.</span><span class="sxs-lookup"><span data-stu-id="433fe-146">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>\_ \_ Палитра MCI AVI сетвидео \_ \_ полутона</span><span class="sxs-lookup"><span data-stu-id="433fe-147"><span id="MCI_AVI_SETVIDEO_PALETTE_HALFTONE"></span><span id="mci_avi_setvideo_palette_halftone"></span>MCI\_AVI\_SETVIDEO\_PALETTE\_HALFTONE</span></span>
</dt> <dd>

<span data-ttu-id="433fe-148">Указывает, что вместо палитры по умолчанию следует использовать палитру полутонов.</span><span class="sxs-lookup"><span data-stu-id="433fe-148">Indicates that the halftone palette should be used, instead of the default palette.</span></span> <span data-ttu-id="433fe-149">Этот флаг распознается только драйвером МЦИАВИ Digital-Video.</span><span class="sxs-lookup"><span data-stu-id="433fe-149">This flag is recognized only by the MCIAVI digital-video driver.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI \_ ДГВ \_ сетвидео \_ битсперпел</span><span class="sxs-lookup"><span data-stu-id="433fe-150"><span id="MCI_DGV_SETVIDEO_BITSPERPEL"></span><span id="mci_dgv_setvideo_bitsperpel"></span>MCI\_DGV\_SETVIDEO\_BITSPERPEL</span></span>
</dt> <dd>

<span data-ttu-id="433fe-151">Число битов на пиксель указывается в элементе **дввалуе** структуры, определенной параметром *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-151">The number of bits per pixel is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-152">Число битов на пиксель используется для сохранения записанных или записанных данных.</span><span class="sxs-lookup"><span data-stu-id="433fe-152">The number of bits per pixel is used for saving captured or recorded data</span></span>

</dd> <dt>

<span data-ttu-id="433fe-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>\_яркость MCI ДГВ \_ сетвидео \_</span><span class="sxs-lookup"><span data-stu-id="433fe-153"><span id="MCI_DGV_SETVIDEO_BRIGHTNESS"></span><span id="mci_dgv_setvideo_brightness"></span>MCI\_DGV\_SETVIDEO\_BRIGHTNESS</span></span>
</dt> <dd>

<span data-ttu-id="433fe-154">Уровень яркости видео указывается в качестве фактора в элементе **дввалуе** структуры, идентифицируемой *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-154">The video brightness level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>\_ \_ Цвет сетвидео MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="433fe-155"><span id="MCI_DGV_SETVIDEO_COLOR"></span><span id="mci_dgv_setvideo_color"></span>MCI\_DGV\_SETVIDEO\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="433fe-156">Уровень насыщенности видео определяется как фактор в элементе **дввалуе** структуры, идентифицируемой *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-156">The video color saturation level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>\_ \_ контрастность MCI ДГВ сетвидео \_</span><span class="sxs-lookup"><span data-stu-id="433fe-157"><span id="MCI_DGV_SETVIDEO_CONTRAST"></span><span id="mci_dgv_setvideo_contrast"></span>MCI\_DGV\_SETVIDEO\_CONTRAST</span></span>
</dt> <dd>

<span data-ttu-id="433fe-158">Уровень контрастности видео указывается в качестве фактора в элементе **дввалуе** структуры, идентифицируемой *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-158">The video contrast level is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>\_ \_ \_ Частота кадров MCI ДГВ \_ сетвидео</span><span class="sxs-lookup"><span data-stu-id="433fe-159"><span id="MCI_DGV_SETVIDEO_FRAME_RATE"></span><span id="mci_dgv_setvideo_frame_rate"></span>MCI\_DGV\_SETVIDEO\_FRAME\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="433fe-160">Частота кадров указывается в элементе **дввалуе** структуры, определенной параметром *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-160">A frame rate is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-161">Частота указана в единицах кадров в секунду, раз в 1000.</span><span class="sxs-lookup"><span data-stu-id="433fe-161">The rate is specified in units of frames per second times 1000.</span></span> <span data-ttu-id="433fe-162">Например, 29,97 кадров в секунду указывается как 29970.</span><span class="sxs-lookup"><span data-stu-id="433fe-162">For example, 29.97 frames per second is specified as 29970.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>\_ \_ гамма-сетвидео MCI ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="433fe-163"><span id="MCI_DGV_SETVIDEO_GAMMA"></span><span id="mci_dgv_setvideo_gamma"></span>MCI\_DGV\_SETVIDEO\_GAMMA</span></span>
</dt> <dd>

<span data-ttu-id="433fe-164">Значение экспоненты гамма-коррекции задается в элементе **дввалуе** структуры, определенной параметром *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-164">A gamma correction exponent value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-165">Гамма-коррекция настраивает сопоставление интенсивности, закодированной в источнике презентации, и отображаемую яркость.</span><span class="sxs-lookup"><span data-stu-id="433fe-165">Gamma correction adjusts the mapping between the intensity encoded in the presentation source and the displayed brightness.</span></span> <span data-ttu-id="433fe-166">Значением является экспонента, умноженная на 1000.</span><span class="sxs-lookup"><span data-stu-id="433fe-166">The value is the exponent multiplied by 1000.</span></span> <span data-ttu-id="433fe-167">Например, 2200 указывает на степень 2,2.</span><span class="sxs-lookup"><span data-stu-id="433fe-167">For example, 2200 indicates an exponent of 2.2.</span></span> <span data-ttu-id="433fe-168">Значение 1000 указывает экспоненту 1, которая не выполняет гамма-коррекцию.</span><span class="sxs-lookup"><span data-stu-id="433fe-168">A value of 1000 indicates an exponent of 1, which applies no gamma correction.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>\_ \_ \_ Цвет ключа MCI ДГВ \_ сетвидео</span><span class="sxs-lookup"><span data-stu-id="433fe-169"><span id="MCI_DGV_SETVIDEO_KEY_COLOR"></span><span id="mci_dgv_setvideo_key_color"></span>MCI\_DGV\_SETVIDEO\_KEY\_COLOR</span></span>
</dt> <dd>

<span data-ttu-id="433fe-170">Ключевой цвет задается в элементе **дввалуе** структуры, определенной параметром *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-170">A key color is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-171">Ключевой цвет — это значение RGB.</span><span class="sxs-lookup"><span data-stu-id="433fe-171">The key color is an RGB value.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>\_ \_ \_ индекс ключа сетвидео MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="433fe-172"><span id="MCI_DGV_SETVIDEO_KEY_INDEX"></span><span id="mci_dgv_setvideo_key_index"></span>MCI\_DGV\_SETVIDEO\_KEY\_INDEX</span></span>
</dt> <dd>

<span data-ttu-id="433fe-173">Значение индекса ключа указывается в элементе **дввалуе** структуры, определенной параметром *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-173">A key index value is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-174">Параметр индекса является физическим индексом палитры.</span><span class="sxs-lookup"><span data-stu-id="433fe-174">The index parameter is a physical palette index.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI \_ ДГВ \_ сетвидео \_ палхандле</span><span class="sxs-lookup"><span data-stu-id="433fe-175"><span id="MCI_DGV_SETVIDEO_PALHANDLE"></span><span id="mci_dgv_setvideo_palhandle"></span>MCI\_DGV\_SETVIDEO\_PALHANDLE</span></span>
</dt> <dd>

<span data-ttu-id="433fe-176">В элементе **дввалуе** структуры, идентифицируемой *лпсетвидео*, указывается маркер палитры.</span><span class="sxs-lookup"><span data-stu-id="433fe-176">A palette handle is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-177">Маркер палитры содержится в слове нижнего порядка.</span><span class="sxs-lookup"><span data-stu-id="433fe-177">The palette handle is contained in the low-order word.</span></span> <span data-ttu-id="433fe-178">Устройствам с цифровыми видео не следует освобождать палитру, переданную с помощью этой команды.</span><span class="sxs-lookup"><span data-stu-id="433fe-178">Digital-video devices should not free the palette passed with this command.</span></span> <span data-ttu-id="433fe-179">Приложения должны освободить его после закрытия устройства.</span><span class="sxs-lookup"><span data-stu-id="433fe-179">Applications should free it after they close the device.</span></span> <span data-ttu-id="433fe-180">Этот флаг поддерживается только устройствами, которые используют палитры.</span><span class="sxs-lookup"><span data-stu-id="433fe-180">This flag is supported only by devices that use palettes.</span></span> <span data-ttu-id="433fe-181">Если этот заданный маркер палитры равен нулю, используется палитра по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="433fe-181">If this specified palette handle is zero, then the default palette is used.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>\_резкость ДГВ \_ СЕТВИДЕОа MCI \_</span><span class="sxs-lookup"><span data-stu-id="433fe-182"><span id="MCI_DGV_SETVIDEO_SHARPNESS"></span><span id="mci_dgv_setvideo_sharpness"></span>MCI\_DGV\_SETVIDEO\_SHARPNESS</span></span>
</dt> <dd>

<span data-ttu-id="433fe-183">Значение четкости задается в виде коэффициента в элементе **дввалуе** структуры, определенной *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-183">A video sharpness value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>\_ \_ источник сетвидео MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="433fe-184"><span id="MCI_DGV_SETVIDEO_SOURCE"></span><span id="mci_dgv_setvideo_source"></span>MCI\_DGV\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="433fe-185">Константа, указывающая источник входных данных видео, указывается в элементе **дввалуе** структуры, определенной параметром *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-185">A constant specifying the source of the video input is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-186">Определены следующие константы:</span><span class="sxs-lookup"><span data-stu-id="433fe-186">The following constants are defined:</span></span>

-   <span data-ttu-id="433fe-187">**MCI \_ ДГВ \_ сетвидео \_ src \_ NTSC**: NTSC телевидение.</span><span class="sxs-lookup"><span data-stu-id="433fe-187">**MCI\_DGV\_SETVIDEO\_SRC\_NTSC**: NTSC television.</span></span>
-   <span data-ttu-id="433fe-188">MCI \_ ДГВ \_ сетвидео \_ src \_ PAL: PAL телевидение.</span><span class="sxs-lookup"><span data-stu-id="433fe-188">MCI\_DGV\_SETVIDEO\_SRC\_PAL: PAL television.</span></span>
-   <span data-ttu-id="433fe-189">MCI \_ ДГВ \_ сетвидео \_ src \_ RGB: видео в формате RGB.</span><span class="sxs-lookup"><span data-stu-id="433fe-189">MCI\_DGV\_SETVIDEO\_SRC\_RGB: RGB video.</span></span>
-   <span data-ttu-id="433fe-190">MCI \_ ДГВ \_ сетвидео \_ src \_ СЕКАМ: СЕКАМ телевидение.</span><span class="sxs-lookup"><span data-stu-id="433fe-190">MCI\_DGV\_SETVIDEO\_SRC\_SECAM: SECAM television.</span></span>
-   <span data-ttu-id="433fe-191">MCI \_ ДГВ \_ сетвидео \_ src \_ Свидео: S-Video.</span><span class="sxs-lookup"><span data-stu-id="433fe-191">MCI\_DGV\_SETVIDEO\_SRC\_SVIDEO: S-Video.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>\_ \_ поток сетвидео MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="433fe-192"><span id="MCI_DGV_SETVIDEO_STREAM"></span><span id="mci_dgv_setvideo_stream"></span>MCI\_DGV\_SETVIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="433fe-193">Поток видео задается в элементе **дввалуе** структуры, определяемой *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-193">A video stream is specified in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-194">Целочисленное значение указывает поток видео, воспроизводимый из рабочей области.</span><span class="sxs-lookup"><span data-stu-id="433fe-194">The integer value specifies the video stream played back from the workspace.</span></span> <span data-ttu-id="433fe-195">Если поток не указан и формат файла не определяет поток по умолчанию, то будет воспроизведен первый физически чередующийся поток видео.</span><span class="sxs-lookup"><span data-stu-id="433fe-195">If the stream is not specified and the file format does not define a default stream, the first physically interleaved video stream is played.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>\_оттенок \_ сетвидео MCI ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="433fe-196"><span id="MCI_DGV_SETVIDEO_TINT"></span><span id="mci_dgv_setvideo_tint"></span>MCI\_DGV\_SETVIDEO\_TINT</span></span>
</dt> <dd>

<span data-ttu-id="433fe-197">Значение оттенка видео указывается как фактор в элементе **дввалуе** структуры, идентифицируемой *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-197">A video tint value is specified as a factor in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-198">Как правило, эта корректировка моделируется после управления оттенок множества наборов цветовых телевизоров с 250, определенными зеленым цветом, 750, определенными красным цветом, а 0 (или 1000) — синим.</span><span class="sxs-lookup"><span data-stu-id="433fe-198">Typically, this adjustment is modeled after the tint control of many color television sets, with 250 defined as green, 750 defined as red, and 0 (or 1000) defined as blue.</span></span> <span data-ttu-id="433fe-199">Номинальное значение всегда равно 500.</span><span class="sxs-lookup"><span data-stu-id="433fe-199">The nominal value is always 500.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>\_ \_ выходные данные сетвидео MCI ДГВ \_</span><span class="sxs-lookup"><span data-stu-id="433fe-200"><span id="MCI_DGV_SETVIDEO_OUTPUT"></span><span id="mci_dgv_setvideo_output"></span>MCI\_DGV\_SETVIDEO\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="433fe-201">**\_ ДГВ \_ сетвидео \_ яркость**, **MCI \_ ДГВ \_ сетвидео \_**, MCI **\_ ДГВ \_ сетвидео \_**,, MCI **\_ ДГВ \_ сетвидео \_ гамма**, **MCI \_ ДГВ \_ сетвидео \_ резкость**, или элемент **MCI \_ ДГВ \_ сетвидео \_ оттенок** , изменяется так, чтобы он влиял только на отображаемый сигнал, а не на записи.</span><span class="sxs-lookup"><span data-stu-id="433fe-201">The **MCI\_DGV\_SETVIDEO\_BRIGHTNESS**, **MCI\_DGV\_SETVIDEO\_COLOR**, **MCI\_DGV\_SETVIDEO\_CONTRAST**, **MCI\_DGV\_SETVIDEO\_GAMMA**, **MCI\_DGV\_SETVIDEO\_SHARPNESS**, or **MCI\_DGV\_SETVIDEO\_TINT** flag is modified so that it affects only the displayed signal and not what is recorded.</span></span> <span data-ttu-id="433fe-202">По возможности это значение по умолчанию при мониторинге файла.</span><span class="sxs-lookup"><span data-stu-id="433fe-202">If possible, this is the default when monitoring a file.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI \_ ДГВ \_ сетвидео \_</span><span class="sxs-lookup"><span data-stu-id="433fe-203"><span id="MCI_DGV_SETVIDEO_OVER"></span><span id="mci_dgv_setvideo_over"></span>MCI\_DGV\_SETVIDEO\_OVER</span></span>
</dt> <dd>

<span data-ttu-id="433fe-204">Параметр длины перехода включается в элемент **двовер** структуры, идентифицируемой *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-204">A transition length parameter is included in the **dwOver** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-205">Длина перехода определяет время (в текущем формате времени), которое должно потребоваться для внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="433fe-205">The transition length specifies how long (in the current time format) it should take to make a change.</span></span> <span data-ttu-id="433fe-206">Если этот флаг не используется, изменение выполняется немедленно.</span><span class="sxs-lookup"><span data-stu-id="433fe-206">If this flag is not used, the change occurs immediately.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>\_ \_ качество сетвидео MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="433fe-207"><span id="MCI_DGV_SETVIDEO_QUALITY"></span><span id="mci_dgv_setvideo_quality"></span>MCI\_DGV\_SETVIDEO\_QUALITY</span></span>
</dt> <dd>

<span data-ttu-id="433fe-208">Элемент **лпстркуалити** структуры, идентифицируемой *лпсетвидео* , содержит адрес буфера, описывающего качество видео.</span><span class="sxs-lookup"><span data-stu-id="433fe-208">The **lpstrQuality** member of the structure identified by *lpSetVideo* contains an address of a buffer describing the video quality.</span></span> <span data-ttu-id="433fe-209">Текстовая строка в буфере определяет характеристики алгоритма сжатия видео.</span><span class="sxs-lookup"><span data-stu-id="433fe-209">A text-string in the buffer specifies the characteristics of the video compression algorithm.</span></span>

<span data-ttu-id="433fe-210">Для выбора дескриптора качества для указанного алгоритма можно использовать флаг **\_ ДГВ \_ сетвидео \_ в MCI** .</span><span class="sxs-lookup"><span data-stu-id="433fe-210">The **MCI\_DGV\_SETVIDEO\_ALG** flag can be used to select a quality descriptor for the specified algorithm.</span></span> <span data-ttu-id="433fe-211">Если этот флаг опущен, используется текущий алгоритм.</span><span class="sxs-lookup"><span data-stu-id="433fe-211">If this flag is omitted, then the current algorithm is used.</span></span>

<span data-ttu-id="433fe-212">Доступные имена алгоритмов и дескрипторов зависят от устройства.</span><span class="sxs-lookup"><span data-stu-id="433fe-212">The algorithms and descriptor names available depend on the device.</span></span> <span data-ttu-id="433fe-213">Каждое устройство предоставляет документацию по доступным алгоритмам и описание применимых имен дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="433fe-213">Each device supplies documentation for the available algorithms and a description of the applicable descriptor names.</span></span> <span data-ttu-id="433fe-214">Команда [ \_ качества MCI](mci-quality.md) может определять дополнительные имена дескрипторов.</span><span class="sxs-lookup"><span data-stu-id="433fe-214">The [MCI\_QUALITY](mci-quality.md) command can define additional descriptor names.</span></span> <span data-ttu-id="433fe-215">Все устройства поддерживают дескрипторы «Low», «Medium» и «High».</span><span class="sxs-lookup"><span data-stu-id="433fe-215">All devices support the descriptors "low", "medium", and "high".</span></span> <span data-ttu-id="433fe-216">Значение по умолчанию — Специальный драйвер.</span><span class="sxs-lookup"><span data-stu-id="433fe-216">The default is driver specific.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>\_ \_ запись сетвидео MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="433fe-217"><span id="MCI_DGV_SETVIDEO_RECORD"></span><span id="mci_dgv_setvideo_record"></span>MCI\_DGV\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="433fe-218">Указывает, включает ли запись видео или исключает их.</span><span class="sxs-lookup"><span data-stu-id="433fe-218">Specifies whether recording includes or excludes video data.</span></span> <span data-ttu-id="433fe-219">Если в сочетании с **MCI \_ установлено \_ On**, данные видео записываются.</span><span class="sxs-lookup"><span data-stu-id="433fe-219">When combined with **MCI\_SET\_ON**, video data is recorded.</span></span> <span data-ttu-id="433fe-220">Если в сочетании с **MCI \_ установлено значение \_ Off**, данные видео исключаются.</span><span class="sxs-lookup"><span data-stu-id="433fe-220">When combined with **MCI\_SET\_OFF**, video data is excluded.</span></span> <span data-ttu-id="433fe-221">По умолчанию включаются данные видео.</span><span class="sxs-lookup"><span data-stu-id="433fe-221">The default includes video data.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>\_ \_ \_ номер src ДГВ сетвидео \_ MCI</span><span class="sxs-lookup"><span data-stu-id="433fe-222"><span id="MCI_DGV_SETVIDEO_SRC_NUMBER"></span><span id="mci_dgv_setvideo_src_number"></span>MCI\_DGV\_SETVIDEO\_SRC\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="433fe-223">Число для источника видео указывается в элементе **двсаурценумбер** структуры, определенной параметром *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-223">A number for the video source is specified in the **dwSourceNumber** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-224">Если имеется более одного входного типа, заданного в **\_ ДГВ \_ сетвидео \_ MCI**, значение выбирает входные данные.</span><span class="sxs-lookup"><span data-stu-id="433fe-224">If there is more than one input of the type specified by **MCI\_DGV\_SETVIDEO\_VALUE**, the value selects the input.</span></span> <span data-ttu-id="433fe-225">Этот флаг всегда должен использоваться с **\_ \_ \_ источником сетвидео MCI ДГВ**.</span><span class="sxs-lookup"><span data-stu-id="433fe-225">This flag must always be used with **MCI\_DGV\_SETVIDEO\_SOURCE**.</span></span> <span data-ttu-id="433fe-226">Однако **Если \_ \_ \_ значение MCI ДГВ сетвидео** опущено, то указанный исходный номер указывает на абсолютный источник, который будет использоваться в качестве указанного в команде [MCI \_ List](mci-list.md) .</span><span class="sxs-lookup"><span data-stu-id="433fe-226">If **MCI\_DGV\_SETVIDEO\_VALUE** is omitted, however, the specified source number indicates the absolute source to use as specified in the [MCI\_LIST](mci-list.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI \_ ДГВ \_ сетвидео \_ по-прежнему</span><span class="sxs-lookup"><span data-stu-id="433fe-227"><span id="MCI_DGV_SETVIDEO_STILL"></span><span id="mci_dgv_setvideo_still"></span>MCI\_DGV\_SETVIDEO\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="433fe-228">Указанное имя алгоритма или значения качества относятся к изображениям.</span><span class="sxs-lookup"><span data-stu-id="433fe-228">The algorithm name or quality value specified applies to still images.</span></span>

<span data-ttu-id="433fe-229">Каждый драйвер устройства должен поддерживать алгоритм "None", что означает отсутствие сжатия.</span><span class="sxs-lookup"><span data-stu-id="433fe-229">Every device driver must support an algorithm of "none", which means no compression.</span></span> <span data-ttu-id="433fe-230">Это значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="433fe-230">This is the default.</span></span> <span data-ttu-id="433fe-231">В этом случае устройства Digital-Video сохраняют изображения по-прежнему как аппаратно-независимые точечные рисунки (DIB).</span><span class="sxs-lookup"><span data-stu-id="433fe-231">In this case, digital-video devices save still images as RGB device-independent bitmaps (DIBs).</span></span>

</dd> <dt>

<span data-ttu-id="433fe-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>\_ \_ значение сетвидео MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="433fe-232"><span id="MCI_DGV_SETVIDEO_VALUE"></span><span id="mci_dgv_setvideo_value"></span>MCI\_DGV\_SETVIDEO\_VALUE</span></span>
</dt> <dd>

<span data-ttu-id="433fe-233">Значение включается в элемент **дввалуе** структуры, идентифицируемой *лпсетвидео*.</span><span class="sxs-lookup"><span data-stu-id="433fe-233">A value is included in the **dwValue** member of the structure identified by *lpSetVideo*.</span></span> <span data-ttu-id="433fe-234">Значение значения задается флагом **\_ \_ \_ элемента MCI ДГВ сетвидео** .</span><span class="sxs-lookup"><span data-stu-id="433fe-234">The meaning of the value is specified by the **MCI\_DGV\_SETVIDEO\_ITEM** flag.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ установлен \_</span><span class="sxs-lookup"><span data-stu-id="433fe-235"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="433fe-236">Отключает вывод видео.</span><span class="sxs-lookup"><span data-stu-id="433fe-236">Disables video output.</span></span> <span data-ttu-id="433fe-237">Для устройств с цифровыми видео. при отключении видео устанавливаются Пиксели в прямоугольнике назначения, определяемые командой [MCI \_ ](mci-put.md) (или ее значением по умолчанию, областью действия клиента текущего окна) сплошным цветом, но не влияет на буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="433fe-237">For digital-video devices, disabling video sets the pixels in the destination rectangle defined by the [MCI\_PUT](mci-put.md) command (or its default, the client region of the current window) to a solid color, but it has no effect on the frame buffer.</span></span> <span data-ttu-id="433fe-238">При необходимости можно скрыть окно с помощью [команды \_ окна MCI](mci-window.md) .</span><span class="sxs-lookup"><span data-stu-id="433fe-238">You can hide the window with the [MCI\_WINDOW](mci-window.md) command if desired.</span></span> <span data-ttu-id="433fe-239">Источник видео, будь то Рабочая область или внешние входные данные, может продолжать хранить новые изображения в буфере кадров, но они не отображаются, пока видео не будет включено.</span><span class="sxs-lookup"><span data-stu-id="433fe-239">The source of video, whether it's the workspace or an external input, might continue to store new images in the frame buffer, but they are not displayed until the video is enabled.</span></span> <span data-ttu-id="433fe-240">Хотя приложения должны использовать команду MCI \_ сетвидео для управления этой функцией, устройства цифрового видео по-прежнему должны поддерживать этот флаг.</span><span class="sxs-lookup"><span data-stu-id="433fe-240">While applications should use the MCI\_SETVIDEO command to control this function, digital-video devices must still support this flag.</span></span> <span data-ttu-id="433fe-241">Значение по умолчанию после открытия.</span><span class="sxs-lookup"><span data-stu-id="433fe-241">The default value after an open is on.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ задан \_ на</span><span class="sxs-lookup"><span data-stu-id="433fe-242"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="433fe-243">Включает вывод видео.</span><span class="sxs-lookup"><span data-stu-id="433fe-243">Enables video output.</span></span>

</dd> </dl>

<span data-ttu-id="433fe-244">Для устройств с цифровыми видео параметр *лпсетвидео* указывает на структуру [**MCI \_ ДГВ \_ сетвидео \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) .</span><span class="sxs-lookup"><span data-stu-id="433fe-244">For digital-video devices, the *lpSetVideo* parameter points to an [**MCI\_DGV\_SETVIDEO\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_setvideo_parmsa) structure.</span></span>

<span data-ttu-id="433fe-245">Следующие дополнительные флаги используются с типом устройства "видеомагнитофон":</span><span class="sxs-lookup"><span data-stu-id="433fe-245">The following additional flags are used with the "vcr" device type:</span></span>

<dl> <dt>

<span data-ttu-id="433fe-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>\_ \_ запись СЕТВИДЕО видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="433fe-246"><span id="MCI_VCR_SETVIDEO_RECORD"></span><span id="mci_vcr_setvideo_record"></span>MCI\_VCR\_SETVIDEO\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="433fe-247">Задает включение или выключение записи видео.</span><span class="sxs-lookup"><span data-stu-id="433fe-247">Sets the video recording to on or off.</span></span> <span data-ttu-id="433fe-248">Используется в сочетании с одним из следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="433fe-248">Used in conjunction with one of following flags:</span></span>

-   <span data-ttu-id="433fe-249">**MCI \_ Задайте значение \_ On**.</span><span class="sxs-lookup"><span data-stu-id="433fe-249">**MCI\_SET\_ON**.</span></span> <span data-ttu-id="433fe-250">Запись видео в.</span><span class="sxs-lookup"><span data-stu-id="433fe-250">Video recording on.</span></span>
-   <span data-ttu-id="433fe-251">**MCI \_ Установите значение \_ Off**.</span><span class="sxs-lookup"><span data-stu-id="433fe-251">**MCI\_SET\_OFF**.</span></span> <span data-ttu-id="433fe-252">Запись видео отключена.</span><span class="sxs-lookup"><span data-stu-id="433fe-252">Video recording off.</span></span> <span data-ttu-id="433fe-253">Для отключения записи видео может потребоваться отключить запись сборки (с помощью команды [MCI с \_](mci-set.md) установленным флагом **\_ \_ \_ сбора \_ записей видеомагнитофона видеомагнитофонов MCI** ).</span><span class="sxs-lookup"><span data-stu-id="433fe-253">It might be necessary to first turn off the assemble recording (using the [MCI\_SET](mci-set.md) command with the **MCI\_VCR\_SET\_ASSEMBLE\_RECORD** flag set to off) before the video recording can be turned off.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>\_направление MCI</span><span class="sxs-lookup"><span data-stu-id="433fe-254"><span id="MCI_TRACK"></span><span id="mci_track"></span>MCI\_TRACK</span></span>
</dt> <dd>

<span data-ttu-id="433fe-255">Элемент **двтракк** структуры, определяемой параметром *лпсетвидео* , указывает, на какую запись влияет команда.</span><span class="sxs-lookup"><span data-stu-id="433fe-255">The **dwTrack** member of the structure identified by *lpSetVideo* specifies which track is affected by the command.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>\_ \_ источник СЕТВИДЕО видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="433fe-256"><span id="MCI_VCR_SETVIDEO_SOURCE"></span><span id="mci_vcr_setvideo_source"></span>MCI\_VCR\_SETVIDEO\_SOURCE</span></span>
</dt> <dd>

<span data-ttu-id="433fe-257">Задает источник видео и должен использоваться с флагом **\_ \_ сетвидео \_ видеомагнитофона MCI** .</span><span class="sxs-lookup"><span data-stu-id="433fe-257">Sets the video source, and must be used with the **MCI\_VCR\_SETVIDEO\_TO** flag.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>\_ \_ монитор СЕТВИДЕО видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="433fe-258"><span id="MCI_VCR_SETVIDEO_MONITOR"></span><span id="mci_vcr_setvideo_monitor"></span>MCI\_VCR\_SETVIDEO\_MONITOR</span></span>
</dt> <dd>

<span data-ttu-id="433fe-259">Задает монитор источника видео и должен использоваться с \_ \_ флагом СЕТВИДЕО видеомагнитофона MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="433fe-259">Sets the video source monitor, and must be used with the MCI\_VCR\_SETVIDEO\_TO flag.</span></span>

</dd> <dt>

<span data-ttu-id="433fe-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>\_сетвидео ВИДЕОМАГНИТОФОН \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="433fe-260"><span id="MCI_VCR_SETVIDEO_TO"></span><span id="mci_vcr_setvideo_to"></span>MCI\_VCR\_SETVIDEO\_TO</span></span>
</dt> <dd>

<span data-ttu-id="433fe-261">Элемент **двто** структуры, идентифицируемой *лпсетвидео* , содержит одну из следующих констант:</span><span class="sxs-lookup"><span data-stu-id="433fe-261">The **dwTo** member of the structure identified by *lpSetVideo* contains one of the following constants:</span></span>

<dl> <dd><span data-ttu-id="433fe-262">**средство \_ \_ \_ настройки типа src \_ видеомагнитофона MCI**</span><span class="sxs-lookup"><span data-stu-id="433fe-262">**MCI\_VCR\_SRC\_TYPE\_TUNER**</span></span></dd> <dd><span data-ttu-id="433fe-263">**\_ \_ \_ Строка типа src видеомагнитофона \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="433fe-263">**MCI\_VCR\_SRC\_TYPE\_LINE**</span></span></dd> <dd><span data-ttu-id="433fe-264">**\_ \_ \_ дополнительный тип src видеомагнитофона \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="433fe-264">**MCI\_VCR\_SRC\_TYPE\_AUX**</span></span></dd> <dd><span data-ttu-id="433fe-265">**\_ \_ тип src видеомагнитофона MCI \_ типа \_ универсальный**</span><span class="sxs-lookup"><span data-stu-id="433fe-265">**MCI\_VCR\_SRC\_TYPE\_GENERIC**</span></span></dd> <dd><span data-ttu-id="433fe-266">**\_выкл. \_ \_ тип src видеомагнитофона MCI \_**</span><span class="sxs-lookup"><span data-stu-id="433fe-266">**MCI\_VCR\_SRC\_TYPE\_MUTE**</span></span></dd> <dd><span data-ttu-id="433fe-267">**\_ \_ \_ выходные данные типа src видеомагнитофона MCI \_**</span><span class="sxs-lookup"><span data-stu-id="433fe-267">**MCI\_VCR\_SRC\_TYPE\_OUTPUT**</span></span></dd> <dd><span data-ttu-id="433fe-268">**\_ \_ тип src видеомагнитофона MCI \_ типа \_ RGB**</span><span class="sxs-lookup"><span data-stu-id="433fe-268">**MCI\_VCR\_SRC\_TYPE\_RGB**</span></span></dd> <dd><span data-ttu-id="433fe-269">**\_ \_ номер СЕТВИДЕО видеомагнитофона \_ MCI**</span><span class="sxs-lookup"><span data-stu-id="433fe-269">**MCI\_VCR\_SETVIDEO\_NUMBER**</span></span></dd> </dl>

<span data-ttu-id="433fe-270">Элемент **двнумбер** структуры, идентифицируемой *лпсетвидео* , содержит входные данные видео (для типа, указанного в элементе **двто** ) для использования.</span><span class="sxs-lookup"><span data-stu-id="433fe-270">The **dwNumber** member of the structure identified by *lpSetVideo* contains the video input (of the type specified in the **dwTo** member) to use.</span></span>

</dd> </dl>

<span data-ttu-id="433fe-271">Для устройств ВИДЕОМАГНИТОФОНА параметр *лпсетвидео* указывает на структуру [**\_ видеомагнитофона MCI \_ сетвидео \_ пармс**](mci-vcr-setvideo-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="433fe-271">For VCR devices, the *lpSetVideo* parameter points to an [**MCI\_VCR\_SETVIDEO\_PARMS**](mci-vcr-setvideo-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="433fe-272">Требования</span><span class="sxs-lookup"><span data-stu-id="433fe-272">Requirements</span></span>



| <span data-ttu-id="433fe-273">Требование</span><span class="sxs-lookup"><span data-stu-id="433fe-273">Requirement</span></span> | <span data-ttu-id="433fe-274">Значение</span><span class="sxs-lookup"><span data-stu-id="433fe-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="433fe-275">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="433fe-275">Minimum supported client</span></span><br/> | <span data-ttu-id="433fe-276">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="433fe-276">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="433fe-277">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="433fe-277">Minimum supported server</span></span><br/> | <span data-ttu-id="433fe-278">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="433fe-278">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="433fe-279">Заголовок</span><span class="sxs-lookup"><span data-stu-id="433fe-279">Header</span></span><br/>                   | <dl> <span data-ttu-id="433fe-280"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="433fe-280"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="433fe-281">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="433fe-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="433fe-282">MCI</span><span class="sxs-lookup"><span data-stu-id="433fe-282">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="433fe-283">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="433fe-283">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

