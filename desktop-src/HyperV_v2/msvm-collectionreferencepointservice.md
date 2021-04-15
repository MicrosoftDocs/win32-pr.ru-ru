---
description: Служба для создания, уничтожения и экспорта опорных точек.
ms.assetid: 88a76319-b5a7-44a3-8a31-83ade999b255
title: Класс Msvm_CollectionReferencePointService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointService
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: f6ba56fcb75a177521b8f3ea3ae0675cfdd8a8dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105682935"
---
# <a name="msvm_collectionreferencepointservice-class"></a>\_Класс мсвм коллектионреференцепоинтсервице

Служба для создания, уничтожения и экспорта опорных точек

коллекций виртуальных систем.

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_CollectionReferencePointService : CIM_Service
{
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ коллектионреференцепоинтсервице** имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Класс **мсвм \_ коллектионреференцепоинтсервице** содержит следующие методы.



| Метод                                                                                      | Описание                                                                                                                                                                                                     |
|:--------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**креатереференцепоинт**](msvm-collectionreferencepointservice-createreferencepoint.md)   | Создает точку ссылки для коллекции виртуальных систем.<br/>                                                                                                                                            |
| [**дестройреференцепоинт**](msvm-collectionreferencepointservice-destroyreferencepoint.md) | Уничтожает существующую коллекцию опорных точек. Этот метод может в качестве побочного действия уничтожить другие опорные точки, зависящие от затронутой коллекции опорных точек.<br/>                      |
| [**експортреференцепоинт**](msvm-collectionreferencepointservice-exportreferencepoint.md)   | Экспортирует коллекцию опорных точек в файл. Коллекция опорных точек, связанные с ней параметры конфигурации и связанные с ней параметры ресурсов будут сохранены в результирующем файле.<br/> |
| [**ремовеассоЦиатеддата**](msvm-collectionreferencepointservice-removeassociateddata.md)   | Удаляет журнал данных, связанный с точкой ссылки.<br/>                                                                                                                                            |



 

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

 

 




