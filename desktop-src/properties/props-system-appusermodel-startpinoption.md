---
description: Присвоить этому свойству ярлыка значение (1) запретить автоматическую Прикрепление приложения к начальному экрану при установке; или (2) указывает, что элемент программным образом добавляется к средству запуска через действие пользователя (что означает, что автоматически закрепляться при запуске и удалении при откреплениях).
ms.assetid: 247ad0a6-ce65-45f1-a0d5-51ad135000aa
title: System. Аппусермодел. Стартпиноптион
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43cdef82a90488ce87bbf182323b00d62a5cdfea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103898670"
---
# <a name="systemappusermodelstartpinoption"></a>System. Аппусермодел. Стартпиноптион

Присвоить этому свойству ярлыка значение (1) запретить автоматическую Прикрепление приложения к начальному экрану при установке; или (2) указывает, что элемент программным образом добавляется к средству запуска через действие пользователя (что означает, что автоматически закрепляться при запуске и удалении при откреплениях).

## <a name="windows-10-version-1703-windows-10-version-1607-windows-10-version-1511-windows-10-version-1507-windows-81-windows-8"></a>Windows 10, версия 1703, Windows 10, версия 1607, Windows 10, версия 1511, Windows 10, версия 1507, Windows 8.1, Windows 8

```
propertyDescription
   name = System.AppUserModel.StartPinOption
   shellPKey = PKEY_AppUserModel_StartPinOption
   formatID = 9F4C2855-9F79-4B39-A8D0-E1D42DE1D5F3
   propID = 12
   SearchInfo
      InInvertedIndex = false
      IsColumn = false
   typeInfo
      type = UInt32
      IsInnate = false
      EnumeratedList
         UseValueForDefault = True
         enum
            name = Default
            value = 0
            text = Default
            defineToken = APPUSERMODEL_STARTPINOPTION_DEFAULT
         enum
            name = NoPinOnInstall
            value = 1
            text = NoPinOnInstall
            defineToken = APPUSERMODEL_STARTPINOPTION_NOPINONINSTALL
         enum
            name = UserPinned
            value = 2
            text = UserPinned
            defineToken = APPUSERMODEL_STARTPINOPTION_USERPINNED
```

## <a name="remarks"></a>Комментарии

Значения PKEY определены в списке PKEY. h.

## <a name="related-topics"></a>См. также

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

 

 
