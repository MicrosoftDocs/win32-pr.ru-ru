---
title: Атрибут имени пользователя-участника
description: Этот атрибут содержит имя входа в Интернет для пользователя, основанного на стандарте RFC 822 в формате Интернета.
ms.assetid: 588e76fa-45b6-4853-821a-9e5730255b9f
ms.tgt_platform: multiple
keywords:
- Имя пользователя-субъекта-схема атрибута AD
- Схема AD атрибута userPrincipalName
topic_type:
- apiref
api_name:
- User-Principal-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ffdb5bde76325409e0911615d1d21b1b4f593c06
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "103989619"
---
# <a name="user-principal-name-attribute"></a>Атрибут имени пользователя-участника

Этот атрибут содержит имя входа в Интернет для пользователя, основанного на стандарте [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)в формате Интернета. Имя участника-пользователя короче различающегося имени и проще запомнить. По соглашению оно должно сопоставляться с именем электронной почты пользователя. Значение, заданное для этого атрибута, равно длине идентификатора пользователя и имени домена. Дополнительные сведения об этом атрибуте см. в разделе [атрибуты именования пользователей](/windows/desktop/AD/naming-properties).



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | User-Principal-Name                         |
| LDAP-отображаемое имя | userPrincipalName                           |
| Размер              | \-                                          |
| Привилегия обновления  | Администратор домена или владелец учетной записи.      |
| Частота обновления  | Теоретически это не должно изменяться.         |
| Attribute-Id      | 1.2.840.113556.1.4.656                      |
| System-ID — GUID    | 28630ebb-41d5-11d1-a9c1-0000f80367c1        |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows 2000 Server**](#windows-2000-server)
-   [**Windows Server 2003**](#windows-server-2003)
-   [**ADAM**](#adam)
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
| Search-Flags           | 0x00000001                        |
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
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Классы, используемые в        | [**Нажат**](c-user.md)<br/> |



## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|--------------|
| Идентификатор ссылки                | \-           |
| MAPI-Id                | \-           |
| System-Only            | Неверно        |
| Является однозначным       | True         |
| Индексируется             | True         |
| В глобальном каталоге      | True         |
| NT-Security-дескриптор | О:БАГ: BAD: S: |
| Range-Lower            | \-           |
| Range-Upper            | \-           |
| Search-Flags           | 0x00000001   |
| System-Flags           | 0x00000012   |
| Классы, используемые в        | \-           |



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
| Search-Flags           | 0x00000001                        |
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
| Search-Flags           | 0x00000001                        |
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
| Search-Flags           | 0x00000001                        |
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
| Search-Flags           | 0x00000001                        |
| System-Flags           | 0x00000012                        |
| Классы, используемые в        | [**Нажат**](c-user.md)<br/> |



## <a name="remarks"></a>Комментарии

В ADAM этот атрибут не обязательно должен быть в стандартном формате RFC 822. Это может быть простое имя.

 

