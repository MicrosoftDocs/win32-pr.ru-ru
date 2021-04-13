---
title: Команда break
description: Команда Break задает ключ для прерывания команды, которая была вызвана с помощью параметра \ 0034; Wait \ 0034; RAS. Эта команда является системной командой MCI; он интерпретируется непосредственно MCI.
ms.assetid: 959df85f-5020-4e37-952b-15ba5e6fb672
keywords:
- прерывание команды мультимедиа Windows
topic_type:
- apiref
api_name:
- break
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6f727fb6cf375e09a260ee68f62eac83816ff5d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492825"
---
# <a name="break-command"></a><span data-ttu-id="46749-105">Команда break</span><span class="sxs-lookup"><span data-stu-id="46749-105">break command</span></span>

<span data-ttu-id="46749-106">Команда Break задает ключ для прерывания команды, которая была вызвана с помощью флага Wait.</span><span class="sxs-lookup"><span data-stu-id="46749-106">The break command specifies a key to abort a command that was invoked using the "wait" flag.</span></span> <span data-ttu-id="46749-107">Эта команда является системной командой MCI; он интерпретируется непосредственно MCI.</span><span class="sxs-lookup"><span data-stu-id="46749-107">This command is an MCI system command; it is interpreted directly by MCI.</span></span>

<span data-ttu-id="46749-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="46749-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("break %s %s %s"), 
  lpszDeviceID, 
  lpszVirtKey, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="46749-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="46749-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46749-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="46749-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="46749-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="46749-111">Identifier of an MCI device.</span></span> <span data-ttu-id="46749-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="46749-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="46749-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*лпсзвирткэй*</span><span class="sxs-lookup"><span data-stu-id="46749-113"><span id="lpszVirtKey"></span><span id="lpszvirtkey"></span><span id="LPSZVIRTKEY"></span>*lpszVirtKey*</span></span>
</dt> <dd>

<span data-ttu-id="46749-114">Один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="46749-114">One of the following flags.</span></span>



| <span data-ttu-id="46749-115">Значение</span><span class="sxs-lookup"><span data-stu-id="46749-115">Value</span></span>                 | <span data-ttu-id="46749-116">Значение</span><span class="sxs-lookup"><span data-stu-id="46749-116">Meaning</span></span>                                                                         |
|-----------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="46749-117">в *коде виртуального ключа*</span><span class="sxs-lookup"><span data-stu-id="46749-117">on *virtual key code*</span></span> | <span data-ttu-id="46749-118">Указывает ключ, который прерывает команду, запущенную с помощью флага "Wait".</span><span class="sxs-lookup"><span data-stu-id="46749-118">Specifies the key that aborts a command that was started using the "wait" flag.</span></span> |
| <span data-ttu-id="46749-119">off</span><span class="sxs-lookup"><span data-stu-id="46749-119">off</span></span>                   | <span data-ttu-id="46749-120">Отключает текущий ключ разрыва.</span><span class="sxs-lookup"><span data-stu-id="46749-120">Disables the current break key.</span></span>                                                 |



 

</dd> <dt>

<span data-ttu-id="46749-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="46749-121"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="46749-122">Может иметь значение "Wait", "notify" или и то, и другое.</span><span class="sxs-lookup"><span data-stu-id="46749-122">Can be "wait", "notify", or both.</span></span> <span data-ttu-id="46749-123">Для устройств с цифровыми видео и ВИДЕОМАГНИТОФОНА можно также указать "Test".</span><span class="sxs-lookup"><span data-stu-id="46749-123">For digital-video and VCR devices, "test" can also be specified.</span></span> <span data-ttu-id="46749-124">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="46749-124">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46749-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="46749-125">Return Value</span></span>

<span data-ttu-id="46749-126">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="46749-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="46749-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="46749-127">Remarks</span></span>

<span data-ttu-id="46749-128">Если ключ разрыва включен и пользователь нажимает клавишу, определенную с помощью кода виртуального ключа, указанного в параметре *лпсзвирткэй* , устройство возвращает управление приложению.</span><span class="sxs-lookup"><span data-stu-id="46749-128">When the break key is enabled and the user presses the key identified by the virtual-key code specified in the *lpszVirtKey* parameter, the device returns control to the application.</span></span> <span data-ttu-id="46749-129">По возможности команда продолжит выполнение.</span><span class="sxs-lookup"><span data-stu-id="46749-129">If possible, the command continues execution.</span></span>

## <a name="examples"></a><span data-ttu-id="46749-130">Примеры</span><span class="sxs-lookup"><span data-stu-id="46749-130">Examples</span></span>

<span data-ttu-id="46749-131">Следующая команда задает F2 в качестве ключа разрыва для устройства "мисаунд".</span><span class="sxs-lookup"><span data-stu-id="46749-131">The following command sets F2 as the break key for the "mysound" device.</span></span>

``` syntax
break mysound on 113
```

## <a name="requirements"></a><span data-ttu-id="46749-132">Требования</span><span class="sxs-lookup"><span data-stu-id="46749-132">Requirements</span></span>



| <span data-ttu-id="46749-133">Требование</span><span class="sxs-lookup"><span data-stu-id="46749-133">Requirement</span></span> | <span data-ttu-id="46749-134">Значение</span><span class="sxs-lookup"><span data-stu-id="46749-134">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="46749-135">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="46749-135">Minimum supported client</span></span><br/> | <span data-ttu-id="46749-136">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="46749-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="46749-137">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="46749-137">Minimum supported server</span></span><br/> | <span data-ttu-id="46749-138">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="46749-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="46749-139">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="46749-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46749-140">MCI</span><span class="sxs-lookup"><span data-stu-id="46749-140">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="46749-141">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="46749-141">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

