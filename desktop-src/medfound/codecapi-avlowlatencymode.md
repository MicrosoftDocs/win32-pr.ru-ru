---
description: Включает режим с малой задержкой в коде.
ms.assetid: 15E8FF6F-AD8C-436F-B3C0-5062B1F86E32
title: Свойство CODECAPI_AVLowLatencyMode (Кодекапи. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5be7e23a29e9dd5f88f7a96e6c32fd42b68a7204
ms.sourcegitcommit: adba238660d8a5f4fe98fc6f5d105d56aac3a400
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/09/2021
ms.locfileid: "111826908"
---
# <a name="codecapi_avlowlatencymode-property"></a><span data-ttu-id="db814-103">КОДЕКАПИ \_ авловлатенцимоде, свойство</span><span class="sxs-lookup"><span data-stu-id="db814-103">CODECAPI\_AVLowLatencyMode property</span></span>

<span data-ttu-id="db814-104">Включает режим с малой задержкой в коде.</span><span class="sxs-lookup"><span data-stu-id="db814-104">Enables low-latency mode in a codec.</span></span>

## <a name="data-type"></a><span data-ttu-id="db814-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="db814-105">Data type</span></span>

<span data-ttu-id="db814-106">**ulong** (**\_ логическое значение VT**)</span><span class="sxs-lookup"><span data-stu-id="db814-106">**ULONG** (**VT\_BOOL**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="db814-107">GUID свойства</span><span class="sxs-lookup"><span data-stu-id="db814-107">Property GUID</span></span>

<span data-ttu-id="db814-108">**КОДЕКАПИ \_ авловлатенцимоде**</span><span class="sxs-lookup"><span data-stu-id="db814-108">**CODECAPI\_AVLowLatencyMode**</span></span>

## <a name="property-value"></a><span data-ttu-id="db814-109">Значение свойства</span><span class="sxs-lookup"><span data-stu-id="db814-109">Property value</span></span>

<span data-ttu-id="db814-110">Если значение равно нулю, режим с низкой задержкой включен.</span><span class="sxs-lookup"><span data-stu-id="db814-110">If the value is nonzero, low-latency mode is enabled.</span></span> <span data-ttu-id="db814-111">Если значение равно нулю, режим с низкой задержкой отключен.</span><span class="sxs-lookup"><span data-stu-id="db814-111">If the value is zero, low-latency mode is disabled.</span></span>

## <a name="remarks"></a><span data-ttu-id="db814-112">Remarks</span><span class="sxs-lookup"><span data-stu-id="db814-112">Remarks</span></span>

<span data-ttu-id="db814-113">Это свойство применяется как к кодировщикам, так и к декодерам.</span><span class="sxs-lookup"><span data-stu-id="db814-113">This property applies to both encoders and decoders.</span></span>

<span data-ttu-id="db814-114">Режим с низкой задержкой полезен для обмена данными в режиме реального времени или для записи в активное время, когда задержка должна быть минимальна.</span><span class="sxs-lookup"><span data-stu-id="db814-114">Low-latency mode is useful for real-time communications or live capture, when latency should be minimized.</span></span> <span data-ttu-id="db814-115">Однако режим с низкой задержкой также может уменьшить качество декодирования или кодировки.</span><span class="sxs-lookup"><span data-stu-id="db814-115">However, low-latency mode might also reduce the decoding or encoding quality.</span></span>

<span data-ttu-id="db814-116">Предполагается, что кодировщик не добавляет какую-либо задержку выборки в результате изменения порядка кадров в процессе кодирования, и один образец ввода должен создать один выходной пример.</span><span class="sxs-lookup"><span data-stu-id="db814-116">The encoder is expected to not add any sample delay due to frame reordering in encoding process, and one input sample shall produce one output sample.</span></span> <span data-ttu-id="db814-117">B. срезы и кадры могут присутствовать, если они не переупорядочивают кадры в кодировщике.</span><span class="sxs-lookup"><span data-stu-id="db814-117">B slices/frames can be present as long as they do not introduce any frame re-ordering in the encoder.</span></span>

> [!WARNING] 
> <span data-ttu-id="db814-118">В текущей реализации декодер Media Foundation H. 264 использует для этого свойства тип **VT_UI4** .</span><span class="sxs-lookup"><span data-stu-id="db814-118">In the current implementation, the Media Foundation H.264 decoder uses the type **VT_UI4** for this property.</span></span> <span data-ttu-id="db814-119">Все другие реализации, включая кодировщик H. 264, используют тип **VT_BOOL**.</span><span class="sxs-lookup"><span data-stu-id="db814-119">All other implementations, including the H.264 encoder, use the type **VT_BOOL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="db814-120">Требования</span><span class="sxs-lookup"><span data-stu-id="db814-120">Requirements</span></span>



| <span data-ttu-id="db814-121">Требование</span><span class="sxs-lookup"><span data-stu-id="db814-121">Requirement</span></span> | <span data-ttu-id="db814-122">Значение</span><span class="sxs-lookup"><span data-stu-id="db814-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="db814-123">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="db814-123">Minimum supported client</span></span><br/> | <span data-ttu-id="db814-124">\[Приложения UWP для классических приложений Windows 8 \|\]</span><span class="sxs-lookup"><span data-stu-id="db814-124">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                     |
| <span data-ttu-id="db814-125">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="db814-125">Minimum supported server</span></span><br/> | <span data-ttu-id="db814-126">\[Приложения UWP для классических приложений Windows Server 2012 \|\]</span><span class="sxs-lookup"><span data-stu-id="db814-126">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="db814-127">Заголовок</span><span class="sxs-lookup"><span data-stu-id="db814-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="db814-128"><dt>Кодекапи. h</dt></span><span class="sxs-lookup"><span data-stu-id="db814-128"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db814-129">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="db814-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db814-130">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="db814-130">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="db814-131">**икодекапи**</span><span class="sxs-lookup"><span data-stu-id="db814-131">**ICodecAPI**</span></span>](/windows/desktop/api/strmif/nn-strmif-icodecapi)
</dt> </dl>

 

