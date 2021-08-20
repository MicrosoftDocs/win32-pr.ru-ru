---
description: требования к необработанным кодекам для Windows 7
ms.assetid: 3f8bd336-ba03-4ffb-9aa2-ea55a276e3bc
title: требования к необработанным кодекам для Windows 7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a67735c3ddd726bb049e8efc1d4253562c84d580ef7499a616fa0d01a8e71bce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118032139"
---
# <a name="raw-codec-requirements-for-windows-7"></a>требования к необработанным кодекам для Windows 7

Следующие функции кодека необходимы как минимум:

все функции, необходимые для поддержки оболочки Windows Vista и фотоальбома: эскиз, предварительный просмотр и (сохраненный) поворот. Обработка необработанных значений по умолчанию должна соответствовать параметрам-снимкам.

Поддержка основных метаданных (как для чтения, так и для записи), не для EXIF, а также для метаданных EXIF, должна сохраняться в форматах необработанных файлов без использования файлов расширения.

Поддержка интерфейса [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) . для Windows 7 Windows wic компонента обработки изображений (wic) требует, чтобы были реализованы все интерфейсы параметров, предоставляемые [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .

Поддержка состояния ориентации:

-   90. повороты изображений шага следует применять с помощью метода [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**сетротатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) . приложения и Windows используют этот метод для смены изображений (а также кэшированных эскизов и предварительных версий).
-   Применение поворота с помощью этого API также должно сохраняться кодеком (см. ранее в этом документе).
-   Приложения могут использовать возможности вращения API [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , но кодек не будет выполнять сериализацию параметров вращения для этого API, поэтому вращение, выполненные с помощью [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) , не будут сохранены.

Поддержка высокоскоростного просмотра эскизов и извлечения. если размерность предварительной версии измерения в пикселях (ширина или высота) меньше 1024 пикселей, Windows Vista запросит отрисовку для предварительного просмотра экрана:

-   Метод [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**сетрендермоде**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) должен поддерживать как минимум режимы [**викраврендеркуалитидрафтмоде**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) и [**викраврендеркуалитибесткуалити**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawrendermode) , чтобы обеспечить более быструю визуализацию эскизов и предварительного просмотра, чем режим полного качества.
-   Windows будет вызывать [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) с запрошенным размером разрешения экрана.
-   Размеры разрешения экрана должны поддерживаться в приведенном выше API.
-   Требуется последовательная обработка изображений эскизов эскиза, предварительного просмотра и полных битов изображений из [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) .

Форматы пикселей с высоким динамическим диапазоном (HDR).

Печать в формате XPS.

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

 

 



