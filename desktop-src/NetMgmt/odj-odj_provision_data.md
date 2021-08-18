---
title: ODJ_PROVISION_DATA
description: Определение ODJ_PROVISION_DATA IDL
ms.assetid: ff623d04-ad3f-4846-b9de-aaa280713018
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 02762a80be9bd60b7f9c8648c9bfb848f3d76184f249567c9e9522189692e0e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119064354"
---
# <a name="odj_provision_data-structure"></a>Структура ODJ_PROVISION_DATA

Задает внешнюю структуру сериализации, используемую API-интерфейсами автономного присоединение к домену.

## <a name="syntax"></a>Синтаксис

```C++
typedef struct _ODJ_PROVISION_DATA
{
    ULONG ulVersion;
    ULONG ulcBlobs;
    [size_is(ulcBlobs)] PODJ_BLOB pBlobs;
} ODJ_PROVISION_DATA;
```

## <a name="members"></a>Члены

### <a name="ulversion"></a>улверсион

Это значение должно быть равно 1.

### <a name="ulcblobs"></a>улкблобс

Это значение должно быть равно количеству элементов в массиве Пблобс.

### <a name="pblobs"></a>пблобс

Указывает на массив структур ODJ_BLOB.

## <a name="see-also"></a>См. также раздел

[**Определения IDL для автономного присоединение к домену**](odj-idl.md)

[**\_большой двоичный объект ODJ**](odj-odj_blob.md)


