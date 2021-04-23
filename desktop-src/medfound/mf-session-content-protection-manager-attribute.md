---
description: Предоставляет интерфейс обратного вызова, который приложение получает объект средства включения содержимого из сеанса защищенного пути к носителю (PMP).
ms.assetid: 66482541-63d4-439b-862f-7507605af5d8
title: Атрибут MF_SESSION_CONTENT_PROTECTION_MANAGER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c90321ae3c10fd7fa2ec39a4fb478e256291b049
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712397"
---
# <a name="mf_session_content_protection_manager-attribute"></a><span data-ttu-id="d6bf6-103">\_ \_ \_ Атрибут диспетчера защиты содержимого сеанса MF \_</span><span class="sxs-lookup"><span data-stu-id="d6bf6-103">MF\_SESSION\_CONTENT\_PROTECTION\_MANAGER attribute</span></span>

<span data-ttu-id="d6bf6-104">Предоставляет интерфейс обратного вызова, который приложение получает объект средства включения содержимого из сеанса защищенного пути к носителю (PMP).</span><span class="sxs-lookup"><span data-stu-id="d6bf6-104">Provides a callback interface for the application to receive a content enabler object from the protected media path (PMP) session.</span></span>

## <a name="data-type"></a><span data-ttu-id="d6bf6-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d6bf6-105">Data type</span></span>

<span data-ttu-id="d6bf6-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="d6bf6-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="d6bf6-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d6bf6-107">Remarks</span></span>

<span data-ttu-id="d6bf6-108">Значение этого атрибута является указателем на интерфейс [_ *имфконтентпротектионманажер* \*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) приложения.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-108">The value of this attribute is a pointer to the application's [_ *IMFContentProtectionManager*\*](/windows/desktop/api/mfidl/nn-mfidl-imfcontentprotectionmanager) interface.</span></span>

<span data-ttu-id="d6bf6-109">Установите этот атрибут в сеансе PMP с помощью параметра *пконфигуратион* функции [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="d6bf6-109">Set this attribute on the PMP session by using the *pConfiguration* parameter of the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="d6bf6-110">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="d6bf6-110">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6bf6-111">Требования</span><span class="sxs-lookup"><span data-stu-id="d6bf6-111">Requirements</span></span>



| <span data-ttu-id="d6bf6-112">Требование</span><span class="sxs-lookup"><span data-stu-id="d6bf6-112">Requirement</span></span> | <span data-ttu-id="d6bf6-113">Значение</span><span class="sxs-lookup"><span data-stu-id="d6bf6-113">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d6bf6-114">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d6bf6-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d6bf6-115">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d6bf6-115">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d6bf6-116">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d6bf6-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d6bf6-117">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d6bf6-117">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d6bf6-118">Header</span><span class="sxs-lookup"><span data-stu-id="d6bf6-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d6bf6-119"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d6bf6-119"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6bf6-120">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d6bf6-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6bf6-121">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d6bf6-121">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d6bf6-122">**Имфаттрибутес:: неизвестный**</span><span class="sxs-lookup"><span data-stu-id="d6bf6-122">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="d6bf6-123">**Имфаттрибутес:: Сетункновн**</span><span class="sxs-lookup"><span data-stu-id="d6bf6-123">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="d6bf6-124">Атрибуты сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d6bf6-124">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="d6bf6-125">Воспроизведение защищенных файлов мультимедиа</span><span class="sxs-lookup"><span data-stu-id="d6bf6-125">How to Play Protected Media Files</span></span>](how-to-play-protected-media-files.md)
</dt> </dl>

 

 




