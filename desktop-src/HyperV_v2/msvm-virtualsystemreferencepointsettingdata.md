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
ms.openlocfilehash: ea36f9504d9c2d6b7e875f32bb7cd0a0efd167da
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/03/2021
ms.locfileid: "105664795"
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

### <a name="properties"></a>Свойства

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

 

 




