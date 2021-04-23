---
title: Команда MCI_INDEX (Ммсистем. h)
description: '\_Команда указателя MCI включает или выключает экран на экране. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.'
ms.assetid: c0f18f28-3578-4648-9b75-2d3ede68b3df
keywords:
- MCI_INDEX команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_INDEX
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e93890b8c3db1150bc7224b0fd8b6ee7475ced
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137582"
---
# <a name="mci_index-command"></a><span data-ttu-id="6108e-105">\_Команда указателя MCI</span><span class="sxs-lookup"><span data-stu-id="6108e-105">MCI\_INDEX command</span></span>

<span data-ttu-id="6108e-106">\_Команда указателя MCI включает или выключает экран на экране.</span><span class="sxs-lookup"><span data-stu-id="6108e-106">The MCI\_INDEX command turns the on-screen display on or off.</span></span> <span data-ttu-id="6108e-107">Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="6108e-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="6108e-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="6108e-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_INDEX, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpIndex
);
```



## <a name="parameters"></a><span data-ttu-id="6108e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="6108e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6108e-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="6108e-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="6108e-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="6108e-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="6108e-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="6108e-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="6108e-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="6108e-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="6108e-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="6108e-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="6108e-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*лпиндекс*</span><span class="sxs-lookup"><span data-stu-id="6108e-115"><span id="lpIndex"></span><span id="lpindex"></span><span id="LPINDEX"></span>*lpIndex*</span></span>
</dt> <dd>

<span data-ttu-id="6108e-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="6108e-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="6108e-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="6108e-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6108e-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6108e-118">Return Value</span></span>

<span data-ttu-id="6108e-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6108e-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6108e-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6108e-120">Remarks</span></span>

<span data-ttu-id="6108e-121">Сведения, представленные на экране экрана, контролируются \_ \_ флагом индекса набора видеомагнитофона MCI \_ в команде [MCI \_ Set](mci-set.md) .</span><span class="sxs-lookup"><span data-stu-id="6108e-121">The information presented in the on-screen display is controlled by the MCI\_VCR\_SET\_INDEX flag in the [MCI\_SET](mci-set.md) command.</span></span>

<span data-ttu-id="6108e-122">Следующие дополнительные флаги применяются к устройствам ВИДЕОМАГНИТОФОНА:</span><span class="sxs-lookup"><span data-stu-id="6108e-122">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="6108e-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI \_ установлен \_</span><span class="sxs-lookup"><span data-stu-id="6108e-123"><span id="MCI_SET_OFF"></span><span id="mci_set_off"></span>MCI\_SET\_OFF</span></span>
</dt> <dd>

<span data-ttu-id="6108e-124">Включает экран.</span><span class="sxs-lookup"><span data-stu-id="6108e-124">Turns on-screen display off.</span></span>

</dd> <dt>

<span data-ttu-id="6108e-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI \_ задан \_ на</span><span class="sxs-lookup"><span data-stu-id="6108e-125"><span id="MCI_SET_ON"></span><span id="mci_set_on"></span>MCI\_SET\_ON</span></span>
</dt> <dd>

<span data-ttu-id="6108e-126">Включает экран на экране.</span><span class="sxs-lookup"><span data-stu-id="6108e-126">Turns on-screen display on.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6108e-127">Требования</span><span class="sxs-lookup"><span data-stu-id="6108e-127">Requirements</span></span>



| <span data-ttu-id="6108e-128">Требование</span><span class="sxs-lookup"><span data-stu-id="6108e-128">Requirement</span></span> | <span data-ttu-id="6108e-129">Значение</span><span class="sxs-lookup"><span data-stu-id="6108e-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6108e-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6108e-130">Minimum supported client</span></span><br/> | <span data-ttu-id="6108e-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6108e-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="6108e-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6108e-132">Minimum supported server</span></span><br/> | <span data-ttu-id="6108e-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6108e-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="6108e-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6108e-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="6108e-135"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6108e-135"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6108e-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6108e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6108e-137">MCI</span><span class="sxs-lookup"><span data-stu-id="6108e-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="6108e-138">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="6108e-138">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

