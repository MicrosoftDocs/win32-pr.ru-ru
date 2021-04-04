---
description: Присоединение компьютерной системы к домену или рабочей группе.
ms.assetid: b9421f04-9b56-4413-af5c-12dffeb6f0c8
ms.tgt_platform: multiple
title: Метод Жоиндомаинорворкграуп класса Win32_ComputerSystem
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_ComputerSystem.JoinDomainOrWorkgroup
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 927dd6b2664c92ff07e94407fdc59fdd917363dd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103896294"
---
# <a name="joindomainorworkgroup-method-of-the-win32_computersystem-class"></a>Метод Жоиндомаинорворкграуп \_ класса ComputerSystem Win32

Метод **жоиндомаинорворкграуп** присоединяет компьютер к домену или рабочей группе.

В этом разделе используется синтаксис MOF-файл (MOF). Дополнительные сведения об использовании этого метода см. [в разделе вызов метода](/windows/desktop/WmiSdk/calling-a-method).

## <a name="syntax"></a>Синтаксис


```mof
uint32 JoinDomainOrWorkgroup(
  [in] string Name,
  [in] string Password,
  [in] string UserName,
  [in] string AccountOU,
  [in] uint32 FJoinOptions = 
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Имя* \[ окне\]
</dt> <dd>

Указывает домен или рабочую группу для приподключения. Не может иметь **значение NULL**.

</dd> <dt>

*Пароль* \[ окне\]
</dt> <dd>

Если параметр *username* указывает имя учетной записи, параметр *Password* должен указывать на пароль, используемый при подключении к контроллеру домена. В противном случае этот параметр должен иметь **значение NULL**.

</dd> <dt>

*Имя пользователя* \[ окне\]
</dt> <dd>

Указатель на постоянную строку символов, завершающуюся **нулем**, которая указывает имя учетной записи, используемой при подключении к контроллеру домена. Необходимо указать NetBIOS-имя домена и учетную запись пользователя, например " \\ пользователь домена". Если этот параметр имеет **значение NULL**, используются сведения о вызывающем объекте.

Также можно использовать имя участника-пользователя (увеличила) в форме user@domain .

</dd> <dt>

*Аккаунтау* \[ окне\]
</dt> <dd>

Задает указатель на постоянную строку символов, завершающуюся **нулем**, которая содержит имя формата [RFC 1779](https://www.ietf.org/rfc/rfc1779.txt) для учетной записи компьютера. Если указать этот параметр, строка должна содержать полный путь, в противном случае *диакритические знаки* должны быть **равны NULL**.

Пример: "OU = Тестау; DC = домен; DC = домен; DC = com "

</dd> <dt>

*Фжоиноптионс* \[ окне\]
</dt> <dd>

Набор битовых флагов, определяющих параметры объединения.

<dt>



  (0)


</dt> <dd>

По умолчанию. Нет параметров объединения.

</dd> <dt>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>

<span id="NETSETUP_JOIN_DOMAIN"></span><span id="netsetup_join_domain"></span>**Нетсетуп \_ Присоединение к \_ домену** (0x00000001)


</dt> <dd>

Присоединяет компьютер к домену. Если это значение не указано, присоединяет компьютер к Рабочей группе.

</dd> <dt>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>

<span id="NETSETUP_ACCT_CREATE"></span><span id="netsetup_acct_create"></span>**Нетсетуп \_ \_Создание acct** (0x00000002)


</dt> <dd>

Создает учетную запись в домене.

</dd> <dt>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>

<span id="NETSETUP_WIN9X_UPGRADE"></span><span id="netsetup_win9x_upgrade"></span>**Нетсетуп \_ \_Обновление Win9x** (0x00000010)


</dt> <dd>

Операция Join выполняется в процессе обновления.

</dd> <dt>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>

<span id="NETSETUP_DOMAIN_JOIN_IF_JOINED"></span><span id="netsetup_domain_join_if_joined"></span>**Нетсетуп \_ Присоединение к ДОМЕНу \_ \_ при \_ присоединении** (0x00000020)


</dt> <dd>

Позволяет присоединиться к новому домену, даже если компьютер уже присоединен к домену.

</dd> <dt>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>

<span id="NETSETUP_JOIN_UNSECURE"></span><span id="netsetup_join_unsecure"></span>**Нетсетуп \_ \_НЕбезопасный присоединение** (0x00000040)


</dt> <dd>

Выполняет незащищенное присоединение.

Этот параметр запрашивает присоединение домена к предварительно созданной учетной записи без проверки подлинности с учетными данными пользователя домена. Этот параметр можно использовать в сочетании с параметром **нетсетуп \_ Machine \_ PWD \_ Passed** . В этом случае *Password* — это пароль предварительно созданной учетной записи компьютера.

До выхода Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008 небезопасное соединение не проходило проверку подлинности на контроллере домена. Все взаимодействие было выполнено с использованием сеанса со значением NULL (без проверки подлинности). Начиная с Windows Vista с пакетом обновления 1 (SP1) и Windows Server 2008, имя учетной записи компьютера и пароль используются для проверки подлинности на контроллере домена.

</dd> <dt>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>

<span id="NETSETUP_MACHINE_PWD_PASSED"></span><span id="netsetup_machine_pwd_passed"></span>**Нетсетуп \_ Пароль компьютера (0x00000080) \_ \_ успешно пройден**


</dt> <dd>

Указывает, что параметр *Password* задает пароль учетной записи локального компьютера, а не пароль пользователя. Этот флаг допустим только для незащищенных соединений, которые необходимо указать, установив \_ \_ флаг небезопасного нетсетуп JOIN.

Если установить этот флаг, то после выполнения операции присоединение пароль компьютера будет установлен в значение *Password*, если это значение является допустимым паролем компьютера.

</dd> <dt>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>

<span id="NETSETUP_DEFER_SPN_SET"></span><span id="netsetup_defer_spn_set"></span>**Нетсетуп \_ Задержать \_ \_ набор SPN** (0x00000100)


</dt> <dd>

Указывает, что имя участника-службы (SPN) и свойства DnsHostName на объекте-компьютере не должны обновляться в данный момент.

Как правило, эти свойства обновляются во время операции JOIN. Вместо этого эти свойства следует обновлять во время последующего вызова метода [**Rename**](rename-method-in-class-win32-computersystem.md) . Эти свойства всегда обновляются во время операции переименования.

</dd> <dt>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>

<span id="NETSETUP_JOIN_DC_ACCOUNT"></span><span id="netsetup_join_dc_account"></span>**Нетсетуп \_ Присоединение \_ \_ учетной записи контроллера домена** (0x00000200)


</dt> <dd>

Разрешить присоединение к домену, если существующая учетная запись является контроллером домена.

> [!Note]  
> Этот флаг поддерживается в Windows Vista и более поздних версиях.

 

</dd> <dt>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>

<span id="NETSETUP_AMBIGUOUS_DC"></span><span id="netsetup_ambiguous_dc"></span>**Нетсетуп \_ НЕОДНОЗНАЧНЫй \_ контроллер домена** (0x00001000)


</dt> <dd>

При присоединении к домену не пытайтесь задать в реестре предпочитаемый контроллер домена.

> [!Note]  
> Этот флаг поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.

 

</dd> <dt>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>

<span id="NETSETUP_NO_NETLOGON_CACHE"></span><span id="netsetup_no_netlogon_cache"></span>**Нетсетуп \_ НЕТ \_ \_ кэша Netlogon** (0x00002000)


</dt> <dd>

При присоединении к домену кэш Netlogon не создается.

> [!Note]  
> Этот флаг поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.

 

</dd> <dt>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>

<span id="NETSETUP_DONT_CONTROL_SERVICES"></span><span id="netsetup_dont_control_services"></span>**Нетсетуп \_ \_ \_ Службы управления не** (0x00004000)


</dt> <dd>

При присоединении к домену Служба Netlogon не будет принудительно запущена.

> [!Note]  
> Этот флаг поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.

 

</dd> <dt>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>

<span id="NETSETUP_SET_MACHINE_NAME"></span><span id="netsetup_set_machine_name"></span>**Нетсетуп \_ ЗАДАТЬ \_ \_ имя компьютера** (0x00008000)


</dt> <dd>

При присоединении к домену только для автономного соединения задайте имя узла и NetBIOS целевого компьютера.

> [!Note]  
> Этот флаг поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.

 

</dd> <dt>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>

<span id="NETSETUP_FORCE_SPN_SET"></span><span id="netsetup_force_spn_set"></span>**Нетсетуп \_ FORCE \_ \_ Set SPN** (0x00010000)


</dt> <dd>

При присоединении к домену переопределите другие параметры во время присоединения к домену и задайте имя участника-службы (SPN).

> [!Note]  
> Этот флаг поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.

 

</dd> <dt>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>

<span id="NETSETUP_NO_ACCT_REUSE"></span><span id="netsetup_no_acct_reuse"></span>**Нетсетуп \_ БЕЗ \_ \_ повторного использования** (0x00020000)


</dt> <dd>

При присоединении к домену не следует повторно использовать имеющуюся учетную запись.

> [!Note]  
> Этот флаг поддерживается в Windows 7, Windows Server 2008 R2 и более поздних версиях.

 

</dd> <dt>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>

<span id="NETSETUP_IGNORE_UNSUPPORTED_FLAGS"></span><span id="netsetup_ignore_unsupported_flags"></span>**Нетсетуп \_ ИГНОРИРОВАТЬ \_ неподдерживаемые \_ Флаги** (0x10000000)


</dt> <dd>

Если этот бит задан, нераспознанные флаги будут игнорироваться функцией **жоиндомаинорворкграуп** , и [**нетжоиндомаин**](/windows/desktop/api/lmjoin/nf-lmjoin-netjoindomain) будет вести себя так, как если бы не были заданы флаги.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Возвращает [код системной ошибки](/windows/desktop/Debug/system-error-codes), который может включать одно из следующих числовых значений. Любое другое значение указывает на ошибку. Дополнительные коды ошибок см. в разделе [**константы WMI Error**](/windows/desktop/WmiSdk/wmi-error-constants) или [**вбемерроренум**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).

<dl> <dt>

**Успешно**
</dt> <dd>

0

</dd> <dt>

**5**
</dt> <dd>

Отказано в доступе".

</dd> <dt>

**87**
</dt> <dd>

Неправильный параметр".

</dd> <dt>

**110**
</dt> <dd>

система не может открыть указанный объект.

</dd> <dt>

**1323**
</dt> <dd>

Не удалось обновить пароль.

</dd> <dt>

**1326**
</dt> <dd>

Ошибка входа: неизвестное имя пользователя или неправильный пароль.

</dd> <dt>

**1355**
</dt> <dd>

Указанный домен не существует, или к нему не удалось подключиться.

</dd> <dt>

**2224**
</dt> <dd>

Учетная запись уже существует.

</dd> <dt>

**2691**
</dt> <dd>

Компьютер уже присоединен к домену.

</dd> <dt>

**2692**
</dt> <dd>

Компьютер в настоящее время не присоединен к домену.

</dd> <dt>

**\_ \_ требуется зашифрованное \_ Подключение WBEM E \_**
</dt> <dd>

0x80041087

Указаны *пароль* и *имя пользователя* , но уровень проверки подлинности не является **\_ \_ AUTHN \_ уровнем \_ \_ безопасности RPC C уровня "PKT**". Для Visual Basic возвращается **вбемерренкриптедконнектионрекуиред** .

</dd> <dt>

**Другое**
</dt> <dd>

1 4294967295

</dd> </dl>

## <a name="remarks"></a>Комментарии

При перемещении компьютера из домена в рабочую группу необходимо удалить компьютер из домена (с помощью вызова [**унжоиндомаинорворкграуп**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)) перед вызовом этого метода для приподключения к Рабочей группе (с вызовом **жоиндомаинорворкграуп**). После вызова этого метода перезагрузите затронутый компьютер, чтобы применить изменения.

*Имя пользователя* и *пароль* можно оставить **пустыми**. Однако проверка подлинности соединения с WMI должна быть равна 6 в скрипте или **вбемаусентикатионлевелпктприваци** в Visual Basic и других языках, которые могут использовать библиотеку [wbemdisp.dll](/windows/desktop/WmiSdk/using-the-wmi-scripting-type-library) . Дополнительные сведения см. [в разделе Задание уровня безопасности процесса по умолчанию с помощью VBScript](/windows/desktop/WmiSdk/setting-the-default-process-security-level-using-vbscript).

В C++ для подключения к прокси-серверу [**IWbemServices**](/windows/desktop/api/wbemcli/nn-wbemcli-iwbemservices) [**на**](/windows/win32/api/combaseapi/nf-combaseapi-coinitializesecurity) **уровне RPC \_ C \_ AUTHN \_ уровня \_ \_** "для всех процессов или в методе [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket)можно задать конфиденциальность. Дополнительные сведения см. в статьях [Настройка проверки подлинности с помощью C++](/windows/desktop/WmiSdk/setting-authentication-using-c-) и [Настройка параметров безопасности для IWbemServices и других прокси-серверов](/windows/desktop/WmiSdk/setting-the-security-on-iwbemservices-and-other-proxies).

## <a name="examples"></a>Примеры

В примере [Присоединение компьютера к домену](https://Gallery.TechNet.Microsoft.Com/Join-a-computer-to-a-domain-6e19d905) PowerShell присоединяет компьютер к домену.

Следующий пример кода VBScript присоединяет компьютер к домену и создает учетную запись компьютера в Active Directory.


```VB
Const JOIN_DOMAIN             = 1
Const ACCT_CREATE             = 2
Const ACCT_DELETE             = 4
Const WIN9X_UPGRADE           = 16
Const DOMAIN_JOIN_IF_JOINED   = 32
Const JOIN_UNSECURE           = 64
Const MACHINE_PASSWORD_PASSED = 128
Const DEFERRED_SPN_SET        = 256
Const INSTALL_INVOCATION      = 262144
strDomain   = "FABRIKAM"
strPassword = "ls4k5ywA"
strUser     = "shenalan"
Set objNetwork = CreateObject("WScript.Network")
strComputer = objNetwork.ComputerName
Set objComputer = GetObject("winmgmts:{impersonationLevel=Impersonate}!\\" & strComputer & _
                            "\root\cimv2:Win32_ComputerSystem.Name='" & strComputer & "'")
ReturnValue = objComputer.JoinDomainOrWorkGroup(strDomain, _
                                                strPassword, _
                                                strDomain & "\" & strUser, _
                                                NULL, _
                                                JOIN_DOMAIN + ACCT_CREATE)
```



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

[**Win32 \_ ComputerSystem**](win32-computersystem.md)
</dt> <dt>

[**Метод Унжоиндомаинорворкграуп**](unjoindomainorworkgroup-method-in-class-win32-computersystem.md)
</dt> </dl>

 

