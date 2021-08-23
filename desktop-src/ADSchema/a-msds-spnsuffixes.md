---
title: Атрибут ms-DS-SPN-суффиксов
description: Этот атрибут описывает суффиксы имен узлов DNS, используемых серверами в лесу. Эти DNS-суффиксы будут использоваться совместно с другими лесами, которые имеют доверие между лесами с этим лесом.
ms.assetid: 56153832-1228-419f-99d4-eb1ce3edc867
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута ms-DS-SPN-суффиксов
- Схема AD атрибута msDS-Спнсуффиксес
topic_type:
- apiref
api_name:
- ms-DS-SPN-Suffixes
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17c51a0805fefe9dbb8ddbeca3da89e3f5b3e66714b562af57cebc7975875cda
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544424"
---
# <a name="ms-ds-spn-suffixes-attribute"></a>Атрибут ms-DS-SPN-суффиксов

Этот атрибут описывает суффиксы имен узлов DNS, используемых серверами в лесу. Эти DNS-суффиксы будут использоваться совместно с другими лесами, которые имеют доверие между лесами с этим лесом.



| Ввод | Значение |
|-------------------|----------------------------------------------|
| CN                | Суффиксы MS-DS-SPN                           |
| LDAP-отображаемое имя | msDS-Спнсуффиксес                             |
| Размер              | 255 байт                                    |
| Привилегия обновления  | Администратор домена                         |
| Частота обновления  | Когда серверы в лесу получают новый суффикс. |
| Attribute-Id      | 1.2.840.113556.1.4.1715                      |
| System-ID — GUID    | 789ee1eb-8c8e-4e4c-8cec-79b31b7617b5         |
| Синтаксис            | [**String(Юникод)**](s-string-unicode.md)  |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|---------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | Нет                                                         |
| Является однозначным       | Нет                                                         |
| Индексируется             | Нет                                                         |
| В глобальном каталоге      | Нет                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| Классы, используемые в        | [**Перекрестные ссылки на контейнеры**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|---------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | Нет                                                         |
| Является однозначным       | Нет                                                         |
| Индексируется             | Нет                                                         |
| В глобальном каталоге      | Нет                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| Классы, используемые в        | [**Перекрестные ссылки на контейнеры**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|---------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | Нет                                                         |
| Является однозначным       | Нет                                                         |
| Индексируется             | Нет                                                         |
| В глобальном каталоге      | Нет                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| Классы, используемые в        | [**Перекрестные ссылки на контейнеры**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|---------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | Нет                                                         |
| Является однозначным       | Нет                                                         |
| Индексируется             | Нет                                                         |
| В глобальном каталоге      | Нет                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| Классы, используемые в        | [**Перекрестные ссылки на контейнеры**](c-crossrefcontainer.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|---------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                            |
| MAPI-Id                | \-                                                            |
| System-Only            | Нет                                                         |
| Является однозначным       | Нет                                                         |
| Индексируется             | Нет                                                         |
| В глобальном каталоге      | Нет                                                         |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                  |
| Range-Lower            | \-                                                            |
| Range-Upper            | \-                                                            |
| Search-Flags           | 0x00000000                                                    |
| System-Flags           | 0x00000010                                                    |
| Классы, используемые в        | [**Перекрестные ссылки на контейнеры**](c-crossrefcontainer.md)<br/> |



 

 





