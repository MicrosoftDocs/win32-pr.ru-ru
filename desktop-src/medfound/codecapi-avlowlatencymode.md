---
description: Включает режим с малой задержкой в коде.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: Свойство CODECAPI_AVLowLatencyMode (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f159045f6b40d531495338b1598c214926a59612
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105692073"
---
# <a name="codecapi_avlowlatencymode-property"></a><span data-ttu-id="f4c9e-103">КОДЕКАПИ \_ авловлатенцимоде, свойство</span><span class="sxs-lookup"><span data-stu-id="f4c9e-103">CODECAPI\_AVLowLatencyMode property</span></span>

<span data-ttu-id="f4c9e-104">Включает режим с малой задержкой в коде.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-104">Enables low-latency mode in a codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="f4c9e-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f4c9e-105">Data type</span></span>

<span data-ttu-id="f4c9e-106">**ulong** (**\_ логическое значение VT**)</span><span class="sxs-lookup"><span data-stu-id="f4c9e-106">**ULONG** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="f4c9e-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="f4c9e-107">Property GUID</span></span>

<span data-ttu-id="f4c9e-108">**КОДЕКАПИ \_ авловлатенцимоде**</span><span class="sxs-lookup"><span data-stu-id="f4c9e-108">**CODECAPI\_AVLowLatencyMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="f4c9e-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="f4c9e-109">Property value</span></span>

<span data-ttu-id="f4c9e-110">Если значение равно нулю, режим с низкой задержкой включен.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-110">If the value is nonzero, low-latency mode is enabled.</span></span> <span data-ttu-id="f4c9e-111">Если значение равно нулю, режим с низкой задержкой отключен.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-111">If the value is zero, low-latency mode is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="f4c9e-112">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f4c9e-112">Remarks</span></span>

<span data-ttu-id="f4c9e-113">Это свойство применяется как к кодировщикам, так и к декодерам.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-113">This property applies to both encoders and decoders.</span></span>

<span data-ttu-id="f4c9e-114">Режим с низкой задержкой полезен для обмена данными в режиме реального времени или для записи в активное время, когда задержка должна быть минимальна.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-114">Low-latency mode is useful for real-time communications or live capture, when latency should be minimized.</span></span> <span data-ttu-id="f4c9e-115">Однако режим с низкой задержкой также может уменьшить качество декодирования или кодировки.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-115">However, low-latency mode might also reduce the decoding or encoding quality.</span></span>

<span data-ttu-id="f4c9e-116">Предполагается, что кодировщик не добавляет какую-либо задержку выборки в результате изменения порядка кадров в процессе кодирования, и один образец ввода должен создать один выходной пример.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-116">The encoder is expected to not add any sample delay due to frame reordering in encoding process, and one input sample shall produce one output sample.</span></span> <span data-ttu-id="f4c9e-117">B. срезы и кадры могут присутствовать, если они не переупорядочивают кадры в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="f4c9e-117">B slices/frames can be present as long as they do not introduce any frame re-ordering in the encoder.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4c9e-118">Требования</span><span class="sxs-lookup"><span data-stu-id="f4c9e-118">Requirements</span></span>



| <span data-ttu-id="f4c9e-119">Требование</span><span class="sxs-lookup"><span data-stu-id="f4c9e-119">Requirement</span></span> | <span data-ttu-id="f4c9e-120">Значение</span><span class="sxs-lookup"><span data-stu-id="f4c9e-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f4c9e-121">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f4c9e-121">Minimum supported client</span></span><br/> | <span data-ttu-id="f4c9e-122">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="f4c9e-122">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="f4c9e-123">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f4c9e-123">Minimum supported server</span></span><br/> | <span data-ttu-id="f4c9e-124">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="f4c9e-124">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="f4c9e-125">Header</span><span class="sxs-lookup"><span data-stu-id="f4c9e-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4c9e-126"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4c9e-126"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4c9e-127">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f4c9e-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4c9e-128">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f4c9e-128">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="f4c9e-129">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="f4c9e-129">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

