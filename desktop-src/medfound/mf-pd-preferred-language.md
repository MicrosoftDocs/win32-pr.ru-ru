---
description: Содержит предпочитаемый язык RFC 1766 для источника мультимедиа.
ms.assetid: 30f99804-6aea-473b-9bbf-e8c715501391
title: Атрибут MF_PD_PREFERRED_LANGUAGE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81bb121c7181724ef06b3e8fe9239342a140104a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272506"
---
# <a name="mf_pd_preferred_language-attribute"></a><span data-ttu-id="617db-103">\_ \_ Атрибут предпочтительного \_ языка MF PD</span><span class="sxs-lookup"><span data-stu-id="617db-103">MF\_PD\_PREFERRED\_LANGUAGE attribute</span></span>

<span data-ttu-id="617db-104">Содержит предпочитаемый язык RFC 1766 для источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="617db-104">Contains the preferred RFC 1766 language of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="617db-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="617db-105">Data type</span></span>

<span data-ttu-id="617db-106">**WCHAR**</span><span class="sxs-lookup"><span data-stu-id="617db-106">**WCHAR**</span></span>

## <a name="getset"></a><span data-ttu-id="617db-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="617db-107">Get/set</span></span>

<span data-ttu-id="617db-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span><span class="sxs-lookup"><span data-stu-id="617db-108">To get this attribute, call [**IMFAttributes::GetString**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring).</span></span>

<span data-ttu-id="617db-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: сеттринг**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span><span class="sxs-lookup"><span data-stu-id="617db-109">To set this attribute, call [**IMFAttributes::Settring**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring).</span></span>

## <a name="applies-to"></a><span data-ttu-id="617db-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="617db-110">Applies to</span></span>

[<span data-ttu-id="617db-111">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="617db-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="617db-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="617db-112">Remarks</span></span>

<span data-ttu-id="617db-113">\_ \_ Атрибут предпочтительного языка MF PD \_ является необязательным.</span><span class="sxs-lookup"><span data-stu-id="617db-113">The MF\_PD\_PREFERRED\_LANGUAGE attribute is optional.</span></span> <span data-ttu-id="617db-114">Приложение может установить этот атрибут в источнике мультимедиа (например, в сетевом источнике), чтобы указать предпочтительный язык.</span><span class="sxs-lookup"><span data-stu-id="617db-114">An application can set this attribute on a media source (such as a network source) to specify its preferred language.</span></span>

<span data-ttu-id="617db-115">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="617db-115">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="617db-116">Требования</span><span class="sxs-lookup"><span data-stu-id="617db-116">Requirements</span></span>



| <span data-ttu-id="617db-117">Требование</span><span class="sxs-lookup"><span data-stu-id="617db-117">Requirement</span></span> | <span data-ttu-id="617db-118">Значение</span><span class="sxs-lookup"><span data-stu-id="617db-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="617db-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="617db-119">Minimum supported client</span></span><br/> | <span data-ttu-id="617db-120">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="617db-120">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="617db-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="617db-121">Minimum supported server</span></span><br/> | <span data-ttu-id="617db-122">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="617db-122">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="617db-123">Header</span><span class="sxs-lookup"><span data-stu-id="617db-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="617db-124"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="617db-124"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="617db-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="617db-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="617db-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="617db-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="617db-127">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="617db-127">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




