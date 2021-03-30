---
description: КАБИНЕТДЛЛВЕРСИОНИНФО содержит сведения о версии для Cabinet.dll.
ms.assetid: 1dc6962c-3087-4f56-8b65-fbf55e17eeb6
title: Структура КАБИНЕТДЛЛВЕРСИОНИНФО
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CABINETDLLVERSIONINFO
api_type:
- NA
api_location: ''
ms.openlocfilehash: b6dfcd68f1bc684554d45feb13b9976465b70efa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/07/2021
ms.locfileid: "103895777"
---
# <a name="cabinetdllversioninfo-structure"></a>Структура КАБИНЕТДЛЛВЕРСИОНИНФО

\[Эта структура содержит сведения, необходимые только при использовании функции **дллжетверсион** , которая не поддерживается. Эта документация предоставляется только в ознакомительных целях.\]

**Кабинетдллверсионинфо** содержит сведения о версии для Cabinet.dll.

## <a name="syntax"></a>Синтаксис


```C++
typedef struct {
  DWORD cbStruct;
  DWORD dwReserved1;
  DWORD dwReserved2;
  DWORD dwFileVersionMS;
  DWORD dwFileVersionLS;
} CABINETDLLVERSIONINFO, *PCABINETDLLVERSIONINFO;
```



## <a name="members"></a>Члены

<dl> <dt>

**кбструкт**
</dt> <dd>

Размер этой структуры в байтах.

</dd> <dt>

**dwReserved1**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**dwReserved2**
</dt> <dd>

Зарезервировано.

</dd> <dt>

**двфилеверсионмс**
</dt> <dd>

Содержит наиболее значимые биты сведений о версии. Биты 0-15 содержат дополнительный номер версии, а BITS 16-31 содержит основную версию.

</dd> <dt>

**двфилеверсионлс**
</dt> <dd>

Содержит наименьшие значащие биты сведений о версии. Биты 0-15 содержат номер редакции, а BITS 16-31 содержит номер сборки.

</dd> </dl>

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**дллжетверсион**](dllgetversion.md)
</dt> </dl>

 

 



