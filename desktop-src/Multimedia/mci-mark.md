---
title: Команда MCI_MARK (Ммсистем. h)
description: Команда MCI \_ Mark записывает или стирает метки, которые можно использовать с \_ командой MCI Seek для высокоскоростных поисков. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.
ms.assetid: 69b17e5b-99a1-4fb9-bc0e-30e772c1f11f
keywords:
- MCI_MARK команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_MARK
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ddc80decb4559659efb29132f17f18459c334fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071315"
---
# <a name="mci_mark-command"></a><span data-ttu-id="49e60-105">\_Команда ДЕЛЕНИЯ MCI</span><span class="sxs-lookup"><span data-stu-id="49e60-105">MCI\_MARK command</span></span>

<span data-ttu-id="49e60-106">Команда MCI \_ Mark записывает или стирает метки, которые можно использовать с командой [MCI \_ Seek](mci-seek.md) для высокоскоростных поисков.</span><span class="sxs-lookup"><span data-stu-id="49e60-106">The MCI\_MARK command records or erases marks that can be used with the [MCI\_SEEK](mci-seek.md) command for high-speed searches.</span></span> <span data-ttu-id="49e60-107">Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="49e60-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="49e60-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="49e60-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_MARK, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpMark
);
```



## <a name="parameters"></a><span data-ttu-id="49e60-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="49e60-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49e60-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="49e60-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="49e60-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="49e60-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="49e60-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="49e60-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="49e60-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="49e60-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="49e60-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="49e60-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="49e60-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*лпмарк*</span><span class="sxs-lookup"><span data-stu-id="49e60-115"><span id="lpMark"></span><span id="lpmark"></span><span id="LPMARK"></span>*lpMark*</span></span>
</dt> <dd>

<span data-ttu-id="49e60-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="49e60-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="49e60-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="49e60-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49e60-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="49e60-118">Return Value</span></span>

<span data-ttu-id="49e60-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="49e60-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="49e60-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="49e60-120">Remarks</span></span>

<span data-ttu-id="49e60-121">Следующие дополнительные флаги применяются к устройствам ВИДЕОМАГНИТОФОНА:</span><span class="sxs-lookup"><span data-stu-id="49e60-121">The following additional flags apply to VCR devices:</span></span>

<dl> <dt>

<span data-ttu-id="49e60-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>\_ \_ стирание метки видеомагнитофона \_ видеомагнитофон</span><span class="sxs-lookup"><span data-stu-id="49e60-122"><span id="MCI_VCR_MARK_ERASE"></span><span id="mci_vcr_mark_erase"></span>MCI\_VCR\_MARK\_ERASE</span></span>
</dt> <dd>

<span data-ttu-id="49e60-123">Удаляет метку в текущей позиции, если она существует.</span><span class="sxs-lookup"><span data-stu-id="49e60-123">Erases a mark at the current position if one exists.</span></span>

</dd> <dt>

<span data-ttu-id="49e60-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>\_ \_ запись маркера видеомагнитофона MCI \_</span><span class="sxs-lookup"><span data-stu-id="49e60-124"><span id="MCI_VCR_MARK_WRITE"></span><span id="mci_vcr_mark_write"></span>MCI\_VCR\_MARK\_WRITE</span></span>
</dt> <dd>

<span data-ttu-id="49e60-125">Записывает метку в текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="49e60-125">Writes a mark at the current position.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="49e60-126">Требования</span><span class="sxs-lookup"><span data-stu-id="49e60-126">Requirements</span></span>



| <span data-ttu-id="49e60-127">Требование</span><span class="sxs-lookup"><span data-stu-id="49e60-127">Requirement</span></span> | <span data-ttu-id="49e60-128">Значение</span><span class="sxs-lookup"><span data-stu-id="49e60-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="49e60-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="49e60-129">Minimum supported client</span></span><br/> | <span data-ttu-id="49e60-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="49e60-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="49e60-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="49e60-131">Minimum supported server</span></span><br/> | <span data-ttu-id="49e60-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="49e60-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="49e60-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="49e60-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="49e60-134"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="49e60-134"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49e60-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="49e60-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e60-136">MCI</span><span class="sxs-lookup"><span data-stu-id="49e60-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="49e60-137">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="49e60-137">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

