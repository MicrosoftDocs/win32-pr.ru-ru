---
description: Форматы необработанных изображений в Windows Vista
ms.assetid: e28b642c-03c8-4ecc-b5f5-e3911b8003a7
title: Форматы необработанных изображений в Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c48b4e3ab5b0d373dbc0313267e58177b189538
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265852"
---
# <a name="raw-image-formats-in-windows-vista"></a><span data-ttu-id="48c2d-103">Форматы необработанных изображений в Windows Vista</span><span class="sxs-lookup"><span data-stu-id="48c2d-103">RAW Image Formats in Windows Vista</span></span>

<span data-ttu-id="48c2d-104">Проводник Windows Vista, фотоальбом Windows Vista, фотоальбом Window Live и средство просмотра фотографий Windows 7 используют компонент Windows Imaging Component (WIC) и поэтому поддерживают необработанные форматы изображений, если на компьютере установлены соответствующие кодеки.</span><span class="sxs-lookup"><span data-stu-id="48c2d-104">Windows Vista Explorer , Windows Vista Photo Gallery, Window Live Photo Gallery, and the Windows 7 Photo Viewer all use Windows Imaging Component (WIC) and therefore support RAW image formats when appropriate codecs are installed on the computer.</span></span>

<span data-ttu-id="48c2d-105">Так как WIC является расширяемой архитектурой создания образов, любое приложение WIC может использовать новые форматы изображений сразу после установки новых кодеков в системе.</span><span class="sxs-lookup"><span data-stu-id="48c2d-105">Because WIC is an extensible imaging architecture, any WIC application can consume new image formats as soon as new codecs are installed on the system.</span></span> <span data-ttu-id="48c2d-106">Это делает WIC идеальным в качестве самонастраивающийсяного решения для форматов необработанных изображений, которые создает цифровая камера.</span><span class="sxs-lookup"><span data-stu-id="48c2d-106">This makes WIC ideal as a Plug and Play solution for the RAW image formats that digital cameras produce.</span></span> <span data-ttu-id="48c2d-107">С помощью WIC приложения Windows могут поддерживать новые модели камеры при наличии обновленных кодеков (в идеале — в Box с новыми камерами).</span><span class="sxs-lookup"><span data-stu-id="48c2d-107">Through WIC, Windows applications can gain support for new camera models whenever updated codecs are made available (ideally in-box with new cameras).</span></span> <span data-ttu-id="48c2d-108">Авторы кодека могут поддерживать эти сценарии, реализуя интерфейсы WIC, общие для всех типов изображений, как описано более подробно в этом документе.</span><span class="sxs-lookup"><span data-stu-id="48c2d-108">Codec authors can support these scenarios by implementing WIC interfaces that are common to all image types, as described in more detail in this document.</span></span>

<span data-ttu-id="48c2d-109">В настоящее время большинство основных приложений потребителя не имеют специальных знаний о форматах необработанных изображений и не предоставляют пользовательский интерфейс для настройки параметров обработки RAW.</span><span class="sxs-lookup"><span data-stu-id="48c2d-109">Today, most mainstream consumer applications have no special knowledge of RAW image formats and do not expose a user interface for adjusting RAW processing settings.</span></span>

<span data-ttu-id="48c2d-110">Однако для поддержки специализированных приложений для работы с образами автор необработанных кодеков должен также реализовать интерфейс [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .</span><span class="sxs-lookup"><span data-stu-id="48c2d-110">However, to support specialized imaging applications, RAW codec authors must also implement the [**IWICDevelopRaw**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) interface.</span></span> <span data-ttu-id="48c2d-111">Этот интерфейс предоставляет специальные возможности для необработанных изображений, например возможность создания общих корректировок изображений и обработки (разработки) необработанных изображений в заданных цветовых пространствах красного и зеленого цвета (RGB).</span><span class="sxs-lookup"><span data-stu-id="48c2d-111">This interface exposes special features for RAW images, such as the ability to make common image adjustments and to process (develop) RAW images into specified red-green-blue (RGB) color spaces.</span></span>

<span data-ttu-id="48c2d-112">Некоторые другие интерфейсы WIC важны для реализации авторами необработанных кодеков.</span><span class="sxs-lookup"><span data-stu-id="48c2d-112">Several other WIC interfaces are important for RAW codec authors to implement.</span></span> <span data-ttu-id="48c2d-113">Эти статьи подробно обсуждаются в этой серии разделов.</span><span class="sxs-lookup"><span data-stu-id="48c2d-113">These are discussed in more detail in this series of topics.</span></span>

## <a name="related-topics"></a><span data-ttu-id="48c2d-114">См. также</span><span class="sxs-lookup"><span data-stu-id="48c2d-114">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="48c2d-115">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="48c2d-115">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="48c2d-116">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="48c2d-116">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="48c2d-117">Рекомендации по WIC для форматов необработанных изображений Camera</span><span class="sxs-lookup"><span data-stu-id="48c2d-117">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="48c2d-118">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="48c2d-118">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



