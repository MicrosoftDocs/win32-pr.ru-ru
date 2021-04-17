---
title: Команда "отметить"
description: Команда Mark управляет записью и стиранием меток на ленте. Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.
ms.assetid: d5f7a546-dc46-459c-b5dc-0651bca842cb
keywords:
- Пометка команды мультимедиа Windows
topic_type:
- apiref
api_name:
- mark
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 570968af05424597a7fe2b59e86e0364694e0e1f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672625"
---
# <a name="mark-command"></a><span data-ttu-id="4bab3-105">Команда "отметить"</span><span class="sxs-lookup"><span data-stu-id="4bab3-105">mark command</span></span>

<span data-ttu-id="4bab3-106">Команда Mark управляет записью и стиранием меток на ленте.</span><span class="sxs-lookup"><span data-stu-id="4bab3-106">The mark command controls recording and erasing of marks on the videotape.</span></span> <span data-ttu-id="4bab3-107">Устройства ВИДЕОМАГНИТОФОНА распознают эту команду.</span><span class="sxs-lookup"><span data-stu-id="4bab3-107">VCR devices recognize this command.</span></span>

<span data-ttu-id="4bab3-108">Чтобы отправить эту команду, вызовите функцию [**mciSendString**](/previous-versions//dd757161(v=vs.85)) с заданным параметром *лпсзкомманд* , как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="4bab3-108">To send this command, call the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function with the *lpszCommand* parameter set as follows.</span></span>

``` syntax
_stprintf_s(
  lpszCommand, 
  TEXT("mark %s %s %s"), 
  lpszDeviceID, 
  lpszMark, 
  lpszFlags
); 
```

## <a name="parameters"></a><span data-ttu-id="4bab3-109">Параметры</span><span class="sxs-lookup"><span data-stu-id="4bab3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bab3-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*лпсздевицеид*</span><span class="sxs-lookup"><span data-stu-id="4bab3-110"><span id="lpszDeviceID"></span><span id="lpszdeviceid"></span><span id="LPSZDEVICEID"></span>*lpszDeviceID*</span></span>
</dt> <dd>

<span data-ttu-id="4bab3-111">Идентификатор устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="4bab3-111">Identifier of an MCI device.</span></span> <span data-ttu-id="4bab3-112">Этот идентификатор или псевдоним назначается при открытии устройства.</span><span class="sxs-lookup"><span data-stu-id="4bab3-112">This identifier or alias is assigned when the device is opened.</span></span>

</dd> <dt>

<span data-ttu-id="4bab3-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*лпсзмарк*</span><span class="sxs-lookup"><span data-stu-id="4bab3-113"><span id="lpszMark"></span><span id="lpszmark"></span><span id="LPSZMARK"></span>*lpszMark*</span></span>
</dt> <dd>

<span data-ttu-id="4bab3-114">Один из следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="4bab3-114">One of the following flags.</span></span>



| <span data-ttu-id="4bab3-115">Значение</span><span class="sxs-lookup"><span data-stu-id="4bab3-115">Value</span></span> | <span data-ttu-id="4bab3-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4bab3-116">Meaning</span></span>                                                                                                                                |
|-------|----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bab3-117">erase</span><span class="sxs-lookup"><span data-stu-id="4bab3-117">erase</span></span> | <span data-ttu-id="4bab3-118">Удаляет метку в текущей позиции, если она существует.</span><span class="sxs-lookup"><span data-stu-id="4bab3-118">Erases a mark at the current position, if one exists.</span></span> <span data-ttu-id="4bab3-119">Чтобы стереть метку, сначала перейдите к метке, а затем выполните команду "стереть".</span><span class="sxs-lookup"><span data-stu-id="4bab3-119">To erase a mark, first seek to the mark and then issue the mark "erase" command.</span></span> |
| <span data-ttu-id="4bab3-120">write</span><span class="sxs-lookup"><span data-stu-id="4bab3-120">write</span></span> | <span data-ttu-id="4bab3-121">Записывает метку в текущей позиции.</span><span class="sxs-lookup"><span data-stu-id="4bab3-121">Writes a mark at the current position.</span></span> <span data-ttu-id="4bab3-122">Для достижения этой команды может потребоваться, чтобы ВИДЕОМАГНИТОФОН был в режиме воспроизведения или записи.</span><span class="sxs-lookup"><span data-stu-id="4bab3-122">The VCR might need to be in play or record mode for this command to succeed.</span></span>                    |



 

</dd> <dt>

<span data-ttu-id="4bab3-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*лпсзфлагс*</span><span class="sxs-lookup"><span data-stu-id="4bab3-123"><span id="lpszFlags"></span><span id="lpszflags"></span><span id="LPSZFLAGS"></span>*lpszFlags*</span></span>
</dt> <dd>

<span data-ttu-id="4bab3-124">Может принимать значение "Wait", "notify" или "Test".</span><span class="sxs-lookup"><span data-stu-id="4bab3-124">Can be "wait", "notify", or "test".</span></span> <span data-ttu-id="4bab3-125">Дополнительные сведения об этих флагах см. [в разделе Флаги ожидания, уведомления и проверки](the-wait-notify-and-test-flags.md).</span><span class="sxs-lookup"><span data-stu-id="4bab3-125">For more information about these flags, see [The Wait, Notify, and Test Flags](the-wait-notify-and-test-flags.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bab3-126">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4bab3-126">Return Value</span></span>

<span data-ttu-id="4bab3-127">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="4bab3-127">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="4bab3-128">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4bab3-128">Remarks</span></span>

<span data-ttu-id="4bab3-129">Метки — это специальные сигналы, записанные в содержимое, которое может быть обнаружено ВИДЕОМАГНИТОФОН во время высокоскоростного поиска.</span><span class="sxs-lookup"><span data-stu-id="4bab3-129">Marks are special signals written to the content that can be detected by the VCR during high-speed searches.</span></span> <span data-ttu-id="4bab3-130">Метки зависят от ВИДЕОМАГНИТОФОНА.</span><span class="sxs-lookup"><span data-stu-id="4bab3-130">Marks are VCR specific.</span></span>

## <a name="requirements"></a><span data-ttu-id="4bab3-131">Требования</span><span class="sxs-lookup"><span data-stu-id="4bab3-131">Requirements</span></span>



| <span data-ttu-id="4bab3-132">Требование</span><span class="sxs-lookup"><span data-stu-id="4bab3-132">Requirement</span></span> | <span data-ttu-id="4bab3-133">Значение</span><span class="sxs-lookup"><span data-stu-id="4bab3-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="4bab3-134">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="4bab3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4bab3-135">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4bab3-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4bab3-136">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="4bab3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4bab3-137">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="4bab3-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="4bab3-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4bab3-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bab3-139">MCI</span><span class="sxs-lookup"><span data-stu-id="4bab3-139">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="4bab3-140">Строки команд MCI</span><span class="sxs-lookup"><span data-stu-id="4bab3-140">MCI Command Strings</span></span>](mci-command-strings.md)
</dt> </dl>

 

