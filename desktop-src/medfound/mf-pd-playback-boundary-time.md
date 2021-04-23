---
description: Сохраняет время (в 100-наносекундах единицах), начиная с которого должна начинаться презентация, относительно начала источника мультимедиа.
ms.assetid: 7a3dddad-067b-46af-9ed9-4ccc65f9d772
title: Атрибут MF_PD_PLAYBACK_BOUNDARY_TIME (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22abadb4e0148a2079a9a7387e43599f4f79b8bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104081508"
---
# <a name="mf_pd_playback_boundary_time-attribute"></a><span data-ttu-id="66e97-103">\_ \_ \_ Атрибут времени границы воспроизведения MF PD \_</span><span class="sxs-lookup"><span data-stu-id="66e97-103">MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute</span></span>

<span data-ttu-id="66e97-104">Сохраняет время (в 100-наносекундах единицах), начиная с которого должна начинаться презентация, относительно начала источника мультимедиа.</span><span class="sxs-lookup"><span data-stu-id="66e97-104">Stores the time (in 100-nanoseconds units) at which the presentation must begin, relative to the start of the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="66e97-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="66e97-105">Data type</span></span>

<span data-ttu-id="66e97-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="66e97-106">**UINT64**</span></span>

## <a name="getset"></a><span data-ttu-id="66e97-107">Get/Set</span><span class="sxs-lookup"><span data-stu-id="66e97-107">Get/set</span></span>

<span data-ttu-id="66e97-108">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="66e97-108">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="66e97-109">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="66e97-109">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="66e97-110">Применяется к</span><span class="sxs-lookup"><span data-stu-id="66e97-110">Applies to</span></span>

[<span data-ttu-id="66e97-111">**имфпресентатиондескриптор**</span><span class="sxs-lookup"><span data-stu-id="66e97-111">**IMFPresentationDescriptor**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfpresentationdescriptor)

## <a name="remarks"></a><span data-ttu-id="66e97-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="66e97-112">Remarks</span></span>

<span data-ttu-id="66e97-113">\_ \_ \_ Атрибут времени границы воспроизведения MF PD \_ необязателен для источников мультимедиа в списке воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="66e97-113">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is optional for media sources in a playlist.</span></span> <span data-ttu-id="66e97-114">Это значение указывает фактическое время начала презентации.</span><span class="sxs-lookup"><span data-stu-id="66e97-114">This value indicates the actual start time of the presentation.</span></span> <span data-ttu-id="66e97-115">Рассмотрим список воспроизведения, включающий в последовательность мультимедийные источники *Element1*, *Element2* и *Element3* .</span><span class="sxs-lookup"><span data-stu-id="66e97-115">Consider a playlist that includes media sources *Element1*, *Element2*, and *Element3* in a sequence.</span></span> <span data-ttu-id="66e97-116">в течение 15 секунд после запуска *Element1* происходит динамическое изменение потока.</span><span class="sxs-lookup"><span data-stu-id="66e97-116">15 seconds after *Element1* starts playing, a dynamic stream change occurs.</span></span> <span data-ttu-id="66e97-117">Новый поток должен начать воспроизведение презентации в течение 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="66e97-117">The new stream must start playing 15 seconds into the presentation.</span></span> <span data-ttu-id="66e97-118">Однако для нового потока ключевой кадр, ближайший к времени презентации, составляет 15 секунд, в течение 12 секунд.</span><span class="sxs-lookup"><span data-stu-id="66e97-118">However, the keyframe nearest the presentation time of 15 seconds is at 12 seconds for the new stream.</span></span> <span data-ttu-id="66e97-119">Чтобы начать новую презентацию в течение 15 секунд, требуется Маркин, чтобы декодированные образцы удалялись с 12 секунд до 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="66e97-119">To start the new presentation at 15 seconds, a markin is required so that the decoded samples are dropped from 12 seconds to 15 seconds.</span></span>

<span data-ttu-id="66e97-120">Перед переходом в источнике мультимедиа вызывается событие [меневпресентатион](menewpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="66e97-120">Before the transition, the [MENewPresentation](menewpresentation.md) event is raised by the media source.</span></span> <span data-ttu-id="66e97-121">Он возвращает дескриптор представления, содержащий атрибут [ \_ \_ \_ \_ идентификатора элемента воспроизведения MF PD](mf-pd-playback-element-id.md) для *Element1*.</span><span class="sxs-lookup"><span data-stu-id="66e97-121">This returns the presentation descriptor that contains the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute for *Element1*.</span></span> <span data-ttu-id="66e97-122">Кроме того, он содержит \_ \_ \_ атрибут времени пограничного воспроизведения MF PD \_ , значение которого равно 15 секундам, чтобы указать время перехода.</span><span class="sxs-lookup"><span data-stu-id="66e97-122">Additionally, it contains the MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute that is set to 15 seconds to indicate the time when the transition occurred.</span></span> <span data-ttu-id="66e97-123">Источник мультимедиа выполняет Маркин через 15 секунд после декодирования, что предотвращает отображение кадров от 12 секунд до 15 секунд.</span><span class="sxs-lookup"><span data-stu-id="66e97-123">The media source performs the markin at 15 seconds after decoding, which prevents the frames from 12 seconds to 15 seconds from being displayed.</span></span>

<span data-ttu-id="66e97-124">Это значение влияет только на Маркин время и не влияет на то, как сеанс мультимедиа корректирует отметки времени.</span><span class="sxs-lookup"><span data-stu-id="66e97-124">This value affects only markin time and does not affect how the Media Session adjusts time stamps.</span></span> <span data-ttu-id="66e97-125">Этот атрибут игнорируется, если источник мультимедиа не указывает атрибут [ \_ \_ \_ \_ идентификатора элемента воспроизведения MF PD](mf-pd-playback-element-id.md) , что эта презентация является тем же элементом воспроизведения, что и Предыдущая.</span><span class="sxs-lookup"><span data-stu-id="66e97-125">This attribute is ignored unless the media source indicates through the [MF\_PD\_PLAYBACK\_ELEMENT\_ID](mf-pd-playback-element-id.md) attribute that this presentation is the same playback element as the previous one.</span></span>

<span data-ttu-id="66e97-126">\_ \_ \_ Атрибут времени границы воспроизведения MF PD \_ аналогичен атрибуту [MF \_ топоноде \_ медиастарт](mf-toponode-mediastart-attribute.md) , заданному в узле Topology.</span><span class="sxs-lookup"><span data-stu-id="66e97-126">The MF\_PD\_PLAYBACK\_BOUNDARY\_TIME attribute is similar to the [MF\_TOPONODE\_MEDIASTART](mf-toponode-mediastart-attribute.md) attribute that is set on the topology node.</span></span> <span data-ttu-id="66e97-127">Для приложений, выполняющихся в Windows Vista, источники мультимедиа, реализующие [**имфмедиасаурцетопологипровидер**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) , должны использовать **MF \_ топоноде \_ МЕДИАСТАРТ** вместо \_ \_ \_ времени ожидания воспроизведения MF PD \_ .</span><span class="sxs-lookup"><span data-stu-id="66e97-127">For applications running on Windows Vista, media sources that implement [**IMFMediaSourceTopologyProvider**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasourcetopologyprovider) should use **MF\_TOPONODE\_MEDIASTART** instead of MF\_PD\_PLAYBACK\_BOUNDARY\_TIME.</span></span>

<span data-ttu-id="66e97-128">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="66e97-128">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="66e97-129">Требования</span><span class="sxs-lookup"><span data-stu-id="66e97-129">Requirements</span></span>



| <span data-ttu-id="66e97-130">Требование</span><span class="sxs-lookup"><span data-stu-id="66e97-130">Requirement</span></span> | <span data-ttu-id="66e97-131">Значение</span><span class="sxs-lookup"><span data-stu-id="66e97-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="66e97-132">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="66e97-132">Minimum supported client</span></span><br/> | <span data-ttu-id="66e97-133">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="66e97-133">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="66e97-134">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="66e97-134">Minimum supported server</span></span><br/> | <span data-ttu-id="66e97-135">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="66e97-135">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="66e97-136">Header</span><span class="sxs-lookup"><span data-stu-id="66e97-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="66e97-137"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="66e97-137"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66e97-138">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="66e97-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66e97-139">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="66e97-139">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="66e97-140">Атрибуты дескриптора представления</span><span class="sxs-lookup"><span data-stu-id="66e97-140">Presentation Descriptor Attributes</span></span>](presentation-descriptor-attributes.md)
</dt> </dl>

 

 




