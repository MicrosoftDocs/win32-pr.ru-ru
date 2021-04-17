---
description: Содержит идентификатор CLSID для загрузчика топологии для сеанса мультимедиа.
ms.assetid: 672274fb-71fc-49ca-bab6-1fc4de21d17c
title: Атрибут MF_SESSION_TOPOLOADER (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6eb5299e058862ad2d26b1fb9debe0028aba4703
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712859"
---
# <a name="mf_session_topoloader-attribute"></a><span data-ttu-id="ccbad-103">\_ \_ Атрибут ТОПОЛОАДЕР сеанса MF</span><span class="sxs-lookup"><span data-stu-id="ccbad-103">MF\_SESSION\_TOPOLOADER attribute</span></span>

<span data-ttu-id="ccbad-104">Содержит идентификатор CLSID для загрузчика топологии для сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ccbad-104">Contains the CLSID of a topology loader for the Media Session.</span></span>

## <a name="data-type"></a><span data-ttu-id="ccbad-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ccbad-105">Data type</span></span>

<span data-ttu-id="ccbad-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="ccbad-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="ccbad-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ccbad-107">Remarks</span></span>

<span data-ttu-id="ccbad-108">Этот атрибут можно использовать для предоставления пользовательского загрузчика топологии для сеанса мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="ccbad-108">You can use this attribute to provide a custom topology loader for the Media Session.</span></span>

<span data-ttu-id="ccbad-109">Задайте этот атрибут с помощью параметра *пконфигуратион* функции [**Мфкреатемедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) или функции [**мфкреатепмпмедиасессион**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) .</span><span class="sxs-lookup"><span data-stu-id="ccbad-109">Set this attribute using the *pConfiguration* parameter of the [**MFCreateMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatemediasession) function or the [**MFCreatePMPMediaSession**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatepmpmediasession) function.</span></span>

<span data-ttu-id="ccbad-110">Если этот атрибут задан, сеанс мультимедиа вызывает **CoCreateInstance** с указанным идентификатором CLSID при создании загрузчика топологии.</span><span class="sxs-lookup"><span data-stu-id="ccbad-110">If this attribute is set, the Media Session calls **CoCreateInstance** with the specified CLSID when it creates the topology loader.</span></span> <span data-ttu-id="ccbad-111">Объект, созданный этим CLSID, должен предоставлять интерфейс [**имфтополоадер**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) .</span><span class="sxs-lookup"><span data-stu-id="ccbad-111">The object created by this CLSID must expose the [**IMFTopoLoader**](/windows/desktop/api/mfidl/nn-mfidl-imftopoloader) interface.</span></span>

<span data-ttu-id="ccbad-112">Если этот атрибут не задан, сеанс мультимедиа создает загрузчик топологии по умолчанию, предоставленный в Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="ccbad-112">If this attribute is not set, the Media Session creates the default topology loader provided in Media Foundation.</span></span>

<span data-ttu-id="ccbad-113">Загрузчик топологии должен поддерживать многопоточные подразделения.</span><span class="sxs-lookup"><span data-stu-id="ccbad-113">A topology loader must support multithreaded apartments.</span></span> <span data-ttu-id="ccbad-114">Необходимо зарегистрировать загрузчик топологии как ThreadingModel = "both".</span><span class="sxs-lookup"><span data-stu-id="ccbad-114">You should register the topology loader as ThreadingModel="Both".</span></span> <span data-ttu-id="ccbad-115">Кроме того, при использовании загрузчика топологии внутри защищенного пути к носителю (PMP) загрузчик топологии должен быть доверенным компонентом.</span><span class="sxs-lookup"><span data-stu-id="ccbad-115">Also, if you are using the topology loader inside the protected media path (PMP), the topology loader must be a trusted component.</span></span> <span data-ttu-id="ccbad-116">Дополнительные сведения см. в разделе [путь к защищенному носителю](protected-media-path.md).</span><span class="sxs-lookup"><span data-stu-id="ccbad-116">For more information, see [Protected Media Path](protected-media-path.md).</span></span>

<span data-ttu-id="ccbad-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="ccbad-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ccbad-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ccbad-118">Requirements</span></span>



| <span data-ttu-id="ccbad-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ccbad-119">Requirement</span></span> | <span data-ttu-id="ccbad-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ccbad-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ccbad-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ccbad-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ccbad-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ccbad-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ccbad-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ccbad-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ccbad-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ccbad-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ccbad-125">Header</span><span class="sxs-lookup"><span data-stu-id="ccbad-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ccbad-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ccbad-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ccbad-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ccbad-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ccbad-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ccbad-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ccbad-129">**Имфаттрибутес:: a GUID**</span><span class="sxs-lookup"><span data-stu-id="ccbad-129">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="ccbad-130">**Имфаттрибутес:: Сетгуид**</span><span class="sxs-lookup"><span data-stu-id="ccbad-130">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="ccbad-131">Атрибуты сеанса мультимедиа</span><span class="sxs-lookup"><span data-stu-id="ccbad-131">Media Session Attributes</span></span>](media-session-attributes.md)
</dt> <dt>

[<span data-ttu-id="ccbad-132">Пользовательские загрузчики топологии</span><span class="sxs-lookup"><span data-stu-id="ccbad-132">Custom Topology Loaders</span></span>](custom-topology-loaders.md)
</dt> </dl>

 

 




