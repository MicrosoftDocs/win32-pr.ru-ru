---
title: Перечисление MP_HASH_TYPE (Мпклиент. h)
description: Возможные типы хэширования.
ms.assetid: 46432C40-6DE1-4FB8-B7C1-C2712CCEB208
keywords:
- MP_HASH_TYPE перечисления устаревшие функции среды Windows
- PMP_HASH_TYPE указателя перечисления устаревшие функции среды Windows
topic_type:
- apiref
api_name:
- MP_HASH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 40c36e709d165845b729673df4aaea1042a7ee49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 12/12/2020
ms.locfileid: "104492639"
---
# <a name="mp_hash_type-enumeration"></a>\_ \_ Перечисление типов хэша MP

Возможные типы хэширования.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum tagMP_HASH_TYPE { 
  MP_HASH_TYPE_NONE    = 0,
  MP_HASH_TYPE_CRC32   = 2,
  MP_HASH_TYPE_MD5     = 4,
  MP_HASH_TYPE_SHA1    = 8,
  MP_HASH_TYPE_SHA256  = 16
} MP_HASH_TYPE, *PMP_HASH_TYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="MP_HASH_TYPE_NONE"></span><span id="mp_hash_type_none"></span>**\_тип ХЭША \_ MP \_ None**
</dt> <dd>

Нет хэша.

</dd> <dt>

<span id="MP_HASH_TYPE_CRC32"></span><span id="mp_hash_type_crc32"></span>**\_ \_ CRC32 тип хэша пакета управления \_**
</dt> <dd>

CRC32

</dd> <dt>

<span id="MP_HASH_TYPE_MD5"></span><span id="mp_hash_type_md5"></span>**\_ \_ MD5 тип хэша \_**
</dt> <dd>

MD5

</dd> <dt>

<span id="MP_HASH_TYPE_SHA1"></span><span id="mp_hash_type_sha1"></span>**\_SHA1- \_ тип \_ хэша пакета управления**
</dt> <dd>

SHA1

</dd> <dt>

<span id="MP_HASH_TYPE_SHA256"></span><span id="mp_hash_type_sha256"></span>**\_Тип хэша пакета управления \_ \_ SHA256**
</dt> <dd>

SHA 256

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Минимальная версия клиента<br/> | \[Только классические приложения Windows 8\]<br/>                                            |
| Минимальная версия сервера<br/> | \[Только для настольных приложений Windows Server 2012\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Мпклиент. h</dt> </dl> |



 

 





