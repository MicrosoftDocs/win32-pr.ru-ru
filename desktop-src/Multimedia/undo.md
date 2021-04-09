---
title: Команда "отменить"
description: Команда Undo отменяет действие, выполняемое последней успешной командой копирования, вырезания, удаления, отмены или вставки. Устройство Digital-Video распознает эту команду.
ms.assetid: 81d696a9-5288-4efd-bc76-8416dd63e694
keywords:
- Команда "отменить" Windows мультимедиа
topic_type:
- apiref
api_name:
- undo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfc0814dff2c684095299b6820b8dc9a2464aa26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071989"
---
# <a name="undo-command"></a><span data-ttu-id="7f8ea-105">Команда "отменить"</span><span class="sxs-lookup"><span data-stu-id="7f8ea-105">undo command</span></span>

<span data-ttu-id="7f8ea-106">Команда Undo отменяет действие, выполняемое последней успешной командой [копирования](copy.md), [вырезания](cut.md), [удаления](delete.md), отмены или [вставки](paste.md) .</span><span class="sxs-lookup"><span data-stu-id="7f8ea-106">The undo command reverses the action taken by the most recent successful [copy](copy.md), [cut](cut.md), [delete](delete.md), undo, or [paste](paste.md) command.</span></span> <span data-ttu-id="7f8ea-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="7f8ea-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="7f8ea-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="7f8ea-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("undo %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="7f8ea-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="7f8ea-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f8ea-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="7f8ea-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="7f8ea-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="7f8ea-111">Identifier of an MCI device.</span></span> <span data-ttu-id="7f8ea-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="7f8ea-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="7f8ea-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="7f8ea-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="7f8ea-114">Может принимать значение "Wait", "notify", "Test" или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="7f8ea-114">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="7f8ea-115">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="7f8ea-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f8ea-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7f8ea-116">Return Value</span></span>

<span data-ttu-id="7f8ea-117">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="7f8ea-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f8ea-118">Требования</span><span class="sxs-lookup"><span data-stu-id="7f8ea-118">Requirements</span></span>



| <span data-ttu-id="7f8ea-119">Требование</span><span class="sxs-lookup"><span data-stu-id="7f8ea-119">Requirement</span></span> | <span data-ttu-id="7f8ea-120">Значение</span><span class="sxs-lookup"><span data-stu-id="7f8ea-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="7f8ea-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7f8ea-121">Minimum supported client</span></span><br/> | <span data-ttu-id="7f8ea-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f8ea-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="7f8ea-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7f8ea-123">Minimum supported server</span></span><br/> | <span data-ttu-id="7f8ea-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="7f8ea-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="7f8ea-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7f8ea-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f8ea-126">MCI</span><span class="sxs-lookup"><span data-stu-id="7f8ea-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="7f8ea-127">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="7f8ea-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="7f8ea-128">copy</span><span class="sxs-lookup"><span data-stu-id="7f8ea-128">copy</span></span>](copy.md)
</dt> <dt>

[<span data-ttu-id="7f8ea-129">бавьте</span><span class="sxs-lookup"><span data-stu-id="7f8ea-129">cut</span></span>](cut.md)
</dt> <dt>

[<span data-ttu-id="7f8ea-130">delete</span><span class="sxs-lookup"><span data-stu-id="7f8ea-130">delete</span></span>](delete.md)
</dt> <dt>

[<span data-ttu-id="7f8ea-131">авить</span><span class="sxs-lookup"><span data-stu-id="7f8ea-131">paste</span></span>](paste.md)
</dt> </dl>

 

