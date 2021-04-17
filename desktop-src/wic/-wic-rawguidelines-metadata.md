---
description: Поддержка метаданных
ms.assetid: f3b4a3d9-a353-4af8-9998-cb7da7a062b7
title: Поддержка метаданных
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32499a88bd9cc12186629476f4d9f32a6e811858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105702737"
---
# <a name="metadata-support"></a>Поддержка метаданных

Форматы RAW также должны поддерживать общие сценарии чтения и записи метаданных для изображений в Windows. Корпорация Майкрософт разработала набор собственных поставщиков метаданных для файла с файлами изображений (EXIF), Международного Совета по Прессским коммуникациям (IPTC) и метаданных XMP, которые в настоящее время вызываются только для контейнеров TIFF и JPEG. Если необработанный образ хранится в одном из этих форматов контейнеров, рекомендуется использовать встроенные поставщики метаданных Windows. Однако автор кодека отвечает за правильную настройку. Для необработанных файлов, которые не основаны на контейнере TIFF, может потребоваться реализовать модули записи EXIF, IPTC или XMP, так как встроенные средства чтения и записи предполагают, что данные будут соответствовать спецификациям макета на диске EXIF, IPTC и XMP. Авторы кодеков также могут реализовать собственные поставщики для любых пользовательских метаданных.

Из-за архитектуры компонента Windows Imaging Component (WIC) средства записи метаданных могут вызываться только через экземпляр кодировщика изображений. Поэтому владельцы формата RAW должны создать по крайней мере "заглушку" [**викравпараметерсет. викаутоаджустедпараметерсет**](/windows/desktop/api/Wincodec/ne-wincodec-wicrawparameterset) кодировщик, даже если фактическая кодировка пикселей в необработанном формате не реализована. Автор кодека должен вызывать правильные обработчики метаданных:

-   [**Ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader) как для декодера, так и для декодера кадров.
-   [**Ивикметадатаблокквритер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockwriter) кодировщика и кодировщика фреймов соответствующим образом.

Для поддержки всех ожидаемых сценариев в приложениях для работы с образами в Windows Vista рекомендуется, чтобы поставщики кодеков поддерживали следующее как минимум:

-   Чтение EXIF
-   Частичная запись EXIF (для разрешения обновления даты и времени записи)
-   Чтение и запись XMP (включая, возможно, IPTC Core для XMP)
-   Чтение и запись IPTC IIMv4

Большая часть доступа к метаданным (как для чтения, так и для записи) в Windows Vista осуществляется через интерфейс [**ивикметадатакуериреадер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataqueryreader) или [**ивикметадатакуеривритер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicmetadataquerywriter) . Таким образом, чтобы участвовать в работе с метаданными в Windows Vista, авторы необработанных кодеков должны реализовать методы [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)::[**жетметадатакуериреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) и [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)::[**жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) .

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

 

 



