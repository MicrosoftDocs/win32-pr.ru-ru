---
title: MS-FRS-Hub-атрибут члена
description: Для записи предпочтительных параметров топологии NTFRS используется атрибут MS-FRS-Hub-Member.
ms.assetid: df8623e0-745a-46f8-a696-8f6e7014fd2b
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута членства MS-FRS-HUB
- Мсфрс-Hub-схема AD атрибута Member
topic_type:
- apiref
api_name:
- ms-FRS-Hub-Member
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fa08d1eb3cbb8086149192e6ecd5fa3880f01e6cfa1800468d2825c243b211e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119803313"
---
# <a name="ms-frs-hub-member-attribute"></a>MS-FRS-Hub-атрибут члена

Для записи предпочтительных параметров топологии NTFRS используется атрибут **MS-FRS-Hub-Member** . Когда член FRS добавляется в набор реплик или удаляется из него, эти атрибуты называются, и в подключения между остальными членами FRS в наборе реплик устанавливаются соответствующие изменения.



| Ввод | Значение |
|-------------------|--------------------------------------------------------------------|
| CN                | MS-FRS-Hub-член                                                  |
| LDAP-отображаемое имя | Мсфрс-Hub-член                                                   |
| Размер              | \-                                                                 |
| Привилегия обновления  | Администратор домена                                               |
| Частота обновления  | При создании набора реплик или изменении предпочтительной топологии. |
| Attribute-Id      | 1.2.840.113556.1.4.1693                                            |
| System-ID — GUID    | 5643ff81-35b6-4ca9-9512-baf0bd0a2772                               |
| Синтаксис            | [**Object(DS-DN)**](s-object-ds-dn.md)                            |



## <a name="implementations"></a>Варианты реализации решения

-   [**Windows Server 2003**](#windows-server-2003)
-   [**Windows Server 2003 R2**](#windows-server-2003-r2)
-   [**Windows Server 2008**](#windows-server-2008)
-   [**Windows Server 2008 R2**](#windows-server-2008-r2)
-   [**Windows Server 2012**](#windows-server-2012)

## <a name="windows-server-2003"></a>Windows Server 2003



| Ввод | Значение |
|------------------------|-----------------------------------------------------------|
| Идентификатор ссылки                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Нет                                                     |
| Является однозначным       | Верно                                                      |
| Индексируется             | Нет                                                     |
| В глобальном каталоге      | Нет                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Классы, используемые в        | [**NTFRS-Set-реплика**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2003-r2"></a>Windows Server 2003 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------|
| Идентификатор ссылки                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Нет                                                     |
| Является однозначным       | Верно                                                      |
| Индексируется             | Нет                                                     |
| В глобальном каталоге      | Нет                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Классы, используемые в        | [**NTFRS-Set-реплика**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008"></a>Windows Server 2008



| Ввод | Значение |
|------------------------|-----------------------------------------------------------|
| Идентификатор ссылки                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Нет                                                     |
| Является однозначным       | Верно                                                      |
| Индексируется             | Нет                                                     |
| В глобальном каталоге      | Нет                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Классы, используемые в        | [**NTFRS-Set-реплика**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2008-r2"></a>Windows Server 2008 R2



| Ввод | Значение |
|------------------------|-----------------------------------------------------------|
| Идентификатор ссылки                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Нет                                                     |
| Является однозначным       | Верно                                                      |
| Индексируется             | Нет                                                     |
| В глобальном каталоге      | Нет                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Классы, используемые в        | [**NTFRS-Set-реплика**](c-ntfrsreplicaset.md)<br/> |



## <a name="windows-server-2012"></a>Windows Server 2012



| Ввод | Значение |
|------------------------|-----------------------------------------------------------|
| Идентификатор ссылки                | 1046                                                      |
| MAPI-Id                | \-                                                        |
| System-Only            | Нет                                                     |
| Является однозначным       | Верно                                                      |
| Индексируется             | Нет                                                     |
| В глобальном каталоге      | Нет                                                     |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                              |
| Range-Lower            | \-                                                        |
| Range-Upper            | \-                                                        |
| Search-Flags           | 0x00000000                                                |
| System-Flags           | 0x00000000                                                |
| Классы, используемые в        | [**NTFRS-Set-реплика**](c-ntfrsreplicaset.md)<br/> |



## <a name="remarks"></a>Remarks

Это полное различающееся имя объекта [**члена NTFRS**](c-ntfrsmember.md) . Различающееся имя имеет формат "CN = *<computerGuid>* , CN = *<Dfs Link Name>* , CN = *<Dfs Root name>* , CN = тома DFS, CN = служба репликации файлов, CN = System, DC =..."

 

 





