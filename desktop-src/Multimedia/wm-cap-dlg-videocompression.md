---
title: Сообщение WM_CAP_DLG_VIDEOCOMPRESSION (VFW. h)
description: В \_ сообщении о \_ видеокомпрессионе WM Cap \_ появляется диалоговое окно, в котором пользователь может выбрать программу сжатия для использования в процессе записи.
ms.assetid: 526e4b5d-49a4-4bb5-92d6-cdd567636354
keywords:
- WM_CAP_DLG_VIDEOCOMPRESSION сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_DLG_VIDEOCOMPRESSION
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d851f73df7adbc205585eb7c69ad9d4d969aba66
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071593"
---
# <a name="wm_cap_dlg_videocompression-message"></a><span data-ttu-id="e27d4-104">\_ \_ Сообщение видеокомпрессион с диалогом WM Cap \_</span><span class="sxs-lookup"><span data-stu-id="e27d4-104">WM\_CAP\_DLG\_VIDEOCOMPRESSION message</span></span>

<span data-ttu-id="e27d4-105">В сообщении о **\_ \_ \_ видеокомпрессионе WM Cap** появляется диалоговое окно, в котором пользователь может выбрать программу сжатия для использования в процессе записи.</span><span class="sxs-lookup"><span data-stu-id="e27d4-105">The **WM\_CAP\_DLG\_VIDEOCOMPRESSION** message displays a dialog box in which the user can select a compressor to use during the capture process.</span></span> <span data-ttu-id="e27d4-106">Список доступных компрессоров может различаться в зависимости от формата видео, выбранного в диалоговом окне Формат видео драйвера записи.</span><span class="sxs-lookup"><span data-stu-id="e27d4-106">The list of available compressors can vary with the video format selected in the capture driver's Video Format dialog box.</span></span> <span data-ttu-id="e27d4-107">Это сообщение можно отправить явно или с помощью макроса [**капдлгвидеокомпрессион**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) .</span><span class="sxs-lookup"><span data-stu-id="e27d4-107">You can send this message explicitly or by using the [**capDlgVideoCompression**](/windows/desktop/api/Vfw/nf-vfw-capdlgvideocompression) macro.</span></span>


```C++
WM_CAP_DLG_VIDEOCOMPRESSION 
wParam = (WPARAM) 0; 
lParam = 0L; 
```



## <a name="return-value"></a><span data-ttu-id="e27d4-108">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e27d4-108">Return Value</span></span>

<span data-ttu-id="e27d4-109">Возвращает **значение true** в случае успеха или **false** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e27d4-109">Returns **TRUE** if successful or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="e27d4-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="e27d4-110">Remarks</span></span>

<span data-ttu-id="e27d4-111">Используйте это сообщение с драйверами записи, предоставляющими кадры только в формате RGB для бизнес-аналитики \_ .</span><span class="sxs-lookup"><span data-stu-id="e27d4-111">Use this message with capture drivers that provide frames only in the BI\_RGB format.</span></span> <span data-ttu-id="e27d4-112">Это сообщение наиболее полезно в операции записи шага для объединения захвата и сжатия в одной операции.</span><span class="sxs-lookup"><span data-stu-id="e27d4-112">This message is most useful in the step capture operation to combine capture and compression in a single operation.</span></span> <span data-ttu-id="e27d4-113">Сжатие кадров с программным компрессором в рамках операции записи в реальном времени, скорее всего, занимает слишком много времени.</span><span class="sxs-lookup"><span data-stu-id="e27d4-113">Compressing frames with a software compressor as part of a real-time capture operation is most likely too time-consuming to perform.</span></span>

<span data-ttu-id="e27d4-114">Сжатие не влияет на кадры, скопированные в буфер обмена.</span><span class="sxs-lookup"><span data-stu-id="e27d4-114">Compression does not affect the frames copied to the clipboard.</span></span>

## <a name="requirements"></a><span data-ttu-id="e27d4-115">Требования</span><span class="sxs-lookup"><span data-stu-id="e27d4-115">Requirements</span></span>



| <span data-ttu-id="e27d4-116">Требование</span><span class="sxs-lookup"><span data-stu-id="e27d4-116">Requirement</span></span> | <span data-ttu-id="e27d4-117">Значение</span><span class="sxs-lookup"><span data-stu-id="e27d4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="e27d4-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="e27d4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e27d4-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e27d4-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="e27d4-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="e27d4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e27d4-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="e27d4-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e27d4-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="e27d4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="e27d4-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="e27d4-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e27d4-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="e27d4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e27d4-125">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="e27d4-125">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="e27d4-126">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="e27d4-126">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





