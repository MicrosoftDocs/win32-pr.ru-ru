---
description: Аллловс Расширенный модуль подготовки видео (Евр) для смешивания видео в прямоугольнике, который меньше, чем прямоугольник вывода, а затем масштабирует результат.
ms.assetid: 7e3b8fe1-959b-4391-a715-5d5a7a7dda39
title: Атрибут EVRConfig_AllowScaling (UUIDs. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef1d0662c7145d9f5c5484df81c2483305402850
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896565"
---
# <a name="evrconfig_allowscaling-attribute"></a><span data-ttu-id="66dbf-103">Еврконфиг \_ алловскалинг, атрибут</span><span class="sxs-lookup"><span data-stu-id="66dbf-103">EVRConfig\_AllowScaling attribute</span></span>

<span data-ttu-id="66dbf-104">Аллловс Расширенный модуль подготовки видео (Евр) для смешивания видео в прямоугольнике, который меньше, чем прямоугольник вывода, а затем масштабирует результат.</span><span class="sxs-lookup"><span data-stu-id="66dbf-104">Alllows the Enhanced Video Renderer (EVR) to mix the video within a rectangle that is smaller than the output rectangle, and then scale the result.</span></span>

## <a name="data-type"></a><span data-ttu-id="66dbf-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="66dbf-105">Data type</span></span>

<span data-ttu-id="66dbf-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="66dbf-106">**UINT32**</span></span>

## <a name="getset"></a><span data-ttu-id="66dbf-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="66dbf-107">Get/set</span></span>

<span data-ttu-id="66dbf-108">Чтобы получить этот атрибут, вызовите метод [**имфаттрибутес:: UInt32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="66dbf-108">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="66dbf-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="66dbf-109">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="66dbf-110">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66dbf-110">Remarks</span></span>

<span data-ttu-id="66dbf-111">Этот атрибут можно задать в приемнике носителей Евр.</span><span class="sxs-lookup"><span data-stu-id="66dbf-111">This attribute can be set on the EVR media sink.</span></span> <span data-ttu-id="66dbf-112">Чтобы задать атрибут, используйте **QueryInterface** , чтобы запросить приемник мультимедиа Евр для интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) .</span><span class="sxs-lookup"><span data-stu-id="66dbf-112">To set the attribute, use **QueryInterface** to query the EVR media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span>

<span data-ttu-id="66dbf-113">Установка этого атрибута оказывает тот же результат, что и установка флага **мфвидеорендерпрефс \_ АЛЛОВСКАЛИНГ** в Евр.</span><span class="sxs-lookup"><span data-stu-id="66dbf-113">Setting this attribute has the same effect as setting the **MFVideoRenderPrefs\_AllowScaling** flag on the EVR.</span></span> <span data-ttu-id="66dbf-114">Описание этого флага см. в разделе [**мфвидеорендерпрефс**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) .</span><span class="sxs-lookup"><span data-stu-id="66dbf-114">See [**MFVideoRenderPrefs**](/windows/desktop/api/evr/ne-evr-mfvideorenderprefs) for a description of this flag.</span></span>

<span data-ttu-id="66dbf-115">Константа GUID для этого атрибута экспортируется из стрмиидс. lib.</span><span class="sxs-lookup"><span data-stu-id="66dbf-115">The GUID constant for this attribute is exported from strmiids.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="66dbf-116">Требования</span><span class="sxs-lookup"><span data-stu-id="66dbf-116">Requirements</span></span>



| <span data-ttu-id="66dbf-117">Требование</span><span class="sxs-lookup"><span data-stu-id="66dbf-117">Requirement</span></span> | <span data-ttu-id="66dbf-118">Значение</span><span class="sxs-lookup"><span data-stu-id="66dbf-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66dbf-119">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66dbf-119">Minimum supported client</span></span><br/> | <span data-ttu-id="66dbf-120">\[Только классические приложения Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="66dbf-120">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="66dbf-121">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66dbf-121">Minimum supported server</span></span><br/> | <span data-ttu-id="66dbf-122">Только классические приложения Windows Server 2008 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="66dbf-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="66dbf-123">Header</span><span class="sxs-lookup"><span data-stu-id="66dbf-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="66dbf-124"><dt>UUID. h</dt></span><span class="sxs-lookup"><span data-stu-id="66dbf-124"><dt>Uuids.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66dbf-125">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66dbf-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66dbf-126">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66dbf-126">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="66dbf-127">Атрибуты Евр</span><span class="sxs-lookup"><span data-stu-id="66dbf-127">EVR Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="66dbf-128">Управление качеством видео</span><span class="sxs-lookup"><span data-stu-id="66dbf-128">Video Quality Management</span></span>](video-quality-management.md)
</dt> </dl>

 

 




