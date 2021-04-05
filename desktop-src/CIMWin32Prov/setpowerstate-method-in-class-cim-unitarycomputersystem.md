---
description: Метод SetPowerState \_ класса CIM унитарикомпутерсистем устанавливает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние.
ms.assetid: a02991d5-3c93-4579-b1f5-f70ad7c7052b
ms.tgt_platform: multiple
title: Метод SetPowerState класса CIM_UnitaryComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_UnitaryComputerSystem.SetPowerState
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4d9b69306c7bb362dceaee254be5dae8f5d37a52
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103990334"
---
# <a name="setpowerstate-method-of-the-cim_unitarycomputersystem-class"></a>Метод SetPowerState \_ класса CIM унитарикомпутерсистем

Метод **SetPowerState** \_ класса CIM унитарикомпутерсистем устанавливает требуемое состояние электропитания для логического устройства и когда устройство должно быть переведено в это состояние. В подклассе набор возможных кодов возврата должен быть указан с помощью квалификатора **ValueMap** в методе. Строки, в которые преобразуются содержимое **ValueMap** , также должны быть указаны в подклассе как квалификатор массива **Values** . Этот метод наследуется [**от \_ CIM**](cim-logicaldevice.md)-ого модели.

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetPowerState(
  [in] uint16   PowerState,
  [in] datetime Time
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*PowerState* \[ окне\]
</dt> <dd>

Значение **ValueMap** , указывающее требуемое состояние питания для этого логического устройства.

<dt>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>

<span id="Full_Power"></span><span id="full_power"></span><span id="FULL_POWER"></span>**Полная мощность** (1)


</dt> <dd>

Полная мощность.

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Энергосбережение **— режим низкого энергопотребления** (2)


</dt> <dd>

Режим энергосбережения с низким энергопотреблением.

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>Энергосбережение **— ждущий режим** (3)


</dt> <dd>

Энергосбережение в режиме ожидания.

</dd> <dt>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>

<span id="Power_Save_-_Other"></span><span id="power_save_-_other"></span><span id="POWER_SAVE_-_OTHER"></span>**Энергосбережение — другие** (4)


</dt> <dd>

Энергосбережение.

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Цикл электропитания** (5)


</dt> <dd>

Цикл электропитания.

</dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Выключение питания** (6)


</dt> <dd>

Выключение питания.

</dd> <dt>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>

<span id="Hibernate"></span><span id="hibernate"></span><span id="HIBERNATE"></span>**Режим гибернации** (7)


</dt> <dd>

Режим гибернации.

</dd> <dt>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>

<span id="Soft_Off"></span><span id="soft_off"></span><span id="SOFT_OFF"></span>**Мягкое отключение** (8)


</dt> <dd>

Мягкое отключение.

</dd> </dl> </dd> <dt>

*Время* \[ окне\]
</dt> <dd>

Указывает, когда должно быть установлено состояние электропитания: как обычное значение даты-времени или как значение интервала (где интервал начинается при получении вызова метода). Если параметр *PowerState* равен 5 ("цикл электропитания"), параметр *времени* указывает, когда устройство должно снова включить питание. Выключение осуществляется немедленно.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает 0 (нуль) в случае успеха, 1 (один), если *указанный запрос* о сбое и *время* не поддерживаются, и другое значение, если произошла какая-либо другая ошибка.

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

[\_УНИТАРИКОМПУТЕРСИСТЕМ CIM](setpowerstate-method-in-class-cim-unitarycomputersystem.md)
</dt> <dt>

[**\_УНИТАРИКОМПУТЕРСИСТЕМ CIM**](cim-unitarycomputersystem.md)
</dt> </dl>

 

 




