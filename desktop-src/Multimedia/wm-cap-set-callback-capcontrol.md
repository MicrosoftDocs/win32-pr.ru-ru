---
title: Сообщение WM_CAP_SET_CALLBACK_CAPCONTROL (VFW. h)
description: '\_ \_ \_ Сообщение капконтрол для обратного вызова Set крепления WM \_ устанавливает функцию обратного вызова в приложении, предоставляющем точный контроль записи. Это сообщение можно отправить явно или с помощью макроса Капсеткаллбакконкапконтрол.'
ms.assetid: 1e93ed7b-8205-45fe-bdcf-efe3f709f728
keywords:
- WM_CAP_SET_CALLBACK_CAPCONTROL сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_CAPCONTROL
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7fda38bbc79461b7c5ccaf9b3a32c2c3a0f9e3e1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661933"
---
# <a name="wm_cap_set_callback_capcontrol-message"></a><span data-ttu-id="0c32f-105">\_Сообщение о \_ \_ капконтрол обратного вызова Set крепления WM \_</span><span class="sxs-lookup"><span data-stu-id="0c32f-105">WM\_CAP\_SET\_CALLBACK\_CAPCONTROL message</span></span>

<span data-ttu-id="0c32f-106">Сообщение **\_ капконтрол для \_ \_ обратного \_ вызова Set крепления WM** устанавливает функцию обратного вызова в приложении, предоставляющем точный контроль записи.</span><span class="sxs-lookup"><span data-stu-id="0c32f-106">The **WM\_CAP\_SET\_CALLBACK\_CAPCONTROL** message sets a callback function in the application giving it precise recording control.</span></span> <span data-ttu-id="0c32f-107">Это сообщение можно отправить явно или с помощью макроса [**капсеткаллбакконкапконтрол**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) .</span><span class="sxs-lookup"><span data-stu-id="0c32f-107">You can send this message explicitly or by using the [**capSetCallbackOnCapControl**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackoncapcontrol) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_CAPCONTROL 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="0c32f-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c32f-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0c32f-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*фппрок*</span><span class="sxs-lookup"><span data-stu-id="0c32f-109"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="0c32f-110">Указатель на функцию обратного вызова типа [**капконтролкаллбакк**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback).</span><span class="sxs-lookup"><span data-stu-id="0c32f-110">Pointer to the callback function, of type [**capControlCallback**](/windows/desktop/api/Vfw/nc-vfw-capcontrolcallback).</span></span> <span data-ttu-id="0c32f-111">Укажите **значение NULL** для этого параметра, чтобы отключить ранее установленную функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="0c32f-111">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0c32f-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c32f-112">Return Value</span></span>

<span data-ttu-id="0c32f-113">Возвращает **значение true** в случае успеха или **false** , если выполняется захват потоковой передачи или однокадровый сеанс записи.</span><span class="sxs-lookup"><span data-stu-id="0c32f-113">Returns **TRUE** if successful or **FALSE** if a streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="0c32f-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0c32f-114">Remarks</span></span>

<span data-ttu-id="0c32f-115">Одна функция обратного вызова используется для предоставления приложению точного контроля над временем начала и завершения потоковой записи.</span><span class="sxs-lookup"><span data-stu-id="0c32f-115">A single callback function is used to give the application precise control over the moments that streaming capture begins and completes.</span></span> <span data-ttu-id="0c32f-116">Окно записи сначала вызывает процедуру с параметром *nсведения* , установленным в значение контролкаллбакк, \_ после выделения всех буферов и завершения всех остальных подготовительных действий.</span><span class="sxs-lookup"><span data-stu-id="0c32f-116">The capture window first calls the procedure with *nState* set to CONTROLCALLBACK\_PREROLL after all buffers have been allocated and all other capture preparations have finished.</span></span> <span data-ttu-id="0c32f-117">Это дает приложению возможность предварительно выполнить предварительную пробную работу с видеоисточниками, возвращая функцию обратного вызова в процессе записи.</span><span class="sxs-lookup"><span data-stu-id="0c32f-117">This gives the application the ability to preroll video sources, returning from the callback function at the exact moment recording is to begin.</span></span> <span data-ttu-id="0c32f-118">Возвращаемое значение **true** из функции обратного вызова продолжит запись, а возвращаемое значение **false** прерывает захват.</span><span class="sxs-lookup"><span data-stu-id="0c32f-118">A return value of **TRUE** from the callback function continues capture, and a return value of **FALSE** aborts capture.</span></span> <span data-ttu-id="0c32f-119">После начала записи эта функция обратного вызова будет вызываться часто с параметром *nсведения* , равным контролкаллбакк \_ Capture, чтобы разрешить приложению завершать захват, возвращая **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0c32f-119">After capture begins, this callback function will be called frequently with *nState* set to CONTROLCALLBACK\_CAPTURING to allow the application to end capture by returning **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c32f-120">Требования</span><span class="sxs-lookup"><span data-stu-id="0c32f-120">Requirements</span></span>



| <span data-ttu-id="0c32f-121">Требование</span><span class="sxs-lookup"><span data-stu-id="0c32f-121">Requirement</span></span> | <span data-ttu-id="0c32f-122">Значение</span><span class="sxs-lookup"><span data-stu-id="0c32f-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="0c32f-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0c32f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="0c32f-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0c32f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="0c32f-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0c32f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="0c32f-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="0c32f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0c32f-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="0c32f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c32f-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="0c32f-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c32f-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0c32f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c32f-130">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="0c32f-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="0c32f-131">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="0c32f-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





