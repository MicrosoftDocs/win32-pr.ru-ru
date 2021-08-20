---
description: Управляет метриками по классу.
ms.assetid: f848fdec-561b-4be0-b1e9-a59e15196d1d
title: Метод Контролметриксбикласс класса Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetricsByClass
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d522a2c66cf8b7127520fc3ec66b809c4e825cb759de116b3a3e820eb0ae676c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120046534"
---
# <a name="controlmetricsbyclass-method-of-the-msvm_metricservice-class"></a>Метод Контролметриксбикласс \_ класса Метриксервице мсвм

Управляет метриками по классу.

## <a name="syntax"></a>Синтаксис


```mof
uint32 ControlMetricsByClass(
  [in] CIM_ManagedElement       REF Subject,
  [in] CIM_BaseMetricDefinition REF Definition,
  [in] uint16                       MetricCollectionEnabled
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Тема* \[ окне\]
</dt> <dd>

Определяет класс CIM, для которого будут контролироваться метрики.

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

 

 




