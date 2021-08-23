---
description: Определяет связь между \_ Басеметрикдефинитион мсвм и CIM \_ манажеделемент для определения метрик для второго. Определение метрик задается контекстом Манажеделемент, поэтому определение зависит от элемента.
ms.assetid: 528d9b1a-089d-48ae-b5a6-40bc9d09191c
title: Класс Msvm_MetricDefForME
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricDefForME
- Msvm_MetricDefForME.Antecedent
- Msvm_MetricDefForME.Dependent
- Msvm_MetricDefForME.MetricCollectionEnabled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 6c6da093c5f902657c51285e124593e0bf44a9be0bf32ed87a55d3349cbfba92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119521604"
---
# <a name="msvm_metricdefforme-class"></a>\_Класс мсвм метрикдефформе

Определяет связь между [**\_ басеметрикдефинитион Мсвм**](msvm-basemetricdefinition.md) и [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) для определения метрик для второго. Определение метрик задается контекстом Манажеделемент, поэтому определение зависит от элемента.

Следующий синтаксис является упрощенным MOF-файлным (MOF) кодом и включает все наследуемые свойства.

## <a name="syntax"></a>Синтаксис

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_MetricDefForME : CIM_MetricDefForME
{
  CIM_ManagedElement       REF Antecedent;
  CIM_BaseMetricDefinition REF Dependent;
  uint16                       MetricCollectionEnabled = 2;
};
```

## <a name="members"></a>Члены

Класс **мсвм \_ метрикдефформе** имеет следующие типы членов:

-   [Свойства](#properties)

### <a name="properties"></a>Элемент Property

Класс **мсвм \_ метрикдефформе** имеет следующие свойства.

<dl> <dt>

**Завершил**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр класса [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , представляющий управляемый элемент, который может иметь метрики типа, определенные **зависимым от** него. Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**Него**
</dt> <dd> <dl> <dt>

Тип данных: **[ **CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Ссылка на экземпляр класса [**CIM \_ басеметрикдефинитион**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , представляющий определение метрики, к которому может быть применена **предшествующая задача** . Это свойство наследуется [**от \_ зависимости CIM**](/windows/desktop/CIMWin32Prov/cim-dependency).

</dd> <dt>

**метрикколлектионенаблед**
</dt> <dd> <dl> <dt>

Тип данных: **UInt16**
</dt> <dt>

Тип доступа: только для чтения
</dt> </dl>

Указывает, собираются ли метрики, определенные **зависимыми** , для **предшествующей задачи**. Это может быть одно из следующих значений.



| Значение                                                                                                                                                                                                                                                               | Значение                                                                  |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span><dl> <dt>**Включено**</dt> <dt>2</dt> </dl>                                         | Метрика собирается.<br/>                                |
| <span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span><dl> <dt>**Отключено**</dt> <dt>3</dt> </dl>                                     | Метрика не собирается.<br/>                            |
| <span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span><dl> <dt>**Зарезервировано**</dt> <dt>4</dt> </dl>                                     |                                                                          |
| <span id="PartiallyEnabled"></span><span id="partiallyenabled"></span><span id="PARTIALLYENABLED"></span><dl> <dt>**Партиалленаблед**</dt> <dt>32768</dt> </dl> | Метрика собирается для некоторых, но не для всех устройств.<br/> |



 

</dd> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

