---
title: Сообщение WM_CAP_DLG_VIDEODISPLAY (VFW. h)
description: В \_ сообщении о \_ видеодисплайе WM Cap \_ появляется диалоговое окно, в котором пользователь может задавать или настраивать выходные данные видео.
ms.assetid: 151056f5-a9d1-4594-a8d7-32d4675ae3d6
keywords:
- WM_CAP_DLG_VIDEODISPLAY сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEODISPLAY
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 378d80923f9c0b7eda65fac83809e30626d53406
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988623"
---
# <a name="wm_cap_dlg_videodisplay-message"></a><span data-ttu-id="53f43-104">\_ \_ Сообщение видеодисплай с диалогом WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="53f43-104">WM\_CAP\_DLG\_VIDEODISPLAY message</span></span>

<span data-ttu-id="53f43-105">В сообщении о **\_ \_ \_ видеодисплайе WM Cap** появляется диалоговое окно, в котором пользователь может задавать или настраивать выходные данные видео.</span><span class="sxs-lookup"><span data-stu-id="53f43-105">The **WM\_CAP\_DLG\_VIDEODISPLAY** message displays a dialog box in which the user can set or adjust the video output.</span></span> <span data-ttu-id="53f43-106">Это диалоговое окно может содержать элементы управления, которые влияют на оттенок, контрастность и яркость отображаемого изображения, а также на выравнивание цветового ключа.</span><span class="sxs-lookup"><span data-stu-id="53f43-106">This dialog box might contain controls that affect the hue, contrast, and brightness of the displayed image, as well as key color alignment.</span></span> <span data-ttu-id="53f43-107">Это сообщение можно отправить явно или с помощью макроса [**капдлгвидеодисплай**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) .</span><span class="sxs-lookup"><span data-stu-id="53f43-107">You can send this message explicitly or by using the [**capDlgVideoDisplay**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideodisplay) macro.</span></span>


```C++
WM_CAP_DLG_VIDEODISPLAY 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="53f43-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="53f43-108">Return Value</span></span>

<span data-ttu-id="53f43-109">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="53f43-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="53f43-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="53f43-110">Remarks</span></span>

<span data-ttu-id="53f43-111">Элементы управления в этом диалоговом окне не влияют на оцифрованные данные видео. они влияют только на вывод или повторное отображение видеосигнала.</span><span class="sxs-lookup"><span data-stu-id="53f43-111">The controls in this dialog box do not affect digitized video data; they affect only the output or redisplay of the video signal.</span></span>

<span data-ttu-id="53f43-112">Диалоговое окно «экран видео» является уникальным для каждого драйвера записи.</span><span class="sxs-lookup"><span data-stu-id="53f43-112">The Video Display dialog box is unique for each capture driver.</span></span> <span data-ttu-id="53f43-113">Некоторые драйверы записи могут не поддерживать диалоговое окно "отображение видео".</span><span class="sxs-lookup"><span data-stu-id="53f43-113">Some capture drivers might not support a Video Display dialog box.</span></span> <span data-ttu-id="53f43-114">Приложения могут определить, поддерживает ли драйвер записи это сообщение, проверив элемент **фхасдлгвидеодисплай** структуры [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="53f43-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoDisplay** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="53f43-115">Требования</span><span class="sxs-lookup"><span data-stu-id="53f43-115">Requirements</span></span>



| <span data-ttu-id="53f43-116">Требование</span><span class="sxs-lookup"><span data-stu-id="53f43-116">Requirement</span></span> | <span data-ttu-id="53f43-117">Значение</span><span class="sxs-lookup"><span data-stu-id="53f43-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="53f43-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="53f43-118">Minimum supported client</span></span><br/> | <span data-ttu-id="53f43-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="53f43-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="53f43-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="53f43-120">Minimum supported server</span></span><br/> | <span data-ttu-id="53f43-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="53f43-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="53f43-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="53f43-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="53f43-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="53f43-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="53f43-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="53f43-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="53f43-125">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="53f43-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="53f43-126">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="53f43-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





