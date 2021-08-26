---
description: Определяет подключение, которое в настоящее время включено и настроено для обеспечения взаимодействия между двумя \_ объектами CIM сервицеакцесспоинт.
ms.assetid: 03f8e43f-a77b-46e2-bb7d-c29758c65aee
title: Класс CIM_ActiveConnection
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActiveConnection
- CIM_ActiveConnection.Antecedent
- CIM_ActiveConnection.Dependent
- CIM_ActiveConnection.TrafficType
- CIM_ActiveConnection.OtherTrafficDescription
- CIM_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a2961779744e90d0e4281e53c3d78c92081993027deb6c435846abbffb41b110
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120041764"
---
# <a name="cim_activeconnection-class"></a>\_Класс CIM ActiveConnection

Определяет подключение, которое в настоящее время включено и настроено для обеспечения взаимодействия между двумя объектами **CIM \_ сервицеакцесспоинт** . **Модель CIM \_ ActiveConnection** используется, если соединение не рассматривается как объект **CIM \_ манажеделемент** . Точки доступа к службам, подключенные активным подключением, обычно находятся на одном уровне сети или приложения.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::Service"), AMENDMENT]
class CIM_ActiveConnection : CIM_SAPSAPDependency
{
  CIM_ServiceAccessPoint REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     TrafficType;
  string                     OtherTrafficDescription;
  boolean                    IsUnidirectional;
};
```

## <a name="members"></a>Члены

Класс **CIM \_ ActiveConnection** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **CIM \_ ActiveConnection** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ сервицеакцесспоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")
</dt> </dl>

Точка доступа к службе, которая подключена к другой точке доступа к службе через активное соединение. **Модель CIM \_ Объект Сервицеакцесспоинт** . В однонаправленном соединении это точка доступа, которая передает данные.

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **CIM \_ сервицеакцесспоинт**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("зависимый")
</dt> </dl>

Точка доступа к службе, настроенная для обмена данными или активно взаимодействующая с точкой доступа к службе, указанной в свойстве **Antecedent** . В однонаправленном соединении это точка доступа, которая получает данные.

</dd> <dt>

**По поднаправлению**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Значение true, если соединение является однонаправленным; значение false, если соединение является двунаправленным. Если соединение является однонаправленным, свойство **Antecedent** указывает точку доступа, которая передает данные. В двунаправленном соединении **Antecedent** может указывать любую точку доступа, назначенную соединению.

</dd> <dt>

**осертраффикдескриптион**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения"), [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**Траффиктипе**")
</dt> </dl>

> [!Note]  
> Это свойство использовать не рекомендуется. Вместо этого рекомендуется указывать эти сведения в параметрах адресации, протокола и базовой функциональности конечных точек.

 

Описание типа трафика, указанного, если свойство **траффиктипе** имеет значение 1 (другое).

</dd> <dt>

**ТипТрафика**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: не [**рекомендуется**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("нет значения"), [**Моделкорреспонденце**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ActiveConnection**.**Осертраффикдескриптион**")
</dt> </dl>

> [!Note]  
> Это свойство использовать не рекомендуется. Вместо этого рекомендуется указывать эти сведения в параметрах адресации, протокола и базовой функциональности конечных точек.

 

Тип трафика, передаваемого через это соединение.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Неизвестно** (0)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Другое** (1)


</dt> <dd></dd> <dt>

<span id="Unicast"></span><span id="unicast"></span><span id="UNICAST"></span>

**Одноадресная рассылка** (2)


</dt> <dd></dd> <dt>

<span id="Broadcast"></span><span id="broadcast"></span><span id="BROADCAST"></span>

**Вещание** (3)


</dt> <dd></dd> <dt>

<span id="Multicast"></span><span id="multicast"></span><span id="MULTICAST"></span>

**Многоадресная рассылка** (4)


</dt> <dd></dd> <dt>

<span id="Anycast"></span><span id="anycast"></span><span id="ANYCAST"></span>

**Рассылки** (5)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8<br/>                                                                                    |
| Минимальная версия сервера<br/> | Windows Server 2012<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_САПСАПДЕПЕНДЕНЦИ CIM**](cim-sapsapdependency.md)
</dt> </dl>

 

