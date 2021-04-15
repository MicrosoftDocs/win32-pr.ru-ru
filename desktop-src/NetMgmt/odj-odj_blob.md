---
title: ODJ_BLOB
description: Определение ODJ_BLOB IDL
ms.assetid: ada2c597-9ab9-4cc0-b5ba-4b533eec5502
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 079ea531b0cb392539679c10574c0cc0f1601318
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/14/2020
ms.locfileid: "104488481"
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

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)

