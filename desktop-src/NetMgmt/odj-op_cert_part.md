---
title: OP_CERT_PART
description: Определение OP_CERT_PART IDL
ms.assetid: 30492801-f26e-447f-bcbf-d1108e7ae524
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: feb4f05171204442085f7d69691aa010d13e6042
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "105719169"
---
# <a name="op_cert_part-structure"></a>Структура OP_CERT_PART

Содержит сериализованные хранилища PFX и сертификатов.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _OP_CERT_PART
{
    ULONG                                       cPfxStores;
    [size_is(cPfxStores)]   POP_CERT_PFX_STORE  pPfxStores;
    ULONG                                       cSstStores;
    [size_is(cSstStores)]   POP_CERT_SST_STORE  pSstStores;
    OP_BLOB                                     Extension;
} OP_CERT_PART, *POP_CERT_PART;
```

## <a name="members"></a>Члены

### <a name="cpfxstores"></a>кпфкссторес

Содержит количество элементов в Ппфкссторес.

### <a name="ppfxstores"></a>ппфкссторес

Содержит массив структур OP_CERT_PFX_STORE.

### <a name="csststores"></a>ксстсторес

Содержит количество элементов в Псстсторес.

### <a name="psststores"></a>псстсторес

Содержит массив структур OP_CERT_SST_STORE.

### <a name="extension"></a>Расширение

Зарезервировано для будущего использования и должно содержать все нули.

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)

[**\_ \_ хранилище PFX CERT \_**](odj-op_cert_pfx_store.md)

[**магазин с OP \_ CERT \_ SST \_**](odj-op_cert_sst_store.md)

[**\_большой двоичный объект Op**](odj-op_blob.md)

