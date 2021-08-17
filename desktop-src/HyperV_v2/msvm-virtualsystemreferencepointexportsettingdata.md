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
ms.openlocfilehash: 2b3fc743d8431d76582553979bb25e1269df970d70187c65c2bddd1014834c76
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147947"
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

### <a name="properties"></a>Элемент Property

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
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




