---
description: Рекомендации по реализации сериализации параметров Ивикдевелоправ
ms.assetid: 4ecff5cc-24f3-4b89-b681-85c867b053e7
title: Рекомендации по реализации сериализации параметров Ивикдевелоправ
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 48cdc78f68e6d63ee7870b9296ae4cfa4f85547a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103816081"
---
# <a name="implementation-guidelines-for-serializing-iwicdevelopraw-settings"></a>Рекомендации по реализации сериализации параметров Ивикдевелоправ

Интерфейс [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) предоставляет параметры, которые приложение может использовать для изменения обработки необработанного изображения. Параметры должны быть сериализованы, чтобы они сохранялись в разных сеансах. Хотя это может быть сделано несколькими способами, рекомендуется кодировать эти данные способом, согласованным с другими метаданными.

Ниже приведены некоторые общие рекомендации по реализации.

-   Любые параметры, сделанные через [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) (например, поворот или белый баланс), должны избегать перезаписи параметров камеры или данных "как-снимок", если только тег не используется в качестве текущего параметра. Например, Теги ориентации EXIF можно использовать для сохранения вращения.
-   Предпочтительно не сохранять весь файл (включая мозаику данных пикселей) каждый раз, когда запрашивается сериализация параметров [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) .
-   Процесс сериализации параметров [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) , как правило, соответствует этому порядку событий. Характеристики этого приложения:

    1.  Создает экземпляр [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) для необработанного файла.
    2.  Вызывает [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)::[**noframes**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe) , чтобы получить [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) для необработанного кадра.
    3.  Вызывает QueryInterface в интерфейсе IWICBitmapFrameDecode для интерфейса Ивикдевелоправ.
    4.  Вызывает метод [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**жеткуррентпараметерсет**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-getcurrentparameterset), который возвращает интерфейс IPropertyBag2 со всеми текущими свойствами, хранящимися в нем.

        На этом этапе процесса целью является сериализация параметров в интерфейсе IPropertyBag2 в необработанный файл. Для этого требуется вращение кодировщика и т. д., что подробно описано в следующих шагах.

    5.  Создает [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder) для необработанного файла.
    6.  Вызывает [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize), передавая новый (пустой) поток для кодирования.
    7.  Вызывает [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe) , чтобы создать новый ивикбитмапфраминкоде для необработанного кадра.
    8.  Вызывает [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**Initialize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)и передает интерфейс IPropertyBag2 из шага 4.
    9.  Вызывает [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**вритесаурце**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource) с [**IWICBitmapSource**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsource) из необработанного кадра изображения декодера.
    10. Вызывает [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit). Затем кодек Сериализует свойства в IPropertyBag2 из шага 8 в файл. Наиболее распространенным методом сериализации свойств является их запись в виде метаданных в файле.
    11. Вызывает [**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)::[**commit**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit).
    12. Вызывает метод IStream:: Commit в потоке на шаге 6.

    Параметры сериализуются в файле.

    Этот метод вызывает стоимость перезаписи всего необработанного файла каждый раз при сериализации параметров. Это можно избежать, если вы реализуете [**ивикфастметадатаенкодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) или если ваш формат файла изображения поддерживает XMP или EXIF, так как WIC предоставляет [**ивикфастметадатаенкодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicfastmetadataencoder) для обоих форматов. Кроме того, если ваш кодек записывает изменения в конец файла изображения, то вы не сможете переписать весь файл изображения.

-   Наборы параметров загружаются из сериализованного состояния, когда приложение задает перечисление [**викравпараметерсет. викусераджустедпараметерсет**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) в методе [**Ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)::[**лоадпараметерсет**](/windows/desktop/api/Wincodec/nf-wincodec-iwicdevelopraw-loadparameterset) . Флаг [**викравпараметерсет. викусераджустедпараметерсет**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) ссылается на последний сохраненный набор параметров, поэтому загрузка с этим флагом должна привести к восстановлению последнего сохраненного состояния.
-   После начальной загрузки необходимо загрузить последний сохраненный набор параметров, если он доступен. В противном случае в качестве предустановок для переменных интерфейса [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) следует использовать параметры "как-то". Эти параметры можно также загрузить с помощью флага [**викравпараметерсет. викасшотпараметерсет**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) .
-   Идентификатор [**викравпараметерсет. викаутоаджустедпараметерсет**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) предназначен для представления параметра Auto. Конструктор кодеков может выбрать любой из следующих подходов к настройке параметров [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) при установке этого параметра:

    -   Выполните алгоритмную оптимизацию некоторых параметров, например раскрытия или цвета. Таким образом, функции Auto в стандартных редакторах изображений и основаны на анализе пиксельных данных.
    -   Задайте параметры камеры так же, как при автоматическом задании параметров. Это полезно, если образ был установлен вручную и позволяет пользователю переопределить параметры вручную.
    -   Не делать ничего. Не все элементы управления должны быть заданы, если выбран параметр "Авто", и можно оставить параметры без изменений.

Фотоальбом Windows Vista и средства редактирования фотоальбома Windows Live и другие приложения для редактирования используют автоматическую загрузку параметров [**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw) , когда пользователь выбирает автозамену для всех обычных настроек элемента управления кодека, таких как цвет и экспозиция для получения лучших результатов.

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

 

 



