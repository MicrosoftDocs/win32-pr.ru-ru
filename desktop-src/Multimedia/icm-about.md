---
title: Сообщение ICM_ABOUT (VFW. h)
description: ICM \_ о сообщении уведомляет драйвер сжатия видео о необходимости отобразить диалоговое окно о программе или запрашивает драйвер сжатия видео, чтобы определить, имеется ли в нем диалоговое окно About. Это сообщение можно отправить явно или с помощью макроса Икабаут.
ms.assetid: 6eca69a3-0463-48e6-befb-5003b7515e7d
keywords:
- ICM_ABOUT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- ICM_ABOUT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1e03e88993ba1e345a3ea32a9de7adb2d63abe9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104071095"
---
# <a name="icm_about-message"></a><span data-ttu-id="b589e-105">ICM \_ о сообщении</span><span class="sxs-lookup"><span data-stu-id="b589e-105">ICM\_ABOUT message</span></span>

<span data-ttu-id="b589e-106">**ICM \_ о** сообщении уведомляет драйвер сжатия видео о необходимости отобразить диалоговое окно о программе или запрашивает драйвер сжатия видео, чтобы определить, имеется ли в нем диалоговое окно About.</span><span class="sxs-lookup"><span data-stu-id="b589e-106">The **ICM\_ABOUT** message notifies a video compression driver to display its About dialog box or queries a video compression driver to determine if it has an About dialog box.</span></span> <span data-ttu-id="b589e-107">Это сообщение можно отправить явно или с помощью макроса [**икабаут**](/windows/desktop/api/Vfw/nf-vfw-icabout) .</span><span class="sxs-lookup"><span data-stu-id="b589e-107">You can send this message explicitly or by using the [**ICAbout**](/windows/desktop/api/Vfw/nf-vfw-icabout) macro.</span></span>


```C++
ICM_ABOUT 
wParam = (DWORD_PTR) (UINT_PTR) hwnd; 
lParam = 0; 
```



## <a name="parameters"></a><span data-ttu-id="b589e-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="b589e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b589e-109"><span id="hwnd"></span><span id="HWND"></span>*HWND*</span><span class="sxs-lookup"><span data-stu-id="b589e-109"><span id="hwnd"></span><span id="HWND"></span>*hwnd*</span></span>
</dt> <dd>

<span data-ttu-id="b589e-110">Обработано с родительским окном отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="b589e-110">Handle to the parent window of the displayed dialog box.</span></span> <span data-ttu-id="b589e-111">Можно также определить, содержит ли драйвер диалоговое окно о программе, указав в этом параметре значение-1, как в макросе [**иккуерябаут**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) .</span><span class="sxs-lookup"><span data-stu-id="b589e-111">You can also determine if a driver has an About dialog box by specifying -1 in this parameter, as in the [**ICQueryAbout**](/windows/desktop/api/Vfw/nf-vfw-icqueryabout) macro.</span></span> <span data-ttu-id="b589e-112">Драйвер возвращает ИЦЕРР \_ ОК, если в нем есть диалоговое окно About или ицерр не \_ поддерживается в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b589e-112">The driver returns ICERR\_OK if it has an About dialog box or ICERR\_UNSUPPORTED otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b589e-113">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b589e-113">Return Value</span></span>

<span data-ttu-id="b589e-114">Возвращает ИЦЕРР \_ ОК, если драйвер поддерживает это сообщение или ИЦЕРР \_ не поддерживается в противном случае.</span><span class="sxs-lookup"><span data-stu-id="b589e-114">Returns ICERR\_OK if the driver supports this message or ICERR\_UNSUPPORTED otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="b589e-115">Требования</span><span class="sxs-lookup"><span data-stu-id="b589e-115">Requirements</span></span>



| <span data-ttu-id="b589e-116">Требование</span><span class="sxs-lookup"><span data-stu-id="b589e-116">Requirement</span></span> | <span data-ttu-id="b589e-117">Значение</span><span class="sxs-lookup"><span data-stu-id="b589e-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="b589e-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b589e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b589e-119">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b589e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="b589e-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b589e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b589e-121">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="b589e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="b589e-122">Заголовок</span><span class="sxs-lookup"><span data-stu-id="b589e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b589e-123"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="b589e-123"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b589e-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b589e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b589e-125">Диспетчер сжатия видео</span><span class="sxs-lookup"><span data-stu-id="b589e-125">Video Compression Manager</span></span>](video-compression-manager.md)
</dt> <dt>

[<span data-ttu-id="b589e-126">Сообщения о сжатии видео</span><span class="sxs-lookup"><span data-stu-id="b589e-126">Video Compression Messages</span></span>](video-compression-messages.md)
</dt> </dl>

 

 





