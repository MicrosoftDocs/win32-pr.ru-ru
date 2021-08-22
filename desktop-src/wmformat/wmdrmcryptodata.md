---
title: Структура Вмдрмкриптодата (Вмдрмсдк. h)
description: Структура Вмдрмкриптодата содержит сведения о алгоритме шифрования, который используется для шифрования и расшифровки содержимого.
ms.assetid: ad14c6d3-4305-47c0-8f67-7ef6d11cc326
keywords:
- Формат Windows Media структура Вмдрмкриптодата
- структура формат мультимедиа Windows
topic_type:
- apiref
api_name:
- WMDRMCryptoData
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a732b7c1c4a4ca8d664255d39573b10ac1bdd4d004deb73d723a43b55db70ee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119083808"
---
# <a name="wmdrmcryptodata-structure"></a>Структура Вмдрмкриптодата

Структура **вмдрмкриптодата** содержит сведения о алгоритме шифрования, который используется для шифрования и расшифровки содержимого.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct WMDRMCryptoData {
  DRM_CRYPTO_TYPE  cryptoType;
  unsigned __int64 qwCounterID;
  unsigned __int64 qwOffset;
} ;
```



## <a name="members"></a>Члены

<dl> <dt>

**криптотипе**
</dt> <dd>

Член перечисления [**\_ \_ типа шифрования DRM**](drm-crypto-type.md) , указывающий тип алгоритма шифрования.

</dd> <dt>

**квкаунтерид**
</dt> <dd>

Старшие 64 бит в режиме счетчика 128-разрядного AES. Этот элемент используется только в том случае  , если для элемента криптотипе **задан \_ тип шифрования \_ MCE**.

</dd> <dt>

**квоффсет**
</dt> <dd>

Младшие 64 бит 128-разрядного режима счетчика AES. Этот элемент используется только в том случае  , если для элемента криптотипе **задан \_ тип шифрования \_ MCE**.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Вмдрмсдк. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Структуры**](drm-structures.md)
</dt> </dl>

 

 





