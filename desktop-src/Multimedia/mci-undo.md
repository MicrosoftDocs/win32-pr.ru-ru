---
title: Команда MCI_UNDO (Ммсистем. h)
description: '\_Команда отмены MCI обращается к последней успешной \_ команде MCI вырезать, MCI \_ Copy, MCI \_ DELETE или команды MCI \_ Paste. Устройство Digital-Video распознает эту команду.'
ms.assetid: 1593457a-e680-4732-a89e-00f4eff7605a
keywords:
- MCI_UNDO команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_UNDO
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d099d95159afee8d91acb77eb64e8e80bee5425d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071237"
---
# <a name="mci_undo-command"></a><span data-ttu-id="d2ecd-105">\_Команда отмены MCI</span><span class="sxs-lookup"><span data-stu-id="d2ecd-105">MCI\_UNDO command</span></span>

<span data-ttu-id="d2ecd-106">\_Команда отмены MCI обращается к последней успешной команде [MCI \_ Вырезать](mci-cut.md), [MCI \_ Copy](mci-copy.md), [MCI \_ Delete](mci-delete.md)или команды [MCI \_ Paste](mci-paste.md) .</span><span class="sxs-lookup"><span data-stu-id="d2ecd-106">The MCI\_UNDO command reverses the most recent successful [MCI\_CUT](mci-cut.md), [MCI\_COPY](mci-copy.md), [MCI\_DELETE](mci-delete.md), or [MCI\_PASTE](mci-paste.md) command.</span></span> <span data-ttu-id="d2ecd-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="d2ecd-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="d2ecd-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="d2ecd-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_UNDO, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpUndo
);
```



## <a name="parameters"></a><span data-ttu-id="d2ecd-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d2ecd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d2ecd-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="d2ecd-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d2ecd-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="d2ecd-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="d2ecd-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="d2ecd-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d2ecd-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="d2ecd-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="d2ecd-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d2ecd-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="d2ecd-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*лпундо*</span><span class="sxs-lookup"><span data-stu-id="d2ecd-115"><span id="lpUndo"></span><span id="lpundo"></span><span id="LPUNDO"></span>*lpUndo*</span></span>
</dt> <dd>

<span data-ttu-id="d2ecd-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="d2ecd-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="d2ecd-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="d2ecd-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d2ecd-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d2ecd-118">Return Value</span></span>

<span data-ttu-id="d2ecd-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d2ecd-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2ecd-120">Требования</span><span class="sxs-lookup"><span data-stu-id="d2ecd-120">Requirements</span></span>



| <span data-ttu-id="d2ecd-121">Требование</span><span class="sxs-lookup"><span data-stu-id="d2ecd-121">Requirement</span></span> | <span data-ttu-id="d2ecd-122">Значение</span><span class="sxs-lookup"><span data-stu-id="d2ecd-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ecd-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d2ecd-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ecd-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d2ecd-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="d2ecd-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d2ecd-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ecd-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d2ecd-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="d2ecd-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d2ecd-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d2ecd-128"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d2ecd-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2ecd-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d2ecd-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ecd-130">MCI</span><span class="sxs-lookup"><span data-stu-id="d2ecd-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d2ecd-131">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="d2ecd-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

