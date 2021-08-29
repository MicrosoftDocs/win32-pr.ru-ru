---
description: Указывает расположение для поиска Active Directory хранилище сертификатов.
ms.assetid: 56b9695e-7ab9-405b-9cae-d78c43071186
title: Перечисление CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_ACTIVE_DIRECTORY_SEARCH_LOCATION
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: 52f205717f3ba361c2c15dafc6e53f6cef3cd9d41cbbbf2ed243c60a74c2ca62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879444"
---
# <a name="capicom_active_directory_search_location-enumeration"></a>\_ \_ \_ \_ Перечисление расположения поиска CAPICOM Active Directory

Тип перечисления **CAPICOM \_ Active \_ Directory \_ Search \_** указывает расположение для поиска Active Directory [*хранилище сертификатов*](../secgloss/c-gly.md).

## <a name="members"></a>Элементы



| Член                               | Описание                                  | Значение |
|--------------------------------------|----------------------------------------------|-------|
| **CAPICOM \_ Поиск \_**             | Выполняет поиск во всех доступных расположениях.<br/> | 0     |
| **CAPICOM \_ Поиск в \_ глобальном \_ каталоге** | Выполняет поиск только в глобальном каталоге.<br/> | 1     |
| **\_Поиск в \_ домене CAPICOM по умолчанию \_** | Выполняет поиск только по домену по умолчанию.<br/> | 2     |



## <a name="remarks"></a>Remarks

Этот тип перечисления используется следующим свойством:

-   [**Параметры. активедиректорисеарчлокатион**](settings-activedirectorysearchlocation.md)

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|--------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                |
| Заголовок<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 
