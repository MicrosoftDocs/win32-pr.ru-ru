---
title: команда записи
description: Команда Capture копирует содержимое буфера кадров и сохраняет его в указанном файле. Устройство Digital-Video распознает эту команду.
ms.assetid: cdf177b9-874e-40d8-af3e-59070c55903d
keywords:
- захват команд мультимедиа Windows
topic_type:
- apiref
api_name:
- capture
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf5edce248fc5402245e36e869cddc97ba3430a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104137391"
---
# <a name="capture-command"></a><span data-ttu-id="51f90-105">команда записи</span><span class="sxs-lookup"><span data-stu-id="51f90-105">capture command</span></span>

<span data-ttu-id="51f90-106">Команда Capture копирует содержимое буфера кадров и сохраняет его в указанном файле.</span><span class="sxs-lookup"><span data-stu-id="51f90-106">The capture command copies the contents of the frame buffer and stores it in the specified file.</span></span> <span data-ttu-id="51f90-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="51f90-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="51f90-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="51f90-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("capture %s %s %s"), 
  lpszDeviceID, 
  lpszCapture, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="51f90-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="51f90-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="51f90-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="51f90-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="51f90-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="51f90-111">Identifier of an MCI device.</span></span> <span data-ttu-id="51f90-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="51f90-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="51f90-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*лпсзкаптуре*</span><span class="sxs-lookup"><span data-stu-id="51f90-113"><span id="lpszCapture"></span><span id="lpszcapture"></span><span id="LPSZCAPTURE"></span>*lpszCapture*</span></span>
</dt> <dd>

<span data-ttu-id="51f90-114">Один или несколько следующих флагов:</span><span class="sxs-lookup"><span data-stu-id="51f90-114">One or more of the following flags:</span></span>



| <span data-ttu-id="51f90-115">Значение</span><span class="sxs-lookup"><span data-stu-id="51f90-115">Value</span></span>          | <span data-ttu-id="51f90-116">Значение</span><span class="sxs-lookup"><span data-stu-id="51f90-116">Meaning</span></span>                                                                                                                                                                                                                                                   |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51f90-117">как *путь*</span><span class="sxs-lookup"><span data-stu-id="51f90-117">as *pathname*</span></span>  | <span data-ttu-id="51f90-118">Задает целевой путь и имя файла для захваченного образа.</span><span class="sxs-lookup"><span data-stu-id="51f90-118">Specifies the destination path and filename for the captured image.</span></span> <span data-ttu-id="51f90-119">Этот флаг является обязательным.</span><span class="sxs-lookup"><span data-stu-id="51f90-119">This flag is required.</span></span>                                                                                                                                                                |
| <span data-ttu-id="51f90-120">в *прямоугольнике*</span><span class="sxs-lookup"><span data-stu-id="51f90-120">at *rectangle*</span></span> | <span data-ttu-id="51f90-121">Задает прямоугольную область в буфере кадров, которую устройство обрезает и сохраняет на диске.</span><span class="sxs-lookup"><span data-stu-id="51f90-121">Specifies the rectangular region within the frame buffer that the device crops and saves to disk.</span></span> <span data-ttu-id="51f90-122">Если этот параметр опущен, то в обрезанной области по умолчанию используется прямоугольник, указанный или установленный по умолчанию [в предыдущей команде "источник" для](put.md) этого экземпляра устройства.</span><span class="sxs-lookup"><span data-stu-id="51f90-122">If omitted, the cropped region defaults to the rectangle specified or defaulted on a previous [put](put.md) "source" command for this device instance.</span></span> |



 

</dd> <dt>

<span data-ttu-id="51f90-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="51f90-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="51f90-124">Может принимать значение "Wait", "notify", "Test" или их сочетание.</span><span class="sxs-lookup"><span data-stu-id="51f90-124">Can be "wait", "notify", "test", or a combination of these.</span></span> <span data-ttu-id="51f90-125">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="51f90-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="51f90-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="51f90-126">Return Value</span></span>

<span data-ttu-id="51f90-127">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="51f90-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="51f90-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="51f90-128">Remarks</span></span>

<span data-ttu-id="51f90-129">Эта команда может завершиться ошибкой, если устройство в данный момент воспроизводит видео о движении или выполняет некоторую другую операцию, требующую больших ресурсов.</span><span class="sxs-lookup"><span data-stu-id="51f90-129">This command might fail if the device is currently playing motion video or executing some other resource-intensive operation.</span></span> <span data-ttu-id="51f90-130">Если буфер фрейма обновляется в режиме реального времени, то обновление мгновенно приостанавливается, что позволяет записать полный образ.</span><span class="sxs-lookup"><span data-stu-id="51f90-130">If the frame buffer is being updated in real time, the updating momentarily pauses so that a complete image is captured.</span></span> <span data-ttu-id="51f90-131">Если устройство приостанавливает обновление, может возникнуть визуальный или звуковой результат.</span><span class="sxs-lookup"><span data-stu-id="51f90-131">If the device pauses the updating, there might be a visual or audible effect.</span></span> <span data-ttu-id="51f90-132">Если формат файла, алгоритм сжатия и уровни качества не заданы, используются значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="51f90-132">If the file format, compression algorithm, and quality levels have not been set, their defaults are used.</span></span>

## <a name="requirements"></a><span data-ttu-id="51f90-133">Требования</span><span class="sxs-lookup"><span data-stu-id="51f90-133">Requirements</span></span>



| <span data-ttu-id="51f90-134">Требование</span><span class="sxs-lookup"><span data-stu-id="51f90-134">Requirement</span></span> | <span data-ttu-id="51f90-135">Значение</span><span class="sxs-lookup"><span data-stu-id="51f90-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="51f90-136">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="51f90-136">Minimum supported client</span></span><br/> | <span data-ttu-id="51f90-137">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51f90-137">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="51f90-138">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="51f90-138">Minimum supported server</span></span><br/> | <span data-ttu-id="51f90-139">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="51f90-139">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="51f90-140">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="51f90-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51f90-141">MCI</span><span class="sxs-lookup"><span data-stu-id="51f90-141">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="51f90-142">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="51f90-142">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="51f90-143">PUT</span><span class="sxs-lookup"><span data-stu-id="51f90-143">put</span></span>](put.md)
</dt> </dl>

 

