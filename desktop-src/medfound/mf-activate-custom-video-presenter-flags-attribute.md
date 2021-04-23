---
description: Указывает, как создать пользовательский объект Presenter для расширенного обработчика видео (Евр).
ms.assetid: 40893e13-bf2e-4424-ae43-2b253fc0b622
title: Атрибут MF_ACTIVATE_CUSTOM_VIDEO_PRESENTER_FLAGS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3681edaed39b63b0f7c13313039f1c6e72311a87
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081107"
---
# <a name="mf_activate_custom_video_presenter_flags-attribute"></a><span data-ttu-id="a64a1-103">MF \_ активировать \_ Пользовательский \_ \_ \_ атрибут флагов видеоадаптера</span><span class="sxs-lookup"><span data-stu-id="a64a1-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_FLAGS attribute</span></span>

<span data-ttu-id="a64a1-104">Указывает, как создать пользовательский объект Presenter для расширенного обработчика видео (Евр).</span><span class="sxs-lookup"><span data-stu-id="a64a1-104">Specifies how to create a custom presenter for the enhanced video renderer (EVR).</span></span>

## <a name="data-type"></a><span data-ttu-id="a64a1-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="a64a1-105">Data type</span></span>

<span data-ttu-id="a64a1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="a64a1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="a64a1-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="a64a1-107">Remarks</span></span>

<span data-ttu-id="a64a1-108">Этот атрибут можно задать для указателя [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , полученного из функции [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="a64a1-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer obtained from the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span> <span data-ttu-id="a64a1-109">Значение этого атрибута является побитовым оператором **или** для следующих значений.</span><span class="sxs-lookup"><span data-stu-id="a64a1-109">The value of this attribute is a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="a64a1-110">Значение</span><span class="sxs-lookup"><span data-stu-id="a64a1-110">Value</span></span>                                          | <span data-ttu-id="a64a1-111">Описание</span><span class="sxs-lookup"><span data-stu-id="a64a1-111">Description</span></span>                                                                                                                                                                                                                                                                                                                          |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a64a1-112">**MF \_ Активация \_ пользовательского \_ Presenter \_ алловфаил**</span><span class="sxs-lookup"><span data-stu-id="a64a1-112">**MF\_ACTIVATE\_CUSTOM\_PRESENTER\_ALLOWFAIL**</span></span> | <span data-ttu-id="a64a1-113">Если метод [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) не может создать настраиваемый объект Presenter приложения, вместо него будет использоваться выступающий по умолчанию Евр.</span><span class="sxs-lookup"><span data-stu-id="a64a1-113">If the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails to create the application's custom presenter, it uses the default EVR presenter instead.</span></span> <span data-ttu-id="a64a1-114">По умолчанию, если происходит сбой объекта [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) при попытке создать пользовательский объект Presenter, метод **активатеобжект** завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="a64a1-114">By default, if the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object fails when it tries to create the custom presenter, the **ActivateObject** method fails.</span></span> |



 

<span data-ttu-id="a64a1-115">Приложения могут использовать [**\_ \_ настраиваемый атрибут \_ \_ \_ CLSID "порт MF**](mf-activate-custom-video-presenter-clsid-attribute.md) ", чтобы указать пользовательский объект Presenter для Евр.</span><span class="sxs-lookup"><span data-stu-id="a64a1-115">Applications can use the [**MF\_ACTIVATE\_CUSTOM\_VIDEO\_PRESENTER\_CLSID**](mf-activate-custom-video-presenter-clsid-attribute.md) attribute to specify a custom presenter for the EVR.</span></span>

<span data-ttu-id="a64a1-116">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="a64a1-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="a64a1-117">Требования</span><span class="sxs-lookup"><span data-stu-id="a64a1-117">Requirements</span></span>



| <span data-ttu-id="a64a1-118">Требование</span><span class="sxs-lookup"><span data-stu-id="a64a1-118">Requirement</span></span> | <span data-ttu-id="a64a1-119">Значение</span><span class="sxs-lookup"><span data-stu-id="a64a1-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a64a1-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="a64a1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a64a1-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="a64a1-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="a64a1-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="a64a1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a64a1-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="a64a1-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a64a1-124">Header</span><span class="sxs-lookup"><span data-stu-id="a64a1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a64a1-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="a64a1-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a64a1-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="a64a1-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a64a1-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a64a1-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="a64a1-128">Расширенные атрибуты модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="a64a1-128">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="a64a1-129">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="a64a1-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="a64a1-130">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="a64a1-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="a64a1-131">Объекты активации</span><span class="sxs-lookup"><span data-stu-id="a64a1-131">Activation Objects</span></span>](activation-objects.md)
</dt> <dt>

[<span data-ttu-id="a64a1-132">Написание выступающего Евр</span><span class="sxs-lookup"><span data-stu-id="a64a1-132">How to Write an EVR Presenter</span></span>](how-to-write-an-evr-presenter.md)
</dt> </dl>

 

 




