---
description: Описывает разрешение теневого буфера z, которое будет использоваться в моделировании предварительно вычисленных Радианце (PRT) с прямым освещением на GPU.
ms.assetid: 05354328-9b6f-45f5-a913-47ede170b03f
title: Перечисление D3DXSHGPUSIMOPT (D3dx9mesh. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXSHGPUSIMOPT
api_type:
- HeaderDef
api_location:
- d3dx9mesh.h
ms.openlocfilehash: a73323dc9d6596f848fa50fe6dc21e236a5b9f2d4362b3c2a27cf773d3939fac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119849754"
---
# <a name="d3dxshgpusimopt-enumeration"></a>Перечисление D3DXSHGPUSIMOPT

Описывает разрешение теневого буфера z, которое будет использоваться в моделировании предварительно вычисленных Радианце (PRT) с прямым освещением на GPU. Можно также задать z-буфер более высокого качества, чтобы уменьшить шум в результатах имитации прямого освещения, хотя моделирование будет выполняться медленнее.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DXSHGPUSIMOPT { 
  D3DXSHGPUSIMOPT_SHADOWRES256   = 1,
  D3DXSHGPUSIMOPT_SHADOWRES512   = 0,
  D3DXSHGPUSIMOPT_SHADOWRES1024  = 2,
  D3DXSHGPUSIMOPT_SHADOWRES2048  = 3,
  D3DXSHGPUSIMOPT_HIGHQUALITY    = 4,
  D3DXSHGPUSIMOPT_FORCE_DWORD    = 0x7fffffff
} D3DXSHGPUSIMOPT, *LPD3DXSHGPUSIMOPT;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES256"></span><span id="d3dxshgpusimopt_shadowres256"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES256**
</dt> <dd>

Эмуляция с низким разрешением. В моделировании используется текстура 256 x 256 пикселей для кодирования теневого z-буфера.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES512"></span><span id="d3dxshgpusimopt_shadowres512"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES512**
</dt> <dd>

Эмуляция среднего разрешения. В моделировании используется текстура 512 x 512 пикселей для кодирования теневого z-буфера. Это значение по умолчанию.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES1024"></span><span id="d3dxshgpusimopt_shadowres1024"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES1024**
</dt> <dd>

Имитация высокого разрешения. В моделировании используется текстура 1024 x 1024 пикселей для кодирования теневого z-буфера.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_SHADOWRES2048"></span><span id="d3dxshgpusimopt_shadowres2048"></span>**D3DXSHGPUSIMOPT \_ SHADOWRES2048**
</dt> <dd>

Эмуляция наивысшего разрешения. В моделировании используется текстура 2048 x 2048 пикселей для кодирования теневого z-буфера.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_HIGHQUALITY"></span><span id="d3dxshgpusimopt_highquality"></span>**D3DXSHGPUSIMOPT \_ хигхкуалити**
</dt> <dd>

Модель имеет высокую точность, независимо от выбранного разрешения. Установка этого значения приведет к уменьшению шума в результатах имитации прямого освещения, хотя моделирование будет выполняться медленнее. Может сочетаться с одним из значений разрешения.

</dd> <dt>

<span id="D3DXSHGPUSIMOPT_FORCE_DWORD"></span><span id="d3dxshgpusimopt_force_dword"></span>**D3DXSHGPUSIMOPT \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

Можно указать только одно из значений разрешения, и оно может сочетаться со значением высокого качества.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3dx9mesh. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления D3DX](dx9-graphics-reference-d3dx-enums.md)
</dt> </dl>

 

 




