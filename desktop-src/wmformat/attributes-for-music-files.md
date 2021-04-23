---
title: Атрибуты для музыкальных файлов
description: Атрибуты для музыкальных файлов
ms.assetid: 098d9241-c8b0-4b0c-b9c1-668497f91e8c
keywords:
- Windows Media Format SDK, атрибуты
- Расширенный системный формат (ASF), атрибуты
- ASF (Расширенный системный формат), атрибуты
- атрибуты, звуковые файлы
- атрибуты, музыкальные файлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e5956296da5ef43ed3a8d35ecc2d7e6d0a4c97e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774303"
---
# <a name="attributes-for-music-files"></a><span data-ttu-id="7c7f3-108">Атрибуты для музыкальных файлов</span><span class="sxs-lookup"><span data-stu-id="7c7f3-108">Attributes for Music Files</span></span>

<span data-ttu-id="7c7f3-109">В этом разделе перечислены атрибуты, обычно используемые для звуковых файлов, содержащих музыку.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-109">This section lists the attributes commonly used for audio files containing music.</span></span> <span data-ttu-id="7c7f3-110">Рекомендуется устанавливать атрибуты для файлов в соответствии с этими списками, чтобы обеспечить полную совместимость файлов с самыми разнообразными приложениями воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-110">It is recommended that you set attributes for files according to these lists to ensure that your files are fully compatible with a wide variety of playback applications.</span></span> <span data-ttu-id="7c7f3-111">Атрибуты в этом разделе перечислены в трех категориях: первичный, вторичный и третичный.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-111">The attributes in this section are listed in three categories: primary, secondary, and tertiary.</span></span>

<span data-ttu-id="7c7f3-112">Основные атрибуты содержат самые основные сведения о файле.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-112">Primary attributes convey the most basic information about a file.</span></span> <span data-ttu-id="7c7f3-113">При создании звуковых файлов для распространения это минимальный набор атрибутов, которые следует использовать.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-113">If you are creating audio files for distribution, this is the minimum set of attributes you should use.</span></span>

<span data-ttu-id="7c7f3-114">Вторичные атрибуты содержат общие метаданные, которые важны, но не являются универсальными для всех звуковых файлов.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-114">Secondary attributes contain common metadata that is important but not universal to all audio files.</span></span>

<span data-ttu-id="7c7f3-115">При необходимости необходимо добавить третичные атрибуты, но не обязательно описывать файл.</span><span class="sxs-lookup"><span data-stu-id="7c7f3-115">Tertiary attributes should be included as needed, but are not essential to describing the file.</span></span>

## <a name="primary-attributes-for-music"></a><span data-ttu-id="7c7f3-116">Основные атрибуты музыки</span><span class="sxs-lookup"><span data-stu-id="7c7f3-116">Primary Attributes for Music</span></span>

-   [<span data-ttu-id="7c7f3-117">**Автор**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-117">**Author**</span></span>](author.md)
-   [<span data-ttu-id="7c7f3-118">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-118">**Title**</span></span>](title.md)
-   [<span data-ttu-id="7c7f3-119">**WM/Албумартист**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-119">**WM/AlbumArtist**</span></span>](wm-albumartist.md)
-   [<span data-ttu-id="7c7f3-120">**WM/Контентдистрибутор**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-120">**WM/ContentDistributor**</span></span>](wm-contentdistributor.md)
-   [<span data-ttu-id="7c7f3-121">**WM/жанр**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-121">**WM/Genre**</span></span>](wm-genre.md)
-   <span data-ttu-id="7c7f3-122">[**WM/мкди**](wm-mcdi.md) (если доступно; в противном случае используйте [**WM/вмколлектионид**](wm-wmcollectionid.md), [**WM/вмколлектионграупид**](wm-wmcollectiongroupid.md)или [**WM/вмконтентид**](wm-wmcontentid.md)).</span><span class="sxs-lookup"><span data-stu-id="7c7f3-122">[**WM/MCDI**](wm-mcdi.md) (if available; otherwise use [**WM/WMCollectionID**](wm-wmcollectionid.md), [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md), or [**WM/WMContentID**](wm-wmcontentid.md))</span></span>
-   [<span data-ttu-id="7c7f3-123">**WM/Медиакласспримарид**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-123">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
-   [<span data-ttu-id="7c7f3-124">**WM/Медиакласссекондарид**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-124">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
-   [<span data-ttu-id="7c7f3-125">**WM/provider**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-125">**WM/Provider**</span></span>](wm-provider.md)
-   [<span data-ttu-id="7c7f3-126">**WM/Траккнумбер**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-126">**WM/TrackNumber**</span></span>](wm-tracknumber.md)

## <a name="secondary-attributes-for-music"></a><span data-ttu-id="7c7f3-127">Дополнительные атрибуты музыки</span><span class="sxs-lookup"><span data-stu-id="7c7f3-127">Secondary Attributes for Music</span></span>

-   [<span data-ttu-id="7c7f3-128">**Информация**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-128">**Copyright**</span></span>](copyright.md)
-   [<span data-ttu-id="7c7f3-129">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-129">**WM/Composer**</span></span>](wm-composer.md)
-   [<span data-ttu-id="7c7f3-130">**WM/Енкодингтиме**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-130">**WM/EncodingTime**</span></span>](wm-encodingtime.md)
-   [<span data-ttu-id="7c7f3-131">**WM/Language**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-131">**WM/Language**</span></span>](wm-language.md)
-   [<span data-ttu-id="7c7f3-132">**WM/Паренталратинг**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-132">**WM/ParentalRating**</span></span>](wm-parentalrating.md)
-   [<span data-ttu-id="7c7f3-133">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-133">**WM/Producer**</span></span>](wm-producer.md)
-   [<span data-ttu-id="7c7f3-134">**WM/ToolName**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-134">**WM/ToolName**</span></span>](wm-toolname.md)
-   [<span data-ttu-id="7c7f3-135">**WM/Тулверсион**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-135">**WM/ToolVersion**</span></span>](wm-toolversion.md)
-   [<span data-ttu-id="7c7f3-136">**WM/Вмколлектионграупид**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-136">**WM/WMCollectionGroupID**</span></span>](wm-wmcollectiongroupid.md)
-   [<span data-ttu-id="7c7f3-137">**WM/Вмколлектионид**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-137">**WM/WMCollectionID**</span></span>](wm-wmcollectionid.md)
-   [<span data-ttu-id="7c7f3-138">**WM/Вмконтентид**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-138">**WM/WMContentID**</span></span>](wm-wmcontentid.md)
-   [<span data-ttu-id="7c7f3-139">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-139">**WM/Writer**</span></span>](wm-writer.md)

## <a name="tertiary-attributes-for-music"></a><span data-ttu-id="7c7f3-140">Третичные атрибуты музыки</span><span class="sxs-lookup"><span data-stu-id="7c7f3-140">Tertiary Attributes for Music</span></span>

-   [<span data-ttu-id="7c7f3-141">**Описание**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-141">**Description**</span></span>](description.md)
-   [<span data-ttu-id="7c7f3-142">**WM/Аусорурл**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-142">**WM/AuthorURL**</span></span>](wm-authorurl.md)
-   [<span data-ttu-id="7c7f3-143">**WM/Беатсперминуте**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-143">**WM/BeatsPerMinute**</span></span>](wm-beatsperminute.md)
-   [<span data-ttu-id="7c7f3-144">**WM/проводник**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-144">**WM/Conductor**</span></span>](wm-conductor.md)
-   [<span data-ttu-id="7c7f3-145">**WM/Контентграупдескриптион**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-145">**WM/ContentGroupDescription**</span></span>](wm-contentgroupdescription.md)
-   [<span data-ttu-id="7c7f3-146">**WM/Енкодедби**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-146">**WM/EncodedBy**</span></span>](wm-encodedby.md)
-   [<span data-ttu-id="7c7f3-147">**WM/Енкодингсеттингс**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-147">**WM/EncodingSettings**</span></span>](wm-encodingsettings.md)
-   [<span data-ttu-id="7c7f3-148">**WM/Инитиалкэй**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-148">**WM/InitialKey**</span></span>](wm-initialkey.md)
-   [<span data-ttu-id="7c7f3-149">**WM/песни**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-149">**WM/Lyrics**</span></span>](wm-lyrics.md)
-   [<span data-ttu-id="7c7f3-150">**WM/ \_ синхронизированы песен**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-150">**WM/Lyrics\_Synchronised**</span></span>](wm-lyrics-synchronised.md)
-   [<span data-ttu-id="7c7f3-151">**WM/настроение**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-151">**WM/Mood**</span></span>](wm-mood.md)
-   [<span data-ttu-id="7c7f3-152">**WM/Партофсет**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-152">**WM/PartOfSet**</span></span>](wm-partofset.md)
-   [<span data-ttu-id="7c7f3-153">**WM/period**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-153">**WM/Period**</span></span>](wm-period.md)
-   [<span data-ttu-id="7c7f3-154">**WM/Picture**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-154">**WM/Picture**</span></span>](wmpicture.md)
-   [<span data-ttu-id="7c7f3-155">**WM/Промотионурл**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-155">**WM/PromotionURL**</span></span>](wm-promotionurl.md)
-   [<span data-ttu-id="7c7f3-156">**WM/Publisher**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-156">**WM/Publisher**</span></span>](wm-publisher.md)
-   [<span data-ttu-id="7c7f3-157">**WM/подзаголовок**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-157">**WM/SubTitle**</span></span>](wm-subtitle.md)
-   [<span data-ttu-id="7c7f3-158">**WM/Уникуефилеидентифиер**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-158">**WM/UniqueFileIdentifier**</span></span>](wm-uniquefileidentifier.md)
-   [<span data-ttu-id="7c7f3-159">**WM/Усервебурл**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-159">**WM/UserWebURL**</span></span>](wm-userweburl.md)

## <a name="related-topics"></a><span data-ttu-id="7c7f3-160">См. также</span><span class="sxs-lookup"><span data-stu-id="7c7f3-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7c7f3-161">**Атрибуты по типу**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-161">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="7c7f3-162">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="7c7f3-162">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




