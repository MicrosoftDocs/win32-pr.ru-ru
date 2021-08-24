---
description: Описывает возможности связанного \_ экземпляра мсвм метриксервице.
ms.assetid: 4E24D675-8265-4B5E-9551-550510B138FE
title: Класс Msvm_MetricServiceCapabilities
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricServiceCapabilities
- Msvm_MetricServiceCapabilities.InstanceID
- Msvm_MetricServiceCapabilities.Caption
- Msvm_MetricServiceCapabilities.Description
- Msvm_MetricServiceCapabilities.ElementName
- Msvm_MetricServiceCapabilities.ElementNameEditSupported
- Msvm_MetricServiceCapabilities.MaxElementNameLen
- Msvm_MetricServiceCapabilities.RequestedStatesSupported
- Msvm_MetricServiceCapabilities.ElementNameMask
- Msvm_MetricServiceCapabilities.ControllableMetrics
- Msvm_MetricServiceCapabilities.MetricsControlTypes
- Msvm_MetricServiceCapabilities.ControllableManagedElements
- Msvm_MetricServiceCapabilities.ManagedElementControlTypes
- Msvm_MetricServiceCapabilities.SupportedMethods
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 37fed3fead642ecfc5370d55c9f8b954477406b4b276cac392d9776a0cefb338
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521334"
---
# <a name="msvm_metricservicecapabilities-class"></a>\_Класс мсвм метриксервицекапабилитиес

Описывает возможности связанного экземпляра [**мсвм \_ метриксервице**](msvm-metricservice.md) .

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricServiceCapabilities : CIM_MetricServiceCapabilities
{
  string  InstanceID;
  string  Caption = "Hyper-V Metric Service Capabilities";
  string  Description = "Defines Hyper-V Metric Service Capabilities";
  string  ElementName = "Hyper-V Metric Service Capabilities";
  boolean ElementNameEditSupported;
  unit16  MaxElementNameLen;
  unit16  RequestedStatesSupported[];
  string  ElementNameMask;
  string  ControllableMetrics[];
  uint16  MetricsControlTypes[];
  string  ControllableManagedElements[];
  uint16  ManagedElementControlTypes[];
  uint16  SupportedMethods[];
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ метриксервицекапабилитиес** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ метриксервицекапабилитиес** имеет следующие свойства.

<dl> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Краткое описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности службы метрик Hyper-V".

</dd> <dt>

**контроллаблеманажеделементс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **arrayType** ("индексированный")
</dt> </dl>

Определяет экземпляры [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , которые могут управляться связанным экземпляром **CIM \_ метриксервице** . Если это свойство имеет **значение NULL**, можно управлять всеми элементами. Это свойство наследуется от **CIM \_ метриксервицекапабилитиес**.

</dd> <dt>

**контроллаблеметрикс**
</dt> <dd> <dl> <dt>

Тип данных: массив **строк**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **arrayType** ("индексированный")
</dt> </dl>

Определяет экземпляры **CIM \_ басеметрикдефинитион** , которые могут управляться связанным экземпляром **CIM \_ метриксервице** . Если это свойство имеет **значение NULL**, можно управлять всеми метриками. Это свойство наследуется от **CIM \_ метриксервицекапабилитиес**.

</dd> <dt>

**Описание**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Описание объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "определяет возможности службы метрик Hyper-V".

</dd> <dt>

**ElementName**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Отображаемое имя объекта. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)и всегда имеет значение "возможности службы метрик Hyper-V".

</dd> <dt>

**елементнамидитсуппортед**
</dt> <dd> <dl> <dt>

Тип данных: **логический**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, можно ли изменить свойство **ElementName** . Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.

</dd> <dt>

**елементнамемаск**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Задает ограничения для **ElementName**, выраженные в виде регулярного выражения. Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.

</dd> <dt>

**InstanceID**
</dt> <dd> <dl> <dt>

Тип данных: **строка**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **ключ**
</dt> </dl>

Уникально идентифицирует экземпляр этого класса. Это свойство наследуется от [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement).

</dd> <dt>

**манажеделементконтролтипес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **arrayType** ("индексированный")
</dt> </dl>

Определяет тип элемента управления, поддерживаемого связанным экземпляром **CIM \_ метриксервице** для объекта [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , идентифицируемого значением по тому же индексу массива в свойстве **контроллаблеманажеделементс** . Если это свойство имеет **значение NULL**, поддерживаются все типы элементов управления. Это свойство наследуется от **CIM \_ метриксервицекапабилитиес**.



| Значение                                                                                   | Значение                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Неизвестно<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | Массовость<br/>            |
| <dl> <dt>4</dt> </dl>            | Оба<br/>            |
| <dl> <dt>5.. 32767</dt> </dl>     | Зарезервировано DMTF<br/>   |
| <dl> <dt>32768.. 65535</dt> </dl> | Зависит от поставщика<br/> |



 

</dd> <dt>

**макселементнамелен**
</dt> <dd> <dl> <dt>

Тип данных: **unit16**
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **MaxValue** (256)
</dt> </dl>

Задает максимальную поддерживаемую длину свойства **ElementName** . Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.

</dd> <dt>

**метриксконтролтипес**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> <dt>

Квалификаторы: **arrayType** ("индексированный")
</dt> </dl>

Определяет тип элемента управления, поддерживаемого связанным экземпляром **CIM \_ метриксервице** для **\_ басеметрикдефинитион CIM** , идентифицируемого значением по тому же индексу массива в свойстве **контроллаблеметрикс** . Если это свойство имеет **значение NULL**, поддерживаются все типы элементов управления. Это свойство наследуется от **CIM \_ метриксервицекапабилитиес**.



| Значение                                                                                   | Значение                    |
|-----------------------------------------------------------------------------------------|----------------------------|
| <dl> <dt>0</dt> </dl>            | Неизвестно<br/>         |
| <dl> <dt>2</dt> </dl>            | Discrete<br/>        |
| <dl> <dt>3</dt> </dl>            | Массовость<br/>            |
| <dl> <dt>4</dt> </dl>            | Оба<br/>            |
| <dl> <dt>5.. 32767</dt> </dl>     | Зарезервировано DMTF<br/>   |
| <dl> <dt>32768.. 65535</dt> </dl> | Зависит от поставщика<br/> |



 

</dd> <dt>

**рекуестедстатессуппортед**
</dt> <dd> <dl> <dt>

Тип данных: массив **unit16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает возможные состояния, которые могут быть запрошены при использовании метода **RequestStateChange** для включенного логического элемента. Это свойство наследуется от **CIM \_ енабледлогикалелементкапабилитиес**.



| Значение                                                                         | Значение              |
|-------------------------------------------------------------------------------|----------------------|
| <dl> <dt>2</dt> </dl>  | Активировано<br/>   |
| <dl> <dt>3</dt> </dl>  | Отключит<br/>  |
| <dl> <dt>4</dt> </dl>  | Завершение работы<br/> |
| <dl> <dt>6</dt> </dl>  | Автономная миграция<br/>   |
| <dl> <dt>7</dt> </dl>  | Тестирование<br/>      |
| <dl> <dt>8</dt> </dl>  | Которого<br/>     |
| <dl> <dt>9</dt> </dl>  | Замораживани<br/>   |
| <dl> <dt>10</dt> </dl> | Перезагрузка<br/>    |
| <dl> <dt>11</dt> </dl> | Reset<br/>     |



 

</dd> <dt>

**SupportedMethods**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16** , массив
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает методы, поддерживаемые службой метрики. Это свойство наследуется от **CIM \_ метриксервицекапабилитиес**.



| Значение                                                                                   | Значение                                                                                         |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>2</dt> </dl>            | Поддерживается метод [**контролметрикс**](controlmetrics-msvm-metricservice.md) .<br/> |
| <dl> <dt>3</dt> </dl>            | Поддерживается метод **контролметриксбикласс** .<br/>                                   |
| <dl> <dt>4</dt> </dl>            | Поддерживается метод **шовметрикс** .<br/>                                             |
| <dl> <dt>5</dt> </dl>            | Поддерживается метод **шовметриксбикласс** .<br/>                                      |
| <dl> <dt>6</dt> </dl>            | Поддерживается метод **жетметриквалуес** .<br/>                                         |
| <dl> <dt>7</dt> </dl>            | Поддерживается метод **контролсамплетимес** .<br/>                                      |
| <dl> <dt>8.. 32767</dt> </dl>     | Зарезервировано DMTF<br/>                                                                        |
| <dl> <dt>32768.. 65535</dt> </dl> | Зависит от поставщика<br/>                                                                      |



 

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_МЕТРИКСЕРВИЦЕКАПАБИЛИТИЕС CIM**](cim-metricservicecapabilities.md)
</dt> <dt>

[**Мсвм \_ метриксервице**](msvm-metricservice.md)
</dt> </dl>

 

