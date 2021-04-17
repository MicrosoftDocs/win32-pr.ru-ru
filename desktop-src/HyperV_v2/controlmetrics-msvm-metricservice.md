---
description: Используется для управления сбором метрик для управляемого элемента или элементов.
ms.assetid: 3DC043ED-A790-4322-BF80-55961E9946C2
title: Метод Контролметрикс класса Msvm_MetricService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ControlMetrics
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b12fbf71b860571bb3bb5ee06cb58483e782f479
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105663744"
---
# <a name="controlmetrics-method-of-the-msvm_metricservice-class"></a>Метод Контролметрикс \_ класса Метриксервице мсвм

Используется для управления сбором метрик для управляемого элемента или элементов.

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

Экземпляр [**CIM \_ манажеделемент**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement) , определяющий управляемые элементы, для которых будут собираться метрики. Если этот параметр имеет **значение NULL**, будут собираться метрики для всех управляемых элементов, связанных с параметром *определения* .

</dd> <dt>

*Определение* \[ окне\]
</dt> <dd>

Экземпляр [**\_ басеметрикдефинитион мсвм**](msvm-basemetricdefinition.md) , указывающий метрики, которые будут собраны. Если этот параметр имеет **значение NULL**, будут собираться метрики для всех определений, связанных с управляемым элементом, идентифицируемым параметром *subject* .

</dd> <dt>

*Метрикколлектионенаблед* \[ окне\]
</dt> <dd>

Указывает операцию для выполнения в коллекции метрик. Это должно быть одно из следующих значений.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Включить** (2)


</dt> <dd>

Включите сбор метрик.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Отключить** (3)


</dt> <dd>

Отключение сбора метрик.

</dd> <dt>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>

<span id="Reset"></span><span id="reset"></span><span id="RESET"></span>**Сброс** (4)


</dt> <dd>

Сбросьте значения метрик.

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**Зарезервировано DMTF** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Поставщик зарезервирован** (32768.. 65535)


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

## <a name="remarks"></a>Комментарии

Этот метод завершится со сбоем в следующих случаях:

-   Параметры *subject* и *definition* равны **null**.
-   Параметры *subject* и *definition* не равны **null** и не имеют экземпляра [**мсвм \_ метрикдефформе**](msvm-metricdefforme.md) , связывающего два экземпляра.
-   Параметр *определения* является ссылкой на экземпляр [**мсвм \_ басеметрикдефинитион**](msvm-basemetricdefinition.md) , который не связан с [**мсвм \_ метриксервице**](msvm-metricservice.md) до [**мсвм \_ сервицеаффектселемент**](msvm-serviceaffectselement.md).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ метриксервице**](msvm-metricservice.md)
</dt> </dl>

 

