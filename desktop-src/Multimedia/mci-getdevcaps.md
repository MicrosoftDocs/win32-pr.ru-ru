---
title: Команда MCI_GETDEVCAPS (Ммсистем. h)
description: Команда MCI \_ жетдевкапс получает статические сведения об устройстве.
ms.assetid: a839006f-ea57-4595-9208-cfc465c95298
keywords:
- MCI_GETDEVCAPS команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_GETDEVCAPS
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85abb0354d36979741d0b292dd9def469cec0049
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535429"
---
# <a name="mci_getdevcaps-command"></a><span data-ttu-id="df28d-104">\_Команда MCI жетдевкапс</span><span class="sxs-lookup"><span data-stu-id="df28d-104">MCI\_GETDEVCAPS command</span></span>

<span data-ttu-id="df28d-105">Команда MCI \_ жетдевкапс получает статические сведения об устройстве.</span><span class="sxs-lookup"><span data-stu-id="df28d-105">The MCI\_GETDEVCAPS command retrieves static information about a device.</span></span> <span data-ttu-id="df28d-106">Все устройства распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="df28d-106">All devices recognize this command.</span></span> <span data-ttu-id="df28d-107">Параметры и флаги, доступные для этой команды, зависят от выбранного устройства.</span><span class="sxs-lookup"><span data-stu-id="df28d-107">The parameters and flags available for this command depend on the selected device.</span></span> <span data-ttu-id="df28d-108">Сведения возвращаются в элементе **двретурн** структуры, определенной параметром *лпкапспармс*.</span><span class="sxs-lookup"><span data-stu-id="df28d-108">Information is returned in the **dwReturn** member of the structure identified by *lpCapsParms*.</span></span>

<span data-ttu-id="df28d-109">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="df28d-109">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_GETDEVCAPS, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GETDEVCAPS_PARMS) lpCapsParms
);
```



## <a name="parameters"></a><span data-ttu-id="df28d-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="df28d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df28d-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="df28d-111"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="df28d-112">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="df28d-112">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="df28d-113"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="df28d-114">\_Уведомление MCI, \_ Ожидание MCI или, для устройств цифрового видео и видеомагнитофона, тест MCI \_ .</span><span class="sxs-lookup"><span data-stu-id="df28d-114">MCI\_NOTIFY, MCI\_WAIT, or, for digital-video and VCR devices, MCI\_TEST.</span></span> <span data-ttu-id="df28d-115">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="df28d-115">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="df28d-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*лпкапспармс*</span><span class="sxs-lookup"><span data-stu-id="df28d-116"><span id="lpCapsParms"></span><span id="lpcapsparms"></span><span id="LPCAPSPARMS"></span>*lpCapsParms*</span></span>
</dt> <dd>

<span data-ttu-id="df28d-117">Указатель на структуру [**\_ \_ пармс MCI жетдевкапс**](mci-getdevcaps-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="df28d-117">Pointer to an [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df28d-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="df28d-118">Return Value</span></span>

<span data-ttu-id="df28d-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="df28d-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="df28d-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="df28d-120">Remarks</span></span>

<span data-ttu-id="df28d-121">Следующие дополнительные стандартные и специальные флаги применяются ко всем устройствам, поддерживающим MCI \_ жетдевкапс:</span><span class="sxs-lookup"><span data-stu-id="df28d-121">The following additional standard and command-specific flags apply to all devices supporting MCI\_GETDEVCAPS:</span></span>

<dl> <dt>

<span data-ttu-id="df28d-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>\_ \_ составное устройство MCI жетдевкапс \_</span><span class="sxs-lookup"><span data-stu-id="df28d-122"><span id="MCI_GETDEVCAPS_COMPOUND_DEVICE"></span><span id="mci_getdevcaps_compound_device"></span>MCI\_GETDEVCAPS\_COMPOUND\_DEVICE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-123">Элемент **двретурн** имеет значение **true** , если устройство использует хранилище данных, которое необходимо явно открыть и закрыть. в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="df28d-123">The **dwReturn** member is set to **TRUE** if the device uses data storage that must be explicitly opened and closed; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>\_ \_ тип устройства mci \_ жетдевкапс</span><span class="sxs-lookup"><span data-stu-id="df28d-124"><span id="MCI_GETDEVCAPS_DEVICE_TYPE"></span><span id="mci_getdevcaps_device_type"></span>MCI\_GETDEVCAPS\_DEVICE\_TYPE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-125">Для элемента **двретурн** задается одно из значений, перечисленных в списке [типы устройств MCI](mci-device-types.md).</span><span class="sxs-lookup"><span data-stu-id="df28d-125">The **dwReturn** member is set to one of the values listed in [MCI Device Types](mci-device-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="df28d-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI \_ жетдевкапс \_ имеет \_ аудио</span><span class="sxs-lookup"><span data-stu-id="df28d-126"><span id="MCI_GETDEVCAPS_HAS_AUDIO"></span><span id="mci_getdevcaps_has_audio"></span>MCI\_GETDEVCAPS\_HAS\_AUDIO</span></span>
</dt> <dd>

<span data-ttu-id="df28d-127">Элемент **двретурн** имеет значение **true** , если устройство имеет звуковые выходные данные; в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="df28d-127">The **dwReturn** member is set to **TRUE** if the device has audio output; it is set to **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI \_ жетдевкапс \_ имеет \_ видео</span><span class="sxs-lookup"><span data-stu-id="df28d-128"><span id="MCI_GETDEVCAPS_HAS_VIDEO"></span><span id="mci_getdevcaps_has_video"></span>MCI\_GETDEVCAPS\_HAS\_VIDEO</span></span>
</dt> <dd>

<span data-ttu-id="df28d-129">Элемент **двретурн** имеет значение **true** , если устройство имеет выходные данные видео; в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="df28d-129">The **dwReturn** member is set to **TRUE** if the device has video output; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="df28d-130">Например, члену присваивается **значение true** для устройств, поддерживающих набор команд видеодиск.</span><span class="sxs-lookup"><span data-stu-id="df28d-130">For example, the member is set to **TRUE** for devices that support the videodisc command set.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>\_элемент ЖЕТДЕВКАПС \_ MCI</span><span class="sxs-lookup"><span data-stu-id="df28d-131"><span id="MCI_GETDEVCAPS_ITEM"></span><span id="mci_getdevcaps_item"></span>MCI\_GETDEVCAPS\_ITEM</span></span>
</dt> <dd>

<span data-ttu-id="df28d-132">Указывает, что элемент **двитем** структуры [**\_ \_ пармс жетдевкапс**](mci-getdevcaps-parms.md) содержит одну из следующих констант:</span><span class="sxs-lookup"><span data-stu-id="df28d-132">Specifies that the **dwItem** member of the [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) structure contains one of the following constants:</span></span>

</dd> <dt>

<span data-ttu-id="df28d-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>\_ЖЕТДЕВКАПС MCI \_ может \_ извлечь</span><span class="sxs-lookup"><span data-stu-id="df28d-133"><span id="MCI_GETDEVCAPS_CAN_EJECT"></span><span id="mci_getdevcaps_can_eject"></span>MCI\_GETDEVCAPS\_CAN\_EJECT</span></span>
</dt> <dd>

<span data-ttu-id="df28d-134">Член **двретурн** имеет значение **true** , если устройство может извлечь носитель; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-134">The **dwReturn** member is set to **TRUE** if the device can eject the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>\_ \_ может играть жетдевкапс \_ MCI</span><span class="sxs-lookup"><span data-stu-id="df28d-135"><span id="MCI_GETDEVCAPS_CAN_PLAY"></span><span id="mci_getdevcaps_can_play"></span>MCI\_GETDEVCAPS\_CAN\_PLAY</span></span>
</dt> <dd>

<span data-ttu-id="df28d-136">Элемент **двретурн** имеет значение **true** , если устройство может воспроизвести носитель; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-136">The **dwReturn** member is set to **TRUE** if the device can play the media; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="df28d-137">Если на устройстве указано **значение true**, это означает, что устройство поддерживает команды [ \_ приостановки](mci-pause.md) и [ \_ остановки](mci-stop.md) MCI, а также команду [MCI \_ Play](mci-play.md) .</span><span class="sxs-lookup"><span data-stu-id="df28d-137">If a device specifies **TRUE**, it implies the device supports the [MCI\_PAUSE](mci-pause.md) and [MCI\_STOP](mci-stop.md) commands as well as the [MCI\_PLAY](mci-play.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI \_ жетдевкапс \_ может \_ записывать</span><span class="sxs-lookup"><span data-stu-id="df28d-138"><span id="MCI_GETDEVCAPS_CAN_RECORD"></span><span id="mci_getdevcaps_can_record"></span>MCI\_GETDEVCAPS\_CAN\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="df28d-139">Элемент **двретурн** имеет значение **true** , если устройство поддерживает запись; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-139">The **dwReturn** member is set to **TRUE** if the device supports recording; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="df28d-140">Если на устройстве указано **значение true**, это означает, что устройство поддерживает \_ команды приостановки и остановки MCI, а \_ также команду [MCI \_ Record](mci-record.md) .</span><span class="sxs-lookup"><span data-stu-id="df28d-140">If a device specifies **TRUE**, it implies the device supports the MCI\_PAUSE and MCI\_STOP commands as well as the [MCI\_RECORD](mci-record.md) command.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>\_ЖЕТДЕВКАПС MCI \_ может \_ сохранить</span><span class="sxs-lookup"><span data-stu-id="df28d-141"><span id="MCI_GETDEVCAPS_CAN_SAVE"></span><span id="mci_getdevcaps_can_save"></span>MCI\_GETDEVCAPS\_CAN\_SAVE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-142">Элемент **двретурн** имеет значение **true** , если устройство может сохранить файл; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-142">The **dwReturn** member is set to **TRUE** if the device can save a file; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI \_ жетдевкапс \_ использует \_ файлы</span><span class="sxs-lookup"><span data-stu-id="df28d-143"><span id="MCI_GETDEVCAPS_USES_FILES"></span><span id="mci_getdevcaps_uses_files"></span>MCI\_GETDEVCAPS\_USES\_FILES</span></span>
</dt> <dd>

<span data-ttu-id="df28d-144">Элемент **двретурн** имеет значение **true** , если устройству требуется имя файла; в противном случае устанавливается значение **false** .</span><span class="sxs-lookup"><span data-stu-id="df28d-144">The **dwReturn** member is set to **TRUE** if the device requires a filename; it is set to **FALSE** otherwise.</span></span> <span data-ttu-id="df28d-145">Файлы используются только для составных устройств.</span><span class="sxs-lookup"><span data-stu-id="df28d-145">Only compound devices use files.</span></span>

</dd> </dl>

<span data-ttu-id="df28d-146">Следующие флаги можно указать в элементе **Двитем** [**MCI \_ жетдевкапс \_ пармс**](mci-getdevcaps-parms.md) для типа устройства **дигиталвидео** :</span><span class="sxs-lookup"><span data-stu-id="df28d-146">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **digitalvideo** device type:</span></span>

<dl> <dt>

<span data-ttu-id="df28d-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI \_ ДГВ \_ жетдевкапс \_ может \_ заморозить</span><span class="sxs-lookup"><span data-stu-id="df28d-147"><span id="MCI_DGV_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_dgv_getdevcaps_can_freeze"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-148">Элемент **двретурн** имеет значение **true** , если устройство может заморозить кадры; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-148">The **dwReturn** member is set to **TRUE** if the device can freeze frames; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>\_жетдевкапс ДГВ \_ MCI \_ может \_ блокировать</span><span class="sxs-lookup"><span data-stu-id="df28d-149"><span id="MCI_DGV_GETDEVCAPS_CAN_LOCK"></span><span id="mci_dgv_getdevcaps_can_lock"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_LOCK</span></span>
</dt> <dd>

<span data-ttu-id="df28d-150">Элемент **двретурн** имеет значение **true** , если устройство может блокироваться; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-150">The **dwReturn** member is set to **TRUE** if the device can lock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>\_ДГВ MCI \_ жетдевкапс \_ может \_ обратить</span><span class="sxs-lookup"><span data-stu-id="df28d-151"><span id="MCI_DGV_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_dgv_getdevcaps_can_reverse"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-152">Элемент **двретурн** имеет значение **true** , если устройство может воспроизводиться в обратную; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-152">The **dwReturn** member is set to **TRUE** if the device can play in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>\_ДГВ MCI \_ жетдевкапс \_ может выполнять \_ str \_</span><span class="sxs-lookup"><span data-stu-id="df28d-153"><span id="MCI_DGV_GETDEVCAPS_CAN_STR_IN"></span><span id="mci_dgv_getdevcaps_can_str_in"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STR\_IN</span></span>
</dt> <dd>

<span data-ttu-id="df28d-154">Элемент **двретурн** имеет значение **true** , если устройство может растягивать входные данные; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-154">The **dwReturn** member is set to **TRUE** if the device can stretch input; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>\_жетдевкапс ДГВ \_ MCI \_ может \_ растянуть</span><span class="sxs-lookup"><span data-stu-id="df28d-155"><span id="MCI_DGV_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_dgv_getdevcaps_can_stretch"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="df28d-156">Элемент **двретурн** имеет значение **true** , если устройство может растянуть изображение; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-156">The **dwReturn** member is set to **TRUE** if the device can stretch an image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>\_ДГВ MCI \_ жетдевкапс \_ может \_ тестировать</span><span class="sxs-lookup"><span data-stu-id="df28d-157"><span id="MCI_DGV_GETDEVCAPS_CAN_TEST"></span><span id="mci_dgv_getdevcaps_can_test"></span>MCI\_DGV\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="df28d-158">Элемент **двретурн** имеет значение **true** , если устройство может выполнять тесты; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-158">The **dwReturn** member is set to **TRUE** if the device can perform tests; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI \_ ДГВ \_ жетдевкапс \_ \_ по-прежнему</span><span class="sxs-lookup"><span data-stu-id="df28d-159"><span id="MCI_DGV_GETDEVCAPS_HAS_STILL"></span><span id="mci_dgv_getdevcaps_has_still"></span>MCI\_DGV\_GETDEVCAPS\_HAS\_STILL</span></span>
</dt> <dd>

<span data-ttu-id="df28d-160">Элемент **двретурн** имеет значение **true** , если устройство может отображать изображения по-прежнему. в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-160">The **dwReturn** member is set to **TRUE** if the device can display still images; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>\_ДГВ \_ жетдевкапс ( \_ Максимальное число \_ окон MCI)</span><span class="sxs-lookup"><span data-stu-id="df28d-161"><span id="MCI_DGV_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_dgv_getdevcaps_max_windows"></span>MCI\_DGV\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="df28d-162">Для элемента **двретурн** задается максимальное число окон, которое устройство может одновременно обрабатывало.</span><span class="sxs-lookup"><span data-stu-id="df28d-162">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>\_ \_ \_ Максимальная \_ Частота жетдевкапс MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="df28d-163"><span id="MCI_DGV_GETDEVCAPS_MAXIMUM_RATE"></span><span id="mci_dgv_getdevcaps_maximum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MAXIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-164">Элемент **двретурн** задает максимальную скорость воспроизведения для устройства в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="df28d-164">The **dwReturn** member is set to the maximum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>\_ \_ \_ Минимальная \_ Частота жетдевкапс MCI ДГВ</span><span class="sxs-lookup"><span data-stu-id="df28d-165"><span id="MCI_DGV_GETDEVCAPS_MINIMUM_RATE"></span><span id="mci_dgv_getdevcaps_minimum_rate"></span>MCI\_DGV\_GETDEVCAPS\_MINIMUM\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-166">Для элемента **двретурн** устанавливается минимальная скорость воспроизведения для устройства, в кадрах в секунду.</span><span class="sxs-lookup"><span data-stu-id="df28d-166">The **dwReturn** member is set to the minimum play rate for the device, in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>\_ \_ палитры MCI ДГВ жетдевкапс \_</span><span class="sxs-lookup"><span data-stu-id="df28d-167"><span id="MCI_DGV_GETDEVCAPS_PALETTES"></span><span id="mci_dgv_getdevcaps_palettes"></span>MCI\_DGV\_GETDEVCAPS\_PALETTES</span></span>
</dt> <dd>

<span data-ttu-id="df28d-168">Элемент **двретурн** имеет значение **true** , если устройство может возвращать маркер палитры; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-168">The **dwReturn** member is set to **TRUE** if the device can return a palette handle; otherwise, it is set to **FALSE**.</span></span>

</dd> </dl>

<span data-ttu-id="df28d-169">Следующие флаги можно указать в элементе **Двитем** [**MCI \_ жетдевкапс \_ пармс**](mci-getdevcaps-parms.md) для типа устройства **видеомагнитофона** :</span><span class="sxs-lookup"><span data-stu-id="df28d-169">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **vcr** device type:</span></span>

<dl> <dt>

<span data-ttu-id="df28d-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>\_ \_ \_ Частота приращения часов жетдевкапс MCI \_</span><span class="sxs-lookup"><span data-stu-id="df28d-170"><span id="MCI_GETDEVCAPS_CLOCK_INCREMENT_RATE"></span><span id="mci_getdevcaps_clock_increment_rate"></span>MCI\_GETDEVCAPS\_CLOCK\_INCREMENT\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-171">Для элемента **двретурн** задается число приращений в секунду.</span><span class="sxs-lookup"><span data-stu-id="df28d-171">The **dwReturn** member is set to the number of increments per second.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может \_ определить \_ длину</span><span class="sxs-lookup"><span data-stu-id="df28d-172"><span id="MCI_VCR_GETDEVCAPS_CAN_DETECT_LENGTH"></span><span id="mci_vcr_getdevcaps_can_detect_length"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_DETECT\_LENGTH</span></span>
</dt> <dd>

<span data-ttu-id="df28d-173">Член **двретурн** имеет значение **true** , если устройство может определить длину носителя; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-173">The **dwReturn** member is set to **TRUE** if the device is capable of detecting the length of the media; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может \_ заморозить</span><span class="sxs-lookup"><span data-stu-id="df28d-174"><span id="MCI_VCR_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_vcr_getdevcaps_can_freeze"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-175">Член **двретурн** имеет значение **true** , если устройство может заморозить выходное изображение; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-175">The **dwReturn** member is set to **TRUE** if the device is capable of freezing the output image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может \_ отслеживать \_ источники</span><span class="sxs-lookup"><span data-stu-id="df28d-176"><span id="MCI_VCR_GETDEVCAPS_CAN_MONITOR_SOURCES"></span><span id="mci_vcr_getdevcaps_can_monitor_sources"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_MONITOR\_SOURCES</span></span>
</dt> <dd>

<span data-ttu-id="df28d-177">Член **двретурн** имеет значение **true** , если устройство может отслеживать источники. в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-177">The **dwReturn** member is set to **TRUE** if the device is capable of monitoring sources; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может \_ выполнить предпробную выгрузку</span><span class="sxs-lookup"><span data-stu-id="df28d-178"><span id="MCI_VCR_GETDEVCAPS_CAN_PREROLL"></span><span id="mci_vcr_getdevcaps_can_preroll"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREROLL</span></span>
</dt> <dd>

<span data-ttu-id="df28d-179">Элемент **двретурн** имеет значение **true** , если устройство поддерживает предустановку; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-179">The **dwReturn** member is set to **TRUE** if the device is capable of preroll; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может быть \_ предварительной версией</span><span class="sxs-lookup"><span data-stu-id="df28d-180"><span id="MCI_VCR_GETDEVCAPS_CAN_PREVIEW"></span><span id="mci_vcr_getdevcaps_can_preview"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_PREVIEW</span></span>
</dt> <dd>

<span data-ttu-id="df28d-181">Элемент **двретурн** имеет значение **true** , если устройство поддерживает предварительный просмотр; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-181">The **dwReturn** member is set to **TRUE** if the device is capable of previews; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может быть \_ обратным</span><span class="sxs-lookup"><span data-stu-id="df28d-182"><span id="MCI_VCR_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vcr_getdevcaps_can_reverse"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-183">Элемент **двретурн** имеет значение **true** , если устройство может воспроизводить в обратную, в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-183">The **dwReturn** member is set to **TRUE** if the device is capable of playing in reverse; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ может \_ протестировать</span><span class="sxs-lookup"><span data-stu-id="df28d-184"><span id="MCI_VCR_GETDEVCAPS_CAN_TEST"></span><span id="mci_vcr_getdevcaps_can_test"></span>MCI\_VCR\_GETDEVCAPS\_CAN\_TEST</span></span>
</dt> <dd>

<span data-ttu-id="df28d-185">Элемент **двретурн** имеет значение **true** , если устройство поддерживает тестирование; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-185">The **dwReturn** member is set to **TRUE** if the device is capable of testing; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>видеомагнитофон MCI \_ \_ жетдевкапс \_ имеет \_ Часы</span><span class="sxs-lookup"><span data-stu-id="df28d-186"><span id="MCI_VCR_GETDEVCAPS_HAS_CLOCK"></span><span id="mci_vcr_getdevcaps_has_clock"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_CLOCK</span></span>
</dt> <dd>

<span data-ttu-id="df28d-187">Элемент **двретурн** имеет значение **true** , если устройство поддерживает внешние часы; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-187">The **dwReturn** member is set to **TRUE** if the device supports an external clock; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>код \_ видеомагнитофона MCI \_ жетдевкапс \_ имеет \_ код времени</span><span class="sxs-lookup"><span data-stu-id="df28d-188"><span id="MCI_VCR_GETDEVCAPS_HAS_TIMECODE"></span><span id="mci_vcr_getdevcaps_has_timecode"></span>MCI\_VCR\_GETDEVCAPS\_HAS\_TIMECODE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-189">Элемент **двретурн** имеет значение **true** , если устройство имеет функцию времени в виде времени или если эта возможность неизвестна. в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-189">The **dwReturn** member is set to **TRUE** if device has timecode capability or if this capability is unknown; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>\_жетдевкапс ВИДЕОМАГНИТОФОН \_ MCI \_ число \_ \_ меток</span><span class="sxs-lookup"><span data-stu-id="df28d-190"><span id="MCI_VCR_GETDEVCAPS_NUMBER_OF_MARKS"></span><span id="mci_vcr_getdevcaps_number_of_marks"></span>MCI\_VCR\_GETDEVCAPS\_NUMBER\_OF\_MARKS</span></span>
</dt> <dd>

<span data-ttu-id="df28d-191">Для элемента **двретурн** задается число меток (99).</span><span class="sxs-lookup"><span data-stu-id="df28d-191">The **dwReturn** member is set to the number of marks (99).</span></span>

</dd> <dt>

<span data-ttu-id="df28d-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>\_ \_ \_ точность поиска жетдевкапс видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="df28d-192"><span id="MCI_VCR_GETDEVCAPS_SEEK_ACCURACY"></span><span id="mci_vcr_getdevcaps_seek_accuracy"></span>MCI\_VCR\_GETDEVCAPS\_SEEK\_ACCURACY</span></span>
</dt> <dd>

<span data-ttu-id="df28d-193">Для элемента **двретурн** задана точность поиска устройства.</span><span class="sxs-lookup"><span data-stu-id="df28d-193">The **dwReturn** member is set to the seek accuracy of the device.</span></span>

</dd> </dl>

<span data-ttu-id="df28d-194">Следующие флаги можно указать в элементе **Двитем** [**MCI \_ жетдевкапс \_ пармс**](mci-getdevcaps-parms.md) для типа устройства **оверлея** :</span><span class="sxs-lookup"><span data-stu-id="df28d-194">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **overlay** device type:</span></span>

<dl> <dt>

<span data-ttu-id="df28d-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI \_ овли \_ жетдевкапс \_ может \_ заморозить</span><span class="sxs-lookup"><span data-stu-id="df28d-195"><span id="MCI_OVLY_GETDEVCAPS_CAN_FREEZE"></span><span id="mci_ovly_getdevcaps_can_freeze"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_FREEZE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-196">Элемент **двретурн** имеет значение **true** , если устройство может заморозить образ; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-196">The **dwReturn** member is set to **TRUE** if the device can freeze the image; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>\_жетдевкапс ОВЛИ \_ MCI \_ может \_ растянуть</span><span class="sxs-lookup"><span data-stu-id="df28d-197"><span id="MCI_OVLY_GETDEVCAPS_CAN_STRETCH"></span><span id="mci_ovly_getdevcaps_can_stretch"></span>MCI\_OVLY\_GETDEVCAPS\_CAN\_STRETCH</span></span>
</dt> <dd>

<span data-ttu-id="df28d-198">Элемент **двретурн** имеет значение **true** , если устройство может растянуть изображение для заполнения рамки; в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-198">The **dwReturn** member is set to **TRUE** if the device can stretch the image to fill the frame; otherwise, it is set to **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>\_овли \_ жетдевкапс ( \_ Максимальное число \_ окон MCI)</span><span class="sxs-lookup"><span data-stu-id="df28d-199"><span id="MCI_OVLY_GETDEVCAPS_MAX_WINDOWS"></span><span id="mci_ovly_getdevcaps_max_windows"></span>MCI\_OVLY\_GETDEVCAPS\_MAX\_WINDOWS</span></span>
</dt> <dd>

<span data-ttu-id="df28d-200">Для элемента **двретурн** задается максимальное число окон, которое устройство может одновременно обрабатывало.</span><span class="sxs-lookup"><span data-stu-id="df28d-200">The **dwReturn** member is set to the maximum number of windows that the device can handle simultaneously.</span></span>

</dd> </dl>

<span data-ttu-id="df28d-201">Следующие флаги можно указать в элементе **Двитем** [**MCI \_ жетдевкапс \_ пармс**](mci-getdevcaps-parms.md) для типа устройства **видеодиск** :</span><span class="sxs-lookup"><span data-stu-id="df28d-201">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **videodisc** device type:</span></span>

<dl> <dt>

<span data-ttu-id="df28d-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>\_VD MCI \_ жетдевкапс \_ может \_ обратить</span><span class="sxs-lookup"><span data-stu-id="df28d-202"><span id="MCI_VD_GETDEVCAPS_CAN_REVERSE"></span><span id="mci_vd_getdevcaps_can_reverse"></span>MCI\_VD\_GETDEVCAPS\_CAN\_REVERSE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-203">Элемент **двретурн** имеет значение **true** , если проигрыватель видеодиск может воспроизводиться в обратную, в противном случае для него задается значение **false**.</span><span class="sxs-lookup"><span data-stu-id="df28d-203">The **dwReturn** member is set to **TRUE** if the videodisc player can play in reverse; otherwise, it is set to **FALSE**.</span></span> <span data-ttu-id="df28d-204">Некоторые игроки могут воспроизводить CLV диски в обратную, а также на Кав дисках.</span><span class="sxs-lookup"><span data-stu-id="df28d-204">Some players can play CLV discs in reverse as well as CAV discs.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI \_ VD \_ жетдевкапс \_ Кав</span><span class="sxs-lookup"><span data-stu-id="df28d-205"><span id="MCI_VD_GETDEVCAPS_CAV"></span><span id="mci_vd_getdevcaps_cav"></span>MCI\_VD\_GETDEVCAPS\_CAV</span></span>
</dt> <dd>

<span data-ttu-id="df28d-206">При объединении с другими элементами указывает, что возвращаемые сведения применяются к Кав формата видеодискс.</span><span class="sxs-lookup"><span data-stu-id="df28d-206">When combined with other items, specifies that the return information applies to CAV format videodiscs.</span></span> <span data-ttu-id="df28d-207">Это значение по умолчанию, если видеодиск не вставлен.</span><span class="sxs-lookup"><span data-stu-id="df28d-207">This is the default if no videodisc is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI \_ VD \_ жетдевкапс \_ CLV</span><span class="sxs-lookup"><span data-stu-id="df28d-208"><span id="MCI_VD_GETDEVCAPS_CLV"></span><span id="mci_vd_getdevcaps_clv"></span>MCI\_VD\_GETDEVCAPS\_CLV</span></span>
</dt> <dd>

<span data-ttu-id="df28d-209">При объединении с другими элементами указывает, что возвращаемые сведения применяются к CLV формата видеодискс.</span><span class="sxs-lookup"><span data-stu-id="df28d-209">When combined with other items, specifies that the return information applies to CLV format videodiscs.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>\_ \_ \_ Ускоренная скорость MCI VD жетдевкапс \_</span><span class="sxs-lookup"><span data-stu-id="df28d-210"><span id="MCI_VD_GETDEVCAPS_FAST_RATE"></span><span id="mci_vd_getdevcaps_fast_rate"></span>MCI\_VD\_GETDEVCAPS\_FAST\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-211">Для элемента **двретурн** задана стандартная частота быстрого воспроизведения в кадрах за секунду.</span><span class="sxs-lookup"><span data-stu-id="df28d-211">The **dwReturn** member is set to the standard fast play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>\_ \_ \_ нормальная ставка mCi VD жетдевкапс \_</span><span class="sxs-lookup"><span data-stu-id="df28d-212"><span id="MCI_VD_GETDEVCAPS_NORMAL_RATE"></span><span id="mci_vd_getdevcaps_normal_rate"></span>MCI\_VD\_GETDEVCAPS\_NORMAL\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-213">Для элемента **двретурн** задана нормальная скорость воспроизведения в кадрах за секунду.</span><span class="sxs-lookup"><span data-stu-id="df28d-213">The **dwReturn** member is set to the normal play rate in frames per second.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>скорость работы MCI \_ VD \_ жетдевкапс \_ \_</span><span class="sxs-lookup"><span data-stu-id="df28d-214"><span id="MCI_VD_GETDEVCAPS_SLOW_RATE"></span><span id="mci_vd_getdevcaps_slow_rate"></span>MCI\_VD\_GETDEVCAPS\_SLOW\_RATE</span></span>
</dt> <dd>

<span data-ttu-id="df28d-215">Для элемента **двретурн** задана Стандартная скорость воспроизведения кадров в секунду.</span><span class="sxs-lookup"><span data-stu-id="df28d-215">The **dwReturn** member is set to the standard slow play rate in frames per second.</span></span>

</dd> </dl>

<span data-ttu-id="df28d-216">Следующие флаги можно указать в элементе **Двитем** [**MCI \_ жетдевкапс \_ пармс**](mci-getdevcaps-parms.md) для типа устройства **вавеаудио** :</span><span class="sxs-lookup"><span data-stu-id="df28d-216">The following flags can be specified in the **dwItem** member of [**MCI\_GETDEVCAPS\_PARMS**](mci-getdevcaps-parms.md) for the **waveaudio** device type:</span></span>

<dl> <dt>

<span data-ttu-id="df28d-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>\_ \_ \_ входные данные MCI Wave жетдевкапс</span><span class="sxs-lookup"><span data-stu-id="df28d-217"><span id="MCI_WAVE_GETDEVCAPS_INPUT"></span><span id="mci_wave_getdevcaps_input"></span>MCI\_WAVE\_GETDEVCAPS\_INPUT</span></span>
</dt> <dd>

<span data-ttu-id="df28d-218">Для элемента **двретурн** задается общее количество входных устройств аудио (запись).</span><span class="sxs-lookup"><span data-stu-id="df28d-218">The **dwReturn** member is set to the total number of waveform input (recording) devices.</span></span>

</dd> <dt>

<span data-ttu-id="df28d-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>\_ \_ выходные данные жетдевкапса MCI Wave \_</span><span class="sxs-lookup"><span data-stu-id="df28d-219"><span id="MCI_WAVE_GETDEVCAPS_OUTPUT"></span><span id="mci_wave_getdevcaps_output"></span>MCI\_WAVE\_GETDEVCAPS\_OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="df28d-220">Для элемента **двретурн** задается общее количество устройств вывода аудио (воспроизведение).</span><span class="sxs-lookup"><span data-stu-id="df28d-220">The **dwReturn** member is set to the total number of waveform output (playback) devices.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="df28d-221">Требования</span><span class="sxs-lookup"><span data-stu-id="df28d-221">Requirements</span></span>



| <span data-ttu-id="df28d-222">Требование</span><span class="sxs-lookup"><span data-stu-id="df28d-222">Requirement</span></span> | <span data-ttu-id="df28d-223">Значение</span><span class="sxs-lookup"><span data-stu-id="df28d-223">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df28d-224">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="df28d-224">Minimum supported client</span></span><br/> | <span data-ttu-id="df28d-225">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df28d-225">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="df28d-226">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="df28d-226">Minimum supported server</span></span><br/> | <span data-ttu-id="df28d-227">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="df28d-227">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="df28d-228">Заголовок</span><span class="sxs-lookup"><span data-stu-id="df28d-228">Header</span></span><br/>                   | <dl> <span data-ttu-id="df28d-229"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df28d-229"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df28d-230">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="df28d-230">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df28d-231">MCI</span><span class="sxs-lookup"><span data-stu-id="df28d-231">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="df28d-232">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="df28d-232">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

