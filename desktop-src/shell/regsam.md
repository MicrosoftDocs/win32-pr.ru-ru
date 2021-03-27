---
description: Тип данных, используемый для указания атрибутов доступа безопасности в реестре.
title: РЕГСАМ (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 003f6be9-e4ba-4d23-b486-a167063c630e
api_name:
- KEY_ALL_ACCESS
- KEY_CREATE_LINK
- KEY_CREATE_SUB_KEY
- KEY_ENUMERATE_SUB_KEYS
- KEY_EXECUTE
- KEY_NOTIFY
- KEY_QUERY_VALUE
- KEY_READ
- KEY_SET_VALUE
- KEY_WRITE
api_type:
- HeaderDef
api_location:
- Winnt.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 2700e278f86db046d532b91b64bf5a2d00582e14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "104987605"
---
# <a name="regsam"></a>регсам

Тип данных, используемый для указания атрибутов доступа безопасности в реестре.



| Константа                                                                                                                                                                                   | Описание                                                                                                                                                                                                |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="KEY_ALL_ACCESS"></span><span id="key_all_access"></span><dl> <dt>**КЛЮЧЕВОЙ \_ полный \_ доступ**</dt> </dl>                          | Сочетание * * * * ключ \_ запроса \_ значения * * * *, * * * * ключ \_ перечисляет \_ \_ подразделы * * * *, * * * * \_ уведомление о ключе * * * *, * * * * \_ ключ \_ создания \_ подраздела * * \_ \_ \_ \_ * *, * * * * ключ создания ссылки * * * * и * * * * * * * * *<br/> |
| <span id="KEY_CREATE_LINK"></span><span id="key_create_link"></span><dl> <dt>**\_ссылка для создания ключа \_**</dt> </dl>                       | Разрешение на создание символьной ссылки.<br/>                                                                                                                                                           |
| <span id="KEY_CREATE_SUB_KEY"></span><span id="key_create_sub_key"></span><dl> <dt>**ключ \_ создания \_ ключа \_**</dt> </dl>             | Разрешение на создание подразделов.<br/>                                                                                                                                                                   |
| <span id="KEY_ENUMERATE_SUB_KEYS"></span><span id="key_enumerate_sub_keys"></span><dl> <dt>**КЛЮЧ, \_ Перечисление \_ вложенных \_ ключей**</dt> </dl> | Разрешение на перечисление подразделов.<br/>                                                                                                                                                                |
| <span id="KEY_EXECUTE"></span><span id="key_execute"></span><dl> <dt>**\_выполнение ключа**</dt> </dl>                                    | Разрешение на доступ для чтения.<br/>                                                                                                                                                                     |
| <span id="KEY_NOTIFY"></span><span id="key_notify"></span><dl> <dt>**\_уведомление ключа**</dt> </dl>                                       | Разрешение на уведомление об изменении.<br/>                                                                                                                                                             |
| <span id="KEY_QUERY_VALUE"></span><span id="key_query_value"></span><dl> <dt>**значение КЛЮЧЕВого \_ запроса \_**</dt> </dl>                       | Разрешение на запрос данных подраздела.<br/>                                                                                                                                                                |
| <span id="KEY_READ"></span><span id="key_read"></span><dl> <dt>**\_чтение ключа**</dt> </dl>                                             | Сочетание * * * * ключ \_ запроса \_ значения * * * *, * * * * ключ \_ перечисляет \_ \_ подразделы * * * * и * * * * \_ уведомление о ключе * * * * доступ.<br/>                                                                                    |
| <span id="KEY_SET_VALUE"></span><span id="key_set_value"></span><dl> <dt>**\_значение набора \_ ключей**</dt> </dl>                             | Разрешение на установку данных подраздела.<br/>                                                                                                                                                                  |
| <span id="KEY_WRITE"></span><span id="key_write"></span><dl> <dt>**\_запись ключа**</dt> </dl>                                          | Сочетание * * * * \_ значения набора ключей \_ * * * * и * * * * ключ \_ создания \_ \_ подраздела * * * * Access.<br/>                                                                                                                |



## <a name="remarks"></a>Примечания

Значение **регсам** может быть одним или несколькими перечисляемыми значениями.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Файл Winnt. h</dt> </dl> |



 

 




