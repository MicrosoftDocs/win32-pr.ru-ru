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
ms.openlocfilehash: 6f912c44659d418d543194ba82a9d82f31e7ef08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713746"
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
| Header<br/> | <dl> <dt>D3dx9anim. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




