---
title: Spin, команда
description: Команда Spin запускает вращение диска или останавливает вращение диска. Устройства видеодиск распознают эту команду.
ms.assetid: 1fdf4d09-fafd-4245-ad92-397114d0f473
keywords:
- Команда "вращение" Windows мультимедиа
topic_type:
- apiref
api_name:
- spin
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c25e25f5a44ad6e6c9562d05653ab25cb2950b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672703"
---
# <a name="spin-command"></a><span data-ttu-id="952c4-105">Spin, команда</span><span class="sxs-lookup"><span data-stu-id="952c4-105">spin command</span></span>

<span data-ttu-id="952c4-106">Команда Spin запускает вращение диска или останавливает вращение диска.</span><span class="sxs-lookup"><span data-stu-id="952c4-106">The spin command starts spinning a disc or stops the disc from spinning.</span></span> <span data-ttu-id="952c4-107">Устройства видеодиск распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="952c4-107">Videodisc devices recognize this command.</span></span>

<span data-ttu-id="952c4-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="952c4-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("spin %s %s %s"), 
  lpszDeviceID, 
  lpszUpDown, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="952c4-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="952c4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="952c4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="952c4-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="952c4-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="952c4-111">Identifier of an MCI device.</span></span> <span data-ttu-id="952c4-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="952c4-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="952c4-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*лпсзупдовн*</span><span class="sxs-lookup"><span data-stu-id="952c4-113"><span id="lpszUpDown"></span><span id="lpszupdown"></span><span id="LPSZUPDOWN"></span>*lpszUpDown*</span></span>
</dt> <dd>

<span data-ttu-id="952c4-114">Один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="952c4-114">One of the following flags.</span></span>



| <span data-ttu-id="952c4-115">Значение</span><span class="sxs-lookup"><span data-stu-id="952c4-115">Value</span></span> | <span data-ttu-id="952c4-116">Значение</span><span class="sxs-lookup"><span data-stu-id="952c4-116">Meaning</span></span>                       |
|-------|-------------------------------|
| <span data-ttu-id="952c4-117">работу</span><span class="sxs-lookup"><span data-stu-id="952c4-117">down</span></span>  | <span data-ttu-id="952c4-118">Останавливает вращение диска.</span><span class="sxs-lookup"><span data-stu-id="952c4-118">Stops the disc from spinning.</span></span> |
| <span data-ttu-id="952c4-119">up</span><span class="sxs-lookup"><span data-stu-id="952c4-119">up</span></span>    | <span data-ttu-id="952c4-120">Начинает вращать диск.</span><span class="sxs-lookup"><span data-stu-id="952c4-120">Starts spinning the disc.</span></span>     |



 

</dd> <dt>

<span data-ttu-id="952c4-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="952c4-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="952c4-122">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="952c4-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="952c4-123">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="952c4-123">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="952c4-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="952c4-124">Return Value</span></span>

<span data-ttu-id="952c4-125">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="952c4-125">Returns zero if successful or an error otherwise.</span></span>

## <a name="examples"></a><span data-ttu-id="952c4-126">Примеры</span><span class="sxs-lookup"><span data-stu-id="952c4-126">Examples</span></span>

<span data-ttu-id="952c4-127">Следующая команда запускает вращающееся устройство видеодиск.</span><span class="sxs-lookup"><span data-stu-id="952c4-127">The following command starts spinning a videodisc device.</span></span>

``` syntax
spin videodisc up
```

## <a name="requirements"></a><span data-ttu-id="952c4-128">Требования</span><span class="sxs-lookup"><span data-stu-id="952c4-128">Requirements</span></span>



| <span data-ttu-id="952c4-129">Требование</span><span class="sxs-lookup"><span data-stu-id="952c4-129">Requirement</span></span> | <span data-ttu-id="952c4-130">Значение</span><span class="sxs-lookup"><span data-stu-id="952c4-130">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="952c4-131">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="952c4-131">Minimum supported client</span></span><br/> | <span data-ttu-id="952c4-132">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="952c4-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="952c4-133">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="952c4-133">Minimum supported server</span></span><br/> | <span data-ttu-id="952c4-134">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="952c4-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="952c4-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="952c4-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="952c4-136">MCI</span><span class="sxs-lookup"><span data-stu-id="952c4-136">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="952c4-137">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="952c4-137">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

