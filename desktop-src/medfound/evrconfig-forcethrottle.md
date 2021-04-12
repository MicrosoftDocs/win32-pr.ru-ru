---
description: Заставляет Расширенный модуль обработки видео (Евр) ограничивать выходные данные в соответствии с пропускной способностью GPU.
ms.assetid: e81e67d6-aa72-44c1-90e9-72ab18bca1c9
title: Атрибут EVRConfig_ForceThrottle (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f39cef0bd032eeaf84129e74274b59dbafadbc47
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104342482"
---
# <a name="evrconfig_forcethrottle-attribute"></a><span data-ttu-id="76970-103">Еврконфиг \_ форцесроттле, атрибут</span><span class="sxs-lookup"><span data-stu-id="76970-103">EVRConfig\_ForceThrottle attribute</span></span>

<span data-ttu-id="76970-104">Заставляет Расширенный модуль обработки видео (Евр) ограничивать выходные данные в соответствии с пропускной способностью GPU.</span><span class="sxs-lookup"><span data-stu-id="76970-104">Forces the Enhanced Video Renderer (EVR) to limit its output to match GPU bandwidth.</span></span>

## <a name="data-type"></a><span data-ttu-id="76970-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="76970-105">Data type</span></span>

<span data-ttu-id="76970-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="76970-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="76970-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="76970-107">Get/set</span></span>

<span data-ttu-id="76970-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="76970-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="76970-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="76970-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="76970-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="76970-110">Remarks</span></span>

<span data-ttu-id="76970-111">Этот атрибут можно задать в приемнике носителей Евр.</span><span class="sxs-lookup"><span data-stu-id="76970-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="76970-112">Чтобы задать атрибут, используйте **IUnknown:: QueryInterface** , чтобы запросить приемник мультимедиа Евр для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="76970-112">To set the attribute, use **IUnknown::QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="76970-113">Установка этого атрибута оказывает тот же результат, что и установка флага **мфвидеорендерпрефс \_ ФОРЦЕАУТПУТСРОТТЛИНГ** в Евр.</span><span class="sxs-lookup"><span data-stu-id="76970-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_ForceOutputThrottling** flag on the EVR.</span></span> <span data-ttu-id="76970-114">Описание этого флага см. в разделе [**мфвидеорендерпрефс**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .</span><span class="sxs-lookup"><span data-stu-id="76970-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="76970-115">Константа GUID для этого атрибута экспортируется из стрмиидс. lib.</span><span class="sxs-lookup"><span data-stu-id="76970-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="76970-116">Требования</span><span class="sxs-lookup"><span data-stu-id="76970-116">Requirements</span></span>



| <span data-ttu-id="76970-117">Требование</span><span class="sxs-lookup"><span data-stu-id="76970-117">Requirement</span></span> | <span data-ttu-id="76970-118">Значение</span><span class="sxs-lookup"><span data-stu-id="76970-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="76970-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="76970-119">Minimum supported client</span></span><br/> | <span data-ttu-id="76970-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="76970-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="76970-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="76970-121">Minimum supported server</span></span><br/> | <span data-ttu-id="76970-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="76970-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="76970-123">Header</span><span class="sxs-lookup"><span data-stu-id="76970-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="76970-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="76970-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="76970-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="76970-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76970-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="76970-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="76970-127">Атрибуты Евр</span><span class="sxs-lookup"><span data-stu-id="76970-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="76970-128">Управление качеством видео</span><span class="sxs-lookup"><span data-stu-id="76970-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




