---
description: Дата приобретения файла или носителя.
ms.assetid: 7c673d21-5243-4e41-91df-c5d84aaf620a
title: System. Датеаккуиред
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a78ae9ccfe938551ab6c4a265972e48c3aad1c1791f02cfa933c583c6d4b0d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119599184"
---
# <a name="systemdateacquired"></a>System. Датеаккуиред

Дата приобретения файла или носителя. Это свойство связано с определенным пользователем или группой пользователей. Например, эти данные используются в качестве основной оси сортировки для виртуальной папки **Новая музыка**, что позволяет пользователям просматривать последние дополнения к их коллекции.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="windows-vista"></a>Windows Vista

```
propertyDescription
   name = System.DateAcquired
   shellPKey = PKEY_DateAcquired
   formatID = 2CBAA8F5-D81F-47CA-B17A-F8D822300131
   propID = 100
   SearchInfo
      IsColumn = true
   typeInfo
      type = DateTime
```

## <a name="remarks"></a>Remarks

Значения PKEY определены в списке PKEY. h.

[Датеаккуиред]() хранится в виде значения в основном потоке файла, но он может не всегда присутствовать. В этих случаях Дата приобретения может быть приблизительна на основе других известных дат содержимого. Обработчик метаданных должен использовать набор правил для определения даты, которую необходимо вернуть. В следующем примере демонстрируется использование музыкальных файлов.

-   Для приобретенной музыки следует использовать время создания файла, если приобретенная Дата не указана. Однако поставщик загрузки должен задать свойство [датеаккуиред]() в файле.
-   Чтобы музыкальные файлы были скопированы пользователем или группой (копирование музыки или видео с компакт-диска или DVD-диска на жесткий диск), Дата приобретения должна быть датой выполнения действия. Например, атрибут [WM/енкодингтиме](../wmp/wm-encodingtime-attribute.md) .
-   Для музыкальных файлов, скопированных из другого расположения, в качестве даты приобретения следует использовать время создания файла.

Примерами [System. датеаккуиред]() являются Дата и время получения изображений с камеры или приобретения музыки через Интернет. Это не то же самое, что [System. датеимпортед](./props-system-dateimported.md).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[пропертидескриптион](./propdesc-schema-propertydescription.md)
</dt> <dt>

[сеарчинфо](./propdesc-schema-searchinfo.md)
</dt> <dt>

[лабелинфо](./propdesc-schema-labelinfo.md)
</dt> <dt>

[typeInfo](./propdesc-schema-typeinfo.md)
</dt> <dt>

[displayInfo](./propdesc-schema-displayinfo.md)
</dt> <dt>

[stringFormat](./propdesc-schema-stringformat.md)
</dt> <dt>

[булеанформат](./propdesc-schema-booleanformat.md)
</dt> <dt>

[numberFormat](./propdesc-schema-numberformat.md)
</dt> <dt>

[dateTimeFormat](./propdesc-schema-datetimeformat.md)
</dt> <dt>

[енумератедлист](./propdesc-schema-enumeratedlist.md)
</dt> <dt>

[дравконтрол](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[едитконтрол](./propdesc-schema-editcontrol.md)
</dt> <dt>

[филтерконтрол](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[куериконтрол](./propdesc-schema-querycontrol.md)
</dt> </dl>

 

 
