---
description: эта статья относится к Windows Vista и более поздних версий.
ms.assetid: 4d88806a-68a6-4394-a704-c7a47a0fdc70
title: интеграция с Windows фотоальбома и обозревателем Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85e20b690e2640fb40830721f1c6a3211641d81311724be2c70efae3781171e8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119549444"
---
# <a name="integration-with-windows-photo-gallery-and-windows-explorer"></a>интеграция с Windows фотоальбома и обозревателем Windows

эта статья относится к Windows Vista и более поздних версий. Он содержит следующие подразделы:

-   [Введение](#introduction)
-   [интеграция с хранилищем свойств Windows](#integration-with-the-windows-property-store)
-   [интеграция с фотоальбомом Windows](#integration-with-the-windows-photo-gallery)
-   [интеграция с кэшем эскизов Windows](#integration-with-the-windows-thumbnail-cache)
-   [Связанные темы](#related-topics)

## <a name="introduction"></a>Введение

чтобы включить Windows фотоальбом и обозреватель Windows для просмотра эскизов и поиска и обновления стандартных метаданных изображения, кодек должен иметь связанную с ним реализацию интерфейсов [исумбнаилпровидер](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) и [ипропертисторе](/windows/win32/api/propsys/nn-propsys-ipropertystore) . Интерфейс Исумбнаилпровидер используется для получения эскизов и заполнения кэша эскизов, а интерфейс Ипропертисторе используется для поиска и обновления метаданных, связанных с файлом. начиная с Windows Vista все типы файлов имеют эскизы и метаданные, но для разных типов файлов требуются разные реализации этих интерфейсов для извлечения или создания эскизов и метаданных для них. Система предоставляет реализации по умолчанию этих интерфейсов. реализацию исумбнаилпровидер по умолчанию можно использовать для Windows любого формата изображения, поддерживающего компонент imaging (WIC). Реализация Ипропертисторе по умолчанию может использоваться с любым форматом изображений с поддержкой WIC, основанным на формате TIFF или в контейнере JPEG. Чтобы связать формат изображения с реализациями по умолчанию обоих интерфейсов, необходимо добавить лишь несколько записей реестра.

следующие записи указывают на Windows фотоальбом и Windows Explorer, что расширение имени файла (ext) и связанный с ним тип MIME связаны с форматом изображения.

следующая запись обозначает Windows и приложения, использующие тип содержимого (также известный как тип mime), что файл с заданным расширением (ext) имеет формат изображения. Владелец типа файла должен выбрать `<image sub type value>` , который однозначно определяет формат файла, и это значение типа содержимого должно быть зарегистрировано в IANA.

```
HKEY_CLASSES_ROOT
   {.ext}
      ContentType = image/<image sub type>
```

следующая запись обозначает Windows, Windows поиск и приложения, использующие [System. Kind](../properties/props-system-kind.md) , что расширение имени файла (ext) должно рассматриваться как изображение. В частности, это означает, что свойству System. Kind расширения файла должно быть присвоено значение Picture.

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

## <a name="integration-with-the-windows-property-store"></a>интеграция с хранилищем свойств Windows

Иногда одни и те же свойства метаданных предоставляются в разных схемах метаданных, часто с разными именами свойств. Когда одно из этих свойств обновляется, но другие — нет, метаданные в файле могут оказаться несинхронизированными. обработчик свойств photo предоставляет **ипропертисторе** реализацию по умолчанию для изображений и используется приложениями, а также фотоальбомом Windows и обозревателем Windows, чтобы гарантировать синхронизацию всех метаданных в образе и отображение свойств, отображаемых приложениями, в фотоальбоме Windows и обозревателе Windows. Когда обработчик свойства Photo обновляет метаданные, гарантируется согласованность этих свойств по всем общим форматам метаданных, присутствующим в файле.

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

## <a name="integration-with-the-windows-photo-gallery"></a>интеграция с фотоальбомом Windows

Windows Фотоальбом построен на основе WIC и может отображать любой формат изображений с поддержкой WIC, для которого установлен кодек. чтобы уведомить систему о том, что ваш формат изображения можно открыть в фотоальбоме Windows, необходимо создать сопоставление файлов, создав следующие записи реестра.

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

ProgID обычно является расширением имени файла, к которому добавляется слово «File». (Например, если расширение имени файла .txt, ProgID обычно имеет значение "ткстфиле".)

Существуют и другие стандартные записи реестра, которые может потребоваться создать для поддержки сопоставлений файлов. Однако, поскольку се'и не относятся к WIC, они выходят за рамки данного раздела.

## <a name="integration-with-the-windows-thumbnail-cache"></a>интеграция с кэшем эскизов Windows

Следующие две записи указывают, что стандартную реализацию поставщика снимков WIC можно использовать для получения эскизов файлов с этим расширением. Первым идентификатором GUID является IID интерфейса [исумбнаилпровидер](/windows/win32/api/thumbcache/nn-thumbcache-ithumbnailprovider) , а вторым — идентификатор GUID стандартной системной реализации этого интерфейса. (Все записи в ХЛКР \\ . ext \\ шеллекс \\ повторяются в разделе HKCR \\ системфилеассоЦиатионс \\ . ext \\ шеллекс \\ .)

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      {.ext}
         ShellEx
            {e357fccd-a995-4576-b01f-234630154e96}
               (Default) = {C7657C4A-9F68-40fa-A4DF-96BC08EB3551}
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

**Зрения**
</dt> <dt>

[Записи реестра, относящиеся к кодировщику](-wic-decoderregentries.md)
</dt> <dt>

[Установка и регистрация КОДЕка](-wic-codecinstallandreg.md)
</dt> <dt>

[Написание WIC-Enabled КОДЕка](-wic-howtowriteacodec.md)
</dt> <dt>

[Windows Общие сведения о компонентах обработки изображений](-wic-about-windows-imaging-codec.md)
</dt> </dl>

 

 
