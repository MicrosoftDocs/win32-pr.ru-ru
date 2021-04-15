---
title: атрибут MS-TAPI-Conference-BLOB
description: Двоичный BLOB-объект данных, описывающий различные свойства многоадресной конференции TAPI. Его формат и содержимое определяются значением атрибута Protocol-Id в том же объекте. Как правило, данные в этом большом двоичном объекте преобразуются в RFC2327.
ms.assetid: f1d5baed-df3f-423e-aa2f-005e77e79725
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута MS-TAPI-Conference-BLOB
- Схема AD атрибута Мстапи-Конференцеблоб
topic_type:
- apiref
api_name:
- ms-TAPI-Conference-Blob
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5f4e3ec8b74144daca7af1788c08270d998c139c
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "105655363"
---
# <a name="ms-tapi-conference-blob-attribute"></a>атрибут MS-TAPI-Conference-BLOB

Двоичный BLOB-объект данных, описывающий различные свойства многоадресной конференции TAPI. Его формат и содержимое определяются значением атрибута Protocol-Id в том же объекте. Как правило, данные в этом большом двоичном объекте преобразуются в RFC2327.



| Ввод | Значение |
|-------------------|--------------------------------------------------------------------------------------------------------------|
| CN                | MS-TAPI-Conference-BLOB                                                                                      |
| LDAP-отображаемое имя | Мстапи — Конференцеблоб                                                                                        |
| Размер              | Может иметь произвольную длину.                                                                                  |
| Привилегия обновления  | Специальные привилегии не требуются.                                                                              |
| Частота обновления  | Может измениться на усмотрение владельца конференции TAPI, когда необходимо изменить некоторые данные о Конференции. |
| Attribute-Id      | 1.2.840.113556.1.4.1700                                                                                      |
| System-ID — GUID    | 4cc4601e-7201-4141-abc8-3e529ae88863                                                                         |
| Синтаксис            | [**Object(ссылка_на_реплику)**](s-object-replica-link.md)                                                        |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Неверно                                                             |
| Является однозначным       | True                                                              |
| Индексируется             | Неверно                                                             |
| В глобальном каталоге      | Неверно                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Неверно                                                             |
| Является однозначным       | True                                                              |
| Индексируется             | Неверно                                                             |
| В глобальном каталоге      | Неверно                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Неверно                                                             |
| Является однозначным       | True                                                              |
| Индексируется             | Неверно                                                             |
| В глобальном каталоге      | Неверно                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Неверно                                                             |
| Является однозначным       | True                                                              |
| Индексируется             | Неверно                                                             |
| В глобальном каталоге      | Неверно                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Неверно                                                             |
| Является однозначным       | True                                                              |
| Индексируется             | Неверно                                                             |
| В глобальном каталоге      | Неверно                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Классы, используемые в        | [**MS-TAPI-RT-Конференция**](c-mstapi-rtconference.md)<br/> |



 

 





