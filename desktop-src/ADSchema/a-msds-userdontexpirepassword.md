---
title: MS-DS-User-не-атрибут срока действия-пароля
description: Указывает, истечет ли срок действия пароля для учетной записи, на которую ссылается этот атрибут.
ms.assetid: bafbcb4a-ee45-4f88-8fb2-93840efd1289
ms.tgt_platform: multiple
keywords:
- Active-DS-User-не-схема AD атрибута срока действия пароля
- Схема AD атрибута msDS-Усердонтекспирепассворд
topic_type:
- apiref
api_name:
- ms-DS-User-Dont-Expire-Password
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75d5c0fa709f549a523d628433ee2b3aa626278e
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104138623"
---
# <a name="ms-ds-user-dont-expire-password-attribute"></a>MS-DS-User-не-атрибут срока действия-пароля

Указывает, истечет ли срок действия пароля для учетной записи, на которую ссылается этот атрибут. Значение true, если срок действия пароля не истечет; в противном случае — значение false.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | MS-DS-User-не-Expires — пароль      |
| LDAP-отображаемое имя | msDS-Усердонтекспирепассворд          |
| Размер              | \-                                   |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1855              |
| System-ID — GUID    | 8788193a-2925-43d9-a221-bb7fff397675 |
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
| System-Flags           | 0x00000010                                                        |
| Классы, используемые в        | [**Объект MS-DS-BIND-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Комментарии

В ADAM этот атрибут заменяет флаг [**ADS \_ УФ \_ не \_ Expires \_ PASSWD**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) атрибута [**userAccountControl**](a-useraccountcontrol.md) .

 

