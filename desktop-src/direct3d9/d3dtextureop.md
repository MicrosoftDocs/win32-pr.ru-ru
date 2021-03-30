---
description: Определяет операции смешения текстур для каждого этапа.
ms.assetid: 7bfdcb15-c3c3-4e7e-b924-6ecfa350e2f3
title: Перечисление D3DTEXTUREOP (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DTEXTUREOP
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: d35e2d4b65cd41a49d8ed8edb3252295ca3baef3
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104354513"
---
# <a name="d3dtextureop-enumeration"></a>Перечисление D3DTEXTUREOP

Определяет операции смешения текстур для каждого этапа.

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DTEXTUREOP { 
  D3DTOP_DISABLE                    = 1,
  D3DTOP_SELECTARG1                 = 2,
  D3DTOP_SELECTARG2                 = 3,
  D3DTOP_MODULATE                   = 4,
  D3DTOP_MODULATE2X                 = 5,
  D3DTOP_MODULATE4X                 = 6,
  D3DTOP_ADD                        = 7,
  D3DTOP_ADDSIGNED                  = 8,
  D3DTOP_ADDSIGNED2X                = 9,
  D3DTOP_SUBTRACT                   = 10,
  D3DTOP_ADDSMOOTH                  = 11,
  D3DTOP_BLENDDIFFUSEALPHA          = 12,
  D3DTOP_BLENDTEXTUREALPHA          = 13,
  D3DTOP_BLENDFACTORALPHA           = 14,
  D3DTOP_BLENDTEXTUREALPHAPM        = 15,
  D3DTOP_BLENDCURRENTALPHA          = 16,
  D3DTOP_PREMODULATE                = 17,
  D3DTOP_MODULATEALPHA_ADDCOLOR     = 18,
  D3DTOP_MODULATECOLOR_ADDALPHA     = 19,
  D3DTOP_MODULATEINVALPHA_ADDCOLOR  = 20,
  D3DTOP_MODULATEINVCOLOR_ADDALPHA  = 21,
  D3DTOP_BUMPENVMAP                 = 22,
  D3DTOP_BUMPENVMAPLUMINANCE        = 23,
  D3DTOP_DOTPRODUCT3                = 24,
  D3DTOP_MULTIPLYADD                = 25,
  D3DTOP_LERP                       = 26,
  D3DTOP_FORCE_DWORD                = 0x7fffffff
} D3DTEXTUREOP, *LPD3DTEXTUREOP;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DTOP_DISABLE"></span><span id="d3dtop_disable"></span>**\_Отключение D3DTOP**
</dt> <dd>

Отключает вывод этого этапа текстуры и всех стадий с более высоким индексом. Чтобы отключить сопоставление текстур, установите его в качестве цветовой операции для первой стадии текстуры (этап 0). Операции Alpha не могут быть отключены, если включены цветовые операции. Установка для операции Alpha значения D3DTOP \_ Disable, если включено смешение цветов, приводит к неопределенному поведению.

</dd> <dt>

<span id="D3DTOP_SELECTARG1"></span><span id="d3dtop_selectarg1"></span>**D3DTOP \_ SELECTARG1**
</dt> <dd>

Используйте первый цвет или альфа-параметр этого этапа текстуры в качестве выходных данных в неизмененном виде. Эта операция влияет на аргумент Color при использовании с \_ состоянием этапа текстуры D3DTSS колороп и альфа-аргумент при использовании с D3DTSS \_ алфаоп.

![уравнение этого аргумента (s (RGBA) = arg1)](images/topfrm1.png)

</dd> <dt>

<span id="D3DTOP_SELECTARG2"></span><span id="d3dtop_selectarg2"></span>**D3DTOP \_ SELECTARG2**
</dt> <dd>

Используйте второй цвет или альфа-параметр этого этапа текстуры без изменений в качестве выходных данных. Эта операция влияет на аргумент Color при использовании с \_ состоянием этапа текстуры D3DTSS колороп и альфа-аргумент при использовании с D3DTSS \_ алфаоп.

![уравнение этого аргумента (s (RGBA) = arg2)](images/topfrm2.png)

</dd> <dt>

<span id="D3DTOP_MODULATE"></span><span id="d3dtop_modulate"></span>**D3DTOPная \_ модуляция**
</dt> <dd>

Умножьте компоненты аргументов.

![уравнение операции модуляции (s (RGBA) = arg1 x ARG 2)](images/topfrm3.png)

</dd> <dt>

<span id="D3DTOP_MODULATE2X"></span><span id="d3dtop_modulate2x"></span>**D3DTOP \_ MODULATE2X**
</dt> <dd>

Умножьте компоненты аргументов и переместит продукты влево на 1 бит (что значительно умножает их на 2) для повышения яркости.

![уравнение операции modulate2x (s (RGBA) = (arg1 x ARG 2), затем сдвиг влево 1)](images/topfrm4.png)

</dd> <dt>

<span id="D3DTOP_MODULATE4X"></span><span id="d3dtop_modulate4x"></span>**D3DTOP \_ MODULATE4X**
</dt> <dd>

Умножьте компоненты аргументов и переместит продукты влево на 2 бита (по сути, умножая их на 4) для повышения яркости.

![уравнение операции modulate4x (s (RGBA) = (arg1 x ARG 2), затем сдвиг влево 2)](images/topfrm5.png)

</dd> <dt>

<span id="D3DTOP_ADD"></span><span id="d3dtop_add"></span>**D3DTOP \_ Добавить**
</dt> <dd>

Добавьте компоненты аргументов.

![уравнение операции добавления (s (RGBA) = arg1 + ARG 2)](images/topfrm6.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED"></span><span id="d3dtop_addsigned"></span>**D3DTOP \_ аддсигнед**
</dt> <dd>

Добавьте компоненты аргументов с помощью смещения-0,5, сделав эффективный диапазон значений от-0,5 до 0,5.

![Уравнение для операции добавления подписанного (s (RGBA) = arg1 + ARG 2 – 0,5)](images/topfrm7.png)

</dd> <dt>

<span id="D3DTOP_ADDSIGNED2X"></span><span id="d3dtop_addsigned2x"></span>**D3DTOP \_ ADDSIGNED2X**
</dt> <dd>

Добавьте компоненты аргументов с помощью смещения-0,5 и переместит продукты на левый 1 бит.

![уравнение операции добавления 2x ((s (RGBA) = arg1 + ARG 2-0,5), затем сдвиг влево 1)](images/topfrm8.png)

</dd> <dt>

<span id="D3DTOP_SUBTRACT"></span><span id="d3dtop_subtract"></span>**\_Вычитание D3DTOP**
</dt> <dd>

Вычтите компоненты второго аргумента из значений первого аргумента.

![уравнение операции вычитания (s (RGBA) = arg1-ARG 2)](images/topfrm9.png)

</dd> <dt>

<span id="D3DTOP_ADDSMOOTH"></span><span id="d3dtop_addsmooth"></span>**D3DTOP \_ аддсмус**
</dt> <dd>

Добавьте первый и второй аргументы. затем вычтите свой продукт из суммы.

![уравнение операции добавления сглаживания (s (RGBA) = arg1 + ARG 2 x (1-arg1))](images/topfrm10.png)

</dd> <dt>

<span id="D3DTOP_BLENDDIFFUSEALPHA"></span><span id="d3dtop_blenddiffusealpha"></span>**D3DTOP \_ бленддиффусеалфа**
</dt> <dd>

Линейный переход на эту стадию текстуры с помощью интерполяции альфа-канала из каждой вершины.

![уравнение операции смешения альфа-канала (s (RGBA) = arg1 x альфа + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHA"></span><span id="d3dtop_blendtexturealpha"></span>**D3DTOP \_ блендтекстуреалфа**
</dt> <dd>

Линейное смешение этой стадии текстуры с помощью альфа-канала на этом этапе.

![Формула Альфа-операции смешения текстур (s (RGBA) = arg1 x альфа + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDFACTORALPHA"></span><span id="d3dtop_blendfactoralpha"></span>**D3DTOP \_ блендфакторалфа**
</dt> <dd>

Линейный переход на эту стадию текстуры с помощью скалярного набора альфа-каналов с \_ состоянием отрисовки D3DRS текстурефактор.

![уравнение операции альфа-канала коэффициента смешения (s (RGBA) = arg1 x альфа + ARG 2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_BLENDTEXTUREALPHAPM"></span><span id="d3dtop_blendtexturealphapm"></span>**D3DTOP \_ блендтекстуреалфапм**
</dt> <dd>

Линейное смешение этапа текстуры с использованием предварительно умноженного альфа-канала.

![Уравнение для операции смешения текстур альфа-канала (s (RGBA) = arg1 + ARG 2 x (1-Alpha))](images/topfrm12.png)

</dd> <dt>

<span id="D3DTOP_BLENDCURRENTALPHA"></span><span id="d3dtop_blendcurrentalpha"></span>**D3DTOP \_ блендкурренталфа**
</dt> <dd>

Линейный переход на эту стадию текстуры с использованием альфа-канала, взятого из предыдущей стадии текстуры.

![уравнение текущей Альфа-операции Blend (s (RGBA) = arg1 x альфа + arg2 x (1-Alpha))](images/topfrm11.png)

</dd> <dt>

<span id="D3DTOP_PREMODULATE"></span><span id="d3dtop_premodulate"></span>**D3DTOPная \_ ПОДмодуляция**
</dt> <dd>

\_Предварительная модуляция D3DTOP установлена на этапе n. Выходные данные этапа n — это arg1. Кроме того, если на этапе n + 1 имеется текстура, все D3DTA, \_ текущие в шаге n + 1, предварительно умножаются на текстуру на этапе n + 1.

</dd> <dt>

<span id="D3DTOP_MODULATEALPHA_ADDCOLOR"></span><span id="d3dtop_modulatealpha_addcolor"></span>**D3DTOP \_ модулатеалфа \_ аддколор**
</dt> <dd>

Модуляция цвета второго аргумента с помощью альфа-канала первого аргумента; Затем добавьте результат в аргумент один. Эта операция поддерживается только для операций с цветами (D3DTSS \_ колороп).

![уравнение операции добавления цветовой модуляции альфа (s (RGBA) = arg1 (RGB) + arg1 (a) x arg2 (RGB))](images/topfrm13.png)

</dd> <dt>

<span id="D3DTOP_MODULATECOLOR_ADDALPHA"></span><span id="d3dtop_modulatecolor_addalpha"></span>**D3DTOP \_ модулатеколор \_ аддалфа**
</dt> <dd>

Модуляция аргументов; Затем добавьте альфа-канал первого аргумента. Эта операция поддерживается только для операций с цветами (D3DTSS \_ колороп).

![уравнение операции добавления цвета для альфа-модуляции (s (RGBA) = arg1 (RGB) x arg2 (RGB) + arg1 (a))](images/topfrm14.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVALPHA_ADDCOLOR"></span><span id="d3dtop_modulateinvalpha_addcolor"></span>**D3DTOP \_ модулатеинвалфа \_ аддколор**
</dt> <dd>

Аналогично D3DTOP \_ модулатеалфа \_ аддколор, но используйте обратную букву альфа-канала первого аргумента. Эта операция поддерживается только для операций с цветами (D3DTSS \_ колороп).

![уравнение добавления цветовой модуляции обратная альфа-операция (s (RGBA) = (1-arg1 (a)) x arg2 (RGB) + arg1 (RGB))](images/topfrm15.png)

</dd> <dt>

<span id="D3DTOP_MODULATEINVCOLOR_ADDALPHA"></span><span id="d3dtop_modulateinvcolor_addalpha"></span>**D3DTOP \_ модулатеинвколор \_ аддалфа**
</dt> <dd>

Аналогично D3DTOP \_ модулатеколор \_ аддалфа, но используйте инверсию цвета первого аргумента. Эта операция поддерживается только для операций с цветами (D3DTSS \_ колороп).

![Формула операции добавления цвета инверсии альфа-модуляции (s (RGBA) = (1-arg1 (RGB)) x arg2 (RGB) + arg1 (a))](images/topfrm16.png)

</dd> <dt>

<span id="D3DTOP_BUMPENVMAP"></span><span id="d3dtop_bumpenvmap"></span>**D3DTOP \_ бумпенвмап**
</dt> <dd>

Выполняйте сопоставление выпуклости по пикселям, используя карту окружения на следующей стадии текстуры без освещенности. Эта операция поддерживается только для операций с цветами (D3DTSS \_ колороп).

</dd> <dt>

<span id="D3DTOP_BUMPENVMAPLUMINANCE"></span><span id="d3dtop_bumpenvmapluminance"></span>**D3DTOP \_ бумпенвмаплуминанце**
</dt> <dd>

Выполняйте сопоставление выпуклости по пикселям, используя карту окружения на следующей стадии текстуры с яркостью. Эта операция поддерживается только для операций с цветами (D3DTSS \_ колороп).

</dd> <dt>

<span id="D3DTOP_DOTPRODUCT3"></span><span id="d3dtop_dotproduct3"></span>**D3DTOP \_ DOTPRODUCT3**
</dt> <dd>

Модуляция компонентов каждого аргумента как подписанных компонентов, добавление их продуктов; затем реплицирует сумму во все цветовые каналы, включая альфа. Эта операция поддерживается для операций Color и Alpha.

![Формула операции с точкой 3 (s) = arg1 (r) x arg2 (r) + arg1 (g) x arg2 (g) + arg1 (b) x arg2 (b))](images/topfrm17.png)

В DirectX 6 и DirectX 7 при работе с несколькими текстурами указанные выше входные данные сдвигаются вниз (y = x-0,5) перед использованием для имитации подписанных данных, а скалярный результат автоматически переносится в положительные значения и реплицируется во все три выходных канала. Кроме того, обратите внимание, что в качестве цветовой операции альфа-канал просто обновляет компоненты RGB.

Однако в шейдерах DirectX 8,1 можно указать, что выходные данные направляются в. RGB или. a или оба (по умолчанию). В альфа-канале можно также указать отдельную скалярную операцию.

</dd> <dt>

<span id="D3DTOP_MULTIPLYADD"></span><span id="d3dtop_multiplyadd"></span>**D3DTOP \_ мултиплядд**
</dt> <dd>

Выполняет операцию умножения накопления. Он принимает два последних аргумента, умножает их вместе и добавляет их к оставшимся аргументам ввода-вывода и помещает их в результат.

S<sub>RGBA</sub> = arg1 + arg2 \* arg3

</dd> <dt>

<span id="D3DTOP_LERP"></span><span id="d3dtop_lerp"></span>**D3DTOP \_ лерп**
</dt> <dd>

Линейная интерполяция между вторым и третьим исходными аргументами по пропорции, указанной в первом аргументе источника.

S<sub>RGBA</sub> = (arg1) \* arg2 + (1-arg1) \* arg3.

</dd> <dt>

<span id="D3DTOP_FORCE_DWORD"></span><span id="d3dtop_force_dword"></span>**D3DTOP \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Комментарии

Элементы этого типа используются при задании цветов или альфа-операций с помощью \_ значений D3DTSS колороп или D3DTSS \_ алфаоп с помощью метода [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate) .

В приведенных выше формулах<sub>RGBA</sub> — это цвет RGBA, созданный операцией текстуры, а arg1, arg2 и arg3 — полный цвет RGBA для аргументов текстуры. Отдельные компоненты аргумента отображаются с помощью индексов. Например, альфа-компонент для аргумента 1 будет показан как arg1<sub>A</sub>.

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)
</dt> </dl>

 

 
