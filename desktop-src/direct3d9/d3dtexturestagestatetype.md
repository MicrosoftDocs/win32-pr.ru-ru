---
description: Состояния этапов текстуры определяют операции текстуры с несколькими операциями смешения.
ms.assetid: 87a5a1bb-e748-4c72-8320-ea82250dcc0e
title: Перечисление D3DTEXTURESTAGESTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTURESTAGESTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0530f428c9ebf89607fa89509c65ddd336fee293
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273743"
---
# <a name="d3dtexturestagestatetype-enumeration"></a>Перечисление D3DTEXTURESTAGESTATETYPE

Состояния этапов текстуры определяют операции текстуры с несколькими операциями смешения. Некоторые состояния образца настроили обработку вершин и некоторые настройки обработки пикселей. Состояния стадии текстуры можно сохранить и восстановить с помощью статеблоккс (см. раздел [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DTEXTURESTAGESTATETYPE { 
  D3DTSS_COLOROP                = 1,
  D3DTSS_COLORARG1              = 2,
  D3DTSS_COLORARG2              = 3,
  D3DTSS_ALPHAOP                = 4,
  D3DTSS_ALPHAARG1              = 5,
  D3DTSS_ALPHAARG2              = 6,
  D3DTSS_BUMPENVMAT00           = 7,
  D3DTSS_BUMPENVMAT01           = 8,
  D3DTSS_BUMPENVMAT10           = 9,
  D3DTSS_BUMPENVMAT11           = 10,
  D3DTSS_TEXCOORDINDEX          = 11,
  D3DTSS_BUMPENVLSCALE          = 22,
  D3DTSS_BUMPENVLOFFSET         = 23,
  D3DTSS_TEXTURETRANSFORMFLAGS  = 24,
  D3DTSS_COLORARG0              = 26,
  D3DTSS_ALPHAARG0              = 27,
  D3DTSS_RESULTARG              = 28,
  D3DTSS_CONSTANT               = 32,
  D3DTSS_FORCE_DWORD            = 0x7fffffff
} D3DTEXTURESTAGESTATETYPE, *LPD3DTEXTURESTAGESTATETYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DTSS_COLOROP"></span><span id="d3dtss_colorop"></span>**D3DTSS \_ колороп**
</dt> <dd>

Состояние стадии текстуры — это операция смешения цветов текстуры, определяемая одним элементом перечисляемого типа [**D3DTEXTUREOP**](./d3dtextureop.md) . Значение по умолчанию для первой стадии текстуры (Стадия 0) — D3DTOP \_ модуляция, для всех остальных этапов значение по умолчанию — D3DTOP \_ disable.

</dd> <dt>

<span id="D3DTSS_COLORARG1"></span><span id="d3dtss_colorarg1"></span>**D3DTSS \_ COLORARG1**
</dt> <dd>

Состояние стадии текстуры — это первый аргумент цвета для этапа, идентифицируемый одним из [D3DTA](d3dta.md). Аргументом по умолчанию является D3DTA \_ текстура.

Укажите D3DTA \_ TEMP, чтобы выбрать временный цвет регистра для чтения или записи. D3DTA \_ TEMP поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп. По умолчанию регистр имеет значение (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_COLORARG2"></span><span id="d3dtss_colorarg2"></span>**D3DTSS \_ COLORARG2**
</dt> <dd>

Состояние этапа текстуры — это второй цветовой аргумент для этапа, идентифицируемый [D3DTA](d3dta.md). Аргумент по умолчанию — D3DTA \_ Current. Укажите D3DTA \_ TEMP, чтобы выбрать временный цвет регистра для чтения или записи. D3DTA \_ TEMP поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп. По умолчанию регистр имеет значение (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAOP"></span><span id="d3dtss_alphaop"></span>**D3DTSS \_ алфаоп**
</dt> <dd>

Состояние стадии текстуры — это операция смешения текстур, определяемая одним членом перечисляемого типа [**D3DTEXTUREOP**](./d3dtextureop.md) . Значение по умолчанию для первой стадии текстуры (Стадия 0) — D3DTOP \_ SELECTARG1, а для всех остальных этапов значение по умолчанию — D3DTOP \_ disable.

</dd> <dt>

<span id="D3DTSS_ALPHAARG1"></span><span id="d3dtss_alphaarg1"></span>**D3DTSS \_ ALPHAARG1**
</dt> <dd>

Состояние этапа текстуры — это первый альфа-аргумент для этапа, идентифицируемый по [D3DTA](d3dta.md). Аргументом по умолчанию является D3DTA \_ текстура. Если для этого этапа не задана текстура, аргументом по умолчанию является D3DTA \_ диффузия. Укажите D3DTA \_ TEMP, чтобы выбрать временный цвет регистра для чтения или записи. D3DTA \_ TEMP поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп. По умолчанию регистр имеет значение (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG2"></span><span id="d3dtss_alphaarg2"></span>**D3DTSS \_ ALPHAARG2**
</dt> <dd>

Состояние этапа текстуры — это второй альфа-аргумент для этапа, идентифицируемый по [D3DTA](d3dta.md). Аргумент по умолчанию — D3DTA \_ Current. Укажите D3DTA \_ TEMP, чтобы выбрать временный цвет регистра для чтения или записи. D3DTA \_ TEMP поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп. По умолчанию регистр имеет значение (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT00"></span><span id="d3dtss_bumpenvmat00"></span>**D3DTSS \_ BUMPENVMAT00**
</dt> <dd>

Состояние этапа текстуры — это значение с плавающей запятой для \[ \] \[ \] коэффициента 0 0 в матрице сопоставления выпуклости. Значение по умолчанию — 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT01"></span><span id="d3dtss_bumpenvmat01"></span>**D3DTSS \_ BUMPENVMAT01**
</dt> <dd>

Состояние этапа текстуры — это значение с плавающей запятой для \[ \] \[ \] коэффициента 0 1 в матрице сопоставления выпуклости. Значение по умолчанию — 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT10"></span><span id="d3dtss_bumpenvmat10"></span>**D3DTSS \_ BUMPENVMAT10**
</dt> <dd>

Состояние этапа текстуры — это значение с плавающей запятой для \[ \] \[ \] коэффициента 1 0 в матрице сопоставления выпуклости. Значение по умолчанию — 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVMAT11"></span><span id="d3dtss_bumpenvmat11"></span>**D3DTSS \_ BUMPENVMAT11**
</dt> <dd>

Состояние этапа текстуры — это значение с плавающей запятой для \[ \] \[ \] коэффициента 1 1 в матрице сопоставления выпуклости. Значение по умолчанию — 0,0.

</dd> <dt>

<span id="D3DTSS_TEXCOORDINDEX"></span><span id="d3dtss_texcoordindex"></span>**D3DTSS \_ текскурдиндекс**
</dt> <dd>

Индекс набора координат текстуры для использования с этой стадией текстуры. Для каждой вершины можно указать до восьми наборов координат текстуры. Если вершина не включает набор координат текстуры по указанному индексу, система по умолчанию использует координаты, заданные вами и v (0, 0).

При подготовке к просмотру с помощью шейдеров вершин в каждом из индексов координат текстуры каждого этапа должно быть задано значение по умолчанию. Индекс по умолчанию для каждого этапа равен индексу этапа. Присвойте этому состоянию Отсчитываемый от нуля индекс набора координат для каждой вершины, используемой этой стадией текстуры.

Кроме того, приложения могут включать в качестве логического или с заданным индексом одну из констант для запроса, что Direct3D автоматически создает координаты входной текстуры для преобразования текстур. Список всех констант см. в разделе [D3DTSS \_ тЦи](d3dtss-tci.md).

За исключением D3DTSS \_ тЦи \_ PassThru, который разрешается в ноль, если любое из следующих значений включено в заданный индекс, система использует индекс строго для определения режима переноса текстур. Эти флаги наиболее полезны при выполнении сопоставления среды.

</dd> <dt>

<span id="D3DTSS_BUMPENVLSCALE"></span><span id="d3dtss_bumpenvlscale"></span>**D3DTSS \_ бумпенвлскале**
</dt> <dd>

Значение масштаба с плавающей запятой для светимости схемы выпуклости. Значение по умолчанию — 0,0.

</dd> <dt>

<span id="D3DTSS_BUMPENVLOFFSET"></span><span id="d3dtss_bumpenvloffset"></span>**D3DTSS \_ бумпенвлоффсет**
</dt> <dd>

Значение смещения с плавающей точкой для светимости схемы выпуклости. Значение по умолчанию — 0,0.

</dd> <dt>

<span id="D3DTSS_TEXTURETRANSFORMFLAGS"></span><span id="d3dtss_texturetransformflags"></span>**D3DTSS \_ текстуретрансформфлагс**
</dt> <dd>

Член перечисляемого типа [**D3DTEXTURETRANSFORMFLAGS**](./d3dtexturetransformflags.md) , который управляет преобразованием координат текстуры для этой стадии текстуры. Значение по умолчанию — D3DTTFF \_ disable.

</dd> <dt>

<span id="D3DTSS_COLORARG0"></span><span id="d3dtss_colorarg0"></span>**D3DTSS \_ COLORARG0**
</dt> <dd>

Параметры для третьего операнда цвета для операций триадик (умножение, Добавление и линейная интерполяция), идентифицируемые [D3DTA](d3dta.md). Этот параметр поддерживается, если имеются \_ возможности устройства D3DTEXOPCAPS мултиплядд или D3DTEXOPCAPS \_ лерп. Аргумент по умолчанию — D3DTA \_ Current. Укажите D3DTA \_ TEMP, чтобы выбрать временный цвет регистра для чтения или записи. D3DTA \_ TEMP поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп. По умолчанию регистр имеет значение (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_ALPHAARG0"></span><span id="d3dtss_alphaarg0"></span>**D3DTSS \_ ALPHAARG0**
</dt> <dd>

Параметры для операнда выбора альфа-канала для операций триадик (умножение, Добавление и линейная интерполяция), идентифицируемые [D3DTA](d3dta.md). Этот параметр поддерживается, если имеются \_ возможности устройства D3DTEXOPCAPS мултиплядд или D3DTEXOPCAPS \_ лерп. Аргумент по умолчанию — D3DTA \_ Current. Укажите D3DTA \_ TEMP, чтобы выбрать временный цвет регистра для чтения или записи. D3DTA \_ TEMP поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп. Аргумент по умолчанию — (0,0, 0,0, 0,0, 0,0).

</dd> <dt>

<span id="D3DTSS_RESULTARG"></span><span id="d3dtss_resultarg"></span>**D3DTSS \_ ресултарг**
</dt> <dd>

Параметр для выбора регистра назначения для результата этого этапа, идентифицируемого [D3DTA](d3dta.md). Это значение можно задать равным D3DTA \_ Current (значение по умолчанию) или D3DTA \_ TEMP, то есть единственный временный регистр, который можно считать на последующие этапы в качестве входного аргумента. Окончательный цвет, передаваемый для смешения тумана и буфера кадров, берется из D3DTA \_ Current, поэтому для последней активной стадии текстуры должно быть задано значение запись в текущее состояние. Этот параметр поддерживается, если \_ имеется возможность устройства D3DPMISCCAPS тссаргтемп.

</dd> <dt>

<span id="D3DTSS_CONSTANT"></span><span id="d3dtss_constant"></span>**\_Константа D3DTSS**
</dt> <dd>

Постоянный цвет для каждого этапа. Чтобы узнать, поддерживает ли устройство постоянную цветовую константу, ознакомьтесь с \_ константой D3DPMISCCAPS перстажеконстант в [D3DPMISCCAPS](d3dpmisccaps.md). Константа D3DTSS \_ используется \_ константой D3DTA. См. [D3DTA](d3dta.md).

</dd> <dt>

<span id="D3DTSS_FORCE_DWORD"></span><span id="d3dtss_force_dword"></span>**D3DTSS \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Члены этого перечислимого типа используются с методами [**IDirect3DDevice9:: жеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate) и [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) для получения и задания значений состояния текстуры.

Допустимый диапазон значений для \_ \_ коэффициентов матрицы D3DTSS BUMPENVMAT00, D3DTSS BUMPENVMAT01, D3DTSS \_ BUMPENVMAT10 и D3DTSS BUMPENVMAT11, которые \_ больше или равны-8,0 и меньше 8,0. Этот диапазон, выраженный в математической нотации, — (-8.0, 8.0).

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: Жеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-gettexturestagestate)
</dt> <dt>

[**IDirect3DDevice9:: Сеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
</dt> </dl>

 

 
