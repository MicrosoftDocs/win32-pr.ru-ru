---
description: Указывает отображаемое имя, используемое для ярлыка, созданного на панели задач при выборе пользователем закрепления приложения на панели задач или при запуске нового экземпляра с помощью списка переходов кнопки.
ms.assetid: a149838b-83b6-44ce-b705-e2804efb3d31
title: System. Аппусермодел. Релаунчдисплайнамересаурце
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22b0af752fb345dd5dd5f1b091a22255e856031affaca266ff6307045f148cd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118233026"
---
# <a name="systemappusermodelrelaunchdisplaynameresource"></a>System. Аппусермодел. Релаунчдисплайнамересаурце

Указывает отображаемое имя, используемое для ярлыка, созданного на панели задач при выборе пользователем закрепления приложения на панели задач или при запуске нового экземпляра с помощью списка переходов кнопки. Значение этого свойства должно быть одним из следующих:

-   Непрямая строка ресурса, например "@% системдир% \\ system32 \\shell32.dll,-19263". Обратите внимание, что символ "@" требуется для различения косвенной строки от обычной текстовой строки (описывается в следующем маркированном абзаце). Эта непрямая строка состоит из двоичного файла и идентификатора ресурса строки, содержащейся в этом двоичном файле. настоятельно рекомендуется использовать эту форму непрямых строк, которая гарантирует, что отображаемое имя изменится соответствующим образом при изменении языка системы с помощью многоязычный пользовательский интерфейс (MUI). Символ "-" перед ИДЕНТИФИКАТОРом ресурса обязателен.
-   Обычная текстовая строка, которая не указывает на ресурс. Этот параметр следует использовать только в том случае, если отображаемое имя динамически вычисляется или получается из источника данных, не поддерживающего MUI. например, строка может быть именем устройства, например Microsoft Zune, в случаях, когда приложение отображается при подключении устройства к компьютеру.

> [!Note]  
> [System. аппусермодел. релаунчкомманд](./props-system-appusermodel-relaunchcommand.md) и [System. аппусермодел. релаунчдисплайнамересаурце]() всегда должны быть заданы вместе. Если одно из этих свойств не задано, ни один из них не используется.

 

Это свойство используется только в том случае, если окно имеет явный идентификатор модели пользователя приложения (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), установленный через [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Если окно не имеет явного AppUserModelID, это свойство игнорируется, а окно группируются и закрепляется как часть процесса, который его владеет. Дополнительные сведения о приложении явной Аппусермоделидс и их последствиях для закрепления панели задач см. в разделе [идентификаторы моделей пользователей приложений (аппусермоделидс)](../shell/appids.md). Это свойство предназначено для использования приложениями или окнами, которые хотят предоставлять сведения о перезапуске не по умолчанию. Дополнительные сведения см. в разделе [System. аппусермодел. релаунчкомманд](./props-system-appusermodel-relaunchcommand.md).

> [!Note]  
> Это свойство игнорируется, если задано значение [System. аппусермодел. превентпиннинг](./props-system-appusermodel-preventpinning.md) . Это позволяет приложению управлять группированием окон путем назначения им явных Аппусермоделидс, но предотвращая закрепление этих окон.

 

Чтобы задать это свойство в окне, используйте [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) для получения хранилища свойств окна и используйте методы, извлекают объект [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы установить свойство [System. аппусермодел. релаунчдисплайнамересаурце]() этого окна.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchDisplayNameResource
   shellPKey = PKEY_AppUserModel_RelaunchDisplayNameResource
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 4
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = String
      IsInnate = false
```

## <a name="remarks"></a>Remarks

Значения PKEY определены в списке PKEY. h.

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

 

 
