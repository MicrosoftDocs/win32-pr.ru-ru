---
description: Содержит флаги для настройки модуля подготовки звука.
ms.assetid: 07433904-1bf6-4e8d-9571-8d663bf4fd13
title: Атрибут MF_AUDIO_RENDERER_ATTRIBUTE_FLAGS (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c17d4b5a51384ebcd180643e0a07601d25e5fb5f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683126"
---
# <a name="mf_audio_renderer_attribute_flags-attribute"></a><span data-ttu-id="b3eb8-103">\_ \_ \_ Атрибут флагов атрибутов модуля подготовки звука \_ MF</span><span class="sxs-lookup"><span data-stu-id="b3eb8-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS attribute</span></span>

<span data-ttu-id="b3eb8-104">Содержит флаги для настройки модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-104">Contains flags to configure the audio renderer.</span></span>

## <a name="data-type"></a><span data-ttu-id="b3eb8-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="b3eb8-105">Data type</span></span>

<span data-ttu-id="b3eb8-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="b3eb8-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="b3eb8-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="b3eb8-107">Remarks</span></span>

<span data-ttu-id="b3eb8-108">Значение этого атрибута является побитовым оператором **или** для следующих флагов.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-108">The value of this attribute is a bitwise **OR** of the following flags.</span></span>



| <span data-ttu-id="b3eb8-109">Значение</span><span class="sxs-lookup"><span data-stu-id="b3eb8-109">Value</span></span>                                                   | <span data-ttu-id="b3eb8-110">Описание</span><span class="sxs-lookup"><span data-stu-id="b3eb8-110">Description</span></span>                                                                                                                                                                                                                                                                                                                       |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b3eb8-111">**\_ \_ Флаги атрибута модуля подготовки звука MF \_ \_ \_ Кросспроцесс**</span><span class="sxs-lookup"><span data-stu-id="b3eb8-111">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_CROSSPROCESS**</span></span> | <span data-ttu-id="b3eb8-112">Модуль подготовки звука использует многопроцессный сеанс аудио.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-112">The audio renderer is uses a cross-process audio session.</span></span> <span data-ttu-id="b3eb8-113">Этот флаг позволяет модулям подготовки звука в нескольких процессах использовать один и тот же сеанс звука вместе с соответствующими элементами управления томами и политиками.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-113">This flag enables audio renderers in multiple processes to share the same audio session, along with the associated volume and policy controls.</span></span><br/> <span data-ttu-id="b3eb8-114">Если этот флаг не установлен, то сеанс звука не может совместно использоваться модулями подготовки звука в других процессах.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-114">If this flag is not set, the audio session cannot be shared by audio renderers in other processes.</span></span><br/> |
| <span data-ttu-id="b3eb8-115">**\_ \_ Флаги атрибута модуля подготовки звука MF \_ \_ \_ не сохранены**</span><span class="sxs-lookup"><span data-stu-id="b3eb8-115">**MF\_AUDIO\_RENDERER\_ATTRIBUTE\_FLAGS\_NOPERSIST**</span></span>    | <span data-ttu-id="b3eb8-116">API сеанса Windows Audio (ВАСАПИ) не сохраняет свойства для этого сеанса аудио, например том сеанса.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-116">The Windows audio session API (WASAPI) will not persist the properties for this audio session, such as the session volume.</span></span><br/> <span data-ttu-id="b3eb8-117">Если этот флаг не установлен, ВАСАПИ сохранит свойства сеанса аудио.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-117">If this flag is not set, WASAPI will persist the audio session properties.</span></span><br/>                                                                                                       |



 

<span data-ttu-id="b3eb8-118">Этот атрибут можно использовать для настройки модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-118">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="b3eb8-119">Использование зависит от того, какая функция вызывается для создания модуля подготовки звука:</span><span class="sxs-lookup"><span data-stu-id="b3eb8-119">The usage depends on which function you call to create the audio renderer:</span></span>

-   <span data-ttu-id="b3eb8-120">[**Мфкреатеаудиорендерер**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Задайте этот атрибут с помощью указателя интерфейса [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , указанного в параметре *паудиоаттрибутес* .</span><span class="sxs-lookup"><span data-stu-id="b3eb8-120">[**MFCreateAudioRenderer**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer): Set this attribute using the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface pointer specified in the *pAudioAttributes* parameter.</span></span>
-   <span data-ttu-id="b3eb8-121">[**Мфкреатеаудиорендерерактивате**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Задайте этот атрибут с помощью указателя интерфейса [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , полученного в параметре *ппактивате* .</span><span class="sxs-lookup"><span data-stu-id="b3eb8-121">[**MFCreateAudioRendererActivate**](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate): Set this attribute using the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) interface pointer retrieved in the *ppActivate* parameter.</span></span> <span data-ttu-id="b3eb8-122">Задайте атрибут перед вызовом [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="b3eb8-122">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span>

<span data-ttu-id="b3eb8-123">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="b3eb8-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="b3eb8-124">Требования</span><span class="sxs-lookup"><span data-stu-id="b3eb8-124">Requirements</span></span>



| <span data-ttu-id="b3eb8-125">Требование</span><span class="sxs-lookup"><span data-stu-id="b3eb8-125">Requirement</span></span> | <span data-ttu-id="b3eb8-126">Значение</span><span class="sxs-lookup"><span data-stu-id="b3eb8-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b3eb8-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="b3eb8-127">Minimum supported client</span></span><br/> | <span data-ttu-id="b3eb8-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="b3eb8-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="b3eb8-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="b3eb8-129">Minimum supported server</span></span><br/> | <span data-ttu-id="b3eb8-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="b3eb8-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="b3eb8-131">Header</span><span class="sxs-lookup"><span data-stu-id="b3eb8-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="b3eb8-132"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3eb8-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b3eb8-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="b3eb8-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3eb8-134">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b3eb8-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="b3eb8-135">Атрибуты модуля подготовки звука</span><span class="sxs-lookup"><span data-stu-id="b3eb8-135">Audio Renderer Attributes</span></span>](audio-renderer-attributes.md)
</dt> <dt>

[<span data-ttu-id="b3eb8-136">**Имфаттрибутес:: UINT32**</span><span class="sxs-lookup"><span data-stu-id="b3eb8-136">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="b3eb8-137">**Имфаттрибутес:: SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="b3eb8-137">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="b3eb8-138">Потоковая прорисовка звука</span><span class="sxs-lookup"><span data-stu-id="b3eb8-138">Streaming Audio Renderer</span></span>](streaming-audio-renderer.md)
</dt> </dl>

 

 




