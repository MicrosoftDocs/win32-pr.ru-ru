---
description: Обработчик для окна обрезки видео.
ms.assetid: 883bc7cf-f52f-4cb5-a942-b42b429b17a9
title: Атрибут MF_ACTIVATE_VIDEO_WINDOW (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a23253c0cd1e4ae90659838acbb58056f770419
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105674014"
---
# <a name="mf_activate_video_window-attribute"></a><span data-ttu-id="59701-103">\_Порт MF \_ активировать \_ атрибут окна видео</span><span class="sxs-lookup"><span data-stu-id="59701-103">MF\_ACTIVATE\_VIDEO\_WINDOW attribute</span></span>

<span data-ttu-id="59701-104">Обработчик для окна обрезки видео.</span><span class="sxs-lookup"><span data-stu-id="59701-104">Handle to the video clipping window.</span></span>

## <a name="data-type"></a><span data-ttu-id="59701-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="59701-105">Data type</span></span>

<span data-ttu-id="59701-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="59701-106">**UINT64**</span></span>

<span data-ttu-id="59701-107">Рассматривать как **DWORD \_ ptr** (**HWND**).</span><span class="sxs-lookup"><span data-stu-id="59701-107">Treat as **DWORD\_PTR** (**HWND**).</span></span>

## <a name="remarks"></a><span data-ttu-id="59701-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="59701-108">Remarks</span></span>

<span data-ttu-id="59701-109">Этот атрибут применяется к объекту активации расширенного обработчика видео (Евр).</span><span class="sxs-lookup"><span data-stu-id="59701-109">This attribute applies to the activation object for the enhanced video renderer (EVR).</span></span> <span data-ttu-id="59701-110">Значение задается автоматически при вызове [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) для создания объекта активации Евр.</span><span class="sxs-lookup"><span data-stu-id="59701-110">The value is set automatically when you call [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) to create the EVR activation object.</span></span>

<span data-ttu-id="59701-111">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="59701-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="59701-112">Требования</span><span class="sxs-lookup"><span data-stu-id="59701-112">Requirements</span></span>



| <span data-ttu-id="59701-113">Требование</span><span class="sxs-lookup"><span data-stu-id="59701-113">Requirement</span></span> | <span data-ttu-id="59701-114">Значение</span><span class="sxs-lookup"><span data-stu-id="59701-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59701-115">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="59701-115">Minimum supported client</span></span><br/> | <span data-ttu-id="59701-116">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="59701-116">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="59701-117">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="59701-117">Minimum supported server</span></span><br/> | <span data-ttu-id="59701-118">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="59701-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="59701-119">Header</span><span class="sxs-lookup"><span data-stu-id="59701-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="59701-120"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="59701-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59701-121">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="59701-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59701-122">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="59701-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="59701-123">Расширенные атрибуты модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="59701-123">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="59701-124">**Имфаттрибутес:: UINT64**</span><span class="sxs-lookup"><span data-stu-id="59701-124">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="59701-125">**Имфаттрибутес:: SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="59701-125">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> <dt>

[<span data-ttu-id="59701-126">Объекты активации</span><span class="sxs-lookup"><span data-stu-id="59701-126">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




