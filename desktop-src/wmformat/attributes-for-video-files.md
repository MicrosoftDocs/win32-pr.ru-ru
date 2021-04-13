---
title: Атрибуты для видеофайлов
description: Атрибуты для видеофайлов
ms.assetid: 4250ad27-075e-4daa-bc04-d24ddd2e8252
keywords:
- Windows Media Format SDK, атрибуты
- Расширенный системный формат (ASF), атрибуты
- ASF (Расширенный системный формат), атрибуты
- атрибуты, видеофайлы
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd19791857d55be8017d291698a3297b395af550
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104410733"
---
# <a name="attributes-for-video-files"></a><span data-ttu-id="d6c65-107">Атрибуты для видеофайлов</span><span class="sxs-lookup"><span data-stu-id="d6c65-107">Attributes for Video Files</span></span>

<span data-ttu-id="d6c65-108">В этом разделе перечислены атрибуты, обычно используемые для видеофайлов.</span><span class="sxs-lookup"><span data-stu-id="d6c65-108">This section lists the attributes commonly used for video files.</span></span> <span data-ttu-id="d6c65-109">Рекомендуется устанавливать атрибуты для файлов в соответствии с этими списками, чтобы обеспечить полную совместимость файлов с самыми разнообразными приложениями воспроизведения.</span><span class="sxs-lookup"><span data-stu-id="d6c65-109">It is recommended that you set attributes for files according to these lists to ensure that your files are fully compatible with a wide variety of playback applications.</span></span> <span data-ttu-id="d6c65-110">Атрибуты в этом разделе перечислены в трех категориях: первичный, вторичный и третичный.</span><span class="sxs-lookup"><span data-stu-id="d6c65-110">The attributes in this section are listed in three categories: primary, secondary, and tertiary.</span></span>

<span data-ttu-id="d6c65-111">Основные атрибуты содержат самые основные сведения о файле.</span><span class="sxs-lookup"><span data-stu-id="d6c65-111">Primary attributes convey the most basic information about a file.</span></span> <span data-ttu-id="d6c65-112">При создании видеофайлов для распространения это минимальный набор атрибутов, которые следует использовать.</span><span class="sxs-lookup"><span data-stu-id="d6c65-112">If you are creating video files for distribution, this is the minimum set of attributes you should use.</span></span>

<span data-ttu-id="d6c65-113">Вторичные атрибуты содержат общие метаданные, которые важны, но не являются универсальными для всех видеофайлов.</span><span class="sxs-lookup"><span data-stu-id="d6c65-113">Secondary attributes contain common metadata that is important but not universal to all video files.</span></span>

<span data-ttu-id="d6c65-114">При необходимости необходимо добавить третичные атрибуты, но не обязательно описывать файл.</span><span class="sxs-lookup"><span data-stu-id="d6c65-114">Tertiary attributes should be included as needed, but are not essential to describing the file.</span></span>

## <a name="primary-attributes-for-video"></a><span data-ttu-id="d6c65-115">Основные атрибуты видео</span><span class="sxs-lookup"><span data-stu-id="d6c65-115">Primary Attributes for Video</span></span>

-   [<span data-ttu-id="d6c65-116">**Автор**</span><span class="sxs-lookup"><span data-stu-id="d6c65-116">**Author**</span></span>](author.md)
-   [<span data-ttu-id="d6c65-117">**Заголовок**</span><span class="sxs-lookup"><span data-stu-id="d6c65-117">**Title**</span></span>](title.md)
-   [<span data-ttu-id="d6c65-118">**WM/Контентдистрибутор**</span><span class="sxs-lookup"><span data-stu-id="d6c65-118">**WM/ContentDistributor**</span></span>](wm-contentdistributor.md)
-   <span data-ttu-id="d6c65-119">[**WM/двдид**](wm-dvdid.md) (если доступно; в противном случае используйте [**WM/вмколлектионид**](wm-wmcollectionid.md), [**WM/вмколлектионграупид**](wm-wmcollectiongroupid.md)и [**WM/вмконтентид**](wm-wmcontentid.md)).</span><span class="sxs-lookup"><span data-stu-id="d6c65-119">[**WM/DVDID**](wm-dvdid.md) (if available; otherwise use [**WM/WMCollectionID**](wm-wmcollectionid.md), [**WM/WMCollectionGroupID**](wm-wmcollectiongroupid.md), and [**WM/WMContentID**](wm-wmcontentid.md))</span></span>
-   [<span data-ttu-id="d6c65-120">**WM/жанр**</span><span class="sxs-lookup"><span data-stu-id="d6c65-120">**WM/Genre**</span></span>](wm-genre.md)
-   [<span data-ttu-id="d6c65-121">**WM/Медиакласспримарид**</span><span class="sxs-lookup"><span data-stu-id="d6c65-121">**WM/MediaClassPrimaryID**</span></span>](wm-mediaprimaryid.md)
-   [<span data-ttu-id="d6c65-122">**WM/Медиакласссекондарид**</span><span class="sxs-lookup"><span data-stu-id="d6c65-122">**WM/MediaClassSecondaryID**</span></span>](wm-mediasecondaryid.md)
-   [<span data-ttu-id="d6c65-123">**WM/provider**</span><span class="sxs-lookup"><span data-stu-id="d6c65-123">**WM/Provider**</span></span>](wm-provider.md)

## <a name="secondary-attributes-for-video"></a><span data-ttu-id="d6c65-124">Дополнительные атрибуты видео</span><span class="sxs-lookup"><span data-stu-id="d6c65-124">Secondary Attributes for Video</span></span>

-   [<span data-ttu-id="d6c65-125">**Информация**</span><span class="sxs-lookup"><span data-stu-id="d6c65-125">**Copyright**</span></span>](copyright.md)
-   [<span data-ttu-id="d6c65-126">**WM/Composer**</span><span class="sxs-lookup"><span data-stu-id="d6c65-126">**WM/Composer**</span></span>](wm-composer.md)
-   [<span data-ttu-id="d6c65-127">**WM/Director**</span><span class="sxs-lookup"><span data-stu-id="d6c65-127">**WM/Director**</span></span>](wm-director.md)
-   [<span data-ttu-id="d6c65-128">**WM/Енкодингтиме**</span><span class="sxs-lookup"><span data-stu-id="d6c65-128">**WM/EncodingTime**</span></span>](wm-encodingtime.md)
-   [<span data-ttu-id="d6c65-129">**WM/Language**</span><span class="sxs-lookup"><span data-stu-id="d6c65-129">**WM/Language**</span></span>](wm-language.md)
-   [<span data-ttu-id="d6c65-130">**WM/Паренталратинг**</span><span class="sxs-lookup"><span data-stu-id="d6c65-130">**WM/ParentalRating**</span></span>](wm-parentalrating.md)
-   [<span data-ttu-id="d6c65-131">**WM/Producer**</span><span class="sxs-lookup"><span data-stu-id="d6c65-131">**WM/Producer**</span></span>](wm-producer.md)
-   [<span data-ttu-id="d6c65-132">**WM/ToolName**</span><span class="sxs-lookup"><span data-stu-id="d6c65-132">**WM/ToolName**</span></span>](wm-toolname.md)
-   [<span data-ttu-id="d6c65-133">**WM/Тулверсион**</span><span class="sxs-lookup"><span data-stu-id="d6c65-133">**WM/ToolVersion**</span></span>](wm-toolversion.md)
-   [<span data-ttu-id="d6c65-134">**WM/Вмколлектионграупид**</span><span class="sxs-lookup"><span data-stu-id="d6c65-134">**WM/WMCollectionGroupID**</span></span>](wm-wmcollectiongroupid.md)
-   [<span data-ttu-id="d6c65-135">**WM/Вмколлектионид**</span><span class="sxs-lookup"><span data-stu-id="d6c65-135">**WM/WMCollectionID**</span></span>](wm-wmcollectionid.md)
-   [<span data-ttu-id="d6c65-136">**WM/Вмконтентид**</span><span class="sxs-lookup"><span data-stu-id="d6c65-136">**WM/WMContentID**</span></span>](wm-wmcontentid.md)
-   [<span data-ttu-id="d6c65-137">**WM/Writer**</span><span class="sxs-lookup"><span data-stu-id="d6c65-137">**WM/Writer**</span></span>](wm-writer.md)

## <a name="tertiary-attributes-for-video"></a><span data-ttu-id="d6c65-138">Третичные атрибуты видео</span><span class="sxs-lookup"><span data-stu-id="d6c65-138">Tertiary Attributes for Video</span></span>

-   [<span data-ttu-id="d6c65-139">**Описание**</span><span class="sxs-lookup"><span data-stu-id="d6c65-139">**Description**</span></span>](description.md)
-   [<span data-ttu-id="d6c65-140">**WM/Аусорурл**</span><span class="sxs-lookup"><span data-stu-id="d6c65-140">**WM/AuthorURL**</span></span>](wm-authorurl.md)
-   [<span data-ttu-id="d6c65-141">**WM/проводник**</span><span class="sxs-lookup"><span data-stu-id="d6c65-141">**WM/Conductor**</span></span>](wm-conductor.md)
-   [<span data-ttu-id="d6c65-142">**WM/Контентграупдескриптион**</span><span class="sxs-lookup"><span data-stu-id="d6c65-142">**WM/ContentGroupDescription**</span></span>](wm-contentgroupdescription.md)
-   [<span data-ttu-id="d6c65-143">**WM/Енкодедби**</span><span class="sxs-lookup"><span data-stu-id="d6c65-143">**WM/EncodedBy**</span></span>](wm-encodedby.md)
-   [<span data-ttu-id="d6c65-144">**WM/Енкодингсеттингс**</span><span class="sxs-lookup"><span data-stu-id="d6c65-144">**WM/EncodingSettings**</span></span>](wm-encodingsettings.md)
-   [<span data-ttu-id="d6c65-145">**WM/Партофсет**</span><span class="sxs-lookup"><span data-stu-id="d6c65-145">**WM/PartOfSet**</span></span>](wm-partofset.md)
-   [<span data-ttu-id="d6c65-146">**WM/Picture**</span><span class="sxs-lookup"><span data-stu-id="d6c65-146">**WM/Picture**</span></span>](wmpicture.md)
-   [<span data-ttu-id="d6c65-147">**WM/Промотионурл**</span><span class="sxs-lookup"><span data-stu-id="d6c65-147">**WM/PromotionURL**</span></span>](wm-promotionurl.md)
-   [<span data-ttu-id="d6c65-148">**WM/Publisher**</span><span class="sxs-lookup"><span data-stu-id="d6c65-148">**WM/Publisher**</span></span>](wm-publisher.md)
-   [<span data-ttu-id="d6c65-149">**WM/подзаголовок**</span><span class="sxs-lookup"><span data-stu-id="d6c65-149">**WM/SubTitle**</span></span>](wm-subtitle.md)
-   [<span data-ttu-id="d6c65-150">**WM/Уникуефилеидентифиер**</span><span class="sxs-lookup"><span data-stu-id="d6c65-150">**WM/UniqueFileIdentifier**</span></span>](wm-uniquefileidentifier.md)
-   [<span data-ttu-id="d6c65-151">**WM/Усервебурл**</span><span class="sxs-lookup"><span data-stu-id="d6c65-151">**WM/UserWebURL**</span></span>](wm-userweburl.md)

## <a name="related-topics"></a><span data-ttu-id="d6c65-152">См. также</span><span class="sxs-lookup"><span data-stu-id="d6c65-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d6c65-153">**Атрибуты по типу**</span><span class="sxs-lookup"><span data-stu-id="d6c65-153">**Attributes By Type**</span></span>](attributes-by-type.md)
</dt> <dt>

[<span data-ttu-id="d6c65-154">**Список атрибутов**</span><span class="sxs-lookup"><span data-stu-id="d6c65-154">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




