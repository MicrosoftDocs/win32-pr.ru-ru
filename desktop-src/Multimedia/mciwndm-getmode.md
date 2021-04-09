---
title: Сообщение MCIWNDM_GETMODE (VFW. h)
description: Сообщение МЦИВНДМ \_ мода получает текущий режим работы устройства MCI. Устройства MCI имеют несколько режимов работы, которые обозначены константами. Это сообщение можно отправить явно или с помощью макроса МЦивнджетмоде.
ms.assetid: cc327281-434e-4047-9e15-c04a10953f47
keywords:
- MCIWNDM_GETMODE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_GETMODE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5daefea2c550a1d0cf807ae03840c38ae8b2567c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104135075"
---
# <a name="mciwndm_getmode-message"></a><span data-ttu-id="b3001-106">Сообщение МЦИВНДМ в \_ режиме</span><span class="sxs-lookup"><span data-stu-id="b3001-106">MCIWNDM\_GETMODE message</span></span>

<span data-ttu-id="b3001-107">Сообщение **МЦИВНДМ \_ мода** получает текущий режим работы устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="b3001-107">The **MCIWNDM\_GETMODE** message retrieves the current operating mode of an MCI device.</span></span> <span data-ttu-id="b3001-108">Устройства MCI имеют несколько режимов работы, которые обозначены константами.</span><span class="sxs-lookup"><span data-stu-id="b3001-108">MCI devices have several operating modes, which are designated by constants.</span></span> <span data-ttu-id="b3001-109">Это сообщение можно отправить явно или с помощью макроса [**мЦивнджетмоде**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) .</span><span class="sxs-lookup"><span data-stu-id="b3001-109">You can send this message explicitly or by using the [**MCIWndGetMode**](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode) macro.</span></span>


```C++
MCIWNDM_GETMODE 
wParam = (WPARAM) (UINT) len; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="b3001-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="b3001-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3001-111"><span id="len"></span><span id="LEN"></span>*len*</span><span class="sxs-lookup"><span data-stu-id="b3001-111"><span id="len"></span><span id="LEN"></span>*len*</span></span>
</dt> <dd>

<span data-ttu-id="b3001-112">Размер буфера в байтах.</span><span class="sxs-lookup"><span data-stu-id="b3001-112">Size, in bytes, of the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="b3001-113"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="b3001-113"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="b3001-114">Указатель на определенный приложением буфер, используемый для возврата режима.</span><span class="sxs-lookup"><span data-stu-id="b3001-114">Pointer to the application-defined buffer used to return the mode.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3001-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b3001-115">Return Value</span></span>

<span data-ttu-id="b3001-116">Возвращает целое число, соответствующее константе MCI, определяющей режим.</span><span class="sxs-lookup"><span data-stu-id="b3001-116">Returns an integer corresponding to the MCI constant defining the mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="b3001-117">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3001-117">Remarks</span></span>

<span data-ttu-id="b3001-118">Если строка с завершающим нулем, описывающая режим, длиннее, чем буфер, она усекается.</span><span class="sxs-lookup"><span data-stu-id="b3001-118">If the null-terminated string describing the mode is longer than the buffer, it is truncated.</span></span>

<span data-ttu-id="b3001-119">Не все устройства могут действовать в каждом режиме.</span><span class="sxs-lookup"><span data-stu-id="b3001-119">Not all devices can operate in every mode.</span></span> <span data-ttu-id="b3001-120">Например, устройство МЦИАВИ является устройством воспроизведения; режим записи не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="b3001-120">For example, the MCIAVI device is a playback device; it doesn't support the recording mode.</span></span> <span data-ttu-id="b3001-121">Следующие режимы можно получить с помощью **мЦивндмного \_ режима**.</span><span class="sxs-lookup"><span data-stu-id="b3001-121">The following modes can be retrieved by using **MCIWNDM\_GETMODE**.</span></span>



| <span data-ttu-id="b3001-122">Режим работы</span><span class="sxs-lookup"><span data-stu-id="b3001-122">Operating mode</span></span> | <span data-ttu-id="b3001-123">Константа MCI</span><span class="sxs-lookup"><span data-stu-id="b3001-123">MCI constant</span></span>          |
|----------------|-----------------------|
| <span data-ttu-id="b3001-124">не готово</span><span class="sxs-lookup"><span data-stu-id="b3001-124">not ready</span></span>      | <span data-ttu-id="b3001-125">\_режим MCI \_ не \_ готов</span><span class="sxs-lookup"><span data-stu-id="b3001-125">MCI\_MODE\_NOT\_READY</span></span> |
| <span data-ttu-id="b3001-126">open</span><span class="sxs-lookup"><span data-stu-id="b3001-126">open</span></span>           | <span data-ttu-id="b3001-127">\_Открытие режима \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b3001-127">MCI\_MODE\_OPEN</span></span>       |
| <span data-ttu-id="b3001-128">пауза</span><span class="sxs-lookup"><span data-stu-id="b3001-128">paused</span></span>         | <span data-ttu-id="b3001-129">\_приостановка режима MCI \_</span><span class="sxs-lookup"><span data-stu-id="b3001-129">MCI\_MODE\_PAUSE</span></span>      |
| <span data-ttu-id="b3001-130">воспроизведение</span><span class="sxs-lookup"><span data-stu-id="b3001-130">playing</span></span>        | <span data-ttu-id="b3001-131">\_Воспроизведение в режиме MCI \_</span><span class="sxs-lookup"><span data-stu-id="b3001-131">MCI\_MODE\_PLAY</span></span>       |
| <span data-ttu-id="b3001-132">запись</span><span class="sxs-lookup"><span data-stu-id="b3001-132">recording</span></span>      | <span data-ttu-id="b3001-133">\_запись режима \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b3001-133">MCI\_MODE\_RECORD</span></span>     |
| <span data-ttu-id="b3001-134">поиск</span><span class="sxs-lookup"><span data-stu-id="b3001-134">seeking</span></span>        | <span data-ttu-id="b3001-135">\_Поиск в режиме MCI \_</span><span class="sxs-lookup"><span data-stu-id="b3001-135">MCI\_MODE\_SEEK</span></span>       |
| <span data-ttu-id="b3001-136">остановлена</span><span class="sxs-lookup"><span data-stu-id="b3001-136">stopped</span></span>        | <span data-ttu-id="b3001-137">\_Завершение режима \_ MCI</span><span class="sxs-lookup"><span data-stu-id="b3001-137">MCI\_MODE\_STOP</span></span>       |



 

## <a name="requirements"></a><span data-ttu-id="b3001-138">Требования</span><span class="sxs-lookup"><span data-stu-id="b3001-138">Requirements</span></span>



| <span data-ttu-id="b3001-139">Требование</span><span class="sxs-lookup"><span data-stu-id="b3001-139">Requirement</span></span> | <span data-ttu-id="b3001-140">Значение</span><span class="sxs-lookup"><span data-stu-id="b3001-140">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b3001-141">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3001-141">Minimum supported client</span></span><br/> | <span data-ttu-id="b3001-142">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b3001-142">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b3001-143">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3001-143">Minimum supported server</span></span><br/> | <span data-ttu-id="b3001-144">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b3001-144">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b3001-145">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b3001-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3001-146"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3001-146"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3001-147">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3001-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3001-148">**мЦивнджетмоде**</span><span class="sxs-lookup"><span data-stu-id="b3001-148">**MCIWndGetMode**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgetmode)
</dt> </dl>

 

 





