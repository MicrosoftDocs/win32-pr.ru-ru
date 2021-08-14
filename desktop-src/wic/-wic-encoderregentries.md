---
description: Encoder-Specific записи реестра
ms.assetid: bbb78d70-bd3e-4d5a-ba59-2e17d2d1cf30
title: Encoder-Specific записи реестра
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83d5d91d917be3940bcece4bed7c224e0f281dbb1cade5d0dc2c25872f89af93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118711233"
---
# <a name="encoder-specific-registry-entries"></a>Encoder-Specific записи реестра


кроме перечисленных выше записей для кодировщика, необходимо также зарегистрировать кодировщик в категории кодировщиков Windows imaging Component (WIC), чтобы механизм обнаружения мог его найти. Для этого необходимо внести в реестр следующие записи. Первым идентификатором GUID в следующих записях является идентификатор категории (CATID) для Викбитмапенкодерс.

```
HKEY_CLASSES_ROOT
   CLSID
      {AC757296-3522-4E11-9862-C17BE5A1767E}
         Instance
            {Encoder CLSID}
               CLSID = {Encoder CLSID}
               FriendlyName = {Name of Encoder}
```

## <a name="registering-a-container-format-with-metadata-writers"></a>Регистрация формата контейнера с помощью модулей записи метаданных

При создании нового формата контейнера для кодека необходимо также создать записи реестра для поддержки модулей записи метаданных для блоков метаданных в изображениях. Следующие записи должны быть созданы с идентификатором класса (CLSID) модуля записи метаданных для каждого формата метаданных, поддерживаемого в вашем формате контейнера. Если кодек использует контейнер формата TIFF, эта информация уже находится в реестре и вам не нужно создавать эти записи.

```
HKEY_CLASSES_ROOT
   CLSID
      {Metadata Writer CLSID}
         Containers
            {Container Format GUID}
               WritePosition = Offset relative to its container
               WriteHeader = Pattern used for metadata header
               WriteOffset = Offset from beginning of header
```

Если используется формат контейнера в стиле TIFF или JPEG, необходимо зарегистрировать связь между контейнером и этим форматом контейнера. дополнительные сведения см. в статье введение в [интеграцию с Windows фотоальбома и обозревателем Windows](-wic-integrationregentries.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Общие записи реестра](-wic-generalregentries.md)
</dt> <dt>

[Записи реестра, относящиеся к кодировщику](-wic-decoderregentries.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Общие сведения о компонентах обработки изображений](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 



