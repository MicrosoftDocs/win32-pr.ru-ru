---
description: Предоставляет дополнительные сведения для использования с методом Креатереференцепоинт \_ класса Коллектионреференцепоинтсервице мсвм.
ms.assetid: abf7953a-e10e-4dab-962f-a7dde5126fbe
title: Класс Msvm_CollectionReferencePointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CollectionReferencePointSettingData
- Msvm_CollectionReferencePointSettingData.ConsistencyLevel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 1164c61f9335ce900dfbcf0b317dd0c4c9a8f84c0a97aaf13b2ea851a80dbd17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130674"
---
# <a name="msvm_collectionreferencepointsettingdata-class"></a>\_Класс мсвм коллектионреференцепоинтсеттингдата

Предоставляет дополнительные сведения для использования с методом [**креатереференцепоинт**](msvm-collectionreferencepointservice-createreferencepoint.md) класса [**\_ коллектионреференцепоинтсервице мсвм**](msvm-collectionreferencepointservice.md) .

Следующий пример синтаксиса — упрощенный MOF-код, который включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[AMENDMENT]
class Msvm_CollectionReferencePointSettingData : CIM_SettingData
{
  uint8 ConsistencyLevel;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ коллектионреференцепоинтсеттингдата** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ коллектионреференцепоинтсеттингдата** имеет следующие свойства.

<dl> <dt>

**ConsistencyLevel**
</dt> <dd> <dl> <dt>

Тип данных: **Uint8**
</dt> <dt>

Тип доступа: чтение и запись
</dt> </dl>

Уровень согласованности контрольной точки.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>

<span id="Application_Consistent"></span><span id="application_consistent"></span><span id="APPLICATION_CONSISTENT"></span>С **совместимостью приложений** (1)


</dt> <dd>

Эталонная точка указывает на момент времени, когда виртуальная система находилась в состоянии сбоя.

</dd> <dt>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>

<span id="Crash_Consistent"></span><span id="crash_consistent"></span><span id="CRASH_CONSISTENT"></span>**Отказоустойчивость (2** )


</dt> <dd>

Эталонная точка указывает на момент времени, когда виртуальная система находилась в состоянии совместимости с приложениями.

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Требования



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

 

 




