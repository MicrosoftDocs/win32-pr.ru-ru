---
title: Escape-команда
description: Управляющая команда отправляет сведения об устройстве на устройство. Устройства видеодиск распознают эту команду.
ms.assetid: 16e0e2b6-6d98-440a-86c1-eca8201ad61a
keywords:
- Экранирование команд Windows мультимедиа
topic_type:
- apiref
api_name:
- escape
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b04f7a2ef6c2e91adc9b24a044d0a7e941843f9e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105650362"
---
# <a name="escape-command"></a><span data-ttu-id="ff1a2-105">Escape-команда</span><span class="sxs-lookup"><span data-stu-id="ff1a2-105">escape command</span></span>

<span data-ttu-id="ff1a2-106">Управляющая команда отправляет сведения об устройстве на устройство.</span><span class="sxs-lookup"><span data-stu-id="ff1a2-106">The escape command sends device-specific information to a device.</span></span> <span data-ttu-id="ff1a2-107">Устройства видеодиск распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="ff1a2-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="ff1a2-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ff1a2-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("escape %s %s %s"), 
  lpszDeviceID, 
  lpszEscape, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="ff1a2-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="ff1a2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff1a2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="ff1a2-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ff1a2-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="ff1a2-111">Identifier of an MCI device.</span></span> <span data-ttu-id="ff1a2-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="ff1a2-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="ff1a2-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*лпсзескапе*</span><span class="sxs-lookup"><span data-stu-id="ff1a2-113"><span id="lpszEscape"></span><span id="lpszescape"></span><span id="LPSZESCAPE"></span>*lpszEscape*</span></span>
</dt> <dd>

<span data-ttu-id="ff1a2-114">Пользовательские данные для отправки на устройство.</span><span class="sxs-lookup"><span data-stu-id="ff1a2-114">Custom information to send to the device.</span></span>

</dd> <dt>

<span data-ttu-id="ff1a2-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="ff1a2-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ff1a2-116">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="ff1a2-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="ff1a2-117">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ff1a2-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff1a2-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ff1a2-118">Return Value</span></span>

<span data-ttu-id="ff1a2-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ff1a2-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="ff1a2-120">Примеры</span><span class="sxs-lookup"><span data-stu-id="ff1a2-120">Examples</span></span>

<span data-ttu-id="ff1a2-121">Следующая команда отправляет escape-строку "SA" на устройство видеодиск.</span><span class="sxs-lookup"><span data-stu-id="ff1a2-121">The following command sends the escape string "SA" to the videodisc device.</span></span>

``` syntax
escape videodisc SA
```

## <a name="requirements"></a><span data-ttu-id="ff1a2-122">Требования</span><span class="sxs-lookup"><span data-stu-id="ff1a2-122">Requirements</span></span>



| <span data-ttu-id="ff1a2-123">Требование</span><span class="sxs-lookup"><span data-stu-id="ff1a2-123">Requirement</span></span> | <span data-ttu-id="ff1a2-124">Значение</span><span class="sxs-lookup"><span data-stu-id="ff1a2-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ff1a2-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ff1a2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ff1a2-126">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ff1a2-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ff1a2-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ff1a2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ff1a2-128">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ff1a2-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ff1a2-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ff1a2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff1a2-130">MCI</span><span class="sxs-lookup"><span data-stu-id="ff1a2-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ff1a2-131">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="ff1a2-131">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

