---
title: OP_CERT_SST_STORE
description: Определение OP_CERT_SST_STORE IDL
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 294d21d730e1cce478088cddb43686706217ec5b
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/18/2020
ms.locfileid: "104414309"
---
# <a name="op_cert_sst_store-structure"></a>Структура OP_CERT_SST_STORE

Содержит сериализованное хранилище сертификатов.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _OP_CERT_SST_STORE
{
    ULONG                       StoreLocation;
    [string] wchar_t            *pStoreName;
    ULONG                       cbSst;
    [size_is(cbSst)]    PBYTE   pSst;
} OP_CERT_SST_STORE, *POP_CERT_SST_STORE;
```

## <a name="members"></a>Члены

### <a name="storelocation"></a>StoreLocation

Содержит идентификатор для хранилища сертификатов из [**расположений системных хранилищ**](../seccrypto/system-store-locations.md).

### <a name="pstorename"></a>псторенаме

Содержит имя хранилища.

### <a name="cbsst"></a>кбсст

Содержит размер ПССТ в байтах.

### <a name="psst"></a>псст

Содержит сериализованное хранилище сертификатов (см. [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)