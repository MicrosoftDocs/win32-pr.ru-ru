---
description: Проверяет, можно ли включить репликацию из текущей системы узла в указанную систему восстановления.
ms.assetid: 404855d5-9a1f-4079-b46d-b378fafff5bb
title: Метод Тестрепликатионконнектион класса Msvm_ReplicationService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ReplicationService.TestReplicationConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6644ead653509d879e779928030ff8912a124ad5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "105662215"
---
# <a name="testreplicationconnection-method-of-the-msvm_replicationservice-class"></a>Метод Тестрепликатионконнектион \_ класса Репликатионсервице мсвм

Проверяет, можно ли включить репликацию из текущей системы узла в указанную систему восстановления.

## <a name="syntax"></a>Синтаксис


```mof
uint32 TestReplicationConnection(
  [in]  string              RecoveryConnectionPoint,
  [in]  uint16              RecoveryServerPortNumber,
  [in]  uint16              AuthenticationType,
  [in]  string              CertificateThumbPrint,
  [in]  boolean             BypassProxyServer,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Рековериконнектионпоинт* \[ окне\]
</dt> <dd>

Имя точки подключения. Для кластера восстановления это имя ограничения брокера. Для изолированного сервера восстановления это имя системы узла.

</dd> <dt>

*Рековерисерверпортнумбер* \[ окне\]
</dt> <dd>

Номер порта точки подключения восстановления.

</dd> <dt>

*AuthenticationType* \[ окне\]
</dt> <dd>

Схема проверки подлинности восстановления. Это должно быть одно из следующих значений.

<dt>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>

<span id="Integrated_authentication"></span><span id="integrated_authentication"></span><span id="INTEGRATED_AUTHENTICATION"></span>**Встроенная проверка подлинности** (1)


</dt> <dd>

Аутентификация Kerberos.

</dd> <dt>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>

<span id="Certificate_based_authentication"></span><span id="certificate_based_authentication"></span><span id="CERTIFICATE_BASED_AUTHENTICATION"></span>**Проверка подлинности на основе сертификата** (2)


</dt> <dd>

Проверка подлинности на основе сертификата.

</dd> </dl> </dd> <dt>

*CertificateThumbPrint* \[ окне\]
</dt> <dd>

Отпечаток сертификата, используемый, если параметр *AuthenticationType* использует проверку подлинности на основе сертификата.

</dd> <dt>

*Бипасспроксисервер* \[ окне\]
</dt> <dd>

Обходить прокси-сервер при подключении к серверу реплики.

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
</dt> <dt>

**Файл не найден** (32779)
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

[**Мсвм \_ репликатионсервице**](msvm-replicationservice.md)
</dt> </dl>

 

