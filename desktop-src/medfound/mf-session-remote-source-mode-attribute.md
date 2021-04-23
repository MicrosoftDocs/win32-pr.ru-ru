---
description: Указывает, что источник мультимедиа будет создан в удаленном процессе.
ms.assetid: 3a2f9ff5-1780-40f3-b36b-3a7cccb47d05
title: Атрибут MF_SESSION_REMOTE_SOURCE_MODE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a27b26a71e8bea53ab687eaf6126a1803e71ba16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265504"
---
# <a name="mf_session_remote_source_mode-attribute"></a><span data-ttu-id="3ad3a-103">\_ \_ \_ Атрибут режима удаленного исходного \_ сеанса MF</span><span class="sxs-lookup"><span data-stu-id="3ad3a-103">MF\_SESSION\_REMOTE\_SOURCE\_MODE attribute</span></span>

<span data-ttu-id="3ad3a-104">Указывает, что источник мультимедиа будет создан в удаленном процессе.</span><span class="sxs-lookup"><span data-stu-id="3ad3a-104">Specifies that the media source will be created in a remote process.</span></span>

## <a name="data-type"></a><span data-ttu-id="3ad3a-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3ad3a-105">Data type</span></span>

<span data-ttu-id="3ad3a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3ad3a-106">**UINT32**</span></span>

<span data-ttu-id="3ad3a-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="3ad3a-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ad3a-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3ad3a-108">Remarks</span></span>

<span data-ttu-id="3ad3a-109">Этот атрибут можно задать в сеансе защищенного пути к носителю (PMP) с помощью параметра *пконфигуратион* функции [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="3ad3a-109">You can set this attribute on the protected media path (PMP) session by using the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="3ad3a-110">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="3ad3a-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ad3a-111">Требования</span><span class="sxs-lookup"><span data-stu-id="3ad3a-111">Requirements</span></span>



| <span data-ttu-id="3ad3a-112">Требование</span><span class="sxs-lookup"><span data-stu-id="3ad3a-112">Requirement</span></span> | <span data-ttu-id="3ad3a-113">Значение</span><span class="sxs-lookup"><span data-stu-id="3ad3a-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad3a-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3ad3a-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad3a-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3ad3a-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3ad3a-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3ad3a-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad3a-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3ad3a-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3ad3a-118">Header</span><span class="sxs-lookup"><span data-stu-id="3ad3a-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ad3a-119"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3ad3a-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ad3a-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3ad3a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ad3a-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3ad3a-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ad3a-122">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="3ad3a-122">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3ad3a-123">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3ad3a-123">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3ad3a-124">Атрибуты сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="3ad3a-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="3ad3a-125">Сеанс PMP мультимедиа</span><span class="sxs-lookup"><span data-stu-id="3ad3a-125">PMP Media Session</span></span>](pmp-media-session.md)
</dt> </dl>

 

 




