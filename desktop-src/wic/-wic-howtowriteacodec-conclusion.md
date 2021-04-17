---
description: Создание кодека на платформе Windows Imaging Component (WIC) позволяет всем приложениям, созданным на основе WIC, получить ту же поддержку платформы для вашего формата образа, которую они получают для стандартных форматов изображений, поставляемых с платформой.
ms.assetid: 4f25f0f4-246c-4cbd-bd11-d061dbc7de45
title: Заключение (написание WIC-Enabled кодека)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de165f20ff81094c3b64d7e9667795f0bf80cef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105719532"
---
# <a name="conclusion-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="2a82e-103">Заключение (написание WIC-Enabled кодека)</span><span class="sxs-lookup"><span data-stu-id="2a82e-103">Conclusion (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="2a82e-104">Создание кодека на платформе Windows Imaging Component (WIC) позволяет всем приложениям, созданным на основе WIC, получить ту же поддержку платформы для вашего формата образа, которую они получают для стандартных форматов изображений, поставляемых с платформой.</span><span class="sxs-lookup"><span data-stu-id="2a82e-104">Building your codec on the Windows Imaging Component (WIC) platform makes it possible for all applications built on WIC to get the same platform support for your image format that they get for the common image formats shipped with the platform.</span></span> <span data-ttu-id="2a82e-105">Он также позволяет Фотоальбому Windows Vista, проводнику Windows и средству просмотра фотографий отображать эскизы и предварительный просмотр изображений в формате с помощью предоставленного декодера.</span><span class="sxs-lookup"><span data-stu-id="2a82e-105">It also enables the Windows Vista Photo Gallery, Windows Explorer, and Photo Viewer to display thumbnails and previews of images in your format using the decoder that you provide.</span></span> <span data-ttu-id="2a82e-106">Для необработанных форматов он позволяет использовать более сложные приложения для работы с образами для использования возможностей обработки необработанных данных декодера.</span><span class="sxs-lookup"><span data-stu-id="2a82e-106">For raw formats, it enables more sophisticated imaging applications to take advantage of your decoder’s raw processing capabilities.</span></span> <span data-ttu-id="2a82e-107">В зависимости от поддерживаемых параметров кодировщика можно также предоставить уникальные возможности кодировщика, чтобы позволить приложениям использовать все преимущества расширенных возможностей вашего формата изображений.</span><span class="sxs-lookup"><span data-stu-id="2a82e-107">Depending on the encoder options you support, you can also expose unique capabilities of your encoder to enable applications to take full advantage of the advanced features of your image format.</span></span>

<span data-ttu-id="2a82e-108">Для разработки кодека с поддержкой WIC необходимо реализовать некоторые новые интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="2a82e-108">Developing a WIC-enabled codec requires you to implement some new interfaces.</span></span> <span data-ttu-id="2a82e-109">Во многих случаях можно написать оболочку для существующего кодека, реализующего эти интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="2a82e-109">In many cases, you can write a wrapper for your existing codec that implements these interfaces.</span></span> <span data-ttu-id="2a82e-110">При установке кодека необходимо внести некоторые записи в реестр, чтобы ваш кодек можно было обнаружить на платформе WIC, и связать его с соответствующими обработчиками метаданных.</span><span class="sxs-lookup"><span data-stu-id="2a82e-110">When you install your codec, you must make some registry entries to make your codec discoverable by the WIC platform and associate it with the appropriate metadata handlers.</span></span> <span data-ttu-id="2a82e-111">Также необходимо вызвать API для очистки кэша эскизов всех (пустых) эскизов по умолчанию, которые могли быть ранее связаны с изображениями в вашем формате.</span><span class="sxs-lookup"><span data-stu-id="2a82e-111">You also need to invoke an API to clear the thumbnail cache of any default (empty) thumbnails that may have previously associated with images in your format.</span></span> <span data-ttu-id="2a82e-112">При необходимости вы можете включить галерею фотографий Windows Vista, чтобы предоставить пользователям ссылку для скачивания кодека, когда в галерее фотографий встретится образ с расширением имени файла.</span><span class="sxs-lookup"><span data-stu-id="2a82e-112">If you want, you can enable the Windows Vista Photo Gallery to provide users with a link to download your codec when the Photo Gallery encounters an image with your file name extension.</span></span> <span data-ttu-id="2a82e-113">Для этого необходимо предоставить корпорации Майкрософт сведения о расширении имени файла кодека и URL-адресе для скачиваемого сайта.</span><span class="sxs-lookup"><span data-stu-id="2a82e-113">To do this, you must provide Microsoft with information about your codec’s file name extension and the URL for your download site.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a82e-114">См. также</span><span class="sxs-lookup"><span data-stu-id="2a82e-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="2a82e-115">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="2a82e-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="2a82e-116">Установка и регистрация КОДЕка</span><span class="sxs-lookup"><span data-stu-id="2a82e-116">CODEC Installation and Registration</span></span>](-wic-codecinstallandreg.md)
</dt> <dt>

[<span data-ttu-id="2a82e-117">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="2a82e-117">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="2a82e-118">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="2a82e-118">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



