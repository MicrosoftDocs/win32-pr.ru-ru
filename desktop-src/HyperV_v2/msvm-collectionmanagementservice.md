---
description: Управляет коллекциями на узле Hyper-V.
ms.assetid: e895217e-352d-4d77-8f1d-7070012e6f60
title: Класс Msvm_CollectionManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionManagementService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 89d63d9a210f8c1074296620f430117d6203e295
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103819017"
---
# <a name="msvm_collectionmanagementservice-class"></a>\_Класс мсвм коллектионманажементсервице

Управляет коллекциями на узле Hyper-V.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionManagementService : CIM_Service
{
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ коллектионманажементсервице** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **мсвм \_ коллектионманажементсервице** содержит следующие методы.



| Метод                                                                          | Описание                                                                                                                                                                                                                   |
|:--------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**аддмембер**](msvm-collectionmanagementservice-addmember.md)                 | Добавляет указанный Манажеделемент в качестве члена данного объекта [**\_ коллектионофмсес CIM**](cim-collectionofmses.md) .<br/>                                                                                           |
| [**дефинеколлектион**](msvm-collectionmanagementservice-definecollection.md)   | Создает новый объект [**CIM \_ коллектионофмсес**](cim-collectionofmses.md) .<br/>                                                                                                                                        |
| [**дестройколлектион**](msvm-collectionmanagementservice-destroycollection.md) | Удаляет данный объект [**CIM \_ коллектионофмсес**](cim-collectionofmses.md) .<br/>                                                                                                                                    |
| [**ремовемембер**](msvm-collectionmanagementservice-removemember.md)           | Удаляет указанный Манажеделемент в качестве члена данного объекта [**\_ коллектионофмсес CIM**](cim-collectionofmses.md) .<br/>                                                                                        |
| [**ремовемембербид**](msvm-collectionmanagementservice-removememberbyid.md)   | Удаляет указанный Манажеделемент в качестве члена [**\_ коллектионофмсес CIM**](cim-collectionofmses.md) с заданным идентификатором. Это будет выполняться, даже если объект с таким идентификатором отсутствует.<br/> |
| [**ренамеколлектион**](msvm-collectionmanagementservice-renamecollection.md)   | Обновляет ElementName заданного объекта [**CIM \_ коллектионофмсес**](cim-collectionofmses.md) .<br/>                                                                                                                    |
| [**StartService**](msvm-collectionmanagementservice-startservice.md)           | запускает службу.<br/>                                                                                                                                                                                                |
| [**StopService**](msvm-collectionmanagementservice-stopservice.md)             | останавливает службу.<br/>                                                                                                                                                                                                 |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

 




