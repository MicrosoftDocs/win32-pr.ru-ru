---
description: Введение (рекомендации по WIC для форматов необработанных изображений Camera)
ms.assetid: 3c588386-1d4d-4ee0-b633-bfc94ca751ea
title: Введение (рекомендации по WIC для форматов необработанных изображений Camera)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec6ee2607326afe289e0a3e54b254dcf581cbf86
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265851"
---
# <a name="introduction-wic-guidelines-for-camera-raw-image-formats"></a><span data-ttu-id="19d47-103">Введение (рекомендации по WIC для форматов необработанных изображений Camera)</span><span class="sxs-lookup"><span data-stu-id="19d47-103">Introduction (WIC Guidelines for Camera RAW Image Formats)</span></span>

<span data-ttu-id="19d47-104">Компонент Windows Imaging Component (WIC) предоставляет расширяемую платформу для работы с изображениями и метаданными изображений.</span><span class="sxs-lookup"><span data-stu-id="19d47-104">The Windows Imaging Component (WIC) provides an extensible framework for working with images and image metadata.</span></span> <span data-ttu-id="19d47-105">WIC позволяет поставщикам программного обеспечения и оборудования разрабатывать кодеки таким образом, чтобы их собственные форматы изображений могли получить ту же поддержку платформы, что и форматы образов в машинном коде, такие как формат файлов изображений с тегами (TIFF), группа фотографий (JPEG) или Фото HD.</span><span class="sxs-lookup"><span data-stu-id="19d47-105">WIC makes it possible for software and hardware vendors to develop codecs so that their own image formats can obtain the same platform support as native image formats such as tagged image file format (TIFF), Joint Photographic Experts Group (JPEG), or HD Photo.</span></span>

<span data-ttu-id="19d47-106">Компонент WIC предоставляет единый последовательный набор интерфейсов для всей обработки изображений независимо от формата изображения.</span><span class="sxs-lookup"><span data-stu-id="19d47-106">WIC provides a single, consistent set of interfaces for all image processing, regardless of image format.</span></span> <span data-ttu-id="19d47-107">Таким образом, любое приложение, использующее WIC, получает автоматическую поддержку новых форматов изображений сразу после установки кодека.</span><span class="sxs-lookup"><span data-stu-id="19d47-107">Therefore, any application that uses WIC receives automatic support for new image formats as soon as the codec is installed.</span></span> <span data-ttu-id="19d47-108">WIC также предоставляет расширяемую платформу метаданных, которая позволяет приложениям считывать и записывать собственные собственные метаданные непосредственно в файлы изображений, поэтому метаданные никогда не теряются и не отделяются от изображения.</span><span class="sxs-lookup"><span data-stu-id="19d47-108">WIC also provides an extensible metadata framework that makes it possible for applications to read and write their own proprietary metadata directly to image files, so the metadata is never lost or separated from the image.</span></span>

<span data-ttu-id="19d47-109">Компонент WIC входит в состав Windows Presentation Foundation (WPF) и встроен в Windows Vista и более поздние версии Windows.</span><span class="sxs-lookup"><span data-stu-id="19d47-109">WIC is included with Windows Presentation Foundation (WPF) and is built into Windows Vista and later Windows versions.</span></span> <span data-ttu-id="19d47-110">Он также доступен в качестве автономного распространяемого компонента для Windows XP.</span><span class="sxs-lookup"><span data-stu-id="19d47-110">It is also available as a stand-alone redistributable component for Windows XP.</span></span>

<span data-ttu-id="19d47-111">Эти рекомендации предназначены для того, чтобы помочь производителям необработанных форматов в разработке кодеков WIC.</span><span class="sxs-lookup"><span data-stu-id="19d47-111">These guidelines are designed to help RAW format manufacturers in their development of WIC codecs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="19d47-112">См. также</span><span class="sxs-lookup"><span data-stu-id="19d47-112">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="19d47-113">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="19d47-113">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="19d47-114">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="19d47-114">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="19d47-115">Рекомендации по WIC для форматов необработанных изображений Camera</span><span class="sxs-lookup"><span data-stu-id="19d47-115">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="19d47-116">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="19d47-116">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



