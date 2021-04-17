---
description: Указывает время окончания презентации.
ms.assetid: c1022538-ea9f-41e9-9075-c106e8b16b7b
title: Атрибут MF_TOPONODE_MEDIASTOP (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a5b763d1d5adabc520900dde6839d1599ddcb3d
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713289"
---
# <a name="mf_toponode_mediastop-attribute"></a><span data-ttu-id="d5e69-103">\_Атрибут MF топоноде \_ медиастоп</span><span class="sxs-lookup"><span data-stu-id="d5e69-103">MF\_TOPONODE\_MEDIASTOP attribute</span></span>

<span data-ttu-id="d5e69-104">Указывает время окончания презентации.</span><span class="sxs-lookup"><span data-stu-id="d5e69-104">Specifies the stop time of the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="d5e69-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="d5e69-105">Data type</span></span>

<span data-ttu-id="d5e69-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="d5e69-106">**UINT64**</span></span>

<span data-ttu-id="d5e69-107">Рассматривать как значение **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="d5e69-107">Treat as a **LONGLONG** value.</span></span>

## <a name="getset"></a><span data-ttu-id="d5e69-108">Get/Set</span><span class="sxs-lookup"><span data-stu-id="d5e69-108">Get/set</span></span>

<span data-ttu-id="d5e69-109">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="d5e69-109">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="d5e69-110">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="d5e69-110">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="d5e69-111">Применяется к</span><span class="sxs-lookup"><span data-stu-id="d5e69-111">Applies to</span></span>

[<span data-ttu-id="d5e69-112">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="d5e69-112">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a><span data-ttu-id="d5e69-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="d5e69-113">Remarks</span></span>

<span data-ttu-id="d5e69-114">Этот атрибут задает позицию в источнике, в которой воспроизведение останавливается в единицах с 100-наносекундных относительных загрузок относительно начала источника.</span><span class="sxs-lookup"><span data-stu-id="d5e69-114">This attribute specifies the position in the source where playback stops, in 100-nanosecond units, relative to the start the source.</span></span> <span data-ttu-id="d5e69-115">Если атрибут не задан, воспроизведение останавливается в конце источника.</span><span class="sxs-lookup"><span data-stu-id="d5e69-115">If the attribute is not set, playback stops at the end of the source.</span></span> <span data-ttu-id="d5e69-116">Например, чтобы прерывать воспроизведение с 5-секундным отметкой, установите для этого атрибута значение 50000000.</span><span class="sxs-lookup"><span data-stu-id="d5e69-116">For example, to stop playback at the 5-second mark, set this attribute to 50000000.</span></span> <span data-ttu-id="d5e69-117">Задайте атрибут для исходных узлов в топологии (узлы с типом, равным **MF \_ \_ саурцестреам \_ node**).</span><span class="sxs-lookup"><span data-stu-id="d5e69-117">Set the attribute on the source nodes in the topology (nodes with type equal to **MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="d5e69-118">Задайте атрибут перед вызовом [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="d5e69-118">Set the attribute before calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

> [!Note]  
> <span data-ttu-id="d5e69-119">Если вы вручную вставили декодер в топологию, необходимо также задать значение [MF \_ топоноде \_ Маркин \_ здесь](mf-toponode-markin-here-attribute.md) и [MF \_ топоноде \_ отметить \_ здесь](mf-toponode-markout-here-attribute.md) атрибуты в узле декодера.</span><span class="sxs-lookup"><span data-stu-id="d5e69-119">If you manually insert a decoder into the topology, you must also set the [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) and [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) attributes on the decoder node.</span></span>

 

<span data-ttu-id="d5e69-120">После установки топологии Установка этого атрибута не оказывает никакого влияния.</span><span class="sxs-lookup"><span data-stu-id="d5e69-120">After the topology is set, setting this attribute has no effect.</span></span>

<span data-ttu-id="d5e69-121">Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="d5e69-121">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="d5e69-122">Однако отрицательные значения не имеют смысла.</span><span class="sxs-lookup"><span data-stu-id="d5e69-122">However, negative values are not meaningful.</span></span>

<span data-ttu-id="d5e69-123">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="d5e69-123">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5e69-124">Требования</span><span class="sxs-lookup"><span data-stu-id="d5e69-124">Requirements</span></span>



| <span data-ttu-id="d5e69-125">Требование</span><span class="sxs-lookup"><span data-stu-id="d5e69-125">Requirement</span></span> | <span data-ttu-id="d5e69-126">Значение</span><span class="sxs-lookup"><span data-stu-id="d5e69-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="d5e69-127">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="d5e69-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d5e69-128">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d5e69-128">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d5e69-129">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="d5e69-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d5e69-130">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d5e69-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="d5e69-131">Header</span><span class="sxs-lookup"><span data-stu-id="d5e69-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="d5e69-132"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="d5e69-132"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d5e69-133">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="d5e69-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5e69-134">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d5e69-134">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="d5e69-135">Время представления последовательности</span><span class="sxs-lookup"><span data-stu-id="d5e69-135">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="d5e69-136">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="d5e69-136">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="d5e69-137">**MF \_ топоноде \_ медиастарт**</span><span class="sxs-lookup"><span data-stu-id="d5e69-137">**MF\_TOPONODE\_MEDIASTART**</span></span>](mf-toponode-mediastart-attribute.md)
</dt> </dl>

 

 




