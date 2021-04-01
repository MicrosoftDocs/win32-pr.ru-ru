---
title: Атрибут управления учетной записью пользователя
description: Флаги, управляющие поведением учетной записи пользователя.
ms.assetid: fc81a16a-f537-44cc-957c-5d7ca66b9755
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута управления учетной записью пользователя
- Схема AD атрибута userAccountControl
topic_type:
- apiref
api_name:
- User-Account-Control
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f60297d22aad76b229c691a667ac22a87271402c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138742"
---
# <a name="user-account-control-attribute"></a>Атрибут управления учетной записью пользователя

Флаги, управляющие поведением учетной записи пользователя.



| Ввод | Значение |
|-------------------|---------------------------------------|
| CN                | Управление учетными записями пользователей                  |
| LDAP-отображаемое имя | userAccountControl                    |
| Размер              | 4 байта.                              |
| Привилегия обновления  | Это значение задается системой.      |
| Частота обновления  | При каждом изменении политики учетной записи. |
| Attribute-Id      | 1.2.840.113556.1.4.8                  |
| System-ID — GUID    | bf967a68-0de6-11d0-a285-00aa003049e2  |
| Синтаксис            | [**Перечисление**](s-enumeration.md)  |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-2000-server"></a>Windows 2000 Server



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Неверно                             |
| Является однозначным       | True                              |
| Индексируется             | True                              |
| В глобальном каталоге      | True                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Классы, используемые в        | [**Нажат**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Неверно                             |
| Является однозначным       | True                              |
| Индексируется             | True                              |
| В глобальном каталоге      | True                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Классы, используемые в        | [**Нажат**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Неверно                             |
| Является однозначным       | True                              |
| Индексируется             | True                              |
| В глобальном каталоге      | True                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Классы, используемые в        | [**Нажат**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Неверно                             |
| Является однозначным       | True                              |
| Индексируется             | True                              |
| В глобальном каталоге      | True                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Классы, используемые в        | [**Нажат**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Неверно                             |
| Является однозначным       | True                              |
| Индексируется             | True                              |
| В глобальном каталоге      | True                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Классы, используемые в        | [**Нажат**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Неверно                             |
| Является однозначным       | True                              |
| Индексируется             | True                              |
| В глобальном каталоге      | True                              |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000019                        |
| System-Flags           | 0x00000012                        |
| Классы, используемые в        | [**Нажат**](c-user.md)<br/> |



## <a name="remarks"></a>Комментарии

Значение этого атрибута может быть равно нулю или быть сочетанием одного или нескольких из следующих значений.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Шестнадцатеричное значение</th>
<th>Идентификатор (определяется в iAds. h)</th>
<th>Описание</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>0x00000001</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SCRIPT</strong></a></td>
<td>Выполняется сценарий входа.</td>
</tr>
<tr class="even">
<td>0x00000002</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ACCOUNTDISABLE</strong></a></td>
<td>Учетная запись пользователя отключена.</td>
</tr>
<tr class="odd">
<td>0x00000008</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_HOMEDIR_REQUIRED</strong></a></td>
<td>Требуется корневой каталог.</td>
</tr>
<tr class="even">
<td>0x00000010</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_LOCKOUT</strong></a></td>
<td>Учетная запись в данный момент заблокирована.</td>
</tr>
<tr class="odd">
<td>0x00000020</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_NOTREQD</strong></a></td>
<td>Пароль не требуется.</td>
</tr>
<tr class="even">
<td>0x00000040</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWD_CANT_CHANGE</strong></a></td>
<td>Пользователь не может изменить пароль.
<blockquote>
[!Note]<br />
Вы не можете назначить параметры разрешений PASSWD_CANT_CHANGE путем непосредственного изменения атрибута UserAccountControl. Дополнительные сведения и пример кода, демонстрирующий, как запретить пользователю изменять пароль, см. в разделе <a href="/windows/desktop/ADSI/user-cannot-change-password">пользователь не может изменить пароль</a>.
</blockquote>
<br/> :</td>
</tr>
<tr class="odd">
<td>0x00000080</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_ENCRYPTED_TEXT_PASSWORD_ALLOWED</strong></a></td>
<td>Пользователь может отправить зашифрованный пароль.</td>
</tr>
<tr class="even">
<td>0x00000100</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TEMP_DUPLICATE_ACCOUNT</strong></a></td>
<td>Это учетная запись для пользователей, Первичная учетная запись которых находится в другом домене. Эта учетная запись предоставляет пользователю доступ к этому домену, но не к домену, который доверяет данному домену. Также называется учетной записью локального пользователя.</td>
</tr>
<tr class="odd">
<td>0x00000200</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NORMAL_ACCOUNT</strong></a></td>
<td>Это тип учетной записи по умолчанию, представляющий обычного пользователя.</td>
</tr>
<tr class="even">
<td>0x00000800</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_INTERDOMAIN_TRUST_ACCOUNT</strong></a></td>
<td>Это позволяет доверять учетной записи для системного домена, который доверяет другим доменам.</td>
</tr>
<tr class="odd">
<td>0x00001000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_WORKSTATION_TRUST_ACCOUNT</strong></a></td>
<td>Это учетная запись компьютера для компьютера, который является членом этого домена.</td>
</tr>
<tr class="even">
<td>0x00002000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SERVER_TRUST_ACCOUNT</strong></a></td>
<td>Это учетная запись компьютера для системного контроллера домена резервного копирования, который является членом этого домена.</td>
</tr>
<tr class="odd">
<td>0x00004000</td>
<td>Н/Д</td>
<td>Не используется.</td>
</tr>
<tr class="even">
<td>0x00008000</td>
<td>Н/Д</td>
<td>Не используется.</td>
</tr>
<tr class="odd">
<td>0x00010000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_EXPIRE_PASSWD</strong></a></td>
<td>Срок действия пароля для этой учетной записи никогда не истечет.</td>
</tr>
<tr class="even">
<td>0x00020000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_MNS_LOGON_ACCOUNT</strong></a></td>
<td>Это учетная запись MNS.</td>
</tr>
<tr class="odd">
<td>0x00040000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_SMARTCARD_REQUIRED</strong></a></td>
<td>Пользователь должен войти в систему с помощью смарт-карты.</td>
</tr>
<tr class="even">
<td>0x00080000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_FOR_DELEGATION</strong></a></td>
<td>Учетная запись службы (учетная запись пользователя или компьютера), под которой выполняется служба, является доверенной для делегирования Kerberos. Любая такая служба может олицетворять клиента, запрашивающего службу.</td>
</tr>
<tr class="odd">
<td>0x00100000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_NOT_DELEGATED</strong></a></td>
<td>Контекст безопасности пользователя не будет делегирован службе, даже если учетная запись службы настроена как доверенная для делегирования Kerberos.</td>
</tr>
<tr class="even">
<td>0x00200000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_USE_DES_KEY_ONLY</strong></a></td>
<td>Ограничьте этот субъект для использования только типов шифрования DES для ключей.</td>
</tr>
<tr class="odd">
<td>0x00400000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_DONT_REQUIRE_PREAUTH</strong></a></td>
<td>Для входа в эту учетную запись не требуется предварительная проверка подлинности Kerberos.</td>
</tr>
<tr class="even">
<td>0x00800000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_PASSWORD_EXPIRED</strong></a></td>
<td>Срок действия пароля пользователя истек. Этот флаг создается системой с использованием данных из атрибута <a href="a-pwdlastset.md"><strong>PWD-Last-Set</strong></a> и политики домена.</td>
</tr>
<tr class="odd">
<td>0x01000000</td>
<td><a href="/windows/desktop/api/iads/ne-iads-ads_user_flag_enum"><strong>ADS_UF_TRUSTED_TO_AUTHENTICATE_FOR_DELEGATION</strong></a></td>
<td>Учетная запись включена для делегирования. Это чувствительный к безопасности параметр. учетные записи с включенным параметром должны быть строго контролируемыми. Этот параметр позволяет службе, работающей под учетной записью, предположить удостоверение клиента и проходить проверку подлинности от имени этого пользователя на других удаленных серверах в сети.</td>
</tr>
</tbody>
</table>



 

