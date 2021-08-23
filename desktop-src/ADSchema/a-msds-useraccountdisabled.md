---
title: Атрибут ms-DS-User-Account-Disabled
description: Показывает включение и отключение учетной записи.
ms.assetid: 5d6ced7b-ca0f-4afa-b394-e61e80454f3d
ms.tgt_platform: multiple
keywords:
- Схема AD атрибута Active-DS-User-Account-Disabled
- Схема AD атрибута msDS-Усераккаунтдисаблед
topic_type:
- apiref
api_name:
- ms-DS-User-Account-Disabled
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9f0744cd835fab641de4f4d3386304a342fe3902fcf1a67b3367dc15b7ee68f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119544144"
---
# <a name="ms-ds-user-account-disabled-attribute"></a>Атрибут ms-DS-User-Account-Disabled

Показывает включение и отключение учетной записи. Значение true, если учетная запись отключена; в противном случае — значение false.



| Ввод | Значение |
|-------------------|--------------------------------------|
| CN                | MS-DS-User-Account-Disabled          |
| LDAP-отображаемое имя | msDS-Усераккаунтдисаблед             |
| Размер              | \-                                   |
| Привилегия обновления  | \-                                   |
| Частота обновления  | \-                                   |
| Attribute-Id      | 1.2.840.113556.1.4.1853              |
| System-ID — GUID    | 7c708658-7372-4211-b22b-13a45ffd1d61 |
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

В ADAM этот атрибут заменяет флаг [**ADS \_ УФ \_ аккаунтдисабле**](/windows/desktop/api/iads/ne-iads-ads_user_flag_enum) атрибута [**userAccountControl**](a-useraccountcontrol.md) .

 

