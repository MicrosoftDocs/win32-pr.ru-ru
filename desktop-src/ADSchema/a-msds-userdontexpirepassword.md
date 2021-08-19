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
ms.openlocfilehash: 7af661ca1317f7506e5bcdbf611010b0fe4c058d5f1e3f1e5f31b917737a6e64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118425434"
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
| Синтаксис            | [**Логическое**](s-boolean.md)         |



## <a name="implementations"></a>Варианты реализации решения

-   [**ADAM**](#adam)

## <a name="adam"></a>ADAM



| Ввод | Значение |
|------------------------|-------------------------------------------------------------------|
| Идентификатор ссылки                | \-                                                                |
| MAPI-Id                | \-                                                                |
| System-Only            | Нет                                                             |
| Является однозначным       | Верно                                                              |
| Индексируется             | Нет                                                             |
| В глобальном каталоге      | Нет                                                             |
| NT-Security-дескриптор | О:БАГ: BAD: S:                                                      |
| Range-Lower            | \-                                                                |
| Range-Upper            | \-                                                                |
| Search-Flags           | 0x00000000                                                        |
| System-Flags           | 0x00000010                                                        |
| Классы, используемые в        | [**Объект MS-DS-BIND-Object**](c-msds-bindableobject.md)<br/> |



## <a name="remarks"></a>Remarks

В ADAM этот атрибут заменяет флаг [**ADS \_ УФ \_ не \_ Expires \_ PASSWD**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) атрибута [**userAccountControl**](a-useraccountcontrol.md) .

 

