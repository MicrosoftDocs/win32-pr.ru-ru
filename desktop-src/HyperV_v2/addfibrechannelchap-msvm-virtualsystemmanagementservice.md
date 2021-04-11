---
description: Добавляет параметры DH-CHAP (протокол проверки пароля Диффи-Хелмана) в виртуальный порт Fibre Channel виртуальной машины.
ms.assetid: b9799ea4-f948-4b5c-bd18-1faa90213bb3
title: Метод Аддфибречаннелчап класса Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFibreChannelChap
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 07151a902efa8f8077debc44bd732286c0a96a81
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998566"
---
# <a name="addfibrechannelchap-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Метод Аддфибречаннелчап \_ класса Виртуалсистемманажементсервице мсвм

Добавляет параметры DH-CHAP (протокол проверки пароля Диффи-Хелмана) в виртуальный порт Fibre Channel виртуальной машины. Этот метод завершится ошибкой, если виртуальная машина запущена.

## <a name="syntax"></a>Синтаксис


```mof
uint32 AddFibreChannelChap(
  [in] string FcPortSettings[],
  [in] uint8  SecretEncoding,
  [in] uint8  SharedSecret[]
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Фкпортсеттингс* \[ окне\]
</dt> <dd>

Массив строк, содержащий встроенный экземпляр класса [**мсвм \_ синсетикфкпортсеттингдата**](msvm-syntheticfcportsettingdata.md) , который описывает параметры для портов искусственного Fibre Channel для виртуальных машин. Свойство **InstanceId** каждого из этих экземпляров определяет изменяемые элементы.

</dd> <dt>

*Секретенкодинг* \[ окне\]
</dt> <dd>

Указывает тип кодировки для общего секрета.

<dt>

<span id="Printable_ASCII"></span><span id="printable_ascii"></span><span id="PRINTABLE_ASCII"></span>

**Печатный текст ASCII** (1)


</dt> <dd></dd> <dt>

<span id="Binary"></span><span id="binary"></span><span id="BINARY"></span>

**Двоичный** (2)


</dt> <dd></dd> </dl> </dd> <dt>

*SharedSecret* \[ окне\]
</dt> <dd>

Указывает общий секрет.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Этот метод возвращает одно из следующих значений.

<dl> <dt>

**Завершено без ошибок** (0)
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
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                              |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                                    |
| Пространство имен<br/>                | Корневая \\ виртуализация \\ версии 2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Виндовсвиртуализатион. v2. mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Мсвм \_ виртуалсистемманажементсервице**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




