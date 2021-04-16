---
description: Определяет идентификатор GUID, который может использоваться в других шаблонах.
ms.assetid: dbfdd307-310f-4c80-b4aa-f16a81a9a372
title: GUID (DirectX 9)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e83e45d6e993153cf293a2ad55080c74f2e6049d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537226"
---
# <a name="guid-directx-9"></a>GUID (DirectX 9)

Определяет идентификатор GUID, который может использоваться в других шаблонах.

``` syntax
template Guid
{
    < a42790e0-7810-11cf-8f52-0040333594a3 >
    DWORD data1;
    WORD data2;
    WORD data3;
    array UCHAR data4[8];
} 
```

Где параметры вместе формируют формат двоичного хранилища для GUID:

-   файл1 — 32-разрядное целочисленное значение без знака
-   значение файл2 — 16-разрядное целое число без знака
-   data3 — 16-разрядное целочисленное значение без знака
-   data4 — Массив беззнаковых символов

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Шаблоны](dx9-graphics-reference-x-file-format-templates.md)
</dt> </dl>

 

 



