---
description: 'Сообщает следующее: метрики, доступные для сбора для всех экземпляров класса CIM, классы CIM, для которых метрика, определенная экземпляром CIM \_ басеметрикдефинитион, доступна для сбора, а также сведения о том, собирается ли определенная метрика для управляемого элемента в данный момент.'
ms.assetid: 0115a5b5-2824-4c43-a8dc-757524c5d3dd
title: Метод Шовметриксбикласс класса CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ShowMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: c70d81f153471e841803dde195f09886137f29b390298c2c7d09ce69ad1648e6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119694955"
---
# <a name="showmetricsbyclass-method-of-the-cim_metricservice-class"></a>Метод Шовметриксбикласс \_ класса CIM метриксервице

Сообщает следующее: метрики, доступные для сбора для всех экземпляров класса CIM, классы CIM, для которых метрика, определенная экземпляром [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , доступна для сбора, а также сведения о том, собирается ли определенная метрика для управляемого элемента в данный момент.

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

При успешном выполнении может содержать ссылки на экземпляры объектов [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , определяющие метрики, доступные для сбора [**для \_ манажеделемент CIM**](cim-managedelement.md) , идентифицируемые параметром *subject* .

</dd> <dt>

*MetricNames* \[ заполняет\]
</dt> <dd>

При успешном выполнении каждый индекс массива должен содержать значение свойства **Name** для экземпляра [**CIM \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , на который ссылается соответствующий индекс массива параметра *дефинитионлист* .

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

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**\_МЕТРИКСЕРВИЦЕ CIM**](cim-metricservice.md)
</dt> </dl>

 

 




