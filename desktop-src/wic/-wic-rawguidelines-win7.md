---
description: Требования к необработанным кодекам для Windows 7
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: Требования к необработанным кодекам для Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e0c4d04175eab1b6e68ac87ed18a648fa4655b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105683776"
---
# <a name="raw-codec-requirements-for-windows-7"></a>Требования к необработанным кодекам для Windows 7

Следующие функции кодека необходимы как минимум:

Все функции, необходимые для поддержки оболочки Windows Vista и фотоальбома: эскиз, предварительный просмотр и (сохраненный) поворот. Обработка необработанных значений по умолчанию должна соответствовать параметрам-снимкам.

Поддержка основных метаданных (как для чтения, так и для записи), не для EXIF, а также для метаданных EXIF, должна сохраняться в форматах необработанных файлов без использования файлов расширения.

Поддержка интерфейса [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . Для Windows 7 компонент WIC компонента Windows Imaging требует, чтобы были реализованы все интерфейсы параметров, предоставляемые [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .

Поддержка состояния ориентации:

-   90. повороты изображений шага следует применять с помощью метода [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**сетротатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) . Приложения и Windows используют этот метод для смены изображений (а также кэшированных эскизов и предварительных версий).
-   Применение поворота с помощью этого API также должно сохраняться кодеком (см. ранее в этом документе).
-   Приложения могут использовать возможности вращения API [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , но кодек не будет выполнять сериализацию параметров вращения для этого API, поэтому вращение, выполненные с помощью [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , не будут сохранены.

Поддержка высокоскоростного просмотра эскизов и извлечения. Если максимальный размер измерения в пикселях (ширина или высота) для предварительного просмотра меньше 1024 пикселей, Windows Vista запросит визуализацию для предварительного просмотра экрана:

-   Метод [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**сетрендермоде**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) должен поддерживать как минимум режимы [**викраврендеркуалитидрафтмоде**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) и [**викраврендеркуалитибесткуалити**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) , чтобы обеспечить более быструю визуализацию эскизов и предварительного просмотра, чем режим полного качества.
-   Windows выполнит вызов [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) с запрошенным размером разрешения экрана.
-   Размеры разрешения экрана должны поддерживаться в приведенном выше API.
-   Требуется последовательная обработка изображений эскизов эскиза, предварительного просмотра и полных битов изображений из [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) .

Форматы пикселей с высоким динамическим диапазоном (HDR).

Печать в формате XPS.

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

 

 



