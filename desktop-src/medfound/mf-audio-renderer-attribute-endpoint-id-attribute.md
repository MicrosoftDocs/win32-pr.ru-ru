---
description: Указывает идентификатор для устройства конечной точки аудио.
ms.assetid: f145fb80-c136-421c-9a65-e69c52109348
title: Атрибут MF_AUDIO_RENDERER_ATTRIBUTE_ENDPOINT_ID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e042f59baf4812c177358acca6badb2422914afc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104344595"
---
# <a name="mf_audio_renderer_attribute_endpoint_id-attribute"></a><span data-ttu-id="92c4f-103">\_ \_ \_ \_ Атрибут идентификатора конечной точки атрибута для модуля подготовки звука MF \_</span><span class="sxs-lookup"><span data-stu-id="92c4f-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ID attribute</span></span>

<span data-ttu-id="92c4f-104">Указывает идентификатор для устройства конечной точки аудио.</span><span class="sxs-lookup"><span data-stu-id="92c4f-104">Specifies the identifier for the audio endpoint device.</span></span>

## <a name="data-type"></a><span data-ttu-id="92c4f-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="92c4f-105">Data type</span></span>

<span data-ttu-id="92c4f-106">Строка расширенных символов</span><span class="sxs-lookup"><span data-stu-id="92c4f-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="92c4f-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="92c4f-107">Remarks</span></span>

<span data-ttu-id="92c4f-108">Этот атрибут можно использовать для настройки модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="92c4f-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="92c4f-109">Использование зависит от того, какая функция вызывается для создания модуля подготовки звука:</span><span class="sxs-lookup"><span data-stu-id="92c4f-109">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="92c4f-110">[**Мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Задайте этот атрибут с помощью указателя интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , указанного в параметре *паудиоаттрибутес* .</span><span class="sxs-lookup"><span data-stu-id="92c4f-110">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="92c4f-111">[**Мфкреатеаудиорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Задайте этот атрибут с помощью указателя интерфейса [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , полученного в параметре *ппактивате* .</span><span class="sxs-lookup"><span data-stu-id="92c4f-111">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="92c4f-112">Задайте атрибут перед вызовом [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="92c4f-112">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="92c4f-113">Устройство конечной точки аудио — это аппаратное устройство, которое использует один конец пути к звуковым данным, например наушники или динамик.</span><span class="sxs-lookup"><span data-stu-id="92c4f-113">An audio endpoint device is a hardware device that lies at one end of an audio data path, such as a headphone or a speaker.</span></span> <span data-ttu-id="92c4f-114">Чтобы получить идентификатор конечной точки аудио, используйте следующие основные API аудио:</span><span class="sxs-lookup"><span data-stu-id="92c4f-114">To obtain the audio endpoint identifier, use the following core audio APIs:</span></span>

-   <span data-ttu-id="92c4f-115">Используйте интерфейс [**иммдевицеенумератор**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) для перечисления устройств в системе.</span><span class="sxs-lookup"><span data-stu-id="92c4f-115">Use the [**IMMDeviceEnumerator**](/windows/win32/api/mmdeviceapi/nn-mmdeviceapi-immdeviceenumerator) interface to enumerate the devices on the system.</span></span>
-   <span data-ttu-id="92c4f-116">Вызовите [**иммдевице:: GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) , чтобы получить идентификатор для устройства.</span><span class="sxs-lookup"><span data-stu-id="92c4f-116">Call [**IMMDevice::GetId**](/windows/win32/api/mmdeviceapi/nf-mmdeviceapi-immdevice-getid) to get the identifier for the device.</span></span>

<span data-ttu-id="92c4f-117">Дополнительные сведения см. в документации по [основным аудио](../coreaudio/core-audio-apis-in-windows-vista.md) API.</span><span class="sxs-lookup"><span data-stu-id="92c4f-117">For more information, see the [Core Audio](../coreaudio/core-audio-apis-in-windows-vista.md) API documentation.</span></span> <span data-ttu-id="92c4f-118">Если этот атрибут не задан, модуль подготовки звука использует устройство конечной точки по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="92c4f-118">If this attribute is not set, the audio renderer uses the default endpoint device.</span></span>

<span data-ttu-id="92c4f-119">Если этот атрибут задан, не устанавливайте атрибут [**\_ \_ \_ \_ \_ роли конечной точки для атрибута «модуль подготовки звука MF**](mf-audio-renderer-attribute-endpoint-role-attribute.md) ».</span><span class="sxs-lookup"><span data-stu-id="92c4f-119">If this attribute is set, do not set the [**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_ENDPOINT\_ROLE**](mf-audio-renderer-attribute-endpoint-role-attribute.md) attribute.</span></span> <span data-ttu-id="92c4f-120">Если заданы оба атрибута, то при создании модуля подготовки звука произойдет сбой.</span><span class="sxs-lookup"><span data-stu-id="92c4f-120">If both attributes are set, a failure will occur when the audio renderer is created.</span></span>

<span data-ttu-id="92c4f-121">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="92c4f-121">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="92c4f-122">Требования</span><span class="sxs-lookup"><span data-stu-id="92c4f-122">Requirements</span></span>



| <span data-ttu-id="92c4f-123">Требование</span><span class="sxs-lookup"><span data-stu-id="92c4f-123">Requirement</span></span> | <span data-ttu-id="92c4f-124">Значение</span><span class="sxs-lookup"><span data-stu-id="92c4f-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="92c4f-125">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="92c4f-125">Minimum supported client</span></span><br/> | <span data-ttu-id="92c4f-126">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="92c4f-126">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="92c4f-127">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="92c4f-127">Minimum supported server</span></span><br/> | <span data-ttu-id="92c4f-128">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="92c4f-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="92c4f-129">Header</span><span class="sxs-lookup"><span data-stu-id="92c4f-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="92c4f-130"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="92c4f-130"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="92c4f-131">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="92c4f-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92c4f-132">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="92c4f-132">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="92c4f-133">Атрибуты модуля подготовки звука</span><span class="sxs-lookup"><span data-stu-id="92c4f-133">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="92c4f-134">**Имфаттрибутес:: GetString**</span><span class="sxs-lookup"><span data-stu-id="92c4f-134">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="92c4f-135">**Имфаттрибутес:: SetString**</span><span class="sxs-lookup"><span data-stu-id="92c4f-135">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="92c4f-136">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="92c4f-136">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
