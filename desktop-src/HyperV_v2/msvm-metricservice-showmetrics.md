---
description: Показывает указанные метрики.
ms.assetid: 3716b5e6-b360-4719-a0f3-60b8d39deb31
title: Метод Шовметрикс класса Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9823ea61864b0d87245ebe8b171195a2fd3c411a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103913124"
---
# <a name="showmetrics-method-of-the-msvm_metricservice-class"></a>Метод Шовметрикс \_ класса Метриксервице мсвм

Показывает указанные метрики.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ShowMetrics(
  [in]  CIM_ManagedElement       REF Subject,
  [in]  CIM_BaseMetricDefinition REF Definition,
  [out] CIM_ManagedElement       REF ManagedElements[],
  [out] CIM_BaseMetricDefinition REF DefinitionList[],
  [out] string                       MetricNames[],
  [out] uint16                       MetricCollectionEnabled[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Тема* \[ окне\]
</dt> <dd>

Параметр Subject определяет экземпляр [**CIM \_ манажеделемент**](cim-managedelement.md) , для которого метод возвращает ссылки на экземпляры [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, которые фиксируются для **CIM \_ манажеделемент**.

</dd> <dt>

*Определение* \[ окне\]
</dt> <dd>

Параметр определения определяет экземпляр [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md). Метод возвращает ссылки на экземпляры [**CIM \_ манажеделемент**](cim-managedelement.md) , для которых можно собирать метрики, определенные экземпляром **CIM \_ басеметрикдефинитион** .

</dd> <dt>

*Манажеделементс* \[ заполняет\]
</dt> <dd>

После успешного завершения метода параметр *манажеделементс* \[ \] может содержать ссылки на [**CIM \_ манажеделемент**](cim-managedelement.md) , для которых метрика, идентифицируемая параметром *определения* , доступна для коллекции.

</dd> <dt>

*Дефинитионлист* \[ заполняет\]
</dt> <dd>

После успешного завершения метода параметр *дефинитионлист* может содержать ссылки на экземпляры [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, доступные для сбора для [**CIM \_ манажеделемент**](cim-managedelement.md) , определяемого параметром *subject* .

</dd> <dt>

*MetricNames* \[ заполняет\]
</dt> <dd>

После успешного завершения метода каждый индекс массива параметра *MetricNames* должен содержать значение свойства Name для экземпляра [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , на который ссылается соответствующий индекс массива параметра *дефинитионлист* .

</dd> <dt>

*Метрикколлектионенаблед* \[ заполняет\]
</dt> <dd>

Параметр *метрикколлектионенаблед* указывает, собирается ли метрика для управляемого элемента.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Включить** (2)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Отключить** (3)


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

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Успешно** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> <dt>

**Сбой** (2)
</dt> <dt>

**Метод зарезервирован** (..)
</dt> <dt>

**Зависит от поставщика** (32768.65 535)
</dt> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ метриксервице**](msvm-metricservice.md)
</dt> </dl>

 

 




