---
description: Определяет режим сжатия, используемый для хранения данных сжатого набора анимации.
ms.assetid: 41592b71-52ba-4727-a885-fb10fc23c5f8
title: Перечисление D3DXCOMPRESSION_FLAGS (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCOMPRESSION_FLAGS
api_type:
- HeaderDef
api_location:
- d3dx9anim.h
ms.openlocfilehash: a4d1e19e2e6fb8e0625b20c7755b3cf3b5c68c06cbc01da1b8a22fd9893d0027
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118300002"
---
# <a name="d3dxcompression_flags-enumeration"></a>\_Перечисление флагов D3DXCOMPRESSION

Определяет режим сжатия, используемый для хранения данных сжатого набора анимации.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXCOMPRESSION_FLAGS { 
  D3DXCOMPRESS_DEFAULT      = 0,
  D3DXCOMPRESS_STRONG       = 1,
  D3DXCOMPRESS_FORCE_DWORD  = 0x7fffffff
} D3DXCOMPRESSION_FLAGS, *LPD3DXCOMPRESSION_FLAGS;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXCOMPRESS_DEFAULT"></span><span id="d3dxcompress_default"></span>**D3DXCOMPRESS \_ по умолчанию**
</dt> <dd>

Реализует быстрое сжатие.

</dd> <dt>

<span id="D3DXCOMPRESS_STRONG"></span><span id="d3dxcompress_strong"></span>**D3DXCOMPRESS \_ strong**
</dt> <dd>

Реализует низкую степень сжатия. Как правило, улучшается качество сжатой анимации, чем при \_ использовании D3DXCOMPRESS по умолчанию.

</dd> <dt>

<span id="D3DXCOMPRESS_FORCE_DWORD"></span><span id="d3dxcompress_force_dword"></span>**D3DXCOMPRESS \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




