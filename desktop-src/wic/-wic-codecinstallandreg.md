---
description: При установке кодека необходимо зарегистрировать его в реестре. Также необходимо убедиться в том, что кэш эскизов обновляется в случае, если на компьютере уже есть изображения в вашем формате.
ms.assetid: 7aec54cb-40ac-495c-99d9-9c397b740b21
title: Установка и регистрация кодека
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d83616071bebdbab14bfdc7dd0f879df3d49789d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702389"
---
# <a name="codec-installation-and-registration"></a><span data-ttu-id="8f8e3-104">Установка и регистрация кодека</span><span class="sxs-lookup"><span data-stu-id="8f8e3-104">Codec Installation and Registration</span></span>

<span data-ttu-id="8f8e3-105">При установке кодека необходимо зарегистрировать его в реестре.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-105">When you install a codec, you must register it in the registry.</span></span> <span data-ttu-id="8f8e3-106">Также необходимо убедиться в том, что кэш эскизов обновляется в случае, если на компьютере уже есть изображения в вашем формате.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-106">You must also make sure the thumbnail cache gets updated in case any images in your format already exist on the computer.</span></span>

<span data-ttu-id="8f8e3-107">В этом разделе содержатся следующие подразделы.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-107">This topic contains the following sections:</span></span>

-   [<span data-ttu-id="8f8e3-108">Регистрация кодека</span><span class="sxs-lookup"><span data-stu-id="8f8e3-108">Registering a Codec</span></span>](#registering-a-codec)
-   [<span data-ttu-id="8f8e3-109">Обновление кэша эскизов при установке кодека</span><span class="sxs-lookup"><span data-stu-id="8f8e3-109">Updating the Thumbnail Cache When Installing Your Codec</span></span>](#updating-the-thumbnail-cache-when-installing-your-codec)
-   [<span data-ttu-id="8f8e3-110">Предоставление пользователям доступ к WIC-Enabled кодеку</span><span class="sxs-lookup"><span data-stu-id="8f8e3-110">Making Your WIC-Enabled Codec Available To Users</span></span>](#making-your-wic-enabled-codec-available-to-users)
-   [<span data-ttu-id="8f8e3-111">См. также</span><span class="sxs-lookup"><span data-stu-id="8f8e3-111">Related topics</span></span>](#related-topics)

## <a name="registering-a-codec"></a><span data-ttu-id="8f8e3-112">Регистрация кодека</span><span class="sxs-lookup"><span data-stu-id="8f8e3-112">Registering a Codec</span></span>

<span data-ttu-id="8f8e3-113">При регистрации кодека на самом деле регистрируются два компонента: кодировщик и декодер.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-113">When you register a codec, you are actually registering two components: the encoder and the decoder.</span></span> <span data-ttu-id="8f8e3-114">Кроме того, необходимо создать записи реестра для регистрации формата контейнера с помощью обработчиков метаданных для форматов метаданных, поддерживаемых форматом изображения.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-114">You also need to make registry entries to register your container format with the metadata handlers for the metadata formats that your image format supports.</span></span>

<span data-ttu-id="8f8e3-115">В следующих разделах описываются записи реестра, необходимые для регистрации кодека:</span><span class="sxs-lookup"><span data-stu-id="8f8e3-115">The following topics describe the registry entries you need to register your codec:</span></span>

[<span data-ttu-id="8f8e3-116">Общие записи реестра</span><span class="sxs-lookup"><span data-stu-id="8f8e3-116">General Registry Entries</span></span>](-wic-generalregentries.md)

[<span data-ttu-id="8f8e3-117">Записи реестра, относящиеся к кодировщику</span><span class="sxs-lookup"><span data-stu-id="8f8e3-117">Encoder-Specific Registry Entries</span></span>](-wic-encoderregentries.md)

[<span data-ttu-id="8f8e3-118">Записи реестра для отдельных декодеров</span><span class="sxs-lookup"><span data-stu-id="8f8e3-118">Decoder-Specific Registry Entries</span></span>](-wic-decoderregentries.md)

[<span data-ttu-id="8f8e3-119">Интеграция с Фотоальбомом Windows и проводником Windows</span><span class="sxs-lookup"><span data-stu-id="8f8e3-119">Integration with Windows Photo Gallery and Windows Explorer</span></span>](-wic-integrationregentries.md)

## <a name="updating-the-thumbnail-cache-when-installing-your-codec"></a><span data-ttu-id="8f8e3-120">Обновление кэша эскизов при установке кодека</span><span class="sxs-lookup"><span data-stu-id="8f8e3-120">Updating the Thumbnail Cache When Installing Your Codec</span></span>

<span data-ttu-id="8f8e3-121">При установке кодека установщику необходимо вызвать следующую функцию после записи ее записей реестра.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-121">When a codec is installed, the installer needs to call the following function after writing its registry entries.</span></span>


```C++
SHChangeNotify(SHCNE_ASSOCCHANGED, SHCNF_IDLIST, NULL, NULL)
```



<span data-ttu-id="8f8e3-122">Этот вызов уведомляет Windows, что доступны новые сведения о сопоставлении файлов.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-122">This call notifies Windows that new file association information is available.</span></span> <span data-ttu-id="8f8e3-123">Если образы в вашем формате уже существуют на компьютере, в кэше эскизов будут содержаться эскизы по умолчанию, так как при первом получении изображений декодер не был доступен для извлечения эскизов.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-123">If images in your image format already exist on the computer, the thumbnail cache will contain default thumbnails for them because no decoder was available to extract the thumbnails when the images were first acquired.</span></span> <span data-ttu-id="8f8e3-124">При уведомлении Windows о наличии новой ассоциации файлов кэш эскизов удаляет все пустые эскизы и извлекает фактические эскизы из файлов, которые теперь можно декодировать.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-124">When you notify Windows that a new file association is available, the thumbnail cache discards any empty thumbnails and extracts the actual thumbnails from the files that can now be decoded.</span></span>

## <a name="making-your-wic-enabled-codec-available-to-users"></a><span data-ttu-id="8f8e3-125">Предоставление пользователям доступ к WIC-Enabled кодеку</span><span class="sxs-lookup"><span data-stu-id="8f8e3-125">Making Your WIC-Enabled Codec Available To Users</span></span>

<span data-ttu-id="8f8e3-126">Если вы являетесь производителем камеры, вы можете отправить необработанные кодеки в поле с камерами.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-126">If you are a camera manufacturer, you can ship your raw codecs in the box with your cameras.</span></span> <span data-ttu-id="8f8e3-127">Вы также можете разместить кодеки на странице загрузки вашего веб-узла.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-127">You can also post your codecs on the Download page of your Web site.</span></span> <span data-ttu-id="8f8e3-128">Тем не менее, если пользователь получает файл изображения в вашем формате из другого источника, такого как дружественный, Бизнес-связь или другой веб-сайт, он может не узнать, куда получить кодек для декодирования.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-128">However, if a user acquires an image file in your format from some other source, such as a friend, business associate, or some other Web site, they may not know where to get the codec to decode it with.</span></span>

<span data-ttu-id="8f8e3-129">Из-за этой проблемы Windows предлагает пользователям более простой способ найти кодек и загрузить его на свой компьютер, начиная с Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-129">Because of this issue, Windows offers an easier way for users of your image format to find your codec and download it onto their computer, starting with Windows Vista.</span></span> <span data-ttu-id="8f8e3-130">Если фотоальбом Windows распознает расширение имени файла как формат изображения, а кодек для этого формата не установлен, в диалоговом окне появится сообщение о том, что фотография не может быть отображена, и спрашивает, требуется ли пользователю загрузить программное обеспечение, необходимое для его отображения.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-130">If the Windows Photo Gallery recognizes a file name extension as an image format, and the codec for that format is not installed, a dialog box tells the user that the photo can’t be displayed, and asks whether the user wants to download the software required to display it.</span></span> <span data-ttu-id="8f8e3-131">Когда пользователь принимает сообщение, отображается веб-сайт, размещенный в корпорации Майкрософт, со ссылкой на сайт загрузки производителя кодека.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-131">When the user accepts, a Microsoft-hosted Web site appears with a link to the codec manufacturer’s download site.</span></span> <span data-ttu-id="8f8e3-132">(При необходимости можно запросить, чтобы пользователи перезагружались непосредственно на сайт загрузки.)</span><span class="sxs-lookup"><span data-stu-id="8f8e3-132">(Optionally, you can request that users be taken directly to your download site.)</span></span>

<span data-ttu-id="8f8e3-133">Если требуется, чтобы расширения имен файлов формата изображений распознаваться фотоальбомом Windows, чтобы пользователи могли направляться на сайт загрузки, необходимо выполнить следующие действия.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-133">If you want your image format’s file name extensions to be recognized by the Windows Photo Gallery so that users can be directed to your download site, you must do the following:</span></span>

1.  <span data-ttu-id="8f8e3-134">Укажите сайт загрузки для своего кодека.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-134">Provide a download site for your codec.</span></span> <span data-ttu-id="8f8e3-135">(У вас может быть отдельная страница для каждого созданного кодека или одна страница, которая предоставляет загружаемые файлы для всех кодеков.)</span><span class="sxs-lookup"><span data-stu-id="8f8e3-135">(You can have a separate page for each codec you provide, or one page that provides downloads for all your codecs.)</span></span>

    <span data-ttu-id="8f8e3-136">Сайт загрузки должен быть локализованным и удобным для поиска с помощью модели камеры.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-136">The download site should be localized and easily searchable by camera model.</span></span>

2.  <span data-ttu-id="8f8e3-137">Предоставьте корпорации Майкрософт список расширений для форматов изображений, а также URL-адреса сайтов для скачивания.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-137">Provide Microsoft with a list of extensions for your image formats, and the URLs for your download sites.</span></span>

<span data-ttu-id="8f8e3-138">Необходимо сообщить корпорации Майкрософт о расширениях для всех новых кодеков, разрабатываемых в будущем, и любых изменениях URL-адресов сайтов загрузки, чтобы новые сведения можно было добавить в фотоальбом Windows.</span><span class="sxs-lookup"><span data-stu-id="8f8e3-138">You must inform Microsoft of the extensions for any new codecs you develop in the future, and of any changes to the URLs of your download sites, so that the new information can be added to the Windows Photo Gallery.</span></span>

## <a name="related-topics"></a><span data-ttu-id="8f8e3-139">См. также</span><span class="sxs-lookup"><span data-stu-id="8f8e3-139">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="8f8e3-140">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="8f8e3-140">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="8f8e3-141">Реализация Ивикметадатаблокквритер</span><span class="sxs-lookup"><span data-stu-id="8f8e3-141">Implementing IWICMetadataBlockWriter</span></span>](-wic-imp-iwicmetadatablockwriter.md)
</dt> <dt>

[<span data-ttu-id="8f8e3-142">Заключение (написание WIC-Enabled КОДЕка)</span><span class="sxs-lookup"><span data-stu-id="8f8e3-142">Conclusion (How to Write a WIC-Enabled CODEC)</span></span>](-wic-howtowriteacodec-conclusion.md)
</dt> <dt>

[<span data-ttu-id="8f8e3-143">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="8f8e3-143">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="8f8e3-144">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="8f8e3-144">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



