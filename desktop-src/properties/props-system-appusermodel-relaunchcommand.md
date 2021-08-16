---
description: Указывает команду, которая может быть выполнена с помощью ShellExecute для запуска приложения при его закреплении на панели задач или при запуске нового экземпляра приложения с помощью списка переходов приложения.
ms.assetid: 83aab060-0629-48e3-a2db-9ba96a8631e5
title: System. Аппусермодел. Релаунчкомманд
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cc2ce3783aa9ab3d76124b8d62f9d9d9ad2e1f5d4b92622716df111456dbabd
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119554524"
---
# <a name="systemappusermodelrelaunchcommand"></a>System. Аппусермодел. Релаунчкомманд

Указывает команду, которая может быть выполнена с помощью [**ShellExecute**](/windows/win32/api/shellapi/nf-shellapi-shellexecutea) для запуска приложения при его закреплении на панели задач или при запуске нового экземпляра приложения с помощью списка переходов приложения.

Вот несколько примеров.


```
shell:::{ED228FDF-9EA8-4870-83B1-96B02CFE0D52}

virtualhost.exe /virtualapp:12345

notepad.exe
```



Это свойство используется только в том случае, если окно имеет явный идентификатор модели пользователя приложения (AppUserModelID) ([System.AppUserModel.ID](./props-system-appusermodel-id.md), установленный через [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow)). Если окно не имеет явного AppUserModelID, это свойство игнорируется, а окно группируются и закрепляется как часть процесса, который его владеет. Дополнительные сведения о приложении явной Аппусермоделидс и их последствиях для закрепления панели задач см. в разделе [идентификаторы моделей пользователей приложений (аппусермоделидс)](../shell/appids.md).

Это свойство предназначено для использования приложениями или окнами, которые хотят предоставлять сведения о перезапуске не по умолчанию.

> [!Note]  
> [System. аппусермодел. релаунчкомманд]() и [System. аппусермодел. релаунчдисплайнамересаурце](./props-system-appusermodel-relaunchdisplaynameresource.md) всегда должны быть заданы вместе. Если одно из этих свойств не задано, ни один из них не используется.

 

Это свойство вместе с [System. аппусермодел. релаунчдисплайнамересаурце](./props-system-appusermodel-relaunchdisplaynameresource.md) и [System. аппусермодел. релаунчиконресаурце](./props-system-appusermodel-relaunchiconresource.md) можно использовать для визуального определения окна в качестве приложения для пользователя. Это полезно для сценариев ведущих приложений, где один экземпляр узла запускает несколько дочерних приложений. Например, виртуальная машина, на которой размещается несколько виртуализированных приложений, может потребовать, чтобы эти виртуализированные приложения отображались как отдельные приложения для пользователя. Виртуальная машина может пометить каждое окно явным образом AppUserModelID и соответствующие свойства перезапуска, чтобы они отображались как приложения. Пользователь может затем закрепить их на панели задач и «перезапустить» закрепленный экземпляр.

> [!Note]  
> Это свойство игнорируется, если задано значение [System. аппусермодел. превентпиннинг](./props-system-appusermodel-preventpinning.md) . Это позволяет приложению управлять группированием окон путем назначения им явных Аппусермоделидс, но предотвращая закрепление этих окон.

 

Чтобы задать это свойство в окне, используйте [**шжетпропертисторефорвиндов**](/windows/desktop/api/Shellapi/nf-shellapi-shgetpropertystoreforwindow) для получения хранилища свойств окна и используйте методы, извлекают объект [**ипропертисторе**](/windows/win32/api/propsys/nn-propsys-ipropertystore) , чтобы установить свойство [System. аппусермодел. релаунчкомманд]() этого окна.

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8-windows-7"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8, Windows 7

```
propertyDescription
   name = System.AppUserModel.RelaunchCommand
   shellPKey = PKEY_AppUserModel_RelaunchCommand
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 2
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

 

 
