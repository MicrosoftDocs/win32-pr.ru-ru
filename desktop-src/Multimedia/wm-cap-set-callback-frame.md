---
title: Сообщение WM_CAP_SET_CALLBACK_FRAME (VFW. h)
description: '\_ \_ \_ Сообщение кадра обратного вызова Set крепления WM \_ устанавливает функцию обратного вызова для предварительного просмотра в приложении. Авикап вызывает эту процедуру, когда окно отслеживания захватывает кадры предварительной версии. Это сообщение можно отправить явно или с помощью макроса Капсеткаллбакконфраме.'
ms.assetid: 3882e6f6-c48c-4e50-9697-cbdf5b9342a5
keywords:
- WM_CAP_SET_CALLBACK_FRAME сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_CALLBACK_FRAME
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b91c2f30ac0875e2f45592d3aa7e0a3ce9c296b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105672699"
---
# <a name="wm_cap_set_callback_frame-message"></a><span data-ttu-id="a47e3-106">\_ \_ \_ Сообщение кадра обратного вызова Set крепления WM \_</span><span class="sxs-lookup"><span data-stu-id="a47e3-106">WM\_CAP\_SET\_CALLBACK\_FRAME message</span></span>

<span data-ttu-id="a47e3-107">Сообщение **\_ \_ \_ \_ кадра обратного вызова Set крепления WM** устанавливает функцию обратного вызова для предварительного просмотра в приложении.</span><span class="sxs-lookup"><span data-stu-id="a47e3-107">The **WM\_CAP\_SET\_CALLBACK\_FRAME** message sets a preview callback function in the application.</span></span> <span data-ttu-id="a47e3-108">Авикап вызывает эту процедуру, когда окно отслеживания захватывает кадры предварительной версии.</span><span class="sxs-lookup"><span data-stu-id="a47e3-108">AVICap calls this procedure when the capture window captures preview frames.</span></span> <span data-ttu-id="a47e3-109">Это сообщение можно отправить явно или с помощью макроса [**капсеткаллбакконфраме**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) .</span><span class="sxs-lookup"><span data-stu-id="a47e3-109">You can send this message explicitly or by using the [**capSetCallbackOnFrame**](/windows/desktop/api/Vfw/nf-vfw-capsetcallbackonframe) macro.</span></span>


```C++
WM_CAP_SET_CALLBACK_FRAME 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (fpProc); 
```



## <a name="parameters"></a><span data-ttu-id="a47e3-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="a47e3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a47e3-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*фппрок*</span><span class="sxs-lookup"><span data-stu-id="a47e3-111"><span id="fpProc"></span><span id="fpproc"></span><span id="FPPROC"></span>*fpProc*</span></span>
</dt> <dd>

<span data-ttu-id="a47e3-112">Указатель на функцию обратного вызова предварительного просмотра типа [**капвидеостреамкаллбакк**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span><span class="sxs-lookup"><span data-stu-id="a47e3-112">Pointer to the preview callback function, of type [**capVideoStreamCallback**](/windows/desktop/api/Vfw/nc-vfw-capvideocallback).</span></span> <span data-ttu-id="a47e3-113">Укажите **значение NULL** для этого параметра, чтобы отключить ранее установленную функцию обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="a47e3-113">Specify **NULL** for this parameter to disable a previously installed callback function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a47e3-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a47e3-114">Return Value</span></span>

<span data-ttu-id="a47e3-115">Возвращает **значение true** в случае успеха или **false** , если выполняется захват потоковой передачи или однокадровый сеанс записи.</span><span class="sxs-lookup"><span data-stu-id="a47e3-115">Returns **TRUE** if successful or **FALSE** if streaming capture or a single-frame capture session is in progress.</span></span>

## <a name="remarks"></a><span data-ttu-id="a47e3-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a47e3-116">Remarks</span></span>

<span data-ttu-id="a47e3-117">Окно Capture (захват) вызывает функцию обратного вызова перед отображением кадров предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="a47e3-117">The capture window calls the callback function before displaying preview frames.</span></span> <span data-ttu-id="a47e3-118">Это позволяет приложению изменять фрейм при необходимости.</span><span class="sxs-lookup"><span data-stu-id="a47e3-118">This allows an application to modify the frame if desired.</span></span> <span data-ttu-id="a47e3-119">Эта функция обратного вызова не используется во время потоковой записи видео.</span><span class="sxs-lookup"><span data-stu-id="a47e3-119">This callback function is not used during streaming video capture.</span></span>

## <a name="requirements"></a><span data-ttu-id="a47e3-120">Требования</span><span class="sxs-lookup"><span data-stu-id="a47e3-120">Requirements</span></span>



| <span data-ttu-id="a47e3-121">Требование</span><span class="sxs-lookup"><span data-stu-id="a47e3-121">Requirement</span></span> | <span data-ttu-id="a47e3-122">Значение</span><span class="sxs-lookup"><span data-stu-id="a47e3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="a47e3-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a47e3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="a47e3-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a47e3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="a47e3-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a47e3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="a47e3-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="a47e3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="a47e3-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="a47e3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="a47e3-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="a47e3-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a47e3-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a47e3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a47e3-130">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="a47e3-130">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="a47e3-131">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="a47e3-131">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





