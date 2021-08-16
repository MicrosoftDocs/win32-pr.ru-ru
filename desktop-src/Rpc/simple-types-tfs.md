---
title: Простые типы
description: Все простые типы представлены одним символом формата, указывающим тип по имени.
ms.assetid: 77c293a1-70c4-4825-bb2e-de36e01d3abb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e265c24d1eaf4b85ab67c7f8997c656257522bfc8290e73596a8628bdd4215c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925164"
---
# <a name="simple-types"></a>Простые типы

Все простые типы представлены одним символом формата, указывающим тип по имени. Сюда входят все числовые типы и другие специальные типы IDL. Список выглядит следующим образом:

``` syntax
FC_BYTE,                    // 0x01
FC_CHAR,                    // 0x02
FC_SMALL,                   // 0x03
FC_USMALL,                  // 0x04
FC_WCHAR,                   // 0x05
FC_SHORT,                   // 0x06
FC_USHORT,                  // 0x07
FC_LONG,                    // 0x08
FC_ULONG,                   // 0x09
FC_FLOAT,                   // 0x0a
FC_HYPER,                   // 0x0b
FC_DOUBLE,                  // 0x0c
FC_ENUM16,                  // 0x0d
FC_ENUM32,                  // 0x0e
FC_ERROR_STATUS_T,          // 0x10
FC_INT3264,                 // 0xb8
FC_UINT3264,                // 0xb9
```

МАЛЫЕ, WCHAR, HYPER, Status ERROR \_ \_ T, \_ \_ INT3264 Types — это встроенные функции MIDL с особыми интерпретациями RPC. Типы INT и \_ \_ Int32 сопоставляются с \_ длинными, беззнаковыми int и без знака \_ \_ Int32 с FC \_ ulong, \_ \_ Int64 и без знака \_ \_ Int64 в FC \_ Hyper.

\_ \_ Типы INT128, FLOAT128 и FLOAT80 не поддерживаются.

 

 




