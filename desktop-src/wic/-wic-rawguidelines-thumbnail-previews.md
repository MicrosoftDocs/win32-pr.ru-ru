---
description: Эскизы и предварительные версии
ms.assetid: e45f025e-a1ac-47c8-b794-ab1402ab35fb
title: Эскизы и предварительные версии
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e279da9771a43eb75bb94faff23d2e6aa29c4ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105656662"
---
# <a name="thumbnails-and-previews"></a>Эскизы и предварительные версии

Windows Vista и фотоальбом Windows используют компонент Windows Imaging Component (WIC) для визуализации быстрых эскизов и предварительного просмотра изображений. Для поддержки быстрой отрисовки и просмотра изображений необработанные кодеки должны реализовывать [**интерфейсы WIC с**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) интерфейсом и [**предварительным просмотром**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) . Для поддержки реагирования на запросы пользователей настоятельно рекомендуется, чтобы эти интерфейсы возвращали [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) вызывающей стороне в течение 200 миллисекунд или меньше.

Корпорация Майкрософт настоятельно рекомендует владельцам формата необработанных файлов создавать предварительно подготовленный Просмотр и кэшировать его в файле изображения. Для формата в устройстве это обычно делается во время записи. Однако предварительные версии также могут быть повторно созданы и сохранены в файле изображения при каждом изменении свойств интерфейса [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) , если это не требует слишком большого объема работы.

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Рекомендации по WIC для форматов необработанных изображений Camera](-wic-rawguidelines.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> </dl>

 

 



