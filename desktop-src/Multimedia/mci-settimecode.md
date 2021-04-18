---
title: Команда MCI_SETTIMECODE (Ммсистем. h)
description: Команда MCI \_ сеттимекоде включает или отключает запись времени для видеомагнитофона. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.
ms.assetid: b014fbe0-de97-4540-a5fe-b22d157361f7
keywords:
- MCI_SETTIMECODE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_SETTIMECODE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7df0727f4386bad46b3fde7f2d816ce951850b8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672889"
---
# <a name="mci_settimecode-command"></a><span data-ttu-id="074cd-105">\_Команда MCI сеттимекоде</span><span class="sxs-lookup"><span data-stu-id="074cd-105">MCI\_SETTIMECODE command</span></span>

<span data-ttu-id="074cd-106">Команда MCI \_ сеттимекоде включает или отключает запись времени для видеомагнитофона.</span><span class="sxs-lookup"><span data-stu-id="074cd-106">The MCI\_SETTIMECODE command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="074cd-107">Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="074cd-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="074cd-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="074cd-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_SETTIMECODE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpSetTimeCode
);
```



## <a name="parameters"></a><span data-ttu-id="074cd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="074cd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="074cd-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="074cd-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="074cd-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="074cd-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="074cd-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="074cd-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="074cd-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="074cd-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="074cd-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="074cd-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="074cd-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*лпсеттимекоде*</span><span class="sxs-lookup"><span data-stu-id="074cd-115"><span id="lpSetTimeCode"></span><span id="lpsettimecode"></span><span id="LPSETTIMECODE"></span>*lpSetTimeCode*</span></span>
</dt> <dd>

<span data-ttu-id="074cd-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="074cd-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="074cd-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="074cd-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="074cd-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="074cd-118">Return Value</span></span>

<span data-ttu-id="074cd-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="074cd-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="074cd-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="074cd-120">Remarks</span></span>

<span data-ttu-id="074cd-121">К устройствам ВИДЕОМАГНИТОФОНА применяется следующий дополнительный флаг:</span><span class="sxs-lookup"><span data-stu-id="074cd-121">The following additional flag applies to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="074cd-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>\_ \_ запись СЕТТИМЕКОДЕ видеомагнитофона \_ MCI</span><span class="sxs-lookup"><span data-stu-id="074cd-122"><span id="MCI_VCR_SETTIMECODE_RECORD"></span><span id="mci_vcr_settimecode_record"></span>MCI\_VCR\_SETTIMECODE\_RECORD</span></span>
</dt> <dd>

<span data-ttu-id="074cd-123">Задает значение ON или OFF для записи времени.</span><span class="sxs-lookup"><span data-stu-id="074cd-123">Sets the timecode track recording to on or off.</span></span> <span data-ttu-id="074cd-124">Этот флаг используется в сочетании с одним из следующих дополнительных флагов:</span><span class="sxs-lookup"><span data-stu-id="074cd-124">This flag is used in combination with one of the following additional flags:</span></span>

</dd> <dt>

<span data-ttu-id="074cd-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ задан \_ на</span><span class="sxs-lookup"><span data-stu-id="074cd-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="074cd-126">Запись времени по времени в.</span><span class="sxs-lookup"><span data-stu-id="074cd-126">Timecode recording on.</span></span>

</dd> <dt>

<span data-ttu-id="074cd-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ установлен \_</span><span class="sxs-lookup"><span data-stu-id="074cd-127"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="074cd-128">Запись времени начала.</span><span class="sxs-lookup"><span data-stu-id="074cd-128">Timecode recording off.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="074cd-129">Требования</span><span class="sxs-lookup"><span data-stu-id="074cd-129">Requirements</span></span>



| <span data-ttu-id="074cd-130">Требование</span><span class="sxs-lookup"><span data-stu-id="074cd-130">Requirement</span></span> | <span data-ttu-id="074cd-131">Значение</span><span class="sxs-lookup"><span data-stu-id="074cd-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="074cd-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="074cd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="074cd-133">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="074cd-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="074cd-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="074cd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="074cd-135">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="074cd-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="074cd-136">Заголовок</span><span class="sxs-lookup"><span data-stu-id="074cd-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="074cd-137"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="074cd-137"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="074cd-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="074cd-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="074cd-139">MCI</span><span class="sxs-lookup"><span data-stu-id="074cd-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="074cd-140">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="074cd-140">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

