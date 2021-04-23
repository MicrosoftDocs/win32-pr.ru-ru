---
description: Указывает класс политики аудио для модуля подготовки звука.
ms.assetid: 80b028f5-7756-4bb8-b5e3-ebc8343e168c
title: Атрибут MF_AUDIO_RENDERER_ATTRIBUTE_SESSION_ID (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4952a60d4438e610677b494290e9738e469770d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911424"
---
# <a name="mf_audio_renderer_attribute_session_id-attribute"></a><span data-ttu-id="016e4-103">\_ \_ \_ \_ Атрибут идентификатора сеанса атрибута для обработчика звука MF \_</span><span class="sxs-lookup"><span data-stu-id="016e4-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_SESSION\_ID attribute</span></span>

<span data-ttu-id="016e4-104">Указывает класс политики аудио для модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="016e4-104">Specifies the audio policy class for the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="016e4-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="016e4-105">Data type</span></span>

<span data-ttu-id="016e4-106">**GUID**</span><span class="sxs-lookup"><span data-stu-id="016e4-106">**GUID**</span></span>

## <a name="remarks"></a><span data-ttu-id="016e4-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="016e4-107">Remarks</span></span>

<span data-ttu-id="016e4-108">Этот атрибут связывает модуль подготовки звука с классом политики аудио.</span><span class="sxs-lookup"><span data-stu-id="016e4-108">This attribute associates the audio renderer with an audio policy class.</span></span> <span data-ttu-id="016e4-109">Каждый класс политики имеет свой собственный том и элемент управления политикой.</span><span class="sxs-lookup"><span data-stu-id="016e4-109">Each policy class has its own volume and policy control.</span></span> <span data-ttu-id="016e4-110">Если этот атрибут не задан, новое приложение будет соединено с звуковым сеансом приложения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="016e4-110">If this attribute is not set, the new SAR joins the application's default audio session.</span></span> <span data-ttu-id="016e4-111">Дополнительные сведения см. в разделе [**иаудиоклиент:: Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) в основной документации по API аудио.</span><span class="sxs-lookup"><span data-stu-id="016e4-111">For more information, see [**IAudioClient::Initialize**](/windows/win32/api/audioclient/nf-audioclient-iaudioclient-initialize) in the core audio API documentation.</span></span>

<span data-ttu-id="016e4-112">Этот атрибут можно использовать для настройки модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="016e4-112">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="016e4-113">Использование зависит от того, какая функция вызывается для создания модуля подготовки звука:</span><span class="sxs-lookup"><span data-stu-id="016e4-113">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="016e4-114">[**Мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Задайте этот атрибут с помощью указателя интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , указанного в параметре *паудиоаттрибутес* .</span><span class="sxs-lookup"><span data-stu-id="016e4-114">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="016e4-115">[**Мфкреатеаудиорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Задайте этот атрибут с помощью указателя интерфейса [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , полученного в параметре *ппактивате* .</span><span class="sxs-lookup"><span data-stu-id="016e4-115">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="016e4-116">Задайте атрибут перед вызовом [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="016e4-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="016e4-117">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="016e4-117">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="016e4-118">Требования</span><span class="sxs-lookup"><span data-stu-id="016e4-118">Requirements</span></span>



| <span data-ttu-id="016e4-119">Требование</span><span class="sxs-lookup"><span data-stu-id="016e4-119">Requirement</span></span> | <span data-ttu-id="016e4-120">Значение</span><span class="sxs-lookup"><span data-stu-id="016e4-120">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="016e4-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="016e4-121">Minimum supported client</span></span><br/> | <span data-ttu-id="016e4-122">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="016e4-122">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="016e4-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="016e4-123">Minimum supported server</span></span><br/> | <span data-ttu-id="016e4-124">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="016e4-124">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="016e4-125">Header</span><span class="sxs-lookup"><span data-stu-id="016e4-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="016e4-126"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="016e4-126"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="016e4-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="016e4-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="016e4-128">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="016e4-128">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="016e4-129">Атрибуты модуля подготовки звука</span><span class="sxs-lookup"><span data-stu-id="016e4-129">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="016e4-130">**Имфаттрибутес:: a GUID**</span><span class="sxs-lookup"><span data-stu-id="016e4-130">**IMFAttributes::GetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getguid)
</dt> <dt>

[<span data-ttu-id="016e4-131">**Имфаттрибутес:: Сетгуид**</span><span class="sxs-lookup"><span data-stu-id="016e4-131">**IMFAttributes::SetGUID**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setguid)
</dt> <dt>

[<span data-ttu-id="016e4-132">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="016e4-132">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 
