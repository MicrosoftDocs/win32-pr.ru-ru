---
description: Эскизы и предварительные версии
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Эскизы и предварительные версии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 110b0f4da08eaf2b17582dabec1ff7bd6d4f3ab4389c6bcf7654cdb5ca3198a8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086887"
---
# <a name="thumbnails-and-previews"></a>Эскизы и предварительные версии

Windows Vista и Windows фотоальбом используют компонент Windows imaging Component (WIC) для просмотра быстрых эскизов и предварительного просмотра изображений. Для поддержки быстрой отрисовки и просмотра изображений необработанные кодеки должны реализовывать [**интерфейсы WIC с**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) интерфейсом и [**предварительным просмотром**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) . Для поддержки реагирования на запросы пользователей настоятельно рекомендуется, чтобы эти интерфейсы возвращали [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) вызывающей стороне в течение 200 миллисекунд или меньше.

Корпорация Майкрософт настоятельно рекомендует владельцам формата необработанных файлов создавать предварительно подготовленный Просмотр и кэшировать его в файле изображения. Для формата в устройстве это обычно делается во время записи. Однако предварительные версии также могут быть повторно созданы и сохранены в файле изображения при каждом изменении свойств интерфейса [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) , если это не требует слишком большого объема работы.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Windows Общие сведения о компонентах обработки изображений](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Рекомендации по WIC для форматов необработанных изображений Camera](-wic-rawguidelines.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



