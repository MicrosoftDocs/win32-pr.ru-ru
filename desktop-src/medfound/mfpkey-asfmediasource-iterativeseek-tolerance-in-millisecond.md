---
description: Задает допуск (в миллисекундах), который используется, когда источник мультимедиа ASF выполняет итеративное Поиск.
ms.assetid: 3ee4410f-857c-4978-a308-87decfba0e2f
title: Свойство MFPKEY_ASFMediaSource_IterativeSeek_Tolerance_In_MilliSecond (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f4190d9f87d906a701908dfc17b61633204fe8a2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105693858"
---
# <a name="mfpkey_asfmediasource_iterativeseek_tolerance_in_millisecond-property"></a><span data-ttu-id="f617b-103">МФПКЭЙ \_ асфмедиасаурце \_ итеративесик \_ погрешность \_ в \_ миллисекундах, свойство</span><span class="sxs-lookup"><span data-stu-id="f617b-103">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond property</span></span>

<span data-ttu-id="f617b-104">Задает допуск (в миллисекундах), который используется, когда источник мультимедиа ASF выполняет итеративное Поиск.</span><span class="sxs-lookup"><span data-stu-id="f617b-104">Sets the tolerance, in milliseconds, that is used when the ASF media source performs iterative seeking.</span></span>



<span data-ttu-id="f617b-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="f617b-105">Data type</span></span>

<span data-ttu-id="f617b-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="f617b-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="f617b-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="f617b-107">PROPVARIANT member</span></span>

<span data-ttu-id="f617b-108">**ULONG**</span><span class="sxs-lookup"><span data-stu-id="f617b-108">**ULONG**</span></span>

<span data-ttu-id="f617b-109">VT \_ UI4</span><span class="sxs-lookup"><span data-stu-id="f617b-109">VT\_UI4</span></span>

<span data-ttu-id="f617b-110">**улвал**</span><span class="sxs-lookup"><span data-stu-id="f617b-110">**ulVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="f617b-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="f617b-111">Remarks</span></span>

<span data-ttu-id="f617b-112">Это свойство используется для настройки источника мультимедиа ASF.</span><span class="sxs-lookup"><span data-stu-id="f617b-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="f617b-113">Чтобы задать свойство, передайте указатель **ипропертисторе** в сопоставитель источника.</span><span class="sxs-lookup"><span data-stu-id="f617b-113">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="f617b-114">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="f617b-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="f617b-115">Это свойство применяется, только если включено итеративное Поиск.</span><span class="sxs-lookup"><span data-stu-id="f617b-115">This property applies only when iterative seeking is enabled.</span></span> <span data-ttu-id="f617b-116">Дополнительные сведения см. в разделе [мфпкэй \_ асфмедиасаурце \_ итеративесикифноиндекс](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span><span class="sxs-lookup"><span data-stu-id="f617b-116">For more information, see [MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex](mfpkey-asfmediasource-iterativeseekifnoindex.md).</span></span>

<span data-ttu-id="f617b-117">Алгоритм итеративного поиска останавливается, если находит пакет, расстояние от которого до времени поиска находится в пределах указанного допуска.</span><span class="sxs-lookup"><span data-stu-id="f617b-117">The iterative seeking algorithm halts if it finds a packet whose distance from the seek time is within the specified tolerance.</span></span> <span data-ttu-id="f617b-118">Значение по умолчанию — 8000 миллисекунд.</span><span class="sxs-lookup"><span data-stu-id="f617b-118">The default value is 8000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="f617b-119">Требования</span><span class="sxs-lookup"><span data-stu-id="f617b-119">Requirements</span></span>



| <span data-ttu-id="f617b-120">Требование</span><span class="sxs-lookup"><span data-stu-id="f617b-120">Requirement</span></span> | <span data-ttu-id="f617b-121">Значение</span><span class="sxs-lookup"><span data-stu-id="f617b-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f617b-122">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="f617b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f617b-123">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="f617b-123">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="f617b-124">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="f617b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f617b-125">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="f617b-125">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="f617b-126">Header</span><span class="sxs-lookup"><span data-stu-id="f617b-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f617b-127"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="f617b-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f617b-128">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="f617b-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f617b-129">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="f617b-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




