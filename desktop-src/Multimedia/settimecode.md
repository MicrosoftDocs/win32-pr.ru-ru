---
title: Команда сеттимекоде
description: Команда сеттимекоде включает или отключает запись времени в видеомагнитофоне. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.
ms.assetid: 1b4b82e8-4f13-4bc9-afb0-796339cabb51
keywords:
- Команда сеттимекоде мультимедиа Windows
topic_type:
- apiref
api_name:
- settimecode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 32092e5af7c77cdc274491b20663218d39a1ec1a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103804078"
---
# <a name="settimecode-command"></a><span data-ttu-id="a73cb-105">Команда сеттимекоде</span><span class="sxs-lookup"><span data-stu-id="a73cb-105">settimecode command</span></span>

<span data-ttu-id="a73cb-106">Команда сеттимекоде включает или отключает запись времени в видеомагнитофоне.</span><span class="sxs-lookup"><span data-stu-id="a73cb-106">The settimecode command enables or disables timecode recording for a VCR.</span></span> <span data-ttu-id="a73cb-107">Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="a73cb-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="a73cb-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="a73cb-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("settimecode %s %s %s"), 
  lpszDeviceID,
  lpszTimecode, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="a73cb-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="a73cb-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a73cb-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="a73cb-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="a73cb-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="a73cb-111">Identifier of an MCI device.</span></span> <span data-ttu-id="a73cb-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="a73cb-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="a73cb-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*лпсзтимекоде*</span><span class="sxs-lookup"><span data-stu-id="a73cb-113"><span id="lpszTimecode"></span><span id="lpsztimecode"></span><span id="LPSZTIMECODE"></span>*lpszTimecode*</span></span>
</dt> <dd>

<span data-ttu-id="a73cb-114">Один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="a73cb-114">One of the following flags.</span></span>



| <span data-ttu-id="a73cb-115">Значение</span><span class="sxs-lookup"><span data-stu-id="a73cb-115">Value</span></span>      | <span data-ttu-id="a73cb-116">Значение</span><span class="sxs-lookup"><span data-stu-id="a73cb-116">Meaning</span></span>                          |
|------------|----------------------------------|
| <span data-ttu-id="a73cb-117">запись в</span><span class="sxs-lookup"><span data-stu-id="a73cb-117">record on</span></span>  | <span data-ttu-id="a73cb-118">Задает запись времени в ВИДЕОМАГНИТОФОН.</span><span class="sxs-lookup"><span data-stu-id="a73cb-118">Sets the VCR to record timecode.</span></span> |
| <span data-ttu-id="a73cb-119">запись отключена</span><span class="sxs-lookup"><span data-stu-id="a73cb-119">record off</span></span> | <span data-ttu-id="a73cb-120">Отключает запись времени.</span><span class="sxs-lookup"><span data-stu-id="a73cb-120">Disables timecode recording.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="a73cb-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="a73cb-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="a73cb-122">Может принимать значение "Wait", "notify", "Test" или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="a73cb-122">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="a73cb-123">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="a73cb-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a73cb-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a73cb-124">Return Value</span></span>

<span data-ttu-id="a73cb-125">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="a73cb-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="a73cb-126">Требования</span><span class="sxs-lookup"><span data-stu-id="a73cb-126">Requirements</span></span>



| <span data-ttu-id="a73cb-127">Требование</span><span class="sxs-lookup"><span data-stu-id="a73cb-127">Requirement</span></span> | <span data-ttu-id="a73cb-128">Значение</span><span class="sxs-lookup"><span data-stu-id="a73cb-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="a73cb-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a73cb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a73cb-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a73cb-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="a73cb-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a73cb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a73cb-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a73cb-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a73cb-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a73cb-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a73cb-134">MCI</span><span class="sxs-lookup"><span data-stu-id="a73cb-134">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="a73cb-135">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="a73cb-135">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

