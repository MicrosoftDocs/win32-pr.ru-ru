---
description: Заставляет Расширенный модуль подготовки видео (Евр) пропускать второе поле каждого кадра с чередованием.
ms.assetid: b79d9230-b127-4e9b-b73b-685ce27aefa9
title: Атрибут EVRConfig_ForceHalfInterlace (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfeab4bcb3d05e615962fb8acc5f304ba3ea7e6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105701315"
---
# <a name="evrconfig_forcehalfinterlace-attribute"></a><span data-ttu-id="94d3d-103">Еврконфиг \_ форцехалфинтерлаце, атрибут</span><span class="sxs-lookup"><span data-stu-id="94d3d-103">EVRConfig\_ForceHalfInterlace attribute</span></span>

<span data-ttu-id="94d3d-104">Заставляет Расширенный модуль подготовки видео (Евр) пропускать второе поле каждого кадра с чередованием.</span><span class="sxs-lookup"><span data-stu-id="94d3d-104">Forces the Enhanced Video Renderer (EVR) to skip the second field of every interlaced frame.</span></span>

## <a name="data-type"></a><span data-ttu-id="94d3d-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="94d3d-105">Data type</span></span>

<span data-ttu-id="94d3d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="94d3d-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="94d3d-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="94d3d-107">Get/set</span></span>

<span data-ttu-id="94d3d-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="94d3d-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="94d3d-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="94d3d-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="94d3d-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="94d3d-110">Remarks</span></span>

<span data-ttu-id="94d3d-111">Этот атрибут можно задать в приемнике носителей Евр.</span><span class="sxs-lookup"><span data-stu-id="94d3d-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="94d3d-112">Чтобы задать атрибут, используйте **QueryInterface** , чтобы запросить приемник мультимедиа Евр для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="94d3d-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="94d3d-113">Установка этого атрибута оказывает тот же результат, что и установка флага **мфвидеомикспрефс \_ ФОРЦЕХАЛФИНТЕРЛАЦЕ** в Евр.</span><span class="sxs-lookup"><span data-stu-id="94d3d-113">Setting this attribute has the same effect as setting the **MFVideoMixPrefs\_ForceHalfInterlace** flag on the EVR.</span></span> <span data-ttu-id="94d3d-114">Описание этого флага см. в разделе [**мфвидеомикспрефс**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) .</span><span class="sxs-lookup"><span data-stu-id="94d3d-114">See [**MFVideoMixPrefs**](/windows/desktop/api/evr/ne-evr-mfvideomixprefs) for a description of this flag.</span></span>

<span data-ttu-id="94d3d-115">Константа GUID для этого атрибута экспортируется из стрмиидс. lib.</span><span class="sxs-lookup"><span data-stu-id="94d3d-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="94d3d-116">Требования</span><span class="sxs-lookup"><span data-stu-id="94d3d-116">Requirements</span></span>



| <span data-ttu-id="94d3d-117">Требование</span><span class="sxs-lookup"><span data-stu-id="94d3d-117">Requirement</span></span> | <span data-ttu-id="94d3d-118">Значение</span><span class="sxs-lookup"><span data-stu-id="94d3d-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="94d3d-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="94d3d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="94d3d-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="94d3d-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="94d3d-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="94d3d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="94d3d-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="94d3d-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="94d3d-123">Header</span><span class="sxs-lookup"><span data-stu-id="94d3d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="94d3d-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="94d3d-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94d3d-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="94d3d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94d3d-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="94d3d-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="94d3d-127">Атрибуты Евр</span><span class="sxs-lookup"><span data-stu-id="94d3d-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="94d3d-128">Управление качеством видео</span><span class="sxs-lookup"><span data-stu-id="94d3d-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




