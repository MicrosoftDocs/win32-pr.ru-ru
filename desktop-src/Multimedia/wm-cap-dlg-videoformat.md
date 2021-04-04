---
title: Сообщение WM_CAP_DLG_VIDEOFORMAT (VFW. h)
description: В \_ сообщении о \_ видеоформате WM Cap \_ появляется диалоговое окно, в котором пользователь может выбрать формат видео.
ms.assetid: 3b44507e-3806-467f-877a-e9992d1337cb
keywords:
- WM_CAP_DLG_VIDEOFORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d244c4c141845d4ede66804918514e091872e89
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103988530"
---
# <a name="wm_cap_dlg_videoformat-message"></a><span data-ttu-id="6c632-104">\_ \_ Сообщение видеоформат с диалогом WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="6c632-104">WM\_CAP\_DLG\_VIDEOFORMAT message</span></span>

<span data-ttu-id="6c632-105">В сообщении о **\_ \_ \_ видеоформате WM Cap** появляется диалоговое окно, в котором пользователь может выбрать формат видео.</span><span class="sxs-lookup"><span data-stu-id="6c632-105">The **WM\_CAP\_DLG\_VIDEOFORMAT** message displays a dialog box in which the user can select the video format.</span></span> <span data-ttu-id="6c632-106">Диалоговое окно Формат видео можно использовать для выбора размеров изображения, глубины битов и параметров аппаратного сжатия.</span><span class="sxs-lookup"><span data-stu-id="6c632-106">The Video Format dialog box might be used to select image dimensions, bit depth, and hardware compression options.</span></span> <span data-ttu-id="6c632-107">Это сообщение можно отправить явно или с помощью макроса [**капдлгвидеоформат**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) .</span><span class="sxs-lookup"><span data-stu-id="6c632-107">You can send this message explicitly or by using the [**capDlgVideoFormat**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideoformat) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOFORMAT 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="6c632-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6c632-108">Return Value</span></span>

<span data-ttu-id="6c632-109">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="6c632-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c632-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="6c632-110">Remarks</span></span>

<span data-ttu-id="6c632-111">После возврата этого сообщения приложениям может потребоваться обновить структуру [**капстатус**](/windows/win32/api/vfw/ns-vfw-capstatus) , так как пользователь мог изменить размеры изображения.</span><span class="sxs-lookup"><span data-stu-id="6c632-111">After this message returns, applications might need to update the [**CAPSTATUS**](/windows/win32/api/vfw/ns-vfw-capstatus) structure because the user might have changed the image dimensions.</span></span>

<span data-ttu-id="6c632-112">Диалоговое окно Формат видео является уникальным для каждого драйвера записи.</span><span class="sxs-lookup"><span data-stu-id="6c632-112">The Video Format dialog box is unique for each capture driver.</span></span> <span data-ttu-id="6c632-113">Некоторые драйверы записи могут не поддерживать диалоговое окно формата видео.</span><span class="sxs-lookup"><span data-stu-id="6c632-113">Some capture drivers might not support a Video Format dialog box.</span></span> <span data-ttu-id="6c632-114">Приложения могут определить, поддерживает ли драйвер записи это сообщение, проверив элемент **фхасдлгвидеоформат** в [**капдриверкапс**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).</span><span class="sxs-lookup"><span data-stu-id="6c632-114">Applications can determine if the capture driver supports this message by checking the **fHasDlgVideoFormat** member of [**CAPDRIVERCAPS**](/windows/win32/api/vfw/ns-vfw-capdrivercaps).</span></span>

## <a name="requirements"></a><span data-ttu-id="6c632-115">Требования</span><span class="sxs-lookup"><span data-stu-id="6c632-115">Requirements</span></span>



| <span data-ttu-id="6c632-116">Требование</span><span class="sxs-lookup"><span data-stu-id="6c632-116">Requirement</span></span> | <span data-ttu-id="6c632-117">Значение</span><span class="sxs-lookup"><span data-stu-id="6c632-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="6c632-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="6c632-118">Minimum supported client</span></span><br/> | <span data-ttu-id="6c632-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6c632-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="6c632-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="6c632-120">Minimum supported server</span></span><br/> | <span data-ttu-id="6c632-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="6c632-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="6c632-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="6c632-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c632-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c632-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c632-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="6c632-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c632-125">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="6c632-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="6c632-126">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="6c632-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





