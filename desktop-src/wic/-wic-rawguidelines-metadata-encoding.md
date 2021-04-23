---
description: Кодирование
ms.assetid: 501e63bf-26ef-42fb-b181-f1a8b26c122c
title: Кодировка (компонент Windows Imaging)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8d6d15b983b7455d0fe0c406cbad64dbbb77588b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105712543"
---
# <a name="encoding-windows-imaging-component"></a><span data-ttu-id="a65e8-103">Кодировка (компонент Windows Imaging)</span><span class="sxs-lookup"><span data-stu-id="a65e8-103">Encoding (Windows Imaging Component)</span></span>

<span data-ttu-id="a65e8-104">Автор кодировщика должен выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="a65e8-104">The encoder author must do the following:</span></span>

-   <span data-ttu-id="a65e8-105">Реализуйте интерфейсы [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) и [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) .</span><span class="sxs-lookup"><span data-stu-id="a65e8-105">Implement [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) and [**IWICBitmapFrameEncode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) interfaces.</span></span>
-   <span data-ttu-id="a65e8-106">Реализуйте [**ивикметадатаблокквритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) в кодировщике Frame.</span><span class="sxs-lookup"><span data-stu-id="a65e8-106">Implement [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) on the frame encoder.</span></span> <span data-ttu-id="a65e8-107">Если кодек поддерживает метаданные уровня контейнера, этот интерфейс должен быть реализован в кодировщике уровня контейнера, а также в кодировщике кадров.</span><span class="sxs-lookup"><span data-stu-id="a65e8-107">If the codec supports container-level metadata, this interface must be implemented on the container-level encoder as well as on the frame encoder.</span></span>
-   <span data-ttu-id="a65e8-108">Если формат контейнера неявно содержит все обязательные блоки метаданных, создайте экземпляр модуля записи метаданных для каждого такого блока.</span><span class="sxs-lookup"><span data-stu-id="a65e8-108">If the container format implicitly contains any mandatory metadata blocks, instantiate a metadata writer for each such block.</span></span> <span data-ttu-id="a65e8-109">Например, для формата TIFF требуется устройство интерфейса (IFD) для каждого кадра, поэтому модуль записи IFD всегда должен быть предоставлен.</span><span class="sxs-lookup"><span data-stu-id="a65e8-109">For example, the TIFF format requires an interface device (IFD) for each frame, so the IFD writer must always be exposed.</span></span>
-   <span data-ttu-id="a65e8-110">Реализуйте поддержку управления коллекцией модулей записи метаданных.</span><span class="sxs-lookup"><span data-stu-id="a65e8-110">Implement support for managing the collection of metadata writers.</span></span> <span data-ttu-id="a65e8-111">Модуль записи блока управляет любыми требованиями к заказам или ограничениями контейнера на типы блоков метаданных, которые могут быть закодированы.</span><span class="sxs-lookup"><span data-stu-id="a65e8-111">The block writer manages any order requirements or container restrictions on the kinds of metadata blocks that can be encoded.</span></span> <span data-ttu-id="a65e8-112">Модуль записи блокировок должен проверять, можно ли внедрять новые модули записи метаданных в формат контейнера.</span><span class="sxs-lookup"><span data-stu-id="a65e8-112">The block writer must verify that any new metadata writers can be embedded within the container format.</span></span>
-   <span data-ttu-id="a65e8-113">При кодировании потока изображения вызовите [**виксериализеметадатаконтент**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) для сериализации содержимого каждого модуля записи метаданных в поток.</span><span class="sxs-lookup"><span data-stu-id="a65e8-113">When encoding the image stream, call [**WICSerializeMetadataContent**](/windows/desktop/api/wincodecsdk/nf-wincodecsdk-wicserializemetadatacontent) to serialize each metadata writer’s content into the stream.</span></span> <span data-ttu-id="a65e8-114">Если блок метаданных содержит метаданные "критическое", кодировщику необходимо задать критические элементы метаданных, прежде чем запрашивать у автора метаданных сериализацию содержимого.</span><span class="sxs-lookup"><span data-stu-id="a65e8-114">If the metadata block contains "critical" metadata the encoder must set the critical metadata items before asking the metadata writer to serialize content.</span></span>
-   <span data-ttu-id="a65e8-115">Проверьте наличие неизвестных обработчиков метаданных, чтобы убедиться, что избыточные блоки метаданных отсутствуют.</span><span class="sxs-lookup"><span data-stu-id="a65e8-115">Check for any unknown metadata handlers to ensure that redundant metadata blocks are not present.</span></span> <span data-ttu-id="a65e8-116">Это важно, поскольку при сохранении метаданных в сценарии декодирования или кодирования неизвестные блоки могут быть дубликатами обязательных блоков метаданных.</span><span class="sxs-lookup"><span data-stu-id="a65e8-116">This is important because, while preserving metadata in a decode or encode scenario, unknown blocks might be a duplicate of mandatory metadata blocks.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a65e8-117">См. также</span><span class="sxs-lookup"><span data-stu-id="a65e8-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="a65e8-118">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="a65e8-118">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="a65e8-119">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="a65e8-119">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="a65e8-120">Рекомендации по WIC для форматов необработанных изображений Camera</span><span class="sxs-lookup"><span data-stu-id="a65e8-120">WIC Guidelines for Camera RAW Image Formats</span></span>](-wic-rawguidelines.md)
</dt> <dt>

[<span data-ttu-id="a65e8-121">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="a65e8-121">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



