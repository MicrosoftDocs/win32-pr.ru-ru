---
title: Команда MCI_RESUME (Ммсистем. h)
description: Команда MCI \_ Resume запускает приостановленное устройство для возобновления приостановленной операции.
ms.assetid: 2df712c1-5005-4e89-a439-a651076bbb73
keywords:
- MCI_RESUME команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_RESUME
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd83b6d753cd223235b8b11f2d4b0be4c828ec28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988313"
---
# <a name="mci_resume-command"></a><span data-ttu-id="9d8ce-104">\_Команда возобновления работы с MCI</span><span class="sxs-lookup"><span data-stu-id="9d8ce-104">MCI\_RESUME command</span></span>

<span data-ttu-id="9d8ce-105">Команда MCI \_ Resume запускает приостановленное устройство для возобновления приостановленной операции.</span><span class="sxs-lookup"><span data-stu-id="9d8ce-105">The MCI\_RESUME command causes a paused device to resume the paused operation.</span></span> <span data-ttu-id="9d8ce-106">Эта команда распознает цифровые видеоролики, видеомагнитофоны и звуковые устройства аудио-видео.</span><span class="sxs-lookup"><span data-stu-id="9d8ce-106">Digital-video, VCR, and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="9d8ce-107">Хотя аудио компакт-диск, программа MIDI Sequencer и устройства видеодиск также распознают эту команду, драйверы устройств МЦИКДА, МЦИСЕК и МЦИПИОНР не поддерживают эти команды.</span><span class="sxs-lookup"><span data-stu-id="9d8ce-107">Although CD audio, MIDI sequencer, and videodisc devices also recognize this command, the MCICDA, MCISEQ, and MCIPIONR device drivers do not support it.</span></span>

<span data-ttu-id="9d8ce-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="9d8ce-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_RESUME, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpResume
);
```



## <a name="parameters"></a><span data-ttu-id="9d8ce-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="9d8ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9d8ce-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="9d8ce-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="9d8ce-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="9d8ce-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="9d8ce-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="9d8ce-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="9d8ce-113">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="9d8ce-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="9d8ce-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="9d8ce-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="9d8ce-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*лпресуме*</span><span class="sxs-lookup"><span data-stu-id="9d8ce-115"><span id="lpResume"></span><span id="lpresume"></span><span id="LPRESUME"></span>*lpResume*</span></span>
</dt> <dd>

<span data-ttu-id="9d8ce-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="9d8ce-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="9d8ce-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="9d8ce-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9d8ce-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9d8ce-118">Return Value</span></span>

<span data-ttu-id="9d8ce-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="9d8ce-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9d8ce-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9d8ce-120">Remarks</span></span>

<span data-ttu-id="9d8ce-121">Эта команда возобновляет воспроизведение и запись, не изменяя текущий набор [ \_ записей](mci-record.md)с помощью [MCI \_ Play](mci-play.md) или MCI.</span><span class="sxs-lookup"><span data-stu-id="9d8ce-121">This command resumes playing and recording without changing the current track position set with [MCI\_PLAY](mci-play.md) or [MCI\_RECORD](mci-record.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9d8ce-122">Требования</span><span class="sxs-lookup"><span data-stu-id="9d8ce-122">Requirements</span></span>



| <span data-ttu-id="9d8ce-123">Требование</span><span class="sxs-lookup"><span data-stu-id="9d8ce-123">Requirement</span></span> | <span data-ttu-id="9d8ce-124">Значение</span><span class="sxs-lookup"><span data-stu-id="9d8ce-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d8ce-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9d8ce-125">Minimum supported client</span></span><br/> | <span data-ttu-id="9d8ce-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9d8ce-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9d8ce-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9d8ce-127">Minimum supported server</span></span><br/> | <span data-ttu-id="9d8ce-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="9d8ce-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="9d8ce-129">Заголовок</span><span class="sxs-lookup"><span data-stu-id="9d8ce-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d8ce-130"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9d8ce-130"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d8ce-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9d8ce-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d8ce-132">MCI</span><span class="sxs-lookup"><span data-stu-id="9d8ce-132">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="9d8ce-133">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="9d8ce-133">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

