---
title: Атрибут User-Parameters
description: Параметры пользователя.
ms.assetid: e3d6d22d-5112-4dfe-af55-a17a63e5f2e4
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута User-Parameters
- Схема AD атрибута Усерпараметерс
topic_type:
- apiref
api_name:
- User-Parameters
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3f26907015ee1c17bc4e809b3b5c2a52adf79ffb20d497e34ff094b620936436
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119922934"
---
# <a name="user-parameters-attribute"></a>Атрибут User-Parameters

Параметры пользователя. Указывает на строку в Юникоде, которая задается не для использования приложениями. Эта строка может быть пустой строкой или содержать любое число символов перед завершающим нулевым символом. Продукты Майкрософт используют этот элемент для хранения пользовательских данных, относящихся к отдельной программе.



| Ввод | Значение |
|-------------------|---------------------------------------------|
| CN                | User-Parameters                             |
| LDAP-отображаемое имя | усерпараметерс                              |
| Размер              | \-                                          |
| Привилегия обновления  | Изменено приложениями.                   |
| Частота обновления  | \-                                          |
| Attribute-Id      | 1.2.840.113556.1.4.138                      |
| System-ID — GUID    | bf967a6d-0de6-11d0-a285-00aa003049e2        |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md) |



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
| System-Only            | Нет.                             |
| Является однозначным       | Верно                              |
| Индексируется             | Нет.                             |
| В глобальном каталоге      | Нет.                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет.                             |
| Является однозначным       | Верно                              |
| Индексируется             | Нет.                             |
| В глобальном каталоге      | Нет.                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет.                             |
| Является однозначным       | Верно                              |
| Индексируется             | Нет.                             |
| В глобальном каталоге      | Нет.                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет.                             |
| Является однозначным       | Верно                              |
| Индексируется             | Нет.                             |
| В глобальном каталоге      | Нет.                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет.                             |
| Является однозначным       | Верно                              |
| Индексируется             | Нет.                             |
| В глобальном каталоге      | Нет.                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------|
| Идентификатор ссылки                | \-                                |
| MAPI-Id                | \-                                |
| System-Only            | Нет.                             |
| Является однозначным       | Верно                              |
| Индексируется             | Нет.                             |
| В глобальном каталоге      | Нет.                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                      |
| Range-Lower            | 0                                 |
| Range-Upper            | 32767                             |
| Search-Flags           | 0x00000000                        |
| System-Flags           | 0x00000010                        |
| Классы, используемые в        | [**Пользователь**](c-user.md)<br/> |



 

 





