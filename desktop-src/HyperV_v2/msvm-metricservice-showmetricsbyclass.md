---
description: Показывает метрики по классу.
ms.assetid: a08c0749-b60b-4b8a-996f-b3bbaf1fb2d3
title: Метод Шовметриксбикласс класса Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 40865847b1deef877c70c1c99349c12915a464b394a38b5b804ea9139d5d0cf1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118147513"
---
# <a name="showmetricsbyclass-method-of-the-msvm_metricservice-class"></a>Метод Шовметриксбикласс \_ класса Метриксервице мсвм

Показывает метрики по классу.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ShowMetricsByClass(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Тема* \[ окне\]
</dt> <dd>

Определяет класс CIM, для которого метод возвращает ссылки на экземпляры [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, доступные для записи во всех экземплярах класса.

</dd> <dt>

*Определение* \[ окне\]
</dt> <dd>

Идентифицирует экземпляр [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md). Метод возвращает ссылки на экземпляры [**CIM \_ манажеделемент**](cim-managedelement.md) , для которых можно собирать метрики, определенные экземпляром **CIM \_ басеметрикдефинитион** .

</dd> <dt>

*Дефинитионлист* \[ заполняет\]
</dt> <dd>

После успешного завершения метода может содержать ссылки на экземпляры [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, доступные для сбора для [**\_ манажеделемент CIM**](cim-managedelement.md) , идентифицируемые параметром *subject* .

</dd> <dt>

*MetricNames* \[ заполняет\]
</dt> <dd>

После успешного завершения метода каждый индекс массива содержит значение свойства **Name** для экземпляра [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , на который ссылается соответствующий индекс массива параметра *дефинитионлист* .

</dd> <dt>

*Метрикколлектионенаблед* \[ заполняет\]
</dt> <dd>

Указывает, собирается ли метрика для всех экземпляров класса управляемых элементов.

<dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Включено** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Отключено** (3)


</dt> <dd></dd> <dt>

<span id="Reserved"></span><span id="reserved"></span><span id="RESERVED"></span>

**Зарезервировано** (4)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

**Поставщик зарезервирован** (32768.. 65535)


</dt> <dd></dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений:

<dl> <dt>

**Успешно** ()
</dt> <dt>

**Не поддерживается** ()
</dt> <dt>

**Сбой** ()
</dt> <dt>

**Метод зарезервирован** ()
</dt> <dt>

**Зависит от поставщика** ()
</dt> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Мсвм \_ метриксервице**](msvm-metricservice.md)
</dt> </dl>

 

 




