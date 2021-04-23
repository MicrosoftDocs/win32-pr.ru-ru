---
description: Доступность кодеков и поддержка платформ
ms.assetid: 6b3d09c9-e91f-4c62-92f7-c2643e51987f
title: Доступность кодеков и поддержка платформ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcc485c5f8db9ff7883263cd614578705eccd3fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265854"
---
# <a name="codec-availability-and-platform-support"></a><span data-ttu-id="b3e3a-103">Доступность кодеков и поддержка платформ</span><span class="sxs-lookup"><span data-stu-id="b3e3a-103">Codec Availability and Platform Support</span></span>

<span data-ttu-id="b3e3a-104">Корпорация Майкрософт рекомендует поставщикам камеры включать обновленные кодеки компонента Windows Imaging Component (WIC) в распространение программного обеспечения с новыми камерами и что обновленный кодек устанавливается вместе с установленным по умолчанию программным обеспечением поставщика Windows 7, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-104">Microsoft recommends that camera vendors include updated RAW Windows Imaging Component (WIC) codecs in the software distribution with new cameras and that the updated codec be installed with the default vendor software installation Windows 7, Windows Vista, and Windows XP.</span></span> <span data-ttu-id="b3e3a-105">Производители камер также должны предоставить последний кодек WIC как загружаемый с веб-узлов поддержки.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-105">Camera vendors should also provide the latest WIC codec as a download from their support sites.</span></span>

## <a name="codec-discovery"></a><span data-ttu-id="b3e3a-106">Обнаружение кодеков</span><span class="sxs-lookup"><span data-stu-id="b3e3a-106">Codec Discovery</span></span>

<span data-ttu-id="b3e3a-107">Корпорация Майкрософт выполняет следующие действия, чтобы помочь пользователям в обращении к веб-сайтам поставщиков для загрузки кодеков:</span><span class="sxs-lookup"><span data-stu-id="b3e3a-107">Microsoft is doing the following to help point users to vendors' Web sites for codec downloads:</span></span>

-   <span data-ttu-id="b3e3a-108">В проводнике Windows, если пользователь дважды щелкает файл, который не распознается (вариант по умолчанию, когда необработанный файл находится на компьютере, но кодек еще не установлен), появится диалоговое окно с сообщением о том, что файл не распознан и спрашивает, нужно ли пользователю найти программу, которая понимает файл.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-108">In Windows Explorer, if a user double-clicks a file that is not recognized (the default case when a RAW file is on the computer, but the codec is not installed yet), a dialog box reports that the file is not recognized and asks whether the user wants to find a program that understands the file.</span></span> <span data-ttu-id="b3e3a-109">Корпорация Майкрософт поддерживает существующую службу перенаправления для перенаправления пользователей на веб-сайты поставщиков, которые могут предоставить программе сведения о файле.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-109">Microsoft maintains an existing redirection service to forward users to vendors' Web sites that can supply the program to understand the file.</span></span> <span data-ttu-id="b3e3a-110">Это средство существует в Windows XP и Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-110">This facility exists in Windows XP and in Windows Vista.</span></span>
-   <span data-ttu-id="b3e3a-111">Фотоальбом Windows, фотоальбом Windows Live и средство просмотра фотографий Windows 7 распознают набор расширений файлов как необработанные файлы.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-111">The Windows Photo Gallery, Windows Live Photo Gallery, and the Windows 7 Photo Viewer recognize a set of file extensions as RAW files.</span></span> <span data-ttu-id="b3e3a-112">Если файлы из этого набора находятся в папках, которые просматриваются каким-либо из этих приложений, а кодек для этого файла еще не установлен, появится диалоговое окно, как описано в предыдущем абзаце.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-112">If files from that set are found in folders that any of these applications are looking at, and a codec for the file is not already installed, then a dialog box appears, as described in the preceding paragraph.</span></span>

<span data-ttu-id="b3e3a-113">Дополнительные сведения об обнаружении кодеков см. в разделе Доступность кодеков и поддержка платформ.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-113">For more information about codec discovery, see Codec Availability and Platform Support.</span></span>

## <a name="windows-xp-platform-support"></a><span data-ttu-id="b3e3a-114">Поддержка платформы Windows XP</span><span class="sxs-lookup"><span data-stu-id="b3e3a-114">Windows XP Platform Support</span></span>

<span data-ttu-id="b3e3a-115">Корпорация Майкрософт выпустила Windows XP с пакетом обновления 3 (SP3) и автономным установщиком WIC для Windows XP SP2.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-115">Microsoft has released Windows XP SP3 with WIC, and a standalone WIC installer for Windows XP SP2.</span></span> <span data-ttu-id="b3e3a-116">Они используют кодеки WIC для включения поддержки эскизов и предварительного просмотра на этих платформах.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-116">These use WIC codecs to enable support for thumbnails and previews on those platforms.</span></span> <span data-ttu-id="b3e3a-117">Поэтому важно, чтобы загрузка и установка кодеков поддерживалась и тестировалась в Windows 7, Windows Vista и Windows XP.</span><span class="sxs-lookup"><span data-stu-id="b3e3a-117">Therefore, it is important that codec download and installation be supported and tested on the Windows 7, Windows Vista, and Windows XP.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b3e3a-118">См. также</span><span class="sxs-lookup"><span data-stu-id="b3e3a-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b3e3a-119">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="b3e3a-119">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="b3e3a-120">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="b3e3a-120">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="b3e3a-121">Рекомендации по WIC для форматов необработанных изображений Camera</span><span class="sxs-lookup"><span data-stu-id="b3e3a-121">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="b3e3a-122">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="b3e3a-122">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



