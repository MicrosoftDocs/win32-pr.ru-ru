---
title: Атрибуты с несколькими значениями (пакет SDK для формата Windows Media 11)
description: Атрибуты с несколькими значениями
ms.assetid: 2e65c5d0-6f5e-45a4-8e13-9e49da007145
keywords:
- Windows Media Format SDK, атрибуты
- Расширенный системный формат (ASF), атрибуты
- ASF (Расширенный системный формат), атрибуты
- атрибуты, несколько значений
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 928aee154f9f824168ce08470702b49c23ba2c0a
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/10/2020
ms.locfileid: "104070968"
---
# <a name="attributes-with-multiple-values-windows-media-format-11-sdk"></a><span data-ttu-id="bb536-107">Атрибуты с несколькими значениями (пакет SDK для формата Windows Media 11)</span><span class="sxs-lookup"><span data-stu-id="bb536-107">Attributes with Multiple Values (Windows Media Format 11 SDK)</span></span>

<span data-ttu-id="bb536-108">Некоторым из предопределенных атрибутов может быть назначено несколько значений.</span><span class="sxs-lookup"><span data-stu-id="bb536-108">Some of the predefined attributes can have multiple values assigned to them.</span></span> <span data-ttu-id="bb536-109">Например, « **исполнитель** » — это атрибут, который может иметь несколько значений.</span><span class="sxs-lookup"><span data-stu-id="bb536-109">For example, **Artist** is an attribute that can have multiple values.</span></span> <span data-ttu-id="bb536-110">Можно вызвать [**IWMHeaderInfo3:: аддаттрибуте**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) несколько раз, чтобы добавить столько значений **исполнителей** , сколько требуется.</span><span class="sxs-lookup"><span data-stu-id="bb536-110">You can call [**IWMHeaderInfo3::AddAttribute**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmheaderinfo3-addattribute) multiple times to add as many **Artist** values as you require.</span></span> <span data-ttu-id="bb536-111">При выполнении нескольких вызовов **аддаттрибуте** для атрибутов, которые не поддерживают несколько значений, метод может вернуть код ошибки или просто проигнорировать запрос.</span><span class="sxs-lookup"><span data-stu-id="bb536-111">If you make multiple calls to **AddAttribute** for attributes that do not support multiple values, the method may return an error code, or simply ignore your request.</span></span>

<span data-ttu-id="bb536-112">В следующей таблице перечислены атрибуты, которые поддерживают несколько значений.</span><span class="sxs-lookup"><span data-stu-id="bb536-112">The following table lists the attributes that support multiple values.</span></span> <span data-ttu-id="bb536-113">Некоторые атрибуты могут иметь несколько значений только в ASF-файлах, а другие могут иметь несколько значений в файлах ASF и MP3.</span><span class="sxs-lookup"><span data-stu-id="bb536-113">Some attributes can have multiple values only in ASF files, while others can have multiple values in both ASF and MP3 files.</span></span>



| <span data-ttu-id="bb536-114">attribute</span><span class="sxs-lookup"><span data-stu-id="bb536-114">Attribute</span></span>                                                 | <span data-ttu-id="bb536-115">Поддержка нескольких значений</span><span class="sxs-lookup"><span data-stu-id="bb536-115">Support for multiple values</span></span> |
|-----------------------------------------------------------|-----------------------------|
| [<span data-ttu-id="bb536-116">**Автор**</span><span class="sxs-lookup"><span data-stu-id="bb536-116">**Author**</span></span>](author.md)                                  | <span data-ttu-id="bb536-117">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="bb536-117">ASF, MP3</span></span>                    |
| [<span data-ttu-id="bb536-118">**WM/Албумартист**</span><span class="sxs-lookup"><span data-stu-id="bb536-118">**WM/AlbumArtist**</span></span>](wm-albumartist.md)                  | <span data-ttu-id="bb536-119">ASF</span><span class="sxs-lookup"><span data-stu-id="bb536-119">ASF</span></span>                         |
| [<span data-ttu-id="bb536-120">**WM/Албумковерурл**</span><span class="sxs-lookup"><span data-stu-id="bb536-120">**WM/AlbumCoverURL**</span></span>](wm-albumcoverurl.md)              | <span data-ttu-id="bb536-121">ASF</span><span class="sxs-lookup"><span data-stu-id="bb536-121">ASF</span></span>                         |
| [<span data-ttu-id="bb536-122">**WM/Category**</span><span class="sxs-lookup"><span data-stu-id="bb536-122">**WM/Category**</span></span>](wm-category.md)                        | <span data-ttu-id="bb536-123">ASF</span><span class="sxs-lookup"><span data-stu-id="bb536-123">ASF</span></span>                         |
| [<span data-ttu-id="bb536-124">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="bb536-124">**WM/Composer**</span></span>](wm-composer.md)                        | <span data-ttu-id="bb536-125">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="bb536-125">ASF, MP3</span></span>                    |
| [<span data-ttu-id="bb536-126">**WM/проводник**</span><span class="sxs-lookup"><span data-stu-id="bb536-126">**WM/Conductor**</span></span>](wm-conductor.md)                      | <span data-ttu-id="bb536-127">ASF</span><span class="sxs-lookup"><span data-stu-id="bb536-127">ASF</span></span>                         |
| [<span data-ttu-id="bb536-128">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="bb536-128">**WM/Director**</span></span>](wm-director.md)                        | <span data-ttu-id="bb536-129">ASF</span><span class="sxs-lookup"><span data-stu-id="bb536-129">ASF</span></span>                         |
| [<span data-ttu-id="bb536-130">**WM/жанр**</span><span class="sxs-lookup"><span data-stu-id="bb536-130">**WM/Genre**</span></span>](wm-genre.md)                              | <span data-ttu-id="bb536-131">ASF</span><span class="sxs-lookup"><span data-stu-id="bb536-131">ASF</span></span>                         |
| [<span data-ttu-id="bb536-132">**WM/GenreID**</span><span class="sxs-lookup"><span data-stu-id="bb536-132">**WM/GenreID**</span></span>](wm-genreid.md)                          | <span data-ttu-id="bb536-133">ASF</span><span class="sxs-lookup"><span data-stu-id="bb536-133">ASF</span></span>                         |
| [<span data-ttu-id="bb536-134">**WM/Language**</span><span class="sxs-lookup"><span data-stu-id="bb536-134">**WM/Language**</span></span>](wm-language.md)                        | <span data-ttu-id="bb536-135">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="bb536-135">ASF, MP3</span></span>                    |
| [<span data-ttu-id="bb536-136">**WM/ \_ синхронизированы песен**</span><span class="sxs-lookup"><span data-stu-id="bb536-136">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md) | <span data-ttu-id="bb536-137">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="bb536-137">ASF, MP3</span></span>                    |
| [<span data-ttu-id="bb536-138">**WM/настроение**</span><span class="sxs-lookup"><span data-stu-id="bb536-138">**WM/Mood**</span></span>](wm-mood.md)                                | <span data-ttu-id="bb536-139">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="bb536-139">ASF, MP3</span></span>                    |
| [<span data-ttu-id="bb536-140">**WM/Picture**</span><span class="sxs-lookup"><span data-stu-id="bb536-140">**WM/Picture**</span></span>](wmpicture.md)                           | <span data-ttu-id="bb536-141">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="bb536-141">ASF, MP3</span></span>                    |
| [<span data-ttu-id="bb536-142">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="bb536-142">**WM/Producer**</span></span>](wm-producer.md)                        | <span data-ttu-id="bb536-143">ASF</span><span class="sxs-lookup"><span data-stu-id="bb536-143">ASF</span></span>                         |
| [<span data-ttu-id="bb536-144">**WM/Промотионурл**</span><span class="sxs-lookup"><span data-stu-id="bb536-144">**WM/PromotionURL**</span></span>](wm-promotionurl.md)                | <span data-ttu-id="bb536-145">ASF</span><span class="sxs-lookup"><span data-stu-id="bb536-145">ASF</span></span>                         |
| [<span data-ttu-id="bb536-146">**WM/Усервебурл**</span><span class="sxs-lookup"><span data-stu-id="bb536-146">**WM/UserWebURL**</span></span>](wm-userweburl.md)                    | <span data-ttu-id="bb536-147">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="bb536-147">ASF, MP3</span></span>                    |
| [<span data-ttu-id="bb536-148">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="bb536-148">**WM/Writer**</span></span>](wm-writer.md)                            | <span data-ttu-id="bb536-149">ASF, MP3</span><span class="sxs-lookup"><span data-stu-id="bb536-149">ASF, MP3</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="bb536-150">См. также</span><span class="sxs-lookup"><span data-stu-id="bb536-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bb536-151">**Атрибуты**</span><span class="sxs-lookup"><span data-stu-id="bb536-151">**Attributes**</span></span>](attributes.md)
</dt> </dl>

 

 




