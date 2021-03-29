---
title: Команда "Закрыть" (Корекрт \_ IO. h)
description: Команда Close закрывает устройство или файл и все связанные с ним ресурсы. MCI выгружает устройство, когда все экземпляры устройства или все файлы закрываются. Все устройства MCI распознают эту команду.
ms.assetid: 0fd7b271-b29e-4170-9a14-81b14dc8a5ee
keywords:
- закрыть команду мультимедиа Windows
topic_type:
- apiref
api_name:
- close
api_location:
- corecrt_io.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d28c255e518553c022dfc833c857b792f43fdbe8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988535"
---
# <a name="close-command"></a><span data-ttu-id="44cd2-106">Команда "Закрыть"</span><span class="sxs-lookup"><span data-stu-id="44cd2-106">close command</span></span>

<span data-ttu-id="44cd2-107">Команда Close закрывает устройство или файл и все связанные с ним ресурсы.</span><span class="sxs-lookup"><span data-stu-id="44cd2-107">The close command closes the device or file and any associated resources.</span></span> <span data-ttu-id="44cd2-108">MCI выгружает устройство, когда все экземпляры устройства или все файлы закрываются.</span><span class="sxs-lookup"><span data-stu-id="44cd2-108">MCI unloads a device when all instances of the device or all files are closed.</span></span> <span data-ttu-id="44cd2-109">Все устройства MCI распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="44cd2-109">All MCI devices recognize this command.</span></span>

<span data-ttu-id="44cd2-110">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="44cd2-110">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("close %s %s"), 
  lpszDeviceID, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="44cd2-111">Параметры</span><span class="sxs-lookup"><span data-stu-id="44cd2-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="44cd2-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="44cd2-112"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="44cd2-113">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="44cd2-113">Identifier of an MCI device.</span></span> <span data-ttu-id="44cd2-114">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="44cd2-114">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="44cd2-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="44cd2-115"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="44cd2-116">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="44cd2-116">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="44cd2-117">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="44cd2-117">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="44cd2-118">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="44cd2-118">Return Value</span></span>

<span data-ttu-id="44cd2-119">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="44cd2-119">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="44cd2-120">Комментарии</span><span class="sxs-lookup"><span data-stu-id="44cd2-120">Remarks</span></span>

<span data-ttu-id="44cd2-121">Чтобы закрыть все устройства, открытые в приложении, укажите идентификатор устройства "ALL" для параметра *лпсздевицеид* .</span><span class="sxs-lookup"><span data-stu-id="44cd2-121">To close all devices opened by your application, specify the "all" device identifier for the *lpszDeviceID* parameter.</span></span>

<span data-ttu-id="44cd2-122">Закрытие устройства **кдаудио** останавливает воспроизведение звука.</span><span class="sxs-lookup"><span data-stu-id="44cd2-122">Closing the **cdaudio** device stops audio playback.</span></span>

<span data-ttu-id="44cd2-123">**Windows 2000/XP:** Если устройство **кдаудио** воспроизводится, закрытие устройства **кдаудио** не приводит к прекращению воспроизведения звука.</span><span class="sxs-lookup"><span data-stu-id="44cd2-123">**Windows 2000/XP:** If the **cdaudio** device is playing, closing the **cdaudio** device does not cause the audio to stop playing.</span></span> <span data-ttu-id="44cd2-124">Сначала отправьте команду " [закончить](stop.md) ".</span><span class="sxs-lookup"><span data-stu-id="44cd2-124">Send the [stop](stop.md) command first.</span></span>

## <a name="examples"></a><span data-ttu-id="44cd2-125">Примеры</span><span class="sxs-lookup"><span data-stu-id="44cd2-125">Examples</span></span>

<span data-ttu-id="44cd2-126">Следующая команда закрывает устройство "мисаунд".</span><span class="sxs-lookup"><span data-stu-id="44cd2-126">The following command closes the "mysound" device.</span></span>

``` syntax
close mysound
```

## <a name="requirements"></a><span data-ttu-id="44cd2-127">Требования</span><span class="sxs-lookup"><span data-stu-id="44cd2-127">Requirements</span></span>



| <span data-ttu-id="44cd2-128">Требование</span><span class="sxs-lookup"><span data-stu-id="44cd2-128">Requirement</span></span> | <span data-ttu-id="44cd2-129">Значение</span><span class="sxs-lookup"><span data-stu-id="44cd2-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="44cd2-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="44cd2-130">Minimum supported client</span></span><br/> | <span data-ttu-id="44cd2-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="44cd2-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="44cd2-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="44cd2-132">Minimum supported server</span></span><br/> | <span data-ttu-id="44cd2-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="44cd2-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="44cd2-134">Заголовок</span><span class="sxs-lookup"><span data-stu-id="44cd2-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="44cd2-135"><dt>Корекрт \_ IO. h</dt></span><span class="sxs-lookup"><span data-stu-id="44cd2-135"><dt>Corecrt\_io.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="44cd2-136">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="44cd2-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44cd2-137">MCI</span><span class="sxs-lookup"><span data-stu-id="44cd2-137">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="44cd2-138">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="44cd2-138">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

