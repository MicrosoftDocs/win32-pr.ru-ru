---
description: Поддержка Ивикдевелоправ
ms.assetid: 8e8ff65b-0849-42e0-924e-2a7c61d4b1bb
title: Поддержка Ивикдевелоправ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa39aa339a3cd21c7ffa848a5ab1fe2dd6426981
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104265849"
---
# <a name="support-for-iwicdevelopraw"></a>Поддержка Ивикдевелоправ

Чтобы позволить приложениям поддерживать обработку в необработанном виде, разработчикам кодеков настоятельно рекомендуется реализовать все параметры [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw). Для Windows 7 компонент Windows Imaging Component (WIC) потребует поддержки всех [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw). Если формат файла не поддерживает все эти параметры, следует изменить формат файла изображения.

Чтобы включить базовую обработку RAW в приложениях, кодеки должны поддерживать корректировки для экспозиции (Експосурекомпенсатионсуппорт) и цвета (например, Келвинвхитепоинтсуппорт и Тинтсуппорт). Кроме того, настоятельно рекомендуется выводить данные в определенные цветовые пространства и форматы пикселей. Поддержка других корректировок —, конечно же, рекомендуется и требуется для Windows 7.

Кодек RAW должен обеспечивать базовую поддержку для смены изображений и быстрого просмотра. Поворот можно указать двумя разными способами:

-   Метод [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**сетротатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) . Этот метод задает желаемый угол вращения для выходных данных последующих вызовов [**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels).
-   Метод [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) . Вызывающий объект может установить параметр Дсттрансформ, чтобы указать желаемый угол поворота.

Эти два подхода отличаются следующими способами.

-   Только параметры [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) могут быть сохранены в экземплярах объекта декодера.
-   [**Ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) применяется только к этому конкретному вызову; сохраняемость любого типа отсутствует.
-   [**Ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) обеспечивает более детализированный контроль при повороте. [**Ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) ограничен приращениями в 90 градусов.

Если поворот указан как в [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) , так и в [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform), то этот эффекта является кумулятивным. Например, если [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) задает поворот на 25 градусов, а [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform) задает поворот на 90 градусов, то должно произойти следующее:

-   Вызовы [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) должны применять поворот на 25 градусов (то есть только величину, указанную в [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)).
-   Вызовы [**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels) с дсттрансформ суммой 90 затем приводят к повороту на 115 градусов (25 + 90).
-   Опять же, можно сохранить только поворот на 25 градусов, указанный с помощью [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**сетротатион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrotation) .

В Windows Vista методы [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode):: Ивикбитмапдекодер [**и**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) [](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**OnPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) позволяют вызывающим объектам получать внедренные эскизы и изображения предварительного просмотра соответственно. Они предназначены для возврата предварительно вычисленных предварительного просмотра и эскизов из потока файлов изображений. Создание предварительных или эскизов "на лету" приводит к снижению производительности в проводнике Windows и средстве просмотра фотографий. Кодек также должен предоставить способ для быстрого возврата обновленного изображения разрешения экрана, когда пользователи выполняют интерактивное управление параметрами обработки.

Вызовы [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**сетрендермоде**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-setrendermode) будут определять, какие последующие вызовы [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels) возвращают (что повышает скорость или качество). Кроме того, можно использовать интерфейс Ивикбитмапсаурцетрансформ, чтобы определить, требуется ли даунсамплинг, и повысить производительность, когда ее можно будет применить. Точность цвета всех изображений должна быть сравнима. При внесении изменений в параметры обработки все эти рендерингы должны отражать изменения.

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

 

 



