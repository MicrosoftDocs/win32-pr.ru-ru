---
title: Команда сисинфо
description: Команда сисинфо извлекает сведения о системе MCI. Команда сисинфо является системной командой MCI; он интерпретируется непосредственно MCI.
ms.assetid: 494e8976-aac3-4d9f-b14b-3d3fd1917b45
keywords:
- Команда сисинфо мультимедиа Windows
topic_type:
- apiref
api_name:
- sysinfo
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4751a5633462afe1ca8e8cd9abee1afeb16ac242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661981"
---
# <a name="sysinfo-command"></a><span data-ttu-id="06440-105">Команда сисинфо</span><span class="sxs-lookup"><span data-stu-id="06440-105">sysinfo command</span></span>

<span data-ttu-id="06440-106">Команда сисинфо извлекает сведения о системе MCI.</span><span class="sxs-lookup"><span data-stu-id="06440-106">The sysinfo command retrieves MCI system information.</span></span> <span data-ttu-id="06440-107">Команда сисинфо является системной командой MCI; он интерпретируется непосредственно MCI.</span><span class="sxs-lookup"><span data-stu-id="06440-107">The sysinfo command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="06440-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="06440-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("sysinfo %s %s %s"), 
  lpszDeviceID, 
  lpszRequest, 
  lpszFlags
);
```

## <a name="parameters"></a><span data-ttu-id="06440-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="06440-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="06440-110">*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="06440-110">*lpszDeviceID*</span></span> 
</dt> <dd>

<span data-ttu-id="06440-111">Идентификатор устройства MCI или типа устройства.</span><span class="sxs-lookup"><span data-stu-id="06440-111">Identifier of an MCI device or device type.</span></span> <span data-ttu-id="06440-112">Если указан тип устройства, это должно быть стандартное имя типа устройства MCI, указанное в справочном материале для команды [**возможности**](capability.md) .</span><span class="sxs-lookup"><span data-stu-id="06440-112">If a device type is specified, it must be a standard MCI device-type name, as listed in the reference material for the [**capability**](capability.md) command.</span></span> <span data-ttu-id="06440-113">Можно указать «ALL», если флаг, указанный в *лпсзрекуест* , допускает эту возможность.</span><span class="sxs-lookup"><span data-stu-id="06440-113">You can specify "all" when the flag specified in *lpszRequest* allows that possibility.</span></span>

</dd> <dt>

<span data-ttu-id="06440-114">*лпсзрекуест*</span><span class="sxs-lookup"><span data-stu-id="06440-114">*lpszRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="06440-115">Один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="06440-115">One of the following flags.</span></span>



| <span data-ttu-id="06440-116">Значение</span><span class="sxs-lookup"><span data-stu-id="06440-116">Value</span></span>                                                                                                                                                                | <span data-ttu-id="06440-117">Значение</span><span class="sxs-lookup"><span data-stu-id="06440-117">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="installname"></span><span id="INSTALLNAME"></span><dl> <span data-ttu-id="06440-118"><dt>**инсталлнаме**</dt></span><span class="sxs-lookup"><span data-stu-id="06440-118"><dt>**installname**</dt></span></span> </dl>               | <span data-ttu-id="06440-119">Возвращает имя, указанное в реестре, или файл SYSTEM.INI, используемый для установки открытого устройства с указанным идентификатором устройства.</span><span class="sxs-lookup"><span data-stu-id="06440-119">Returns the name listed in the registry or the SYSTEM.INI file used to install the open device with the specified device identifier.</span></span><br/>                                                                                                                                                                                                            |
| <span id="quantity"></span><span id="QUANTITY"></span><dl> <span data-ttu-id="06440-120"><dt>**склад**</dt></span><span class="sxs-lookup"><span data-stu-id="06440-120"><dt>**quantity**</dt></span></span> </dl>                        | <span data-ttu-id="06440-121">Возвращает число устройств MCI, перечисленных в реестре, или файл SYSTEM.INI типа, указанного в параметре *лпсздевицеид* .</span><span class="sxs-lookup"><span data-stu-id="06440-121">Returns the number of MCI devices listed in the registry or the SYSTEM.INI file of the type specified in the *lpszDeviceID* parameter.</span></span> <span data-ttu-id="06440-122">Этот идентификатор устройства должен быть стандартным именем типа устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="06440-122">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="06440-123">Все цифры после типа устройства игнорируются.</span><span class="sxs-lookup"><span data-stu-id="06440-123">Any digits after the device type are ignored.</span></span> <span data-ttu-id="06440-124">При указании значения "ALL" для *лпсздевицеид* возвращается общее число устройств MCI в системе.</span><span class="sxs-lookup"><span data-stu-id="06440-124">Specifying "all" for *lpszDeviceID* returns the total number of MCI devices in the system.</span></span><br/> |
| <span id="quantity_open"></span><span id="QUANTITY_OPEN"></span><dl> <span data-ttu-id="06440-125"><dt>**количество открыто**</dt></span><span class="sxs-lookup"><span data-stu-id="06440-125"><dt>**quantity open**</dt></span></span> </dl>         | <span data-ttu-id="06440-126">Возвращает число открытых устройств MCI типа, указанного в *лпсздевицеид*.</span><span class="sxs-lookup"><span data-stu-id="06440-126">Returns the number of open MCI devices of the type specified in *lpszDeviceID*.</span></span> <span data-ttu-id="06440-127">Этот идентификатор устройства должен быть стандартным именем типа устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="06440-127">This device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="06440-128">При указании значения "ALL" для *лпсздевицеид* возвращается общее число открытых устройств MCI в системе.</span><span class="sxs-lookup"><span data-stu-id="06440-128">Specifying "all" for *lpszDeviceID* returns the total number of open MCI devices in the system.</span></span><br/>                                                                                                 |
| <span id="name_index"></span><span id="NAME_INDEX"></span><dl> <span data-ttu-id="06440-129"><dt>\* \* Индекс \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="06440-129"><dt>\*\*name \*index\*\*\*</dt></span></span> </dl>                | <span data-ttu-id="06440-130">Возвращает имя устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="06440-130">Returns the name of an MCI device.</span></span> <span data-ttu-id="06440-131">Идентификатор устройства должен быть стандартным именем типа устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="06440-131">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="06440-132">*Индекс* находится в диапазоне от 1 до числа устройств этого типа.</span><span class="sxs-lookup"><span data-stu-id="06440-132">The *index* ranges from 1 to the number of devices of that type.</span></span> <span data-ttu-id="06440-133">Если для *лпсздевицеид* задано значение ALL, *индекс* будет находиться в диапазоне от 1 до общего числа устройств в системе.</span><span class="sxs-lookup"><span data-stu-id="06440-133">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of devices in the system.</span></span><br/>                                                                |
| <span id="name_index_open"></span><span id="NAME_INDEX_OPEN"></span><dl> <span data-ttu-id="06440-134"><dt>**открыть *индекс* имени**</dt></span><span class="sxs-lookup"><span data-stu-id="06440-134"><dt>**name *index* open**</dt></span></span> </dl> | <span data-ttu-id="06440-135">Возвращает имя открытого устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="06440-135">Returns the name of an open MCI device.</span></span> <span data-ttu-id="06440-136">Идентификатор устройства должен быть стандартным именем типа устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="06440-136">The device identifier must be a standard MCI device-type name.</span></span> <span data-ttu-id="06440-137">*Индекс* находится в диапазоне от 1 до количества открытых устройств этого типа устройства.</span><span class="sxs-lookup"><span data-stu-id="06440-137">The *index* ranges from 1 to the number of open devices of that device type.</span></span> <span data-ttu-id="06440-138">Если для *лпсздевицеид* задано значение ALL, *индекс* будет находиться в диапазоне от 1 до общего числа открытых устройств в системе.</span><span class="sxs-lookup"><span data-stu-id="06440-138">If "all" is specified for *lpszDeviceID*, *index* ranges from 1 to the total number of open devices in the system.</span></span><br/>                                          |



 

</dd> <dt>

<span data-ttu-id="06440-139">*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="06440-139">*lpszFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="06440-140">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="06440-140">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="06440-141">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="06440-141">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="06440-142">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="06440-142">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="06440-143">Примеры</span><span class="sxs-lookup"><span data-stu-id="06440-143">Examples</span></span>

<span data-ttu-id="06440-144">Следующая команда возвращает число открытых устройств аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="06440-144">The following command returns the number of open waveform-audio devices.</span></span>

``` syntax
sysinfo waveaudio quantity open
```

<span data-ttu-id="06440-145">Следующая команда возвращает имя (псевдоним устройства) первого открытого устройства аудио-сигнала.</span><span class="sxs-lookup"><span data-stu-id="06440-145">The following command returns the name (device alias) of the first open waveform-audio device.</span></span>

``` syntax
sysinfo waveaudio name 1 open
```

## <a name="requirements"></a><span data-ttu-id="06440-146">Требования</span><span class="sxs-lookup"><span data-stu-id="06440-146">Requirements</span></span>



| <span data-ttu-id="06440-147">Требование</span><span class="sxs-lookup"><span data-stu-id="06440-147">Requirement</span></span> | <span data-ttu-id="06440-148">Значение</span><span class="sxs-lookup"><span data-stu-id="06440-148">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="06440-149">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="06440-149">Minimum supported client</span></span><br/> | <span data-ttu-id="06440-150">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="06440-150">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="06440-151">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="06440-151">Minimum supported server</span></span><br/> | <span data-ttu-id="06440-152">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="06440-152">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="06440-153">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="06440-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06440-154">MCI</span><span class="sxs-lookup"><span data-stu-id="06440-154">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="06440-155">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="06440-155">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="06440-156">**возможностями**</span><span class="sxs-lookup"><span data-stu-id="06440-156">**capability**</span></span>](capability.md)
</dt> </dl>

 

