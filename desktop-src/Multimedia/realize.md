---
title: Команда "реализовать"
description: Команда "реализовать" указывает устройству выбрать и реализовать его палитру в контексте отображения отображаемого окна. Устройство Digital-Video распознает эту команду.
ms.assetid: ad3a52dc-5c8d-47fc-95bd-437b700fc029
keywords:
- Команда выясняет Windows мультимедиа
topic_type:
- apiref
api_name:
- realize
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33accaa9638210adf4385a1776fcd8d2bd2021e7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989215"
---
# <a name="realize-command"></a><span data-ttu-id="16dfc-105">Команда "реализовать"</span><span class="sxs-lookup"><span data-stu-id="16dfc-105">realize command</span></span>

<span data-ttu-id="16dfc-106">Команда "реализовать" указывает устройству выбрать и реализовать его палитру в контексте отображения отображаемого окна.</span><span class="sxs-lookup"><span data-stu-id="16dfc-106">The realize command instructs a device to select and realize its palette into the display context of the displayed window.</span></span> <span data-ttu-id="16dfc-107">Устройство Digital-Video распознает эту команду.</span><span class="sxs-lookup"><span data-stu-id="16dfc-107">Digital-video devices recognize this command.</span></span>

<span data-ttu-id="16dfc-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="16dfc-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("realize %s %s %s"), 
  lpszDeviceID, 
  lpszPalette, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="16dfc-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="16dfc-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16dfc-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="16dfc-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="16dfc-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="16dfc-111">Identifier of an MCI device.</span></span> <span data-ttu-id="16dfc-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="16dfc-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="16dfc-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*лпсзпалетте*</span><span class="sxs-lookup"><span data-stu-id="16dfc-113"><span id="lpszPalette"></span><span id="lpszpalette"></span><span id="LPSZPALETTE"></span>*lpszPalette*</span></span>
</dt> <dd>

<span data-ttu-id="16dfc-114">Один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="16dfc-114">One of the following flags.</span></span>



| <span data-ttu-id="16dfc-115">Значение</span><span class="sxs-lookup"><span data-stu-id="16dfc-115">Value</span></span>      | <span data-ttu-id="16dfc-116">Значение</span><span class="sxs-lookup"><span data-stu-id="16dfc-116">Meaning</span></span>                                                                   |
|------------|---------------------------------------------------------------------------|
| <span data-ttu-id="16dfc-117">background</span><span class="sxs-lookup"><span data-stu-id="16dfc-117">background</span></span> | <span data-ttu-id="16dfc-118">Реализует палитру в виде палитры фона.</span><span class="sxs-lookup"><span data-stu-id="16dfc-118">Realizes the palette as a background palette.</span></span>                             |
| <span data-ttu-id="16dfc-119">нормальный</span><span class="sxs-lookup"><span data-stu-id="16dfc-119">normal</span></span>     | <span data-ttu-id="16dfc-120">Реализует палитру для окна верхнего уровня.</span><span class="sxs-lookup"><span data-stu-id="16dfc-120">Realizes the palette for a top-level window.</span></span> <span data-ttu-id="16dfc-121">Это параметр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="16dfc-121">This is the default setting.</span></span> |



 

</dd> <dt>

<span data-ttu-id="16dfc-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="16dfc-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="16dfc-123">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="16dfc-123">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="16dfc-124">Для устройств Digital-Video также можно указать "Test".</span><span class="sxs-lookup"><span data-stu-id="16dfc-124">For digital-video devices, "test" can also be specified.</span></span> <span data-ttu-id="16dfc-125">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="16dfc-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16dfc-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="16dfc-126">Return Value</span></span>

<span data-ttu-id="16dfc-127">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="16dfc-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="16dfc-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="16dfc-128">Remarks</span></span>

<span data-ttu-id="16dfc-129">Используйте эту команду, только если приложение использует обработчик окна и получает сообщение **WM \_ Куериневпаллетте** или **WM \_ палеттечанжед** .</span><span class="sxs-lookup"><span data-stu-id="16dfc-129">Use this command only if your application uses a window handle and receives a **WM\_QUERYNEWPALLETTE** or **WM\_PALETTECHANGED** message.</span></span>

## <a name="examples"></a><span data-ttu-id="16dfc-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="16dfc-130">Examples</span></span>

<span data-ttu-id="16dfc-131">Следующая команда сообщает устройству "мивидео" о своей палитре.</span><span class="sxs-lookup"><span data-stu-id="16dfc-131">The following command tells the "myvideo" device to realize its palette.</span></span>

``` syntax
realize myvideo normal
```

## <a name="requirements"></a><span data-ttu-id="16dfc-132">Требования</span><span class="sxs-lookup"><span data-stu-id="16dfc-132">Requirements</span></span>



| <span data-ttu-id="16dfc-133">Требование</span><span class="sxs-lookup"><span data-stu-id="16dfc-133">Requirement</span></span> | <span data-ttu-id="16dfc-134">Значение</span><span class="sxs-lookup"><span data-stu-id="16dfc-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="16dfc-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="16dfc-135">Minimum supported client</span></span><br/> | <span data-ttu-id="16dfc-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="16dfc-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="16dfc-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="16dfc-137">Minimum supported server</span></span><br/> | <span data-ttu-id="16dfc-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="16dfc-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="16dfc-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="16dfc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16dfc-140">MCI</span><span class="sxs-lookup"><span data-stu-id="16dfc-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="16dfc-141">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="16dfc-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

