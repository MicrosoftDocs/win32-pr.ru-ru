---
title: ODJ_BLOB
description: Определение ODJ_BLOB IDL
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: aa1c2b593e0e9f63a52672eb3b29ee83fbf86ea91d7f4860f2351a8e4538f05d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119779574"
---
# <a name="odj_blob-structure"></a>Структура ODJ_BLOB

Задает структуру, содержащую либо сериализованную ODJ_WIN7BLOB структуру, либо сериализованную OP_PACKAGE структуру.

## <a name="syntax"></a>Синтаксис

```c++
typedef struct _ODJ_BLOB
{
    ULONG ulODJFormat;
    ULONG cbBlob;
    [size_is(cbBlob)] PBYTE pBlob;
} ODJ_BLOB, *PODJ_BLOB;

```

## <a name="members"></a>Члены

### <a name="ulodjformat"></a>улоджформат

Указывает логическую версию структуры и должно иметь одно из следующих значений:

|Значение|Значение|
| --- | --- |
|ODJ_WIN7_FORMAT (0x00000001)|Байты, содержащиеся в Пблоб, должны содержать сериализованную структуру ODJ_WIN7_BLOB.|
|ODJ_WIN8_FORMAT (0x00000002)|Байты, содержащиеся в Пблоб, должны содержать сериализованную структуру OP_PACKAGE.|

### <a name="cbblob"></a>кбблоб

Это значение должно быть равно количеству байтов в массиве Пблоб.

### <a name="pblob"></a>пблоб

Указывает на буфер байтов, содержащий сериализованную структуру, указанную в Улоджформат выше.

## <a name="see-also"></a>См. также

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)

