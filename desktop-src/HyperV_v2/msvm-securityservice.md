---
description: Представляет службу безопасности. Он используется для настройки параметров безопасности виртуальной системы.
ms.assetid: 00097d81-9fea-4b84-b5dd-e45af46d6e0a
title: Класс Msvm_SecurityService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SecurityService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cc7b15af3d3033487464fe7b29a93dc649ffbd62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103998637"
---
# <a name="msvm_securityservice-class"></a>\_Класс мсвм SecurityService

Представляет службу безопасности. Он используется для настройки параметров безопасности виртуальной системы.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SecurityService : CIM_Service
{
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ SecurityService** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **мсвм \_ SecurityService** содержит следующие методы.



| Метод                                                                                            | Описание                                                             |
|:--------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------|
| [**жеткэйпротектор**](msvm-securityservice-getkeyprotector.md)                                   | Метод для получения предохранителя ключа для виртуальной системы.<br/>   |
| [**модифисекуритисеттингс**](msvm-securityservice-modifysecuritysettings.md)                     | Изменяет текущие параметры безопасности виртуальной машины.<br/> |
| [**рестореласткновнгудкэйпротектор**](msvm-securityservice-restorelastknowngoodkeyprotector.md) | Метод восстановления до последнего известного предохранителя ключа.<br/> |
| [**сеткэйпротектор**](msvm-securityservice-setkeyprotector.md)                                   | Метод для задания предохранителя ключа виртуальной системы.<br/>        |
| [**сетсекуритиполици**](msvm-securityservice-setsecuritypolicy.md)                               | Метод для задания предохранителя ключа виртуальной системы.<br/>        |
| [**StartService**](msvm-securityservice-startservice.md)                                         | запускает службу.<br/>                                          |
| [**StopService**](msvm-securityservice-stopservice.md)                                           | останавливает службу.<br/>                                           |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только для настольных приложений Windows 10 версии 1703\]<br/>                                               |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

 




