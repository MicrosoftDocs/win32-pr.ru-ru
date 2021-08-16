---
title: Структура BITS_FILE_PROPERTY_VALUE (Deliveryoptimization. h)
description: BITS_FILE_PROPERTY_VALUE Union предоставляет значение свойства файла DO, основанное на значении из перечисления BITS_FILE_PROPERTY_ID.
ms.assetid: 56A634F9-FB30-49D5-BD03-DD59AEF702C1
keywords:
- Структура BITS_FILE_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_FILE_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ba01a8c83cef842c40149b3fe8cbc586a7da5f819ffc387befb9f84182cbce24
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118544629"
---
# <a name="bits_file_property_value-structure"></a>Структура BITS_FILE_PROPERTY_VALUE

**BITS_FILE_PROPERTY_VALUE** Union предоставляет значение свойства файла Do, основанное на значении из перечисления [**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md) .

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  LPWSTR String;
} BITS_FILE_PROPERTY_VALUE;
```



## <a name="members"></a>Члены

<dl> <dt>

**String**
</dt> <dd>

Это значение используется при использовании значения перечисления идентификатора свойства **BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | Windows 10, только для \[ настольных приложений версии 1709\]<br/>                                         |
| Минимальная версия сервера<br/> | Windows Server, только для \[ настольных приложений версии 1709\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Deliveryoptimization. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**BITS_FILE_PROPERTY_ID**](bits-file-property-id-.md)
</dt> <dt>

[**IBackgroundCopyFile5., свойство**](ibackgroundcopyfile5-getproperty.md)
</dt> <dt>

[**IBackgroundCopyFile5. SetProperty**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





