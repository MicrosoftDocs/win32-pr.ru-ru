---
title: Команда MCI_COPY (Ммсистем. h)
description: Команда MCI \_ Copy копирует данные в буфер обмена. Устройство Digital-Video распознает эту команду.
ms.assetid: 41807920-3312-4cdb-82e6-6ab4b9b35162
keywords:
- MCI_COPY команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_COPY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4c27950b9599d0b565b982eb59755e4d3f2ea65
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988715"
---
# <a name="mci_copy-command"></a><span data-ttu-id="ea9a0-105">\_Команда копирования MCI</span><span class="sxs-lookup"><span data-stu-id="ea9a0-105">MCI\_COPY command</span></span>

<span data-ttu-id="ea9a0-106">Команда MCI \_ Copy копирует данные в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-106">The MCI\_COPY command copies data to the clipboard.</span></span> <span data-ttu-id="ea9a0-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="ea9a0-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_COPY, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_DGV_COPY_PARMS) lpCopy
);
```



## <a name="parameters"></a><span data-ttu-id="ea9a0-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ea9a0-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea9a0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="ea9a0-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ea9a0-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="ea9a0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="ea9a0-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ea9a0-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="ea9a0-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ea9a0-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="ea9a0-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*лпкопи*</span><span class="sxs-lookup"><span data-stu-id="ea9a0-115"><span id="lpCopy"></span><span id="lpcopy"></span><span id="LPCOPY"></span>*lpCopy*</span></span>
</dt> <dd>

<span data-ttu-id="ea9a0-116">Указатель на структуру [**\_ \_ \_ пармс копирования ДГВ MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) .</span><span class="sxs-lookup"><span data-stu-id="ea9a0-116">Pointer to an [**MCI\_DGV\_COPY\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_copy_parms) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea9a0-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ea9a0-117">Return Value</span></span>

<span data-ttu-id="ea9a0-118">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea9a0-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea9a0-119">Remarks</span></span>

<span data-ttu-id="ea9a0-120">Следующие дополнительные флаги применяются к устройствам цифрового видео:</span><span class="sxs-lookup"><span data-stu-id="ea9a0-120">The following additional flags apply to digital-video devices:</span></span>

<dl> <dt>

<span data-ttu-id="ea9a0-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>\_копирование ДГВ \_ MCI \_ в</span><span class="sxs-lookup"><span data-stu-id="ea9a0-121"><span id="MCI_DGV_COPY_AT"></span><span id="mci_dgv_copy_at"></span>MCI\_DGV\_COPY\_AT</span></span>
</dt> <dd>

<span data-ttu-id="ea9a0-122">Прямоугольник включается в элемент **RC** структуры, идентифицируемой *лпкопи*.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-122">A rectangle is included in the **rc** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="ea9a0-123">Прямоугольник указывает часть каждого копируемого кадра.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-123">The rectangle specifies the portion of each frame to copy.</span></span> <span data-ttu-id="ea9a0-124">Если флаг опущен, \_ то при копировании MCI копируется весь кадр.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-124">If the flag is omitted, MCI\_COPY copies the entire frame.</span></span>

</dd> <dt>

<span data-ttu-id="ea9a0-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>\_ \_ копирование \_ звукового \_ потока MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="ea9a0-125"><span id="MCI_DGV_COPY_AUDIO_STREAM"></span><span id="mci_dgv_copy_audio_stream"></span>MCI\_DGV\_COPY\_AUDIO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="ea9a0-126">Номер звукового потока включается в элемент **дваудиостреам** структуры, определяемой *лпкопи*.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-126">An audio-stream number is included in the **dwAudioStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="ea9a0-127">Если вы используете этот флаг, а также хотите скопировать видео, необходимо также использовать \_ \_ \_ \_ флаг копирования видеопотоков MCI ДГВ.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-127">If you use this flag and also want to copy video, you must also use the MCI\_DGV\_COPY\_VIDEO\_STREAM flag.</span></span> <span data-ttu-id="ea9a0-128">(Если ни один из флагов не указан, копируются данные из всех потоков аудио и видео.)</span><span class="sxs-lookup"><span data-stu-id="ea9a0-128">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="ea9a0-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>\_ \_ копирование \_ \_ видеопотока MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="ea9a0-129"><span id="MCI_DGV_COPY_VIDEO_STREAM"></span><span id="mci_dgv_copy_video_stream"></span>MCI\_DGV\_COPY\_VIDEO\_STREAM</span></span>
</dt> <dd>

<span data-ttu-id="ea9a0-130">Номер видеопотока включается в элемент **дввидеостреам** структуры, определяемой *лпкопи*.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-130">A video-stream number is included in the **dwVideoStream** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="ea9a0-131">Если вы используете этот флаг, а также хотите скопировать аудио, необходимо также использовать \_ \_ флаг копирования звука MCI ДГВ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="ea9a0-131">If you use this flag and also want to copy audio, you must also use the MCI\_DGV\_COPY\_AUDIO\_STREAM flag.</span></span> <span data-ttu-id="ea9a0-132">(Если ни один из флагов не указан, копируются данные из всех потоков аудио и видео.)</span><span class="sxs-lookup"><span data-stu-id="ea9a0-132">(If neither flag is specified, data from all audio and video streams is copied.)</span></span>

</dd> <dt>

<span data-ttu-id="ea9a0-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI \_ из</span><span class="sxs-lookup"><span data-stu-id="ea9a0-133"><span id="MCI_FROM"></span><span id="mci_from"></span>MCI\_FROM</span></span>
</dt> <dd>

<span data-ttu-id="ea9a0-134">Начальное расположение включается в элемент **двфром** структуры, идентифицируемой *лпкопи*.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-134">A starting location is included in the **dwFrom** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="ea9a0-135">Единицы, назначенные значениям позиций, задаются с \_ помощью \_ флага "Установка формата времени MCI" \_ команды [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="ea9a0-135">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the [MCI\_SET](mci-set.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="ea9a0-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI \_ —</span><span class="sxs-lookup"><span data-stu-id="ea9a0-136"><span id="MCI_TO"></span><span id="mci_to"></span>MCI\_TO</span></span>
</dt> <dd>

<span data-ttu-id="ea9a0-137">Конечное расположение включено в элемент **двто** структуры, идентифицируемой *лпкопи*.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-137">An ending location is included in the **dwTo** member of the structure identified by *lpCopy*.</span></span> <span data-ttu-id="ea9a0-138">Единицы, назначенные значениям позиций, задаются с \_ помощью \_ флага "Установка формата времени MCI" \_ \_ команды MCI Set.</span><span class="sxs-lookup"><span data-stu-id="ea9a0-138">The units assigned to the position values are specified with the MCI\_SET\_TIME\_FORMAT flag of the MCI\_SET command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ea9a0-139">Требования</span><span class="sxs-lookup"><span data-stu-id="ea9a0-139">Requirements</span></span>



| <span data-ttu-id="ea9a0-140">Требование</span><span class="sxs-lookup"><span data-stu-id="ea9a0-140">Requirement</span></span> | <span data-ttu-id="ea9a0-141">Значение</span><span class="sxs-lookup"><span data-stu-id="ea9a0-141">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9a0-142">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea9a0-142">Minimum supported client</span></span><br/> | <span data-ttu-id="ea9a0-143">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ea9a0-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="ea9a0-144">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea9a0-144">Minimum supported server</span></span><br/> | <span data-ttu-id="ea9a0-145">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ea9a0-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="ea9a0-146">Заголовок</span><span class="sxs-lookup"><span data-stu-id="ea9a0-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea9a0-147"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea9a0-147"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea9a0-148">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea9a0-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea9a0-149">MCI</span><span class="sxs-lookup"><span data-stu-id="ea9a0-149">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ea9a0-150">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="ea9a0-150">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

