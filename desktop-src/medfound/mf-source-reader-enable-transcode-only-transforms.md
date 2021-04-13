---
description: Позволяет модулю чтения исходного кода использовать Media Foundation преобразований (МФТС), оптимизированных для перекодирования.
ms.assetid: 9463EB8C-2CA3-4F8F-8A2A-B1292879DD1B
title: Атрибут MF_SOURCE_READER_ENABLE_TRANSCODE_ONLY_TRANSFORMS (Мфреадврите. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04a9559254216a102613d97824601c004c71bfd2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541346"
---
# <a name="mf_source_reader_enable_transcode_only_transforms-attribute"></a><span data-ttu-id="9457d-103">MF \_ исходный \_ считыватель \_ включить \_ \_ \_ атрибут преобразования "только преобразование кода"</span><span class="sxs-lookup"><span data-stu-id="9457d-103">MF\_SOURCE\_READER\_ENABLE\_TRANSCODE\_ONLY\_TRANSFORMS attribute</span></span>

<span data-ttu-id="9457d-104">Позволяет [модулю чтения исходного кода](source-reader.md) использовать Media Foundation преобразований (МФТС), оптимизированных для перекодирования.</span><span class="sxs-lookup"><span data-stu-id="9457d-104">Enables the [Source Reader](source-reader.md) to use Media Foundation transforms (MFTs) that are optimized for transcoding.</span></span>

## <a name="data-type"></a><span data-ttu-id="9457d-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="9457d-105">Data type</span></span>

<span data-ttu-id="9457d-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="9457d-106">**UINT32**</span></span>

<span data-ttu-id="9457d-107">Рассматривать как логическое значение.</span><span class="sxs-lookup"><span data-stu-id="9457d-107">Treat as Boolean.</span></span>

## <a name="remarks"></a><span data-ttu-id="9457d-108">Комментарии</span><span class="sxs-lookup"><span data-stu-id="9457d-108">Remarks</span></span>

<span data-ttu-id="9457d-109">Некоторые МФТС, особенно декодеры, оптимизированы для перекодирования, а не для воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="9457d-109">Some MFTs, particularly decoders, are optimized for transcoding rather than playback.</span></span> <span data-ttu-id="9457d-110">По умолчанию модуль чтения исходного кода не будет загружать такие преобразования.</span><span class="sxs-lookup"><span data-stu-id="9457d-110">By default, the Source Reader will not load such transforms.</span></span> <span data-ttu-id="9457d-111">Установите для этого атрибута **значение true** , если вы хотите использовать перекодирование МФТС с модулем чтения исходного кода.</span><span class="sxs-lookup"><span data-stu-id="9457d-111">Set this attribute to **TRUE** if you want to use transcoding MFTs with the Source Reader.</span></span>

<span data-ttu-id="9457d-112">Приложение может установить этот атрибут, если он не обрабатывает данные в режиме реального времени (для перекодирования или аналогичных сценариев).</span><span class="sxs-lookup"><span data-stu-id="9457d-112">An application might set this attribute if it does not process the data in real time (for transcoding or similar scenarios).</span></span> <span data-ttu-id="9457d-113">В противном случае для воспроизведения в режиме реального времени используйте поведение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9457d-113">Otherwise, for real-time playback, use the default behavior.</span></span>

<span data-ttu-id="9457d-114">На внутреннем уровне этот атрибут заставляет модуль чтения исходного кода включить **флаг \_ перечисления MFT \_ флага Enum \_ \_ только** при вызове [**мфтенумекс**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span><span class="sxs-lookup"><span data-stu-id="9457d-114">Internally, this attribute causes the Source Reader to include the **MFT\_ENUM\_FLAG\_TRANSCODE\_ONLY** flag when it calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

## <a name="requirements"></a><span data-ttu-id="9457d-115">Требования</span><span class="sxs-lookup"><span data-stu-id="9457d-115">Requirements</span></span>



| <span data-ttu-id="9457d-116">Требование</span><span class="sxs-lookup"><span data-stu-id="9457d-116">Requirement</span></span> | <span data-ttu-id="9457d-117">Значение</span><span class="sxs-lookup"><span data-stu-id="9457d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9457d-118">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="9457d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="9457d-119">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="9457d-119">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                        |
| <span data-ttu-id="9457d-120">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="9457d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="9457d-121">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="9457d-121">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                              |
| <span data-ttu-id="9457d-122">Header</span><span class="sxs-lookup"><span data-stu-id="9457d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="9457d-123"><dt>Мфреадврите. h</dt></span><span class="sxs-lookup"><span data-stu-id="9457d-123"><dt>Mfreadwrite.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9457d-124">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="9457d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9457d-125">Алфавитный список атрибутов Media Foundation</span><span class="sxs-lookup"><span data-stu-id="9457d-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="9457d-126">Модуль чтения исходного кода</span><span class="sxs-lookup"><span data-stu-id="9457d-126">Source Reader</span></span>](source-reader.md)
</dt> </dl>

 

 




