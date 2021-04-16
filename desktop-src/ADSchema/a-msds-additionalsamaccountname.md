---
title: Атрибут ms-DS-дополнительно-SAM-Account-Name
description: Этот атрибут используется для хранения имен учетных записей SAM, соответствующих именам узлов DNS в MS-DS-дополнительно-DNS-Host-Name.
ms.assetid: eb69e1d4-42b7-42e1-aeae-77188db307ef
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута ms-DS-дополнительно-SAM-Account-Name
- Схема AD атрибута msDS-Аддитионалсамаккаунтнаме
topic_type:
- apiref
api_name:
- ms-DS-Additional-Sam-Account-Name
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a437c30e6ddb0e551498480f7589791bce59feaf
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655463"
---
# <a name="ms-ds-additional-sam-account-name-attribute"></a>Атрибут ms-DS-дополнительно-SAM-Account-Name

Этот атрибут используется для хранения имен учетных записей SAM, соответствующих именам узлов DNS в MS-DS-дополнительно-DNS-Host-Name.



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | MS-DS-дополнительно-SAM-Account-Name           |
| LDAP-отображаемое имя | msDS-Аддитионалсамаккаунтнаме               |
| Размер              | Менее 20 байт.                         |
| Привилегия обновления  | Это значение задается системой.            |
| Частота обновления  | При переименовании контроллера домена.                     |
| Attribute-Id      | 1.2.840.113556.1.4.1718                     |
| System-ID — GUID    | 975571df-a4d5-429a-9f59-cdc6581d91e6        |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md) |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-------------------------------------------|
| Идентификатор ссылки                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | True                                      |
| Является однозначным       | Неверно                                     |
| Индексируется             | True                                      |
| В глобальном каталоге      | Неверно                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 256                                       |
| Search-Flags           | 0x0000000D                                |
| System-Flags           | 0x00000010                                |
| Классы, используемые в        | [**Компьютер**](c-computer.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-------------------------------------------|
| Идентификатор ссылки                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | True                                      |
| Является однозначным       | Неверно                                     |
| Индексируется             | True                                      |
| В глобальном каталоге      | Неверно                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 256                                       |
| Search-Flags           | 0x0000000D                                |
| System-Flags           | 0x00000010                                |
| Классы, используемые в        | [**Компьютер**](c-computer.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-------------------------------------------|
| Идентификатор ссылки                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | True                                      |
| Является однозначным       | Неверно                                     |
| Индексируется             | True                                      |
| В глобальном каталоге      | Неверно                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 256                                       |
| Search-Flags           | 0x0000000D                                |
| System-Flags           | 0x00000010                                |
| Классы, используемые в        | [**Компьютер**](c-computer.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-------------------------------------------|
| Идентификатор ссылки                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | True                                      |
| Является однозначным       | Неверно                                     |
| Индексируется             | True                                      |
| В глобальном каталоге      | Неверно                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 256                                       |
| Search-Flags           | 0x0000000D                                |
| System-Flags           | 0x00000010                                |
| Классы, используемые в        | [**Компьютер**](c-computer.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-------------------------------------------|
| Идентификатор ссылки                | \-                                        |
| MAPI-Id                | \-                                        |
| System-Only            | True                                      |
| Является однозначным       | Неверно                                     |
| Индексируется             | True                                      |
| В глобальном каталоге      | Неверно                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                              |
| Range-Lower            | 0                                         |
| Range-Upper            | 256                                       |
| Search-Flags           | 0x0000000D                                |
| System-Flags           | 0x00000010                                |
| Классы, используемые в        | [**Компьютер**](c-computer.md)<br/> |



 

 





