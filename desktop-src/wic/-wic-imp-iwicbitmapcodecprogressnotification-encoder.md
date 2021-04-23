---
description: Реализация Ивикбитмапкодекпрогресснотификатион (кодировщик)
ms.assetid: d470ec93-d329-48c0-9556-0c15daece491
title: Реализация Ивикбитмапкодекпрогресснотификатион (кодировщик)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 260fac41068de0695813d569881e4a71938eb83d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911955"
---
# <a name="implementing-iwicbitmapcodecprogressnotification-encoder"></a><span data-ttu-id="50926-103">Реализация Ивикбитмапкодекпрогресснотификатион (кодировщик)</span><span class="sxs-lookup"><span data-stu-id="50926-103">Implementing IWICBitmapCodecProgressNotification (Encoder)</span></span>

## <a name="iwicbitmapcodecprogressnotification"></a><span data-ttu-id="50926-104">ивикбитмапкодекпрогресснотификатион</span><span class="sxs-lookup"><span data-stu-id="50926-104">IWICBitmapCodecProgressNotification</span></span>

<span data-ttu-id="50926-105">Хотя интерфейс [**ивикбитмапкодекпрогресснотификатион**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) является необязательным, рекомендуется реализовать его в классе кодировщика уровня контейнера.</span><span class="sxs-lookup"><span data-stu-id="50926-105">Although the [**IWICBitmapCodecProgressNotification**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapcodecprogressnotification) interface is optional, it is recommended that it be implemented on the container-level encoder class.</span></span> <span data-ttu-id="50926-106">Этот интерфейс рассматривается более подробно в разделе [Реализация ивикбитмапкодекпрогресснотификатион (декодер)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md).</span><span class="sxs-lookup"><span data-stu-id="50926-106">This interface is discussed in more details in [Implementing IWICBitmapCodecProgressNotification (Decoder)](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md).</span></span> <span data-ttu-id="50926-107">Реализация одинакова для декодера и кодировщика.</span><span class="sxs-lookup"><span data-stu-id="50926-107">The implementation is the same for either the decoder and the encoder.</span></span>

## <a name="related-topics"></a><span data-ttu-id="50926-108">См. также</span><span class="sxs-lookup"><span data-stu-id="50926-108">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="50926-109">**Зрения**</span><span class="sxs-lookup"><span data-stu-id="50926-109">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="50926-110">Реализация Ивикбитмапенкодер</span><span class="sxs-lookup"><span data-stu-id="50926-110">Implementing IWICBitmapEncoder</span></span>](-wic-imp-iwicbitmapencoder.md)
</dt> <dt>

[<span data-ttu-id="50926-111">Реализация Ивикбитмапфраминкоде</span><span class="sxs-lookup"><span data-stu-id="50926-111">Implementing IWICBitmapFrameEncode</span></span>](-wic-imp-iwicbitmapframeencode.md)
</dt> <dt>

[<span data-ttu-id="50926-112">Написание WIC-Enabled КОДЕка</span><span class="sxs-lookup"><span data-stu-id="50926-112">How to Write a WIC-Enabled CODEC</span></span>](-wic-howtowriteacodec.md)
</dt> <dt>

[<span data-ttu-id="50926-113">Общие сведения о компоненте создания образов Windows</span><span class="sxs-lookup"><span data-stu-id="50926-113">Windows Imaging Component Overview</span></span>](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[<span data-ttu-id="50926-114">Реализация Ивикбитмапкодекпрогресснотификатион (декодер)</span><span class="sxs-lookup"><span data-stu-id="50926-114">Implementing IWICBitmapCodecProgressNotification (Decoder)</span></span>](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md)
</dt> </dl>

 

 



