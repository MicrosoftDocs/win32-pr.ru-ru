---
description: Реализация кодировщика WIC-Enabled
ms.assetid: 9c1a4fa4-30b9-445f-8aee-46711355ace7
title: Реализация кодировщика WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e65f969ba7c65e6860009b2fc998024d358301
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265447"
---
# <a name="implementing-a-wic-enabled-encoder"></a><span data-ttu-id="24830-103">Реализация кодировщика WIC-Enabled</span><span class="sxs-lookup"><span data-stu-id="24830-103">Implementing a WIC-Enabled Encoder</span></span>

## <a name="introduction"></a><span data-ttu-id="24830-104">Введение</span><span class="sxs-lookup"><span data-stu-id="24830-104">Introduction</span></span>

<span data-ttu-id="24830-105">Реализация кодировщика Windows Imaging Component (WIC) требует написания двух классов, как и для реализации декодера WIC.</span><span class="sxs-lookup"><span data-stu-id="24830-105">Implementing a Windows Imaging Component (WIC) encoder requires writing two classes, as is also true for implementing a WIC decoder.</span></span> <span data-ttu-id="24830-106">Интерфейсы в этих классах непосредственно соответствуют обязанностям кодировщика, описанным в разделе [кодирование](-wic-howwicworks.md) , как работает компонент Windows Imaging.</span><span class="sxs-lookup"><span data-stu-id="24830-106">The interfaces on these classes correspond directly to the encoder responsibilities outlined in the [Encoding](-wic-howwicworks.md) section of How The Windows Imaging Component Works.</span></span>

<span data-ttu-id="24830-107">Один из классов предоставляет службы уровня контейнера и управляет сериализацией отдельных кадров изображения в контейнере.</span><span class="sxs-lookup"><span data-stu-id="24830-107">One of the classes provides container-level services and manages the serialization of the individual image frames within the container.</span></span> <span data-ttu-id="24830-108">Этот класс реализует интерфейс [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) .</span><span class="sxs-lookup"><span data-stu-id="24830-108">This class implements the [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) interface.</span></span> <span data-ttu-id="24830-109">Если формат изображения поддерживает метаданные уровня контейнера, необходимо также реализовать интерфейс [**ивикметадатаблокквритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) для этого класса.</span><span class="sxs-lookup"><span data-stu-id="24830-109">If your image format supports container-level metadata, you must also implement the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface on this class.</span></span>

<span data-ttu-id="24830-110">Другой класс предоставляет службы на уровне кадров и выполняет фактическую кодировку битов изображения для каждого кадра в контейнере.</span><span class="sxs-lookup"><span data-stu-id="24830-110">The other class provides frame-level services and does the actual encoding of the image bits for each frame in the container.</span></span> <span data-ttu-id="24830-111">Он также выполняет перебор блоков метаданных для каждого кадра и запрашивает соответствующие модули записи метаданных для сериализации блоков.</span><span class="sxs-lookup"><span data-stu-id="24830-111">It also iterates through the metadata blocks for each frame and requests the appropriate metadata writers to serialize the blocks.</span></span> <span data-ttu-id="24830-112">Этот класс реализует интерфейс **ивикбитмапфраминкоде** и интерфейс [**ивикметадатаблокквритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) .</span><span class="sxs-lookup"><span data-stu-id="24830-112">This class implements the **IWICBitmapFrameEncode** interface and the [**IWICMetadataBlockWriter**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) interface.</span></span> <span data-ttu-id="24830-113">Этот класс должен иметь член IStream, который инициализируется классом уровня контейнера при создании экземпляра, в котором метод **commit** будет выполнять сериализацию данных кадра.</span><span class="sxs-lookup"><span data-stu-id="24830-113">This class should have an IStream member that the container-level class initializes on instantiation, into which the **Commit** method will serialize the frame data.</span></span>

<span data-ttu-id="24830-114">В некоторых случаях, например в необработанных форматах, автор кодека может не захотеть, чтобы приложения могли закодировать или перекодировать в Необработанный формат, так как цель необработанного файла заключается в том, чтобы содержать данные датчика в точном соответствии с камерой.</span><span class="sxs-lookup"><span data-stu-id="24830-114">In some cases, such as raw formats, the codec author may not want applications to be able to encode or re-encode to the raw format, because the purpose of a raw file is to contain the sensor data exactly as it came from the camera.</span></span> <span data-ttu-id="24830-115">В случаях, когда автор кодека не хочет включить кодирование, по-прежнему необходимо реализовать элементарный кодировщик, чтобы включить добавление метаданных.</span><span class="sxs-lookup"><span data-stu-id="24830-115">In cases where the codec author doesn’t want to enable encoding, it is still necessary to implement a rudimentary encoder just to enable adding metadata.</span></span> <span data-ttu-id="24830-116">В этом случае кодировщику требуется только поддержка тех методов, которые необходимы для записи метаданных, и возможность копирования битов изображения из декодера.</span><span class="sxs-lookup"><span data-stu-id="24830-116">In that case, the encoder need only support those methods necessary for writing metadata, and can copy the image bits untouched from the decoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="24830-117">Связанные темы</span><span class="sxs-lookup"><span data-stu-id="24830-117">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="24830-118">**Reference**</span><span class="sxs-lookup"><span data-stu-id="24830-118">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="24830-119">**ивикбитмапенкодер**</span><span class="sxs-lookup"><span data-stu-id="24830-119">**IWICBitmapEncoder**</span></span>](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)
</dt> <dt>

<span data-ttu-id="24830-120">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="24830-120">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="24830-121">Реализация Ивикдевелоправ</span><span class="sxs-lookup"><span data-stu-id="24830-121">Implementing IWICDevelopRaw</span></span>](-wic-imp-iwicdevelopraw.md)
</dt> <dt>

[<span data-ttu-id="24830-122">Интерфейсы кодировщика</span><span class="sxs-lookup"><span data-stu-id="24830-122">Encoder Interfaces</span></span>](-wic-encoderinterfaces.md)
</dt> <dt>

[<span data-ttu-id="24830-123">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="24830-123">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="24830-124">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="24830-124">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



