---
description: Метод Жеткараокечаннелассигнмент извлекает значение, которое указывает, как каналы караоке назначаются для динамиков.
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: Метод Жеткараокечаннелассигнмент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dafe1217e08f3dc4f55aeec42424b1ebf9d86d22
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103895229"
---
# <a name="getkaraokechannelassignment-method"></a><span data-ttu-id="4b770-103">Метод Жеткараокечаннелассигнмент</span><span class="sxs-lookup"><span data-stu-id="4b770-103">GetKaraokeChannelAssignment Method</span></span>

> [!Note]  
> <span data-ttu-id="4b770-104">Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="4b770-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="4b770-105">В последующих версиях он может быть изменен или недоступен.</span><span class="sxs-lookup"><span data-stu-id="4b770-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="4b770-106">`GetKaraokeChannelAssignment`Метод получает значение, указывающее, как каналы караоке назначаются динамикам.</span><span class="sxs-lookup"><span data-stu-id="4b770-106">The `GetKaraokeChannelAssignment` method retrieves a value that indicates how the karaoke channels are assigned to the speakers.</span></span>

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a><span data-ttu-id="4b770-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4b770-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4b770-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span><span class="sxs-lookup"><span data-stu-id="4b770-108"><span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*</span></span>
</dt> <dd>

<span data-ttu-id="4b770-109">Задает аудиопоток в виде целого числа.</span><span class="sxs-lookup"><span data-stu-id="4b770-109">Specifies the audio stream as an Integer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4b770-110">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="4b770-110">Return Value</span></span>

<span data-ttu-id="4b770-111">Возвращает целое число, указывающее назначение динамика для указанного потока.</span><span class="sxs-lookup"><span data-stu-id="4b770-111">Returns an integer indicating the speaker assignment for the specified stream.</span></span>



| <span data-ttu-id="4b770-112">Код возврата</span><span class="sxs-lookup"><span data-stu-id="4b770-112">Return code</span></span> | <span data-ttu-id="4b770-113">Описание</span><span class="sxs-lookup"><span data-stu-id="4b770-113">Description</span></span>                                                             |
|-------------|-------------------------------------------------------------------------|
| <span data-ttu-id="4b770-114">2</span><span class="sxs-lookup"><span data-stu-id="4b770-114">2</span></span>           | <span data-ttu-id="4b770-115">Поток назначается левому и правому колонкам.</span><span class="sxs-lookup"><span data-stu-id="4b770-115">The stream is assigned to the left and right speakers.</span></span>                  |
| <span data-ttu-id="4b770-116">3</span><span class="sxs-lookup"><span data-stu-id="4b770-116">3</span></span>           | <span data-ttu-id="4b770-117">Поток назначается левым, правым и средним динамиками.</span><span class="sxs-lookup"><span data-stu-id="4b770-117">The stream is assigned to the left, right, and middle speakers.</span></span>         |
| <span data-ttu-id="4b770-118">4</span><span class="sxs-lookup"><span data-stu-id="4b770-118">4</span></span>           | <span data-ttu-id="4b770-119">Поток назначается левым, правым и audio1 докладчиками.</span><span class="sxs-lookup"><span data-stu-id="4b770-119">The stream is assigned to the left, right, and audio1 speakers.</span></span>         |
| <span data-ttu-id="4b770-120">5</span><span class="sxs-lookup"><span data-stu-id="4b770-120">5</span></span>           | <span data-ttu-id="4b770-121">Поток назначается левым, правым, средним и audio1 докладчиками.</span><span class="sxs-lookup"><span data-stu-id="4b770-121">The stream is assigned to the left, right, middle, and audio1 speakers.</span></span> |
| <span data-ttu-id="4b770-122">6</span><span class="sxs-lookup"><span data-stu-id="4b770-122">6</span></span>           | <span data-ttu-id="4b770-123">Поток назначается левым, правым и Audio2 докладчиками.</span><span class="sxs-lookup"><span data-stu-id="4b770-123">The stream is assigned to the left, right, and audio2 speakers.</span></span>         |
| <span data-ttu-id="4b770-124">7</span><span class="sxs-lookup"><span data-stu-id="4b770-124">7</span></span>           | <span data-ttu-id="4b770-125">Поток назначается левым, правым, средним и Audio2 докладчиками.</span><span class="sxs-lookup"><span data-stu-id="4b770-125">The stream is assigned to the left, right, middle, and audio2 speakers.</span></span> |



 

## <a name="see-also"></a><span data-ttu-id="4b770-126">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="4b770-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b770-127">**караокеаудиопресентатионмоде**</span><span class="sxs-lookup"><span data-stu-id="4b770-127">**KaraokeAudioPresentationMode**</span></span>](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



