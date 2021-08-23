---
description: Требования к методам интерфейса
ms.assetid: 8c2afeb3-3e0b-4f8a-a2f4-df7c9ce4b098
title: Требования к методам интерфейса
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8525f7b04fe82247ecd64a38f5f1acc298be5d3ace56303072268fed6a4a3cfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119086927"
---
# <a name="interface-method-requirements"></a>Требования к методам интерфейса

Не каждый метод в каждом интерфейсе должен иметь реализацию. Например, некоторые кодеки имеют глобальные метаданные, эскизы или цветовые контексты, тогда как другие кодеки предоставляют их только для отдельных кадров. Если авторы кодека предоставляют их только для каждого фрейма, им нужно только реализовать [**Get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) или колорконтекстс или реализовать методы [**жетметадатакуериреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader) или [**жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-getmetadataquerywriter) в [**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode) и [**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode) , а не в [**IWICBitmapDecoder**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder) и [**IWICBitmapEncoder**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder). Аналогично, некоторые кодеки не используют Индексированные форматы, поэтому не требуется реализовывать методы [**копипалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette) и [**сетпалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpalette) . Таким образом, эти методы являются необязательными и остаются на усмотрение создателя кодека. Большинство других методов являются обязательными.

для Windows 7 [**get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview) / [**сетпревиев**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) и [**get**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) / [**сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) являются обязательными и должны быть реализованы в классах на уровне вложения или в классах уровня кадров. Если формат файла изображения не поддерживает предварительный просмотр или эскизы в любом из этих расположений, следует изменить формат файла изображения, чтобы обеспечить такую поддержку.

Если метод не реализован, важно вернуть соответствующую ошибку, чтобы вызывающий объект мог определить, что запрошенная функция не поддерживается. Например, если авторы кодека не поддерживают эскизы на уровне контейнера, они должны возвращать [винкодек \_ Err \_ кодекносумбнаил](-wic-codec-error-codes.md) , когда приложение вызывает метод- [**эскиз**](-wic-codec-iwicbitmapdecoder-getthumbnail-proxy.md), и если у них нет палитры, они должны возвращать [винкодек \_ Err \_ палеттеунаваилабле](-wic-codec-error-codes.md). Если подходящий код [ \_ Err винкодек](-wic-codec-error-codes.md) не существует, кодек должен вернуть E \_ нотимпл для нереализованных методов.

в следующих таблицах перечислены обязательные и необязательные методы для каждого интерфейса компонента обработки изображений Windows (WIC).

[**ивикбитмапдекодер**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapdecoder)



Обязательно

[**куерикапабилити**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-querycapability)

[**Инициализация**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-initialize)

[**жетконтаинерформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcontainerformat)

[**жетдекодеринфо**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getdecoderinfo)

[**жетфрамекаунт**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframecount)

[**GetFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getframe)

Необязательно

[**OnPreview**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getpreview)¹

[**Эскиз**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail)²

[**жетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getcolorcontexts)

[**жетметадатакуериреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getmetadataqueryreader)

[**копипалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

¹ требуется, если формат файла изображения поддерживает предварительные версии уровня контейнера. Если это не так, настоятельно рекомендуется изменить формат файла изображения для поддержки этой ситуации. Если реализуется здесь, то для класса кодирования на уровне контейнера требуется соответствующий [**сетпревиев**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview) .

в зависимости от того, где в формате файла изображения хранятся эскизы, необходимо ввести ² или на класс декодирования на уровне кадров. Если реализуется здесь, то для класса кодирования на уровне контейнера требуется соответствующий [**сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail) .

[**IWICBitmapFrameDecode**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframedecode)



Обязательно

[**жетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getcolorcontexts)

[**жетметадатакуериреадер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getmetadataqueryreader)

[**GetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getsize)

[**жетпикселформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getpixelformat)

[**Решение с высоким разрешением**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-getresolution)

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypixels)

Необязательно

[**Эскиз**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail)¹

[**копипалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-copypalette)



 

¹, требуемое здесь, или на классе декодирования на уровне контейнера, в зависимости от того, в каком месте изображения хранятся эскизы форматов файлов. При реализации здесь для класса кодировщика на уровне кадров требуется соответствующий [**сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail) .

[**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



Обязательно

[**жетконтаинерформат**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcontainerformat)

[**GetCount**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getcount)

[**жетреадербиндекс**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getreaderbyindex)

[**GetEnumerator**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockreader-getenumerator)



 

[**ивикбитмапсаурцетрансформ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapsourcetransform)



Обязательно

[**доессуппорттрансформ**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-doessupporttransform)

[**CopyPixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-copypixels)

Необязательно

[**жетклосестсизе**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestsize)

[**жетклосестпикселформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsourcetransform-getclosestpixelformat)



 

[**ивикдевелоправ**](/windows/desktop/api/Wincodec/nn-wincodec-iwicdevelopraw)

См. раздел [Поддержка ивикдевелоправ](./-wic-rawguidelines-iwicdevelopraw.md)далее в этом документе.

[**ивикбитмапенкодер**](/windows/desktop/api/wincodec/nn-wincodec-iwicbitmapencoder)



Обязательно

[**Инициализация**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[**жетконтаинерформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getcontainerformat)

[**жетенкодеринфо**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getencoderinfo)

[**CreateNewFrame**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-createnewframe)

[**Фиксация**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

Необязательно

[**Сетпревиев**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setpreview)¹

[**Сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setthumbnail)²

[**сетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-setcolorcontexts)

[**жетметадатакуеривритер**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-getmetadataquerywriter)

[**сетпалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmap-setpalette)



 

¹ требуется, если формат файла изображения поддерживает предварительный просмотр на уровне кадров.

в зависимости от того, где в формате файла изображения хранятся эскизы, требуется ², или для класса кодирования на уровне кадров. Если реализуется здесь, то для класса декодирования на уровне контейнера [**требуется соответствующий параметр ","**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapdecoder-getthumbnail) .

[**ивикбитмапфраминкоде**](/windows/desktop/api/Wincodec/nn-wincodec-iwicbitmapframeencode)



Обязательно

[**Инициализация**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-initialize)

[**сетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[**сетколорконтекстс**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setcolorcontexts)

[**SetSize**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setsize)

[**сетпикселформат**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setpixelformat)

[**сетресолутион**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setresolution)

[**WritePixels**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writepixels)

[**вритесаурце**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-writesource)

[**Фиксация**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapencoder-commit)

Необязательно

[**Сетсумбнаил**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframeencode-setthumbnail)¹

[**копипалетте**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapsource-copypalette)



 

¹, требуемое здесь, или в классе кодирования уровня контейнера, в зависимости от того, где хранятся эскизы в формате файлов изображений. Если реализуется здесь, то для класса декодирования на уровне кадров [**требуется соответствующий параметр**](/windows/desktop/api/Wincodec/nf-wincodec-iwicbitmapframedecode-getthumbnail) «NOFRAMES».

[**ивикметадатаблоккреадер**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwicmetadatablockreader)



Обязательно

[**инитиализефромблоккреадер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-initializefromblockreader)

[**аддвритер**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-addwriter)

[**жетвритербиндекс**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-getwriterbyindex)

[**сетвритербиндекс**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-setwriterbyindex)

[**ремовевритербиндекс**](/windows/desktop/api/Wincodecsdk/nf-wincodecsdk-iwicmetadatablockwriter-removewriterbyindex)



 

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

 

 
