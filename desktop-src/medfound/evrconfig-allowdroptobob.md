---
description: Позволяет расширенному обработчику видео (Евр) повысить производительность, используя для этого Bob-чересстрочную развертку.
ms.assetid: e145e862-b987-4962-a94b-f8370bbcd5ac
title: Атрибут EVRConfig_AllowDropToBob (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3940edd0945999f7300060d963806e3572a5d0fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423534"
---
# <a name="evrconfig_allowdroptobob-attribute"></a><span data-ttu-id="ea1ed-103">Еврконфиг \_ алловдроптобоб, атрибут</span><span class="sxs-lookup"><span data-stu-id="ea1ed-103">EVRConfig\_AllowDropToBob attribute</span></span>

<span data-ttu-id="ea1ed-104">Позволяет расширенному обработчику видео (Евр) повысить производительность, используя для этого Bob-чересстрочную развертку.</span><span class="sxs-lookup"><span data-stu-id="ea1ed-104">Allows the Enhanced Video Renderer (EVR) to improve performance by using bob deinterlacing.</span></span>

## <a name="data-type"></a><span data-ttu-id="ea1ed-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ea1ed-105">Data type</span></span>

<span data-ttu-id="ea1ed-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="ea1ed-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="ea1ed-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="ea1ed-107">Get/set</span></span>

<span data-ttu-id="ea1ed-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="ea1ed-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="ea1ed-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="ea1ed-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="ea1ed-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ea1ed-110">Remarks</span></span>

<span data-ttu-id="ea1ed-111">Этот атрибут можно задать в приемнике Еврмедиа.</span><span class="sxs-lookup"><span data-stu-id="ea1ed-111">This attribute can be set on the EVRmedia sink.</span></span> <span data-ttu-id="ea1ed-112">Чтобы задать атрибут, **QueryInterface** будет запрашивать приемник мультимедиа Евр для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="ea1ed-112">To set the attribute, **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="ea1ed-113">Установка этого атрибута оказывает тот же результат, что и установка флага **мфвидеомикспрефс \_ АЛЛОВДРОПТОБОБ** в Евр.</span><span class="sxs-lookup"><span data-stu-id="ea1ed-113">Setting this attribute has the same effect as setting the **MFVideoMixPrefs\_AllowDropToBob** flag on the EVR.</span></span> <span data-ttu-id="ea1ed-114">Описание этого флага см. в разделе [**мфвидеомикспрефс**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) .</span><span class="sxs-lookup"><span data-stu-id="ea1ed-114">See [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) for a description of this flag.</span></span>

<span data-ttu-id="ea1ed-115">Константа GUID для этого атрибута экспортируется из стрмиидс. lib.</span><span class="sxs-lookup"><span data-stu-id="ea1ed-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea1ed-116">Требования</span><span class="sxs-lookup"><span data-stu-id="ea1ed-116">Requirements</span></span>



| <span data-ttu-id="ea1ed-117">Требование</span><span class="sxs-lookup"><span data-stu-id="ea1ed-117">Requirement</span></span> | <span data-ttu-id="ea1ed-118">Значение</span><span class="sxs-lookup"><span data-stu-id="ea1ed-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ea1ed-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ea1ed-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ea1ed-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="ea1ed-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="ea1ed-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ea1ed-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ea1ed-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="ea1ed-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="ea1ed-123">Header</span><span class="sxs-lookup"><span data-stu-id="ea1ed-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea1ed-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="ea1ed-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea1ed-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ea1ed-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea1ed-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ea1ed-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ea1ed-127">Атрибуты Евр</span><span class="sxs-lookup"><span data-stu-id="ea1ed-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ea1ed-128">Управление качеством видео</span><span class="sxs-lookup"><span data-stu-id="ea1ed-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




