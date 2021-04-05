---
title: MS-DS-User-Account-атрибут автоматической блокировки
description: Указывает, заблокирована ли учетная запись, на которую ссылается этот атрибут.
ms.assetid: f9d9c98a-3c4f-4687-8133-4476aeec10e8
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-DS-User-Account-Auto-locked
- Схема AD атрибута ms-DS-Усераккаунтаутолоккед
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Auto-Locked
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6623a1b348af14fecc8dab41a44439bf2d745bf9
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104072112"
---
# <a name="ms-ds-user-account-auto-locked-attribute"></a>MS-DS-User-Account-атрибут автоматической блокировки

Указывает, заблокирована ли учетная запись, на которую ссылается этот атрибут. Значение true, если учетная запись заблокирована; в противном случае — значение false.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | MS-DS-пользователь-учетная запись — автоматическая блокировка       |
| LDAP-отображаемое имя | MS-DS-Усераккаунтаутолоккед          |
| Размер              | \-                                   |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1857              |
| System-ID — GUID    | f2dd7bab-1f3b-47cf-89fa-143b56ad0a3d |
| Синтаксис            | [**Логическая**](s-boolean.md)         |



## <a name="implementations"></a>Варианты реализации решения

-   [**ADAM**](#adam)

## <a name="adam"></a>ADAM



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
| System-Flags           | 0x00000014                                                        |
| Классы, используемые в        | [**Объект MS-DS-BIND-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Комментарии

В ADAM этот атрибут заменяет флаг [**ADS \_ УФ \_ блокировки**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) атрибута [**userAccountControl**](a-useraccountcontrol.md) .

 

