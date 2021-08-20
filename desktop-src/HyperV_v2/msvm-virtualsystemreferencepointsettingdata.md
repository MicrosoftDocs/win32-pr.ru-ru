---
description: Предоставляет дополнительные сведения для использования с методом Креатереференцепоинт \_ класса Виртуалсистемреференцепоинтсервице мсвм.
ms.assetid: 6b997ba5-871c-4c33-9ed5-b9a13cbfaacd
title: Класс Msvm_VirtualSystemReferencePointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointSettingData
- Msvm_VirtualSystemReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 703b0b1cedc93e670ff8ac97c7dddf9041145a4eccc064e07562947aec898c0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146376"
---
# <a name="msvm_virtualsystemreferencepointsettingdata-class"></a>\_Класс мсвм виртуалсистемреференцепоинтсеттингдата

Предоставляет дополнительные сведения для использования с методом [**креатереференцепоинт**](msvm-virtualsystemreferencepointservice-createreferencepoint.md) класса [**\_ виртуалсистемреференцепоинтсервице мсвм**](msvm-virtualsystemreferencepointservice.md) .

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Msvm_VirtualSystemReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ виртуалсистемреференцепоинтсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ виртуалсистемреференцепоинтсеттингдата** имеет следующие свойства.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Уровень согласованности контрольной точки.

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10 \[ только классические приложения\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_SETTINGDATA CIM**](cim-settingdata.md)
</dt> </dl>

 

 




