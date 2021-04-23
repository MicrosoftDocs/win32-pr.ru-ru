---
description: Указывает объект активации, который создает пользовательский Видеомикшер для приемника расширенного модуля подготовки видео (Евр).
ms.assetid: 60484f87-7588-4b52-93aa-ef8fad66d971
title: Атрибут MF_ACTIVATE_CUSTOM_VIDEO_MIXER_ACTIVATE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d6268f3630b013235f3d365e0b8ab0578c9dd3e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155574"
---
# <a name="mf_activate_custom_video_mixer_activate-attribute"></a><span data-ttu-id="9b0cb-103">MF \_ Активация \_ пользовательского \_ \_ микшера \_ активации атрибута</span><span class="sxs-lookup"><span data-stu-id="9b0cb-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_ACTIVATE attribute</span></span>

<span data-ttu-id="9b0cb-104">Указывает объект активации, который создает пользовательский Видеомикшер для приемника расширенного модуля подготовки видео (Евр).</span><span class="sxs-lookup"><span data-stu-id="9b0cb-104">Specifies an activation object that creates a custom video mixer for the enhanced video renderer (EVR) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="9b0cb-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9b0cb-105">Data type</span></span>

<span data-ttu-id="9b0cb-106">\**IUnknown \** _</span><span class="sxs-lookup"><span data-stu-id="9b0cb-106">\**IUnknown\** _</span></span>

## <a name="remarks"></a><span data-ttu-id="9b0cb-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9b0cb-107">Remarks</span></span>

<span data-ttu-id="9b0cb-108">При создании Евр с помощью объекта активации этот атрибут можно использовать для установки пользовательского видеомикшера на Евр.</span><span class="sxs-lookup"><span data-stu-id="9b0cb-108">If you are creating the EVR through an activation object, you can use this attribute to set a custom video mixer on the EVR.</span></span> <span data-ttu-id="9b0cb-109">Используйте этот атрибут, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="9b0cb-109">Use this attribute as follows:</span></span>

1.  <span data-ttu-id="9b0cb-110">Вызовите функцию [_ *мфкреатевидеорендерерактивате* \*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) , чтобы создать объект активации для Евр.</span><span class="sxs-lookup"><span data-stu-id="9b0cb-110">Call the [_ *MFCreateVideoRendererActivate*\*](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function to create an activation object for the EVR.</span></span> <span data-ttu-id="9b0cb-111">Функция возвращает указатель на интерфейс [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) .</span><span class="sxs-lookup"><span data-stu-id="9b0cb-111">The function returns a pointer to the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface.</span></span>
2.  <span data-ttu-id="9b0cb-112">Установите этот атрибут для указателя [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , вызвав [**Имфаттрибутес:: сетункновн**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span><span class="sxs-lookup"><span data-stu-id="9b0cb-112">Set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer by calling [**IMFAttributes::SetUnknown**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown).</span></span> <span data-ttu-id="9b0cb-113">Значение атрибута является указателем на объект активации, реализованный вызывающим объектом.</span><span class="sxs-lookup"><span data-stu-id="9b0cb-113">The value of the attribute is a pointer to an activation object implemented by the caller.</span></span> <span data-ttu-id="9b0cb-114">Объект активации вызывающего объекта должен предоставлять интерфейс **имфактивате** .</span><span class="sxs-lookup"><span data-stu-id="9b0cb-114">The caller's activation object must expose the **IMFActivate** interface.</span></span>

<span data-ttu-id="9b0cb-115">Если задать этот атрибут, ЕВР вызывает [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) для создания пользовательского видеомикшера.</span><span class="sxs-lookup"><span data-stu-id="9b0cb-115">If you set this attribute, the EVR calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the custom video mixer.</span></span> <span data-ttu-id="9b0cb-116">Видеомикшер должен предоставлять интерфейс [**имфтрансформ**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) .</span><span class="sxs-lookup"><span data-stu-id="9b0cb-116">The video mixer must expose the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface.</span></span>

<span data-ttu-id="9b0cb-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="9b0cb-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b0cb-118">Требования</span><span class="sxs-lookup"><span data-stu-id="9b0cb-118">Requirements</span></span>



| <span data-ttu-id="9b0cb-119">Требование</span><span class="sxs-lookup"><span data-stu-id="9b0cb-119">Requirement</span></span> | <span data-ttu-id="9b0cb-120">Значение</span><span class="sxs-lookup"><span data-stu-id="9b0cb-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9b0cb-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9b0cb-121">Minimum supported client</span></span><br/> | <span data-ttu-id="9b0cb-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="9b0cb-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="9b0cb-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9b0cb-123">Minimum supported server</span></span><br/> | <span data-ttu-id="9b0cb-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="9b0cb-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="9b0cb-125">Header</span><span class="sxs-lookup"><span data-stu-id="9b0cb-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="9b0cb-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="9b0cb-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9b0cb-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9b0cb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9b0cb-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9b0cb-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9b0cb-129">Расширенные атрибуты модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="9b0cb-129">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="9b0cb-130">**Имфаттрибутес:: неизвестный**</span><span class="sxs-lookup"><span data-stu-id="9b0cb-130">**IMFAttributes::GetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getunknown)
</dt> <dt>

[<span data-ttu-id="9b0cb-131">**Имфаттрибутес:: Сетункновн**</span><span class="sxs-lookup"><span data-stu-id="9b0cb-131">**IMFAttributes::SetUnknown**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setunknown)
</dt> <dt>

[<span data-ttu-id="9b0cb-132">**имфактивате**</span><span class="sxs-lookup"><span data-stu-id="9b0cb-132">**IMFActivate**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate)
</dt> <dt>

[<span data-ttu-id="9b0cb-133">Объекты активации</span><span class="sxs-lookup"><span data-stu-id="9b0cb-133">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




