---
description: Этот раздел относится к Windows Vista и более поздним версиям.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: Интеграция с Фотоальбомом Windows и проводником Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b2ab2bb725b151a069f53a94a8fb2e31766132d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105647485"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a>Интеграция с Фотоальбомом Windows и проводником Windows

Этот раздел относится к Windows Vista и более поздним версиям. Он содержит следующие подразделы:

-   [Введение](#introduction)
-   [Интеграция с хранилищем свойств Windows](#integration-with-the-windows-property-store)
-   [Интеграция с Фотоальбомом Windows](#integration-with-the-windows-photo-gallery)
-   [Интеграция с кэшем эскизов Windows](#integration-with-the-windows-thumbnail-cache)
-   [См. также](#related-topics)

## <a name="introduction"></a>Введение

Чтобы включить в фотоальбоме Windows и проводнике Windows отображение эскизов и поиск и обновление метаданных стандартного образа, кодек должен иметь связанную с ним реализацию интерфейсов [исумбнаилпровидер](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) и [ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore) . Интерфейс Исумбнаилпровидер используется для получения эскизов и заполнения кэша эскизов, а интерфейс Ипропертисторе используется для поиска и обновления метаданных, связанных с файлом. Начиная с Windows Vista, все типы файлов имеют эскизы и метаданные, но для разных типов файлов требуются разные реализации этих интерфейсов для извлечения или создания эскизов и метаданных для них. Система предоставляет реализации по умолчанию этих интерфейсов. Реализация Исумбнаилпровидер по умолчанию может использоваться для любого формата изображения, поддерживающего Windows Imaging Component (WIC). Реализация Ипропертисторе по умолчанию может использоваться с любым форматом изображений с поддержкой WIC, основанным на формате TIFF или в контейнере JPEG. Чтобы связать формат изображения с реализациями по умолчанию обоих интерфейсов, необходимо добавить лишь несколько записей реестра.

Следующие записи указывают на Фотоальбом Windows и проводник Windows, что расширение имени файла (EXT) и связанный с ним тип MIME связаны с форматом изображения.

Следующая запись обозначает Windows и приложения, использующие тип содержимого (также известный как тип MIME), что файл с заданным расширением (EXT) имеет формат изображения. Владелец типа файла должен выбрать `<image sub type value>` , который однозначно определяет формат файла, и это значение типа содержимого должно быть зарегистрировано в IANA.

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

Следующая запись обозначает Windows, Поиск Windows и приложения, использующие [System. Kind](../properties/props-system-kind.md) , что расширение имени файла (EXT) должно рассматриваться как изображение. В частности, это означает, что свойству System. Kind расширения файла должно быть присвоено значение Picture.

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  KindMap
                     {.ext} = Picture
```

## <a name="integration-with-the-windows-property-store"></a>Интеграция с хранилищем свойств Windows

Иногда одни и те же свойства метаданных предоставляются в разных схемах метаданных, часто с разными именами свойств. Когда одно из этих свойств обновляется, но другие — нет, метаданные в файле могут оказаться несинхронизированными. Обработчик свойств Photo предоставляет **ипропертисторе** реализацию по умолчанию для изображений и используется приложениями, а также фотоальбомом Windows и проводником Windows, чтобы гарантировать синхронизацию всех метаданных в образе и отображение свойств, отображаемых приложениями, в фотоальбоме Windows и проводнике Windows. Когда обработчик свойства Photo обновляет метаданные, гарантируется согласованность этих свойств по всем общим форматам метаданных, присутствующим в файле.

Обработчик свойства Photo должен понимать формат контейнера и способ определения различных свойств в нем. В целом, обработчик свойства Photo не может узнать, как различные блоки метаданных размещаются в собственном формате контейнера. Однако если метаданные в вашем формате контейнера размещаются так же, как метаданные в формате контейнера TIFF или в формате контейнера JPEG, то обработчик свойства Photo может воспользоваться этими знаниями для согласованного обновления метаданных в вашем формате контейнера.

Эту связь можно зарегистрировать, создав следующую запись реестра. Эта запись сообщает обработчику свойства Photo, что формат контейнера, идентифицируемый этим идентификатором GUID, распознает те же пути языка запросов метаданных, что и формат контейнера с идентификатором GUID 163bcc30-e2e9-4f0b-961d-a3e9fdb788a3. (163bcc30-e2e9-4f0b-961d-a3e9fdb788a3 — это идентификатор GUID для формата контейнера TIFF.)

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  ContainerAssociations
                     {Container Format GUID} = {163bcc30-e2e9-4f0b-961d-a3e9fdb788a3}
```

Следующая запись связывает стандартную реализацию **ипропертисторе** обработчика свойства Photo с файлами с расширением ext. Первым идентификатором GUID является IID интерфейса **ипропертисторе** , а вторым — идентификатор GUID его реализации обработчика свойства Photo.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PhotoPropertyHandler
                  {.ext}
                     (Default) = {a38b883c-1682-497e-97b0-0a3a9e801682}
```

Кодеки, использующие собственный формат, несовместимый с форматом контейнера TIFF или JPEG, должны записывать собственную реализацию **ипропертисторе** .

## <a name="integration-with-the-windows-photo-gallery"></a>Интеграция с Фотоальбомом Windows

Фотоальбом Windows построен на основе WIC и может отображать любой формат изображений с поддержкой WIC, для которого установлен кодек. Чтобы уведомить систему о том, что ваш формат изображения можно открыть в фотоальбоме Windows, необходимо создать сопоставление файлов, создав следующие записи реестра.

```
HKEY_CLASSES_ROOT
   {.ext}
      (Default) = {ProgID} for example, jpegfile)
      OpenWithProgids
         {ProgID}
      OpenWithList
         PhotoViewer.dll
      ShellEx
         ContextMenuHandlers
            ShellImagePreview
               (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   SystemFileAssociations
      {.ext}
         OpenWithList
            PhotoViewer.dll
         ShellEx
            ContextMenuHandlers
               ShellImagePreview
                  (Default) = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
   {Image Format ProgID}
      (Default) = Name of Image Format
      DefaultIcon
         (Default) = Path to icon for type, icon index
      shell
         open
            MuiVerb = @%PROGRAMFILES%\Windows Photo Gallery\photoviewer.dll,-3043
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%ProgramFiles%\Windows Photo Gallery\PhotoViewer.dll", ImageView_Fullscreen %1
            DropTarget
               Clsid = {FFE2A43C-56B9-4bf5-9A79-CC6D4285608A}
         printo
            command
               (Default) = %SystemRoot%\System32\rundll32.exe "%SystemRoot%\System32\shimgvw.dll", ImageView_PrintTo /pt "%1" "%2" "%3" "%4"
```

ProgID обычно является расширением имени файла, к которому добавляется слово «File». (Например, если расширение имени файла — txt, ProgID обычно имеет значение "ткстфиле".)

Существуют и другие стандартные записи реестра, которые может потребоваться создать для поддержки сопоставлений файлов. Однако, поскольку се'и не относятся к WIC, они выходят за рамки данного раздела.

## <a name="integration-with-the-windows-thumbnail-cache"></a>Интеграция с кэшем эскизов Windows

Следующие две записи указывают, что стандартную реализацию поставщика снимков WIC можно использовать для получения эскизов файлов с этим расширением. Первым идентификатором GUID является IID интерфейса [исумбнаилпровидер](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) , а вторым — идентификатор GUID стандартной системной реализации этого интерфейса. (Все записи в ХЛКР \\ . ext \\ шеллекс \\ повторяются в разделе HKCR \\ системфилеассоЦиатионс \\ . ext \\ шеллекс \\ .)

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Записи реестра, относящиеся к кодировщику](-wic-decoderregentries.md)
</dt> <dt>

[Установка и регистрация КОДЕка](-wic-codecinstallandreg.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Общие сведения о компоненте создания образов Windows](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
