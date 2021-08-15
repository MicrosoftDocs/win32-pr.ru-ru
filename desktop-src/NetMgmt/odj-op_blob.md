---
title: OP_BLOB
description: Определение OP_BLOB IDL
ms.assetid: c215c793-5fad-4baa-97c0-c809040dda1e
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 757df1549d1bdb0a9a87ee22373a1903a034a1e267d087d51dac46bb6bc5a762
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "117796894"
---
# <a name="op_blob-structure"></a>Структура OP_BLOB

Содержит непрозрачный байтовый буфер.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _OP_BLOB
{
    ULONG                       cbBlob;
    [size_is(cbBlob)]   PBYTE   pBlob;
} OP_BLOB, *POP_BLOB;
```

## <a name="members"></a>Члены

### <a name="cbblob"></a>кбблоб

Задает размер Пблоб в байтах.

### <a name="pblob"></a>пблоб

Указывает на буфер байтов.

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)
