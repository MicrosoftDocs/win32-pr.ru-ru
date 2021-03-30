---
description: Настраивает источник носителя ASF для использования итеративного поиска, если исходный файл не имеет индекса.
ms.assetid: 0dd6f202-cdbc-4a28-8907-5530a0a2141b
title: Свойство MFPKEY_ASFMediaSource_IterativeSeekIfNoIndex (Мфидл. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10cdc22f0b4f5490c7691cc40166cf929a16ba64
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "103820285"
---
# <a name="mfpkey_asfmediasource_iterativeseekifnoindex-property"></a><span data-ttu-id="904e7-103">МФПКЭЙ \_ асфмедиасаурце \_ итеративесикифноиндекс, свойство</span><span class="sxs-lookup"><span data-stu-id="904e7-103">MFPKEY\_ASFMediaSource\_IterativeSeekIfNoIndex property</span></span>

<span data-ttu-id="904e7-104">Настраивает источник носителя ASF для использования итеративного поиска, если исходный файл не имеет индекса.</span><span class="sxs-lookup"><span data-stu-id="904e7-104">Configures the ASF media source to use iterative seeking if the source file has no index.</span></span>



<span data-ttu-id="904e7-105">Тип данных</span><span class="sxs-lookup"><span data-stu-id="904e7-105">Data type</span></span>

<span data-ttu-id="904e7-106">Тип ПРОПВАРИАНТ (VT)</span><span class="sxs-lookup"><span data-stu-id="904e7-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="904e7-107">ПРОПВАРИАНТ, элемент</span><span class="sxs-lookup"><span data-stu-id="904e7-107">PROPVARIANT member</span></span>

<span data-ttu-id="904e7-108">**VARIANT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="904e7-108">**VARIANT\_BOOL**</span></span>

<span data-ttu-id="904e7-109">Логическое значение VT \_</span><span class="sxs-lookup"><span data-stu-id="904e7-109">VT\_BOOL</span></span>

<span data-ttu-id="904e7-110">**булвал**</span><span class="sxs-lookup"><span data-stu-id="904e7-110">**boolVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="904e7-111">Комментарии</span><span class="sxs-lookup"><span data-stu-id="904e7-111">Remarks</span></span>

<span data-ttu-id="904e7-112">Это свойство используется для настройки источника мультимедиа ASF.</span><span class="sxs-lookup"><span data-stu-id="904e7-112">Use this property to configure the ASF media source.</span></span> <span data-ttu-id="904e7-113">Чтобы задать свойство, передайте указатель **ипропертисторе** в *сопоставитель источника*.</span><span class="sxs-lookup"><span data-stu-id="904e7-113">To set the property, pass an **IPropertyStore** pointer to the *source resolver*.</span></span> <span data-ttu-id="904e7-114">Дополнительные сведения см. [в разделе Настройка источника мультимедиа](configuring-a-media-source.md).</span><span class="sxs-lookup"><span data-stu-id="904e7-114">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="904e7-115">*Итеративное Поиск* — это алгоритм поиска позиции в файле ASF без индекса.</span><span class="sxs-lookup"><span data-stu-id="904e7-115">*Iterative seeking* is an algorithm to find a position in an ASF file with no index.</span></span> <span data-ttu-id="904e7-116">Он использует ряд приближений, основанный на средней скорости, чтобы постепенно ближе к целевому времени поиска.</span><span class="sxs-lookup"><span data-stu-id="904e7-116">It uses a series of approximations, based on the average bit rate, to get progressively closer to the target seek time.</span></span> <span data-ttu-id="904e7-117">(Алгоритм аналогичен двоичному поиску.) Итеративное Поиск может занять больше времени, чем поиск по индексу, поэтому по умолчанию он отключен.</span><span class="sxs-lookup"><span data-stu-id="904e7-117">(The algorithm is similar to a binary search.) Iterative seeking can take longer than seeking by index, so it is disabled by default.</span></span>

<span data-ttu-id="904e7-118">Если задать это свойство, используйте следующие свойства, чтобы задать параметры поиска:</span><span class="sxs-lookup"><span data-stu-id="904e7-118">If you set this property, use the following properties to set the search parameters:</span></span>

-   [<span data-ttu-id="904e7-119">\_ \_ \_ Максимальное число мфпкэй асфмедиасаурце \_ итеративесик</span><span class="sxs-lookup"><span data-stu-id="904e7-119">MFPKEY\_ASFMediaSource\_IterativeSeek\_Max\_Count</span></span>](mfpkey-asfmediasource-iterativeseek-max-count.md)
-   [<span data-ttu-id="904e7-120">\_Допуск мфпкэй \_ асфмедиасаурце \_ итеративесик \_ в \_ миллисекундах</span><span class="sxs-lookup"><span data-stu-id="904e7-120">MFPKEY\_ASFMediaSource\_IterativeSeek\_Tolerance\_In\_MilliSecond</span></span>](mfpkey-asfmediasource-iterativeseek-tolerance-in-millisecond.md)

<span data-ttu-id="904e7-121">Эти свойства устанавливают максимальное число итераций и допуск соответственно.</span><span class="sxs-lookup"><span data-stu-id="904e7-121">These properties set the maximum number of iterations and the tolerance, respectively.</span></span> <span data-ttu-id="904e7-122">Алгоритм останавливается при достижении максимального числа итераций или при обнаружении пакета, расстояние от которого до времени поиска находится в пределах указанного значения.</span><span class="sxs-lookup"><span data-stu-id="904e7-122">The algorithm halts when it reaches the maximum number of iterations, or when it finds a packet whose distance from the seek time is within the specified tolerance.</span></span>

## <a name="requirements"></a><span data-ttu-id="904e7-123">Требования</span><span class="sxs-lookup"><span data-stu-id="904e7-123">Requirements</span></span>



| <span data-ttu-id="904e7-124">Требование</span><span class="sxs-lookup"><span data-stu-id="904e7-124">Requirement</span></span> | <span data-ttu-id="904e7-125">Значение</span><span class="sxs-lookup"><span data-stu-id="904e7-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="904e7-126">Минимальная версия клиента</span><span class="sxs-lookup"><span data-stu-id="904e7-126">Minimum supported client</span></span><br/> | <span data-ttu-id="904e7-127">\[Приложения UWP для классических приложений Windows 7 \|\]</span><span class="sxs-lookup"><span data-stu-id="904e7-127">Windows 7 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="904e7-128">Минимальная версия сервера</span><span class="sxs-lookup"><span data-stu-id="904e7-128">Minimum supported server</span></span><br/> | <span data-ttu-id="904e7-129">\[Приложения UWP для классических приложений Windows Server 2008 R2 \|\]</span><span class="sxs-lookup"><span data-stu-id="904e7-129">Windows Server 2008 R2 \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="904e7-130">Header</span><span class="sxs-lookup"><span data-stu-id="904e7-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="904e7-131"><dt>Мфидл. h</dt></span><span class="sxs-lookup"><span data-stu-id="904e7-131"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="904e7-132">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="904e7-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="904e7-133">Свойства Media Foundation</span><span class="sxs-lookup"><span data-stu-id="904e7-133">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




