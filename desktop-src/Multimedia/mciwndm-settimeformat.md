---
title: Сообщение MCIWNDM_SETTIMEFORMAT (VFW. h)
description: Сообщение МЦИВНДМ \_ сеттимеформат задает формат времени для устройства MCI. Это сообщение можно отправить явно или с помощью макроса МЦивндсеттимеформат.
ms.assetid: 7de82094-6d35-44fd-88e7-ebd18a558cfd
keywords:
- MCIWNDM_SETTIMEFORMAT сообщения Windows мультимедиа
topic_type:
- apiref
api_name:
- MCIWNDM_SETTIMEFORMAT
api_location:
- Vfw.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcec1f0db5accad93211bf1eb6f1c9297e2b9f33
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533800"
---
# <a name="mciwndm_settimeformat-message"></a><span data-ttu-id="3f49b-105">\_Сообщение мЦивндм сеттимеформат</span><span class="sxs-lookup"><span data-stu-id="3f49b-105">MCIWNDM\_SETTIMEFORMAT message</span></span>

<span data-ttu-id="3f49b-106">Сообщение **мЦивндм \_ сеттимеформат** задает формат времени для устройства MCI.</span><span class="sxs-lookup"><span data-stu-id="3f49b-106">The **MCIWNDM\_SETTIMEFORMAT** message sets the time format of an MCI device.</span></span> <span data-ttu-id="3f49b-107">Это сообщение можно отправить явно или с помощью макроса [**мЦивндсеттимеформат**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="3f49b-107">You can send this message explicitly or by using the [**MCIWndSetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat) macro.</span></span>


```C++
MCIWNDM_SETTIMEFORMAT 
wParam = 0; 
lParam = (LPARAM) (LPSTR) lp; 
```



## <a name="parameters"></a><span data-ttu-id="3f49b-108">Параметры</span><span class="sxs-lookup"><span data-stu-id="3f49b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3f49b-109"><span id="lp"></span><span id="LP"></span>*LP*</span><span class="sxs-lookup"><span data-stu-id="3f49b-109"><span id="lp"></span><span id="LP"></span>*lp*</span></span>
</dt> <dd>

<span data-ttu-id="3f49b-110">Указатель на буфер, содержащий строку, завершающуюся нулем, указывающую формат времени.</span><span class="sxs-lookup"><span data-stu-id="3f49b-110">Pointer to a buffer containing the null-terminated string indicating the time format.</span></span> <span data-ttu-id="3f49b-111">Укажите "кадры", чтобы задать формат времени "кадры", или "MS", чтобы задать формат времени равным миллисекундам.</span><span class="sxs-lookup"><span data-stu-id="3f49b-111">Specify "frames" to set the time format to frames, or "ms" to set the time format to milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3f49b-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="3f49b-112">Return Value</span></span>

<span data-ttu-id="3f49b-113">Возвращает нуль в случае успеха или ошибку в противном случае.</span><span class="sxs-lookup"><span data-stu-id="3f49b-113">Returns zero if successful or an error otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="3f49b-114">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3f49b-114">Remarks</span></span>

<span data-ttu-id="3f49b-115">Приложение может указывать форматы времени, отличные от кадров, или миллисекунды, если форматы поддерживаются устройством MCI.</span><span class="sxs-lookup"><span data-stu-id="3f49b-115">An application can specify time formats other than frames or milliseconds as long as the formats are supported by the MCI device.</span></span> <span data-ttu-id="3f49b-116">Непостоянное форматирование, например дорожные и SMPTE, может привести к нестабильному поведению TrackBar.</span><span class="sxs-lookup"><span data-stu-id="3f49b-116">Noncontinuous formats, such as tracks and SMPTE, can cause the trackbar to behave erratically.</span></span> <span data-ttu-id="3f49b-117">Для этих форматов времени может потребоваться отключить панель инструментов с помощью макроса [**мЦивндчанжестилес**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) и указать \_ стиль окна мЦивндф ноплайбар.</span><span class="sxs-lookup"><span data-stu-id="3f49b-117">For these time formats, you might want to turn off the toolbar by using the [**MCIWndChangeStyles**](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles) macro and specifying the MCIWNDF\_NOPLAYBAR window style.</span></span>

<span data-ttu-id="3f49b-118">Если необходимо задать формат времени для кадров или миллисекунд, можно также использовать макрос [**мЦивндусефрамес**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) или [**мЦивндусетиме**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) .</span><span class="sxs-lookup"><span data-stu-id="3f49b-118">If you want to set the time format to frames or milliseconds, you can also use the [**MCIWndUseFrames**](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes) or [**MCIWndUseTime**](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime) macro.</span></span> <span data-ttu-id="3f49b-119">Список форматов времени см. в разделе макрос [**мЦивнджеттимеформат**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) .</span><span class="sxs-lookup"><span data-stu-id="3f49b-119">For a list of time formats, see the [**MCIWndGetTimeFormat**](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat) macro.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f49b-120">Требования</span><span class="sxs-lookup"><span data-stu-id="3f49b-120">Requirements</span></span>



| <span data-ttu-id="3f49b-121">Требование</span><span class="sxs-lookup"><span data-stu-id="3f49b-121">Requirement</span></span> | <span data-ttu-id="3f49b-122">Значение</span><span class="sxs-lookup"><span data-stu-id="3f49b-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="3f49b-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3f49b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="3f49b-124">Windows 2000 Professional \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3f49b-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                       |
| <span data-ttu-id="3f49b-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3f49b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="3f49b-126">Windows 2000 Server \[только классические приложения\]</span><span class="sxs-lookup"><span data-stu-id="3f49b-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="3f49b-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="3f49b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f49b-128"><dt>VFW. h</dt></span><span class="sxs-lookup"><span data-stu-id="3f49b-128"><dt>Vfw.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f49b-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3f49b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f49b-130">**мЦивндчанжестилес**</span><span class="sxs-lookup"><span data-stu-id="3f49b-130">**MCIWndChangeStyles**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndchangestyles)
</dt> <dt>

[<span data-ttu-id="3f49b-131">**мЦивнджеттимеформат**</span><span class="sxs-lookup"><span data-stu-id="3f49b-131">**MCIWndGetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndgettimeformat)
</dt> <dt>

[<span data-ttu-id="3f49b-132">**мЦивндсеттимеформат**</span><span class="sxs-lookup"><span data-stu-id="3f49b-132">**MCIWndSetTimeFormat**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndsettimeformat)
</dt> <dt>

[<span data-ttu-id="3f49b-133">**мЦивндусефрамес**</span><span class="sxs-lookup"><span data-stu-id="3f49b-133">**MCIWndUseFrames**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwnduseframes)
</dt> <dt>

[<span data-ttu-id="3f49b-134">**мЦивндусетиме**</span><span class="sxs-lookup"><span data-stu-id="3f49b-134">**MCIWndUseTime**</span></span>](/windows/desktop/api/Vfw/nf-vfw-mciwndusetime)
</dt> </dl>

 

 





