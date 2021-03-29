---
description: Декодирование
ms.assetid: ff7e5e66-e1ea-49fc-909f-de361214afc3
title: Декодирование
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6700865d55ba7349447f5e41285d60446f0e4630
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911936"
---
# <a name="decoding"></a>Декодирование

Для правильной поддержки метаданных авторы декодера должны выполнить следующие действия:

-   Реализуйте интерфейсы [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) и [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) .
-   Реализуйте [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) в декодере кадров. Если кодек поддерживает метаданные уровня контейнера, этот интерфейс должен быть реализован в декодере уровня контейнера, а также в декодере кадров.
-   При декодировании потока изображения вызовите [**ивиккомпонентфактори**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory)::[**креатеметадатареадерфромконтаинер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwiccomponentfactory-createmetadatareaderfromcontainer) , чтобы создать экземпляр модуля чтения метаданных для каждого блока метаданных. (Все новые читатели метаданных, реализуемые кодеком, должны быть зарегистрированы в WIC.)

    Декодер не должен создавать модули чтения метаданных самостоятельно, а использует WIC для создания их на основе блоков метаданных в потоке. Декодер должен сделать это на всех найденных блоках, даже если они не известны докодер, так как в системе могут быть установлены средства чтения метаданных, которые понимают, как обрабатывать эти блоки метаданных.

-   Если обработчик метаданных для блока отсутствует, создайте экземпляр модуля чтения неизвестных метаданных с помощью параметров создания метаданных.
-   Предоставьте коллекцию средств чтения метаданных через интерфейс [**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) .

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

 

 



