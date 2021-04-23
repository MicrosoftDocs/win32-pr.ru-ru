---
title: Команда MCI_SETTUNER (Ммсистем. h)
description: Команда MCI \_ сеттунер устанавливает текущий канал на тюнере. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.
ms.assetid: d9f4d6b8-ba73-40ec-a2f9-76adab0fd6f4
keywords:
- MCI_SETTUNER команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SETTUNER
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5774a927e1f41cf5d3bf42d6e93e532e0c2961a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104072001"
---
# <a name="mci_settuner-command"></a><span data-ttu-id="d145d-105">\_Команда MCI сеттунер</span><span class="sxs-lookup"><span data-stu-id="d145d-105">MCI\_SETTUNER command</span></span>

<span data-ttu-id="d145d-106">Команда MCI \_ сеттунер устанавливает текущий канал на тюнере.</span><span class="sxs-lookup"><span data-stu-id="d145d-106">The MCI\_SETTUNER command sets the current channel on the tuner.</span></span> <span data-ttu-id="d145d-107">Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="d145d-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="d145d-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="d145d-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTUNER, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTuner
);
```



## <a name="parameters"></a><span data-ttu-id="d145d-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d145d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d145d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="d145d-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d145d-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="d145d-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d145d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d145d-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d145d-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="d145d-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="d145d-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d145d-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d145d-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*лпсеттунер*</span><span class="sxs-lookup"><span data-stu-id="d145d-115"><span id="lpSetTuner"></span><span id="lpsettuner"></span><span id="LPSETTUNER"></span>*lpSetTuner*</span></span>
</dt> <dd>

<span data-ttu-id="d145d-116">Указатель на структуру [**\_ \_ \_ пармс сеттунер видеомагнитофона MCI**](mci-vcr-settuner-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d145d-116">Pointer to an [**MCI\_VCR\_SETTUNER\_PARMS**](mci-vcr-settuner-parms.md) structure.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d145d-117">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d145d-117">Return Value</span></span>

<span data-ttu-id="d145d-118">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d145d-118">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d145d-119">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d145d-119">Remarks</span></span>

<span data-ttu-id="d145d-120">Следующие дополнительные флаги применяются к устройствам ВИДЕОМАГНИТОФОНА:</span><span class="sxs-lookup"><span data-stu-id="d145d-120">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="d145d-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>\_ \_ канал СЕТТУНЕР видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="d145d-121"><span id="MCI_VCR_SETTUNER_CHANNEL"></span><span id="mci_vcr_settuner_channel"></span>MCI\_VCR\_SETTUNER\_CHANNEL</span></span>
</dt> <dd>

<span data-ttu-id="d145d-122">Элемент **двчаннел** структуры, идентифицируемой *лпсеттунер* , содержит новый номер канала.</span><span class="sxs-lookup"><span data-stu-id="d145d-122">The **dwChannel** member of the structure identified by *lpSetTuner* contains the new channel number.</span></span>

</dd> <dt>

<span data-ttu-id="d145d-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>\_ \_ канал СЕТТУНЕР видеомагнитофона \_ MCI \_</span><span class="sxs-lookup"><span data-stu-id="d145d-123"><span id="MCI_VCR_SETTUNER_CHANNEL_DOWN"></span><span id="mci_vcr_settuner_channel_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="d145d-124">Уменьшает канал тюнера.</span><span class="sxs-lookup"><span data-stu-id="d145d-124">Decrements the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="d145d-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>\_ \_ \_ Поиск канала сеттунер \_ видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="d145d-125"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_DOWN"></span><span id="mci_vcr_settuner_channel_seek_down"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_DOWN</span></span>
</dt> <dd>

<span data-ttu-id="d145d-126">Выполняет поиск допустимого канала в обратном направлении.</span><span class="sxs-lookup"><span data-stu-id="d145d-126">Searches for a valid channel in the reverse direction.</span></span>

</dd> <dt>

<span data-ttu-id="d145d-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>\_ \_ \_ Поиск канала сеттунер \_ видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="d145d-127"><span id="MCI_VCR_SETTUNER_CHANNEL_SEEK_UP"></span><span id="mci_vcr_settuner_channel_seek_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_SEEK\_UP</span></span>
</dt> <dd>

<span data-ttu-id="d145d-128">Выполняет поиск допустимого канала в прямом направлении.</span><span class="sxs-lookup"><span data-stu-id="d145d-128">Searches for a valid channel in the forward direction.</span></span>

</dd> <dt>

<span data-ttu-id="d145d-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>\_канал MCI \_ сеттунер \_ Channel \_ up</span><span class="sxs-lookup"><span data-stu-id="d145d-129"><span id="MCI_VCR_SETTUNER_CHANNEL_UP"></span><span id="mci_vcr_settuner_channel_up"></span>MCI\_VCR\_SETTUNER\_CHANNEL\_UP</span></span>
</dt> <dd>

<span data-ttu-id="d145d-130">Увеличивает канал тюнера.</span><span class="sxs-lookup"><span data-stu-id="d145d-130">Increments the tuner channel.</span></span>

</dd> <dt>

<span data-ttu-id="d145d-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>\_ \_ номер СЕТТУНЕР видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="d145d-131"><span id="MCI_VCR_SETTUNER_NUMBER"></span><span id="mci_vcr_settuner_number"></span>MCI\_VCR\_SETTUNER\_NUMBER</span></span>
</dt> <dd>

<span data-ttu-id="d145d-132">Элемент **двнумбер** структуры, определяемой параметром *лпсеттунер* , указывает, какой логический тюнер будет влиять на эту команду.</span><span class="sxs-lookup"><span data-stu-id="d145d-132">The **dwNumber** member of the structure identified by *lpSetTuner* specifies which logical tuner to affect with this command.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d145d-133">Требования</span><span class="sxs-lookup"><span data-stu-id="d145d-133">Requirements</span></span>



| <span data-ttu-id="d145d-134">Требование</span><span class="sxs-lookup"><span data-stu-id="d145d-134">Requirement</span></span> | <span data-ttu-id="d145d-135">Значение</span><span class="sxs-lookup"><span data-stu-id="d145d-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d145d-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d145d-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d145d-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d145d-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d145d-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d145d-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d145d-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d145d-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d145d-140">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d145d-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="d145d-141"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d145d-141"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d145d-142">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d145d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d145d-143">MCI</span><span class="sxs-lookup"><span data-stu-id="d145d-143">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d145d-144">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="d145d-144">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

