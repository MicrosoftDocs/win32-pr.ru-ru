---
description: Содержит идентификатор CLSID диспетчера качества для сеанса мультимедиа.
ms.assetid: 24b4a5e3-84f1-44d0-a8ac-75c127ec8a8a
title: Атрибут MF_SESSION_QUALITY_MANAGER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 736f37a46c3aeb4216243f058ea7fb8a33bdbd1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346655"
---
# <a name="mf_session_quality_manager-attribute"></a><span data-ttu-id="79224-103">\_ \_ Атрибут диспетчера качества сеанса MF \_</span><span class="sxs-lookup"><span data-stu-id="79224-103">MF\_SESSION\_QUALITY\_MANAGER attribute</span></span>

<span data-ttu-id="79224-104">Содержит идентификатор CLSID диспетчера качества для сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="79224-104">Contains the CLSID of a quality manager for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="79224-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="79224-105">Data type</span></span>

<span data-ttu-id="79224-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="79224-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="79224-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="79224-107">Remarks</span></span>

<span data-ttu-id="79224-108">Этот атрибут можно использовать для предоставления пользовательского диспетчера качества для сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="79224-108">You can use this attribute to provide a custom quality manager for the Media Session.</span></span>

<span data-ttu-id="79224-109">Задайте этот атрибут с помощью параметра *пконфигуратион* функции [**мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) или [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="79224-109">Set this attribute by using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) or [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="79224-110">Если этот атрибут задан, сеанс мультимедиа вызывает **CoCreateInstance** с указанным идентификатором CLSID для создания диспетчера качества.</span><span class="sxs-lookup"><span data-stu-id="79224-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID to create the quality manager.</span></span> <span data-ttu-id="79224-111">Объект, созданный этим CLSID, должен предоставлять интерфейс [**имфкуалитиманажер**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) .</span><span class="sxs-lookup"><span data-stu-id="79224-111">The object created by this CLSID must expose the [**IMFQualityManager**](/windows/desktop/api/mfidl/nn-mfidl-imfqualitymanager) interface.</span></span>

<span data-ttu-id="79224-112">Если этот атрибут не задан, сеанс мультимедиа создает диспетчер качества по умолчанию, предоставленный в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="79224-112">If this attribute is not set, the Media Session creates the default quality manager provided in Media Foundation.</span></span>

<span data-ttu-id="79224-113">Если вы хотите запустить сеанс мультимедиа без диспетчера качества, присвойте этому атрибуту **\_ значение GUID NULL**.</span><span class="sxs-lookup"><span data-stu-id="79224-113">If you want to run the Media Session with no quality manager at all, set this attribute to **GUID\_NULL**.</span></span>

<span data-ttu-id="79224-114">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="79224-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="79224-115">Требования</span><span class="sxs-lookup"><span data-stu-id="79224-115">Requirements</span></span>



| <span data-ttu-id="79224-116">Требование</span><span class="sxs-lookup"><span data-stu-id="79224-116">Requirement</span></span> | <span data-ttu-id="79224-117">Значение</span><span class="sxs-lookup"><span data-stu-id="79224-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="79224-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="79224-118">Minimum supported client</span></span><br/> | <span data-ttu-id="79224-119">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="79224-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="79224-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="79224-120">Minimum supported server</span></span><br/> | <span data-ttu-id="79224-121">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="79224-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="79224-122">Header</span><span class="sxs-lookup"><span data-stu-id="79224-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="79224-123"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="79224-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="79224-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="79224-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79224-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="79224-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="79224-126">**Имфаттрибутес:: a GUID**</span><span class="sxs-lookup"><span data-stu-id="79224-126">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="79224-127">**Имфаттрибутес:: Сетгуид**</span><span class="sxs-lookup"><span data-stu-id="79224-127">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="79224-128">Атрибуты сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="79224-128">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> </dl>

 

 




