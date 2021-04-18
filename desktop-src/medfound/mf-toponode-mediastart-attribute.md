---
description: Указывает время начала презентации.
ms.assetid: a2a64cac-0dc1-41b0-b59c-a477c7304ba1
title: Атрибут MF_TOPONODE_MEDIASTART (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1ab00727cc328bfd6ba780050160fb21eecbb96f
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105713277"
---
# <a name="mf_toponode_mediastart-attribute"></a><span data-ttu-id="27640-103">\_Атрибут MF топоноде \_ медиастарт</span><span class="sxs-lookup"><span data-stu-id="27640-103">MF\_TOPONODE\_MEDIASTART attribute</span></span>

<span data-ttu-id="27640-104">Указывает время начала презентации.</span><span class="sxs-lookup"><span data-stu-id="27640-104">Specifies the start time of the presentation.</span></span>

## <a name="data-type"></a><span data-ttu-id="27640-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="27640-105">Data type</span></span>

<span data-ttu-id="27640-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="27640-106">**UINT64**</span></span>

<span data-ttu-id="27640-107">Рассматривать как значение **лонглонг** .</span><span class="sxs-lookup"><span data-stu-id="27640-107">Treat as a **LONGLONG** value.</span></span>

## <a name="getset"></a><span data-ttu-id="27640-108">Get/Set</span><span class="sxs-lookup"><span data-stu-id="27640-108">Get/set</span></span>

<span data-ttu-id="27640-109">Чтобы получить этот атрибут, вызовите [**имфаттрибутес:: UInt64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span><span class="sxs-lookup"><span data-stu-id="27640-109">To get this attribute, call [**IMFAttributes::GetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64).</span></span>

<span data-ttu-id="27640-110">Чтобы задать этот атрибут, вызовите [**имфаттрибутес:: SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span><span class="sxs-lookup"><span data-stu-id="27640-110">To set this attribute, call [**IMFAttributes::SetUINT64**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64).</span></span>

## <a name="applies-to"></a><span data-ttu-id="27640-111">Применяется к</span><span class="sxs-lookup"><span data-stu-id="27640-111">Applies to</span></span>

[<span data-ttu-id="27640-112">**имфтопологиноде**</span><span class="sxs-lookup"><span data-stu-id="27640-112">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)

## <a name="remarks"></a><span data-ttu-id="27640-113">Комментарии</span><span class="sxs-lookup"><span data-stu-id="27640-113">Remarks</span></span>

<span data-ttu-id="27640-114">Этот атрибут указывает позицию в источнике, с которого начинается воспроизведение, в единицах 100-наносекундных относительно начала источника.</span><span class="sxs-lookup"><span data-stu-id="27640-114">This attribute specifies the position in the source where playback starts, in 100-nanosecond units, relative to the start the source.</span></span> <span data-ttu-id="27640-115">Если атрибут не задан, воспроизведение начинается с нуля (начало файла).</span><span class="sxs-lookup"><span data-stu-id="27640-115">If the attribute is not set, playback starts at zero (the start of the file).</span></span> <span data-ttu-id="27640-116">Например, чтобы начать воспроизведение с 5-секундной метки, установите для этого атрибута значение 50000000.</span><span class="sxs-lookup"><span data-stu-id="27640-116">For example, to start playback at the 5-second mark, set this attribute to 50000000.</span></span> <span data-ttu-id="27640-117">Задайте атрибут для исходных узлов в топологии (узлы с типом, равным **MF \_ \_ саурцестреам \_ node**).</span><span class="sxs-lookup"><span data-stu-id="27640-117">Set the attribute on the source nodes in the topology (nodes with type equal to **MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="27640-118">Задайте атрибут перед вызовом [**имфмедиасессион:: сеттопологи**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span><span class="sxs-lookup"><span data-stu-id="27640-118">Set the attribute before calling [**IMFMediaSession::SetTopology**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology).</span></span>

> [!Note]  
> <span data-ttu-id="27640-119">Если вы вручную вставили декодер в топологию, необходимо также задать значение [MF \_ топоноде \_ Маркин \_ здесь](mf-toponode-markin-here-attribute.md) и [MF \_ топоноде \_ отметить \_ здесь](mf-toponode-markout-here-attribute.md) атрибуты в узле декодера.</span><span class="sxs-lookup"><span data-stu-id="27640-119">If you manually insert a decoder into the topology, you must also set the [MF\_TOPONODE\_MARKIN\_HERE](mf-toponode-markin-here-attribute.md) and [MF\_TOPONODE\_MARKOUT\_HERE](mf-toponode-markout-here-attribute.md) attributes on the decoder node.</span></span>

 

<span data-ttu-id="27640-120">Этот атрибут имеет значение со знаком, хотя оно хранится в виде **UINT64**.</span><span class="sxs-lookup"><span data-stu-id="27640-120">This attribute is a signed value, although it is stored as a **UINT64**.</span></span> <span data-ttu-id="27640-121">Однако отрицательные значения не имеют смысла.</span><span class="sxs-lookup"><span data-stu-id="27640-121">However, negative values are not meaningful.</span></span>

<span data-ttu-id="27640-122">Константа GUID для этого атрибута экспортируется из мфууид. lib.</span><span class="sxs-lookup"><span data-stu-id="27640-122">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="27640-123">Требования</span><span class="sxs-lookup"><span data-stu-id="27640-123">Requirements</span></span>



| <span data-ttu-id="27640-124">Требование</span><span class="sxs-lookup"><span data-stu-id="27640-124">Requirement</span></span> | <span data-ttu-id="27640-125">Значение</span><span class="sxs-lookup"><span data-stu-id="27640-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="27640-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="27640-126">Minimum supported client</span></span><br/> | <span data-ttu-id="27640-127">Только для \[ классических приложений Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="27640-127">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="27640-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="27640-128">Minimum supported server</span></span><br/> | <span data-ttu-id="27640-129">\[Только для настольных приложений Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="27640-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="27640-130">Header</span><span class="sxs-lookup"><span data-stu-id="27640-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="27640-131"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="27640-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27640-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="27640-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27640-133">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="27640-133">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="27640-134">Время представления последовательности</span><span class="sxs-lookup"><span data-stu-id="27640-134">Sequence Presentation Times</span></span>](sequence-presentation-times.md)
</dt> <dt>

[<span data-ttu-id="27640-135">Атрибуты узла топологии</span><span class="sxs-lookup"><span data-stu-id="27640-135">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="27640-136">**MF \_ топоноде \_ медиастоп**</span><span class="sxs-lookup"><span data-stu-id="27640-136">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)
</dt> </dl>

 

 




