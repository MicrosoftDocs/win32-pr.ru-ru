---
title: Сообщение MM_MCINOTIFY (Ммсистем. h)
description: '\_Сообщение МЦИНОТИФИ mm уведомляет приложение о том, что устройство MCI завершило операцию. Устройства MCI отправляют это сообщение только при \_ использовании флага уведомления MCI.'
ms.assetid: a0840130-2969-4ce5-b098-3e45401eebb1
keywords:
- MM_MCINOTIFY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MM_MCINOTIFY
api_location:
- Mmsystem.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96ee62c4a2b6e17bf5ad6d719dcb7d6e992a2f2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104136586"
---
# <a name="mm_mcinotify-message"></a><span data-ttu-id="30518-105">MM \_ мЦинотифи, сообщение</span><span class="sxs-lookup"><span data-stu-id="30518-105">MM\_MCINOTIFY message</span></span>

<span data-ttu-id="30518-106">Сообщение **\_ мЦинотифи mm** уведомляет приложение о том, что устройство MCI завершило операцию.</span><span class="sxs-lookup"><span data-stu-id="30518-106">The **MM\_MCINOTIFY** message notifies an application that an MCI device has completed an operation.</span></span> <span data-ttu-id="30518-107">Устройства MCI отправляют это сообщение только при \_ использовании флага уведомления MCI.</span><span class="sxs-lookup"><span data-stu-id="30518-107">MCI devices send this message only when the MCI\_NOTIFY flag is used.</span></span>


```C++
MM_MCINOTIFY 
wParam = (WPARAM) wFlags 
lParam = (LONG) lDevID
```



## <a name="parameters"></a><span data-ttu-id="30518-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="30518-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30518-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*вфлагс*</span><span class="sxs-lookup"><span data-stu-id="30518-109"><span id="wFlags"></span><span id="wflags"></span><span id="WFLAGS"></span>*wFlags*</span></span>
</dt> <dd>

<span data-ttu-id="30518-110">Причина уведомления.</span><span class="sxs-lookup"><span data-stu-id="30518-110">Reason for the notification.</span></span> <span data-ttu-id="30518-111">Определены следующие значения:</span><span class="sxs-lookup"><span data-stu-id="30518-111">The following values are defined:</span></span>



| <span data-ttu-id="30518-112">Требование</span><span class="sxs-lookup"><span data-stu-id="30518-112">Requirement</span></span> | <span data-ttu-id="30518-113">Значение</span><span class="sxs-lookup"><span data-stu-id="30518-113">Value</span></span> |
|-------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30518-114">\_уведомление MCI \_ прервано</span><span class="sxs-lookup"><span data-stu-id="30518-114">MCI\_NOTIFY\_ABORTED</span></span>    | <span data-ttu-id="30518-115">Устройство получило команду, которая не позволила выполнить текущие условия для инициации функции обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="30518-115">The device received a command that prevented the current conditions for initiating the callback function from being met.</span></span> <span data-ttu-id="30518-116">Если новая команда прерывает текущую команду, а также запрашивает уведомление, устройство отправляет только это сообщение, а не \_ уведомляет о \_ ЗАМЕНе MCI.</span><span class="sxs-lookup"><span data-stu-id="30518-116">If a new command interrupts the current command and it also requests notification, the device sends this message only and not MCI\_NOTIFY\_SUPERSEDED</span></span> |
| <span data-ttu-id="30518-117">\_сбой уведомления \_ MCI</span><span class="sxs-lookup"><span data-stu-id="30518-117">MCI\_NOTIFY\_FAILURE</span></span>    | <span data-ttu-id="30518-118">Произошла ошибка устройства во время выполнения команды устройством.</span><span class="sxs-lookup"><span data-stu-id="30518-118">A device error occurred while the device was executing the command.</span></span>                                                                                                                                                                                                            |
| <span data-ttu-id="30518-119">\_уведомление MCI \_ успешно установлено</span><span class="sxs-lookup"><span data-stu-id="30518-119">MCI\_NOTIFY\_SUCCESSFUL</span></span> | <span data-ttu-id="30518-120">Выполнены условия, инициирующие функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="30518-120">The conditions initiating the callback function have been met.</span></span>                                                                                                                                                                                                                 |
| <span data-ttu-id="30518-121">\_уведомление MCI \_ заменено</span><span class="sxs-lookup"><span data-stu-id="30518-121">MCI\_NOTIFY\_SUPERSEDED</span></span> | <span data-ttu-id="30518-122">Устройство получило еще одну команду с установленным флагом "notify", и текущие условия для инициализации функции обратного вызова были заменены.</span><span class="sxs-lookup"><span data-stu-id="30518-122">The device received another command with the "notify" flag set and the current conditions for initiating the callback function have been superseded.</span></span>                                                                                                                           |



 

</dd> <dt>

<span data-ttu-id="30518-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*лдевид*</span><span class="sxs-lookup"><span data-stu-id="30518-123"><span id="lDevID"></span><span id="ldevid"></span><span id="LDEVID"></span>*lDevID*</span></span>
</dt> <dd>

<span data-ttu-id="30518-124">Идентификатор устройства, запускающего функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="30518-124">Identifier of the device initiating the callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30518-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="30518-125">Return Value</span></span>

<span data-ttu-id="30518-126">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="30518-126">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="30518-127">Комментарии</span><span class="sxs-lookup"><span data-stu-id="30518-127">Remarks</span></span>

<span data-ttu-id="30518-128">Дополнительные сведения о \_ флаге уведомления MCI см. [в разделе флаг уведомления](the-notify-flag.md).</span><span class="sxs-lookup"><span data-stu-id="30518-128">For more information about the MCI\_NOTIFY flag, see [The Notify Flag](the-notify-flag.md).</span></span>

<span data-ttu-id="30518-129">Устройство возвращает \_ команду MCI уведомлять об \_ успешном флаге с **\_ мЦинотифи мм** при завершении действия для команды.</span><span class="sxs-lookup"><span data-stu-id="30518-129">A device returns the MCI\_NOTIFY\_SUCCESSFUL flag with **MM\_MCINOTIFY** when the action for a command finishes.</span></span> <span data-ttu-id="30518-130">Например, устройство CD Audio использует этот флаг для уведомления о команде [**Play**](play.md) ( [**MCI \_ Play**](mci-play.md)) при завершении воспроизведения устройства.</span><span class="sxs-lookup"><span data-stu-id="30518-130">For example, a CD audio device uses this flag for notification for the [**play**](play.md) ( [**MCI\_PLAY**](mci-play.md)) command when the device finishes playing.</span></span> <span data-ttu-id="30518-131">Команда **Play** завершается успешно, только когда достигает указанной конечной точки или достигает конца носителя.</span><span class="sxs-lookup"><span data-stu-id="30518-131">The **play** command is successful only when it reaches the specified end position or reaches the end of the media.</span></span> <span data-ttu-id="30518-132">Аналогичным образом команды [**Seek**](seek.md) ( [**\_ Поиск MCI**](mci-seek.md)) и [**запись**](record.md) ( [**\_ запись MCI**](mci-record.md)) не возвращают \_ уведомление MCI \_ , пока не достигают указанной конечной точки или не достигли конца носителя.</span><span class="sxs-lookup"><span data-stu-id="30518-132">Similarly, the [**seek**](seek.md) ( [**MCI\_SEEK**](mci-seek.md)) and [**record**](record.md) ( [**MCI\_RECORD**](mci-record.md)) commands do not return MCI\_NOTIFY\_SUCCESSFUL until they reach the specified end position or reach the end of the media.</span></span>

<span data-ttu-id="30518-133">Устройство возвращает \_ флаг с уведомлением MCI \_ с параметром **mm \_ мЦинотифи** только в том случае, если он получает команду, которая не может удовлетворить условия уведомления.</span><span class="sxs-lookup"><span data-stu-id="30518-133">A device returns the MCI\_NOTIFY\_ABORTED flag with **MM\_MCINOTIFY** only when it receives a command that prevents it from meeting the notification conditions.</span></span> <span data-ttu-id="30518-134">Например, команда [**Play**](play.md) не будет прерывать уведомление для предыдущей команды **Play** при условии, что новая команда не изменяет направление воспроизведения или не изменяет конечную точку.</span><span class="sxs-lookup"><span data-stu-id="30518-134">For example, the [**play**](play.md) command would not abort notification for a previous **play** command provided that the new command does not change the play direction or change the ending position.</span></span> <span data-ttu-id="30518-135">Команды [**поиска**](seek.md) и [**записи**](record.md) ведут себя аналогичным образом.</span><span class="sxs-lookup"><span data-stu-id="30518-135">The [**seek**](seek.md) and [**record**](record.md) commands behave similarly.</span></span> <span data-ttu-id="30518-136">Кроме того, MCI не отправляет \_ уведомление MCI, \_ Если воспроизведение или запись приостанавливаются командой [**Pause**](pause.md) ( [**\_ Пауза MCI**](mci-pause.md)).</span><span class="sxs-lookup"><span data-stu-id="30518-136">MCI also does not send MCI\_NOTIFY\_ABORTED when playback or recording is paused with the [**pause**](pause.md) ( [**MCI\_PAUSE**](mci-pause.md)) command.</span></span> <span data-ttu-id="30518-137">Отправка команды [**Resume**](resume.md) ( [**\_ возобновление MCI**](mci-resume.md)) позволяет им продолжать отвечать на условия обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="30518-137">Sending the [**resume**](resume.md) ( [**MCI\_RESUME**](mci-resume.md)) command allows them to continue to meet the callback conditions.</span></span>

<span data-ttu-id="30518-138">Когда приложение запрашивает уведомление для команды, проверьте ошибку, возвращаемую функциями [**mciSendString**](/previous-versions//dd757161(v=vs.85)) или [**мЦисендкомманд**](/previous-versions//dd757160(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="30518-138">When your application requests notification for a command, check the error return of the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) or [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) functions.</span></span> <span data-ttu-id="30518-139">Если эти функции обнаруживают ошибку и возвращают ненулевое значение, MCI не установит уведомление для команды.</span><span class="sxs-lookup"><span data-stu-id="30518-139">If these functions encounter an error and return a nonzero value, MCI will not set notification for the command.</span></span>

## <a name="requirements"></a><span data-ttu-id="30518-140">Требования</span><span class="sxs-lookup"><span data-stu-id="30518-140">Requirements</span></span>



| <span data-ttu-id="30518-141">Требование</span><span class="sxs-lookup"><span data-stu-id="30518-141">Requirement</span></span> | <span data-ttu-id="30518-142">Значение</span><span class="sxs-lookup"><span data-stu-id="30518-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30518-143">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="30518-143">Minimum supported client</span></span><br/> | <span data-ttu-id="30518-144">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="30518-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="30518-145">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="30518-145">Minimum supported server</span></span><br/> | <span data-ttu-id="30518-146">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="30518-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="30518-147">Заголовок</span><span class="sxs-lookup"><span data-stu-id="30518-147">Header</span></span><br/>                   | <dl> <span data-ttu-id="30518-148"><dt>Ммсистем. h (включение Windows. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30518-148"><dt>Mmsystem.h (include Windows.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30518-149">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="30518-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30518-150">MCI</span><span class="sxs-lookup"><span data-stu-id="30518-150">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="30518-151">Сообщения MCI</span><span class="sxs-lookup"><span data-stu-id="30518-151">MCI Messages</span></span>](mci-messages.md)
</dt> <dt>

[<span data-ttu-id="30518-152">**работу**</span><span class="sxs-lookup"><span data-stu-id="30518-152">**pause**</span></span>](pause.md)
</dt> <dt>

[<span data-ttu-id="30518-153">**воспроизводит**</span><span class="sxs-lookup"><span data-stu-id="30518-153">**play**</span></span>](play.md)
</dt> <dt>

[<span data-ttu-id="30518-154">**запись**</span><span class="sxs-lookup"><span data-stu-id="30518-154">**record**</span></span>](record.md)
</dt> <dt>

[<span data-ttu-id="30518-155">**выход**</span><span class="sxs-lookup"><span data-stu-id="30518-155">**resume**</span></span>](resume.md)
</dt> <dt>

[<span data-ttu-id="30518-156">**поиска**</span><span class="sxs-lookup"><span data-stu-id="30518-156">**seek**</span></span>](seek.md)
</dt> </dl>

 

