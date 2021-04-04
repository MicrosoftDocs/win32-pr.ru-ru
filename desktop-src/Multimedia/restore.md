---
title: команда Restore
description: Команда Restore копирует изображение из файла в буфер кадров. Это обратный шаг команды Capture. Устройство Digital-Video распознает эту команду.
ms.assetid: e84a478a-3e0f-4767-94d7-eb3c79c31b8b
keywords:
- команда Restore Windows мультимедиа
topic_type:
- apiref
api_name:
- restore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2d7f0f236b26e3e73807b32485442d597e93d40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988219"
---
# <a name="restore-command"></a><span data-ttu-id="ec31a-106">команда Restore</span><span class="sxs-lookup"><span data-stu-id="ec31a-106">restore command</span></span>

<span data-ttu-id="ec31a-107">Команда Restore копирует изображение из файла в буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="ec31a-107">The restore command copies a still image from a file to the frame buffer.</span></span> <span data-ttu-id="ec31a-108">Это обратный шаг команды [Capture](capture.md) .</span><span class="sxs-lookup"><span data-stu-id="ec31a-108">This is the reverse of the [capture](capture.md) command.</span></span> <span data-ttu-id="ec31a-109">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="ec31a-109">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="ec31a-110">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ec31a-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("restore %s %s %s"), 
  lpszDeviceID, 
  lpszRestore, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="ec31a-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="ec31a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec31a-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="ec31a-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="ec31a-113">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="ec31a-113">Identifier of an MCI device.</span></span> <span data-ttu-id="ec31a-114">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="ec31a-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="ec31a-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*лпсзресторе*</span><span class="sxs-lookup"><span data-stu-id="ec31a-115"><span id="lpszRestore"></span><span id="lpszrestore"></span><span id="LPSZRESTORE"></span>*lpszRestore*</span></span>
</dt> <dd>

<span data-ttu-id="ec31a-116">Один или несколько следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="ec31a-116">One or more of the following flags.</span></span>



| <span data-ttu-id="ec31a-117">Значение</span><span class="sxs-lookup"><span data-stu-id="ec31a-117">Value</span></span>           | <span data-ttu-id="ec31a-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ec31a-118">Meaning</span></span>                                                                                                                                                                                                                                                                                                                         |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ec31a-119">в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="ec31a-119">at *rectangle*</span></span>  | <span data-ttu-id="ec31a-120">Задает прямоугольник относительно исходного буфера фрейма.</span><span class="sxs-lookup"><span data-stu-id="ec31a-120">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="ec31a-121">*Прямоугольник* задается как *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="ec31a-121">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="ec31a-122">Координаты *x1 Y1* определяют левый верхний угол, а координаты *x2 Y2* определяют ширину и высоту. Если этот флаг не используется, изображение копируется в левый верхний угол буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="ec31a-122">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.If this flag is not used, the image is copied to the upper left corner of the frame buffer.</span></span><br/> |
| <span data-ttu-id="ec31a-123">из *имени файла*</span><span class="sxs-lookup"><span data-stu-id="ec31a-123">from *filename*</span></span> | <span data-ttu-id="ec31a-124">Указывает имя файла образа для отзыва.</span><span class="sxs-lookup"><span data-stu-id="ec31a-124">Specifies the image filename to recall.</span></span> <span data-ttu-id="ec31a-125">Этот флаг является обязательным.</span><span class="sxs-lookup"><span data-stu-id="ec31a-125">This flag is required.</span></span>                                                                                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="ec31a-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="ec31a-126"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="ec31a-127">Может принимать значение "Wait", "notify", "Test" или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="ec31a-127">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="ec31a-128">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="ec31a-128">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec31a-129">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ec31a-129">Return Value</span></span>

<span data-ttu-id="ec31a-130">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ec31a-130">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="ec31a-131">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ec31a-131">Remarks</span></span>

<span data-ttu-id="ec31a-132">Устройства могут распознать различные форматы изображений. независимый от устройства точечный рисунок Windows всегда распознается.</span><span class="sxs-lookup"><span data-stu-id="ec31a-132">Devices can recognize a variety of image formats; a Windows device-independent bitmap is always recognized.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec31a-133">Требования</span><span class="sxs-lookup"><span data-stu-id="ec31a-133">Requirements</span></span>



| <span data-ttu-id="ec31a-134">Требование</span><span class="sxs-lookup"><span data-stu-id="ec31a-134">Requirement</span></span> | <span data-ttu-id="ec31a-135">Значение</span><span class="sxs-lookup"><span data-stu-id="ec31a-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="ec31a-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ec31a-136">Minimum supported client</span></span><br/> | <span data-ttu-id="ec31a-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ec31a-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="ec31a-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ec31a-138">Minimum supported server</span></span><br/> | <span data-ttu-id="ec31a-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="ec31a-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="ec31a-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ec31a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec31a-141">MCI</span><span class="sxs-lookup"><span data-stu-id="ec31a-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="ec31a-142">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="ec31a-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="ec31a-143">выделяем</span><span class="sxs-lookup"><span data-stu-id="ec31a-143">capture</span></span>](capture.md)
</dt> </dl>

 

