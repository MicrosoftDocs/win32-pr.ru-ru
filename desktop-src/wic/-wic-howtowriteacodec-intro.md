---
description: Компонент Windows Imaging Component (WIC) — это расширяемая платформа для создания цифровых образов в операционных системах Windows Vista и Windows 7.
ms.assetid: ffcd5239-ae2d-436f-9402-8c10a79256c3
title: Введение (написание WIC-Enabled кодека)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 776bf9f2c0cb5df8b45ce04d55f20d40d05a12a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712040"
---
# <a name="introduction-how-to-write-a-wic-enabled-codec"></a><span data-ttu-id="c84b4-103">Введение (написание WIC-Enabled кодека)</span><span class="sxs-lookup"><span data-stu-id="c84b4-103">Introduction (How to Write a WIC-Enabled Codec)</span></span>

<span data-ttu-id="c84b4-104">Компонент Windows Imaging Component (WIC) — это расширяемая платформа для создания цифровых образов в операционных системах Windows Vista и Windows 7.</span><span class="sxs-lookup"><span data-stu-id="c84b4-104">The Windows Imaging Component (WIC) is an extensible platform for digital imaging on the Windows Vista and Windows 7 operating systems.</span></span> <span data-ttu-id="c84b4-105">Компонент WIC также доступен в Windows XP и Windows Server 2003 либо в составе Microsoft .NET Framework 3,0, либо в виде отдельного компонента, который можно распространять повторно.</span><span class="sxs-lookup"><span data-stu-id="c84b4-105">WIC is also available on Windows XP and Windows Server 2003, either as part of Microsoft .NET Framework 3.0 or as a separate component that you can redistribute.</span></span> <span data-ttu-id="c84b4-106">Любое приложение, использующее WIC, может получать доступ, отображать, обрабатывать и печатать изображения в любом формате изображения, предоставляющем кодек с поддержкой WIC, используя единый набор последовательных интерфейсов, устраняющих необходимость специального знания определенных форматов.</span><span class="sxs-lookup"><span data-stu-id="c84b4-106">Any application using the WIC can access, display, process, and print images in any image format that provides a WIC-enabled codec, using a single set of consistent interfaces that eliminate the need for specialized knowledge of specific formats.</span></span>

<span data-ttu-id="c84b4-107">Проводник Windows Vista, фотоальбом Windows Vista, фотоальбом Live Photo Viewer и средство просмотра фотографий Windows 7 основаны на WIC.</span><span class="sxs-lookup"><span data-stu-id="c84b4-107">The Windows Vista Explorer, Windows Vista Photo Gallery, Live Photo Gallery, and Windows 7 Photo Viewer are built on WIC.</span></span> <span data-ttu-id="c84b4-108">После установки кодеков с поддержкой WIC в системе Windows Vista или Windows 7 операционная система предоставляет тот же уровень поддержки для соответствующего формата изображений, что и для стандартных форматов изображений, поставляемых с платформой.</span><span class="sxs-lookup"><span data-stu-id="c84b4-108">After a WIC-enabled codec is installed on a Windows Vista or Windows 7 system, the operating system provides the same level of support for the associated image format as for the standard image formats that ship with the platform.</span></span> <span data-ttu-id="c84b4-109">Так как вы пишете кодек для собственного формата изображений, вы можете обеспечить единообразное качество в любом месте, где используется формат изображения, и получить преимущества полной поддержки платформы.</span><span class="sxs-lookup"><span data-stu-id="c84b4-109">Because you write the codec for your own image format, you can ensure consistent quality wherever your image format is used, and you get the benefits of full platform support.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c84b4-110">См. также</span><span class="sxs-lookup"><span data-stu-id="c84b4-110">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c84b4-111">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="c84b4-111">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="c84b4-112">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="c84b4-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="c84b4-113">Принцип работы компонента Windows Imaging</span><span class="sxs-lookup"><span data-stu-id="c84b4-113">How The Windows Imaging Component Works</span></span>](-wic-howwicworks.md)
</dt> <dt>

<span data-ttu-id="c84b4-114">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="c84b4-114">How to Write a WIC-Enabled CODEC</span></span>
</dt> <dt>

[<span data-ttu-id="c84b4-115">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="c84b4-115">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



