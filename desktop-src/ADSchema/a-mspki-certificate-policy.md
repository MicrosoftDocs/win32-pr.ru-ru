---
title: MS-PKI-Certificate-атрибут политики
description: Содержит список идентификаторов OID политики и их необязательных CSP в выданном сертификате.
ms.assetid: bc84c5ff-9cb1-406c-825c-97fa479d52eb
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута политики MS-PKI-Certificate
- Мспки-схема AD атрибута политики сертификата
topic_type:
- apiref
api_name:
- ms-PKI-Certificate-Policy
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8abe92cda39428e397f06105a0ca8c5b151f84989615e06ec2f6c8371f87fc75
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119081688"
---
# <a name="ms-pki-certificate-policy-attribute"></a>MS-PKI-Certificate-атрибут политики

Содержит список идентификаторов OID политики и их необязательных CSP в выданном сертификате.



| Ввод | Значение |
|-------------------|---------------------------------------------------------------------------------------------------|
| CN                | MS-PKI-Certificate-политика                                                                         |
| LDAP-отображаемое имя | Мспки — политика сертификата                                                                          |
| Размер              | 64 байт больше числа записей.                                                             |
| Привилегия обновления  | Администратор домена                                                                              |
| Частота обновления  | При изменении, создании или клонировании объекта шаблона сертификата (MS-PKI-Certificate-Template). |
| Attribute-Id      | 1.2.840.113556.1.4.1439                                                                           |
| System-ID — GUID    | 38942346-cc5b-424b-a7d8-6ffd12029c5f                                                              |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md)                                                       |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Нет                                                                   |
| Является однозначным       | Нет                                                                   |
| Индексируется             | Нет                                                                   |
| В глобальном каталоге      | Нет                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Классы, используемые в        | [**PKI — шаблон сертификата**](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Нет                                                                   |
| Является однозначным       | Нет                                                                   |
| Индексируется             | Нет                                                                   |
| В глобальном каталоге      | Нет                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Классы, используемые в        | [**PKI — шаблон сертификата**](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Нет                                                                   |
| Является однозначным       | Нет                                                                   |
| Индексируется             | Нет                                                                   |
| В глобальном каталоге      | Нет                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Классы, используемые в        | [**PKI — шаблон сертификата**](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Нет                                                                   |
| Является однозначным       | Нет                                                                   |
| Индексируется             | Нет                                                                   |
| В глобальном каталоге      | Нет                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Классы, используемые в        | [**PKI — шаблон сертификата**](c-pkicertificatetemplate.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                      |
| MAPI-Id                | \-                                                                      |
| System-Only            | Нет                                                                   |
| Является однозначным       | Нет                                                                   |
| Индексируется             | Нет                                                                   |
| В глобальном каталоге      | Нет                                                                   |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                            |
| Range-Lower            | \-                                                                      |
| Range-Upper            | \-                                                                      |
| Search-Flags           | 0x00000000                                                              |
| System-Flags           | 0x00000010                                                              |
| Классы, используемые в        | [**PKI — шаблон сертификата**](c-pkicertificatetemplate.md)<br/> |



 

 





