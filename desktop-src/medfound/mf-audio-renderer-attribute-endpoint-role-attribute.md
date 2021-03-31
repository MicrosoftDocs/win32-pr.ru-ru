---
description: Указывает роль конечной точки аудио для модуля подготовки звука.
ms.assetid: f0456337-5351-457e-9830-920bf346bfc4
title: Атрибут MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ROLE (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a1b6599ffc97cfa9c7fc2b6a75f4ed4ae7c2c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998854"
---
# <a name="mf_audio_renderer_attribute_endpoint_role-attribute"></a><span data-ttu-id="673c8-103">\_ \_ \_ \_ Атрибут роли конечной точки для атрибута для обработчика звука MF \_</span><span class="sxs-lookup"><span data-stu-id="673c8-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE attribute</span></span>

<span data-ttu-id="673c8-104">Указывает роль конечной точки аудио для модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="673c8-104">Specifies the audio endpoint role for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="673c8-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="673c8-105">Data type</span></span>

<span data-ttu-id="673c8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="673c8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="673c8-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="673c8-107">Remarks</span></span>

<span data-ttu-id="673c8-108">Этот атрибут можно использовать для настройки модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="673c8-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="673c8-109">Использование зависит от того, какая функция вызывается для создания модуля подготовки звука:</span><span class="sxs-lookup"><span data-stu-id="673c8-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="673c8-110">[**Мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Задайте этот атрибут с помощью указателя интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , указанного в параметре *паудиоаттрибутес* .</span><span class="sxs-lookup"><span data-stu-id="673c8-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="673c8-111">[**Мфкреатеаудиорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Задайте этот атрибут с помощью указателя интерфейса [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , полученного в параметре *ппактивате* .</span><span class="sxs-lookup"><span data-stu-id="673c8-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="673c8-112">Задайте атрибут перед вызовом [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="673c8-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="673c8-113">Устройство конечной точки аудио — это аппаратное устройство, которое использует один конец пути к звуковым данным, например наушники или динамик.</span><span class="sxs-lookup"><span data-stu-id="673c8-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span>

<span data-ttu-id="673c8-114">Если этот атрибут задан, модуль подготовки звука использует для указанной роли звуковое устройство по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="673c8-114">If this attribute is set, the audio renderer uses the default audio device for the specified role.</span></span> <span data-ttu-id="673c8-115">Значение этого атрибута является членом перечисления **ероле** , который определен в файле заголовка ммдевицеапи. h.</span><span class="sxs-lookup"><span data-stu-id="673c8-115">The value of this attribute is a member of the **ERole** enumeration, which is defined in the header file mmdeviceapi.h.</span></span> <span data-ttu-id="673c8-116">Дополнительные сведения см. в документации по основным аудио API.</span><span class="sxs-lookup"><span data-stu-id="673c8-116">For more information, see the Core Audio API documentation.</span></span> <span data-ttu-id="673c8-117">Если этот атрибут не задан, модуль подготовки звука использует устройство конечной точки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="673c8-117">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="673c8-118">Если этот атрибут задан, не задавайте атрибут [**\_ \_ \_ \_ \_ ID конечной точки атрибута «модуль подготовки звука MF**](mf-audio-renderer-attribute-endpoint-id-attribute.md) ».</span><span class="sxs-lookup"><span data-stu-id="673c8-118">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID**](mf-audio-renderer-attribute-endpoint-id-attribute.md) attribute.</span></span> <span data-ttu-id="673c8-119">Если заданы оба атрибута, то при создании модуля подготовки звука произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="673c8-119">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="673c8-120">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="673c8-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="673c8-121">Требования</span><span class="sxs-lookup"><span data-stu-id="673c8-121">Requirements</span></span>



| <span data-ttu-id="673c8-122">Требование</span><span class="sxs-lookup"><span data-stu-id="673c8-122">Requirement</span></span> | <span data-ttu-id="673c8-123">Значение</span><span class="sxs-lookup"><span data-stu-id="673c8-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="673c8-124">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="673c8-124">Minimum supported client</span></span><br/> | <span data-ttu-id="673c8-125">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="673c8-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="673c8-126">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="673c8-126">Minimum supported server</span></span><br/> | <span data-ttu-id="673c8-127">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="673c8-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="673c8-128">Header</span><span class="sxs-lookup"><span data-stu-id="673c8-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="673c8-129"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="673c8-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="673c8-130">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="673c8-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="673c8-131">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="673c8-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="673c8-132">Атрибуты модуля подготовки звука</span><span class="sxs-lookup"><span data-stu-id="673c8-132">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="673c8-133">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="673c8-133">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="673c8-134">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="673c8-134">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="673c8-135">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="673c8-135">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




