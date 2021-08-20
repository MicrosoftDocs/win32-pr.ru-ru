---
description: Представляет службу, управляющую переносом виртуальных систем между системами узлов. Этот класс также проверяет, вероятна ли успешная миграция.
ms.assetid: 28948a36-3b92-4d52-9a48-aaa155e7fad5
title: Класс CIM_VirtualSystemMigrationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44b034c5b91eb024bdbcde0b0d835ba12f0367bedc6dbd9c5c2d52dca1029f87
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068544"
---
# <a name="cim_virtualsystemmigrationservice-class"></a>\_Класс CIM виртуалсистеммигратионсервице

Представляет службу, управляющую переносом виртуальных систем между системами узлов. Этот класс также проверяет, вероятна ли успешная миграция.

## <a name="syntax"></a>Синтаксис

``` syntax
[Experimental, Abstract, Version("2.17.0"), UMLPackagePath("CIM::System::Virtualization"), AMENDMENT]
class CIM_VirtualSystemMigrationService : CIM_Service
{
};
```

## <a name="members"></a>Члены

Класс **CIM \_ виртуалсистеммигратионсервице** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **CIM \_ виртуалсистеммигратионсервице** содержит следующие методы.



| Метод                                                                                                                     | Описание                                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**чекквиртуалсистемисмигратаблетохост**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletohost.md)     | Проверяет, вероятна ли успешная миграция виртуальной системы на узел.<br/>   |
| [**чекквиртуалсистемисмигратаблетосистем**](cim-virtualsystemmigrationservice-checkvirtualsystemismigratabletosystem.md) | Проверяет, вероятна ли успешная миграция виртуальной системы в систему.<br/> |
| [**мигратевиртуалсистемтохост**](cim-virtualsystemmigrationservice-migratevirtualsystemtohost.md)                         | Переносит виртуальную систему на целевой узел.<br/>                                           |
| [**мигратевиртуалсистемтосистем**](cim-virtualsystemmigrationservice-migratevirtualsystemtosystem.md)                     | Переносит виртуальную систему в целевую систему.<br/>                                           |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

 




