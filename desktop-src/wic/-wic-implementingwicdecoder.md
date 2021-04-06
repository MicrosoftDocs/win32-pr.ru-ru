---
description: 'Дополнительные сведения: реализация декодера WIC-Enabled'
ms.assetid: a26a592d-42ef-4690-95b4-48a5324be75a
title: Реализация декодера WIC-Enabled
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebd6d56258bf18e6cc914a40efa4cd3a57a92fc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911380"
---
# <a name="implementing-a-wic-enabled-decoder"></a>Реализация декодера WIC-Enabled


Для реализации декодера компонента обработки изображений Windows (WIC) требуется написание двух классов. Интерфейсы в этих классах непосредственно соответствуют обязанностям декодера, описанным в разделе [декодирование](-wic-howwicworks.md) [принципа работы компонента Windows Imaging](-wic-howwicworks.md).

Один из классов предоставляет службы уровня контейнера и реализует интерфейс [ивикбитмапдекодер](-wic-imp-iwicbitmapdecoder.md) . Если формат изображения поддерживает метаданные уровня контейнера, необходимо также реализовать интерфейс [ивикметадатаблоккреадер](-wic-imp-iwicmetadatablockreader.md) для этого класса. Рекомендуется поддерживать интерфейс [ивикбитмапкодекпрогресснотификатион](-wic-imp-iwicbitmapcodecprogressnotification-decoder.md) как для декодера, так и для кодировщика, чтобы обеспечить лучшее взаимодействие с пользователем.

Другой класс, который вы реализуете, предоставляет службы на уровне кадров и выполняет фактическое декодирование битов изображения для каждого кадра в контейнере. Этот класс реализует интерфейс [IWICBitmapFrameDecode](-wic-imp-iwicbitmapframedecode.md) и интерфейс [ивикметадатаблоккреадер](-wic-imp-iwicmetadatablockreader.md) . При написании декодера для необработанного формата в этом классе также реализуется интерфейс [ивикдевелоправ](-wic-imp-iwicdevelopraw.md) . В дополнение к необходимым интерфейсам настоятельно рекомендуется реализовать интерфейс [ивикбитмапсаурцетрансформ](-wic-imp-iwicmetadatablockreader.md) для этого класса, чтобы обеспечить наилучшую производительность для вашего формата изображения.

Одним из объектов, предоставляемых компонентом WIC, является [**имагингфактори**](/windows/desktop/api/Wincodec/nn-wincodec-iwicimagingfactory). Интерфейс [**ивиккомпонентфактори**](/windows/desktop/api/Wincodecsdk/nn-wincodecsdk-iwiccomponentfactory) для этого объекта часто используется для создания различных компонентов. Так как он часто используется, следует ссылаться на него как на свойство члена в классах декодера и кодировщика.


```C++
IWICImagingFactory* m_pImagingFactory = NULL;
IWICComponentFactory* m_pComponentFactory = NULL;
HRESULT hr;
      
hr = CoCreateInstance(CLSID_WICImagingFactory, NULL,
  CLSCTX_INPROC_SERVER, IID_IWICImagingFactory,
  (LPVOID*) m_pImagingFactory);

hr = m_pImagingFactory->QueryInterface(
  IID_IWICComponentFactory, (void**)&m_pComponentFactory);
```



## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Принцип работы компонента Windows Imaging](-wic-howwicworks.md)
</dt> <dt>

[Интерфейсы декодера](-wic-decoderinterfaces.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[Общие сведения о метаданных компонента WIC](-wic-about-metadata.md)
</dt> <dt>

[Общие сведения о кодировке](-wic-creating-encoder.md)
</dt> </dl>

 

 



