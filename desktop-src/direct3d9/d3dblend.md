---
description: Определяет поддерживаемый режим смешения.
ms.assetid: 60ff384c-15a0-4c6f-9e2c-59fdea76b7a1
title: Перечисление D3DBLEND (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBLEND
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 55edb432913720f58860d4f5cb87d8da9b9a8681
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343389"
---
# <a name="d3dblend-enumeration"></a>Перечисление D3DBLEND

Определяет поддерживаемый режим смешения.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DBLEND { 
  D3DBLEND_ZERO             = 1,
  D3DBLEND_ONE              = 2,
  D3DBLEND_SRCCOLOR         = 3,
  D3DBLEND_INVSRCCOLOR      = 4,
  D3DBLEND_SRCALPHA         = 5,
  D3DBLEND_INVSRCALPHA      = 6,
  D3DBLEND_DESTALPHA        = 7,
  D3DBLEND_INVDESTALPHA     = 8,
  D3DBLEND_DESTCOLOR        = 9,
  D3DBLEND_INVDESTCOLOR     = 10,
  D3DBLEND_SRCALPHASAT      = 11,
  D3DBLEND_BOTHSRCALPHA     = 12,
  D3DBLEND_BOTHINVSRCALPHA  = 13,
  D3DBLEND_BLENDFACTOR      = 14,
  D3DBLEND_INVBLENDFACTOR   = 15,
  D3DBLEND_SRCCOLOR2        = 16,
  D3DBLEND_INVSRCCOLOR2     = 17,
  D3DBLEND_FORCE_DWORD      = 0x7fffffff
} D3DBLEND, *LPD3DBLEND;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DBLEND_ZERO"></span><span id="d3dblend_zero"></span>**D3DBLEND \_ 0**
</dt> <dd>

Коэффициент смешения равен (0, 0, 0, 0).

</dd> <dt>

<span id="D3DBLEND_ONE"></span><span id="d3dblend_one"></span>**D3DBLEND \_ один**
</dt> <dd>

Коэффициент смешения равен (1, 1, 1, 1).

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR"></span><span id="d3dblend_srccolor"></span>**D3DBLEND \_ сркколор**
</dt> <dd>

Коэффициент смешения — (RS, GS, BS, AS).

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR"></span><span id="d3dblend_invsrccolor"></span>**D3DBLEND \_ инвсркколор**
</dt> <dd>

Коэффициент смешения — (1-RS, 1-GS, 1-BS, 1 — как).

</dd> <dt>

<span id="D3DBLEND_SRCALPHA"></span><span id="d3dblend_srcalpha"></span>**D3DBLEND \_ сркалфа**
</dt> <dd>

Коэффициент смешения равен (как, как, как).

</dd> <dt>

<span id="D3DBLEND_INVSRCALPHA"></span><span id="d3dblend_invsrcalpha"></span>**D3DBLEND \_ инвсркалфа**
</dt> <dd>

Коэффициент смешения равен (1-как, 1-как, 1-как, 1 — как).

</dd> <dt>

<span id="D3DBLEND_DESTALPHA"></span><span id="d3dblend_destalpha"></span>**D3DBLEND \_ десталфа**
</dt> <dd>

Коэффициент смешения — (<sub>a d a</sub> d<sub></sub> a d<sub>).</sub><sub></sub>

</dd> <dt>

<span id="D3DBLEND_INVDESTALPHA"></span><span id="d3dblend_invdestalpha"></span>**D3DBLEND \_ инвдесталфа**
</dt> <dd>

Коэффициент смешения — (1-A<sub>d</sub> 1 —<sub>a d 1</sub> -<sub>a d</sub> <sub>).</sub>

</dd> <dt>

<span id="D3DBLEND_DESTCOLOR"></span><span id="d3dblend_destcolor"></span>**D3DBLEND \_ дестколор**
</dt> <dd>

Коэффициент смешения — (R<sub>d</sub>, G<sub>d</sub>, B<sub>d</sub>, A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_INVDESTCOLOR"></span><span id="d3dblend_invdestcolor"></span>**D3DBLEND \_ инвдестколор**
</dt> <dd>

Коэффициент смешения равен (1-R<sub>d</sub>, 1-G<sub>d</sub>, 1-B<sub>d</sub>, 1-A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_SRCALPHASAT"></span><span id="d3dblend_srcalphasat"></span>**D3DBLEND \_ сркалфасат**
</dt> <dd>

Коэффициент смешения — (f, f, f, 1); где f = min (как, 1-A<sub>d</sub>).

</dd> <dt>

<span id="D3DBLEND_BOTHSRCALPHA"></span><span id="d3dblend_bothsrcalpha"></span>**D3DBLEND \_ боссркалфа**
</dt> <dd>

**Устарел**. Начиная с версии DirectX 6, можно добиться того же результата, установив для исходных и целевых коэффициентов смешения D3DBLEND \_ сркалфа и D3DBLEND \_ инвсркалфа в отдельных вызовах.

</dd> <dt>

<span id="D3DBLEND_BOTHINVSRCALPHA"></span><span id="d3dblend_bothinvsrcalpha"></span>**D3DBLEND \_ босинвсркалфа**
</dt> <dd>

**Устарел**. Коэффициент смешения исходного кода равен (1-как, 1-как, 1-как, 1 — как), а целевой коэффициент смешения — (AS, AS, AS); Выбор назначения Blend переопределяется. Этот режим наложения поддерживается только для \_ состояния отрисовки D3DRS сркбленд.

</dd> <dt>

<span id="D3DBLEND_BLENDFACTOR"></span><span id="d3dblend_blendfactor"></span>**D3DBLEND \_ блендфактор**
</dt> <dd>

Постоянный коэффициент смешения цветов, используемый средством смешения буферов кадров. Этот режим наложения поддерживается, только если D3DPBLENDCAPS \_ блендфактор задан в **Сркблендкапс** или **дестблендкапс** членах [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

<span id="D3DBLEND_INVBLENDFACTOR"></span><span id="d3dblend_invblendfactor"></span>**D3DBLEND \_ инвблендфактор**
</dt> <dd>

Инвертированный коэффициент смешения цветов, используемый средством смешения буферов кадров. Этот режим наложения поддерживается только в том случае, если \_ бит БЛЕНДФАКТОР D3DPBLENDCAPS установлен в **Сркблендкапс** или **дестблендкапс** членов [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9).

</dd> <dt>

<span id="D3DBLEND_SRCCOLOR2"></span><span id="d3dblend_srccolor2"></span>**D3DBLEND \_ SRCCOLOR2**
</dt> <dd>

Коэффициент смешения равен (Псаутколор \[ 1 \] <sub>r</sub>, псаутколор \[ 1 \] <sub>g</sub>, псаутколор \[ 1 \] <sub>b</sub>, не используется). См. раздел [наложение целевого объекта прорисовки](#render-target-blending).

Различия между Direct3D 9 и Direct3D 9Ex:

- Этот флаг доступен только в Direct3D 9Ex.



 

</dd> <dt>

<span id="D3DBLEND_INVSRCCOLOR2"></span><span id="d3dblend_invsrccolor2"></span>**D3DBLEND \_ INVSRCCOLOR2**
</dt> <dd>

Коэффициент смешения равен (1-Псаутколор \[ 1 \] <sub>r</sub>, 1-псаутколор \[ 1 \] <sub>g</sub>, 1-псаутколор \[ 1 \] <sub>b</sub>, не используется)). См. раздел [наложение целевого объекта прорисовки](#render-target-blending).


Различия между Direct3D 9 и Direct3D 9Ex:

- Этот флаг доступен только в Direct3D 9Ex.



 

</dd> <dt>

<span id="D3DBLEND_FORCE_DWORD"></span><span id="d3dblend_force_dword"></span>**D3DBLEND \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks

В приведенных выше описаниях элементов значения RGBA источника и назначения обозначаются подстрочными индексами s и d.

Значения в этом перечислимом типе используются в следующих состояниях рендеринга:

-   D3DRS \_ дестбленд
-   D3DRS \_ сркбленд
-   D3DRS \_ дестблендалфа
-   D3DRS \_ сркблендалфа

См. [ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)

### <a name="render-target-blending"></a>Наложение целевого объекта прорисовки

В Direct3D 9Ex улучшены возможности отрисовки текста. Для отрисовки шрифтов с четким типом обычно требуется два прохода. Чтобы устранить второй проход, можно использовать шейдер пикселей для вывода двух цветов, которые можно вызвать Псаутколор \[ 0 \] и псаутколор \[ 1 \] . Первый цвет будет содержать стандартные 3 цветовых компонента (RGB). Второй цвет будет содержать три альфа-компонента (по одному для каждого компонента первого цвета).

Эти новые режимы наложения используются только для отрисовки текста на первом объекте отрисовки.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> </dl>

 

 
