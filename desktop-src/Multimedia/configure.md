---
title: Настройка команды
description: Команда configure выводит диалоговое окно, используемое для настройки устройства. Устройство Digital-Video распознает эту команду.
ms.assetid: 17d99992-f432-4b8a-ae98-2a70637c29c3
keywords:
- Настройка команд мультимедиа Windows
topic_type:
- apiref
api_name:
- configure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61f131159d389577e3c717e5630633bb46558d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801030"
---
# <a name="configure-command"></a><span data-ttu-id="56c1f-105">Настройка команды</span><span class="sxs-lookup"><span data-stu-id="56c1f-105">configure command</span></span>

<span data-ttu-id="56c1f-106">Команда configure выводит диалоговое окно, используемое для настройки устройства.</span><span class="sxs-lookup"><span data-stu-id="56c1f-106">The configure command displays a dialog box used to configure the device.</span></span> <span data-ttu-id="56c1f-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="56c1f-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="56c1f-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="56c1f-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("configure %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="56c1f-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="56c1f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56c1f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="56c1f-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="56c1f-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="56c1f-111">Identifier of an MCI device.</span></span> <span data-ttu-id="56c1f-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="56c1f-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="56c1f-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="56c1f-113"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="56c1f-114">Может принимать значение "Wait", "notify" или "Test".</span><span class="sxs-lookup"><span data-stu-id="56c1f-114">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="56c1f-115">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="56c1f-115">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56c1f-116">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="56c1f-116">Return Value</span></span>

<span data-ttu-id="56c1f-117">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="56c1f-117">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="56c1f-118">Требования</span><span class="sxs-lookup"><span data-stu-id="56c1f-118">Requirements</span></span>



| <span data-ttu-id="56c1f-119">Требование</span><span class="sxs-lookup"><span data-stu-id="56c1f-119">Requirement</span></span> | <span data-ttu-id="56c1f-120">Значение</span><span class="sxs-lookup"><span data-stu-id="56c1f-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="56c1f-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="56c1f-121">Minimum supported client</span></span><br/> | <span data-ttu-id="56c1f-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="56c1f-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="56c1f-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="56c1f-123">Minimum supported server</span></span><br/> | <span data-ttu-id="56c1f-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="56c1f-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="56c1f-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="56c1f-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56c1f-126">MCI</span><span class="sxs-lookup"><span data-stu-id="56c1f-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="56c1f-127">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="56c1f-127">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

