---
description: Включает и отключает сбор метрик.
ms.assetid: afb90863-e70a-46e5-b1b7-d959dcacc306
title: Метод Контролметрикс класса CIM_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 60a7d0b34227594cf7146a988aa7e0d232f2d6cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104264728"
---
# <a name="controlmetrics-method-of-the-cim_metricservice-class"></a>Метод Контролметрикс \_ класса CIM метриксервице

Включает и отключает сбор метрик. **Контролметрикс** используется для управления сбором каждого типа метрики для [**CIM \_ манажеделемент**](cim-managedelement.md), коллекции заданного типа метрики для всех управляемых элементов или коллекции определенной метрики для конкретного управляемого элемента.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ControlMetrics(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Тема* \[ окне\]
</dt> <dd>

[**\_ Манажеделемент CIM**](cim-managedelement.md) , определяющий управляемые элементы, для которых будут контролироваться метрики.

</dd> <dt>

*Определение* \[ окне\]
</dt> <dd>

Определяет [**CIM- \_ басеметрикдефинитион**](cim-basemetricdefinition.md) , для которой будут контролироваться метрики.

</dd> <dt>

*Метрикколлектионенаблед* \[ окне\]
</dt> <dd>

Указывает требуемую операцию для метрик.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Включить** (2)


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Отключить** (3)


</dt> <dd></dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

**Сброс** (4)


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

 

 




