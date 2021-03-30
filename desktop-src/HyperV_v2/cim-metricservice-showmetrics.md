---
description: 'Выводит следующие сведения: метрики, доступные для сбора для управляемого элемента, управляемые элементы, для которых метрика, определенная экземпляром CIM \_ басеметрикдефинитион, доступна для сбора, а также сведения о том, собирается ли определенная метрика для управляемого элемента в данный момент.'
ms.assetid: 5af430d2-9ab3-4bee-ad51-d9045b51172a
title: Метод Шовметрикс класса CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1e0e062adaefd6c6d9bdabe6f168bd64e789acc2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104156594"
---
# <a name="showmetrics-method-of-the-cim_metricservice-class"></a>Метод Шовметрикс \_ класса CIM метриксервице

Выводит следующие сведения: метрики, доступные для сбора для управляемого элемента, управляемые элементы, для которых метрика, определенная экземпляром [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , доступна для сбора, а также сведения о том, собирается ли определенная метрика для управляемого элемента в данный момент.

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

Определяет экземпляр [**CIM \_ манажеделемент**](cim-managedelement.md) , для которого метод возвращает ссылки на экземпляры [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, которые фиксируются для **CIM \_ манажеделемент**.

</dd> <dt>

*Определение* \[ окне\]
</dt> <dd>

Идентифицирует экземпляр [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md). Метод возвращает ссылки на экземпляры [**CIM \_ манажеделемент**](cim-managedelement.md) , для которых можно собирать метрики, определенные экземпляром **CIM \_ басеметрикдефинитион** .

</dd> <dt>

*Манажеделементс* \[ заполняет\]
</dt> <dd>

При успешном выполнении может содержать ссылки на объекты [**CIM \_ манажеделемент**](cim-managedelement.md) , для которых метрика, определяемая параметром *определения* , доступна для коллекции.

</dd> <dt>

*Дефинитионлист* \[ заполняет\]
</dt> <dd>

При успешном выполнении может содержать ссылки на экземпляры объектов [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, доступные для сбора [**для \_ манажеделемент CIM**](cim-managedelement.md) , идентифицируемые параметром *subject* .

</dd> <dt>

*MetricNames* \[ заполняет\]
</dt> <dd>

При успешном выполнении каждый индекс массива должен содержать значение свойства **Name** для экземпляра [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , на который ссылается соответствующий индекс массива параметра *дефинитионлист* .

</dd> <dt>

*Метрикколлектионенаблед* \[ заполняет\]
</dt> <dd>

Указывает, собирается ли метрика для управляемого элемента.

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

Возвращает значение 0 в случае успешного выполнения; в противном случае возвращает ошибку.

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

[**\_МЕТРИКСЕРВИЦЕ CIM**](cim-metricservice.md)
</dt> </dl>

 

 




