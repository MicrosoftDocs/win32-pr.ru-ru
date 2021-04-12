---
description: В разделе описывается декодер точечных рисунков — основной компонент кодека Windows Imaging Component (WIC), используемый для декодирования файлов изображений из потока.
ms.assetid: 9dc8d2ec-5cc5-45fa-8a4d-5bdc3072c90c
title: Общие сведения о декодировании
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a15e6a9c914cfa220e1aad5bff4badeb8fc8cc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104349872"
---
# <a name="decoding-overview"></a>Общие сведения о декодировании

В разделе описывается декодер точечных рисунков — основной компонент кодека Windows Imaging Component (WIC), используемый для декодирования файлов изображений из потока.

В этом разделе содержатся следующие подразделы.

-   [Введение](#introduction)
-   [Встроенные декодеры битовой карты](#native-bitmap-decoders)
-   [Создание растрового декодера](#creating-a-bitmap-decoder)
-   [Расширяемость декодера](#decoder-extensibility)
-   [См. также](#related-topics)

## <a name="introduction"></a>Введение

Растровые декодеры можно просматривать как внешний контейнер цифрового изображения и предоставлять доступ к глобальным свойствам и кадрам изображений. Некоторые форматы изображений поддерживают глобальные эскизы, обзоры, контексты цвета или метаданные, а другие предоставляют эти свойства только на уровне фрейма. Однако обратите внимание, что многие стандартные форматы изображений не поддерживают эти глобальные свойства. Таким образом, многие реализации собственных кодеков, предоставляемые компонентом WIC, не поддерживают большинство этих глобальных свойств. Сведения о поддержке глобальных свойств см. в таблице в разделе декодеры машинного кода в этом разделе.

В WIC декодеры битовой карты представлены интерфейсом [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) и предоставляют доступ к этим глобальным свойствам точечного рисунка и, что более важно, к кадрам, которые он содержит. Интерфейс [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) представляет отдельный кадр точечного рисунка, который подробно обсуждается в разделе [Общие сведения об источниках битовой карты](-wic-bitmapsources.md).

## <a name="native-bitmap-decoders"></a>Встроенные декодеры битовой карты

WIC предоставляет несколько собственных реализаций интерфейса [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) для стандартных форматов веб-изображений и высокоскоростного формата Фото HD. В следующей таблице перечислены доступные встроенные декодеры, имя идентификатора класса и поддержка глобальных свойств. Хотя функция может не поддерживать такие свойства, как эскизы на глобальном уровне, формат изображения может поддерживать такие свойства на уровне отдельных кадров.



| Формат образа | Имя CLSID            | Эскизы | Предварительный просмотр | Контексты цвета | Метаданные |
|--------------|-----------------------|------------|----------|----------------|----------|
| BMP          | \_ВИКБМПДЕКОДЕР CLSID  | Нет         | Нет       | Нет             | Нет       |
| GIF          | \_ВИКГИФДЕКОДЕР CLSID  | Нет         | Нет       | Нет             | Да      |
| ICO          | \_ВИЦИКОДЕКОДЕР CLSID  | Нет         | Нет       | Нет             | Нет       |
| JPEG         | \_ВИКЖПЕГДЕКОДЕР CLSID | Нет         | Нет       | Нет             | Нет       |
| PNG          | \_ВИКПНГДЕКОДЕР CLSID  | Нет         | Нет       | Нет             | Нет       |
| TIFF         | \_ВИКТИФФДЕКОДЕР CLSID | Нет         | Нет       | Нет             | Нет       |
| Фото HD     | \_ВИКВМПДЕКОДЕР CLSID  | Нет         | Да      | Нет             | Нет       |



 

## <a name="creating-a-bitmap-decoder"></a>Создание растрового декодера

Чтобы декодировать изображение с помощью WIC, сначала необходимо создать экземпляр [**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) для целевого формата образа. Экземпляр декодера позволяет получить доступ к глобальным свойствам и метаданным, если они поддерживаются, а также к кадрам изображений. Фабрика обработки изображений WIC, [**IWICImagingFactory**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory), предоставляет несколько методов для создания декодеров битовой карты. Для создания декодеров точечных рисунков предоставляются следующие заводские методы.

-   [**креатедекодер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoder)
-   [**креатедекодерфромфилехандле**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilehandle)
-   [**креатедекодерфромфиленаме**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromfilename)
-   [**креатедекодерфромстреам**](/windows/desktop/api/Wincodec/nf-wincodec-iwicimagingfactory-createdecoderfromstream)

В следующем коде показано, как создать растровый декодер с помощью имени файла изображения и получить первый кадр изображения.


```C++
   // Create a decoder
   IWICBitmapDecoder *pDecoder = NULL;

   hr = m_pIWICFactory->CreateDecoderFromFilename(
       szFileName,                      // Image to be decoded
       NULL,                            // Do not prefer a particular vendor
       GENERIC_READ,                    // Desired read access to the file
       WICDecodeMetadataCacheOnDemand,  // Cache metadata when needed
       &pDecoder                        // Pointer to the decoder
       );

   // Retrieve the first frame of the image from the decoder
   IWICBitmapFrameDecode *pFrame = NULL;

   if (SUCCEEDED(hr))
   {
       hr = pDecoder->GetFrame(0, &pFrame);
   }
```



## <a name="decoder-extensibility"></a>Расширяемость декодера

Одной из основных функций WIC является инфраструктура расширяемости, которая позволяет разработчикам кодеков разрабатывать собственные кодеки изображений и получать ту же поддержку платформ, что и собственные реализации кодеков изображений. Один последовательный набор интерфейсов используется для обработки изображений независимо от формата изображения. Любое приложение, использующее WIC, получает автоматическую поддержку новых форматов изображений сразу после установки кодека. Дополнительные сведения о разработке кодеков см. в разделах, посвященных [разработке компонентов](-wic-component-development.md). Дополнительные сведения о разработке декодеров см. в разделе [Реализация декодера WIC-Enabled](-wic-implementingwicdecoder.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Общие сведения о кодировке](-wic-creating-encoder.md)
</dt> <dt>

[Разработка компонентов](-wic-component-development.md)
</dt> </dl>

 

 



