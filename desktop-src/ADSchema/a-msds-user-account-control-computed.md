---
title: MS-DS-User-Account-Control-вычисленный атрибут
description: msDS-User-Account-Control — вычисление выполняется примерно так же, как userAccountControl, но значение атрибута может содержать дополнительные несохраненные биты.
ms.assetid: 4c635c04-8d2e-41b4-809c-58ce64271a02
ms.tgt_platform: multiple
keywords:
- MS-DS-User-Account-Control-схема AD для атрибута
- msDS-User-Account-Control-схема AD для атрибута
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Control-Computed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8747bddccdfa65222072592b7f418fd35529d987f9903d71cddf5e01556fec53
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119763264"
---
# <a name="ms-ds-user-account-control-computed-attribute"></a>MS-DS-User-Account-Control-вычисленный атрибут

**msDS-User-Account-Control — вычисление** выполняется примерно так же, как [**userAccountControl**](a-useraccountcontrol.md), но значение атрибута может содержать дополнительные несохраненные биты. К вычисленным битам относятся следующие.



| Значение                | Имя (определено в iAds. h)                     |
|----------------------|----------------------------------------------|
| 0x0010<br/>    | **\_Блокировка УФ**<br/>                   |
| 0x800000<br/>  | **\_ \_ срок действия пароля УФ истек**<br/>         |
| 0x4000000<br/> | **\_ \_ учетная запись частичных СЕКРЕТов УФ \_**<br/> |
| 0x8000000<br/> | **УФ \_ использовать \_ \_ ключи AES**<br/>            |



 

Полный список битов [**управления учетными записями пользователей**](a-useraccountcontrol.md) и, следовательно, определяемых пользователем контрольных данных **msDS-User-Control** , также можно найти на странице справочника по **контролю учетных записей** (сопоставляется через набор флагов [ADSI](/windows/desktop/ADSI/active-directory-service-interfaces-adsi) ) или на страницах справочника по управлению сетями для структуры [**\_ сведений о пользователе \_ 1008**](/windows/desktop/api/lmaccess/ns-lmaccess-user_info_1008) .



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | MS-DS-User-Account-Control — вычисленный  |
| LDAP-отображаемое имя | msDS-User-Account-Control — вычисление   |
| Размер              | \-                                   |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1460              |
| System-ID — GUID    | 2cc4b836-b63f-4940-8d23-ea7acf06af56 |
| Синтаксис            | [**Перечисление**](s-enumeration.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Неверно                             |
| Является однозначным       | Верно                              |
| Индексируется             | Неверно                             |
| В глобальном каталоге      | Неверно                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Неверно                                                             |
| Является однозначным       | Верно                                                              |
| Индексируется             | Неверно                                                             |
| В глобальном каталоге      | Неверно                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000014                                                        |
| Классы, используемые в        | [**Объект MS-DS-BIND-Object**](c-msds-bindableobject.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Неверно                             |
| Является однозначным       | Верно                              |
| Индексируется             | Неверно                             |
| В глобальном каталоге      | Неверно                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Неверно                             |
| Является однозначным       | Верно                              |
| Индексируется             | Неверно                             |
| В глобальном каталоге      | Неверно                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Неверно                             |
| Является однозначным       | Верно                              |
| Индексируется             | Неверно                             |
| В глобальном каталоге      | Неверно                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Неверно                             |
| Является однозначным       | Верно                              |
| Индексируется             | Неверно                             |
| В глобальном каталоге      | Неверно                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | \-                                |
| Range-Upper            | \-                                |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000014                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



 

