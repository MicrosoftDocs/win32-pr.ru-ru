---
title: отменить закрепление команды
description: Команда unfreeze снова включает получение видео в буфер фрейма после того, как он был отключен командой Freeze. Эта команда распознает цифровые видеоролики, видеомагнитофоны и устройства наложения видео.
ms.assetid: ca90c299-2003-44cb-a879-4bc767480965
keywords:
- Отмена закрепления команды мультимедиа Windows
topic_type:
- apiref
api_name:
- unfreeze
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 155ba6b65fb08411d8404920c8f3337d1bddbcb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803820"
---
# <a name="unfreeze-command"></a><span data-ttu-id="d25ce-105">отменить закрепление команды</span><span class="sxs-lookup"><span data-stu-id="d25ce-105">unfreeze command</span></span>

<span data-ttu-id="d25ce-106">Команда unfreeze снова включает получение видео в буфер фрейма после того, как он был отключен командой [Freeze](freeze.md) .</span><span class="sxs-lookup"><span data-stu-id="d25ce-106">The unfreeze command reenables video acquisition to the frame buffer after it has been disabled by the [freeze](freeze.md) command.</span></span> <span data-ttu-id="d25ce-107">Эта команда распознает цифровые видеоролики, видеомагнитофоны и устройства наложения видео.</span><span class="sxs-lookup"><span data-stu-id="d25ce-107">Digital-video, VCR, and video-overlay devices recognize this command.</span></span>

<span data-ttu-id="d25ce-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="d25ce-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("unfreeze %s %s %s"), 
  lpszDeviceID, 
  lpszUnfreeze, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="d25ce-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="d25ce-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d25ce-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="d25ce-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="d25ce-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="d25ce-111">Identifier of an MCI device.</span></span> <span data-ttu-id="d25ce-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="d25ce-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="d25ce-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*лпсзунфризе*</span><span class="sxs-lookup"><span data-stu-id="d25ce-113"><span id="lpszUnfreeze"></span><span id="lpszunfreeze"></span><span id="LPSZUNFREEZE"></span>*lpszUnfreeze*</span></span>
</dt> <dd>

<span data-ttu-id="d25ce-114">Флаг для повторного включения получения видео в буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="d25ce-114">Flag for reenabling video acquisition to the frame buffer.</span></span> <span data-ttu-id="d25ce-115">В следующей таблице перечислены типы устройств, которые распознают команду **разморозки** и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="d25ce-115">The following table lists device types that recognize the **unfreeze** command and the flags used by each type.</span></span>



| <span data-ttu-id="d25ce-116">Значение</span><span class="sxs-lookup"><span data-stu-id="d25ce-116">Value</span></span>        | <span data-ttu-id="d25ce-117">Значение</span><span class="sxs-lookup"><span data-stu-id="d25ce-117">Meaning</span></span>        |
|--------------|----------------|
| <span data-ttu-id="d25ce-118">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="d25ce-118">digitalvideo</span></span> | <span data-ttu-id="d25ce-119">в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="d25ce-119">at *rectangle*</span></span> |
| <span data-ttu-id="d25ce-120">overlay</span><span class="sxs-lookup"><span data-stu-id="d25ce-120">overlay</span></span>      | <span data-ttu-id="d25ce-121">в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="d25ce-121">at *rectangle*</span></span> |
| <span data-ttu-id="d25ce-122">видеомагнитофон</span><span class="sxs-lookup"><span data-stu-id="d25ce-122">vcr</span></span>          | <span data-ttu-id="d25ce-123">входные выходные данные</span><span class="sxs-lookup"><span data-stu-id="d25ce-123">input output</span></span>   |



 

<span data-ttu-id="d25ce-124">В следующей таблице перечислены флаги, которые могут быть указаны в параметре **лпсзунфризе** , и их значения.</span><span class="sxs-lookup"><span data-stu-id="d25ce-124">The following table lists the flags that can be specified in the **lpszUnfreeze** parameter and their meanings.</span></span>



| <span data-ttu-id="d25ce-125">Значение</span><span class="sxs-lookup"><span data-stu-id="d25ce-125">Value</span></span>          | <span data-ttu-id="d25ce-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d25ce-126">Meaning</span></span>                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d25ce-127">в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="d25ce-127">at *rectangle*</span></span> | <span data-ttu-id="d25ce-128">Указывает регион, в котором будет включено повторное получение видео.</span><span class="sxs-lookup"><span data-stu-id="d25ce-128">Specifies the region that will have video acquisition reenabled.</span></span> <span data-ttu-id="d25ce-129">Прямоугольник задается относительно источника видеобуфера и задается как *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="d25ce-129">The rectangle is relative to the video buffer origin and is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="d25ce-130">Координаты *x1 Y1* определяют левый верхний угол прямоугольника, а координаты *x2 Y2* определяют ширину и высоту.</span><span class="sxs-lookup"><span data-stu-id="d25ce-130">The coordinates *X1 Y1* specify the upper left corner of the rectangle, and the coordinates *X2 Y2* specify the width and height.</span></span> |
| <span data-ttu-id="d25ce-131">input</span><span class="sxs-lookup"><span data-stu-id="d25ce-131">input</span></span>          | <span data-ttu-id="d25ce-132">Разморозить входной образ.</span><span class="sxs-lookup"><span data-stu-id="d25ce-132">Unfreeze the input image.</span></span>                                                                                                                                                                                                                                                                  |
| <span data-ttu-id="d25ce-133">output</span><span class="sxs-lookup"><span data-stu-id="d25ce-133">output</span></span>         | <span data-ttu-id="d25ce-134">Разморозить выходное изображение.</span><span class="sxs-lookup"><span data-stu-id="d25ce-134">Unfreeze the output image.</span></span> <span data-ttu-id="d25ce-135">Если не указано ни «вход», ни «Output», то предполагается «Output».</span><span class="sxs-lookup"><span data-stu-id="d25ce-135">If neither "input" nor "output" is given, "output" is assumed.</span></span>                                                                                                                                                                                                  |



 

</dd> <dt>

<span data-ttu-id="d25ce-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="d25ce-136"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="d25ce-137">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="d25ce-137">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="d25ce-138">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="d25ce-138">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="d25ce-139">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="d25ce-139">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d25ce-140">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d25ce-140">Return Value</span></span>

<span data-ttu-id="d25ce-141">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d25ce-141">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="d25ce-142">Примеры</span><span class="sxs-lookup"><span data-stu-id="d25ce-142">Examples</span></span>

<span data-ttu-id="d25ce-143">Следующая команда отменяет фиксацию области видеобуфера.</span><span class="sxs-lookup"><span data-stu-id="d25ce-143">The following command unfreezes a region of the video buffer.</span></span>

``` syntax
unfreeze vboard at 10 20 90 165
```

## <a name="requirements"></a><span data-ttu-id="d25ce-144">Требования</span><span class="sxs-lookup"><span data-stu-id="d25ce-144">Requirements</span></span>



| <span data-ttu-id="d25ce-145">Требование</span><span class="sxs-lookup"><span data-stu-id="d25ce-145">Requirement</span></span> | <span data-ttu-id="d25ce-146">Значение</span><span class="sxs-lookup"><span data-stu-id="d25ce-146">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="d25ce-147">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d25ce-147">Minimum supported client</span></span><br/> | <span data-ttu-id="d25ce-148">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d25ce-148">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d25ce-149">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d25ce-149">Minimum supported server</span></span><br/> | <span data-ttu-id="d25ce-150">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d25ce-150">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="d25ce-151">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d25ce-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d25ce-152">MCI</span><span class="sxs-lookup"><span data-stu-id="d25ce-152">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="d25ce-153">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="d25ce-153">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="d25ce-154">фиксировать</span><span class="sxs-lookup"><span data-stu-id="d25ce-154">freeze</span></span>](freeze.md)
</dt> </dl>

 

