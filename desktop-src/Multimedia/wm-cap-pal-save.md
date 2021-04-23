---
title: Сообщение WM_CAP_PAL_SAVE (VFW. h)
description: Сообщение о \_ СОХРАНЕНИИ WM Cap \_ PAL \_ сохраняет текущую палитру в файле палитры. Файлы палитры обычно используют расширение имени файла. Списком. Это сообщение можно отправить явно или с помощью макроса Каппалеттесаве.
ms.assetid: b1fa3978-9147-403f-aa08-db1a803aa5ac
keywords:
- WM_CAP_PAL_SAVE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_PAL_SAVE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5ea36b2eaf50b2555fa849a176d12d0932eed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "105661934"
---
# <a name="wm_cap_pal_save-message"></a><span data-ttu-id="d31c8-106">Сообщение о сохранении в формате WM \_ Cap \_ PAL \_</span><span class="sxs-lookup"><span data-stu-id="d31c8-106">WM\_CAP\_PAL\_SAVE message</span></span>

<span data-ttu-id="d31c8-107">Сообщение **о \_ \_ \_ сохранении WM Cap PAL** сохраняет текущую палитру в файле палитры.</span><span class="sxs-lookup"><span data-stu-id="d31c8-107">The **WM\_CAP\_PAL\_SAVE** message saves the current palette to a palette file.</span></span> <span data-ttu-id="d31c8-108">Файлы палитры обычно используют расширение имени файла. Списком.</span><span class="sxs-lookup"><span data-stu-id="d31c8-108">Palette files typically use the filename extension .PAL.</span></span> <span data-ttu-id="d31c8-109">Это сообщение можно отправить явно или с помощью макроса [**каппалеттесаве**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) .</span><span class="sxs-lookup"><span data-stu-id="d31c8-109">You can send this message explicitly or by using the [**capPaletteSave**](/windows/desktop/api/Vfw/nf-vfw-cappalettesave) macro.</span></span>


```C++
WM_CAP_PAL_SAVE 
wParam = (WPARAM) 0; 
lParam = (LPARAM) (LPVOID) (LPSTR) (szName); 
```



## <a name="parameters"></a><span data-ttu-id="d31c8-110">Параметры</span><span class="sxs-lookup"><span data-stu-id="d31c8-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d31c8-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span><span class="sxs-lookup"><span data-stu-id="d31c8-111"><span id="szName"></span><span id="szname"></span><span id="SZNAME"></span>*szName*</span></span>
</dt> <dd>

<span data-ttu-id="d31c8-112">Указатель на строку с завершающим нулем, содержащую имя файла палитры.</span><span class="sxs-lookup"><span data-stu-id="d31c8-112">Pointer to a null-terminated string containing the palette filename.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d31c8-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d31c8-113">Return Value</span></span>

<span data-ttu-id="d31c8-114">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="d31c8-114">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

<span data-ttu-id="d31c8-115">Если возникает ошибка и функция обратного вызова ошибки устанавливается с помощью сообщения [**\_ \_ \_ \_ об ошибке обратного вызова**](wm-cap-set-callback-error.md) , то вызывается функция обратного вызова ошибки.</span><span class="sxs-lookup"><span data-stu-id="d31c8-115">If an error occurs and an error callback function is set using the [**WM\_CAP\_SET\_CALLBACK\_ERROR**](wm-cap-set-callback-error.md) message, the error callback function is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="d31c8-116">Требования</span><span class="sxs-lookup"><span data-stu-id="d31c8-116">Requirements</span></span>



| <span data-ttu-id="d31c8-117">Требование</span><span class="sxs-lookup"><span data-stu-id="d31c8-117">Requirement</span></span> | <span data-ttu-id="d31c8-118">Значение</span><span class="sxs-lookup"><span data-stu-id="d31c8-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d31c8-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d31c8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="d31c8-120">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d31c8-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="d31c8-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d31c8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="d31c8-122">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="d31c8-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="d31c8-123">Заголовок</span><span class="sxs-lookup"><span data-stu-id="d31c8-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="d31c8-124"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="d31c8-124"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d31c8-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d31c8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d31c8-126">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="d31c8-126">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="d31c8-127">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="d31c8-127">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





