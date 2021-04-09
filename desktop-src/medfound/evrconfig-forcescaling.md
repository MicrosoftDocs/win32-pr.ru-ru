---
description: Заставляет Расширенный модуль обработки видео (Евр) смешивать видео в прямоугольнике, меньшем, чем прямоугольник вывода, а затем масштабировать результат.
ms.assetid: f85c4114-ac94-4deb-a1cf-896209079f8b
title: Атрибут EVRConfig_ForceScaling (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b82b7e017d414e86b8b4332fe5646e4808d4009
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104072563"
---
# <a name="evrconfig_forcescaling-attribute"></a><span data-ttu-id="7d0a6-103">Еврконфиг \_ форцескалинг, атрибут</span><span class="sxs-lookup"><span data-stu-id="7d0a6-103">EVRConfig\_ForceScaling attribute</span></span>

<span data-ttu-id="7d0a6-104">Заставляет Расширенный модуль обработки видео (Евр) смешивать видео в прямоугольнике, меньшем, чем прямоугольник вывода, а затем масштабировать результат.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-104">Forces the Enhanced Video Renderer (EVR) to mix the video within a rectangle that is smaller than the output rectangle, and then scale the result.</span></span>

## <a name="data-type"></a><span data-ttu-id="7d0a6-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="7d0a6-105">Data type</span></span>

<span data-ttu-id="7d0a6-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="7d0a6-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="7d0a6-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="7d0a6-107">Get/set</span></span>

<span data-ttu-id="7d0a6-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="7d0a6-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="7d0a6-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="7d0a6-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="7d0a6-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="7d0a6-110">Remarks</span></span>

<span data-ttu-id="7d0a6-111">Этот атрибут можно задать в приемнике носителей Евр.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="7d0a6-112">Чтобы задать атрибут, используйте **QueryInterface** , чтобы запросить приемник мультимедиа Евр для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="7d0a6-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="7d0a6-113">Установка этого атрибута оказывает тот же результат, что и установка флага **мфвидеорендерпрефс \_ ФОРЦЕСКАЛИНГ** в Евр.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_ForceScaling** flag on the EVR.</span></span> <span data-ttu-id="7d0a6-114">Описание этого флага см. в разделе [**мфвидеорендерпрефс**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .</span><span class="sxs-lookup"><span data-stu-id="7d0a6-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="7d0a6-115">Константа GUID для этого атрибута экспортируется из стрмиидс. lib.</span><span class="sxs-lookup"><span data-stu-id="7d0a6-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d0a6-116">Требования</span><span class="sxs-lookup"><span data-stu-id="7d0a6-116">Requirements</span></span>



| <span data-ttu-id="7d0a6-117">Требование</span><span class="sxs-lookup"><span data-stu-id="7d0a6-117">Requirement</span></span> | <span data-ttu-id="7d0a6-118">Значение</span><span class="sxs-lookup"><span data-stu-id="7d0a6-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7d0a6-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="7d0a6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7d0a6-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7d0a6-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="7d0a6-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="7d0a6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7d0a6-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="7d0a6-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="7d0a6-123">Header</span><span class="sxs-lookup"><span data-stu-id="7d0a6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="7d0a6-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="7d0a6-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d0a6-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="7d0a6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d0a6-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7d0a6-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="7d0a6-127">Атрибуты Евр</span><span class="sxs-lookup"><span data-stu-id="7d0a6-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="7d0a6-128">Управление качеством видео</span><span class="sxs-lookup"><span data-stu-id="7d0a6-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




