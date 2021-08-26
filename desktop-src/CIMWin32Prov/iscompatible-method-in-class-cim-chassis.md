---
description: Проверяет, может ли физический корпус, на который указывает ссылка, находиться в физическом пакете или вставляться в него.
ms.assetid: 9a1aa1b7-2b95-4887-9d14-e416ff69f9df
ms.tgt_platform: multiple
title: Метод, совместимый с классом CIM_Chassis
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Chassis.IsCompatible
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: a0bbaa063006d6c7829b3a38b0bc28be78c451b0f2302897a456e1be4cf9eb6c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120003294"
---
# <a name="iscompatible-method-of-the-cim_chassis-class"></a>Метод, совместимый с \_ классом CIM Chassis

Метод, **совместимый** с, позволяет проверить, может ли связанный физический корпус быть включен в физический пакет или вставляться в него. В подклассе набор возможных кодов возврата можно указать с помощью квалификатора [**ValueMap**](/windows/desktop/WmiSdk/standard-qualifiers) в методе. Строки, в которые транслируются содержимое **ValueMap** , также можно указать в подклассе как квалификатор массива **значений** . Этот метод наследуется от [**CIM \_ фисикалпаккаже**](cim-physicalpackage.md).

> [!IMPORTANT]
> Классы CIM (модель CIM) в DMTF (распределенная задача управления) являются родительскими классами, на которых строятся классы WMI. В настоящее время WMI поддерживает только [схемы версии CIM 2. x](https://dmtf.org/standards/cim/schemas).

 

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 IsCompatible(
  [in] CIM_PhysicalElement REF ElementToCheck
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Елементточекк* \[ окне\]
</dt> <dd>

Ссылка на физический элемент, для которого проверяется совместимость.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение 0 (нуль) при успешном выполнении, 1 (один), если запрос не поддерживается, и любое другое число для указания ошибки.

## <a name="remarks"></a>Remarks

В настоящее время этот метод не реализован инструментарием WMI. Чтобы использовать этот метод, его необходимо реализовать в собственном поставщике.

Эта документация является производной от описаний класса CIM, опубликованных в формате DMTF. Корпорация Майкрософт могла внести изменения в Исправление незначительных ошибок, соответствовать стандартам документации пакета Microsoft SDK или предоставить дополнительные сведения.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                          |
| Пространство имен<br/>                | Корневой \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**\_Корпус CIM**](iscompatible-method-in-class-cim-chassis.md)
</dt> <dt>

[**\_Корпус CIM**](cim-chassis.md)
</dt> </dl>

 

