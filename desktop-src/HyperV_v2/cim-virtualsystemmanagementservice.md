---
description: Представляет службу, которая управляет виртуальными системами.
ms.assetid: b2645546-3c04-4d3f-8d53-019a6db08e24
title: Класс CIM_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 903b751b405c103313c0f83c38687e08ee7bb36a33ae803bd175b6ad91c559cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119068624"
---
# <a name="cim_virtualsystemmanagementservice-class"></a>\_Класс CIM виртуалсистемманажементсервице

Представляет службу, которая управляет виртуальными системами.

## <a name="syntax"></a>Синтаксис

``` syntax
[Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Virtualization"), AMENDMENT]
class CIM_VirtualSystemManagementService : CIM_Service
{
};
```

## <a name="members"></a>Члены

Класс **CIM \_ виртуалсистемманажементсервице** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **CIM \_ виртуалсистемманажементсервице** содержит следующие методы.



| Метод                                                                                      | Описание                                                                           |
|:--------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------|
| [**аддресаурцесеттингс**](cim-virtualsystemmanagementservice-addresourcesettings.md)       | Добавляет ресурсы в конфигурацию виртуальной системы.<br/>                          |
| [**дефинесистем**](cim-virtualsystemmanagementservice-definesystem.md)                     | Определяет виртуальную систему.<br/>                                                  |
| [**дестройсистем**](cim-virtualsystemmanagementservice-destroysystem.md)                   | Удаляет виртуальную систему.<br/>                                                  |
| [**модифиресаурцесеттингс**](cim-virtualsystemmanagementservice-modifyresourcesettings.md) | Изменяет параметры виртуального ресурса для конфигурации виртуальной системы.<br/> |
| [**модифисистемсеттингс**](cim-virtualsystemmanagementservice-modifysystemsettings.md)     | Изменяет параметры виртуальной системы.<br/>                                          |
| [**ремовересаурцесеттингс**](cim-virtualsystemmanagementservice-removeresourcesettings.md) | Удаляет параметры виртуального ресурса из конфигурации виртуальной системы.<br/>     |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

 




