---
description: Общие записи реестра
ms.assetid: 6a140c7f-df8c-4a8e-9e4d-dbb38901e14f
title: Общие записи реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7420124f47f904712c7e955465b88972e77c8eeac26a6d42eca7fcb306ec158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118033131"
---
# <a name="general-registry-entries"></a>Общие записи реестра


Следующие записи реестра должны быть сделаны отдельно для декодера и кодировщика:

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Encoder/Decoder CLSID}
         Author = Author's Name
         Description = Your Codec Description
         DeviceManufacturer = Manufacturer's Name
         DeviceModels = Device,Device
         FriendlyName = Codec Friendly Name
         Date = mm-dd-yyyy
         Vendor = {GUID_Vendor}
         ContainerFormat = {GUID_ContainerFormat}
         Version = Major.Minor.Build.Number
         SpecVersion = Major.Minor.Build.Number
         MimeTypes = Your Mime Type
         SupportAnimation = 0|1
         SupportChromakey = 0|1
         SupportLossless = 0|1
         SupportMultiframe = 0|1
         Formats
            {Supported PixelFormat GUID 1}
            {Supported PixelFormat GUID ...}
            {Supported PixelFormat GUID N}
         ArbitrationPriority  = 0-10
```

Записи FriendlyName, Вендоргуид, Контаинерформат, Миметипес, FileExtensions и formats являются обязательными. Все остальные являются необязательными.

Обратите внимание, что записи Девицемануфактурер и DeviceModels относятся к необработанным кодекам и относятся к производителю камеры и моделям камеры, к которым применим кодек. Версия спецификации — это версия спецификации формата изображения, которая соответствует кодеку. В записи formats указываются форматы пикселей, поддерживаемые кодеком. Кодек может поддерживать более одного формата пикселей. В этом случае вы вводите несколько ключей в \_ \_ форматах корневого CLSID класса hKey \\ \\ (CLSID/кодировщик) \\ .

## <a name="arbitrationpriority"></a>арбитратионприорити

начиная с Windows 8 арбитратионприорити — это новая запись реестра. Допустимые значения: от 0 до 10. При наличии ключа Арбитратионприорити значение этого параметра указывает компоненту WIC определить приоритет связанного кодека для других кодеков с меньшим значением Арбитратионприорити. Эта оценка происходит до того, как будет вызвана существующая арбитражка кодека WIC и обеспечивает приоритет для соответствующего кодека под любым конкурирующим кодеком, даже если он является как или более мощным. Любой кодек, не имеющий явного значения Арбитратионприорити, определенного в реестре, по умолчанию имеет приоритет 0.

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Установка и регистрация КОДЕка](-wic-codecinstallandreg.md)
</dt> <dt>

[Записи реестра, относящиеся к кодировщику](-wic-encoderregentries.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Общие сведения о компонентах обработки изображений](-wic-about-windows-imaging-codec.md)
</dt> <dt>

[**как работает компонент работы с образами Windows: обнаружение и арбитраж кодеков**](-wic-howwicworks.md)
</dt> </dl>

 

 



