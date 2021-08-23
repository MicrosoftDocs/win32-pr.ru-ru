---
description: Настраивает сетевые адаптеры в гостевой операционной системе.
ms.assetid: 698e0c17-f8bd-433f-b982-5481f9701ba6
title: Метод Сетгуестнетворкадаптерконфигуратион класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetGuestNetworkAdapterConfiguration
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3fb1433151c733d0c11bfd054ac5cf8f18b52d57cf683ed4662397da2eff56ff
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119500874"
---
# <a name="setguestnetworkadapterconfiguration-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Метод Сетгуестнетворкадаптерконфигуратион \_ класса Виртуалсистемманажементсервице мсвм

Настраивает сетевые адаптеры в гостевой операционной системе. эти параметры конфигурации применяются сразу же после установления связи с компонентом интеграции KVP Exchange, работающего в гостевой операционной системе.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetGuestNetworkAdapterConfiguration(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkConfiguration[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ComputerSystem* \[ окне\]
</dt> <dd>

Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , сетевые адаптеры которого должны быть настроены.

</dd> <dt>

*NetworkConfiguration* \[ окне\]
</dt> <dd>

Массив внедренных экземпляров класса [**мсвм \_ гуестнетворкадаптерконфигуратион**](msvm-guestnetworkadapterconfiguration.md) . Каждый экземпляр описывает параметры конфигурации для одного из сетевых адаптеров в виртуальной машине. Для каждого экземпляра необходимо указать свойство **DHCPEnabled** .

</dd> <dt>

*Задание* \[ заполняет\]
</dt> <dd>

Если операция выполняется асинхронно, этот метод возвратит 4096, и этот параметр будет содержать ссылку на объект, производный от [**CIM \_ конкретежоб**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Завершено без ошибок** (0)
</dt> <dt>

**Параметры метода проверены — задание запущено** (4096)
</dt> <dt>

**Сбой** (32768)
</dt> <dt>

**Отказано в доступе** (32769)
</dt> <dt>

**Не поддерживается** (32770)
</dt> <dt>

**Состояние неизвестно** (32771)
</dt> <dt>

**Время ожидания** (32772)
</dt> <dt>

**Недопустимый параметр** (32773)
</dt> <dt>

**Система используется** (32774)
</dt> <dt>

**Недопустимое состояние для этой операции** (32775)
</dt> <dt>

**Неверный тип данных** (32776)
</dt> <dt>

**Система недоступна** (32777)
</dt> <dt>

**Недостаточно памяти** (32778)
</dt> </dl>

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

