---
title: Команда MCI_CONFIGURE (Ммсистем. h)
description: Команда MCI \_ Configure выводит диалоговое окно для настройки параметров операционной системы. Устройство Digital-Video распознает эту команду.
ms.assetid: 92683579-e6af-42a7-8a0f-6b88b04441f2
keywords:
- MCI_CONFIGURE команды мультимедиа Windows
topic_type:
- apiref
api_name:
- MCI_CONFIGURE
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f752f17ac0d0a5c04edf628edfb6c04a339783f5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104414857"
---
# <a name="mci_configure-command"></a><span data-ttu-id="a317e-105">\_Команда настройки MCI</span><span class="sxs-lookup"><span data-stu-id="a317e-105">MCI\_CONFIGURE command</span></span>

<span data-ttu-id="a317e-106">Команда MCI \_ Configure выводит диалоговое окно для настройки параметров операционной системы.</span><span class="sxs-lookup"><span data-stu-id="a317e-106">The MCI\_CONFIGURE command displays a dialog box for setting the operating options.</span></span> <span data-ttu-id="a317e-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="a317e-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="a317e-108">Чтобы отправить эту команду, вызовите функцию [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) со следующими параметрами.</span><span class="sxs-lookup"><span data-stu-id="a317e-108">To send this command, call the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function with the following parameters.</span></span>


```C++
MCIERROR mciSendCommand(
  MCIDEVICEID wDeviceID, 
  MCI_CONFIGURE, 
  DWORD dwFlags, 
  (DWORD) (LPMCI_GENERIC_PARMS) lpConfigure
);
```



## <a name="parameters"></a><span data-ttu-id="a317e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a317e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a317e-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*вдевицеид*</span><span class="sxs-lookup"><span data-stu-id="a317e-110"><span id="wDeviceID"></span><span id="wdeviceid"></span><span id="WDEVICEID"></span>*wDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a317e-111">Идентификатор устройства MCI, который должен получить командное сообщение.</span><span class="sxs-lookup"><span data-stu-id="a317e-111">Device identifier of the MCI device that is to receive the command message.</span></span>

</dd> <dt>

<span data-ttu-id="a317e-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="a317e-112"><span id="dwFlags"></span><span id="dwflags"></span><span id="DWFLAGS"></span>*dwFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a317e-113">\_Уведомление MCI, \_ Ожидание MCI или \_ тест MCI.</span><span class="sxs-lookup"><span data-stu-id="a317e-113">MCI\_NOTIFY, MCI\_WAIT, or MCI\_TEST.</span></span> <span data-ttu-id="a317e-114">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a317e-114">For information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="a317e-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*лпконфигуре*</span><span class="sxs-lookup"><span data-stu-id="a317e-115"><span id="lpConfigure"></span><span id="lpconfigure"></span><span id="LPCONFIGURE"></span>*lpConfigure*</span></span>
</dt> <dd>

<span data-ttu-id="a317e-116">Указатель на [**общую структуру \_ \_ пармс MCI**](mci-generic-parms.md) .</span><span class="sxs-lookup"><span data-stu-id="a317e-116">Pointer to an [**MCI\_GENERIC\_PARMS**](mci-generic-parms.md) structure.</span></span> <span data-ttu-id="a317e-117">(Устройства с расширенными наборами команд могут заменить эту структуру структурой, зависящей от устройства.)</span><span class="sxs-lookup"><span data-stu-id="a317e-117">(Devices with extended command sets might replace this structure with a device-specific structure.)</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a317e-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a317e-118">Return Value</span></span>

<span data-ttu-id="a317e-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a317e-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a317e-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a317e-120">Requirements</span></span>



| <span data-ttu-id="a317e-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a317e-121">Requirement</span></span> | <span data-ttu-id="a317e-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a317e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a317e-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a317e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a317e-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a317e-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="a317e-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a317e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a317e-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a317e-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="a317e-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a317e-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a317e-128"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a317e-128"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a317e-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a317e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a317e-130">MCI</span><span class="sxs-lookup"><span data-stu-id="a317e-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a317e-131">Команды MCI</span><span class="sxs-lookup"><span data-stu-id="a317e-131">MCI Commands</span></span>](mci-commands.md)
</dt> </dl>

 

