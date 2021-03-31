---
description: Предоставляет дополнительные сведения для использования с методом Експортреференцепоинт \_ класса Виртуалсистемреференцепоинтсервице мсвм.
ms.assetid: 4897fad4-3a3f-47bc-837d-2e36434b3fab
title: Класс Msvm_VirtualSystemReferencePointExportSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportSettingData
- Msvm_VirtualSystemReferencePointExportSettingData.BaseReferencePoint
- Msvm_VirtualSystemReferencePointExportSettingData.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 65fc16f409fd79782ec4a91f223dfc754563f8bb
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "104081708"
---
# <a name="msvm_virtualsystemreferencepointexportsettingdata-class"></a>\_Класс мсвм виртуалсистемреференцепоинтекспортсеттингдата

Предоставляет дополнительные сведения для использования с методом [**експортреференцепоинт**](msvm-virtualsystemreferencepointservice-exportreferencepoint.md) класса [**\_ виртуалсистемреференцепоинтсервице мсвм**](msvm-virtualsystemreferencepointservice.md) .

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointExportSettingData : CIM_SettingData
{
  String BaseReferencePoint;
  String DisksToExport[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемреференцепоинтекспортсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Свойства

Класс **мсвм \_ виртуалсистемреференцепоинтекспортсеттингдата** имеет следующие свойства.

<dl> <dt>

**басереференцепоинт**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Путь к базовой опорной точке относительно того, в какой операции следует выполнить экспорт.

</dd> <dt>

**дискстоекспорт**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Идентификаторы экземпляров WMI для дисков, для которых необходимо экспортировать данные.

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

 

 




