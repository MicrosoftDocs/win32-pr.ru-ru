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
ms.openlocfilehash: 0614349ed6f6358316826bbfc2cd10ac55cba953
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664803"
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
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_Служба CIM**](cim-service.md)
</dt> </dl>

 

 




