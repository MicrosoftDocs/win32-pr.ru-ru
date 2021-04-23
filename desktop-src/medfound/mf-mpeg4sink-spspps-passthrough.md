---
description: Указывает, отфильтровывает ли приемник файлов MPEG-4 набор параметров последовательности (SPS) и набор параметров изображения (PPS) Налус.
ms.assetid: B2574BE5-6334-4ED2-A008-86326CDC13B8
title: Атрибут MF_MPEG4SINK_SPSPPS_PASSTHROUGH (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3c02f4f1cdcac17a104b5061c8899c92e0ad824
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811855"
---
# <a name="mf_mpeg4sink_spspps_passthrough-attribute"></a><span data-ttu-id="2864d-103">\_ \_ \_ Атрибут транзитного MPEG4SINK спсппс MF</span><span class="sxs-lookup"><span data-stu-id="2864d-103">MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute</span></span>

<span data-ttu-id="2864d-104">Указывает, отфильтровывает ли [**приемник файлов MPEG-4**](mpeg-4-file-sink.md) набор параметров последовательности (SPS) и набор параметров изображения (PPS) налус.</span><span class="sxs-lookup"><span data-stu-id="2864d-104">Specifies whether the [**MPEG-4 File Sink**](mpeg-4-file-sink.md) filters out sequence parameter set (SPS) and picture parameter set (PPS) NALUs.</span></span>

## <a name="data-type"></a><span data-ttu-id="2864d-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="2864d-105">Data type</span></span>

<span data-ttu-id="2864d-106">**Bool** , сохраненный как **UINT32**</span><span class="sxs-lookup"><span data-stu-id="2864d-106">**BOOL** stored as **UINT32**</span></span>

## <a name="applies-to"></a><span data-ttu-id="2864d-107">Применяется к</span><span class="sxs-lookup"><span data-stu-id="2864d-107">Applies to</span></span>

[<span data-ttu-id="2864d-108">**имфмедиасинк**</span><span class="sxs-lookup"><span data-stu-id="2864d-108">**IMFMediaSink**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasink)

## <a name="remarks"></a><span data-ttu-id="2864d-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="2864d-109">Remarks</span></span>

<span data-ttu-id="2864d-110">[**Приемник файлов MPEG-4**](mpeg-4-file-sink.md) записывает параметры SPS и PPS в поле Описание образца файла MP4.</span><span class="sxs-lookup"><span data-stu-id="2864d-110">The [**MPEG-4 File Sink**](mpeg-4-file-sink.md) writes the SPS and PPS parameters into the sample description box of the MP4 file.</span></span> <span data-ttu-id="2864d-111">По умолчанию он фильтрует Налус SPS и PPS из видеопотока.</span><span class="sxs-lookup"><span data-stu-id="2864d-111">By default, it filters out the SPS and PPS NALUs from the video stream.</span></span> <span data-ttu-id="2864d-112">Чтобы переопределить это поведение, присвойте \_ \_ \_ атрибуту passthrough MPEG4SINK Спсппс транзита **значение true**.</span><span class="sxs-lookup"><span data-stu-id="2864d-112">To override this behavior, set the MF\_MPEG4SINK\_SPSPPS\_PASSTHROUGH attribute to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="2864d-113">Требования</span><span class="sxs-lookup"><span data-stu-id="2864d-113">Requirements</span></span>



| <span data-ttu-id="2864d-114">Требование</span><span class="sxs-lookup"><span data-stu-id="2864d-114">Requirement</span></span> | <span data-ttu-id="2864d-115">Значение</span><span class="sxs-lookup"><span data-stu-id="2864d-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="2864d-116">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="2864d-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2864d-117">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="2864d-117">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="2864d-118">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="2864d-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2864d-119">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="2864d-119">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="2864d-120">Header</span><span class="sxs-lookup"><span data-stu-id="2864d-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="2864d-121"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="2864d-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2864d-122">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="2864d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2864d-123">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2864d-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




