---
description: Идентификатор CLSID пользовательского средства показа видео для приемника расширенного модуля подготовки видео (Евр).
ms.assetid: f035ee56-7582-45d3-bafe-dd9c821b6326
title: Атрибут MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_CLSID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0eb913a56671d5d2ac8d27c785e1cc1fbfc51a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692512"
---
# <a name="mf_activate_custom_video_presenter_clsid-attribute"></a><span data-ttu-id="b71f3-103">MF \_ активировать \_ настраиваемый \_ \_ \_ атрибут CLSID видеоустройства</span><span class="sxs-lookup"><span data-stu-id="b71f3-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID attribute</span></span>

<span data-ttu-id="b71f3-104">Идентификатор CLSID пользовательского средства показа видео для приемника расширенного модуля подготовки видео (Евр).</span><span class="sxs-lookup"><span data-stu-id="b71f3-104">CLSID of a custom video presenter for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="b71f3-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b71f3-105">Data type</span></span>

<span data-ttu-id="b71f3-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="b71f3-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="b71f3-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b71f3-107">Remarks</span></span>

<span data-ttu-id="b71f3-108">Если вы создаете Евр с помощью объекта активации, этот атрибут можно использовать для задания пользовательского устройства показа видео в Евр.</span><span class="sxs-lookup"><span data-stu-id="b71f3-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video presenter on the EVR.</span></span> <span data-ttu-id="b71f3-109">Используйте этот атрибут, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="b71f3-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="b71f3-110">Вызовите функцию [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) , чтобы создать объект активации для Евр.</span><span class="sxs-lookup"><span data-stu-id="b71f3-110">Call the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="b71f3-111">Функция возвращает указатель на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="b71f3-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>

2.  <span data-ttu-id="b71f3-112">Задайте этот аттрибуе в указателе [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , вызвав [**Имфаттрибутес:: сетгуид**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span><span class="sxs-lookup"><span data-stu-id="b71f3-112">Set this attribue on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetGUID**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid).</span></span> <span data-ttu-id="b71f3-113">Значением атрибута является идентификатор CLSID пользовательского выступающего видео приложения.</span><span class="sxs-lookup"><span data-stu-id="b71f3-113">The value of the attribute is the CLSID of the application's custom video presenter.</span></span>

<span data-ttu-id="b71f3-114">Если этот атрибут задан, ЕВР вызывает **CoCreateInstance** с указанным идентификатором CLSID для создания пользовательского устройства показа видео.</span><span class="sxs-lookup"><span data-stu-id="b71f3-114">If this attribute is set, the EVR calls **CoCreateInstance** with the specified CLSID to create the custom video presenter.</span></span> <span data-ttu-id="b71f3-115">Устройство показа видео должно предоставлять интерфейс [**имфвидеопресентер**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) .</span><span class="sxs-lookup"><span data-stu-id="b71f3-115">The video presenter must expose the [**IMFVideoPresenter**](/windows/desktop/api/evr/nn-evr-imfvideopresenter) interface.</span></span> <span data-ttu-id="b71f3-116">Выступающий создается как внутрипроцессный COM-сервер.</span><span class="sxs-lookup"><span data-stu-id="b71f3-116">The presenter is created as an in-process COM server.</span></span>

<span data-ttu-id="b71f3-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="b71f3-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b71f3-118">Требования</span><span class="sxs-lookup"><span data-stu-id="b71f3-118">Requirements</span></span>



| <span data-ttu-id="b71f3-119">Требование</span><span class="sxs-lookup"><span data-stu-id="b71f3-119">Requirement</span></span> | <span data-ttu-id="b71f3-120">Значение</span><span class="sxs-lookup"><span data-stu-id="b71f3-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b71f3-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b71f3-121">Minimum supported client</span></span><br/> | <span data-ttu-id="b71f3-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b71f3-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b71f3-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b71f3-123">Minimum supported server</span></span><br/> | <span data-ttu-id="b71f3-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b71f3-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b71f3-125">Header</span><span class="sxs-lookup"><span data-stu-id="b71f3-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="b71f3-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b71f3-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b71f3-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b71f3-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b71f3-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b71f3-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b71f3-129">Расширенные атрибуты модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="b71f3-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="b71f3-130">**Имфаттрибутес:: a GUID**</span><span class="sxs-lookup"><span data-stu-id="b71f3-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="b71f3-131">**Имфаттрибутес:: Сетгуид**</span><span class="sxs-lookup"><span data-stu-id="b71f3-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="b71f3-132">**имфактивате**</span><span class="sxs-lookup"><span data-stu-id="b71f3-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="b71f3-133">Объекты активации</span><span class="sxs-lookup"><span data-stu-id="b71f3-133">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="b71f3-134">Написание выступающего Евр</span><span class="sxs-lookup"><span data-stu-id="b71f3-134">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




