---
description: Метод Сетурженци задает требуемый уровень срочности сигнала.
ms.assetid: ac2e7fda-1317-440a-adbd-1ef0844d124c
ms.tgt_platform: multiple
title: Метод Сетурженци класса CIM_AlarmDevice
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AlarmDevice.SetUrgency
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 35918677e210ac2fe7ac4798a04db9dc628f5fa1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990571"
---
# <a name="seturgency-method-of-the-cim_alarmdevice-class"></a>Метод Сетурженци \_ класса CIM алармдевице

Метод **сетурженци** задает требуемый уровень срочности сигнала.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetUrgency(
  [in] uint16 RequestedUrgency
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Рекуестедурженци* \[ окне\]
</dt> <dd>

Относительная частота, с которой будильник мигает, вибратес или выдает звуковые сигналы. Следующие значения относятся к свойству **срочности** в [**CIM \_ алармдевице**](cim-alarmdevice.md).

<dt>

0
</dt> <dd>

Неизвестно.

</dd> <dt>

1
</dt> <dd>

Другое

</dd> <dt>

2
</dt> <dd>

Не поддерживается.

</dd> <dt>

3
</dt> <dd>

Извещен.

</dd> <dt>

4
</dt> <dd>

Не является критическим.

</dd> <dt>

5
</dt> <dd>

Критическое —

</dd> <dt>

6
</dt> <dd>

Неустранимая.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль) при успешном выполнении, 1 (один), если запрошенный уровень срочности не поддерживается, и любое другое число для указания ошибки.

## <a name="remarks"></a>Комментарии

В настоящее время этот метод не реализован инструментарием WMI. Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[\_АЛАРМДЕВИЦЕ CIM](seturgency-method-in-class-cim-alarmdevice.md)
</dt> <dt>

[**\_АЛАРМДЕВИЦЕ CIM**](cim-alarmdevice.md)
</dt> </dl>

 

