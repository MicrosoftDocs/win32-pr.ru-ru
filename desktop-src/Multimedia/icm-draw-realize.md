---
title: Сообщение ICM_DRAW_REALIZE (VFW. h)
description: Сообщение ICM \_ Draw дает \_ уведомление драйверу подготовки отчетов о том, что во время рисования он реализует свою палитру рисования. Это сообщение можно отправить явно или с помощью макроса Икдравреализе.
ms.assetid: 501540cd-41e2-4f80-abf8-2ec2179970a9
keywords:
- ICM_DRAW_REALIZE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_DRAW_REALIZE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd054c16caae55cba25c30098337e54b0ec4b681
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104415361"
---
# <a name="icm_draw_realize-message"></a><span data-ttu-id="40a7e-105">\_Сообщение о выводе ICM \_</span><span class="sxs-lookup"><span data-stu-id="40a7e-105">ICM\_DRAW\_REALIZE message</span></span>

<span data-ttu-id="40a7e-106">Сообщение **ICM \_ Draw \_** дает уведомление драйверу подготовки отчетов о том, что во время рисования он реализует свою палитру рисования.</span><span class="sxs-lookup"><span data-stu-id="40a7e-106">The **ICM\_DRAW\_REALIZE** message notifies a rendering driver to realize its drawing palette while drawing.</span></span> <span data-ttu-id="40a7e-107">Это сообщение можно отправить явно или с помощью макроса [**икдравреализе**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) .</span><span class="sxs-lookup"><span data-stu-id="40a7e-107">You can send this message explicitly or by using the [**ICDrawRealize**](/windows/desktop/api/Vfw/nf-vfw-icdrawrealize) macro.</span></span>


```C++
ICM_DRAW_REALIZE 
wParam = (DWORD_PTR) (UINT_PTR) (HDC) hdc; 
lParam = (DWORD_PTR) (BOOL) fBackground; 
```



## <a name="parameters"></a><span data-ttu-id="40a7e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="40a7e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40a7e-109"><span id="hdc"></span><span id="HDC"></span>*HDC*</span><span class="sxs-lookup"><span data-stu-id="40a7e-109"><span id="hdc"></span><span id="HDC"></span>*hdc*</span></span>
</dt> <dd>

<span data-ttu-id="40a7e-110">Обработчик контроллера домена, используемый для реализации палитры.</span><span class="sxs-lookup"><span data-stu-id="40a7e-110">Handle to the DC used to realize the palette.</span></span>

</dd> <dt>

<span data-ttu-id="40a7e-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*фбаккграунд*</span><span class="sxs-lookup"><span data-stu-id="40a7e-111"><span id="fBackground"></span><span id="fbackground"></span><span id="FBACKGROUND"></span>*fBackground*</span></span>
</dt> <dd>

<span data-ttu-id="40a7e-112">Флаг фона.</span><span class="sxs-lookup"><span data-stu-id="40a7e-112">Background flag.</span></span> <span data-ttu-id="40a7e-113">Укажите **значение true** , чтобы реализовать палитру в качестве фоновой задачи, или **false** , чтобы реализовать палитру на переднем плане.</span><span class="sxs-lookup"><span data-stu-id="40a7e-113">Specify **TRUE** to realize the palette as a background task or **FALSE** to realize the palette in the foreground.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40a7e-114">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="40a7e-114">Return Value</span></span>

<span data-ttu-id="40a7e-115">Возвращает ИЦЕРР \_ ОК, если палитра рисования реализована или ицерр не \_ поддерживается, если реализована палитра, связанная с распакованными данными.</span><span class="sxs-lookup"><span data-stu-id="40a7e-115">Returns ICERR\_OK if the drawing palette is realized or ICERR\_UNSUPPORTED if the palette associated with the decompressed data is realized.</span></span>

## <a name="remarks"></a><span data-ttu-id="40a7e-116">Комментарии</span><span class="sxs-lookup"><span data-stu-id="40a7e-116">Remarks</span></span>

<span data-ttu-id="40a7e-117">Драйверы должны отвечать на это сообщение, только если палитра рисования отличается от сжатой палитры.</span><span class="sxs-lookup"><span data-stu-id="40a7e-117">Drivers need to respond to this message only if the drawing palette is different from the decompressed palette.</span></span>

## <a name="requirements"></a><span data-ttu-id="40a7e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="40a7e-118">Requirements</span></span>



| <span data-ttu-id="40a7e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="40a7e-119">Requirement</span></span> | <span data-ttu-id="40a7e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="40a7e-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="40a7e-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="40a7e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="40a7e-122">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="40a7e-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="40a7e-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="40a7e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="40a7e-124">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="40a7e-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="40a7e-125">Заголовок</span><span class="sxs-lookup"><span data-stu-id="40a7e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="40a7e-126"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="40a7e-126"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="40a7e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="40a7e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40a7e-128">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="40a7e-128">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="40a7e-129">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="40a7e-129">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





