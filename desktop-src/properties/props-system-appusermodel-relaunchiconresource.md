---
description: Задает значок, используемый для ярлыка, созданного на панели задач при нажатии пользователем кнопки закрепить приложение на панели задач или запуска нового экземпляра с помощью его списка переходов.
ms.assetid: 3559d1f5-988c-41d9-ba9a-dfa4ba643ee2
title: System. Аппусермодел. Релаунчиконресаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b43394bd5ee7dca6084526224dac268500f6881317215d63d6fc0e9a126c5b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118970843"
---
# <a name="systemappusermodelrelaunchiconresource"></a>System. Аппусермодел. Релаунчиконресаурце

Задает значок, используемый для ярлыка, созданного на панели задач при нажатии пользователем кнопки закрепить приложение на панели задач или запуска нового экземпляра с помощью его списка переходов. Это значок, используемый для группы панелей задач и отображаемый для закрепленного приложения независимо от того, работает ли это приложение. Он должен быть указан в одном из следующих форматов:

-   Стандартный формат ресурсов, например "% системдир% \\ system32 \\shell32.dll,-128". Символ "-" перед ИДЕНТИФИКАТОРом ресурса обязателен. Не используйте символ "@" в начале строки пути.
-   прямой путь к файлу значка, например "% programfiles% \\ Microsoft \\ Блокнот \\ Блокнот. ico, 0". Обратите внимание, что, поскольку ICO-файлы могут содержать несколько ресурсов значков, в строке необходимо указать идентификатор ресурса. Если ICO-файл является одним изображением, используйте "0" (без символа "-") в качестве идентификатора ресурса.

[System. аппусермодел. релаунчиконресаурце]() является необязательным свойством. Если он не задан, используется значок целевого объекта для команды повторного запуска ([System. аппусермодел. релаунчкомманд](./props-system-appusermodel-relaunchcommand.md)). Однако, поскольку это может привести к нежелательным результатам, настоятельно рекомендуется явно указать значок с помощью этого свойства.

Это свойство используется только в том случае, если окно имеет явный идентификатор модели пользователя приложения (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), установленный через [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Если окно не имеет явного AppUserModelID (System.AppUserModel.ID), это свойство игнорируется, а окно группируются и закрепляется как часть его процесса-владельца. Дополнительные сведения о приложении явной Аппусермоделидс и их последствиях для закрепления панели задач см. в разделе [идентификаторы моделей пользователей приложений (аппусермоделидс)](../shell/appids.md). Это свойство предназначено для использования приложениями или окнами, которые хотят предоставлять сведения о перезапуске не по умолчанию. Дополнительные сведения см. в разделе [System. аппусермодел. релаунчкомманд](./props-system-appusermodel-relaunchcommand.md).

Если в окне задан явный AppUserModelID, но это свойство не задано, система пытается найти ярлык с тем же AppUserModelID и закрепляет этот ярлык на панели задач для представления окна. Если такое сочетание клавиш не удается найти, используется резервный исполняемый файл процесса, которому он принадлежит.

> [!Note]  
> Это свойство игнорируется, если задано значение [System. аппусермодел. превентпиннинг](./props-system-appusermodel-preventpinning.md) . Это позволяет приложению управлять группированием окон путем назначения им явных Аппусермоделидс, но предотвращая закрепление этих окон.

 

Чтобы задать это свойство в окне, используйте [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) для получения хранилища свойств окна и используйте методы, извлекают объект [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы установить свойство [System. аппусермодел. релаунчиконресаурце]() этого окна.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = true
   typeInfo
      type = String
      IsInnate = false
```

## <a name="windows-8-windows-7"></a>Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchIconResource
   shellPKey = PKEY_AppUserModel_RelaunchIconResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 3
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Идентификаторы модели пользователя приложения (Аппусермоделидс)](../shell/appids.md)
</dt> <dt>

[System.AppUserModel.ID](./props-system-appusermodel-id.md)
</dt> <dt>

[пропертидескриптионлист](./propdesc-schema-propertydescriptionlist.md)
</dt> <dt>

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

[aliasInfo](./propdesc-schema-aliasinfo.md)
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

[enum](./propdesc-schema-enum.md)
</dt> <dt>

[енумранже](./propdesc-schema-enumrange.md)
</dt> <dt>

[image](./propdesc-schema-image.md)
</dt> <dt>

[дравконтрол](./propdesc-schema-drawcontrol.md)
</dt> <dt>

[едитконтрол](./propdesc-schema-editcontrol.md)
</dt> <dt>

[филтерконтрол](./propdesc-schema-filtercontrol.md)
</dt> <dt>

[куериконтрол](./propdesc-schema-querycontrol.md)
</dt> <dt>

[релатедпропертинфо](./propdesc-schema-relatedpropertyinfo.md)
</dt> <dt>

[relatedProperty](./propdesc-schema-relatedproperty.md)
</dt> </dl>

 

 
