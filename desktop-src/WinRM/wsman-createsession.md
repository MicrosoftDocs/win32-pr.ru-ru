---
title: Метод WSMan. CreateSession (Всмандисп. h)
description: Создает объект сеанса, который затем может использоваться для последующих сетевых операций.
ms.assetid: 299d9a95-bd30-414c-996d-6633e8b7ce52
ms.tgt_platform: multiple
keywords:
- служба удаленного управления Windows метода CreateSession
- Служба удаленного управления Windows метода CreateSession, объект WSMan
- Объект WSMan служба удаленного управления Windows, метод CreateSession
topic_type:
- apiref
api_name:
- WSMan.CreateSession
api_location:
- WSMAuto.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 966fd1f43db7114d3a4c0cf4cddaa4428fcb41c6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534529"
---
# <a name="wsmancreatesession-method"></a>Метод WSMan. CreateSession

Создает объект [**сеанса**](session.md) , который затем может использоваться для последующих сетевых операций.

## <a name="syntax"></a>Синтаксис


```VB
WSMan.CreateSession( _
  [ ByVal connection ], _
  [ ByVal flags ], _
  [ ByVal connectionOptions ] _
)
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Подключение к* \[ в необязательное\]
</dt> <dd>

Протокол и служба для подключения, включая IPv4 или IPv6. Формат сведений о соединении выглядит следующим образом: < ><  >< *суффикса* адреса транспорта>. Примеры см. в разделе Примечания. Если сведения о соединении не указаны, используется локальный компьютер.

</dd> <dt>

*Флаги* \[ в необязательное\]
</dt> <dd>

Флаги сеанса, указывающие метод проверки подлинности, например [*Negotiate*](windows-remote-management-glossary.md) или [*дайджест-аутентификация*](windows-remote-management-glossary.md), для подключения к удаленному компьютеру. Эти флаги также указывают другие сведения о подключении сеанса, такие как кодирование или шифрование. Этот параметр должен содержать один или несколько флагов в **\_ \_ всмансессионфлагс** для удаленного подключения. Дополнительные сведения см. в разделе [константы сеанса](session-constants.md). Для подключения к WinRM на локальном компьютере параметры флага не требуются. Значение по умолчанию — **всманфлагусенеготиате**.

Дополнительные сведения см. в разделе [Проверка подлинности удаленных подключений](authentication-for-remote-connections.md) и параметр *connectionOptions* .

</dd> <dt>

*connectionOptions* \[ в необязательное\]
</dt> <dd>

Указатель на объект [**ConnectionOptions**](connectionoptions.md) , содержащий имя пользователя и пароль. Значение по умолчанию — **null**.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Объект [**сеанса**](session.md) , который затем можно использовать для выполнения локальных или удаленных операций WinRM.

## <a name="remarks"></a>Комментарии

Метод **CreateSession** Инициализирует объект [**Session**](session.md) , собирая параметры, такие как флаги, учетные данные и строку подключения для параметра *соединения* . **CreateSession** на самом деле не подключается к локальному или удаленному компьютеру. Если соединение не может быть установлено, происходит сбой при выполнении первой операции **сеанса** , такой как [**Get**](session-get.md) или [**reenumerate**](session-enumerate.md), после вызова **CreateSession**. Это поведение отличается от [*WMI*](windows-remote-management-glossary.md) -соединения с [*пространством имен*](windows-remote-management-glossary.md) на удаленном компьютере. Дополнительные сведения см. в разделе [Служба удаленного управления Windows и инструментарий WMI](windows-remote-management-and-wmi.md).

Для вызова этого метода используется следующий пример кода VBScript.


```VB
Set session = _
    wsman.CreateSession("<Transport><Address><Suffix>")
```



В следующих примерах показаны различные форматы, используемые для указания сведений о соединении в параметре *подключения* (при создании сеанса HTTPS поле <*адрес*> должно совпадать с именем сертификата компьютера сервера, в противном случае произойдет сбой):

-   "https://service"

    Использует протокол HTTPS для подключения к расположению веб-службы по умолчанию.

-   "https://service.corp.com/websvcs/wsman"

    Использует протокол HTTPS для подключения к определенному расположению веб-службы.

-   "https:// \[ E3D7:0000:0000:0000:51F4:9BC8: c0a8:6420 \] "

    Использует HTTPS и IPv6 с портом по умолчанию.

-   "https:// \[ E3D7:0000:0000:0000:51F4:9BC8: c0a8:6420 \] : 9999/WSMAN"

    Использует HTTPS и IPv6 с заданным портом.

## <a name="examples"></a>Примеры

Следующий пример кода VBScript создает сеанс на локальном компьютере.


```VB
 Set NewSession = Wsman.CreateSession   
   
```



В следующем примере кода VBScript создается сеанс на удаленном компьютере, который идентифицируется по IP-адресу. Сценарий предоставляет имя пользователя и пароль для учетной записи. Флаги **всманфлагкредусернамепассворд** и **всманфлагусебасик** объединяются, чтобы указать, что учетная запись является локальной учетной записью на удаленном компьютере. В случае сбоя создания сеанса сценарий завершается. Скрипт использует методы, возвращающие константу, например [**WSMan. сессионфлагусебасик**](wsman-sessionflagusebasic.md).

Чтобы выполнить этот сценарий, необходимо настроить параметры конфигурации по умолчанию как для клиента, так и для сервера, чтобы разрешить незашифрованный трафик и обычную проверку подлинности (для **алловуненкриптед** задано значение **true** , а для параметра Basic — значение **true**). Дополнительные сведения см. в разделе [Установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md).


```VB
iFlags = WSMan.SessionFlagUseBasic Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



В следующем примере кода VBScript учетная запись является учетной записью домена и используется проверка подлинности Negotiate. При использовании проверки подлинности Negotiate необходимо указать имя пользователя как `computername\username` или `ipaddress\username` .


```VB
iFlags = WSMan.SessionFlagUseNegotiate Or WSMan.SessionFlagCredUsernamePassword
Set Options = Wsman.CreateConnectionOptions
Options.Username = "MyComputer\MyUserName"
Options.Password = "MyPassword"
Set NewSession = WSMan.CreateSession("127.0.51.1", iFlags, _
    Options) 
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |
| Библиотека<br/>                  | <dl> <dt>Всмандисп. tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>WSMAuto.dll</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Ведущий**](wsman.md)
</dt> <dt>

[**ConnectionOptions**](connectionoptions.md)
</dt> <dt>

[**Session**](session.md)
</dt> <dt>

[Проверка подлинности для удаленных подключений](authentication-for-remote-connections.md)
</dt> <dt>

[Установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md)
</dt> </dl>

 

 





