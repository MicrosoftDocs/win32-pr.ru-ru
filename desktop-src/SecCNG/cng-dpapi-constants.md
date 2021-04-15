---
description: API-интерфейс защиты данных CNG использует следующие константы.
ms.assetid: 4E43FAA9-7D6F-43DB-A998-189411E0AB4C
title: Константы DPAPI CNG (Нкриптпротект. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ece376a0b7282f26ef933b249a1356b2d012d438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496971"
---
# <a name="cng-dpapi-constants"></a>Константы DPAPI CNG

API-интерфейс защиты данных CNG использует следующие константы.

<dl> <dt>

<span id="NCRYPT_DESCR_DELIMITER_AND"></span><span id="ncrypt_descr_delimiter_and"></span>**NCRYPT \_ Descr \_ разделитель \_ и**
</dt> <dd> <dl> <dt>

L "И"
</dt> <dt>



Может использоваться для проверки строки дескриптора защиты для разделителя и.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_EQUAL"></span><span id="ncrypt_descr_equal"></span>**NCRYPT \_ Descr \_ EQUAL**
</dt> <dd> <dl> <dt>

L "="
</dt> <dt>



Может использоваться для проверки строки дескриптора защиты для знака равенства.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_DESCR_DELIMITER_OR"></span><span id="ncrypt_descr_delimiter_or"></span>**NCRYPT \_ Descr \_ разделитель \_ или**
</dt> <dd> <dl> <dt>

L "ИЛИ"
</dt> <dt>



Может использоваться для проверки строки дескриптора защиты для разделителя или.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_LOCAL"></span><span id="ncrypt_key_protection_algorithm_local"></span>**\_ \_ \_ локальный алгоритм защиты ключей \_ NCRYPT**
</dt> <dd> <dl> <dt>

"LOCAL"
</dt> <dt>



ЛОКАЛЬНЫЙ дескриптор защиты защищает содержимое для сеанса входа в систему, текущего пользователя или локального компьютера, как определено следующими константами:

-   **\_ \_ \_ локальный \_ Вход в систему защиты ключей NCRYPT**
-   **\_ \_ \_ локальный \_ Пользователь защиты ключей NCRYPT**
-   **\_ \_ \_ локальный \_ компьютер защиты ключей NCRYPT**


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SDDL"></span><span id="ncrypt_key_protection_algorithm_sddl"></span>**\_ \_ алгоритм защиты ключей \_ NCRYPT \_ SDDL**
</dt> <dd> <dl> <dt>

АВТОРИЗАЦИИ
</dt> <dt>



Защищает содержимое до строки SDDL (языка определения дескрипторов безопасности), содержащей сведения о дескрипторе безопасности.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_SID"></span><span id="ncrypt_key_protection_algorithm_sid"></span>**\_ \_ \_ ИД безопасности алгоритма защиты ключей NCRYPT \_**
</dt> <dd> <dl> <dt>

ТРАНСЛЯЦИЮ
</dt> <dt>



Дескриптор защиты SID содержит удостоверение группы или участника.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_ALGORITHM_WEBCREDENTIALS"></span><span id="ncrypt_key_protection_algorithm_webcredentials"></span>**\_ \_ \_ учетные данные для алгоритма защиты ключей NCRYPT \_**
</dt> <dd> <dl> <dt>

"УЧЕТные данные"
</dt> <dt>



Обеспечивает защиту учетных данных веб-учетной записи пользователя.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_LOGON"></span><span id="ncrypt_key_protection_local_logon"></span>**\_ \_ \_ локальный \_ Вход в систему защиты ключей NCRYPT**
</dt> <dd> <dl> <dt>

входа
</dt> <dt>



Защищает содержимое в текущем сеансе входа. Пользователи не смогут расшифровывать защищенное содержимое после выхода из системы или перезагрузки.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_MACHINE"></span><span id="ncrypt_key_protection_local_machine"></span>**\_ \_ \_ локальный \_ компьютер защиты ключей NCRYPT**
</dt> <dd> <dl> <dt>

машине
</dt> <dt>



Защищает содержимое на локальном компьютере. Все пользователи на локальном компьютере могут расшифровывать защищенное содержимое.


</dt> </dl> </dd> <dt>

<span id="NCRYPT_KEY_PROTECTION_LOCAL_USER"></span><span id="ncrypt_key_protection_local_user"></span>**\_ \_ \_ локальный \_ Пользователь защиты ключей NCRYPT**
</dt> <dd> <dl> <dt>

нажат
</dt> <dt>



Защищает содержимое в текущем сеансе пользователя. Только этот пользователь на локальном компьютере сможет расшифровать защищенное содержимое.


</dt> </dl> </dd> <dt>

<span id="MS_KEY_PROTECTION_PROVIDER"></span><span id="ms_key_protection_provider"></span>**\_ \_ поставщик защиты ключей \_ MS**
</dt> <dd> <dl> <dt>

"Поставщик защиты ключей (Майкрософт)"
</dt> <dt>



Представляет поставщик защиты ключей (Майкрософт), который поддерживает форматы, представленные следующими константами:

-   **\_ \_ \_ ИД безопасности алгоритма защиты ключей NCRYPT \_**
-   **\_ \_ \_ локальный алгоритм защиты ключей \_ NCRYPT**
-   **\_ \_ алгоритм защиты ключей \_ NCRYPT \_ SDDL**


</dt> </dl> </dd> <dt>

<span id="WINDOWS_CLIENT_KEY_PROTECTION_PROVIDER"></span><span id="windows_client_key_protection_provider"></span>**\_ \_ \_ поставщик защиты ключа клиента \_ Windows**
</dt> <dd> <dl> <dt>

"Поставщик защиты ключа клиента Windows"
</dt> <dt>



Представляет поставщик защиты ключей (Майкрософт), доступный только на клиенте и поддерживающий форматы, представленные следующими константами:

-   **\_ \_ \_ учетные данные для алгоритма защиты ключей NCRYPT \_**


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                                 |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                       |
| Header<br/>                   | <dl> <dt>Нкриптпротект. h</dt> </dl> |



 

 




