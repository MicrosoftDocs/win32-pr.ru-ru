---
description: Явный идентификатор модели пользователя приложения (AppUserModelID), используемый для связывания процессов, файлов и окон с определенным приложением.
ms.assetid: 07858b3c-e601-40ec-a87a-d66612d5473a
title: System.AppUserModel.ID
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6dd60b64598a620221ec2b610b10cbc05002f38aaf633e51e788b24797620cab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033742"
---
# <a name="systemappusermodelid"></a>System.AppUserModel.ID

Явный идентификатор модели пользователя приложения (AppUserModelID), используемый для связывания процессов, файлов и окон с определенным приложением. В некоторых случаях достаточно полагаться на внутренний AppUserModelID, назначенный процессу системы. Однако приложение, владеющее несколькими процессами или приложением, которое выполняется в хост-процессе, может потребовать явно идентифицировать себя через это свойство, чтобы оно могло сгруппировать разрозненные окна под одной кнопкой на панели задач и управлять содержимым списка переходов этого приложения.

Чтобы задать это свойство в окне, используйте [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) для получения хранилища свойств окна и используйте методы, извлекают объект [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы установить свойство [System.AppUserModel.ID]() этого окна.

Дополнительные сведения см. в разделе [идентификаторы моделей пользователей приложения (аппусермоделидс)](../shell/appids.md).

Когда свойство [System.AppUserModel.ID]() установлено, панель задач уведомляется о необходимости обновления сведений в окне или ярлыке, заданному этим AppUserModelID.

Другие свойства окна и ярлыка можно использовать в сочетании с явным AppUserModelID для дальнейшего управления группированием и закреплением, связанным с окном, отображаемым именем и значком, используемым для него на панели задач, и командой для запуска приложения, закрепленного на панели задач, или нового экземпляра приложения с помощью списка переходов этого приложения. Эти свойства должны быть установлены перед установкой свойства [System.AppUserModel.ID]() . Дополнительные сведения см. в следующих разделах:

-   [System. Аппусермодел. Превентпиннинг](./props-system-appusermodel-preventpinning.md)
-   [System. Аппусермодел. Релаунчкомманд](./props-system-appusermodel-relaunchcommand.md)
-   [System. Аппусермодел. Релаунчдисплайнамересаурце](./props-system-appusermodel-relaunchdisplaynameresource.md)
-   [System. Аппусермодел. Релаунчиконресаурце](./props-system-appusermodel-relaunchiconresource.md)

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.ID
   shellPKey = PKEY_AppUserModel_ID
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 5
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

[**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)
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

 

 
