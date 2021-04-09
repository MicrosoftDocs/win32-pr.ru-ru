---
title: Атрибут ms-DS-User-Password-unrequired
description: Указывает, требуется ли пароль для учетной записи, на которую ссылается этот атрибут.
ms.assetid: 86779c6f-d05c-409a-afe4-99ebf7c0593e
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута ms-DS-User-Password-необязательна
- Схема AD атрибута ms-DS-Усерпассворднотрекуиред
topic_type:
- apiref
api_name:
- ms-DS-User-Password-Not-Required
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c8ebb439af9a960d2dc0721940d9f4d2ab852b6
ms.sourcegitcommit: b77ace27b0432e7cd3863191b11926be032fbe2f
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/14/2020
ms.locfileid: "104139030"
---
# <a name="ms-ds-user-password-not-required-attribute"></a>Атрибут ms-DS-User-Password-unrequired

Указывает, требуется ли пароль для учетной записи, на которую ссылается этот атрибут. Значение true, если пароль не требуется; в противном случае — значение false.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | MS-DS-User-Password — не требуется     |
| LDAP-отображаемое имя | MS-DS-Усерпассворднотрекуиред        |
| Размер              | \-                                   |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1854              |
| System-ID — GUID    | 8f066172-a25e-4f53-8dcd-0a67d5fb883d |
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

В ADAM этот атрибут заменяет флаг [**ADS \_ УФ \_ PASSWD \_ нотрекд**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) атрибута [**userAccountControl**](a-useraccountcontrol.md) .

 

