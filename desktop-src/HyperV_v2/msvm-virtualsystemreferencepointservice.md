---
description: Описывает службу опорной точки виртуальной системы.
ms.assetid: 888ecd21-4b59-46a9-b2e1-538e30dd2d1c
title: Класс Msvm_VirtualSystemReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f33ac35e9848b913978ef6fab91f60823e5c40e9a2bb652236b2ab902e4ea435
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119340164"
---
# <a name="msvm_virtualsystemreferencepointservice-class"></a>\_Класс мсвм виртуалсистемреференцепоинтсервице

Описывает службу опорной точки виртуальной системы.

Следующий синтаксис упрощен из MOF-кода и включает все унаследованные свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualSystemReferencePointService : CIM_Service
{
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемреференцепоинтсервице** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **мсвм \_ виртуалсистемреференцепоинтсервице** содержит следующие методы.



| Метод                                                                                                       | Описание                                                          |
|:-------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------|
| [**креатереференцепоинт**](msvm-virtualsystemreferencepointservice-createreferencepoint.md)                 | Создает опорную точку виртуальной системы.<br/>            |
| [**дестройреференцепоинт**](msvm-virtualsystemreferencepointservice-destroyreferencepoint.md)               | Удаляет указанную точку ссылки.<br/>                    |
| [**експортреференцепоинт**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md)                 | Экспортирует опорную точку виртуальной системы.<br/>        |
| [**импортреференцепоинтметадата**](msvm-virtualsystemreferencepointservice-importreferencepointmetadata.md) | Импортирует метаданные опорной точки виртуальной системы.<br/>   |
| [**ремовеассоЦиатеддата**](msvm-virtualsystemreferencepointservice-removeassociateddata.md)                 | Удаляет журнал данных, связанный с точкой ссылки.<br/> |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

 




