---
title: Атрибуты с несколькими значениями (пакет SDK для формата Windows Media 11)
description: Сведения об атрибутах с несколькими значениями в пакете SDK для формата Windows Media 11. Некоторые атрибуты элемента мультимедиа могут иметь несколько значений.
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK, атрибуты
- Расширенный системный формат (ASF), атрибуты
- ASF (Расширенный системный формат), атрибуты
- атрибуты, несколько значений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9466cd3f993cc1b12f27bc162e5188e6d45404b
ms.sourcegitcommit: d0eb44d0a95f5e5efbfec3d3e9c143f5cba25bc3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/17/2021
ms.locfileid: "112262696"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="2a4ac-108">Атрибуты с несколькими значениями (пакет SDK для формата Windows Media 11)</span><span class="sxs-lookup"><span data-stu-id="2a4ac-108">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="2a4ac-109">Некоторым из предопределенных атрибутов может быть назначено несколько значений.</span><span class="sxs-lookup"><span data-stu-id="2a4ac-109">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="2a4ac-110">Например, « **исполнитель** » — это атрибут, который может иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="2a4ac-110">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="2a4ac-111">Можно вызвать [**IWMHeaderInfo3:: аддаттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) несколько раз, чтобы добавить столько значений **исполнителей** , сколько требуется.</span><span class="sxs-lookup"><span data-stu-id="2a4ac-111">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="2a4ac-112">При выполнении нескольких вызовов **аддаттрибуте** для атрибутов, которые не поддерживают несколько значений, метод может вернуть код ошибки или просто проигнорировать запрос.</span><span class="sxs-lookup"><span data-stu-id="2a4ac-112">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="2a4ac-113">В следующей таблице перечислены атрибуты, которые поддерживают несколько значений.</span><span class="sxs-lookup"><span data-stu-id="2a4ac-113">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="2a4ac-114">Некоторые атрибуты могут иметь несколько значений только в ASF-файлах, а другие могут иметь несколько значений в файлах ASF и MP3.</span><span class="sxs-lookup"><span data-stu-id="2a4ac-114">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="2a4ac-115">attribute</span><span class="sxs-lookup"><span data-stu-id="2a4ac-115">Attribute</span></span>                                                 | <span data-ttu-id="2a4ac-116">Поддержка нескольких значений</span><span class="sxs-lookup"><span data-stu-id="2a4ac-116">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="2a4ac-117">**Автор**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-117">**Author**</span></span>](author.md)                                  | <span data-ttu-id="2a4ac-118">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="2a4ac-118">ASF, MP3</span></span>                    |
| [<span data-ttu-id="2a4ac-119">**WM/Албумартист**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-119">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="2a4ac-120">ASF</span><span class="sxs-lookup"><span data-stu-id="2a4ac-120">ASF</span></span>                         |
| [<span data-ttu-id="2a4ac-121">**WM/Албумковерурл**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-121">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="2a4ac-122">ASF</span><span class="sxs-lookup"><span data-stu-id="2a4ac-122">ASF</span></span>                         |
| [<span data-ttu-id="2a4ac-123">**WM/Category**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-123">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="2a4ac-124">ASF</span><span class="sxs-lookup"><span data-stu-id="2a4ac-124">ASF</span></span>                         |
| [<span data-ttu-id="2a4ac-125">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-125">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="2a4ac-126">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="2a4ac-126">ASF, MP3</span></span>                    |
| [<span data-ttu-id="2a4ac-127">**WM/проводник**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-127">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="2a4ac-128">ASF</span><span class="sxs-lookup"><span data-stu-id="2a4ac-128">ASF</span></span>                         |
| [<span data-ttu-id="2a4ac-129">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-129">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="2a4ac-130">ASF</span><span class="sxs-lookup"><span data-stu-id="2a4ac-130">ASF</span></span>                         |
| [<span data-ttu-id="2a4ac-131">**WM/жанр**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-131">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="2a4ac-132">ASF</span><span class="sxs-lookup"><span data-stu-id="2a4ac-132">ASF</span></span>                         |
| [<span data-ttu-id="2a4ac-133">**WM/GenreID**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-133">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="2a4ac-134">ASF</span><span class="sxs-lookup"><span data-stu-id="2a4ac-134">ASF</span></span>                         |
| [<span data-ttu-id="2a4ac-135">**WM/Language**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-135">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="2a4ac-136">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="2a4ac-136">ASF, MP3</span></span>                    |
| [<span data-ttu-id="2a4ac-137">**WM/ \_ синхронизированы песен**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-137">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="2a4ac-138">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="2a4ac-138">ASF, MP3</span></span>                    |
| [<span data-ttu-id="2a4ac-139">**WM/настроение**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-139">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="2a4ac-140">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="2a4ac-140">ASF, MP3</span></span>                    |
| [<span data-ttu-id="2a4ac-141">**WM/Picture**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-141">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="2a4ac-142">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="2a4ac-142">ASF, MP3</span></span>                    |
| [<span data-ttu-id="2a4ac-143">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-143">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="2a4ac-144">ASF</span><span class="sxs-lookup"><span data-stu-id="2a4ac-144">ASF</span></span>                         |
| [<span data-ttu-id="2a4ac-145">**WM/Промотионурл**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-145">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="2a4ac-146">ASF</span><span class="sxs-lookup"><span data-stu-id="2a4ac-146">ASF</span></span>                         |
| [<span data-ttu-id="2a4ac-147">**WM/Усервебурл**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-147">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="2a4ac-148">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="2a4ac-148">ASF, MP3</span></span>                    |
| [<span data-ttu-id="2a4ac-149">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-149">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="2a4ac-150">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="2a4ac-150">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="2a4ac-151">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="2a4ac-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a4ac-152">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="2a4ac-152">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




