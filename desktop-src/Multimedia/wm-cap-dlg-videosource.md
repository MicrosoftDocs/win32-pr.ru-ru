---
title: Сообщение WM_CAP_DLG_VIDEOSOURCE (VFW. h)
description: В \_ сообщении о \_ видеосаурцее WM Cap \_ появляется диалоговое окно, в котором пользователь может управлять источником видео.
ms.assetid: 8dc2f271-1f48-4e63-badf-9f3322063018
keywords:
- WM_CAP_DLG_VIDEOSOURCE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOSOURCE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 38e8ae7e3d619964a547fbe0db4517fd1e7d277f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490113"
---
# <a name="wm_cap_dlg_videosource-message"></a><span data-ttu-id="dd91b-104">\_ \_ Сообщение видеосаурце с диалогом WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="dd91b-104">WM\_CAP\_DLG\_VIDEOSOURCE message</span></span>

<span data-ttu-id="dd91b-105">В сообщении о **\_ \_ \_ видеосаурцее WM Cap** появляется диалоговое окно, в котором пользователь может управлять источником видео.</span><span class="sxs-lookup"><span data-stu-id="dd91b-105">The **WM\_CAP\_DLG\_VIDEOSOURCE** message displays a dialog box in which the user can control the video source.</span></span> <span data-ttu-id="dd91b-106">Диалоговое окно Источник видео может содержать элементы управления, которые выбирают источники входных данных. изменение оттенка, контраста, яркости изображения; и изменить качество видео перед воспроизведением изображений в буфер кадров.</span><span class="sxs-lookup"><span data-stu-id="dd91b-106">The Video Source dialog box might contain controls that select input sources; alter the hue, contrast, brightness of the image; and modify the video quality before digitizing the images into the frame buffer.</span></span> <span data-ttu-id="dd91b-107">Это сообщение можно отправить явно или с помощью макроса [**капдлгвидеосаурце**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) .</span><span class="sxs-lookup"><span data-stu-id="dd91b-107">You can send this message explicitly or by using the [**capDlgVideoSource**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideosource) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOSOURCE 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="dd91b-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="dd91b-108">Return Value</span></span>

<span data-ttu-id="dd91b-109">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="dd91b-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="dd91b-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="dd91b-110">Remarks</span></span>

<span data-ttu-id="dd91b-111">Диалоговое окно Источник видео является уникальным для каждого драйвера записи.</span><span class="sxs-lookup"><span data-stu-id="dd91b-111">The Video Source dialog box is unique for each capture driver.</span></span> <span data-ttu-id="dd91b-112">Некоторые драйверы записи могут не поддерживать диалоговое окно "источник видео".</span><span class="sxs-lookup"><span data-stu-id="dd91b-112">Some capture drivers might not support a Video Source dialog box.</span></span> <span data-ttu-id="dd91b-113">Приложения могут определить, поддерживает ли драйвер записи это сообщение, проверив элемент **фхасдлгвидеосаурце** структуры [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) .</span><span class="sxs-lookup"><span data-stu-id="dd91b-113">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoSource** member of the [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd91b-114">Требования</span><span class="sxs-lookup"><span data-stu-id="dd91b-114">Requirements</span></span>



| <span data-ttu-id="dd91b-115">Требование</span><span class="sxs-lookup"><span data-stu-id="dd91b-115">Requirement</span></span> | <span data-ttu-id="dd91b-116">Значение</span><span class="sxs-lookup"><span data-stu-id="dd91b-116">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="dd91b-117">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="dd91b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="dd91b-118">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dd91b-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="dd91b-119">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="dd91b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="dd91b-120">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="dd91b-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="dd91b-121">Заголовок</span><span class="sxs-lookup"><span data-stu-id="dd91b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="dd91b-122"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="dd91b-122"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd91b-123">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="dd91b-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd91b-124">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="dd91b-124">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="dd91b-125">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="dd91b-125">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





