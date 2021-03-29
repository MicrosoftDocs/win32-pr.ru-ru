---
description: Определяет запланированную виртуальную систему.
ms.assetid: f129554b-e43e-4c3a-8418-d5d810f4c4b5
title: Метод Дефинепланнедсистем класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.DefinePlannedSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: d5e9fa8a49e86850d044216a3d95e3d4dd756fc0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540298"
---
# <a name="defineplannedsystem-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Метод Дефинепланнедсистем \_ класса Виртуалсистемманажементсервице мсвм

Определяет запланированную виртуальную систему.

Входные данные, которые указаны не полностью, могут быть заполнены значениями по умолчанию.

## <a name="syntax"></a>Синтаксис


```mof
uint32 DefinePlannedSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*SystemSettings* \[ окне\]
</dt> <dd>

Параметры системы для виртуальной системы.

</dd> <dt>

*Ресаурцесеттингс* \[ окне\]
</dt> <dd>

Параметры ресурсов для виртуальной системы.

</dd> <dt>

*Референцеконфигуратион* \[ окне\]
</dt> <dd>

[**\_ Виртуалсистемсеттингдата CIM**](cim-virtualsystemsettingdata.md) , содержащий конфигурацию ссылки.

</dd> <dt>

*Ресултингсистем* \[ заполняет\]
</dt> <dd>

Объект [**\_ ComputerSystem CIM**](cim-computersystem.md) , содержащий результирующую систему.

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

При успешном выполнении возвращает 0 или 4096; в противном случае возвращает ошибку.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Не поддерживается** (1)
</dt> <dt>

**Сбой** (2)
</dt> <dt>

**Время ожидания** (3)
</dt> <dt>

**Недопустимый параметр** (4)
</dt> <dt>

**Зарезервировано DMTF** (..)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Метод зарезервирован** (4097.. 32767)
</dt> <dt>

**Зависит от поставщика** (32768.65 535)
</dt> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Только для \[ настольных приложений Windows 10\]<br/>                                                             |
| Минимальная версия сервера<br/> | Windows Server 2016<br/>                                                                          |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

