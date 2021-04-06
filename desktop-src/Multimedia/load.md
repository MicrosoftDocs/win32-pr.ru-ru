---
title: Команда Load
description: Команда Load загружает файл в формате, характерном для устройства. Эта команда распознает цифровые видеоролики и устройства наложения видео.
ms.assetid: ae7bfe92-7957-4756-a408-e3ab60dd9aa4
keywords:
- Загрузка команды Windows мультимедиа
topic_type:
- apiref
api_name:
- load
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b199a6d3aea8a2697217eb75176c24b2b0bc2e2a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803022"
---
# <a name="load-command"></a><span data-ttu-id="0da2e-105">Команда Load</span><span class="sxs-lookup"><span data-stu-id="0da2e-105">load command</span></span>

<span data-ttu-id="0da2e-106">Команда Load загружает файл в формате, характерном для устройства.</span><span class="sxs-lookup"><span data-stu-id="0da2e-106">The load command loads a file in a device-specific format.</span></span> <span data-ttu-id="0da2e-107">Эта команда распознает цифровые видеоролики и устройства наложения видео.</span><span class="sxs-lookup"><span data-stu-id="0da2e-107">Digital-video and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="0da2e-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="0da2e-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("load %s %s %s"), 
  lpszDeviceID, 
  lpszFilePos, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="0da2e-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="0da2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0da2e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="0da2e-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="0da2e-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="0da2e-111">Identifier of an MCI device.</span></span> <span data-ttu-id="0da2e-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="0da2e-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="0da2e-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*лпсзфилепос*</span><span class="sxs-lookup"><span data-stu-id="0da2e-113"><span id="lpszFilePos"></span><span id="lpszfilepos"></span><span id="LPSZFILEPOS"></span>*lpszFilePos*</span></span>
</dt> <dd>

<span data-ttu-id="0da2e-114">Путь и имя файла для загрузки.</span><span class="sxs-lookup"><span data-stu-id="0da2e-114">Path and filename to load.</span></span> <span data-ttu-id="0da2e-115">Для устройств с наложением видео это также может включать целевой прямоугольник для данных.</span><span class="sxs-lookup"><span data-stu-id="0da2e-115">For video-overlay devices, this can also include a target rectangle for the data.</span></span> <span data-ttu-id="0da2e-116">Чтобы указать целевой прямоугольник, укажите "at", за которым следует **x1 Y1 x2 Y2**, где **x1 Y1** укажите верхний левый угол прямоугольника, а **x2 Y2** — ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="0da2e-116">To specify a target rectangle, specify "at" followed by **X1 Y1 X2 Y2**, where **X1 Y1** specify the upper left corner of the rectangle, and **X2 Y2** specify the width and height.</span></span> <span data-ttu-id="0da2e-117">Прямоугольник задается относительно источника видеобуфера.</span><span class="sxs-lookup"><span data-stu-id="0da2e-117">The rectangle is relative to the video buffer origin.</span></span>

</dd> <dt>

<span data-ttu-id="0da2e-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="0da2e-118"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="0da2e-119">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="0da2e-119">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="0da2e-120">Для устройств Digital-Video также можно указать "Test".</span><span class="sxs-lookup"><span data-stu-id="0da2e-120">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="0da2e-121">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="0da2e-121">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0da2e-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0da2e-122">Return Value</span></span>

<span data-ttu-id="0da2e-123">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0da2e-123">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="0da2e-124">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0da2e-124">Remarks</span></span>

<span data-ttu-id="0da2e-125">Устройство "видбоард" отправляет сообщение с уведомлением о завершении загрузки.</span><span class="sxs-lookup"><span data-stu-id="0da2e-125">The "vidboard" device sends a notification message when the loading is completed.</span></span>

## <a name="examples"></a><span data-ttu-id="0da2e-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="0da2e-126">Examples</span></span>

<span data-ttu-id="0da2e-127">Следующая команда загружает файл на устройство "видбоард".</span><span class="sxs-lookup"><span data-stu-id="0da2e-127">The following command loads a file into the "vidboard" device.</span></span>

``` syntax
load vidboard c:\vid\fish.vid notify
```

## <a name="requirements"></a><span data-ttu-id="0da2e-128">Требования</span><span class="sxs-lookup"><span data-stu-id="0da2e-128">Requirements</span></span>



| <span data-ttu-id="0da2e-129">Требование</span><span class="sxs-lookup"><span data-stu-id="0da2e-129">Requirement</span></span> | <span data-ttu-id="0da2e-130">Значение</span><span class="sxs-lookup"><span data-stu-id="0da2e-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="0da2e-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0da2e-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0da2e-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0da2e-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="0da2e-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0da2e-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0da2e-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0da2e-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="0da2e-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0da2e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0da2e-136">MCI</span><span class="sxs-lookup"><span data-stu-id="0da2e-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="0da2e-137">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="0da2e-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

