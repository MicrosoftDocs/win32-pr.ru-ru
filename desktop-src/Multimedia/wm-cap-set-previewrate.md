---
title: Сообщение WM_CAP_SET_PREVIEWRATE (VFW. h)
description: '\_Сообщение превиеврате закрепления WM \_ \_ устанавливает частоту показа кадров в режиме предварительного просмотра. Это сообщение можно отправить явно или с помощью макроса Каппревиеврате.'
ms.assetid: 1189ad4a-1f32-4684-920b-ee3c26ef97f8
keywords:
- WM_CAP_SET_PREVIEWRATE сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- WM_CAP_SET_PREVIEWRATE
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1134255b73e579841800af6cd5f6900965217106
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "103989321"
---
# <a name="wm_cap_set_previewrate-message"></a><span data-ttu-id="32596-105">\_ \_ Сообщение превиеврате установки крепления WM \_</span><span class="sxs-lookup"><span data-stu-id="32596-105">WM\_CAP\_SET\_PREVIEWRATE message</span></span>

<span data-ttu-id="32596-106">Сообщение **\_ \_ \_ превиеврате закрепления WM** устанавливает частоту показа кадров в режиме предварительного просмотра.</span><span class="sxs-lookup"><span data-stu-id="32596-106">The **WM\_CAP\_SET\_PREVIEWRATE** message sets the frame display rate in preview mode.</span></span> <span data-ttu-id="32596-107">Это сообщение можно отправить явно или с помощью макроса [**каппревиеврате**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) .</span><span class="sxs-lookup"><span data-stu-id="32596-107">You can send this message explicitly or by using the [**capPreviewRate**](/windows/desktop/api/Vfw/nf-vfw-cappreviewrate) macro.</span></span>


```C++
WM_CAP_SET_PREVIEWRATE 
wParam = (WPARAM) (wMS); 
lParam = 0L; 
```



## <a name="parameters"></a><span data-ttu-id="32596-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="32596-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32596-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*</span><span class="sxs-lookup"><span data-stu-id="32596-109"><span id="wMS"></span><span id="wms"></span><span id="WMS"></span>*wMS*</span></span>
</dt> <dd>

<span data-ttu-id="32596-110">Скорость записи и отображения новых кадров (в миллисекундах).</span><span class="sxs-lookup"><span data-stu-id="32596-110">Rate, in milliseconds, at which new frames are captured and displayed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32596-111">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="32596-111">Return Value</span></span>

<span data-ttu-id="32596-112">Возвращает **значение true** в случае успеха или **false** , если окно записи не подключено к драйверу записи.</span><span class="sxs-lookup"><span data-stu-id="32596-112">Returns **TRUE** if successful or **FALSE** if the capture window is not connected to a capture driver.</span></span>

## <a name="remarks"></a><span data-ttu-id="32596-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="32596-113">Remarks</span></span>

<span data-ttu-id="32596-114">В режиме предварительного просмотра используются существенные ресурсы ЦП.</span><span class="sxs-lookup"><span data-stu-id="32596-114">The preview mode uses substantial CPU resources.</span></span> <span data-ttu-id="32596-115">Приложения могут отключить предварительный просмотр или уменьшить частоту предварительной версии, когда фокус находится на другом приложении.</span><span class="sxs-lookup"><span data-stu-id="32596-115">Applications can disable preview or lower the preview rate when another application has the focus.</span></span> <span data-ttu-id="32596-116">Во время потоковой передачи видео задача предварительного просмотра имеет более низкий приоритет, чем запись кадров на диск, а предварительный просмотр кадров отображается только в том случае, если другие буферы недоступны для записи.</span><span class="sxs-lookup"><span data-stu-id="32596-116">During streaming video capture, the previewing task is lower priority than writing frames to disk, and preview frames are displayed only if no other buffers are available for writing.</span></span>

## <a name="requirements"></a><span data-ttu-id="32596-117">Требования</span><span class="sxs-lookup"><span data-stu-id="32596-117">Requirements</span></span>



| <span data-ttu-id="32596-118">Требование</span><span class="sxs-lookup"><span data-stu-id="32596-118">Requirement</span></span> | <span data-ttu-id="32596-119">Значение</span><span class="sxs-lookup"><span data-stu-id="32596-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="32596-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="32596-120">Minimum supported client</span></span><br/> | <span data-ttu-id="32596-121">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="32596-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="32596-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="32596-122">Minimum supported server</span></span><br/> | <span data-ttu-id="32596-123">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="32596-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="32596-124">Заголовок</span><span class="sxs-lookup"><span data-stu-id="32596-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="32596-125"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="32596-125"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32596-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="32596-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32596-127">Видеозапись</span><span class="sxs-lookup"><span data-stu-id="32596-127">Video Capture</span></span>](video-capture.md)
</dt> <dt>

[<span data-ttu-id="32596-128">Сообщения видеозаписи</span><span class="sxs-lookup"><span data-stu-id="32596-128">Video Capture Messages</span></span>](video-capture-messages.md)
</dt> </dl>

 

 





