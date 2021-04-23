---
title: Команда index
description: Команда index управляет экраном видеомагнитофона. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.
ms.assetid: 16066acf-37aa-4bff-b97e-5eb2420ac3c4
keywords:
- Команда index мультимедиа Windows
topic_type:
- apiref
api_name:
- index
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da652b1a7a48dffd9850c435345fcfcb11c2e674
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989423"
---
# <a name="index-command"></a><span data-ttu-id="e6a95-105">Команда index</span><span class="sxs-lookup"><span data-stu-id="e6a95-105">index command</span></span>

<span data-ttu-id="e6a95-106">Команда index управляет экраном видеомагнитофона.</span><span class="sxs-lookup"><span data-stu-id="e6a95-106">The index command controls a VCR's on-screen display.</span></span> <span data-ttu-id="e6a95-107">Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="e6a95-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="e6a95-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e6a95-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("index %s %s %s"), 
  lpszDeviceID, 
  lpszIndex, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="e6a95-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="e6a95-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6a95-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="e6a95-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="e6a95-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="e6a95-111">Identifier of an MCI device.</span></span> <span data-ttu-id="e6a95-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="e6a95-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="e6a95-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*лпсзиндекс*</span><span class="sxs-lookup"><span data-stu-id="e6a95-113"><span id="lpszIndex"></span><span id="lpszindex"></span><span id="LPSZINDEX"></span>*lpszIndex*</span></span>
</dt> <dd>

<span data-ttu-id="e6a95-114">Один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="e6a95-114">One of the following flags.</span></span>



| <span data-ttu-id="e6a95-115">Значение</span><span class="sxs-lookup"><span data-stu-id="e6a95-115">Value</span></span> | <span data-ttu-id="e6a95-116">Значение</span><span class="sxs-lookup"><span data-stu-id="e6a95-116">Meaning</span></span>                                                                                                                  |
|-------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a95-117">off</span><span class="sxs-lookup"><span data-stu-id="e6a95-117">off</span></span>   | <span data-ttu-id="e6a95-118">Отключает экран.</span><span class="sxs-lookup"><span data-stu-id="e6a95-118">Turns off the on-screen display.</span></span>                                                                                         |
| <span data-ttu-id="e6a95-119">on</span><span class="sxs-lookup"><span data-stu-id="e6a95-119">on</span></span>    | <span data-ttu-id="e6a95-120">Включает экран на экране.</span><span class="sxs-lookup"><span data-stu-id="e6a95-120">Turns on the on-screen display.</span></span> <span data-ttu-id="e6a95-121">Отображаемый элемент задается с помощью флага "index" команды [Set](set.md) .</span><span class="sxs-lookup"><span data-stu-id="e6a95-121">The item to be displayed is specified by the "index" flag of the [set](set.md) command.</span></span> |



 

</dd> <dt>

<span data-ttu-id="e6a95-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="e6a95-122"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="e6a95-123">Может принимать значение "Wait", "notify" или "Test".</span><span class="sxs-lookup"><span data-stu-id="e6a95-123">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="e6a95-124">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="e6a95-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6a95-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e6a95-125">Return Value</span></span>

<span data-ttu-id="e6a95-126">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e6a95-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a95-127">Требования</span><span class="sxs-lookup"><span data-stu-id="e6a95-127">Requirements</span></span>



| <span data-ttu-id="e6a95-128">Требование</span><span class="sxs-lookup"><span data-stu-id="e6a95-128">Requirement</span></span> | <span data-ttu-id="e6a95-129">Значение</span><span class="sxs-lookup"><span data-stu-id="e6a95-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="e6a95-130">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e6a95-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a95-131">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e6a95-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e6a95-132">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e6a95-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a95-133">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e6a95-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="e6a95-134">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e6a95-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a95-135">MCI</span><span class="sxs-lookup"><span data-stu-id="e6a95-135">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="e6a95-136">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="e6a95-136">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> <dt>

[<span data-ttu-id="e6a95-137">set</span><span class="sxs-lookup"><span data-stu-id="e6a95-137">set</span></span>](set.md)
</dt> </dl>

 

