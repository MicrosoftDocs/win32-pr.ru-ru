---
title: Сообщение WM_CAP_SET_CALLBACK_YIELD (VFW. h)
description: Сообщение о выдачей \_ \_ \_ обратного вызова Set крепления WM \_ устанавливает функцию обратного вызова в приложении. Авикап вызывает эту процедуру, когда окно записи выдается во время потоковой записи. Это сообщение можно отправить явно или с помощью макроса Капсеткаллбаккониелд.
ms.assetid: d978dc3b-4336-46a4-85ae-7d588a63489b
keywords:
- WM_CAP_SET_CALLBACK_YIELD сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_YIELD
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b95c9ba0be7a0abeb99c0590e255adb0bd442343
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672473"
---
# <a name="wm_cap_set_callback_yield-message"></a><span data-ttu-id="0e817-106">\_Сообщение о \_ \_ выдает ответ обратного вызова Set крепления WM \_</span><span class="sxs-lookup"><span data-stu-id="0e817-106">WM\_CAP\_SET\_CALLBACK\_YIELD message</span></span>

<span data-ttu-id="0e817-107">Сообщение о выдачей **\_ \_ \_ обратного вызова \_ Set крепления WM** устанавливает функцию обратного вызова в приложении.</span><span class="sxs-lookup"><span data-stu-id="0e817-107">The **WM\_CAP\_SET\_CALLBACK\_YIELD** message sets a callback function in the application.</span></span> <span data-ttu-id="0e817-108">Авикап вызывает эту процедуру, когда окно записи выдается во время потоковой записи.</span><span class="sxs-lookup"><span data-stu-id="0e817-108">AVICap calls this procedure when the capture window yields during streaming capture.</span></span> <span data-ttu-id="0e817-109">Это сообщение можно отправить явно или с помощью макроса [**капсеткаллбаккониелд**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) .</span><span class="sxs-lookup"><span data-stu-id="0e817-109">You can send this message explicitly or by using the [**capSetCallbackOnYield**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonyield) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_YIELD 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="0e817-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="0e817-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e817-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*фппрок*</span><span class="sxs-lookup"><span data-stu-id="0e817-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="0e817-112">Указатель на функцию обратного вызова yield типа [**капиелдкаллбакк**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback).</span><span class="sxs-lookup"><span data-stu-id="0e817-112">Pointer to the yield callback function, of type [**capYieldCallback**](/windows/desktop/api/Vfw/nc-vfw-capyieldcallback).</span></span> <span data-ttu-id="0e817-113">Укажите **значение NULL** для этого параметра, чтобы отключить ранее установленную функцию обратного вызова yield.</span><span class="sxs-lookup"><span data-stu-id="0e817-113">Specify **NULL** for this parameter to disable a previously installed yield callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e817-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0e817-114">Return Value</span></span>

<span data-ttu-id="0e817-115">Возвращает **значение true** в случае успеха или **false** , если выполняется захват потоковой передачи или однокадровый сеанс записи.</span><span class="sxs-lookup"><span data-stu-id="0e817-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e817-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0e817-116">Remarks</span></span>

<span data-ttu-id="0e817-117">При необходимости приложения могут устанавливать функцию обратного вызова yield.</span><span class="sxs-lookup"><span data-stu-id="0e817-117">Applications can optionally set a yield callback function.</span></span> <span data-ttu-id="0e817-118">Функция обратного вызова yield вызывается по крайней мере один раз для каждого видеокадра, захваченного при захвате потоковой передачи.</span><span class="sxs-lookup"><span data-stu-id="0e817-118">The yield callback function is called at least once for each video frame captured during streaming capture.</span></span> <span data-ttu-id="0e817-119">Если установлена функция обратного вызова yield, она будет вызываться независимо от состояния элемента **Фиелд** структуры [**каптурепармс**](/windows/win32/api/vfw/ns-vfw-captureparms) .</span><span class="sxs-lookup"><span data-stu-id="0e817-119">If a yield callback function is installed, it will be called regardless of the state of the **fYield** member of the [**CAPTUREPARMS**](/windows/win32/api/vfw/ns-vfw-captureparms) structure.</span></span>

<span data-ttu-id="0e817-120">Если используется функция обратного вызова yield, ее необходимо установить перед запуском сеанса записи, и она должна оставаться включенной в течение сеанса.</span><span class="sxs-lookup"><span data-stu-id="0e817-120">If the yield callback function is used, it must be installed before starting the capture session and it must remain enabled for the duration of the session.</span></span> <span data-ttu-id="0e817-121">Его можно отключить после завершения потоковой записи.</span><span class="sxs-lookup"><span data-stu-id="0e817-121">It can be disabled after streaming capture ends.</span></span>

<span data-ttu-id="0e817-122">Приложения обычно выполняют некоторый тип обработки сообщений в функции обратного вызова, состоящей из цикла [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) , как в цикле обработки сообщений функции [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) .</span><span class="sxs-lookup"><span data-stu-id="0e817-122">Applications typically perform some type of message processing in the callback function consisting of a [PeekMessage](/windows/win32/api/winuser/nf-winuser-peekmessagea), [TranslateMessage](/windows/win32/api/winuser/nf-winuser-translatemessage), [DispatchMessage](/windows/win32/api/winuser/nf-winuser-dispatchmessage) loop, as in the message loop of a [WinMain](/windows/win32/api/winbase/nf-winbase-winmain) function.</span></span> <span data-ttu-id="0e817-123">Функция обратного вызова yield также должна фильтровать и удалять сообщения, которые могут вызвать проблемы повторного входа.</span><span class="sxs-lookup"><span data-stu-id="0e817-123">The yield callback function must also filter and remove messages that can cause reentrancy problems.</span></span>

<span data-ttu-id="0e817-124">Приложение обычно возвращает **значение true** в процедуре yield, чтобы продолжить потоковую передачу.</span><span class="sxs-lookup"><span data-stu-id="0e817-124">An application typically returns **TRUE** in the yield procedure to continue streaming capture.</span></span> <span data-ttu-id="0e817-125">Если функция обратного вызова Yield возвращает **значение false**, окно отслеживания останавливает процесс отслеживания.</span><span class="sxs-lookup"><span data-stu-id="0e817-125">If a yield callback function returns **FALSE**, the capture window stops the capture process.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e817-126">Требования</span><span class="sxs-lookup"><span data-stu-id="0e817-126">Requirements</span></span>



| <span data-ttu-id="0e817-127">Требование</span><span class="sxs-lookup"><span data-stu-id="0e817-127">Requirement</span></span> | <span data-ttu-id="0e817-128">Значение</span><span class="sxs-lookup"><span data-stu-id="0e817-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0e817-129">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0e817-129">Minimum supported client</span></span><br/> | <span data-ttu-id="0e817-130">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0e817-130">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0e817-131">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0e817-131">Minimum supported server</span></span><br/> | <span data-ttu-id="0e817-132">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0e817-132">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0e817-133">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0e817-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e817-134"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e817-134"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e817-135">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0e817-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e817-136">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="0e817-136">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="0e817-137">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="0e817-137">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

