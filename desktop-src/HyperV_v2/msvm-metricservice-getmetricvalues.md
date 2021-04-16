---
description: Возвращает значения метрик.
ms.assetid: 71c614ef-a005-45aa-9999-a19dc9f9c0df
title: Метод Жетметриквалуес класса Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.GetMetricValues
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fe3e32b21ec0baa497fcef781e1b48fae37fbf66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105664510"
---
# <a name="getmetricvalues-method-of-the-msvm_metricservice-class"></a>Метод Жетметриквалуес \_ класса Метриксервице мсвм

Возвращает значения метрик.

## <a name="syntax"></a>Синтаксис


```mof
uint32 GetMetricValues(
  [in]  CIM_BaseMetricDefinition REF Definition,
  [in]  uint16                       Range,
  [in]  uint16                       Count,
  [out] CIM_BaseMetricValue      REF Values[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Определение* \[ окне\]
</dt> <dd>

Идентифицирует [**\_ басеметрикдефинитион CIM**](cim-basemetricdefinition.md) , для которого будут возвращены метрики.

</dd> <dt>

*Диапазон значений* \[ окне\]
</dt> <dd>

Определяет, как выбираются экземпляры. Алгоритм упорядочивания экземпляров является специфическим определением метрик.

<dt>

<span id="Minimum"></span><span id="minimum"></span><span id="MINIMUM"></span>

**Минимум** (2)


</dt> <dd></dd> <dt>

<span id="Maximum"></span><span id="maximum"></span><span id="MAXIMUM"></span>

**Максимум** (3)


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Specific"></span><span id="vendor_specific"></span><span id="VENDOR_SPECIFIC"></span>

**Зависит от поставщика** (32768.65 535)


</dt> <dd></dd> </dl> </dd> <dt>

*Количество* \[ окне\]
</dt> <dd>

Определяет максимальное число экземпляров, возвращаемых методом.

</dd> <dt>

*Значения* \[ заполняет\]
</dt> <dd>

После успешного завершения метода содержит ссылки на экземпляры [**CIM \_ басеметриквалуе**](cim-basemetricvalue.md), отфильтрованные в соответствии со значениями входных параметров.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений:

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

 

 




