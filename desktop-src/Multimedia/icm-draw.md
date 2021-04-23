---
title: Сообщение ICM_DRAW (VFW. h)
description: Сообщение ICM \_ Draw уведомляет драйвер подготовки, чтобы распаковать кадр данных и нарисовать его на экране.
ms.assetid: eceb42c6-d91a-45b7-98dc-e0944df3e558
keywords:
- ICM_DRAW сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d0840c6df2c69f4d3e45600cf8599c214b36200a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103802027"
---
# <a name="icm_draw-message"></a><span data-ttu-id="8820f-104">\_Сообщение о выводе ICM</span><span class="sxs-lookup"><span data-stu-id="8820f-104">ICM\_DRAW message</span></span>

<span data-ttu-id="8820f-105">Сообщение **ICM \_ Draw** уведомляет драйвер подготовки, чтобы распаковать кадр данных и нарисовать его на экране.</span><span class="sxs-lookup"><span data-stu-id="8820f-105">The **ICM\_DRAW** message notifies a rendering driver to decompress a frame of data and draw it to the screen.</span></span>


```C++
ICM_DRAW 
wParam = (DWORD) (LPVOID) &icdraw; 
lParam = sizeof(ICDRAW); 
```



## <a name="parameters"></a><span data-ttu-id="8820f-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8820f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8820f-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span><span class="sxs-lookup"><span data-stu-id="8820f-107"><span id="wParam"></span><span id="wparam"></span><span id="WPARAM"></span>*wParam*</span></span>
</dt> <dd>

<span data-ttu-id="8820f-108">Указатель на структуру [**икдрав**](/windows/desktop/api/Vfw/ns-vfw-icdraw) .</span><span class="sxs-lookup"><span data-stu-id="8820f-108">Pointer to an [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw) structure.</span></span>

</dd> <dt>

<span data-ttu-id="8820f-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span><span class="sxs-lookup"><span data-stu-id="8820f-109"><span id="lParam"></span><span id="lparam"></span><span id="LPARAM"></span>*lParam*</span></span>
</dt> <dd>

<span data-ttu-id="8820f-110">Размер [**икдрав**](/windows/desktop/api/Vfw/ns-vfw-icdraw)в байтах.</span><span class="sxs-lookup"><span data-stu-id="8820f-110">Size, in bytes, of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8820f-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="8820f-111">Return Value</span></span>

<span data-ttu-id="8820f-112">Возвращает ИЦЕРР \_ ОК в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="8820f-112">Returns ICERR\_OK if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="8820f-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="8820f-113">Remarks</span></span>

<span data-ttu-id="8820f-114">Если установлен \_ флаг обновления икдрав в элементе **dwFlags** [**икдрав**](/windows/desktop/api/Vfw/ns-vfw-icdraw), то область экрана, используемая для рисования, недопустима и должна быть обновлена.</span><span class="sxs-lookup"><span data-stu-id="8820f-114">If the ICDRAW\_UPDATE flag is set in the **dwFlags** member of [**ICDRAW**](/windows/desktop/api/Vfw/ns-vfw-icdraw), the area of the screen used for drawing is invalid and needs to be updated.</span></span> <span data-ttu-id="8820f-115">Степень обновления зависит от содержимого элемента **лпдата** .</span><span class="sxs-lookup"><span data-stu-id="8820f-115">The extent of updating depends on the contents of the **lpData** member.</span></span>

<span data-ttu-id="8820f-116">Если **лпдата** имеет **значение NULL**, драйвер должен обновить весь конечный прямоугольник с текущим изображением.</span><span class="sxs-lookup"><span data-stu-id="8820f-116">If **lpData** is **NULL**, the driver should update the entire destination rectangle with the current image.</span></span> <span data-ttu-id="8820f-117">Если драйвер сохраняет копию образа в буфере, который находится вне экрана, это сообщение может быть неудачным.</span><span class="sxs-lookup"><span data-stu-id="8820f-117">If the driver maintains a copy of the image in an off-screen buffer, it can fail this message.</span></span> <span data-ttu-id="8820f-118">Если **лпдата** имеет значение, не **равное NULL**, драйвер должен рисовать данные и обеспечить обновление всего места назначения.</span><span class="sxs-lookup"><span data-stu-id="8820f-118">If **lpData** is not **NULL**, the driver should draw the data and make sure the entire destination is updated.</span></span>

<span data-ttu-id="8820f-119">Если флаг ИКДРАВ \_ хуррюп установлен в **dwFlags**, вызывающее приложение хочет, чтобы драйвер был как можно быстрее, возможно, даже не обновлял экран.</span><span class="sxs-lookup"><span data-stu-id="8820f-119">If the ICDRAW\_HURRYUP flag is set in **dwFlags**, the calling application wants the driver to proceed as quickly as possible, possibly not even updating the screen.</span></span>

<span data-ttu-id="8820f-120">Если \_ в **dwFlags** ЗАДАН флаг предварительного отката икдрав, этот видеокадр является предварительной информацией и не должен отображаться, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="8820f-120">If the ICDRAW\_PREROLL flag is set in **dwFlags**, this video frame is preliminary information and should not be displayed if possible.</span></span> <span data-ttu-id="8820f-121">Например, если воспроизведение начинается с кадра 10, а кадр 0 является ближайшим предыдущим ключевым кадром, в кадрах от 0 до 9 будет \_ предустановлен икдрав.</span><span class="sxs-lookup"><span data-stu-id="8820f-121">For example, if play is to start from frame 10, and frame 0 is the nearest previous key frame, frames 0 through 9 will have ICDRAW\_PREROLL set.</span></span>

<span data-ttu-id="8820f-122">Если требуется, чтобы драйвер распаковать данные в буфер, отправьте сообщение [**ICM \_ unуплотнение**](icm-decompress.md) .</span><span class="sxs-lookup"><span data-stu-id="8820f-122">If you want the driver to decompress data into a buffer, send the [**ICM\_DECOMPRESS**](icm-decompress.md) message.</span></span>

## <a name="requirements"></a><span data-ttu-id="8820f-123">Требования</span><span class="sxs-lookup"><span data-stu-id="8820f-123">Requirements</span></span>



| <span data-ttu-id="8820f-124">Требование</span><span class="sxs-lookup"><span data-stu-id="8820f-124">Requirement</span></span> | <span data-ttu-id="8820f-125">Значение</span><span class="sxs-lookup"><span data-stu-id="8820f-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="8820f-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="8820f-126">Minimum supported client</span></span><br/> | <span data-ttu-id="8820f-127">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8820f-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="8820f-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="8820f-128">Minimum supported server</span></span><br/> | <span data-ttu-id="8820f-129">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="8820f-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="8820f-130">Заголовок</span><span class="sxs-lookup"><span data-stu-id="8820f-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="8820f-131"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="8820f-131"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8820f-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="8820f-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8820f-133">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="8820f-133">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="8820f-134">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="8820f-134">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





