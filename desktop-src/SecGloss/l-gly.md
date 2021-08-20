---
description: Содержит определения терминов безопасности, начинающихся с буквы L.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 65dd9a04-fc7c-4179-95ff-dac7dad4668f
title: L (глоссарий по безопасности)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d99ec1b1b5a9328d8bf4cc789dababb7161a9230810a558e54648e7b8ea2da9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970161"
---
# <a name="l-security-glossary"></a>L (глоссарий по безопасности)

[A](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) F [G](g-gly.md) [р](h-gly.md) [.](i-gly.md) J [K](k-gly.md) L [M](m-gly.md) [N](n-gly.md) [O](o-gly.md) [P](p-gly.md) Q [R](r-gly.md) [S](s-gly.md) [T](t-gly.md) [U](u-gly.md) [V](v-gly.md) [W](w-gly.md) [X](x-gly.md) Y Z

<dl> <dt>

<span id="_security_ldap_gly"></span><span id="_SECURITY_LDAP_GLY"></span>**LDAP**
</dt> <dd>

См. раздел *протокол упрощенного доступа к каталогу*

</dd> <dt>

<span id="_security_lightweight_directory_access_protocol_gly"></span><span id="_SECURITY_LIGHTWEIGHT_DIRECTORY_ACCESS_PROTOCOL_GLY"></span>**Упрощенный протокол доступа к каталогу**
</dt> <dd>

Более легко реализовано подмножество стандарта X. 500 для служб каталогов.

</dd> <dt>

<span id="_security_little_endian_gly"></span><span id="_SECURITY_LITTLE_ENDIAN_GLY"></span>**с прямым порядком байтов**
</dt> <dd>

Формат памяти или данных, в котором наименьший значащий байт хранится по нижнему адресу или прибывается первым.

См. также [*обратный порядок байтов*](b-gly.md).

</dd> <dt>

<span id="_security_locally_unique_identifier_gly"></span><span id="_SECURITY_LOCALLY_UNIQUE_IDENTIFIER_GLY"></span>**локально уникальный идентификатор**
</dt> <dd>

LUID 64-разрядное значение, которое гарантированно уникально в операционной системе, создавшей ее до перезапуска системы.

</dd> <dt>

<span id="_security_local_registration_authority_gly"></span><span id="_SECURITY_LOCAL_REGISTRATION_AUTHORITY_GLY"></span>**локальный центр регистрации**
</dt> <dd>

(ЛРА) Посредник между издателем и [*центром сертификации*](c-gly.md) (ЦС). ЛРА может, например, проверить учетные данные издателя перед их отправкой в ЦС.

</dd> <dt>

<span id="_security_local_security_authority_gly"></span><span id="_SECURITY_LOCAL_SECURITY_AUTHORITY_GLY"></span>**Локальный центр безопасности**
</dt> <dd>

СЛУЖБУ Защищенная подсистема, которая выполняет проверку подлинности и регистрирует пользователей в локальной системе. LSA также хранит сведения обо всех аспектах локальной безопасности системы, называемых локальной политикой безопасности системы.

</dd> <dt>

<span id="_security_logical_store_gly"></span><span id="_SECURITY_LOGICAL_STORE_GLY"></span>**Логическое хранилище**
</dt> <dd>

См. раздел [*виртуальное хранилище*](v-gly.md).

</dd> <dt>

<span id="_security_logon_data_gly"></span><span id="_SECURITY_LOGON_DATA_GLY"></span>**данные входа**
</dt> <dd>

Сведения, представленные в системе [*субъектом безопасности*](s-gly.md) для проверки подлинности.

</dd> <dt>

<span id="_security_logon_identifier_gly"></span><span id="_SECURITY_LOGON_IDENTIFIER_GLY"></span>**Идентификатор входа**
</dt> <dd>

LUID, определяющий *сеанс входа в систему*. Идентификатор входа действителен до тех пор, пока пользователь не выйдет из системы. Идентификатор входа уникален во время работы компьютера; ни один другой сеанс входа не будет иметь такой же идентификатор входа. Однако набор возможных идентификаторов входа сбрасывается при запуске компьютера. Чтобы получить идентификатор входа из [*маркера доступа*](a-gly.md), вызовите функцию **GetTokenInformation** для токенстатистикс; Идентификатор входа находится в элементе **аусентикатионид** .

</dd> <dt>

<span id="_security_logon_session_gly"></span><span id="_SECURITY_LOGON_SESSION_GLY"></span>**сеанс входа**
</dt> <dd>

Сеанс входа в систему начинается каждый раз, когда пользователь входит в систему на компьютере. Все процессы в сеансе входа имеют одинаковый первичный [*маркер доступа*](a-gly.md). Маркер доступа содержит сведения о контексте безопасности сеанса входа в систему, включая SID пользователя, *идентификатор входа* и идентификатор *безопасности входа*.

</dd> <dt>

<span id="_security_logon_sid_gly"></span><span id="_SECURITY_LOGON_SID_GLY"></span>**Идентификатор безопасности входа**
</dt> <dd>

[*Идентификатор безопасности*](s-gly.md) (SID), определяющий *сеанс входа в систему*. Идентификатор безопасности входа можно использовать в [*списке DACL*](d-gly.md) для управления доступом во время сеанса входа в систему. Идентификатор безопасности входа действителен до тех пор, пока пользователь не выйдет из системы. Идентификатор безопасности входа уникален во время работы компьютера; ни один другой сеанс входа не будет иметь тот же идентификатор безопасности входа. Однако при запуске компьютера будет сброшен набор возможных идентификаторов SID для входа. Чтобы получить идентификатор SID для входа из [*маркера доступа*](a-gly.md), вызовите функцию **GetTokenInformation** для токенграупс.

</dd> <dt>

<span id="_security_low_level_message_functions_gly"></span><span id="_SECURITY_LOW_LEVEL_MESSAGE_FUNCTIONS_GLY"></span>**низкоуровневые функции сообщений**
</dt> <dd>

Функции управления сообщениями, которые работают на более высоком уровне, чем базовые криптографические функции. Эти функции предоставляют функциональные возможности для кодирования данных для передачи и декодирования полученных данных. Низкоуровневые функции сообщений обеспечивают большую гибкость, чем упрощенные функции сообщений, но требует больше вызовов функций.

См. также [*упрощенные функции сообщений*](s-gly.md).

</dd> <dt>

<span id="_security_lsa_gly"></span><span id="_SECURITY_LSA_GLY"></span>**СЛУЖБУ**
</dt> <dd>

См. раздел *локальный центр безопасности*.

</dd> <dt>

<span id="_security_luid_gly"></span><span id="_SECURITY_LUID_GLY"></span>**LUID**
</dt> <dd>

См. *локальный уникальный идентификатор*.

</dd> </dl>

 

 



