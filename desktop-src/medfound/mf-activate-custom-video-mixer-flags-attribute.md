---
description: Указывает, как создать пользовательское микшер для расширенного обработчика видео (Евр).
ms.assetid: 00e65718-885f-4e1f-9b06-66c7f5786851
title: Атрибут MF_ACTIVATE_CUSTOM_VIDEO_MIXER_FLAGS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b17a0063b7ef4b6a1cbb5993ea2fb7af2a4a678
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815513"
---
# <a name="mf_activate_custom_video_mixer_flags-attribute"></a><span data-ttu-id="3c9e9-103">MF \_ активировать \_ Пользовательский \_ \_ \_ атрибут флагов микшера видео</span><span class="sxs-lookup"><span data-stu-id="3c9e9-103">MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_FLAGS attribute</span></span>

<span data-ttu-id="3c9e9-104">Указывает, как создать пользовательское микшер для расширенного обработчика видео (Евр).</span><span class="sxs-lookup"><span data-stu-id="3c9e9-104">Specifies how to create a custom mixer for the enhanced video renderer (EVR).</span></span>

## <a name="data-type"></a><span data-ttu-id="3c9e9-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="3c9e9-105">Data type</span></span>

<span data-ttu-id="3c9e9-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="3c9e9-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="3c9e9-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="3c9e9-107">Remarks</span></span>

<span data-ttu-id="3c9e9-108">Этот атрибут можно задать для указателя [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , полученного из функции [**мфкреатевидеорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) .</span><span class="sxs-lookup"><span data-stu-id="3c9e9-108">You can set this attribute on the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer obtained from the [**MFCreateVideoRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatevideorendereractivate) function.</span></span> <span data-ttu-id="3c9e9-109">Значение этого атрибута является побитовым оператором **или** для следующих значений.</span><span class="sxs-lookup"><span data-stu-id="3c9e9-109">The value of this attribute is a bitwise **OR** of the following values.</span></span>



| <span data-ttu-id="3c9e9-110">Значение</span><span class="sxs-lookup"><span data-stu-id="3c9e9-110">Value</span></span>                                      | <span data-ttu-id="3c9e9-111">Описание</span><span class="sxs-lookup"><span data-stu-id="3c9e9-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|--------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c9e9-112">**MF \_ Активация \_ настраиваемого \_ алловфаил микшера \_**</span><span class="sxs-lookup"><span data-stu-id="3c9e9-112">**MF\_ACTIVATE\_CUSTOM\_MIXER\_ALLOWFAIL**</span></span> | <span data-ttu-id="3c9e9-113">Если метод [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) не может создать пользовательское микшер приложения, вместо него используется микшер Евр по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="3c9e9-113">If the [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method fails to create the application's custom mixer, it uses the default EVR mixer instead.</span></span> <span data-ttu-id="3c9e9-114">По умолчанию, если при попытке создания пользовательского микшера происходит сбой объекта [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , метод **активатеобжект** завершается ошибкой.</span><span class="sxs-lookup"><span data-stu-id="3c9e9-114">By default, if the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) object fails when it tries to create the custom mixer, the **ActivateObject** method fails.</span></span> |



 

<span data-ttu-id="3c9e9-115">Приложения могут использовать [**\_ \_ настраиваемый атрибут \_ \_ \_ CLSID "порт MF**](mf-activate-custom-video-mixer-clsid-attribute.md) ", чтобы указать пользовательское микшер для Евр.</span><span class="sxs-lookup"><span data-stu-id="3c9e9-115">Applications can use the [**MF\_ACTIVATE\_CUSTOM\_VIDEO\_MIXER\_CLSID**](mf-activate-custom-video-mixer-clsid-attribute.md) attribute to specify a custom mixer for the EVR.</span></span>

<span data-ttu-id="3c9e9-116">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="3c9e9-116">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c9e9-117">Требования</span><span class="sxs-lookup"><span data-stu-id="3c9e9-117">Requirements</span></span>



| <span data-ttu-id="3c9e9-118">Требование</span><span class="sxs-lookup"><span data-stu-id="3c9e9-118">Requirement</span></span> | <span data-ttu-id="3c9e9-119">Значение</span><span class="sxs-lookup"><span data-stu-id="3c9e9-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="3c9e9-120">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="3c9e9-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3c9e9-121">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3c9e9-121">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="3c9e9-122">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="3c9e9-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3c9e9-123">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3c9e9-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="3c9e9-124">Header</span><span class="sxs-lookup"><span data-stu-id="3c9e9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c9e9-125"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="3c9e9-125"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c9e9-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="3c9e9-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c9e9-127">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3c9e9-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="3c9e9-128">Расширенные атрибуты модуля подготовки видео</span><span class="sxs-lookup"><span data-stu-id="3c9e9-128">Enhanced Video Renderer Attributes</span></span>](enhanced-video-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="3c9e9-129">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="3c9e9-129">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="3c9e9-130">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="3c9e9-130">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="3c9e9-131">Объекты активации</span><span class="sxs-lookup"><span data-stu-id="3c9e9-131">Activation Objects</span></span>](activation-objects.md)
</dt> </dl>

 

 




