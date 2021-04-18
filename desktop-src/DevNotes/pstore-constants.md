---
description: В PStore используются следующие константы.
ms.assetid: 4bdccb86-2e0e-461c-9a74-184861b7db1e
title: Константы PStore (PStore. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PST_E_OK
- PST_E_TYPE_EXISTS
- PST_AUTHENTICODE
- PST_BINARY_CHECK
- PST_SECURITY_DESCRIPTOR
api_type:
- HeaderDef
api_location:
- Pstore.h
ms.openlocfilehash: 1c80fe7235a859ef0a754420fe5bd22caa10d6bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/22/2021
ms.locfileid: "105668539"
---
# <a name="pstore-constants"></a>Константы PStore

\[Защищенное хранилище (PStore) доступно для использования в Windows Server 2003 и Windows XP. Она доступна только для операций чтения в Windows Server 2008 и Windows Vista, но может быть недоступна в последующих версиях. PStore использует старую реализацию защиты данных. Разработчикам настоятельно рекомендуется использовать преимущества более надежной защиты данных, предоставляемые функциями [**CryptProtectData**](/windows/win32/api/dpapi/nf-dpapi-cryptprotectdata) и [**CryptUnprotectData**](/windows/win32/api/dpapi/nf-dpapi-cryptunprotectdata) .\]

В PStore используются следующие константы.

Коды ошибок защищенного хранилища



| Константа/значение                                                                                                                                                                                                                               | Описание                                                        |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| <span id="PST_E_OK"></span><span id="pst_e_ok"></span><dl> PST-файл <dt>**\_ E \_**</dt> ! <dt>0x00000000</dt> </dl>                             | Операция выполнена успешно.<br/>                           |
| <span id="PST_E_TYPE_EXISTS"></span><span id="pst_e_type_exists"></span><dl> PST-файл <dt>**\_ \_Тип E \_ существует**</dt> <dt>0x800C0004L</dt> </dl> | Элемент данных уже существует в защищенном хранилище. <br/> |



Значения предложения Access



| Константа/значение                                                                                                                                                                                                                                      | Описание                                                                             |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------|
| <span id="PST_AUTHENTICODE"></span><span id="pst_authenticode"></span><dl> PST-файл <dt>**\_ AUTHENTICODE**</dt> <dt>1</dt> </dl>                       | Указывает на структуру [**PST \_ аусентикодедата**](pst-authenticodedata.md) .<br/> |
| <span id="PST_BINARY_CHECK_"></span><span id="pst_binary_check_"></span><dl> <dt> **\_ Двоичная \_ Проверка PST**</dt> <dt>2</dt> </dl>                   | Указывает на структуру **PST \_ бинаричеккдата** .<br/>                              |
| <span id="PST_SECURITY_DESCRIPTOR"></span><span id="pst_security_descriptor"></span><dl> PST-файл <dt>**\_ \_Дескриптор безопасности**</dt> <dt>4</dt> </dl> | Указывает на допустимый дескриптор безопасности Windows. <br/>                              |



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|-------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>PStore. h</dt> </dl> |



 

 
