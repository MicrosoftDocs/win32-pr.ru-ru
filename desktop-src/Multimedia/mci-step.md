---
title: Команда MCI_STEP (Ммсистем. h)
description: Команда MCI \_ Step пошаговое описание одного или нескольких кадров в проигрывателе. Это команда распознает устройства Digital-Video, ВИДЕОМАГНИТОФОН и Кав-Format видеодиск.
ms.assetid: 8d976840-fe9d-4393-b9fc-10f847166b1b
keywords:
- MCI_STEP команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_STEP
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd81b3ad0e1f10c14d68df12399045149f686a8c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135079"
---
# <a name="mci_step-command"></a><span data-ttu-id="65ea2-105">\_Команда на шаге MCI</span><span class="sxs-lookup"><span data-stu-id="65ea2-105">MCI\_STEP command</span></span>

<span data-ttu-id="65ea2-106">Команда MCI \_ Step пошаговое описание одного или нескольких кадров в проигрывателе.</span><span class="sxs-lookup"><span data-stu-id="65ea2-106">The MCI\_STEP command steps the player one or more frames.</span></span> <span data-ttu-id="65ea2-107">Это команда распознает устройства Digital-Video, ВИДЕОМАГНИТОФОН и Кав-Format видеодиск.</span><span class="sxs-lookup"><span data-stu-id="65ea2-107">Digital-video, VCR, and CAV-format videodisc devices recognize this command.</span></span>

<span data-ttu-id="65ea2-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="65ea2-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_STEP, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpStep
);
```



## <a name="parameters"></a><span data-ttu-id="65ea2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="65ea2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65ea2-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="65ea2-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="65ea2-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="65ea2-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="65ea2-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="65ea2-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="65ea2-113">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="65ea2-113">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="65ea2-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="65ea2-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="65ea2-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*лпстеп*</span><span class="sxs-lookup"><span data-stu-id="65ea2-115"><span id="lpStep"></span><span id="lpstep"></span><span id="LPSTEP"></span>*lpStep*</span></span>
</dt> <dd>

<span data-ttu-id="65ea2-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="65ea2-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="65ea2-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="65ea2-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="65ea2-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="65ea2-118">Return Value</span></span>

<span data-ttu-id="65ea2-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="65ea2-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="65ea2-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="65ea2-120">Remarks</span></span>

<span data-ttu-id="65ea2-121">Эта команда поддерживает устройства, которые возвращают **значение true** параметру MCI \_ жетдевкапс \_ с \_ флагом Video команды [MCI \_ жетдевкапс](mci-getdevcaps.md) .</span><span class="sxs-lookup"><span data-stu-id="65ea2-121">This command supports devices that return **TRUE** to the MCI\_GETDEVCAPS\_HAS\_VIDEO flag of the [MCI\_GETDEVCAPS](mci-getdevcaps.md) command.</span></span>

<span data-ttu-id="65ea2-122">С типом устройства **дигиталвидео** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="65ea2-122">The following additional flags are used with the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="65ea2-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>\_ \_ кадры шага MCI \_ ДГВ</span><span class="sxs-lookup"><span data-stu-id="65ea2-123"><span id="MCI_DGV_STEP_FRAMES"></span><span id="mci_dgv_step_frames"></span>MCI\_DGV\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="65ea2-124">Элемент **двфрамес** структуры, идентифицируемой *лпстеп* , задает число кадров, которые должны быть предварительно выведены перед отображением другого изображения.</span><span class="sxs-lookup"><span data-stu-id="65ea2-124">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="65ea2-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>\_ \_ обратный шаг ДГВ \_ MCI</span><span class="sxs-lookup"><span data-stu-id="65ea2-125"><span id="MCI_DGV_STEP_REVERSE"></span><span id="mci_dgv_step_reverse"></span>MCI\_DGV\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="65ea2-126">Действия в обратную.</span><span class="sxs-lookup"><span data-stu-id="65ea2-126">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="65ea2-127">Для устройств с цифровыми видео параметр *лпстеп* указывает на структуру [**\_ ДГВ \_ шага \_ пармс MCI**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) .</span><span class="sxs-lookup"><span data-stu-id="65ea2-127">For digital-video devices, the *lpStep* parameter points to an [**MCI\_DGV\_STEP\_PARMS**](/windows/desktop/api/Digitalv/ns-digitalv-mci_dgv_step_parms) structure.</span></span>

<span data-ttu-id="65ea2-128">Для типа устройства **видеомагнитофона** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="65ea2-128">The following additional flags are used with the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="65ea2-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>\_кадры для \_ шага \_ видеомагнитофона MCI</span><span class="sxs-lookup"><span data-stu-id="65ea2-129"><span id="MCI_VCR_STEP_FRAMES"></span><span id="mci_vcr_step_frames"></span>MCI\_VCR\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="65ea2-130">Элемент **двфрамес** структуры, идентифицируемой *лпстеп* , задает число кадров, которые должны быть предварительно выведены перед отображением другого изображения.</span><span class="sxs-lookup"><span data-stu-id="65ea2-130">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to advance before displaying another image.</span></span>

</dd> <dt>

<span data-ttu-id="65ea2-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>\_обратный шаг видеомагнитофона MCI \_ \_</span><span class="sxs-lookup"><span data-stu-id="65ea2-131"><span id="MCI_VCR_STEP_REVERSE"></span><span id="mci_vcr_step_reverse"></span>MCI\_VCR\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="65ea2-132">Действия в обратную.</span><span class="sxs-lookup"><span data-stu-id="65ea2-132">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="65ea2-133">Для устройств ВИДЕОМАГНИТОФОНА параметр *лпстеп* указывает на структуру пармс на [**\_ \_ этапе \_ видеомагнитофона MCI**](mci-vcr-step-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="65ea2-133">For VCR devices, the *lpStep* parameter points to an [**MCI\_VCR\_STEP\_PARMS**](mci-vcr-step-parms.md) structure.</span></span>

<span data-ttu-id="65ea2-134">С типом устройства **видеодиск** используются следующие дополнительные флаги:</span><span class="sxs-lookup"><span data-stu-id="65ea2-134">The following additional flags are used with the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="65ea2-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>\_ \_ кадры шага MCI \_ VD</span><span class="sxs-lookup"><span data-stu-id="65ea2-135"><span id="MCI_VD_STEP_FRAMES"></span><span id="mci_vd_step_frames"></span>MCI\_VD\_STEP\_FRAMES</span></span>
</dt> <dd>

<span data-ttu-id="65ea2-136">Элемент **двфрамес** структуры, определяемой параметром *лпстеп* , указывает количество кадров для шага.</span><span class="sxs-lookup"><span data-stu-id="65ea2-136">The **dwFrames** member of the structure identified by *lpStep* specifies the number of frames to step.</span></span>

</dd> <dt>

<span data-ttu-id="65ea2-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>\_ \_ обратный шаг VD \_ MCI</span><span class="sxs-lookup"><span data-stu-id="65ea2-137"><span id="MCI_VD_STEP_REVERSE"></span><span id="mci_vd_step_reverse"></span>MCI\_VD\_STEP\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="65ea2-138">Действия в обратную.</span><span class="sxs-lookup"><span data-stu-id="65ea2-138">Steps in reverse.</span></span>

</dd> </dl>

<span data-ttu-id="65ea2-139">Для устройств видеодиск параметр *лпстеп* указывает на структуру [**\_ VD \_ шага MCI \_ пармс**](mci-vd-step-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="65ea2-139">For videodisc devices, the *lpStep* parameter points to an [**MCI\_VD\_STEP\_PARMS**](mci-vd-step-parms.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="65ea2-140">Требования</span><span class="sxs-lookup"><span data-stu-id="65ea2-140">Requirements</span></span>



| <span data-ttu-id="65ea2-141">Требование</span><span class="sxs-lookup"><span data-stu-id="65ea2-141">Requirement</span></span> | <span data-ttu-id="65ea2-142">Значение</span><span class="sxs-lookup"><span data-stu-id="65ea2-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65ea2-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="65ea2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="65ea2-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65ea2-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="65ea2-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="65ea2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="65ea2-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="65ea2-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="65ea2-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="65ea2-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="65ea2-148"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65ea2-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ea2-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="65ea2-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ea2-150">MCI</span><span class="sxs-lookup"><span data-stu-id="65ea2-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="65ea2-151">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="65ea2-151">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

