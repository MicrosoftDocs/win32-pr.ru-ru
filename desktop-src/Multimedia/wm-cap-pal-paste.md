---
title: Сообщение WM_CAP_PAL_PASTE (VFW. h)
description: Сообщение о \_ \_ вставке WM Cap PAL \_ копирует палитру из буфера обмена и передает ее драйверу записи. Это сообщение можно отправить явно или с помощью макроса Каппалеттепасте.
ms.assetid: d49c7fd9-be40-4a07-8339-b85f7c4c331e
keywords:
- WM_CAP_PAL_PASTE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_PAL_PASTE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3daf88c69edbb8bad6257456b95a86c8a68df328
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988454"
---
# <a name="wm_cap_pal_paste-message"></a><span data-ttu-id="b661c-105">\_Вставка сообщения с ограничением WM \_ PAL \_</span><span class="sxs-lookup"><span data-stu-id="b661c-105">WM\_CAP\_PAL\_PASTE message</span></span>

<span data-ttu-id="b661c-106">Сообщение **о \_ \_ \_ вставке WM Cap PAL** копирует палитру из буфера обмена и передает ее драйверу записи.</span><span class="sxs-lookup"><span data-stu-id="b661c-106">The **WM\_CAP\_PAL\_PASTE** message copies the palette from the clipboard and passes it to a capture driver.</span></span> <span data-ttu-id="b661c-107">Это сообщение можно отправить явно или с помощью макроса [**каппалеттепасте**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) .</span><span class="sxs-lookup"><span data-stu-id="b661c-107">You can send this message explicitly or by using the [**capPalettePaste**](/windows/desktop/api/Vfw/nf-vfw-cappalettepaste) macro.</span></span>


```C++
WM_CAP_PAL_PASTE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="b661c-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b661c-108">Return Value</span></span>

<span data-ttu-id="b661c-109">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b661c-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="b661c-110">Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.</span><span class="sxs-lookup"><span data-stu-id="b661c-110">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="remarks"></a><span data-ttu-id="b661c-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b661c-111">Remarks</span></span>

<span data-ttu-id="b661c-112">Драйвер записи использует палитру при необходимости в указанном цифровом формате видео.</span><span class="sxs-lookup"><span data-stu-id="b661c-112">A capture driver uses a palette when required by the specified digitized video format.</span></span>

## <a name="requirements"></a><span data-ttu-id="b661c-113">Требования</span><span class="sxs-lookup"><span data-stu-id="b661c-113">Requirements</span></span>



| <span data-ttu-id="b661c-114">Требование</span><span class="sxs-lookup"><span data-stu-id="b661c-114">Requirement</span></span> | <span data-ttu-id="b661c-115">Значение</span><span class="sxs-lookup"><span data-stu-id="b661c-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b661c-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b661c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b661c-117">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b661c-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b661c-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b661c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b661c-119">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b661c-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b661c-120">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b661c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b661c-121"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b661c-121"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b661c-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b661c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b661c-123">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="b661c-123">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="b661c-124">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="b661c-124">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





