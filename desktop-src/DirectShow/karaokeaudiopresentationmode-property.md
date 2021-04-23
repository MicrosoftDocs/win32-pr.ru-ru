---
description: Свойство Караокеаудиопресентатионмоде задает или получает правый левый набор динамиков для вспомогательных каналов караоке.
ms.assetid: f32706eb-7f97-433d-854a-17d57cc60190
title: Караокеаудиопресентатионмоде, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 429f15c99d58136d4c423c4f66b19d12c93802a9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105682194"
---
# <a name="karaokeaudiopresentationmode-property"></a><span data-ttu-id="4d033-103">Караокеаудиопресентатионмоде, свойство</span><span class="sxs-lookup"><span data-stu-id="4d033-103">KaraokeAudioPresentationMode Property</span></span>

> [!Note]  
> <span data-ttu-id="4d033-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4d033-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4d033-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="4d033-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4d033-106">`KaraokeAudioPresentationMode`Свойство задает или получает правый левый набор динамиков для вспомогательных каналов караоке.</span><span class="sxs-lookup"><span data-stu-id="4d033-106">The `KaraokeAudioPresentationMode` property sets or retrieves the right-left speaker mix for the auxiliary karaoke channels.</span></span>

``` syntax
[iMode ] = MSWebDVD.KaraokeAudioPresentationMode
```

## <a name="return-value"></a><span data-ttu-id="4d033-107">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4d033-107">Return Value</span></span>

<span data-ttu-id="4d033-108">Возвращает целочисленное значение, содержащее набор битовых флагов, указывающих, как вспомогательные каналы караоке довнмиксед на левый и правый динамики.</span><span class="sxs-lookup"><span data-stu-id="4d033-108">Returns an integer value containing a set of bit flags indicating how the auxiliary karaoke channels are downmixed to the left and right speakers.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d033-109">Комментарии</span><span class="sxs-lookup"><span data-stu-id="4d033-109">Remarks</span></span>

<span data-ttu-id="4d033-110">Это свойство доступно для чтения и записи и имеет нулевое значение по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="4d033-110">This property is read/write with a default value of zero.</span></span>

<span data-ttu-id="4d033-111">Звуковые каналы отсчитываются от нуля, поэтому каналы 0 и 1 обычно представляют правый и левый каналы динамиков, а каналы 2 – 4 — три вспомогательных канала караоке.</span><span class="sxs-lookup"><span data-stu-id="4d033-111">Audio channels are zero-based, so channels 0 and 1 generally represent the right and left speaker channels and channels 2 through 4 are the three auxiliary karaoke channels.</span></span> <span data-ttu-id="4d033-112">Когда объект Мсвебдвд переходит в режим Караоке, он автоматически выключает каналы 2 и выше.</span><span class="sxs-lookup"><span data-stu-id="4d033-112">When the MSWebDVD object enters karaoke mode, it automatically mutes channels 2 and higher.</span></span> <span data-ttu-id="4d033-113">Используйте побитовые операции **или** , чтобы задать соответствующий бит для отправки вспомогательного канала на левый динамик, правый докладчик, оба динамика (оба бита на) или отсутствие динамиков (оба бита выключены).</span><span class="sxs-lookup"><span data-stu-id="4d033-113">Use bitwise **OR** operations to set the appropriate bit in order to send an auxiliary channel to the left speaker, right speaker, both speakers (both bits on), or to no speakers (both bits off).</span></span> <span data-ttu-id="4d033-114">По умолчанию эти биты отключены каждый раз, когда Навигатор DVD переходит в режим караоке.</span><span class="sxs-lookup"><span data-stu-id="4d033-114">These bits are all off by default whenever the DVD Navigator enters karaoke mode.</span></span> <span data-ttu-id="4d033-115">Значения битов и соответствующие им действия приведены в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="4d033-115">The value of the bits and their corresponding action is given in the following table.</span></span>



| <span data-ttu-id="4d033-116">Значение</span><span class="sxs-lookup"><span data-stu-id="4d033-116">Value</span></span>  | <span data-ttu-id="4d033-117">Описание</span><span class="sxs-lookup"><span data-stu-id="4d033-117">Description</span></span>                            |
|--------|----------------------------------------|
| <span data-ttu-id="4d033-118">0x0004</span><span class="sxs-lookup"><span data-stu-id="4d033-118">0x0004</span></span> | <span data-ttu-id="4d033-119">Довнмикс канал 2 на левый динамик</span><span class="sxs-lookup"><span data-stu-id="4d033-119">Downmix Channel 2 to the left speaker</span></span>  |
| <span data-ttu-id="4d033-120">0x0008</span><span class="sxs-lookup"><span data-stu-id="4d033-120">0x0008</span></span> | <span data-ttu-id="4d033-121">Довнмикс Channel 3 к левому докладчику</span><span class="sxs-lookup"><span data-stu-id="4d033-121">Downmix Channel 3 to the left speaker</span></span>  |
| <span data-ttu-id="4d033-122">0x0010</span><span class="sxs-lookup"><span data-stu-id="4d033-122">0x0010</span></span> | <span data-ttu-id="4d033-123">Канал довнмикс 4 на левый динамик</span><span class="sxs-lookup"><span data-stu-id="4d033-123">Downmix Channel 4 to the left speaker</span></span>  |
| <span data-ttu-id="4d033-124">0x0400</span><span class="sxs-lookup"><span data-stu-id="4d033-124">0x0400</span></span> | <span data-ttu-id="4d033-125">Довнмикс канал 2 к правому докладчику</span><span class="sxs-lookup"><span data-stu-id="4d033-125">Downmix Channel 2 to the right speaker</span></span> |
| <span data-ttu-id="4d033-126">0x0800</span><span class="sxs-lookup"><span data-stu-id="4d033-126">0x0800</span></span> | <span data-ttu-id="4d033-127">Довнмикс Channel 3 к правому докладчику</span><span class="sxs-lookup"><span data-stu-id="4d033-127">Downmix Channel 3 to the right speaker</span></span> |
| <span data-ttu-id="4d033-128">0x1000</span><span class="sxs-lookup"><span data-stu-id="4d033-128">0x1000</span></span> | <span data-ttu-id="4d033-129">Довнмикс Channel 4 к правому докладчику</span><span class="sxs-lookup"><span data-stu-id="4d033-129">Downmix Channel 4 to the right speaker</span></span> |



 

 

 



