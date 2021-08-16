---
description: проверяет сетевое подключение виртуальной машины в среде Windows виртуализации сети.
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Метод Тестнетворкконнектион класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.TestNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66988944b6c4f4a97a450f63964d57084fc5886716d109e655921d8744bba721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388383"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Метод Тестнетворкконнектион \_ класса Виртуалсистемманажементсервице мсвм

проверяет сетевое подключение виртуальной машины в среде Windows виртуализации сети.

## <a name="syntax"></a>Синтаксис


```mof
uint32 TestNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  boolean                                    IsSender,
  [in]  string                                     SenderIP,
  [in]  string                                     ReceiverIP,
  [in]  string                                     ReceiverMac,
  [in]  uint32                                     IsolationId,
  [in]  uint32                                     SequenceNumber,
  [out] uint32                                     RoundTripTime,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Таржетнетворкадаптер* \[ окне\]
</dt> <dd>

Ссылка на [**мсвм \_ есернетпорталлокатионсеттингдата**](msvm-ethernetportallocationsettingdata.md) , описывающий целевой сетевой адаптер.

</dd> <dt>

*Отправители* \[ окне\]
</dt> <dd>

Указывает, вызывается ли этот метод у отправителя или получателя.

</dd> <dt>

*Сендерип* \[ окне\]
</dt> <dd>

IP-адрес отправителя.

</dd> <dt>

*Рецеиверип* \[ окне\]
</dt> <dd>

Mac-адрес отправителя.

</dd> <dt>

*Рецеивермак* \[ окне\]
</dt> <dd>

Mac-адрес отправителя.

</dd> <dt>

*Исолатионид* \[ окне\]
</dt> <dd>

Идентификатор изоляции.

</dd> <dt>

*SequenceNumber* \[ окне\]
</dt> <dd>

Идентификатор изоляции.

</dd> <dt>

*Раундтриптиме* \[ заполняет\]
</dt> <dd>

Время кругового пути.

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
| Минимальная версия клиента<br/> | Windows 8.1<br/>                                                                                  |
| Минимальная версия сервера<br/> | Windows Server 2012 R2<br/>                                                                       |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

