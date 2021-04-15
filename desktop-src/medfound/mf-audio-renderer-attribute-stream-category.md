---
description: Указывает категорию звукового потока для модуля подготовки потоковой передачи звука (САР).
ms.assetid: 88E79DE6-2062-4471-A939-D1D4DD2EC42D
title: Атрибут MF_AUDIO_RENDERER_ATTRIBUTE_STREAM_CATEGORY (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd96c219e43f85c516a5f862e2a978724328a69f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105683125"
---
# <a name="mf_audio_renderer_attribute_stream_category-attribute"></a><span data-ttu-id="0d049-103">\_ \_ \_ \_ Атрибут категории потока атрибута для модуля подготовки звука MF \_</span><span class="sxs-lookup"><span data-stu-id="0d049-103">MF\_AUDIO\_RENDERER\_ATTRIBUTE\_STREAM\_CATEGORY attribute</span></span>

<span data-ttu-id="0d049-104">Указывает категорию звукового потока для модуля [подготовки потоковой передачи звука](streaming-audio-renderer.md) (САР).</span><span class="sxs-lookup"><span data-stu-id="0d049-104">Specifies the audio stream category for the [Streaming Audio Renderer](streaming-audio-renderer.md) (SAR).</span></span>

## <a name="data-type"></a><span data-ttu-id="0d049-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="0d049-105">Data type</span></span>

<span data-ttu-id="0d049-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="0d049-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="0d049-107">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0d049-107">Remarks</span></span>

<span data-ttu-id="0d049-108">Этот атрибут можно использовать для настройки модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="0d049-108">You can use this attribute to configure the audio renderer.</span></span> <span data-ttu-id="0d049-109">Использование зависит от того, какая функция вызывается для создания модуля подготовки звука.</span><span class="sxs-lookup"><span data-stu-id="0d049-109">The usage depends on which function you call to create the audio renderer.</span></span>



| <span data-ttu-id="0d049-110">Функция</span><span class="sxs-lookup"><span data-stu-id="0d049-110">Function</span></span>                                                               | <span data-ttu-id="0d049-111">Как задать атрибут</span><span class="sxs-lookup"><span data-stu-id="0d049-111">How to Set the attribute</span></span>                                                                                                                                                                       |
|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0d049-112">**мфкреатеаудиорендерер**</span><span class="sxs-lookup"><span data-stu-id="0d049-112">**MFCreateAudioRenderer**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorenderer)                 | <span data-ttu-id="0d049-113">Используйте указатель [**имфаттрибутес**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) , указанный в параметре *паудиоаттрибутес* .</span><span class="sxs-lookup"><span data-stu-id="0d049-113">Use the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) pointer specified in the *pAudioAttributes* parameter.</span></span>                                                                                          |
| [<span data-ttu-id="0d049-114">**мфкреатеаудиорендерерактивате**</span><span class="sxs-lookup"><span data-stu-id="0d049-114">**MFCreateAudioRendererActivate**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-mfcreateaudiorendereractivate) | <span data-ttu-id="0d049-115">Используйте указатель [**имфактивате**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) , возвращенный в параметре *ппактивате* .</span><span class="sxs-lookup"><span data-stu-id="0d049-115">Use the [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointer returned in the *ppActivate* parameter.</span></span> <span data-ttu-id="0d049-116">Задайте атрибут перед вызовом [**имфактивате:: активатеобжект**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span><span class="sxs-lookup"><span data-stu-id="0d049-116">Set the attribute before calling [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject).</span></span> |



 

<span data-ttu-id="0d049-117">Значение атрибута является членом перечисления [**\_ \_ категории аудиопотока**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) .</span><span class="sxs-lookup"><span data-stu-id="0d049-117">The value of the attribute is a member of the [**AUDIO\_STREAM\_CATEGORY**](/windows/win32/api/audiosessiontypes/ne-audiosessiontypes-audio_stream_category) enumeration.</span></span> <span data-ttu-id="0d049-118">Служба аудио использует категорию Stream для определения политик аудио, когда несколько приложений одновременно воспроизводят звук.</span><span class="sxs-lookup"><span data-stu-id="0d049-118">The audio service uses the stream category to determine audio policies when multiple applications play audio at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="0d049-119">Требования</span><span class="sxs-lookup"><span data-stu-id="0d049-119">Requirements</span></span>



| <span data-ttu-id="0d049-120">Требование</span><span class="sxs-lookup"><span data-stu-id="0d049-120">Requirement</span></span> | <span data-ttu-id="0d049-121">Значение</span><span class="sxs-lookup"><span data-stu-id="0d049-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0d049-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="0d049-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0d049-123">\[Только классические приложения Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="0d049-123">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0d049-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="0d049-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0d049-125">\[Только для настольных приложений Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="0d049-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="0d049-126">Header</span><span class="sxs-lookup"><span data-stu-id="0d049-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d049-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d049-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d049-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0d049-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d049-129">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0d049-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 
