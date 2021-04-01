---
title: Атрибут ms-DS-User-Password-Expires
description: Указывает, истек ли срок действия пароля для учетной записи, на которую ссылается этот атрибут.
ms.assetid: cab4a2e8-b440-45d2-8da8-9f020ffee08c
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута с истекшим сроком действия MS-DS-User-Password
- Схема AD атрибута msDS-Усерпассвордекспиред
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Expired
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73d99143c470e58d1b1cb5e0cbd7e5302618ff0a
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104262266"
---
# <a name="ms-ds-user-password-expired-attribute"></a>Атрибут ms-DS-User-Password-Expires

Указывает, истек ли срок действия пароля для учетной записи, на которую ссылается этот атрибут. Значение true, если срок действия пароля истек; в противном случае — значение false.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | MS-DS-User-Password-срок действия истек          |
| LDAP-отображаемое имя | msDS-Усерпассвордекспиред             |
| Размер              | \-                                   |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1858              |
| System-ID — GUID    | 565c7ab5-e13e-47f6-abb5-de741806f125 |
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

В ADAM этот атрибут заменяет флаг " [**ADS" \_ УФ " \_ \_ срок действия пароля истек**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) " атрибута [**userAccountControl**](a-useraccountcontrol.md) .

 

