---
title: Команда MCI_CUT (Ммсистем. h)
description: Команда MCI \_ Cut удаляет данные из файла и копирует их в буфер обмена. Устройство Digital-Video распознает эту команду.
ms.assetid: 09bb505b-715a-4393-80f0-e9ba270a8ac1
keywords:
- MCI_CUT команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_CUT
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c564451596f115daca8514785449abf001e224ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988965"
---
# <a name="mci_cut-command"></a><span data-ttu-id="4376b-105">\_Команда MCI Cut</span><span class="sxs-lookup"><span data-stu-id="4376b-105">MCI\_CUT command</span></span>

<span data-ttu-id="4376b-106">Команда MCI \_ Cut удаляет данные из файла и копирует их в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="4376b-106">The MCI\_CUT command removes data from the file and copies it to the clipboard.</span></span> <span data-ttu-id="4376b-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="4376b-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="4376b-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="4376b-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CUT, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_CUT_PARMS) lpCut
);
```



## <a name="parameters"></a><span data-ttu-id="4376b-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4376b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4376b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="4376b-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4376b-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="4376b-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="4376b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="4376b-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4376b-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="4376b-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="4376b-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4376b-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="4376b-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*лпкут*</span><span class="sxs-lookup"><span data-stu-id="4376b-115"><span id="lpCut"></span><span id="lpcut"></span><span id="LPCUT"></span>*lpCut*</span></span>
</dt> <dd>

<span data-ttu-id="4376b-116">Указатель на [**\_ ДГВ \_ Вырезать \_ пармс**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) структуру.</span><span class="sxs-lookup"><span data-stu-id="4376b-116">Pointer to an [**MCI\_DGV\_CUT\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_cut_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4376b-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4376b-117">Return Value</span></span>

<span data-ttu-id="4376b-118">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4376b-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4376b-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4376b-119">Remarks</span></span>

<span data-ttu-id="4376b-120">Следующие дополнительные флаги применяются к устройствам цифрового видео:</span><span class="sxs-lookup"><span data-stu-id="4376b-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="4376b-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>\_ДГВ MCI \_ Вырезать \_ в</span><span class="sxs-lookup"><span data-stu-id="4376b-121"><span id="MCI_DGV_CUT_AT"></span><span id="mci_dgv_cut_at"></span>MCI\_DGV\_CUT\_AT</span></span>
</dt> <dd>

<span data-ttu-id="4376b-122">Прямоугольник включается в элемент **RC** структуры, идентифицируемой *лпкут*.</span><span class="sxs-lookup"><span data-stu-id="4376b-122">A rectangle is included in the **rc** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="4376b-123">Прямоугольник указывает часть каждого кадра для вырезания.</span><span class="sxs-lookup"><span data-stu-id="4376b-123">The rectangle specifies the portion of each frame to cut.</span></span> <span data-ttu-id="4376b-124">Если этот флаг опущен, MCI \_ вырезает весь фрейм целиком.</span><span class="sxs-lookup"><span data-stu-id="4376b-124">If the flag is omitted, MCI\_CUT cuts the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="4376b-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>\_вырезанный АУДИОПОТОК MCI ДГВ \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="4376b-125"><span id="MCI_DGV_CUT_AUDIO_STREAM"></span><span id="mci_dgv_cut_audio_stream"></span>MCI\_DGV\_CUT\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="4376b-126">Номер звукового потока включается в элемент **дваудиостреам** структуры, определяемой *лпкут*.</span><span class="sxs-lookup"><span data-stu-id="4376b-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="4376b-127">Если вы используете этот флаг, а также хотите вырезать видео, необходимо также использовать \_ \_ \_ \_ флаг воспроизведения видеопотока MCI ДГВ.</span><span class="sxs-lookup"><span data-stu-id="4376b-127">If you use this flag and also want to cut video, you must also use the MCI\_DGV\_CUT\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="4376b-128">(Если ни один из флагов не указан, данные из всех потоков аудио и видео обрезаются.)</span><span class="sxs-lookup"><span data-stu-id="4376b-128">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="4376b-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>\_ \_ \_ \_ потоковая передача видео MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="4376b-129"><span id="MCI_DGV_CUT_VIDEO_STREAM"></span><span id="mci_dgv_cut_video_stream"></span>MCI\_DGV\_CUT\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="4376b-130">Номер видеопотока включается в элемент **дввидеостреам** структуры, определяемой *лпкут*.</span><span class="sxs-lookup"><span data-stu-id="4376b-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="4376b-131">Если вы используете этот флаг, а также хотите вырезать звук, необходимо также использовать \_ \_ флаг «вырезать \_ аудио поток» MCI ДГВ \_ .</span><span class="sxs-lookup"><span data-stu-id="4376b-131">If you use this flag and also want to cut audio, you must also use the MCI\_DGV\_CUT\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="4376b-132">(Если ни один из флагов не указан, данные из всех потоков аудио и видео обрезаются.)</span><span class="sxs-lookup"><span data-stu-id="4376b-132">(If neither flag is specified, data from all audio and video streams is cut.)</span></span>

</dd> <dt>

<span data-ttu-id="4376b-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ из</span><span class="sxs-lookup"><span data-stu-id="4376b-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="4376b-134">Начальное расположение включается в элемент **двфром** структуры, идентифицируемой *лпкут*.</span><span class="sxs-lookup"><span data-stu-id="4376b-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="4376b-135">Единицы, назначенные значениям позиций, задаются с \_ помощью \_ флага "Установка формата времени MCI" \_ команды [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="4376b-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="4376b-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ —</span><span class="sxs-lookup"><span data-stu-id="4376b-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="4376b-137">Конечное расположение включено в элемент **двто** структуры, идентифицируемой *лпкут*.</span><span class="sxs-lookup"><span data-stu-id="4376b-137">An ending location is included in the **dwTo** member of the structure identified by *lpCut*.</span></span> <span data-ttu-id="4376b-138">Единицы, назначенные значениям позиций, задаются \_ \_ \_ флагом формата MCI Set Time \_ .</span><span class="sxs-lookup"><span data-stu-id="4376b-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of MCI\_SET.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4376b-139">Требования</span><span class="sxs-lookup"><span data-stu-id="4376b-139">Requirements</span></span>



| <span data-ttu-id="4376b-140">Требование</span><span class="sxs-lookup"><span data-stu-id="4376b-140">Requirement</span></span> | <span data-ttu-id="4376b-141">Значение</span><span class="sxs-lookup"><span data-stu-id="4376b-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4376b-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4376b-142">Minimum supported client</span></span><br/> | <span data-ttu-id="4376b-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4376b-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="4376b-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4376b-144">Minimum supported server</span></span><br/> | <span data-ttu-id="4376b-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4376b-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="4376b-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="4376b-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="4376b-147"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4376b-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4376b-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4376b-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4376b-149">MCI</span><span class="sxs-lookup"><span data-stu-id="4376b-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4376b-150">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="4376b-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

