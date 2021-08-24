---
description: Настройка параметров IP сетевых адаптеров для применения к виртуальной машине после отработки отказа.
ms.assetid: a49d089e-f5dc-4bfb-9f66-2593304b9795
title: Метод Сетфаиловернетворкадаптерсеттингс класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.SetFailoverNetworkAdapterSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 744c1b2e56fb50e5a0c16db7d03d7558b1ed69360de98f69a4aac795f9f7db63
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147767"
---
# <a name="setfailovernetworkadaptersettings-method-of-the-msvm_replicationservice-class"></a>Метод Сетфаиловернетворкадаптерсеттингс \_ класса Репликатионсервице мсвм

Настройка IP-параметров сетевого адаптера для применения к виртуальной машине после отработки отказа. эти параметры конфигурации применяются после операции отработки отказа сразу же после установки связи с компонентом интеграции KVP Exchange, работающим в гостевой операционной системе.

## <a name="syntax"></a>Синтаксис


```mof
uint32 SetFailoverNetworkAdapterSettings(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkSettings[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*ComputerSystem* \[ окне\]
</dt> <dd>

Ссылка на экземпляр [**CIM \_ ComputerSystem**](/windows/desktop/CIMWin32Prov/cim-computersystem) , представляющий виртуальную машину, сетевые адаптеры которой необходимо настроить.

</dd> <dt>

*Нетворксеттингс* \[ окне\]
</dt> <dd>

Массив внедренных экземпляров объектов [**мсвм \_ фаиловернетворкадаптерсеттингдата**](msvm-failovernetworkadaptersettingdata.md) . Каждый экземпляр описывает параметры конфигурации для одного из сетевых адаптеров в виртуальной машине. Свойства **ipaddresses** и **DHCPEnabled** должны быть указаны в каждом экземпляре.

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

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 8 \[ только классические приложения\]<br/>                                                              |
| Минимальная версия сервера<br/> | Windows Server 2012 \[ только классические приложения\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**инитиатефаиловер**](initiatefailover-msvm-replicationservice.md)
</dt> <dt>

[**Мсвм \_ репликатионсервице**](msvm-replicationservice.md)
</dt> <dt>

[**ревертфаиловер**](revertfailover-msvm-replicationservice.md)
</dt> </dl>

 

