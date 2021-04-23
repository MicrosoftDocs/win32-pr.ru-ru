---
description: Идентификатор CLSID пользовательского видеомикшера для приемника расширенного модуля подготовки видео (Евр).
ms.assetid: a3586e6f-a2a2-4932-8b43-a076f64c5958
title: Атрибут MF_ACTIVATE_CUSTOM_VIDEO_MIXER_CLSID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0cc1049fb3bc77b65fb48fe9a4c10a059b2a4651
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343945"
---
# <a name="mf_activate_custom_video_mixer_clsid-attribute"></a><span data-ttu-id="ba911-103">MF \_ активировать \_ Пользовательский \_ \_ атрибут CLSID микшера видео \_</span><span class="sxs-lookup"><span data-stu-id="ba911-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID attribute</span></span>

<span data-ttu-id="ba911-104">Идентификатор CLSID пользовательского видеомикшера для приемника расширенного модуля подготовки видео (Евр).</span><span class="sxs-lookup"><span data-stu-id="ba911-104">CLSID of a custom video mixer for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="ba911-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="ba911-105">Data type</span></span>

<span data-ttu-id="ba911-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="ba911-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="ba911-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="ba911-107">Remarks</span></span>

<span data-ttu-id="ba911-108">При создании Евр с помощью объекта активации этот атрибут можно использовать для установки пользовательского видеомикшера на Евр.</span><span class="sxs-lookup"><span data-stu-id="ba911-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video mixer on the EVR.</span></span> <span data-ttu-id="ba911-109">Используйте этот атрибут, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="ba911-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="ba911-110">Вызовите функцию [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) , чтобы создать объект активации для Евр.</span><span class="sxs-lookup"><span data-stu-id="ba911-110">Call the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="ba911-111">Функция возвращает указатель на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="ba911-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>

2.  <span data-ttu-id="ba911-112">Задайте этот аттрибуе в указателе [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , вызвав [**Имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="ba911-112">Set this attribue on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span> <span data-ttu-id="ba911-113">Значение атрибута является идентификатором CLSID пользовательского видеомикшера приложения.</span><span class="sxs-lookup"><span data-stu-id="ba911-113">The value of the attribute is the CLSID of the application's custom video mixer.</span></span>

<span data-ttu-id="ba911-114">Если этот атрибут задан, ЕВР вызывает **CoCreateInstance** с указанным идентификатором CLSID для создания пользовательского видеомикшера.</span><span class="sxs-lookup"><span data-stu-id="ba911-114">If this attribute is set, the EVR calls **CoCreateInstance** with the specified CLSID to create the custom video mixer.</span></span> <span data-ttu-id="ba911-115">Видеомикшер должен предоставлять интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="ba911-115">The video mixer must expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span> <span data-ttu-id="ba911-116">Микшер создается как внутрипроцессный COM-сервер.</span><span class="sxs-lookup"><span data-stu-id="ba911-116">The mixer is created as an in-process COM server.</span></span>

<span data-ttu-id="ba911-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="ba911-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba911-118">Требования</span><span class="sxs-lookup"><span data-stu-id="ba911-118">Requirements</span></span>



| <span data-ttu-id="ba911-119">Требование</span><span class="sxs-lookup"><span data-stu-id="ba911-119">Requirement</span></span> | <span data-ttu-id="ba911-120">Значение</span><span class="sxs-lookup"><span data-stu-id="ba911-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ba911-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="ba911-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ba911-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="ba911-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ba911-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="ba911-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ba911-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="ba911-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ba911-125">Header</span><span class="sxs-lookup"><span data-stu-id="ba911-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="ba911-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="ba911-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba911-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="ba911-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba911-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="ba911-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="ba911-129">Расширенные атрибуты модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="ba911-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="ba911-130">**Имфаттрибутес:: a GUID**</span><span class="sxs-lookup"><span data-stu-id="ba911-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="ba911-131">**Имфаттрибутес:: Сетгуид**</span><span class="sxs-lookup"><span data-stu-id="ba911-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="ba911-132">**имфактивате**</span><span class="sxs-lookup"><span data-stu-id="ba911-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="ba911-133">Объекты активации</span><span class="sxs-lookup"><span data-stu-id="ba911-133">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




