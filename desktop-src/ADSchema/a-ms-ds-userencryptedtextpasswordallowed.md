---
title: Атрибут ms-DS-User-encrypted-Text-Password-Allowed
description: Указывает, будет ли Active Directory хранить пароль в формате обратимого шифрования.
ms.assetid: 67067cf6-60e3-4626-bf8c-a0a1264a899e
ms.tgt_platform: multiple
keywords:
- Схема AD для атрибута Active-DS-User-encrypted-Text-Password
- Схема AD атрибута ms-DS-Усеренкриптедтекстпассвордалловед
topic_type:
- apiref
api_name:
- ms-DS-User-Encrypted-Text-Password-Allowed
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e8fc10b3facce4bef7cc5ff73abe9e901f67171dc2615b79c62355ac61a7c10
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118687005"
---
# <a name="ms-ds-user-encrypted-text-password-allowed-attribute"></a>Атрибут ms-DS-User-encrypted-Text-Password-Allowed

Указывает, будет ли Active Directory хранить пароль в формате обратимого шифрования. Значение true, если пароль хранится в формате обратимого шифрования; в противном случае — значение false.

> [!Note]  
> Этот атрибут не используется [службы Active Directory облегченного доступа к каталогам](/previous-versions/windows/desktop/adam/active-directory-lightweight-directory-services) и включается только для полноты или контроля четности с помощью userAccountControl. AD LDS не сохраняет пароли с обратимым шифрованием независимо от значения этого атрибута на любом заданном объекте или политики безопасности компьютера, относящейся к обратимому шифрованию самого компьютера.

 



| Ввод | Значение |
|-------------------|--------------------------------------------|
| CN                | MS-DS-User-encrypted-Text-Password-Allowed |
| LDAP-отображаемое имя | MS-DS-Усеренкриптедтекстпассвордалловед     |
| Размер              | \-                                         |
| Привилегия обновления  | \-                                         |
| Частота обновления  | \-                                         |
| Attribute-Id      | 1.2.840.113556.1.4.1856                    |
| System-ID — GUID    | 5a87c7f2-93c5-454c-a8c5-8cb09613292e       |
| Синтаксис            | [**Логическое**](s-boolean.md)               |



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



## <a name="remarks"></a>Remarks

В ADAM этот атрибут заменяет флаг " [**ADS \_ УФ \_ Encrypted \_ Text \_ password \_**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) " для атрибута [**userAccountControl**](a-useraccountcontrol.md) .

 

