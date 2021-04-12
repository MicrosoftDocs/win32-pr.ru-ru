---
title: Руководством по программированию для WIC
description: Описывает, как использовать API-интерфейсы WIC.
ms.assetid: ed7987f0-5983-4bb5-8640-0830a87c8f2e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0bb6675ef7f5c065d2d3e00ab470cb334af25525
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104423946"
---
# <a name="wic-programming-guide"></a><span data-ttu-id="78bfe-103">Руководством по программированию для WIC</span><span class="sxs-lookup"><span data-stu-id="78bfe-103">WIC programming guide</span></span>

<span data-ttu-id="78bfe-104">В этом разделе содержатся основные разделы, в которых описывается использование интерфейсов API компонента Windows Imaging Component (WIC).</span><span class="sxs-lookup"><span data-stu-id="78bfe-104">This section contains conceptual topics that describe how to use the Windows Imaging Component (WIC) APIs.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="78bfe-105">В этом разделе</span><span class="sxs-lookup"><span data-stu-id="78bfe-105">In this section</span></span>



| <span data-ttu-id="78bfe-106">Раздел</span><span class="sxs-lookup"><span data-stu-id="78bfe-106">Topic</span></span>                                                                                 | <span data-ttu-id="78bfe-107">Описание</span><span class="sxs-lookup"><span data-stu-id="78bfe-107">Description</span></span>                                                                                                                                                                                                           |
|---------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="78bfe-108">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="78bfe-108">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)<br/> | <span data-ttu-id="78bfe-109">WIC предоставляет расширяемую платформу для работы с изображениями и метаданными изображений.</span><span class="sxs-lookup"><span data-stu-id="78bfe-109">The WIC provides an extensible framework for working with images and image metadata.</span></span><br/>                                                                                                                       |
| [<span data-ttu-id="78bfe-110">Общие сведения об API WIC</span><span class="sxs-lookup"><span data-stu-id="78bfe-110">WIC API Overview</span></span>](-wic-api.md)<br/>                                           | <span data-ttu-id="78bfe-111">Компонент WIC предоставляет API на основе модели COM для использования в C и C++.</span><span class="sxs-lookup"><span data-stu-id="78bfe-111">The WIC provides a Component Object Model (COM) based API for use in C and C++.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="78bfe-112">Декодирование цифровых изображений</span><span class="sxs-lookup"><span data-stu-id="78bfe-112">Decoding Digital Images</span></span>](-wic-decoder-portal.md)<br/>                         | <span data-ttu-id="78bfe-113">Этот раздел содержит общие сведения и практические руководства, в которых описываются декодеры битовой карты WIC, используемые при декодировании цифровых изображений.</span><span class="sxs-lookup"><span data-stu-id="78bfe-113">This section contains conceptual and how-to topics that describe WIC bitmap decoders which are used in decoding digital images.</span></span><br/>                                                                            |
| [<span data-ttu-id="78bfe-114">Использование данных изображения</span><span class="sxs-lookup"><span data-stu-id="78bfe-114">Using Image Data</span></span>](-wic-bitmapsources-portal.md)<br/>                          | <span data-ttu-id="78bfe-115">Этот раздел содержит общие сведения и практические руководства, в которых описываются источники битовых карт WIC и способы их управления.</span><span class="sxs-lookup"><span data-stu-id="78bfe-115">This section contains conceptual and how-to topics that describe WIC bitmap sources and how to manipulate them.</span></span><br/>                                                                                            |
| [<span data-ttu-id="78bfe-116">Кодирование данных изображения</span><span class="sxs-lookup"><span data-stu-id="78bfe-116">Encoding Image Data</span></span>](encoding-bitmaps-to-digital-images.md)<br/>              | <span data-ttu-id="78bfe-117">В этом разделе приводятся общие сведения и инструкции, описывающие кодировщики растровых изображений WIC, которые используются для кодирования цифровых изображений.</span><span class="sxs-lookup"><span data-stu-id="78bfe-117">This section contains conceptual and how-to topics that describe WIC bitmap encoders which are used to encode digital images.</span></span><br/>                                                                              |
| [<span data-ttu-id="78bfe-118">Собственные кодеки WIC</span><span class="sxs-lookup"><span data-stu-id="78bfe-118">Native WIC Codecs</span></span>](native-wic-codecs.md)<br/>                                 | <span data-ttu-id="78bfe-119">В этом разделе содержатся сведения о кодеках машинного копирования, доступных в WIC.</span><span class="sxs-lookup"><span data-stu-id="78bfe-119">This section contains information about the native imaging codecs available in WIC.</span></span><br/>                                                                                                                        |
| [<span data-ttu-id="78bfe-120">Обработка метаданных изображения</span><span class="sxs-lookup"><span data-stu-id="78bfe-120">Processing Image Metadata</span></span>](-wic-metadata-portal.md)<br/>                      | <span data-ttu-id="78bfe-121">В этом разделе содержатся основные разделы, описывающие систему метаданных WIC.</span><span class="sxs-lookup"><span data-stu-id="78bfe-121">This section contains conceptual topics that describe the WIC metadata system.</span></span><br/>                                                                                                                             |
| [<span data-ttu-id="78bfe-122">Поддержка Икбкр JPEG</span><span class="sxs-lookup"><span data-stu-id="78bfe-122">JPEG YCbCr Support</span></span>](jpeg-ycbcr-support.md)<br/>                               | <span data-ttu-id="78bfe-123">Начиная с Windows 8.1 кодек [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) JPEG поддерживает чтение и запись данных изображений в собственной форме Yc<sub>b</sub>C<sub>r</sub> .</span><span class="sxs-lookup"><span data-stu-id="78bfe-123">Starting with Windows 8.1, the [Windows Imaging Component (WIC)](-wic-about-windows-imaging-codec.md) JPEG codec supports reading and writing image data in its native YC<sub>b</sub>C<sub>r</sub> form.</span></span> <br/> |
| [<span data-ttu-id="78bfe-124">Управление цветом</span><span class="sxs-lookup"><span data-stu-id="78bfe-124">Color Management</span></span>](-wic-colormanagement.md)<br/>                               | <span data-ttu-id="78bfe-125">WIC упрощает управление цветом, предоставляя интерфейс [**ивикколорконтекст**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) и интерфейс [**ивикколортрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) .</span><span class="sxs-lookup"><span data-stu-id="78bfe-125">WIC simplifies color management by providing the [**IWICColorContext**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolorcontext) interface and the [**IWICColorTransform**](/windows/desktop/api/Wincodec/nn-wincodec-iwiccolortransform) interface.</span></span><br/>          |
| [<span data-ttu-id="78bfe-126">Разработка компонентов</span><span class="sxs-lookup"><span data-stu-id="78bfe-126">Component Development</span></span>](-wic-component-development.md)<br/>                    | <span data-ttu-id="78bfe-127">WIC — это расширяемая платформа, которая предоставляет низкоуровневые API для цифровых изображений.</span><span class="sxs-lookup"><span data-stu-id="78bfe-127">The WIC is an extensible platform that provides low-level API for digital images.</span></span><br/>                                                                                                                          |



 

## <a name="see-also"></a><span data-ttu-id="78bfe-128">См. также:</span><span class="sxs-lookup"><span data-stu-id="78bfe-128">See Also</span></span>

[<span data-ttu-id="78bfe-129">Справочник по WIC</span><span class="sxs-lookup"><span data-stu-id="78bfe-129">WIC Reference</span></span>](-wic-codec-reference.md)


[<span data-ttu-id="78bfe-130">Примеры WIC</span><span class="sxs-lookup"><span data-stu-id="78bfe-130">WIC Samples</span></span>](-wic-samples.md)


 

 




