---
description: Позволяет двум экземплярам сеанса мультимедиа совместно использовать один и тот же процесс защищенного пути к файлам мультимедиа (PMP).
ms.assetid: a922c79b-d6c1-447d-b6fa-993970169a3f
title: Атрибут MF_SESSION_SERVER_CONTEXT (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b1ce68d1dcd4318f68c4547845e6ce12d2f3aaca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156803"
---
# <a name="mf_session_server_context-attribute"></a><span data-ttu-id="3122d-103">\_ \_ Атрибут контекста сервера сеанса MF \_</span><span class="sxs-lookup"><span data-stu-id="3122d-103">MF\_SESSION\_SERVER\_CONTEXT attribute</span></span>

<span data-ttu-id="3122d-104">Позволяет двум экземплярам сеанса мультимедиа совместно использовать один и тот же процесс защищенного пути к файлам мультимедиа (PMP).</span><span class="sxs-lookup"><span data-stu-id="3122d-104">Enables two instances of the Media Session to share the same Protected Media Path (PMP) process.</span></span>

## <a name="data-type"></a><span data-ttu-id="3122d-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3122d-105">Data type</span></span>

<span data-ttu-id="3122d-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="3122d-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="3122d-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3122d-107">Remarks</span></span>

<span data-ttu-id="3122d-108">Используйте этот атрибут, если вы хотите создать сеанс мультимедиа PMP в существующем процессе PMP.</span><span class="sxs-lookup"><span data-stu-id="3122d-108">Use this attribute if you want to create the PMP Media Session in an existing PMP process.</span></span> <span data-ttu-id="3122d-109">Значение атрибута является указателем на интерфейс [_ *имфпмпсервер* \*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) .</span><span class="sxs-lookup"><span data-stu-id="3122d-109">The value of the attribute is a pointer to the [_ *IMFPMPServer*\*](/windows/desktop/api/mfidl/nn-mfidl-imfpmpserver) interface.</span></span>

<span data-ttu-id="3122d-110">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="3122d-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3122d-111">Требования</span><span class="sxs-lookup"><span data-stu-id="3122d-111">Requirements</span></span>



| <span data-ttu-id="3122d-112">Требование</span><span class="sxs-lookup"><span data-stu-id="3122d-112">Requirement</span></span> | <span data-ttu-id="3122d-113">Значение</span><span class="sxs-lookup"><span data-stu-id="3122d-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3122d-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3122d-114">Minimum supported client</span></span><br/> | <span data-ttu-id="3122d-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3122d-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3122d-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3122d-116">Minimum supported server</span></span><br/> | <span data-ttu-id="3122d-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3122d-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3122d-118">Header</span><span class="sxs-lookup"><span data-stu-id="3122d-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="3122d-119"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3122d-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3122d-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3122d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3122d-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3122d-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3122d-122">**Имфаттрибутес:: неизвестный**</span><span class="sxs-lookup"><span data-stu-id="3122d-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="3122d-123">**Имфаттрибутес:: Сетункновн**</span><span class="sxs-lookup"><span data-stu-id="3122d-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="3122d-124">Атрибуты сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="3122d-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




