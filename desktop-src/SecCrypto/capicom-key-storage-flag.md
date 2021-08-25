---
description: '\_ \_ \_ Перечисление флагов хранилища CAPICOM определяет флаги хранилища ключей.'
ms.assetid: 326cef75-24a5-4dc9-a7e9-a63dd3d8de54
title: Перечисление CAPICOM_KEY_STORAGE_FLAG (CAPICOM. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAPICOM_KEY_STORAGE_FLAG
api_type:
- HeaderDef
api_location:
- Capicom.h
ms.openlocfilehash: cb1c2c4761403223c8ed0eb225709fbd189127bc9d56d60b82a534e2bc15b8e0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119879094"
---
# <a name="capicom_key_storage_flag-enumeration"></a>\_ \_ \_ Перечисление ФЛАГов хранилища CAPICOM

Перечисление **\_ \_ \_ флагов хранилища CAPICOM** определяет флаги хранилища ключей.

## <a name="members"></a>Элементы



| Член                                     | Описание                           | Значение |
|--------------------------------------------|---------------------------------------|-------|
| **\_хранилище CAPICOM \_ key \_ по умолчанию**         | Хранилище ключей по умолчанию.<br/>       | 0     |
| **\_хранилище CAPICOM Key, \_ \_ экспортируемое**      | Ключ доступен для экспорта.<br/>     | 1     |
| **\_ \_ \_ защищенное пользователем хранилище CAPICOM key \_** | Ключ защищен пользователем.<br/> | 2     |



## <a name="remarks"></a>Remarks

Это перечисление используется следующим методом:

-   [**Certificate. Load**](certificate-load.md)
-   [**Store. Load**](store-load.md)

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|----------------------------|--------------------------------------------------------------------------------------|
| Распространяемые компоненты<br/> | CAPICOM 2,0 или более поздней версии на Windows Server 2003 и Windows XP<br/>                |
| Заголовок<br/>          | <dl> <dt>CAPICOM. h</dt> </dl> |



 

 




