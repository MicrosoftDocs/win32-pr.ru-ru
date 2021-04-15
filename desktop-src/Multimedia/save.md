---
title: Команда "Сохранить"
description: Команда Save сохраняет файл MCI. Эта команда распознает видео-наложение и аудио-изображения. Несмотря на то, что Цифровые видеоустройства и технологии MIDI также распознают эту команду, они не поддерживаются драйверами МЦИАВИ и МЦИСЕК.
ms.assetid: cae199b3-4ac4-49e0-9213-12d816b2f865
keywords:
- сохранение команд мультимедиа Windows
topic_type:
- apiref
api_name:
- save
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0029ad03c1b7fe855e8485b2719b11628fac1103
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672475"
---
# <a name="save-command"></a><span data-ttu-id="dcf07-106">Команда "Сохранить"</span><span class="sxs-lookup"><span data-stu-id="dcf07-106">save command</span></span>

<span data-ttu-id="dcf07-107">Команда Save сохраняет файл MCI.</span><span class="sxs-lookup"><span data-stu-id="dcf07-107">The save command saves an MCI file.</span></span> <span data-ttu-id="dcf07-108">Эта команда распознает видео-наложение и аудио-изображения.</span><span class="sxs-lookup"><span data-stu-id="dcf07-108">Video-overlay and waveform-audio devices recognize this command.</span></span> <span data-ttu-id="dcf07-109">Несмотря на то, что Цифровые видеоустройства и технологии MIDI также распознают эту команду, они не поддерживаются драйверами МЦИАВИ и МЦИСЕК.</span><span class="sxs-lookup"><span data-stu-id="dcf07-109">Although digital-video devices and MIDI sequencers also recognize this command, the MCIAVI and MCISEQ drivers do not support it.</span></span>

<span data-ttu-id="dcf07-110">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="dcf07-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("save %s %s %s"), 
  lpszDeviceID, 
  lpszFilename, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="dcf07-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="dcf07-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dcf07-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="dcf07-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="dcf07-113">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="dcf07-113">Identifier of an MCI device.</span></span> <span data-ttu-id="dcf07-114">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="dcf07-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="dcf07-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*лпсзфиленаме*</span><span class="sxs-lookup"><span data-stu-id="dcf07-115"><span id="lpszFilename"></span><span id="lpszfilename"></span><span id="LPSZFILENAME"></span>*lpszFilename*</span></span>
</dt> <dd>

<span data-ttu-id="dcf07-116">Флаг, указывающий имя сохраняемого файла и, дополнительно, дополнительные флаги, изменяющие операцию сохранения.</span><span class="sxs-lookup"><span data-stu-id="dcf07-116">Flag specifying the name of the file being saved and, optionally, additional flags modifying the save operation.</span></span> <span data-ttu-id="dcf07-117">В следующей таблице перечислены типы устройств, которые распознают команду **Save** , и флаги, используемые каждым типом.</span><span class="sxs-lookup"><span data-stu-id="dcf07-117">The following table lists device types that recognize the **save** command and the flags used by each type.</span></span>



| <span data-ttu-id="dcf07-118">Значение</span><span class="sxs-lookup"><span data-stu-id="dcf07-118">Value</span></span>        | <span data-ttu-id="dcf07-119">Значение</span><span class="sxs-lookup"><span data-stu-id="dcf07-119">Meaning</span></span>              | <span data-ttu-id="dcf07-120">Значение</span><span class="sxs-lookup"><span data-stu-id="dcf07-120">Meaning</span></span>               |
|--------------|----------------------|-----------------------|
| <span data-ttu-id="dcf07-121">дигиталвидео</span><span class="sxs-lookup"><span data-stu-id="dcf07-121">digitalvideo</span></span> | <span data-ttu-id="dcf07-122">прервать в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="dcf07-122">abort at *rectangle*</span></span> | <span data-ttu-id="dcf07-123">*имя файла* кипресерве</span><span class="sxs-lookup"><span data-stu-id="dcf07-123">*filename* keepreserve</span></span> |
| <span data-ttu-id="dcf07-124">overlay</span><span class="sxs-lookup"><span data-stu-id="dcf07-124">overlay</span></span>      | <span data-ttu-id="dcf07-125">в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="dcf07-125">at *rectangle*</span></span>       | <span data-ttu-id="dcf07-126">*filename*</span><span class="sxs-lookup"><span data-stu-id="dcf07-126">*filename*</span></span>            |
| <span data-ttu-id="dcf07-127">sequencer</span><span class="sxs-lookup"><span data-stu-id="dcf07-127">sequencer</span></span>    | <span data-ttu-id="dcf07-128">*filename*</span><span class="sxs-lookup"><span data-stu-id="dcf07-128">*filename*</span></span>           |                       |
| <span data-ttu-id="dcf07-129">вавеаудио</span><span class="sxs-lookup"><span data-stu-id="dcf07-129">waveaudio</span></span>    | <span data-ttu-id="dcf07-130">*filename*</span><span class="sxs-lookup"><span data-stu-id="dcf07-130">*filename*</span></span>           |                       |



 

<span data-ttu-id="dcf07-131">В следующей таблице перечислены флаги, которые могут быть указаны в параметре **лпсзфиленаме** , и их значения.</span><span class="sxs-lookup"><span data-stu-id="dcf07-131">The following table lists the flags that can be specified in the **lpszFilename** parameter and their meanings.</span></span>



| <span data-ttu-id="dcf07-132">Значение</span><span class="sxs-lookup"><span data-stu-id="dcf07-132">Value</span></span>          | <span data-ttu-id="dcf07-133">Значение</span><span class="sxs-lookup"><span data-stu-id="dcf07-133">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="dcf07-134">abort</span><span class="sxs-lookup"><span data-stu-id="dcf07-134">abort</span></span>          | <span data-ttu-id="dcf07-135">Останавливает операцию **сохранения** .</span><span class="sxs-lookup"><span data-stu-id="dcf07-135">Stops a **save** operation in progress.</span></span> <span data-ttu-id="dcf07-136">При использовании этого элемента должен быть только текущий элемент.</span><span class="sxs-lookup"><span data-stu-id="dcf07-136">If used, this must be the only item present.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="dcf07-137">в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="dcf07-137">at *rectangle*</span></span> | <span data-ttu-id="dcf07-138">Задает прямоугольник относительно исходного буфера фрейма.</span><span class="sxs-lookup"><span data-stu-id="dcf07-138">Specifies a rectangle relative to the frame buffer origin.</span></span> <span data-ttu-id="dcf07-139">*Прямоугольник* задается как *x1 Y1 x2 Y2*.</span><span class="sxs-lookup"><span data-stu-id="dcf07-139">The *rectangle* is specified as *X1 Y1 X2 Y2*.</span></span> <span data-ttu-id="dcf07-140">Координаты *x1 Y1* определяют левый верхний угол, а координаты *x2 Y2* определяют ширину и высоту. Для устройств с цифровыми видео команда [записи](capture.md) используется для записи содержимого буфера кадров.</span><span class="sxs-lookup"><span data-stu-id="dcf07-140">The coordinates *X1 Y1* specify the upper left corner and the coordinates *X2 Y2* specify the width and height.For digital-video devices, the [capture](capture.md) command is used to capture the contents of the frame buffer.</span></span><br/>                                                                                                                                               |
| <span data-ttu-id="dcf07-141">*filename*</span><span class="sxs-lookup"><span data-stu-id="dcf07-141">*filename*</span></span>     | <span data-ttu-id="dcf07-142">Указывает имя файла, присваиваемого файлу данных.</span><span class="sxs-lookup"><span data-stu-id="dcf07-142">Specifies the filename to assign to the data file.</span></span> <span data-ttu-id="dcf07-143">Если путь не указан, файл будет помещен на диск и в каталог, ранее указанный в команде Explicit или Implicit [Reserve](reserve.md) .</span><span class="sxs-lookup"><span data-stu-id="dcf07-143">If a path is not specified, the file will be placed on the disk and in the directory previously specified on the explicit or implicit [reserve](reserve.md) command.</span></span> <span data-ttu-id="dcf07-144">Если **резерв** не был выдан, диск и каталог по умолчанию связаны с задачей приложения.</span><span class="sxs-lookup"><span data-stu-id="dcf07-144">If **reserve** has not been issued, the default drive and directory are those associated with the application's task.</span></span> <span data-ttu-id="dcf07-145">Если указан путь, устройство может потребовать, чтобы оно было на диске, указанном явным или неявным **резервом**.</span><span class="sxs-lookup"><span data-stu-id="dcf07-145">If a path is specified, the device might require it to be on the disk drive specified by the explicit or implicit **reserve**.</span></span> <span data-ttu-id="dcf07-146">Этот флаг является обязательным.</span><span class="sxs-lookup"><span data-stu-id="dcf07-146">This flag is required.</span></span> |
| <span data-ttu-id="dcf07-147">кипресерве</span><span class="sxs-lookup"><span data-stu-id="dcf07-147">keepreserve</span></span>    | <span data-ttu-id="dcf07-148">Указывает, что неиспользуемое место на диске, оставшееся до исходной команды **Reserve** , не освобождается.</span><span class="sxs-lookup"><span data-stu-id="dcf07-148">Specifies that unused disk space left over from the original **reserve** command is not deallocated.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                 |



 

</dd> <dt>

<span data-ttu-id="dcf07-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="dcf07-149"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="dcf07-150">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="dcf07-150">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="dcf07-151">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="dcf07-151">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="dcf07-152">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="dcf07-152">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dcf07-153">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dcf07-153">Return Value</span></span>

<span data-ttu-id="dcf07-154">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="dcf07-154">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcf07-155">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dcf07-155">Remarks</span></span>

<span data-ttu-id="dcf07-156">Переменная *filename* является обязательной, если устройство было открыто с помощью идентификатора устройства "New".</span><span class="sxs-lookup"><span data-stu-id="dcf07-156">The *filename* variable is required if the device was opened using the "new" device identifier.</span></span>

## <a name="examples"></a><span data-ttu-id="dcf07-157">Примеры</span><span class="sxs-lookup"><span data-stu-id="dcf07-157">Examples</span></span>

<span data-ttu-id="dcf07-158">Следующая команда сохраняет весь буфер видео в файл с именем ВКАПФИЛЕ. TGA.</span><span class="sxs-lookup"><span data-stu-id="dcf07-158">The following command saves the entire video buffer to a file named VCAPFILE.TGA.</span></span>

``` syntax
save vboard c:\vcap\vcapfile.tga
```

## <a name="requirements"></a><span data-ttu-id="dcf07-159">Требования</span><span class="sxs-lookup"><span data-stu-id="dcf07-159">Requirements</span></span>



| <span data-ttu-id="dcf07-160">Требование</span><span class="sxs-lookup"><span data-stu-id="dcf07-160">Requirement</span></span> | <span data-ttu-id="dcf07-161">Значение</span><span class="sxs-lookup"><span data-stu-id="dcf07-161">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="dcf07-162">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dcf07-162">Minimum supported client</span></span><br/> | <span data-ttu-id="dcf07-163">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dcf07-163">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="dcf07-164">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dcf07-164">Minimum supported server</span></span><br/> | <span data-ttu-id="dcf07-165">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dcf07-165">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="dcf07-166">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dcf07-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcf07-167">MCI</span><span class="sxs-lookup"><span data-stu-id="dcf07-167">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="dcf07-168">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="dcf07-168">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="dcf07-169">выделяем</span><span class="sxs-lookup"><span data-stu-id="dcf07-169">capture</span></span>](capture.md)
</dt> <dt>

[<span data-ttu-id="dcf07-170">предназначен</span><span class="sxs-lookup"><span data-stu-id="dcf07-170">reserve</span></span>](reserve.md)
</dt> </dl>

 

