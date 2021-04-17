---
description: Экспорт данных параметров, передаваемых в метод Експортреференцепоинт \_ класса мсвм коллектионреференцепоинтсервице.
ms.assetid: 38299050-a53a-496c-8792-9199c394591d
title: Класс Msvm_CollectionReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointExportSettingData
- Msvm_CollectionReferencePointExportSettingData.BaseReferencePointCollection
- Msvm_CollectionReferencePointExportSettingData.VirtualMachinesToDisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 4e5b3513fd30035283a6b4dc305f2768b85cb7e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684270"
---
# <a name="msvm_collectionreferencepointexportsettingdata-class"></a>\_Класс мсвм коллектионреференцепоинтекспортсеттингдата

Экспорт данных параметров, передаваемых в метод [**експортреференцепоинт**](msvm-collectionreferencepointservice-exportreferencepoint.md) класса [**мсвм \_ коллектионреференцепоинтсервице**](msvm-collectionreferencepointservice.md) .

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointExportSettingData : CIM_SettingData
{
  string BaseReferencePointCollection;
  string VirtualMachinesToDisksToExport[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ коллектионреференцепоинтекспортсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ коллектионреференцепоинтекспортсеттингдата** имеет следующие свойства.

<dl> <dt>

**басереференцепоинтколлектион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Путь к экземпляру [**\_ референцепоинтколлектион мсвм**](msvm-referencepointcollection.md) , который представляет базовую коллекцию опорных точек, используемую для разностного экспорта.

</dd> <dt>

**виртуалмачинестодискстоекспорт**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: чтение и запись
</dt> <dt>

Квалификаторы: **хипервембеддединстанце** ("мсвм \_ виртуалмачинетодискс")
</dt> </dl>

Список сведений о сопоставлении "VirtualMachines со Дискстоекспорт", для которых необходимо экспортировать данные.

</dd> </dl>

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

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




