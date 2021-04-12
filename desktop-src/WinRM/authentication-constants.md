---
title: Константы проверки подлинности (Всмандисп. h)
description: Укажите метод проверки подлинности и способ обработки серверов сертификатов для транспорта запросов по протоколу HTTPS.
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce45d1474cf6c925149c05ae348231333c3356e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535159"
---
# <a name="authentication-constants"></a>Константы проверки подлинности

Константы проверки подлинности — это константы в перечислении **\_ \_ всмансессионфлагс** , которые указывают метод проверки подлинности и способ обработки серверов сертификатов для транспорта запросов по протоколу HTTPS.

Одна или несколько констант, перечисленных в следующем списке, являются обязательными в параметре *flags* в вызовах [**WSMan. CreateSession**](wsman-createsession.md) или в вызовах [**ивсман:: CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) , подключающихся к удаленному компьютеру.

<dl> <dt>

<span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**всманфлагкредусернамепассворд**
</dt> <dd> <dl> <dt>

4096 (0x1000)
</dt> <dt>



Используйте имя пользователя и пароль в качестве учетных данных. Установите этот флаг при создании объекта [**ConnectionOptions**](connectionoptions.md) и укажите [**имя пользователя**](connectionoptions-username.md) и [**пароль**](connectionoptions-password.md). Учетные данные могут быть учетной записью домена или учетной записью на локальном компьютере. По умолчанию учетная запись должна быть членом локальной группы администраторов на локальном или удаленном компьютере. Однако службу WinRM можно настроить для предоставления другим пользователям. Дополнительные сведения см. в разделе [Установка и настройка для служба удаленного управления Windows](installation-and-configuration-for-windows-remote-management.md). Этот флаг можно установить при указании учетных данных для проверки подлинности согласования (также известной как [*Встроенная проверка подлинности Windows*](windows-remote-management-glossary.md)) или [*обычной проверки подлинности*](windows-remote-management-glossary.md).

Связанный метод создания скриптов — это [**WSMan. сессионфлагкредусернамепассворд**](wsman-sessionflagcredusernamepassword.md), а метод C++ — [**ивсманекс. сессионфлагкредусернамепассворд**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**всманфлагскипкачекк**
</dt> <dd> <dl> <dt>

8192 (0x2000)
</dt> <dt>



При подключении по протоколу HTTPS клиент не проверяет, подписан ли сертификат сервера доверенным центром сертификации (ЦС). Используйте это значение только в том случае, если удаленный компьютер является доверенным другим средством, например, если удаленный компьютер является частью сети, физически защищенной и изолированной, либо удаленный компьютер указан как доверенный узел в конфигурации WinRM.

Связанный метод создания скриптов — это [**WSMan. сессионфлагскипкачекк**](wsman-sessionflagskipcacheck.md), а метод C++ — [**ивсманекс. сессионфлагскипкачекк**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**всманфлагскипкнчекк**
</dt> <dd> <dl> <dt>

16384 (0x4000)
</dt> <dt>



При подключении по протоколу HTTPS клиент не будет проверять, соответствует ли общее имя (CN) в сертификате сервера имени компьютера в строке подключения. Используйте только в том случае, если удаленный компьютер является доверенным другим средством, например, если удаленный компьютер является частью сети, физически защищенной и изолированной, либо удаленный компьютер указан как доверенный узел в конфигурации WinRM.

Связанный метод создания скриптов — это [**WSMan. сессионфлагскипкнчекк**](wsman-sessionflagskipcncheck.md), а метод C++ — [**ивсманекс. сессионфлагскипкнчекк**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**всманфлагусеноаусентикатион**
</dt> <dd> <dl> <dt>

32768 (0x8000)
</dt> <dt>



Не использовать проверку подлинности. Укажите эту константу при проверке подключения к удаленному компьютеру, чтобы определить, настроен ли для службы, реализующей Протокол WS-Management, прослушивание запросов данных. **Всманфлагусеноаусентикатион** нельзя сочетать с другими константами [**сеанса**](session.md) . Связанный метод создания скриптов — это [**WSMan. сессионфлагусеноаусентикатион**](wsman-sessionflagusenoauthentication.md), а метод C++ — [**всманекс. сессионфлагусеноаусентикатион**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**всманфлагуседижест**
</dt> <dd> <dl> <dt>

65536 (0x10000)
</dt> <dt>



Использовать дайджест-проверку подлинности. Инициировать запрос дайджест-проверки подлинности может только клиентский компьютер. Клиент отправляет запрос на сервер для проверки подлинности и получения строки токена с сервера. Затем клиент отправляет запрос ресурса, включая имя пользователя и криптографический хэш пароля, в сочетании со строкой токена. Дайджест-проверка подлинности поддерживается для HTTP и HTTPS. Клиентские скрипты и приложения WinRM могут указывать дайджест-проверку подлинности, но не службу.

Связанный метод создания скриптов — это [**WSMan. сессионфлагуседижест**](wsman-sessionflagusedigest.md), а метод C++ — [**ивсманекс. сессионфлагуседижест**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**всманфлагусенеготиате**
</dt> <dd> <dl> <dt>

131072 (0x20000)
</dt> <dt>



Использовать проверку подлинности Negotiate. Клиент отправляет запрос на сервер для проверки подлинности. Сервер определяет, следует ли использовать Kerberos или NTLM. Выбран протокол Kerberos для проверки подлинности учетной записи домена, и для учетных записей локального компьютера выбран протокол NTLM. Имя пользователя должно быть указано в формате домен \\ имя_пользователя для пользователя домена или имени пользователя ServerName \\ для локального пользователя на компьютере сервера.

[Управление учетными записями пользователей (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) влияет на доступ к службе WinRM. Если в Рабочей группе или домене используется проверка подлинности Negotiate, доступ к службе может получить только встроенная учетная запись администратора. Чтобы разрешить всем учетным записям в группе "Администраторы" доступ к службе, присвойте следующему разделу реестра значение 1: **hKey \_ Local \_ Machine \\ Software \\ Microsoft \\ Windows \\ CurrentVersion \\ политики \\ System \\ LocalAccountTokenFilterPolicy**.

Связанный метод создания скриптов — это [**WSMan. сессионфлагусенеготиате**](wsman-sessionflagusenegotiate.md), а метод C++ — [**ивсманекс. сессионфлагусенеготиате**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**всманфлагусебасик**
</dt> <dd> <dl> <dt>

262144 (0x40000)
</dt> <dt>



Используйте обычную проверку подлинности. Клиент предоставляет учетные данные в виде имени пользователя и пароля, которые передаются непосредственно в сообщении запроса. Можно указать только учетные данные, которые определяют учетную запись локального администратора на удаленном компьютере.

Связанный метод создания скриптов — это [**WSMan. сессионфлагусебасик**](wsman-sessionflagusebasic.md), а метод C++ — [**ивсманекс. сессионфлагусебасик**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**всманфлагусекерберос**
</dt> <dd> <dl> <dt>

524288 (0x80000)
</dt> <dt>



Используйте проверку подлинности Kerberos. Клиент и сервер выполняют взаимную проверку подлинности с помощью билетов Kerberos.

Связанный метод создания скриптов — это [**WSMan. сессионфлагусекерберос**](wsman-sessionflagusekerberos.md), а метод C++ — [**ивсманекс. WSMan. сессионфлагусекерберос**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).


</dt> </dl> </dd> <dt>

<span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**всманфлагноенкриптион**
</dt> <dd> <dl> <dt>

1048576 (0x100000)
</dt> <dt>



Не использовать шифрование. По умолчанию незашифрованный трафик не разрешен и должен быть включен как на клиенте, так и на сервере.

Связанный метод создания скриптов — это [**WSMan. сессионфлагноенкриптион**](wsman-sessionflagnoencryption.md), а метод C++ — [**ивсманекс. сессионфлагноенкриптион**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**всманфлагусеклиентцертификате**
</dt> <dd> <dl> <dt>

2097152 (0x200000)
</dt> <dt>



Использовать проверку подлинности на основе сертификата клиента.

Связанный метод создания скриптов — это [**WSMan. сессионфлагусеклиентцертификате**](wsman-sessionflaguseclientcert.md), а метод C++ — [**IWSManEx2. сессионфлагусеклиентцертификате**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**всманфлагусекредссп**
</dt> <dd> <dl> <dt>

16777216 (0x1000000)
</dt> <dt>



Используйте проверку подлинности с помощью поставщика поддержки безопасности учетных данных (CredSSP).

Связанный метод создания скриптов — это [**WSMan. сессионфлагусекредссп**](wsman-sessionflagusecredssp.md), а метод C++ — [**IWSManEx3. сессионфлагусекредссп**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).


</dt> </dl> </dd> <dt>

<span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**всманфлагскипревокатиончекк**
</dt> <dd> <dl> <dt>

0x2000000
</dt> <dt>



Не проверять отзыв сертификата во время проверки подлинности.


</dt> </dl> </dd> <dt>

<span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**всманфлагалловнеготиатеимплиЦиткредентиалс**
</dt> <dd> <dl> <dt>

0x4000000
</dt> <dt>



Разрешить неявные учетные данные.


</dt> </dl> </dd> <dt>

<span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**всманфлагусессл**
</dt> <dd> <dl> <dt>

0x8000000
</dt> <dt>



Используйте защищенный уровень сокетов, включает протокол HTTPS.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows Vista<br/>                                                                 |
| Минимальная версия сервера<br/> | Windows Server 2008<br/>                                                           |
| Header<br/>                   | <dl> <dt>Всмандисп. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Всмандисп. idl</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Константы сеанса](session-constants.md)
</dt> </dl>

 

 





