---
description: Состояния отрисовки определяют состояния настройки для всех видов обработки вершин и пикселей.
ms.assetid: 2fd56388-f3bd-409f-876c-ae893840b623
title: Перечисление D3DRENDERSTATETYPE (D3D9Types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DRENDERSTATETYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0a7ad803535032705e6e1bb5456109486c59d190
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343069"
---
# <a name="d3drenderstatetype-enumeration"></a>Перечисление D3DRENDERSTATETYPE

Состояния отрисовки определяют состояния настройки для всех видов обработки вершин и пикселей. Некоторые состояния рендеринга настроили обработку вершин и некоторые настройки обработки пикселей (см. раздел [состояния рендеринга (Direct3D 9)](render-states.md)). Состояния отрисовки можно сохранить и восстановить с помощью статеблоккс (см. раздел [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).

## <a name="syntax"></a>Синтаксис


```C++
typedef enum D3DRENDERSTATETYPE { 
  D3DRS_ZENABLE                     = 7,
  D3DRS_FILLMODE                    = 8,
  D3DRS_SHADEMODE                   = 9,
  D3DRS_ZWRITEENABLE                = 14,
  D3DRS_ALPHATESTENABLE             = 15,
  D3DRS_LASTPIXEL                   = 16,
  D3DRS_SRCBLEND                    = 19,
  D3DRS_DESTBLEND                   = 20,
  D3DRS_CULLMODE                    = 22,
  D3DRS_ZFUNC                       = 23,
  D3DRS_ALPHAREF                    = 24,
  D3DRS_ALPHAFUNC                   = 25,
  D3DRS_DITHERENABLE                = 26,
  D3DRS_ALPHABLENDENABLE            = 27,
  D3DRS_FOGENABLE                   = 28,
  D3DRS_SPECULARENABLE              = 29,
  D3DRS_FOGCOLOR                    = 34,
  D3DRS_FOGTABLEMODE                = 35,
  D3DRS_FOGSTART                    = 36,
  D3DRS_FOGEND                      = 37,
  D3DRS_FOGDENSITY                  = 38,
  D3DRS_RANGEFOGENABLE              = 48,
  D3DRS_STENCILENABLE               = 52,
  D3DRS_STENCILFAIL                 = 53,
  D3DRS_STENCILZFAIL                = 54,
  D3DRS_STENCILPASS                 = 55,
  D3DRS_STENCILFUNC                 = 56,
  D3DRS_STENCILREF                  = 57,
  D3DRS_STENCILMASK                 = 58,
  D3DRS_STENCILWRITEMASK            = 59,
  D3DRS_TEXTUREFACTOR               = 60,
  D3DRS_WRAP0                       = 128,
  D3DRS_WRAP1                       = 129,
  D3DRS_WRAP2                       = 130,
  D3DRS_WRAP3                       = 131,
  D3DRS_WRAP4                       = 132,
  D3DRS_WRAP5                       = 133,
  D3DRS_WRAP6                       = 134,
  D3DRS_WRAP7                       = 135,
  D3DRS_CLIPPING                    = 136,
  D3DRS_LIGHTING                    = 137,
  D3DRS_AMBIENT                     = 139,
  D3DRS_FOGVERTEXMODE               = 140,
  D3DRS_COLORVERTEX                 = 141,
  D3DRS_LOCALVIEWER                 = 142,
  D3DRS_NORMALIZENORMALS            = 143,
  D3DRS_DIFFUSEMATERIALSOURCE       = 145,
  D3DRS_SPECULARMATERIALSOURCE      = 146,
  D3DRS_AMBIENTMATERIALSOURCE       = 147,
  D3DRS_EMISSIVEMATERIALSOURCE      = 148,
  D3DRS_VERTEXBLEND                 = 151,
  D3DRS_CLIPPLANEENABLE             = 152,
  D3DRS_POINTSIZE                   = 154,
  D3DRS_POINTSIZE_MIN               = 155,
  D3DRS_POINTSPRITEENABLE           = 156,
  D3DRS_POINTSCALEENABLE            = 157,
  D3DRS_POINTSCALE_A                = 158,
  D3DRS_POINTSCALE_B                = 159,
  D3DRS_POINTSCALE_C                = 160,
  D3DRS_MULTISAMPLEANTIALIAS        = 161,
  D3DRS_MULTISAMPLEMASK             = 162,
  D3DRS_PATCHEDGESTYLE              = 163,
  D3DRS_DEBUGMONITORTOKEN           = 165,
  D3DRS_POINTSIZE_MAX               = 166,
  D3DRS_INDEXEDVERTEXBLENDENABLE    = 167,
  D3DRS_COLORWRITEENABLE            = 168,
  D3DRS_TWEENFACTOR                 = 170,
  D3DRS_BLENDOP                     = 171,
  D3DRS_POSITIONDEGREE              = 172,
  D3DRS_NORMALDEGREE                = 173,
  D3DRS_SCISSORTESTENABLE           = 174,
  D3DRS_SLOPESCALEDEPTHBIAS         = 175,
  D3DRS_ANTIALIASEDLINEENABLE       = 176,
  D3DRS_MINTESSELLATIONLEVEL        = 178,
  D3DRS_MAXTESSELLATIONLEVEL        = 179,
  D3DRS_ADAPTIVETESS_X              = 180,
  D3DRS_ADAPTIVETESS_Y              = 181,
  D3DRS_ADAPTIVETESS_Z              = 182,
  D3DRS_ADAPTIVETESS_W              = 183,
  D3DRS_ENABLEADAPTIVETESSELLATION  = 184,
  D3DRS_TWOSIDEDSTENCILMODE         = 185,
  D3DRS_CCW_STENCILFAIL             = 186,
  D3DRS_CCW_STENCILZFAIL            = 187,
  D3DRS_CCW_STENCILPASS             = 188,
  D3DRS_CCW_STENCILFUNC             = 189,
  D3DRS_COLORWRITEENABLE1           = 190,
  D3DRS_COLORWRITEENABLE2           = 191,
  D3DRS_COLORWRITEENABLE3           = 192,
  D3DRS_BLENDFACTOR                 = 193,
  D3DRS_SRGBWRITEENABLE             = 194,
  D3DRS_DEPTHBIAS                   = 195,
  D3DRS_WRAP8                       = 198,
  D3DRS_WRAP9                       = 199,
  D3DRS_WRAP10                      = 200,
  D3DRS_WRAP11                      = 201,
  D3DRS_WRAP12                      = 202,
  D3DRS_WRAP13                      = 203,
  D3DRS_WRAP14                      = 204,
  D3DRS_WRAP15                      = 205,
  D3DRS_SEPARATEALPHABLENDENABLE    = 206,
  D3DRS_SRCBLENDALPHA               = 207,
  D3DRS_DESTBLENDALPHA              = 208,
  D3DRS_BLENDOPALPHA                = 209,
  D3DRS_FORCE_DWORD                 = 0x7fffffff
} D3DRENDERSTATETYPE, *LPD3DRENDERSTATETYPE;
```



## <a name="constants"></a>Константы

<dl> <dt>

<span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ зенабле**
</dt> <dd>

Режим буферизации по глубине в виде одного члена перечисляемого типа [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) . Задайте для этого состояния \_ значение D3DZB true, чтобы включить z-буферизацию, D3DZB \_ усев для включения w-Buffering или D3DZB \_ false для отключения буферизации глубины.

Значение по умолчанию для этого состояния рендеринга — D3DZB \_ true, если набор элементов глубины был создан вместе с цепочкой буферов, установив для элемента енаблеаутодепсстенЦил структуры [**\_ параметров D3DPRESENT**](d3dpresent-parameters.md) **значение true**, а D3DZB \_ false в противном случае.

</dd> <dt>

<span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ филлмоде**
</dt> <dd>

Один или несколько элементов перечисляемого типа [**D3DFILLMODE**](./d3dfillmode.md) . Значение по умолчанию — D3DFILL \_ сплошной.

</dd> <dt>

<span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ шадемоде**
</dt> <dd>

Один или несколько элементов перечисляемого типа [**D3DSHADEMODE**](./d3dshademode.md) . Значение по умолчанию — D3DSHADE \_ Гуро.

</dd> <dt>

<span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ звритинабле**
</dt> <dd>

**Значение true** , чтобы разрешить приложению выполнять запись в буфер глубины. Значение по умолчанию — **true**. Этот член позволяет приложению запретить системе обновлять буфер глубины новыми значениями глубины. Если **значение равно false**, сравнение глубины выполняется в соответствии с состоянием отрисовки D3DRS \_ зфунк, предполагая, что буферизация глубины выполняется, но значения глубины не записываются в буфер.

</dd> <dt>

<span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ алфатестенабле**
</dt> <dd>

**Значение true** , чтобы включить тестирование альфа-составляющей для каждого пикселя. Если тест проходит успешно, пиксель обрабатывается буфером кадров. В противном случае вся обработка буфера кадров пропускается для пикселя.

Тестирование выполняется путем сравнения входящего альфа-значения со ссылочным альфа-значением с помощью функции сравнения, предоставляемой \_ состоянием визуализации D3DRS алфафунк. Значение ссылки Alpha определяется значением, заданным для D3DRS \_ алфареф. Дополнительные сведения см. в разделе [Состояние тестирования Alpha (Direct3D 9)](alpha-testing-state.md).

Значение этого параметра по умолчанию равно **false**.

</dd> <dt>

<span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ ластпиксел**
</dt> <dd>

Значение по умолчанию — **true**, что позволяет рисовать последний пиксель в строке. Чтобы запретить Рисование последнего пикселя, присвойте этому параметру значение **false**. Дополнительные сведения см. в разделе [состояние структуры и заливки (Direct3D 9)](outline-and-fill-state.md).

</dd> <dt>

<span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ сркбленд**
</dt> <dd>

Один член перечисляемого типа [**D3DBLEND**](./d3dblend.md) . Значение по умолчанию — D3DBLEND \_ 1.

</dd> <dt>

<span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ дестбленд**
</dt> <dd>

Один член перечисляемого типа [**D3DBLEND**](./d3dblend.md) . Значение по умолчанию — D3DBLEND \_ нуль.

</dd> <dt>

<span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ куллмоде**
</dt> <dd>

Указывает, как исключаются Задние треугольники, если вообще. Для этого параметра можно задать один элемент перечисляемого типа [**D3DCULL**](./d3dcull.md) . Значение по умолчанию — D3DCULL \_ CCW.

</dd> <dt>

<span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ зфунк**
</dt> <dd>

Один член перечисляемого типа [**D3DCMPFUNC**](./d3dcmpfunc.md) . Значение по умолчанию — D3DCMP \_ лессекуал. Этот член позволяет приложению принимать или отклонять пиксель на основе его расстояния от камеры.

Значение глубины пикселя сравнивается со значением в буфере глубины. Если значение глубины пикселя проходит функцию сравнения, пиксель записывается.

Значение глубины записывается в буфер глубины только в том случае, если состояние визуализации равно **true**.

Программы программной прорисовки и многие ускорители оборудования работают быстрее, если тест глубины завершается неудачно, так как нет необходимости отфильтровать и произвести модуляцию текстуры, если пиксель не будет подготовлен к просмотру.

</dd> <dt>

<span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ алфареф**
</dt> <dd>

Значение, указывающее альфа-значение ссылки, по которому проверяются Пиксели при включенном тестировании альфа-канала. Это 8-разрядное значение, помещаемое в младшие 8 бит значения состояния отображения DWORD. Значения могут находиться в диапазоне от 0x00000000 до 0x000000FF. Значение по умолчанию — 0.

</dd> <dt>

<span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ алфафунк**
</dt> <dd>

Один член перечисляемого типа [**D3DCMPFUNC**](./d3dcmpfunc.md) . Значение по умолчанию — D3DCMP \_ Always. Этот член позволяет приложению принимать или отклонять пиксель на основе его альфа-значения.

</dd> <dt>

<span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ дисеренабле**
</dt> <dd>

**Значение true** , чтобы включить Дизеринг. Значение по умолчанию — **FALSE**.

</dd> <dt>

<span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ алфабленденабле**
</dt> <dd>

**Значение true** , чтобы включить прозрачность с альфа-смешением. Значение по умолчанию — **FALSE**.

Тип альфа-смешения определяется с помощью \_ состояний отрисовки D3DRS сркбленд и D3DRS \_ дестбленд.

</dd> <dt>

<span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ фоженабле**
</dt> <dd>

**Значение true** , чтобы включить смешение тумана. Значение по умолчанию — **FALSE**. Дополнительные сведения об использовании смешения тумана см. в разделе [туман](fog.md).

</dd> <dt>

<span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ спекуларенабле**
</dt> <dd>

**Значение true** , чтобы включить отраженные блики. Значение по умолчанию — **FALSE**.

Отраженные блики рассчитываются так, как будто каждая вершина в объекте освещена в источнике объекта. Это дает ожидаемый результат при условии, что объект моделируется по отношению к источнику, а расстояние от светлого к объекту относительно велико. В других случаях результаты считаются неопределенными.

Если для этого элемента задано **значение true**, то отраженный цвет добавляется к базовому цвету после текстуры Cascade, но перед альфа-смешением.

</dd> <dt>

<span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS \_ фогколор**
</dt> <dd>

Значение, тип которого — [**D3DCOLOR**](d3dcolor.md). Значение по умолчанию — 0. Дополнительные сведения о цвете тумана см. в разделе [Цвет тумана (Direct3D 9)](fog-color.md).

</dd> <dt>

<span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ фогтаблемоде**
</dt> <dd>

Формула тумана, используемая для пиксельного тумана. Задайте один из элементов перечисляемого типа [**D3DFOGMODE**](./d3dfogmode.md) . Значение по умолчанию — D3DFOG \_ None. Дополнительные сведения о пиксельном тумане см. в разделе [Pixel туман (Direct3D 9)](pixel-fog.md).

</dd> <dt>

<span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS \_ фогстарт**
</dt> <dd>

Глубина, на которой эффект пиксельного или вершинного тумана начинается для линейного режима тумана. Значение по умолчанию — 0,0 f. Глубина задается в мировом пространстве для вершинного тумана и в пространстве устройства \[ 0,0, 1,0 \] или мировом пространстве для пиксельного тумана. Для пиксельных туманов эти значения находятся в пространстве устройства, когда система использует z для вычислений тумана и мирового пространства, когда в системе используется относительный туман (w-туман). Дополнительные сведения см. в разделе [Параметры тумана (Direct3D 9)](fog-parameters.md) и [глубина по сравнению с Z](pixel-fog.md)-ориентированным глазом.

Значения для этого состояния рендеринга — это значения с плавающей запятой. Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS \_ фоженд**
</dt> <dd>

Глубина, на которой эффекты пиксельного или вершинного тумана заканчиваются линейным режимом тумана. Значение по умолчанию — 1,0 f. Глубина задается в мировом пространстве для вершинного тумана и в пространстве устройства \[ 0,0, 1,0 \] или мировом пространстве для пиксельного тумана. Для пиксельных туманов эти значения находятся в пространстве устройства, когда система использует z для вычислений тумана и в мировом пространстве, когда в системе используется относительный туман (w-туман). Дополнительные сведения см. в разделе [Параметры тумана (Direct3D 9)](fog-parameters.md) и [глубина по сравнению с Z](pixel-fog.md)-ориентированным глазом.

Значения для этого состояния рендеринга — это значения с плавающей запятой. Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS \_ фогденсити**
</dt> <dd>

Плотность тумана для пиксельного или вершинного тумана, используемого в экспоненциальном режиме тумана (D3DFOG \_ EXP и D3DFOG \_ EXP2). Допустимые значения плотности находятся в диапазоне от 0,0 до 1,0. Значение по умолчанию — 1,0. Дополнительные сведения см. в разделе [Параметры тумана (Direct3D 9)](fog-parameters.md).

Значения для этого состояния рендеринга — это значения с плавающей запятой. Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ ранжефоженабле**
</dt> <dd>

**Значение true** , чтобы включить вершинный туман на основе диапазона. Значение по умолчанию — **false**. в этом случае система использует туман на основе глубины. В тумане на основе диапазона расстояние объекта от средства просмотра используется для расчета эффектов тумана, а не глубины объекта (то есть z-координаты) в сцене. В тумане, основанном на диапазоне, все методы тумана работают как обычно, за исключением того, что они используют диапазон, а не глубину в вычислениях.

Диапазон — это правильный фактор, используемый для вычислений тумана, но вместо этого обычно используется глубина, поскольку диапазон занимает много времени. Использование функции Depth для вычисления тумана имеет нежелательное воздействие на изменение фоггинесса периферийных объектов при перемещении средства просмотра. в этом случае глубина изменяется, а диапазон остается постоянным.

Поскольку оборудование в настоящее время не поддерживает туман на основе диапазона, исправление диапазона предлагается только для вершинного тумана.

Дополнительные сведения см. в разделе [вершинный туман (Direct3D 9)](vertex-fog.md).

</dd> <dt>

<span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ стенЦиленабле**
</dt> <dd>

**Значение true** , чтобы включить набор элементов, или **false** , чтобы отключить набор элементов. Значение по умолчанию — **FALSE**. Дополнительные сведения см. в разделе [методы буферизации элементов (Direct3D 9)](stencil-buffer-techniques.md).

</dd> <dt>

<span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ стенЦилфаил**
</dt> <dd>

Операция с набором элементов, выполняемая при сбое теста шаблона. Значения из перечисляемого типа [**D3DSTENCILOP**](./d3dstencilop.md) . Значение по умолчанию — D3DSTENCILOP \_ держитесь.

</dd> <dt>

<span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ стенЦилзфаил**
</dt> <dd>

Операция с набором элементов, которую необходимо выполнить, если тест шаблона прошел успешно и тест глубины (z-Test) завершается сбоем. Значения из перечисляемого типа [**D3DSTENCILOP**](./d3dstencilop.md) . Значение по умолчанию — D3DSTENCILOP \_ держитесь.

</dd> <dt>

<span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ стенЦилпасс**
</dt> <dd>

Операция с набором элементов, которую необходимо выполнить, если пройдены тесты набора элементов и глубины (z). Значения из перечисляемого типа [**D3DSTENCILOP**](./d3dstencilop.md) . Значение по умолчанию — D3DSTENCILOP \_ держитесь.

</dd> <dt>

<span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ стенЦилфунк**
</dt> <dd>

Функция сравнения для теста набора элементов. Значения из перечисляемого типа [**D3DCMPFUNC**](./d3dcmpfunc.md) . Значение по умолчанию — D3DCMP \_ Always.

Функция сравнения используется для сравнения ссылочного значения с записью в буфере набора элементов. Это сравнение применяется только к битам в записи ссылочного значения и буфера трафарета, заданных в маске набора элементов (задается \_ состоянием отрисовки D3DRS стенЦилмаск). Если **значение равно true**, проверка шаблона проходит успешно.

</dd> <dt>

<span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ стенЦилреф**
</dt> <dd>

Значение ссылочного типа int для теста набора элементов. Значение по умолчанию — 0.

</dd> <dt>

<span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ стенЦилмаск**
</dt> <dd>

Маска, применяемая к значению ссылки и записи буфера набора элементов для определения значимых битов для теста набора элементов. Маска по умолчанию — 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ стенЦилвритемаск**
</dt> <dd>

Маска записи, применяемая к значениям, записанным в буфер шаблона. Маска по умолчанию — 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ текстурефактор**
</dt> <dd>

Цвет, используемый для смешения текстур с помощью \_ аргумента D3DTA тфактор текстура-смешения или \_ операции смешения текстур D3DTOP блендфакторалфа. Связанное значение является переменной [**D3DCOLOR**](d3dcolor.md) . Значение по умолчанию — непрозрачный белый (0xFFFFFFFF).

</dd> <dt>

<span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**
</dt> <dd>

Поведение при переносе текстур для нескольких наборов координат текстуры. Допустимые значения для этого состояния рендеринга: D3DWRAPCOORD \_ 0 (или D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (или D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (или D3DWRAP \_ W) и D3DWRAPCOORD \_ 3. Это приводит к тому, что система переносится в направлении первого, второго, третьего и четвертого измерений, которые иногда называют направлениями s, t, r и q для заданной текстуры. Значение по умолчанию для этого состояния рендеринга равно 0 (в всех направлениях отключено обтекание).

</dd> <dt>

<span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS \_ Обрезка**
</dt> <dd>

**Значение true** , чтобы включить примитив, вырезая Direct3D, или **false** , чтобы отключить его. Значение по умолчанию — **true**.

</dd> <dt>

<span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**\_Освещение D3DRS**
</dt> <dd>

**Значение true** , чтобы включить освещение Direct3D, или **false** , чтобы отключить его. Значение по умолчанию — **true**. Правильно освещены только вершины, включающие нормальную вершину. в вершинах, не содержащих обычных, используется точка с координатами 0 во всех вычислениях освещения.

</dd> <dt>

<span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS \_ окружение**
</dt> <dd>

Цвет освещения. Это значение типа [**D3DCOLOR**](d3dcolor.md). Значение по умолчанию — 0.

</dd> <dt>

<span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS \_ фогвертексмоде**
</dt> <dd>

Формула тумана, используемая для вершинного тумана. Задайте для одного члена перечисляемого типа [**D3DFOGMODE**](./d3dfogmode.md) . Значение по умолчанию — D3DFOG \_ None.

</dd> <dt>

<span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ колорвертекс**
</dt> <dd>

**Значение true** , чтобы включить цвет каждой вершины или **значение false** , чтобы отключить его. Значение по умолчанию — **true**. Включение цвета на уровне вершины позволяет системе включать цвет, определенный для отдельных вершин в вычислениях освещения.

Дополнительные сведения см. в следующих состояниях рендеринга:

-   D3DRS \_ диффусематериалсаурце
-   D3DRS \_ спекуларматериалсаурце
-   D3DRS \_ амбиентматериалсаурце
-   D3DRS \_ емиссивематериалсаурце

</dd> <dt>

<span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ локалвиевер**
</dt> <dd>

**Значение true** для включения отражения относительно камеры или **false** для использования ортогональных отраженных светов. Значение по умолчанию — **true**. В приложениях, использующих ортогональную проекцию, должно быть указано **значение false**.

</dd> <dt>

<span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ нормализенормалс**
</dt> <dd>

**Значение true** , чтобы включить автоматическую нормализацию нормалей вершин, или **false** , чтобы отключить ее. Значение по умолчанию — **FALSE**. Включение этой функции приводит к нормализации нормалей вершин для вершин после их преобразования в место на камере, что может потребовать вычислений по времени.

</dd> <dt>

<span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ диффусематериалсаурце**
</dt> <dd>

Источник рассеянного цвета для вычислений освещения. Допустимые значения — члены перечисляемого типа [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . Значение по умолчанию — D3DMCS \_ COLOR1. Значение для этого состояния визуализации используется только в том случае, если \_ для состояния отрисовки D3DRS колорвертекс задано значение **true**.

</dd> <dt>

<span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ спекуларматериалсаурце**
</dt> <dd>

Источник отраженного цвета для вычислений освещения. Допустимые значения — члены перечисляемого типа [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . Значение по умолчанию — D3DMCS \_ COLOR2.

</dd> <dt>

<span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ амбиентматериалсаурце**
</dt> <dd>

Источник внешнего цвета для вычислений освещения. Допустимые значения — члены перечисляемого типа [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . Значение по умолчанию — D3DMCS \_ Material.

</dd> <dt>

<span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ емиссивематериалсаурце**
</dt> <dd>

Источник цвета эмиссионный для вычислений освещения. Допустимые значения — члены перечисляемого типа [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) . Значение по умолчанию — D3DMCS \_ Material.

</dd> <dt>

<span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ вертексбленд**
</dt> <dd>

Число матриц, используемых для смешения геометрии, если таковые имеются. Допустимые значения — члены перечисляемого типа [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) . Значение по умолчанию — D3DVBF \_ disable.

</dd> <dt>

<span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ клиппланинабле**
</dt> <dd>

Включает или отключает определенные пользователем отрезкиные плоскости. Допустимые значения: DWORD, в котором состояние каждого бита (установка или не задано) переключает состояние активации соответствующей определяемой пользователем плоскости отсечения. Наименее важный бит (бит 0) управляет первой плоскостью обрезки с индексом 0, а последующие биты управляют активацией обтравочных плоскостей с большими индексами. Если бит установлен, система применяет соответствующую плоскость обрезки во время отрисовки сцены. Значение по умолчанию — 0.

Макросы [**D3DCLIPPLANEn**](d3dclipplanen.md) определяются, чтобы обеспечить удобный способ включения обрезкиных плоскостей.

</dd> <dt>

<span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ POINTSIZE**
</dt> <dd>

Значение float, указывающее размер, используемый при вычислении размера точки в случаях, когда размер точки не указан для каждой вершины. Это значение не используется, если вершина содержит размер точки. Это значение находится в единицах пространства экрана, если D3DRS \_ поинтскалинабле имеет **значение false**; в противном случае это значение находится в единицах универсального пространства. Значение по умолчанию — это значение, возвращаемое драйвером. Если драйвер возвращает 0 или 1, значение по умолчанию — 64, что позволяет эмулировать размер точки программного обеспечения. Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ POINTSIZE \_ мин**
</dt> <dd>

Значение float, определяющее минимальный размер примитивов Point. Примитивы точек обрабатываются на этот размер во время подготовки к просмотру. Если задать для этого параметра значения меньше 1,0, то результаты будут выдаваться, когда точка не охватывает пиксельный центр, а сглаживание отключено или отображается с пониженной интенсивностью при включении сглаживания. Значение по умолчанию — 1,0 f. Диапазон для этого значения больше или равен 0,0 f. Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ поинтспритинабле**
</dt> <dd>

Логическое значение. Если **значение равно true**, координаты текстуры примитивных точек задаются таким образом, чтобы полные текстуры сопоставлены в каждой точке. Если **значение равно false**, координаты текстуры вершины используются для всей точки. Значение по умолчанию — **FALSE**. Можно достичь однопиксельных точек в стиле DirectX 7, установив \_ для D3DRS Поинтскалинабле **значение false** , а D3DRS \_ POINTSIZE — 1,0. это значения по умолчанию.

</dd> <dt>

<span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ поинтскалинабле**
</dt> <dd>

Логическое значение, которое управляет вычислением размера для примитивов точек. Если **значение равно true**, размер точки интерпретируется как значение пространства камеры и масштабируется с помощью функции расстояния, а фрустум — с масштабированием по оси y окна просмотра для расчета конечного размера точки на экране. Если **значение равно false**, размер точки интерпретируется как пространство экрана и используется напрямую. Значение по умолчанию — **FALSE**.

</dd> <dt>

<span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ поинтскале \_ A**
</dt> <dd>

Значение float, которое управляет ослаблением размера на основе расстояния для примитивов точек. Активен, только если D3DRS \_ поинтскалинабле имеет **значение true**. Значение по умолчанию — 1,0 f. Диапазон для этого значения больше или равен 0,0 f. Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ поинтскале \_ B**
</dt> <dd>

Значение float, которое управляет ослаблением размера на основе расстояния для примитивов точек. Активен, только если D3DRS \_ поинтскалинабле имеет **значение true**. Значение по умолчанию — 0,0 f. Диапазон для этого значения больше или равен 0,0 f. Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ поинтскале \_ C**
</dt> <dd>

Значение float, которое управляет ослаблением размера на основе расстояния для примитивов точек. Активен, только если D3DRS \_ поинтскалинабле имеет **значение true**. Значение по умолчанию — 0,0 f. Диапазон для этого значения больше или равен 0,0 f. Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ мултисамплеантиалиас**
</dt> <dd>

Логическое значение, определяющее, как вычисляются отдельные выборки при использовании буфера целевой визуализации с несколькими образцами. Если задано **значение true**, вычисляются несколько выборок, чтобы сглаживание выполнялось с помощью выборки в различных позициях выборки для каждого множественного примера. Если задано **значение false**, то несколько выборок записываются с одним и тем же значением выборки, выборке на пиксельном центре, что позволяет отформатировать несглаженный буфер. Это состояние рендеринга не действует при подготовке к просмотру в одном буфере выборки. Значение по умолчанию — **true**.

</dd> <dt>

<span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ мултисамплемаск**
</dt> <dd>

Каждый бит в этой маске, начиная с наименее значимого бита (ЛСБ), управляет изменением одного из примеров в многовыборочной цели рендеринга. Таким образом, в 8-примерном целевом объекте отрисовки младший байт включает 8 операций записи для каждого из восьми выборок. Это состояние рендеринга не действует при подготовке к просмотру в одном буфере выборки. Значение по умолчанию — 0xFFFFFFFF.

Это состояние рендеринга позволяет использовать многопримерный буфер в качестве буфера накопления, выполняя многопроходную отрисовку геометрии, в которой каждый проход обновляет подмножество образцов.

При наличии n многовыборочных и включенных образцов возможный объем отображаемого изображения должен быть k/n. Каждый RGB-компонент каждого пикселя размещается на k/n.

</dd> <dt>

<span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ патчеджестиле**
</dt> <dd>

Задает, будут ли края исправлений использовать тесселяцию типа float. Возможные значения определяются перечисляемым типом [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) . Значение по умолчанию — D3DPATCHEDGE \_ Дискретный.

</dd> <dt>

<span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ дебугмонитортокен**
</dt> <dd>

Задается только для отладки монитора. Возможные значения определяются перечисляемым типом [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) . Обратите внимание, что если задан параметр D3DRS \_ дебугмонитортокен, вызов обрабатывается как передающий маркер в монитор отладки. Например, если параметр-After передает D3DDMT \_ Enable или D3DDMT \_ Disable в D3DRS \_ дебугмонитортокен-другие значения токена передаются, состояние (включено или отключено) монитора отладки сохраняется.

Это состояние полезно только для отладочных сборок. По умолчанию монитор отладки имеет значение D3DDMT \_ Enable.

</dd> <dt>

<span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ POINTSIZE \_ Max**
</dt> <dd>

Значение float, указывающее максимальный размер, до которого будут относиться спрайты. Значение должно быть меньше или равно Макспоинтсизе члену [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) и больше или равно D3DRS \_ POINTSIZE \_ min. Значение по умолчанию — 64,0. Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ индекседвертексбленденабле**
</dt> <dd>

Логическое значение, которое включает или отключает индексированное смешение вершин. Значение по умолчанию — **FALSE**. Если задано **значение true**, индексирование вершинного смешения включено. Если задано **значение false**, индексирование вершинного смешения отключено. Если это состояние рендеринга включено, пользователь должен передавать индексы матрицы в виде упакованной Двордвис каждой вершины. Если состояние прорисовки отключено и включен режим смешивания вершин через D3DRS \_ вертексбленд, то он эквивалентен индексам матриц 0, 1, 2, 3 в каждой вершине.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ колорвритинабле**
</dt> <dd>

Значение UINT, которое включает запись на канал для буфера цвета целевого объекта подготовки к просмотру. Заданный бит приводит к изменению цветового канала во время трехмерной отрисовки. Четкий бит приводит к неизменности канала цвета. Эта функция доступна, если бит D3DPMISCCAPS \_ колорвритинабле может быть установлен в элементе примитивемисккапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) для устройства. Это состояние визуализации не влияет на операцию очистки. Значение по умолчанию — 0x0000000F.

Допустимые значения для этого состояния рендеринга: D3DCOLORWRITEENABLE \_ альфа, D3DCOLORWRITEENABLE \_ Blue, D3DCOLORWRITEENABLE \_ Green или D3DCOLORWRITEENABLE \_ Red flags.

</dd> <dt>

<span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ твинфактор**
</dt> <dd>

Значение float, которое управляет коэффициентом анимации. Значение по умолчанию — 0,0 f. Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ блендоп**
</dt> <dd>

Значение, используемое для выбора арифметической операции, применяемой, когда в альфа-смешенном состоянии рендеринга D3DRS \_ алфабленденабле имеет значение **true**. Допустимые значения определяются перечисляемым типом [**D3DBLENDOP**](./d3dblendop.md) . Значение по умолчанию — D3DBLENDOP \_ Add.

Если \_ возможность устройства D3DPMISCCAPS блендоп не поддерживается, \_ добавляется D3DBLENDOP Add.

</dd> <dt>

<span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ поситиондегри**
</dt> <dd>

N — степень интерполяции для исправления. Значения могут быть D3DDEGREE \_ кубическим (по умолчанию) или D3DDEGREE \_ линейным. Дополнительные сведения см. в разделе [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ нормалдегри**
</dt> <dd>

N — исправлять нормальную степень интерполяции. Значения могут быть D3DDEGREE \_ линейным (по умолчанию) или D3DDEGREEным \_ квадратичным. Дополнительные сведения см. в разделе [**D3DDEGREETYPE**](./d3ddegreetype.md).

</dd> <dt>

<span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ сЦиссортестенабле**
</dt> <dd>

**Значение true** , чтобы включить ножницное тестирование, и **false** , чтобы отключить его. Значение по умолчанию — **FALSE**.

</dd> <dt>

<span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ слопескаледепсбиас**
</dt> <dd>

Используется для определения того, какой объем смещения можно применить к трехмерным примитивам для снижения степени борьбы с z. Значение по умолчанию — 0.

смещение = (Max \* D3DRS \_ слопескаледепсбиас) + D3DRS \_ депсбиас.

где Max — это максимальная глубина глубины отображаемого треугольника.

</dd> <dt>

<span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ антиалиаседлининабле**
</dt> <dd>

**Значение true** , чтобы включить сглаживание линий; **значение false** , чтобы отключить сглаживание линий. Значение по умолчанию — **FALSE**.

При подготовке к просмотру в многовыборочной цели рендеринга D3DRS \_ антиалиаседлининабле игнорируется и все строки отображаются с псевдонимами. Используйте [**ID3DXLine**](id3dxline.md) для отображения сглаженных линий в многовыборочной цели рендеринга.

</dd> <dt>

<span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ минтесселлатионлевел**
</dt> <dd>

Минимальный уровень тесселяции. Значение по умолчанию — 1,0 f. См. раздел [тесселяция (Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ макстесселлатионлевел**
</dt> <dd>

Максимальный уровень тесселяции. Значение по умолчанию — 1,0 f. См. раздел [тесселяция (Direct3D 9)](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ адаптиветесс \_ X**
</dt> <dd>

Величина адаптивной мозаики в направлении по оси x. Значение по умолчанию — 0,0 f. См. раздел [Адаптивная тесселяция](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ адаптиветесс \_ Y**
</dt> <dd>

Величина адаптивной мозаики в направлении оси y. Значение по умолчанию — 0,0 f. См. раздел [Адаптивная \_ тесселяция](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ адаптиветесс \_ Z**
</dt> <dd>

Величина адаптивной мозаики в направлении по оси z. Значение по умолчанию — 1,0 f. См. раздел [Адаптивная \_ тесселяция](tessellation.md).

</dd> <dt>

<span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ адаптиветесс \_ W**
</dt> <dd>

Величина адаптивной тесселяции в направлении "w". Значение по умолчанию — 0,0 f. См. раздел [Адаптивная \_ тесселяция](tessellation.md).

</dd> <dt>

<span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ енаблеадаптиветесселлатион**
</dt> <dd>

**Значение true** , чтобы включить адаптивную тесселяцию, и **false** для отключения. Значение по умолчанию — **FALSE**. См. раздел [Адаптивная \_ тесселяция](tessellation.md).

</dd> <dt>

<span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ твосидедстенЦилмоде**
</dt> <dd>

**Значение true** включает двухстороннее набор элементов, **false** — отключает его. Значение по умолчанию — **FALSE**. Приложение должно установить D3DRS \_ куллмоде в значение D3DCULL \_ None, чтобы включить режим с двумя сторонами набора элементов. Если порядок заполнения треугольника является по часовой стрелке, \_ будут использоваться операции с набором элементов D3DRS \* . Если порядок поворота имеет значение против часовой стрелки, \_ \_ будут использоваться операции с набором элементов D3DRS CCW \* .

Чтобы узнать, поддерживается ли двусторонний набор элементов, проверьте элемент СтенЦилкапс в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) для D3DSTENCILCAPS \_ твосидед. См. также [D3DSTENCILCAPS](d3dstencilcaps.md).

</dd> <dt>

<span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ стенЦилфаил**
</dt> <dd>

Операция с набором элементов, выполняемая при сбое теста трафарета CCW. Значения из перечисляемого типа [**D3DSTENCILOP**](./d3dstencilop.md) . Значение по умолчанию — D3DSTENCILOP \_ держитесь.

</dd> <dt>

<span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ стенЦилзфаил**
</dt> <dd>

Операция с набором элементов, которую необходимо выполнить, если пройден тест шаблона CCW и не пройден z-тест. Значения из перечисляемого типа [**D3DSTENCILOP**](./d3dstencilop.md) . Значение по умолчанию — D3DSTENCILOP \_ держитесь.

</dd> <dt>

<span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ стенЦилпасс**
</dt> <dd>

Операция с набором элементов, выполняемая, если пройден и набор элементов, и z-тесты. Значения из перечисляемого типа [**D3DSTENCILOP**](./d3dstencilop.md) . Значение по умолчанию — D3DSTENCILOP \_ держитесь.

</dd> <dt>

<span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ стенЦилфунк**
</dt> <dd>

Функция сравнения. Проверка трафаретного шаблона CCW передается, если функция шаблона ((ref & Mask) (маска шаблона &)) имеет **значение true**. Значения из перечисляемого типа [**D3DCMPFUNC**](./d3dcmpfunc.md) . Значение по умолчанию — D3DCMP \_ Always.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**
</dt> <dd>

Дополнительные значения Колорвритинабле для устройств. См. раздел D3DRS \_ колорвритинабле. Эта функция доступна, если бит D3DPMISCCAPS \_ индепендентвритемаскс может быть установлен в элементе примитивемисккапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) для устройства. Значение по умолчанию — 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**
</dt> <dd>

Дополнительные значения Колорвритинабле для устройств. См. раздел D3DRS \_ колорвритинабле. Эта функция доступна, если бит D3DPMISCCAPS \_ индепендентвритемаскс может быть установлен в элементе примитивемисккапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) для устройства. Значение по умолчанию — 0x0000000f.

</dd> <dt>

<span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**
</dt> <dd>

Дополнительные значения Колорвритинабле для устройств. См. раздел D3DRS \_ колорвритинабле. Эта функция доступна, если бит D3DPMISCCAPS \_ индепендентвритемаскс может быть установлен в элементе примитивемисккапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) для устройства. Значение по умолчанию — 0x0000000f.

</dd> <dt>

<span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ блендфактор**
</dt> <dd>

[**D3DCOLOR**](d3dcolor.md) используется для константного коэффициента смешения во время альфа-смешения. Эта функция доступна, если бит D3DPBLENDCAPS \_ блендфактор может быть установлен в сркблендкапс член [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) или **дестблендкапс D3DCAPS9**. См. [**D3DRENDERSTATETYPE**](). Значение по умолчанию — 0xFFFFFFFF.

</dd> <dt>

<span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ сргбвритинабле**
</dt> <dd>

Включение подготовки к просмотру для исправления гаммы в sRGB. Формат должен предоставлять D3DUSAGE \_ сргбврите. Значение по умолчанию — 0.

</dd> <dt>

<span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ депсбиас**
</dt> <dd>

Значение с плавающей запятой, используемое для сравнения значений глубины. См. раздел [смещение глубины (Direct3D 9)](depth-bias.md). Значение по умолчанию — 0.

</dd> <dt>

<span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**
</dt> <dd>

См. раздел D3DRS \_ WRAP0.

</dd> <dt>

<span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ сепаратеалфабленденабле**
</dt> <dd>

**Значение true** включает отдельный режим смешения для альфа-канала. Значение по умолчанию — **FALSE**.

Если задано **значение false**, то коэффициенты смешения и операции, применяемые к альфа-каналу, должны быть такими же, как и для цвета. Этот режим фактически **прикован в реализации** , не устанавливая ограничение D3DPMISCCAPS \_ сепаратеалфабленд. См. [D3DPMISCCAPS](d3dpmisccaps.md).

Тип отдельного альфа-смешения определяется с помощью \_ состояний отрисовки D3DRS сркблендалфа и D3DRS \_ дестблендалфа.

</dd> <dt>

<span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ сркблендалфа**
</dt> <dd>

Один член перечисляемого типа [**D3DBLEND**](./d3dblend.md) . Это значение игнорируется, если D3DRS \_ сепаратеалфабленденабле имеет **значение true**. Значение по умолчанию — D3DBLEND \_ 1.

</dd> <dt>

<span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ дестблендалфа**
</dt> <dd>

Один член перечисляемого типа [**D3DBLEND**](./d3dblend.md) . Это значение игнорируется, если D3DRS \_ сепаратеалфабленденабле имеет **значение true**. Значение по умолчанию — D3DBLEND \_ нуль.

</dd> <dt>

<span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ блендопалфа**
</dt> <dd>

Значение, используемое для выбора арифметической операции, применяемой к отдельной альфа-смешению, когда для состояния отрисовки D3DRS \_ сепаратеалфабленденабле задано **значение true**.

Допустимые значения определяются перечисляемым типом [**D3DBLENDOP**](./d3dblendop.md) . Значение по умолчанию — D3DBLENDOP \_ Add.

Если \_ возможность устройства D3DPMISCCAPS блендоп не поддерживается, \_ добавляется D3DBLENDOP Add. См. [D3DPMISCCAPS](d3dpmisccaps.md).

</dd> <dt>

<span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ Force \_ DWORD**
</dt> <dd>

Заставляет это перечисление компилироваться до 32 бит в размере. Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит. Это значение не используется.

</dd> </dl>

## <a name="remarks"></a>Remarks



| Состояния отрисовки        |   Образец текстуры                 |
|----------------------|--------------------|
| PS \_ 1 \_ 1 – PS \_ 1 \_ 3 | 4 образцов текстуры |



 

Direct3D определяет \_ константу D3DRENDERSTATE врапбиас в качестве удобства для включения или отключения переноса текстур на основе нуля целого числа набора координат текстуры (вместо явного использования одного из значений состояния D3DRS, переданных по \_ словам n). Добавьте значение D3DRENDERSTATE \_ врапбиас в Отсчитываемый от нуля индекс набора координат текстуры, чтобы вычислить \_ значение D3DRS Wrap n, соответствующее этому индексу, как показано в следующем примере.


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>D3D9Types. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[Перечисления Direct3D](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[**IDirect3DDevice9:: Жетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
