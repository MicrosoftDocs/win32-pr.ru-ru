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
ms.openlocfilehash: 2386762eaa45f1eefbccac97723c3ad71c3a76fd
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105703685"
---
# <a name="d3drenderstatetype-enumeration"></a><span data-ttu-id="0a07c-103">Перечисление D3DRENDERSTATETYPE</span><span class="sxs-lookup"><span data-stu-id="0a07c-103">D3DRENDERSTATETYPE enumeration</span></span>

<span data-ttu-id="0a07c-104">Состояния отрисовки определяют состояния настройки для всех видов обработки вершин и пикселей.</span><span class="sxs-lookup"><span data-stu-id="0a07c-104">Render states define set-up states for all kinds of vertex and pixel processing.</span></span> <span data-ttu-id="0a07c-105">Некоторые состояния рендеринга настроили обработку вершин и некоторые настройки обработки пикселей (см. раздел [состояния рендеринга (Direct3D 9)](render-states.md)).</span><span class="sxs-lookup"><span data-stu-id="0a07c-105">Some render states set up vertex processing, and some set up pixel processing (see [Render States (Direct3D 9)](render-states.md)).</span></span> <span data-ttu-id="0a07c-106">Состояния отрисовки можно сохранить и восстановить с помощью статеблоккс (см. раздел [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span><span class="sxs-lookup"><span data-stu-id="0a07c-106">Render states can be saved and restored using stateblocks (see [State Blocks Save and Restore State (Direct3D 9)](state-blocks-save-and-restore-state.md)).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a07c-107">Синтаксис</span><span class="sxs-lookup"><span data-stu-id="0a07c-107">Syntax</span></span>


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



## <a name="constants"></a><span data-ttu-id="0a07c-108">Константы</span><span class="sxs-lookup"><span data-stu-id="0a07c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0a07c-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS \_ зенабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-109"><span id="D3DRS_ZENABLE"></span><span id="d3drs_zenable"></span>**D3DRS\_ZENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-110">Режим буферизации по глубине в виде одного члена перечисляемого типа [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-110">Depth-buffering state as one member of the [**D3DZBUFFERTYPE**](./d3dzbuffertype.md) enumerated type.</span></span> <span data-ttu-id="0a07c-111">Задайте для этого состояния \_ значение D3DZB true, чтобы включить z-буферизацию, D3DZB \_ усев для включения w-Buffering или D3DZB \_ false для отключения буферизации глубины.</span><span class="sxs-lookup"><span data-stu-id="0a07c-111">Set this state to D3DZB\_TRUE to enable z-buffering, D3DZB\_USEW to enable w-buffering, or D3DZB\_FALSE to disable depth buffering.</span></span>

<span data-ttu-id="0a07c-112">Значение по умолчанию для этого состояния рендеринга — D3DZB \_ true, если набор элементов глубины был создан вместе с цепочкой буферов, установив для элемента енаблеаутодепсстенЦил структуры [**\_ параметров D3DPRESENT**](d3dpresent-parameters.md) **значение true**, а D3DZB \_ false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="0a07c-112">The default value for this render state is D3DZB\_TRUE if a depth stencil was created along with the swap chain by setting the EnableAutoDepthStencil member of the [**D3DPRESENT\_PARAMETERS**](d3dpresent-parameters.md) structure to **TRUE**, and D3DZB\_FALSE otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS \_ филлмоде**</span><span class="sxs-lookup"><span data-stu-id="0a07c-113"><span id="D3DRS_FILLMODE"></span><span id="d3drs_fillmode"></span>**D3DRS\_FILLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-114">Один или несколько элементов перечисляемого типа [**D3DFILLMODE**](./d3dfillmode.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-114">One or more members of the [**D3DFILLMODE**](./d3dfillmode.md) enumerated type.</span></span> <span data-ttu-id="0a07c-115">Значение по умолчанию — D3DFILL \_ сплошной.</span><span class="sxs-lookup"><span data-stu-id="0a07c-115">The default value is D3DFILL\_SOLID.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS \_ шадемоде**</span><span class="sxs-lookup"><span data-stu-id="0a07c-116"><span id="D3DRS_SHADEMODE"></span><span id="d3drs_shademode"></span>**D3DRS\_SHADEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-117">Один или несколько элементов перечисляемого типа [**D3DSHADEMODE**](./d3dshademode.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-117">One or more members of the [**D3DSHADEMODE**](./d3dshademode.md) enumerated type.</span></span> <span data-ttu-id="0a07c-118">Значение по умолчанию — D3DSHADE \_ Гуро.</span><span class="sxs-lookup"><span data-stu-id="0a07c-118">The default value is D3DSHADE\_GOURAUD.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS \_ звритинабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-119"><span id="D3DRS_ZWRITEENABLE"></span><span id="d3drs_zwriteenable"></span>**D3DRS\_ZWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-120">**Значение true** , чтобы разрешить приложению выполнять запись в буфер глубины.</span><span class="sxs-lookup"><span data-stu-id="0a07c-120">**TRUE** to enable the application to write to the depth buffer.</span></span> <span data-ttu-id="0a07c-121">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-121">The default value is **TRUE**.</span></span> <span data-ttu-id="0a07c-122">Этот член позволяет приложению запретить системе обновлять буфер глубины новыми значениями глубины.</span><span class="sxs-lookup"><span data-stu-id="0a07c-122">This member enables an application to prevent the system from updating the depth buffer with new depth values.</span></span> <span data-ttu-id="0a07c-123">Если **значение равно false**, сравнение глубины выполняется в соответствии с состоянием отрисовки D3DRS \_ зфунк, предполагая, что буферизация глубины выполняется, но значения глубины не записываются в буфер.</span><span class="sxs-lookup"><span data-stu-id="0a07c-123">If **FALSE**, depth comparisons are still made according to the render state D3DRS\_ZFUNC, assuming that depth buffering is taking place, but depth values are not written to the buffer.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS \_ алфатестенабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-124"><span id="D3DRS_ALPHATESTENABLE"></span><span id="d3drs_alphatestenable"></span>**D3DRS\_ALPHATESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-125">**Значение true** , чтобы включить тестирование альфа-составляющей для каждого пикселя.</span><span class="sxs-lookup"><span data-stu-id="0a07c-125">**TRUE** to enable per pixel alpha testing.</span></span> <span data-ttu-id="0a07c-126">Если тест проходит успешно, пиксель обрабатывается буфером кадров.</span><span class="sxs-lookup"><span data-stu-id="0a07c-126">If the test passes, the pixel is processed by the frame buffer.</span></span> <span data-ttu-id="0a07c-127">В противном случае вся обработка буфера кадров пропускается для пикселя.</span><span class="sxs-lookup"><span data-stu-id="0a07c-127">Otherwise, all frame-buffer processing is skipped for the pixel.</span></span>

<span data-ttu-id="0a07c-128">Тестирование выполняется путем сравнения входящего альфа-значения со ссылочным альфа-значением с помощью функции сравнения, предоставляемой \_ состоянием визуализации D3DRS алфафунк.</span><span class="sxs-lookup"><span data-stu-id="0a07c-128">The test is done by comparing the incoming alpha value with the reference alpha value, using the comparison function provided by the D3DRS\_ALPHAFUNC render state.</span></span> <span data-ttu-id="0a07c-129">Значение ссылки Alpha определяется значением, заданным для D3DRS \_ алфареф.</span><span class="sxs-lookup"><span data-stu-id="0a07c-129">The reference alpha value is determined by the value set for D3DRS\_ALPHAREF.</span></span> <span data-ttu-id="0a07c-130">Дополнительные сведения см. в разделе [Состояние тестирования Alpha (Direct3D 9)](alpha-testing-state.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-130">For more information, see [Alpha Testing State (Direct3D 9)](alpha-testing-state.md).</span></span>

<span data-ttu-id="0a07c-131">Значение этого параметра по умолчанию равно **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-131">The default value of this parameter is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS \_ ластпиксел**</span><span class="sxs-lookup"><span data-stu-id="0a07c-132"><span id="D3DRS_LASTPIXEL"></span><span id="d3drs_lastpixel"></span>**D3DRS\_LASTPIXEL**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-133">Значение по умолчанию — **true**, что позволяет рисовать последний пиксель в строке.</span><span class="sxs-lookup"><span data-stu-id="0a07c-133">The default value is **TRUE**, which enables drawing of the last pixel in a line.</span></span> <span data-ttu-id="0a07c-134">Чтобы запретить Рисование последнего пикселя, присвойте этому параметру значение **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-134">To prevent drawing of the last pixel, set this value to **FALSE**.</span></span> <span data-ttu-id="0a07c-135">Дополнительные сведения см. в разделе [состояние структуры и заливки (Direct3D 9)](outline-and-fill-state.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-135">For more information, see [Outline and Fill State (Direct3D 9)](outline-and-fill-state.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS \_ сркбленд**</span><span class="sxs-lookup"><span data-stu-id="0a07c-136"><span id="D3DRS_SRCBLEND"></span><span id="d3drs_srcblend"></span>**D3DRS\_SRCBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-137">Один член перечисляемого типа [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-137">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="0a07c-138">Значение по умолчанию — D3DBLEND \_ 1.</span><span class="sxs-lookup"><span data-stu-id="0a07c-138">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS \_ дестбленд**</span><span class="sxs-lookup"><span data-stu-id="0a07c-139"><span id="D3DRS_DESTBLEND"></span><span id="d3drs_destblend"></span>**D3DRS\_DESTBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-140">Один член перечисляемого типа [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-140">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="0a07c-141">Значение по умолчанию — D3DBLEND \_ нуль.</span><span class="sxs-lookup"><span data-stu-id="0a07c-141">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS \_ куллмоде**</span><span class="sxs-lookup"><span data-stu-id="0a07c-142"><span id="D3DRS_CULLMODE"></span><span id="d3drs_cullmode"></span>**D3DRS\_CULLMODE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-143">Указывает, как исключаются Задние треугольники, если вообще.</span><span class="sxs-lookup"><span data-stu-id="0a07c-143">Specifies how back-facing triangles are culled, if at all.</span></span> <span data-ttu-id="0a07c-144">Для этого параметра можно задать один элемент перечисляемого типа [**D3DCULL**](./d3dcull.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-144">This can be set to one member of the [**D3DCULL**](./d3dcull.md) enumerated type.</span></span> <span data-ttu-id="0a07c-145">Значение по умолчанию — D3DCULL \_ CCW.</span><span class="sxs-lookup"><span data-stu-id="0a07c-145">The default value is D3DCULL\_CCW.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS \_ зфунк**</span><span class="sxs-lookup"><span data-stu-id="0a07c-146"><span id="D3DRS_ZFUNC"></span><span id="d3drs_zfunc"></span>**D3DRS\_ZFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-147">Один член перечисляемого типа [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-147">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="0a07c-148">Значение по умолчанию — D3DCMP \_ лессекуал.</span><span class="sxs-lookup"><span data-stu-id="0a07c-148">The default value is D3DCMP\_LESSEQUAL.</span></span> <span data-ttu-id="0a07c-149">Этот член позволяет приложению принимать или отклонять пиксель на основе его расстояния от камеры.</span><span class="sxs-lookup"><span data-stu-id="0a07c-149">This member enables an application to accept or reject a pixel, based on its distance from the camera.</span></span>

<span data-ttu-id="0a07c-150">Значение глубины пикселя сравнивается со значением в буфере глубины.</span><span class="sxs-lookup"><span data-stu-id="0a07c-150">The depth value of the pixel is compared with the depth-buffer value.</span></span> <span data-ttu-id="0a07c-151">Если значение глубины пикселя проходит функцию сравнения, пиксель записывается.</span><span class="sxs-lookup"><span data-stu-id="0a07c-151">If the depth value of the pixel passes the comparison function, the pixel is written.</span></span>

<span data-ttu-id="0a07c-152">Значение глубины записывается в буфер глубины только в том случае, если состояние визуализации равно **true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-152">The depth value is written to the depth buffer only if the render state is **TRUE**.</span></span>

<span data-ttu-id="0a07c-153">Программы программной прорисовки и многие ускорители оборудования работают быстрее, если тест глубины завершается неудачно, так как нет необходимости отфильтровать и произвести модуляцию текстуры, если пиксель не будет подготовлен к просмотру.</span><span class="sxs-lookup"><span data-stu-id="0a07c-153">Software rasterizers and many hardware accelerators work faster if the depth test fails, because there is no need to filter and modulate the texture if the pixel is not going to be rendered.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS \_ алфареф**</span><span class="sxs-lookup"><span data-stu-id="0a07c-154"><span id="D3DRS_ALPHAREF"></span><span id="d3drs_alpharef"></span>**D3DRS\_ALPHAREF**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-155">Значение, указывающее альфа-значение ссылки, по которому проверяются Пиксели при включенном тестировании альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="0a07c-155">Value that specifies a reference alpha value against which pixels are tested when alpha testing is enabled.</span></span> <span data-ttu-id="0a07c-156">Это 8-разрядное значение, помещаемое в младшие 8 бит значения состояния отображения DWORD.</span><span class="sxs-lookup"><span data-stu-id="0a07c-156">This is an 8-bit value placed in the low 8 bits of the DWORD render-state value.</span></span> <span data-ttu-id="0a07c-157">Значения могут находиться в диапазоне от 0x00000000 до 0x000000FF.</span><span class="sxs-lookup"><span data-stu-id="0a07c-157">Values can range from 0x00000000 through 0x000000FF.</span></span> <span data-ttu-id="0a07c-158">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-158">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS \_ алфафунк**</span><span class="sxs-lookup"><span data-stu-id="0a07c-159"><span id="D3DRS_ALPHAFUNC"></span><span id="d3drs_alphafunc"></span>**D3DRS\_ALPHAFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-160">Один член перечисляемого типа [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-160">One member of the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="0a07c-161">Значение по умолчанию — D3DCMP \_ Always.</span><span class="sxs-lookup"><span data-stu-id="0a07c-161">The default value is D3DCMP\_ALWAYS.</span></span> <span data-ttu-id="0a07c-162">Этот член позволяет приложению принимать или отклонять пиксель на основе его альфа-значения.</span><span class="sxs-lookup"><span data-stu-id="0a07c-162">This member enables an application to accept or reject a pixel, based on its alpha value.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS \_ дисеренабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-163"><span id="D3DRS_DITHERENABLE"></span><span id="d3drs_ditherenable"></span>**D3DRS\_DITHERENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-164">**Значение true** , чтобы включить Дизеринг.</span><span class="sxs-lookup"><span data-stu-id="0a07c-164">**TRUE** to enable dithering.</span></span> <span data-ttu-id="0a07c-165">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-165">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS \_ алфабленденабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-166"><span id="D3DRS_ALPHABLENDENABLE"></span><span id="d3drs_alphablendenable"></span>**D3DRS\_ALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-167">**Значение true** , чтобы включить прозрачность с альфа-смешением.</span><span class="sxs-lookup"><span data-stu-id="0a07c-167">**TRUE** to enable alpha-blended transparency.</span></span> <span data-ttu-id="0a07c-168">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-168">The default value is **FALSE**.</span></span>

<span data-ttu-id="0a07c-169">Тип альфа-смешения определяется с помощью \_ состояний отрисовки D3DRS сркбленд и D3DRS \_ дестбленд.</span><span class="sxs-lookup"><span data-stu-id="0a07c-169">The type of alpha blending is determined by the D3DRS\_SRCBLEND and D3DRS\_DESTBLEND render states.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS \_ фоженабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-170"><span id="D3DRS_FOGENABLE"></span><span id="d3drs_fogenable"></span>**D3DRS\_FOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-171">**Значение true** , чтобы включить смешение тумана.</span><span class="sxs-lookup"><span data-stu-id="0a07c-171">**TRUE** to enable fog blending.</span></span> <span data-ttu-id="0a07c-172">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-172">The default value is **FALSE**.</span></span> <span data-ttu-id="0a07c-173">Дополнительные сведения об использовании смешения тумана см. в разделе [туман](fog.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-173">For more information about using fog blending, see [Fog](fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS \_ спекуларенабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-174"><span id="D3DRS_SPECULARENABLE"></span><span id="d3drs_specularenable"></span>**D3DRS\_SPECULARENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-175">**Значение true** , чтобы включить отраженные блики.</span><span class="sxs-lookup"><span data-stu-id="0a07c-175">**TRUE** to enable specular highlights.</span></span> <span data-ttu-id="0a07c-176">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-176">The default value is **FALSE**.</span></span>

<span data-ttu-id="0a07c-177">Отраженные блики рассчитываются так, как будто каждая вершина в объекте освещена в источнике объекта.</span><span class="sxs-lookup"><span data-stu-id="0a07c-177">Specular highlights are calculated as though every vertex in the object being lit is at the object's origin.</span></span> <span data-ttu-id="0a07c-178">Это дает ожидаемый результат при условии, что объект моделируется по отношению к источнику, а расстояние от светлого к объекту относительно велико.</span><span class="sxs-lookup"><span data-stu-id="0a07c-178">This gives the expected results as long as the object is modeled around the origin and the distance from the light to the object is relatively large.</span></span> <span data-ttu-id="0a07c-179">В других случаях результаты считаются неопределенными.</span><span class="sxs-lookup"><span data-stu-id="0a07c-179">In other cases, the results as undefined.</span></span>

<span data-ttu-id="0a07c-180">Если для этого элемента задано **значение true**, то отраженный цвет добавляется к базовому цвету после текстуры Cascade, но перед альфа-смешением.</span><span class="sxs-lookup"><span data-stu-id="0a07c-180">When this member is set to **TRUE**, the specular color is added to the base color after the texture cascade but before alpha blending.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS \_ фогколор**</span><span class="sxs-lookup"><span data-stu-id="0a07c-181"><span id="D3DRS_FOGCOLOR"></span><span id="d3drs_fogcolor"></span>**D3DRS\_FOGCOLOR**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-182">Значение, тип которого — [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-182">Value whose type is [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="0a07c-183">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-183">The default value is 0.</span></span> <span data-ttu-id="0a07c-184">Дополнительные сведения о цвете тумана см. в разделе [Цвет тумана (Direct3D 9)](fog-color.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-184">For more information about fog color, see [Fog Color (Direct3D 9)](fog-color.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS \_ фогтаблемоде**</span><span class="sxs-lookup"><span data-stu-id="0a07c-185"><span id="D3DRS_FOGTABLEMODE"></span><span id="d3drs_fogtablemode"></span>**D3DRS\_FOGTABLEMODE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-186">Формула тумана, используемая для пиксельного тумана.</span><span class="sxs-lookup"><span data-stu-id="0a07c-186">The fog formula to be used for pixel fog.</span></span> <span data-ttu-id="0a07c-187">Задайте один из элементов перечисляемого типа [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-187">Set to one of the members of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="0a07c-188">Значение по умолчанию — D3DFOG \_ None.</span><span class="sxs-lookup"><span data-stu-id="0a07c-188">The default value is D3DFOG\_NONE.</span></span> <span data-ttu-id="0a07c-189">Дополнительные сведения о пиксельном тумане см. в разделе [Pixel туман (Direct3D 9)](pixel-fog.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-189">For more information about pixel fog, see [Pixel Fog (Direct3D 9)](pixel-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS \_ фогстарт**</span><span class="sxs-lookup"><span data-stu-id="0a07c-190"><span id="D3DRS_FOGSTART"></span><span id="d3drs_fogstart"></span>**D3DRS\_FOGSTART**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-191">Глубина, на которой эффект пиксельного или вершинного тумана начинается для линейного режима тумана.</span><span class="sxs-lookup"><span data-stu-id="0a07c-191">Depth at which pixel or vertex fog effects begin for linear fog mode.</span></span> <span data-ttu-id="0a07c-192">Значение по умолчанию — 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-192">The default value is 0.0f.</span></span> <span data-ttu-id="0a07c-193">Глубина задается в мировом пространстве для вершинного тумана и в пространстве устройства \[ 0,0, 1,0 \] или мировом пространстве для пиксельного тумана.</span><span class="sxs-lookup"><span data-stu-id="0a07c-193">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="0a07c-194">Для пиксельных туманов эти значения находятся в пространстве устройства, когда система использует z для вычислений тумана и мирового пространства, когда в системе используется относительный туман (w-туман).</span><span class="sxs-lookup"><span data-stu-id="0a07c-194">For pixel fog, these values are in device space when the system uses z for fog calculations and world-world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="0a07c-195">Дополнительные сведения см. в разделе [Параметры тумана (Direct3D 9)](fog-parameters.md) и [глубина по сравнению с Z](pixel-fog.md)-ориентированным глазом.</span><span class="sxs-lookup"><span data-stu-id="0a07c-195">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="0a07c-196">Значения для этого состояния рендеринга — это значения с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0a07c-196">Values for this render state are floating-point values.</span></span> <span data-ttu-id="0a07c-197">Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="0a07c-197">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
pDevice9->SetRenderState(D3DRS_FOGSTART, 
                         *((DWORD*) (&fFogStart)));
```



</dd> <dt>

<span data-ttu-id="0a07c-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS \_ фоженд**</span><span class="sxs-lookup"><span data-stu-id="0a07c-198"><span id="D3DRS_FOGEND"></span><span id="d3drs_fogend"></span>**D3DRS\_FOGEND**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-199">Глубина, на которой эффекты пиксельного или вершинного тумана заканчиваются линейным режимом тумана.</span><span class="sxs-lookup"><span data-stu-id="0a07c-199">Depth at which pixel or vertex fog effects end for linear fog mode.</span></span> <span data-ttu-id="0a07c-200">Значение по умолчанию — 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-200">The default value is 1.0f.</span></span> <span data-ttu-id="0a07c-201">Глубина задается в мировом пространстве для вершинного тумана и в пространстве устройства \[ 0,0, 1,0 \] или мировом пространстве для пиксельного тумана.</span><span class="sxs-lookup"><span data-stu-id="0a07c-201">Depth is specified in world space for vertex fog and either device space \[0.0, 1.0\] or world space for pixel fog.</span></span> <span data-ttu-id="0a07c-202">Для пиксельных туманов эти значения находятся в пространстве устройства, когда система использует z для вычислений тумана и в мировом пространстве, когда в системе используется относительный туман (w-туман).</span><span class="sxs-lookup"><span data-stu-id="0a07c-202">For pixel fog, these values are in device space when the system uses z for fog calculations and in world space when the system is using eye-relative fog (w-fog).</span></span> <span data-ttu-id="0a07c-203">Дополнительные сведения см. в разделе [Параметры тумана (Direct3D 9)](fog-parameters.md) и [глубина по сравнению с Z](pixel-fog.md)-ориентированным глазом.</span><span class="sxs-lookup"><span data-stu-id="0a07c-203">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md) and [Eye-Relative vs. Z-based Depth](pixel-fog.md).</span></span>

<span data-ttu-id="0a07c-204">Значения для этого состояния рендеринга — это значения с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0a07c-204">Values for this render state are floating-point values.</span></span> <span data-ttu-id="0a07c-205">Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="0a07c-205">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_FOGEND, *((DWORD*) (&fFogEnd)));
```



</dd> <dt>

<span data-ttu-id="0a07c-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS \_ фогденсити**</span><span class="sxs-lookup"><span data-stu-id="0a07c-206"><span id="D3DRS_FOGDENSITY"></span><span id="d3drs_fogdensity"></span>**D3DRS\_FOGDENSITY**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-207">Плотность тумана для пиксельного или вершинного тумана, используемого в экспоненциальном режиме тумана (D3DFOG \_ EXP и D3DFOG \_ EXP2).</span><span class="sxs-lookup"><span data-stu-id="0a07c-207">Fog density for pixel or vertex fog used in the exponential fog modes (D3DFOG\_EXP and D3DFOG\_EXP2).</span></span> <span data-ttu-id="0a07c-208">Допустимые значения плотности находятся в диапазоне от 0,0 до 1,0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-208">Valid density values range from 0.0 through 1.0.</span></span> <span data-ttu-id="0a07c-209">Значение по умолчанию — 1,0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-209">The default value is 1.0.</span></span> <span data-ttu-id="0a07c-210">Дополнительные сведения см. в разделе [Параметры тумана (Direct3D 9)](fog-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-210">For more information, see [Fog Parameters (Direct3D 9)](fog-parameters.md).</span></span>

<span data-ttu-id="0a07c-211">Значения для этого состояния рендеринга — это значения с плавающей запятой.</span><span class="sxs-lookup"><span data-stu-id="0a07c-211">Values for this render state are floating-point values.</span></span> <span data-ttu-id="0a07c-212">Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="0a07c-212">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
    m_pDevice9->SetRenderState(D3DRS_FOGDENSITY, *((DWORD*) (&fFogDensity)));
```



</dd> <dt>

<span data-ttu-id="0a07c-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS \_ ранжефоженабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-213"><span id="D3DRS_RANGEFOGENABLE"></span><span id="d3drs_rangefogenable"></span>**D3DRS\_RANGEFOGENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-214">**Значение true** , чтобы включить вершинный туман на основе диапазона.</span><span class="sxs-lookup"><span data-stu-id="0a07c-214">**TRUE** to enable range-based vertex fog.</span></span> <span data-ttu-id="0a07c-215">Значение по умолчанию — **false**. в этом случае система использует туман на основе глубины.</span><span class="sxs-lookup"><span data-stu-id="0a07c-215">The default value is **FALSE**, in which case the system uses depth-based fog.</span></span> <span data-ttu-id="0a07c-216">В тумане на основе диапазона расстояние объекта от средства просмотра используется для расчета эффектов тумана, а не глубины объекта (то есть z-координаты) в сцене.</span><span class="sxs-lookup"><span data-stu-id="0a07c-216">In range-based fog, the distance of an object from the viewer is used to compute fog effects, not the depth of the object (that is, the z-coordinate) in the scene.</span></span> <span data-ttu-id="0a07c-217">В тумане, основанном на диапазоне, все методы тумана работают как обычно, за исключением того, что они используют диапазон, а не глубину в вычислениях.</span><span class="sxs-lookup"><span data-stu-id="0a07c-217">In range-based fog, all fog methods work as usual, except that they use range instead of depth in the computations.</span></span>

<span data-ttu-id="0a07c-218">Диапазон — это правильный фактор, используемый для вычислений тумана, но вместо этого обычно используется глубина, поскольку диапазон занимает много времени.</span><span class="sxs-lookup"><span data-stu-id="0a07c-218">Range is the correct factor to use for fog computations, but depth is commonly used instead because range is time-consuming to compute and depth is generally already available.</span></span> <span data-ttu-id="0a07c-219">Использование функции Depth для вычисления тумана имеет нежелательное воздействие на изменение фоггинесса периферийных объектов при перемещении средства просмотра. в этом случае глубина изменяется, а диапазон остается постоянным.</span><span class="sxs-lookup"><span data-stu-id="0a07c-219">Using depth to calculate fog has the undesirable effect of having the fogginess of peripheral objects change as the viewer's eye moves - in this case, the depth changes and the range remains constant.</span></span>

<span data-ttu-id="0a07c-220">Поскольку оборудование в настоящее время не поддерживает туман на основе диапазона, исправление диапазона предлагается только для вершинного тумана.</span><span class="sxs-lookup"><span data-stu-id="0a07c-220">Because no hardware currently supports per-pixel range-based fog, range correction is offered only for vertex fog.</span></span>

<span data-ttu-id="0a07c-221">Дополнительные сведения см. в разделе [вершинный туман (Direct3D 9)](vertex-fog.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-221">For more information, see [Vertex Fog (Direct3D 9)](vertex-fog.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS \_ стенЦиленабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-222"><span id="D3DRS_STENCILENABLE"></span><span id="d3drs_stencilenable"></span>**D3DRS\_STENCILENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-223">**Значение true** , чтобы включить набор элементов, или **false** , чтобы отключить набор элементов.</span><span class="sxs-lookup"><span data-stu-id="0a07c-223">**TRUE** to enable stenciling, or **FALSE** to disable stenciling.</span></span> <span data-ttu-id="0a07c-224">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-224">The default value is **FALSE**.</span></span> <span data-ttu-id="0a07c-225">Дополнительные сведения см. в разделе [методы буферизации элементов (Direct3D 9)](stencil-buffer-techniques.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-225">For more information, see [Stencil Buffer Techniques (Direct3D 9)](stencil-buffer-techniques.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS \_ стенЦилфаил**</span><span class="sxs-lookup"><span data-stu-id="0a07c-226"><span id="D3DRS_STENCILFAIL"></span><span id="d3drs_stencilfail"></span>**D3DRS\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-227">Операция с набором элементов, выполняемая при сбое теста шаблона.</span><span class="sxs-lookup"><span data-stu-id="0a07c-227">Stencil operation to perform if the stencil test fails.</span></span> <span data-ttu-id="0a07c-228">Значения из перечисляемого типа [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-228">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="0a07c-229">Значение по умолчанию — D3DSTENCILOP \_ держитесь.</span><span class="sxs-lookup"><span data-stu-id="0a07c-229">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS \_ стенЦилзфаил**</span><span class="sxs-lookup"><span data-stu-id="0a07c-230"><span id="D3DRS_STENCILZFAIL"></span><span id="d3drs_stencilzfail"></span>**D3DRS\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-231">Операция с набором элементов, которую необходимо выполнить, если тест шаблона прошел успешно и тест глубины (z-Test) завершается сбоем.</span><span class="sxs-lookup"><span data-stu-id="0a07c-231">Stencil operation to perform if the stencil test passes and the depth test (z-test) fails.</span></span> <span data-ttu-id="0a07c-232">Значения из перечисляемого типа [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-232">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="0a07c-233">Значение по умолчанию — D3DSTENCILOP \_ держитесь.</span><span class="sxs-lookup"><span data-stu-id="0a07c-233">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS \_ стенЦилпасс**</span><span class="sxs-lookup"><span data-stu-id="0a07c-234"><span id="D3DRS_STENCILPASS"></span><span id="d3drs_stencilpass"></span>**D3DRS\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-235">Операция с набором элементов, которую необходимо выполнить, если пройдены тесты набора элементов и глубины (z).</span><span class="sxs-lookup"><span data-stu-id="0a07c-235">Stencil operation to perform if both the stencil and the depth (z) tests pass.</span></span> <span data-ttu-id="0a07c-236">Значения из перечисляемого типа [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-236">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="0a07c-237">Значение по умолчанию — D3DSTENCILOP \_ держитесь.</span><span class="sxs-lookup"><span data-stu-id="0a07c-237">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS \_ стенЦилфунк**</span><span class="sxs-lookup"><span data-stu-id="0a07c-238"><span id="D3DRS_STENCILFUNC"></span><span id="d3drs_stencilfunc"></span>**D3DRS\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-239">Функция сравнения для теста набора элементов.</span><span class="sxs-lookup"><span data-stu-id="0a07c-239">Comparison function for the stencil test.</span></span> <span data-ttu-id="0a07c-240">Значения из перечисляемого типа [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-240">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="0a07c-241">Значение по умолчанию — D3DCMP \_ Always.</span><span class="sxs-lookup"><span data-stu-id="0a07c-241">The default value is D3DCMP\_ALWAYS.</span></span>

<span data-ttu-id="0a07c-242">Функция сравнения используется для сравнения ссылочного значения с записью в буфере набора элементов.</span><span class="sxs-lookup"><span data-stu-id="0a07c-242">The comparison function is used to compare the reference value to a stencil buffer entry.</span></span> <span data-ttu-id="0a07c-243">Это сравнение применяется только к битам в записи ссылочного значения и буфера трафарета, заданных в маске набора элементов (задается \_ состоянием отрисовки D3DRS стенЦилмаск).</span><span class="sxs-lookup"><span data-stu-id="0a07c-243">This comparison applies only to the bits in the reference value and stencil buffer entry that are set in the stencil mask (set by the D3DRS\_STENCILMASK render state).</span></span> <span data-ttu-id="0a07c-244">Если **значение равно true**, проверка шаблона проходит успешно.</span><span class="sxs-lookup"><span data-stu-id="0a07c-244">If **TRUE**, the stencil test passes.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS \_ стенЦилреф**</span><span class="sxs-lookup"><span data-stu-id="0a07c-245"><span id="D3DRS_STENCILREF"></span><span id="d3drs_stencilref"></span>**D3DRS\_STENCILREF**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-246">Значение ссылочного типа int для теста набора элементов.</span><span class="sxs-lookup"><span data-stu-id="0a07c-246">An int reference value for the stencil test.</span></span> <span data-ttu-id="0a07c-247">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-247">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS \_ стенЦилмаск**</span><span class="sxs-lookup"><span data-stu-id="0a07c-248"><span id="D3DRS_STENCILMASK"></span><span id="d3drs_stencilmask"></span>**D3DRS\_STENCILMASK**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-249">Маска, применяемая к значению ссылки и записи буфера набора элементов для определения значимых битов для теста набора элементов.</span><span class="sxs-lookup"><span data-stu-id="0a07c-249">Mask applied to the reference value and each stencil buffer entry to determine the significant bits for the stencil test.</span></span> <span data-ttu-id="0a07c-250">Маска по умолчанию — 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="0a07c-250">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS \_ стенЦилвритемаск**</span><span class="sxs-lookup"><span data-stu-id="0a07c-251"><span id="D3DRS_STENCILWRITEMASK"></span><span id="d3drs_stencilwritemask"></span>**D3DRS\_STENCILWRITEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-252">Маска записи, применяемая к значениям, записанным в буфер шаблона.</span><span class="sxs-lookup"><span data-stu-id="0a07c-252">Write mask applied to values written into the stencil buffer.</span></span> <span data-ttu-id="0a07c-253">Маска по умолчанию — 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="0a07c-253">The default mask is 0xFFFFFFFF.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS \_ текстурефактор**</span><span class="sxs-lookup"><span data-stu-id="0a07c-254"><span id="D3DRS_TEXTUREFACTOR"></span><span id="d3drs_texturefactor"></span>**D3DRS\_TEXTUREFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-255">Цвет, используемый для смешения текстур с помощью \_ аргумента D3DTA тфактор текстура-смешения или \_ операции смешения текстур D3DTOP блендфакторалфа.</span><span class="sxs-lookup"><span data-stu-id="0a07c-255">Color used for multiple-texture blending with the D3DTA\_TFACTOR texture-blending argument or the D3DTOP\_BLENDFACTORALPHA texture-blending operation.</span></span> <span data-ttu-id="0a07c-256">Связанное значение является переменной [**D3DCOLOR**](d3dcolor.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-256">The associated value is a [**D3DCOLOR**](d3dcolor.md) variable.</span></span> <span data-ttu-id="0a07c-257">Значение по умолчанию — непрозрачный белый (0xFFFFFFFF).</span><span class="sxs-lookup"><span data-stu-id="0a07c-257">The default value is opaque white (0xFFFFFFFF).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS \_ WRAP0**</span><span class="sxs-lookup"><span data-stu-id="0a07c-258"><span id="D3DRS_WRAP0"></span><span id="d3drs_wrap0"></span>**D3DRS\_WRAP0**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-259">Поведение при переносе текстур для нескольких наборов координат текстуры.</span><span class="sxs-lookup"><span data-stu-id="0a07c-259">Texture-wrapping behavior for multiple sets of texture coordinates.</span></span> <span data-ttu-id="0a07c-260">Допустимые значения для этого состояния рендеринга: D3DWRAPCOORD \_ 0 (или D3DWRAP \_ U), D3DWRAPCOORD \_ 1 (или D3DWRAP \_ V), D3DWRAPCOORD \_ 2 (или D3DWRAP \_ W) и D3DWRAPCOORD \_ 3.</span><span class="sxs-lookup"><span data-stu-id="0a07c-260">Valid values for this render state can be any combination of the D3DWRAPCOORD\_0 (or D3DWRAP\_U), D3DWRAPCOORD\_1 (or D3DWRAP\_V), D3DWRAPCOORD\_2 (or D3DWRAP\_W), and D3DWRAPCOORD\_3 flags.</span></span> <span data-ttu-id="0a07c-261">Это приводит к тому, что система переносится в направлении первого, второго, третьего и четвертого измерений, которые иногда называют направлениями s, t, r и q для заданной текстуры.</span><span class="sxs-lookup"><span data-stu-id="0a07c-261">These cause the system to wrap in the direction of the first, second, third, and fourth dimensions, sometimes referred to as the s, t, r, and q directions, for a given texture.</span></span> <span data-ttu-id="0a07c-262">Значение по умолчанию для этого состояния рендеринга равно 0 (в всех направлениях отключено обтекание).</span><span class="sxs-lookup"><span data-stu-id="0a07c-262">The default value for this render state is 0 (wrapping disabled in all directions).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS \_ WRAP1**</span><span class="sxs-lookup"><span data-stu-id="0a07c-263"><span id="D3DRS_WRAP1"></span><span id="d3drs_wrap1"></span>**D3DRS\_WRAP1**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-264">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-264">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS \_ WRAP2**</span><span class="sxs-lookup"><span data-stu-id="0a07c-265"><span id="D3DRS_WRAP2"></span><span id="d3drs_wrap2"></span>**D3DRS\_WRAP2**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-266">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-266">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS \_ WRAP3**</span><span class="sxs-lookup"><span data-stu-id="0a07c-267"><span id="D3DRS_WRAP3"></span><span id="d3drs_wrap3"></span>**D3DRS\_WRAP3**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-268">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-268">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS \_ WRAP4**</span><span class="sxs-lookup"><span data-stu-id="0a07c-269"><span id="D3DRS_WRAP4"></span><span id="d3drs_wrap4"></span>**D3DRS\_WRAP4**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-270">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-270">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS \_ WRAP5**</span><span class="sxs-lookup"><span data-stu-id="0a07c-271"><span id="D3DRS_WRAP5"></span><span id="d3drs_wrap5"></span>**D3DRS\_WRAP5**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-272">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-272">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS \_ WRAP6**</span><span class="sxs-lookup"><span data-stu-id="0a07c-273"><span id="D3DRS_WRAP6"></span><span id="d3drs_wrap6"></span>**D3DRS\_WRAP6**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-274">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-274">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS \_ WRAP7**</span><span class="sxs-lookup"><span data-stu-id="0a07c-275"><span id="D3DRS_WRAP7"></span><span id="d3drs_wrap7"></span>**D3DRS\_WRAP7**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-276">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-276">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS \_ Обрезка**</span><span class="sxs-lookup"><span data-stu-id="0a07c-277"><span id="D3DRS_CLIPPING"></span><span id="d3drs_clipping"></span>**D3DRS\_CLIPPING**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-278">**Значение true** , чтобы включить примитив, вырезая Direct3D, или **false** , чтобы отключить его.</span><span class="sxs-lookup"><span data-stu-id="0a07c-278">**TRUE** to enable primitive clipping by Direct3D, or **FALSE** to disable it.</span></span> <span data-ttu-id="0a07c-279">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-279">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**\_Освещение D3DRS**</span><span class="sxs-lookup"><span data-stu-id="0a07c-280"><span id="D3DRS_LIGHTING"></span><span id="d3drs_lighting"></span>**D3DRS\_LIGHTING**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-281">**Значение true** , чтобы включить освещение Direct3D, или **false** , чтобы отключить его.</span><span class="sxs-lookup"><span data-stu-id="0a07c-281">**TRUE** to enable Direct3D lighting, or **FALSE** to disable it.</span></span> <span data-ttu-id="0a07c-282">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-282">The default value is **TRUE**.</span></span> <span data-ttu-id="0a07c-283">Правильно освещены только вершины, включающие нормальную вершину. в вершинах, не содержащих обычных, используется точка с координатами 0 во всех вычислениях освещения.</span><span class="sxs-lookup"><span data-stu-id="0a07c-283">Only vertices that include a vertex normal are properly lit; vertices that do not contain a normal employ a dot product of 0 in all lighting calculations.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS \_ окружение**</span><span class="sxs-lookup"><span data-stu-id="0a07c-284"><span id="D3DRS_AMBIENT"></span><span id="d3drs_ambient"></span>**D3DRS\_AMBIENT**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-285">Цвет освещения.</span><span class="sxs-lookup"><span data-stu-id="0a07c-285">Ambient light color.</span></span> <span data-ttu-id="0a07c-286">Это значение типа [**D3DCOLOR**](d3dcolor.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-286">This value is of type [**D3DCOLOR**](d3dcolor.md).</span></span> <span data-ttu-id="0a07c-287">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-287">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS \_ фогвертексмоде**</span><span class="sxs-lookup"><span data-stu-id="0a07c-288"><span id="D3DRS_FOGVERTEXMODE"></span><span id="d3drs_fogvertexmode"></span>**D3DRS\_FOGVERTEXMODE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-289">Формула тумана, используемая для вершинного тумана.</span><span class="sxs-lookup"><span data-stu-id="0a07c-289">Fog formula to be used for vertex fog.</span></span> <span data-ttu-id="0a07c-290">Задайте для одного члена перечисляемого типа [**D3DFOGMODE**](./d3dfogmode.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-290">Set to one member of the [**D3DFOGMODE**](./d3dfogmode.md) enumerated type.</span></span> <span data-ttu-id="0a07c-291">Значение по умолчанию — D3DFOG \_ None.</span><span class="sxs-lookup"><span data-stu-id="0a07c-291">The default value is D3DFOG\_NONE.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS \_ колорвертекс**</span><span class="sxs-lookup"><span data-stu-id="0a07c-292"><span id="D3DRS_COLORVERTEX"></span><span id="d3drs_colorvertex"></span>**D3DRS\_COLORVERTEX**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-293">**Значение true** , чтобы включить цвет каждой вершины или **значение false** , чтобы отключить его.</span><span class="sxs-lookup"><span data-stu-id="0a07c-293">**TRUE** to enable per-vertex color or **FALSE** to disable it.</span></span> <span data-ttu-id="0a07c-294">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-294">The default value is **TRUE**.</span></span> <span data-ttu-id="0a07c-295">Включение цвета на уровне вершины позволяет системе включать цвет, определенный для отдельных вершин в вычислениях освещения.</span><span class="sxs-lookup"><span data-stu-id="0a07c-295">Enabling per-vertex color allows the system to include the color defined for individual vertices in its lighting calculations.</span></span>

<span data-ttu-id="0a07c-296">Дополнительные сведения см. в следующих состояниях рендеринга:</span><span class="sxs-lookup"><span data-stu-id="0a07c-296">For more information, see the following render states:</span></span>

-   <span data-ttu-id="0a07c-297">D3DRS \_ диффусематериалсаурце</span><span class="sxs-lookup"><span data-stu-id="0a07c-297">D3DRS\_DIFFUSEMATERIALSOURCE</span></span>
-   <span data-ttu-id="0a07c-298">D3DRS \_ спекуларматериалсаурце</span><span class="sxs-lookup"><span data-stu-id="0a07c-298">D3DRS\_SPECULARMATERIALSOURCE</span></span>
-   <span data-ttu-id="0a07c-299">D3DRS \_ амбиентматериалсаурце</span><span class="sxs-lookup"><span data-stu-id="0a07c-299">D3DRS\_AMBIENTMATERIALSOURCE</span></span>
-   <span data-ttu-id="0a07c-300">D3DRS \_ емиссивематериалсаурце</span><span class="sxs-lookup"><span data-stu-id="0a07c-300">D3DRS\_EMISSIVEMATERIALSOURCE</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS \_ локалвиевер**</span><span class="sxs-lookup"><span data-stu-id="0a07c-301"><span id="D3DRS_LOCALVIEWER"></span><span id="d3drs_localviewer"></span>**D3DRS\_LOCALVIEWER**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-302">**Значение true** для включения отражения относительно камеры или **false** для использования ортогональных отраженных светов.</span><span class="sxs-lookup"><span data-stu-id="0a07c-302">**TRUE** to enable camera-relative specular highlights, or **FALSE** to use orthogonal specular highlights.</span></span> <span data-ttu-id="0a07c-303">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-303">The default value is **TRUE**.</span></span> <span data-ttu-id="0a07c-304">В приложениях, использующих ортогональную проекцию, должно быть указано **значение false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-304">Applications that use orthogonal projection should specify **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS \_ нормализенормалс**</span><span class="sxs-lookup"><span data-stu-id="0a07c-305"><span id="D3DRS_NORMALIZENORMALS"></span><span id="d3drs_normalizenormals"></span>**D3DRS\_NORMALIZENORMALS**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-306">**Значение true** , чтобы включить автоматическую нормализацию нормалей вершин, или **false** , чтобы отключить ее.</span><span class="sxs-lookup"><span data-stu-id="0a07c-306">**TRUE** to enable automatic normalization of vertex normals, or **FALSE** to disable it.</span></span> <span data-ttu-id="0a07c-307">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-307">The default value is **FALSE**.</span></span> <span data-ttu-id="0a07c-308">Включение этой функции приводит к нормализации нормалей вершин для вершин после их преобразования в место на камере, что может потребовать вычислений по времени.</span><span class="sxs-lookup"><span data-stu-id="0a07c-308">Enabling this feature causes the system to normalize the vertex normals for vertices after transforming them to camera space, which can be computationally time-consuming.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS \_ диффусематериалсаурце**</span><span class="sxs-lookup"><span data-stu-id="0a07c-309"><span id="D3DRS_DIFFUSEMATERIALSOURCE"></span><span id="d3drs_diffusematerialsource"></span>**D3DRS\_DIFFUSEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-310">Источник рассеянного цвета для вычислений освещения.</span><span class="sxs-lookup"><span data-stu-id="0a07c-310">Diffuse color source for lighting calculations.</span></span> <span data-ttu-id="0a07c-311">Допустимые значения — члены перечисляемого типа [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-311">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="0a07c-312">Значение по умолчанию — D3DMCS \_ COLOR1.</span><span class="sxs-lookup"><span data-stu-id="0a07c-312">The default value is D3DMCS\_COLOR1.</span></span> <span data-ttu-id="0a07c-313">Значение для этого состояния визуализации используется только в том случае, если \_ для состояния отрисовки D3DRS колорвертекс задано значение **true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-313">The value for this render state is used only if the D3DRS\_COLORVERTEX render state is set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS \_ спекуларматериалсаурце**</span><span class="sxs-lookup"><span data-stu-id="0a07c-314"><span id="D3DRS_SPECULARMATERIALSOURCE"></span><span id="d3drs_specularmaterialsource"></span>**D3DRS\_SPECULARMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-315">Источник отраженного цвета для вычислений освещения.</span><span class="sxs-lookup"><span data-stu-id="0a07c-315">Specular color source for lighting calculations.</span></span> <span data-ttu-id="0a07c-316">Допустимые значения — члены перечисляемого типа [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-316">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="0a07c-317">Значение по умолчанию — D3DMCS \_ COLOR2.</span><span class="sxs-lookup"><span data-stu-id="0a07c-317">The default value is D3DMCS\_COLOR2.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS \_ амбиентматериалсаурце**</span><span class="sxs-lookup"><span data-stu-id="0a07c-318"><span id="D3DRS_AMBIENTMATERIALSOURCE"></span><span id="d3drs_ambientmaterialsource"></span>**D3DRS\_AMBIENTMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-319">Источник внешнего цвета для вычислений освещения.</span><span class="sxs-lookup"><span data-stu-id="0a07c-319">Ambient color source for lighting calculations.</span></span> <span data-ttu-id="0a07c-320">Допустимые значения — члены перечисляемого типа [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-320">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="0a07c-321">Значение по умолчанию — D3DMCS \_ Material.</span><span class="sxs-lookup"><span data-stu-id="0a07c-321">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS \_ емиссивематериалсаурце**</span><span class="sxs-lookup"><span data-stu-id="0a07c-322"><span id="D3DRS_EMISSIVEMATERIALSOURCE"></span><span id="d3drs_emissivematerialsource"></span>**D3DRS\_EMISSIVEMATERIALSOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-323">Источник цвета эмиссионный для вычислений освещения.</span><span class="sxs-lookup"><span data-stu-id="0a07c-323">Emissive color source for lighting calculations.</span></span> <span data-ttu-id="0a07c-324">Допустимые значения — члены перечисляемого типа [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-324">Valid values are members of the [**D3DMATERIALCOLORSOURCE**](./d3dmaterialcolorsource.md) enumerated type.</span></span> <span data-ttu-id="0a07c-325">Значение по умолчанию — D3DMCS \_ Material.</span><span class="sxs-lookup"><span data-stu-id="0a07c-325">The default value is D3DMCS\_MATERIAL.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS \_ вертексбленд**</span><span class="sxs-lookup"><span data-stu-id="0a07c-326"><span id="D3DRS_VERTEXBLEND"></span><span id="d3drs_vertexblend"></span>**D3DRS\_VERTEXBLEND**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-327">Число матриц, используемых для смешения геометрии, если таковые имеются.</span><span class="sxs-lookup"><span data-stu-id="0a07c-327">Number of matrices to use to perform geometry blending, if any.</span></span> <span data-ttu-id="0a07c-328">Допустимые значения — члены перечисляемого типа [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-328">Valid values are members of the [**D3DVERTEXBLENDFLAGS**](./d3dvertexblendflags.md) enumerated type.</span></span> <span data-ttu-id="0a07c-329">Значение по умолчанию — D3DVBF \_ disable.</span><span class="sxs-lookup"><span data-stu-id="0a07c-329">The default value is D3DVBF\_DISABLE.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS \_ клиппланинабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-330"><span id="D3DRS_CLIPPLANEENABLE"></span><span id="d3drs_clipplaneenable"></span>**D3DRS\_CLIPPLANEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-331">Включает или отключает определенные пользователем отрезкиные плоскости.</span><span class="sxs-lookup"><span data-stu-id="0a07c-331">Enables or disables user-defined clipping planes.</span></span> <span data-ttu-id="0a07c-332">Допустимые значения: DWORD, в котором состояние каждого бита (установка или не задано) переключает состояние активации соответствующей определяемой пользователем плоскости отсечения.</span><span class="sxs-lookup"><span data-stu-id="0a07c-332">Valid values are any DWORD in which the status of each bit (set or not set) toggles the activation state of a corresponding user-defined clipping plane.</span></span> <span data-ttu-id="0a07c-333">Наименее важный бит (бит 0) управляет первой плоскостью обрезки с индексом 0, а последующие биты управляют активацией обтравочных плоскостей с большими индексами.</span><span class="sxs-lookup"><span data-stu-id="0a07c-333">The least significant bit (bit 0) controls the first clipping plane at index 0, and subsequent bits control the activation of clipping planes at higher indexes.</span></span> <span data-ttu-id="0a07c-334">Если бит установлен, система применяет соответствующую плоскость обрезки во время отрисовки сцены.</span><span class="sxs-lookup"><span data-stu-id="0a07c-334">If a bit is set, the system applies the appropriate clipping plane during scene rendering.</span></span> <span data-ttu-id="0a07c-335">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-335">The default value is 0.</span></span>

<span data-ttu-id="0a07c-336">Макросы [**D3DCLIPPLANEn**](d3dclipplanen.md) определяются, чтобы обеспечить удобный способ включения обрезкиных плоскостей.</span><span class="sxs-lookup"><span data-stu-id="0a07c-336">The [**D3DCLIPPLANEn**](d3dclipplanen.md) macros are defined to provide a convenient way to enable clipping planes.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS \_ POINTSIZE**</span><span class="sxs-lookup"><span data-stu-id="0a07c-337"><span id="D3DRS_POINTSIZE"></span><span id="d3drs_pointsize"></span>**D3DRS\_POINTSIZE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-338">Значение float, указывающее размер, используемый при вычислении размера точки в случаях, когда размер точки не указан для каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="0a07c-338">A float value that specifies the size to use for point size computation in cases where point size is not specified for each vertex.</span></span> <span data-ttu-id="0a07c-339">Это значение не используется, если вершина содержит размер точки.</span><span class="sxs-lookup"><span data-stu-id="0a07c-339">This value is not used when the vertex contains point size.</span></span> <span data-ttu-id="0a07c-340">Это значение находится в единицах пространства экрана, если D3DRS \_ поинтскалинабле имеет **значение false**; в противном случае это значение находится в единицах универсального пространства.</span><span class="sxs-lookup"><span data-stu-id="0a07c-340">This value is in screen space units if D3DRS\_POINTSCALEENABLE is **FALSE**; otherwise this value is in world space units.</span></span> <span data-ttu-id="0a07c-341">Значение по умолчанию — это значение, возвращаемое драйвером.</span><span class="sxs-lookup"><span data-stu-id="0a07c-341">The default value is the value a driver returns.</span></span> <span data-ttu-id="0a07c-342">Если драйвер возвращает 0 или 1, значение по умолчанию — 64, что позволяет эмулировать размер точки программного обеспечения.</span><span class="sxs-lookup"><span data-stu-id="0a07c-342">If a driver returns 0 or 1, the default value is 64, which allows software point size emulation.</span></span> <span data-ttu-id="0a07c-343">Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="0a07c-343">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE, *((DWORD*)&pointSize));
```



</dd> <dt>

<span data-ttu-id="0a07c-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS \_ POINTSIZE \_ мин**</span><span class="sxs-lookup"><span data-stu-id="0a07c-344"><span id="D3DRS_POINTSIZE_MIN"></span><span id="d3drs_pointsize_min"></span>**D3DRS\_POINTSIZE\_MIN**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-345">Значение float, определяющее минимальный размер примитивов Point.</span><span class="sxs-lookup"><span data-stu-id="0a07c-345">A float value that specifies the minimum size of point primitives.</span></span> <span data-ttu-id="0a07c-346">Примитивы точек обрабатываются на этот размер во время подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="0a07c-346">Point primitives are clamped to this size during rendering.</span></span> <span data-ttu-id="0a07c-347">Если задать для этого параметра значения меньше 1,0, то результаты будут выдаваться, когда точка не охватывает пиксельный центр, а сглаживание отключено или отображается с пониженной интенсивностью при включении сглаживания.</span><span class="sxs-lookup"><span data-stu-id="0a07c-347">Setting this to values smaller than 1.0 results in points dropping out when the point does not cover a pixel center and antialiasing is disabled or being rendered with reduced intensity when antialiasing is enabled.</span></span> <span data-ttu-id="0a07c-348">Значение по умолчанию — 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-348">The default value is 1.0f.</span></span> <span data-ttu-id="0a07c-349">Диапазон для этого значения больше или равен 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-349">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="0a07c-350">Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="0a07c-350">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSIZE_MIN, *((DWORD*)&pointSizeMin));
```



</dd> <dt>

<span data-ttu-id="0a07c-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS \_ поинтспритинабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-351"><span id="D3DRS_POINTSPRITEENABLE"></span><span id="d3drs_pointspriteenable"></span>**D3DRS\_POINTSPRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-352">Логическое значение.</span><span class="sxs-lookup"><span data-stu-id="0a07c-352">bool value.</span></span> <span data-ttu-id="0a07c-353">Если **значение равно true**, координаты текстуры примитивных точек задаются таким образом, чтобы полные текстуры сопоставлены в каждой точке.</span><span class="sxs-lookup"><span data-stu-id="0a07c-353">When **TRUE**, texture coordinates of point primitives are set so that full textures are mapped on each point.</span></span> <span data-ttu-id="0a07c-354">Если **значение равно false**, координаты текстуры вершины используются для всей точки.</span><span class="sxs-lookup"><span data-stu-id="0a07c-354">When **FALSE**, the vertex texture coordinates are used for the entire point.</span></span> <span data-ttu-id="0a07c-355">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-355">The default value is **FALSE**.</span></span> <span data-ttu-id="0a07c-356">Можно достичь однопиксельных точек в стиле DirectX 7, установив \_ для D3DRS Поинтскалинабле **значение false** , а D3DRS \_ POINTSIZE — 1,0. это значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0a07c-356">You can achieve DirectX 7 style single-pixel points by setting D3DRS\_POINTSCALEENABLE to **FALSE** and D3DRS\_POINTSIZE to 1.0, which are the default values.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS \_ поинтскалинабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-357"><span id="D3DRS_POINTSCALEENABLE"></span><span id="d3drs_pointscaleenable"></span>**D3DRS\_POINTSCALEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-358">Логическое значение, которое управляет вычислением размера для примитивов точек.</span><span class="sxs-lookup"><span data-stu-id="0a07c-358">bool value that controls computation of size for point primitives.</span></span> <span data-ttu-id="0a07c-359">Если **значение равно true**, размер точки интерпретируется как значение пространства камеры и масштабируется с помощью функции расстояния, а фрустум — с масштабированием по оси y окна просмотра для расчета конечного размера точки на экране.</span><span class="sxs-lookup"><span data-stu-id="0a07c-359">When **TRUE**, the point size is interpreted as a camera space value and is scaled by the distance function and the frustum to viewport y-axis scaling to compute the final screen-space point size.</span></span> <span data-ttu-id="0a07c-360">Если **значение равно false**, размер точки интерпретируется как пространство экрана и используется напрямую.</span><span class="sxs-lookup"><span data-stu-id="0a07c-360">When **FALSE**, the point size is interpreted as screen space and used directly.</span></span> <span data-ttu-id="0a07c-361">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-361">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS \_ поинтскале \_ A**</span><span class="sxs-lookup"><span data-stu-id="0a07c-362"><span id="D3DRS_POINTSCALE_A"></span><span id="d3drs_pointscale_a"></span>**D3DRS\_POINTSCALE\_A**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-363">Значение float, которое управляет ослаблением размера на основе расстояния для примитивов точек.</span><span class="sxs-lookup"><span data-stu-id="0a07c-363">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="0a07c-364">Активен, только если D3DRS \_ поинтскалинабле имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-364">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="0a07c-365">Значение по умолчанию — 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-365">The default value is 1.0f.</span></span> <span data-ttu-id="0a07c-366">Диапазон для этого значения больше или равен 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-366">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="0a07c-367">Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="0a07c-367">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_A, *((DWORD*)&pointScaleA));
```



</dd> <dt>

<span data-ttu-id="0a07c-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS \_ поинтскале \_ B**</span><span class="sxs-lookup"><span data-stu-id="0a07c-368"><span id="D3DRS_POINTSCALE_B"></span><span id="d3drs_pointscale_b"></span>**D3DRS\_POINTSCALE\_B**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-369">Значение float, которое управляет ослаблением размера на основе расстояния для примитивов точек.</span><span class="sxs-lookup"><span data-stu-id="0a07c-369">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="0a07c-370">Активен, только если D3DRS \_ поинтскалинабле имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-370">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="0a07c-371">Значение по умолчанию — 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-371">The default value is 0.0f.</span></span> <span data-ttu-id="0a07c-372">Диапазон для этого значения больше или равен 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-372">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="0a07c-373">Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="0a07c-373">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_B, *((DWORD*)&pointScaleB));
```



</dd> <dt>

<span data-ttu-id="0a07c-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS \_ поинтскале \_ C**</span><span class="sxs-lookup"><span data-stu-id="0a07c-374"><span id="D3DRS_POINTSCALE_C"></span><span id="d3drs_pointscale_c"></span>**D3DRS\_POINTSCALE\_C**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-375">Значение float, которое управляет ослаблением размера на основе расстояния для примитивов точек.</span><span class="sxs-lookup"><span data-stu-id="0a07c-375">A float value that controls for distance-based size attenuation for point primitives.</span></span> <span data-ttu-id="0a07c-376">Активен, только если D3DRS \_ поинтскалинабле имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-376">Active only when D3DRS\_POINTSCALEENABLE is **TRUE**.</span></span> <span data-ttu-id="0a07c-377">Значение по умолчанию — 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-377">The default value is 0.0f.</span></span> <span data-ttu-id="0a07c-378">Диапазон для этого значения больше или равен 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-378">The range for this value is greater than or equal to 0.0f.</span></span> <span data-ttu-id="0a07c-379">Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="0a07c-379">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_POINTSCALE_C, *((DWORD*)&pointScaleC));
```



</dd> <dt>

<span data-ttu-id="0a07c-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS \_ мултисамплеантиалиас**</span><span class="sxs-lookup"><span data-stu-id="0a07c-380"><span id="D3DRS_MULTISAMPLEANTIALIAS"></span><span id="d3drs_multisampleantialias"></span>**D3DRS\_MULTISAMPLEANTIALIAS**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-381">Логическое значение, определяющее, как вычисляются отдельные выборки при использовании буфера целевой визуализации с несколькими образцами.</span><span class="sxs-lookup"><span data-stu-id="0a07c-381">bool value that determines how individual samples are computed when using a multisample render-target buffer.</span></span> <span data-ttu-id="0a07c-382">Если задано **значение true**, вычисляются несколько выборок, чтобы сглаживание выполнялось с помощью выборки в различных позициях выборки для каждого множественного примера.</span><span class="sxs-lookup"><span data-stu-id="0a07c-382">When set to **TRUE**, the multiple samples are computed so that full-scene antialiasing is performed by sampling at different sample positions for each multiple sample.</span></span> <span data-ttu-id="0a07c-383">Если задано **значение false**, то несколько выборок записываются с одним и тем же значением выборки, выборке на пиксельном центре, что позволяет отформатировать несглаженный буфер.</span><span class="sxs-lookup"><span data-stu-id="0a07c-383">When set to **FALSE**, the multiple samples are all written with the same sample value, sampled at the pixel center, which allows non-antialiased rendering to a multisample buffer.</span></span> <span data-ttu-id="0a07c-384">Это состояние рендеринга не действует при подготовке к просмотру в одном буфере выборки.</span><span class="sxs-lookup"><span data-stu-id="0a07c-384">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="0a07c-385">Значение по умолчанию — **true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-385">The default value is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS \_ мултисамплемаск**</span><span class="sxs-lookup"><span data-stu-id="0a07c-386"><span id="D3DRS_MULTISAMPLEMASK"></span><span id="d3drs_multisamplemask"></span>**D3DRS\_MULTISAMPLEMASK**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-387">Каждый бит в этой маске, начиная с наименее значимого бита (ЛСБ), управляет изменением одного из примеров в многовыборочной цели рендеринга.</span><span class="sxs-lookup"><span data-stu-id="0a07c-387">Each bit in this mask, starting at the least significant bit (LSB), controls modification of one of the samples in a multisample render target.</span></span> <span data-ttu-id="0a07c-388">Таким образом, в 8-примерном целевом объекте отрисовки младший байт включает 8 операций записи для каждого из восьми выборок.</span><span class="sxs-lookup"><span data-stu-id="0a07c-388">Thus, for an 8-sample render target, the low byte contains the eight write enables for each of the eight samples.</span></span> <span data-ttu-id="0a07c-389">Это состояние рендеринга не действует при подготовке к просмотру в одном буфере выборки.</span><span class="sxs-lookup"><span data-stu-id="0a07c-389">This render state has no effect when rendering to a single sample buffer.</span></span> <span data-ttu-id="0a07c-390">Значение по умолчанию — 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="0a07c-390">The default value is 0xFFFFFFFF.</span></span>

<span data-ttu-id="0a07c-391">Это состояние рендеринга позволяет использовать многопримерный буфер в качестве буфера накопления, выполняя многопроходную отрисовку геометрии, в которой каждый проход обновляет подмножество образцов.</span><span class="sxs-lookup"><span data-stu-id="0a07c-391">This render state enables use of a multisample buffer as an accumulation buffer, doing multipass rendering of geometry where each pass updates a subset of samples.</span></span>

<span data-ttu-id="0a07c-392">При наличии n многовыборочных и включенных образцов возможный объем отображаемого изображения должен быть k/n.</span><span class="sxs-lookup"><span data-stu-id="0a07c-392">If there are n multisamples and k enabled samples, the resulting intensity of the rendered image should be k/n.</span></span> <span data-ttu-id="0a07c-393">Каждый RGB-компонент каждого пикселя размещается на k/n.</span><span class="sxs-lookup"><span data-stu-id="0a07c-393">Each component RGB of every pixel is factored by k/n.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS \_ патчеджестиле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-394"><span id="D3DRS_PATCHEDGESTYLE"></span><span id="d3drs_patchedgestyle"></span>**D3DRS\_PATCHEDGESTYLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-395">Задает, будут ли края исправлений использовать тесселяцию типа float.</span><span class="sxs-lookup"><span data-stu-id="0a07c-395">Sets whether patch edges will use float style tessellation.</span></span> <span data-ttu-id="0a07c-396">Возможные значения определяются перечисляемым типом [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-396">Possible values are defined by the [**D3DPATCHEDGESTYLE**](./d3dpatchedgestyle.md) enumerated type.</span></span> <span data-ttu-id="0a07c-397">Значение по умолчанию — D3DPATCHEDGE \_ Дискретный.</span><span class="sxs-lookup"><span data-stu-id="0a07c-397">The default value is D3DPATCHEDGE\_DISCRETE.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS \_ дебугмонитортокен**</span><span class="sxs-lookup"><span data-stu-id="0a07c-398"><span id="D3DRS_DEBUGMONITORTOKEN"></span><span id="d3drs_debugmonitortoken"></span>**D3DRS\_DEBUGMONITORTOKEN**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-399">Задается только для отладки монитора.</span><span class="sxs-lookup"><span data-stu-id="0a07c-399">Set only for debugging the monitor.</span></span> <span data-ttu-id="0a07c-400">Возможные значения определяются перечисляемым типом [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-400">Possible values are defined by the [**D3DDEBUGMONITORTOKENS**](./d3ddebugmonitortokens.md) enumerated type.</span></span> <span data-ttu-id="0a07c-401">Обратите внимание, что если задан параметр D3DRS \_ дебугмонитортокен, вызов обрабатывается как передающий маркер в монитор отладки.</span><span class="sxs-lookup"><span data-stu-id="0a07c-401">Note that if D3DRS\_DEBUGMONITORTOKEN is set, the call is treated as passing a token to the debug monitor.</span></span> <span data-ttu-id="0a07c-402">Например, если параметр-After передает D3DDMT \_ Enable или D3DDMT \_ Disable в D3DRS \_ дебугмонитортокен-другие значения токена передаются, состояние (включено или отключено) монитора отладки сохраняется.</span><span class="sxs-lookup"><span data-stu-id="0a07c-402">For example, if - after passing D3DDMT\_ENABLE or D3DDMT\_DISABLE to D3DRS\_DEBUGMONITORTOKEN - other token values are passed in, the state (enabled or disabled) of the debug monitor will still persist.</span></span>

<span data-ttu-id="0a07c-403">Это состояние полезно только для отладочных сборок.</span><span class="sxs-lookup"><span data-stu-id="0a07c-403">This state is only useful for debug builds.</span></span> <span data-ttu-id="0a07c-404">По умолчанию монитор отладки имеет значение D3DDMT \_ Enable.</span><span class="sxs-lookup"><span data-stu-id="0a07c-404">The debug monitor defaults to D3DDMT\_ENABLE.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS \_ POINTSIZE \_ Max**</span><span class="sxs-lookup"><span data-stu-id="0a07c-405"><span id="D3DRS_POINTSIZE_MAX"></span><span id="d3drs_pointsize_max"></span>**D3DRS\_POINTSIZE\_MAX**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-406">Значение float, указывающее максимальный размер, до которого будут относиться спрайты.</span><span class="sxs-lookup"><span data-stu-id="0a07c-406">A float value that specifies the maximum size to which point sprites will be clamped.</span></span> <span data-ttu-id="0a07c-407">Значение должно быть меньше или равно Макспоинтсизе члену [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) и больше или равно D3DRS \_ POINTSIZE \_ min.</span><span class="sxs-lookup"><span data-stu-id="0a07c-407">The value must be less than or equal to the MaxPointSize member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) and greater than or equal to D3DRS\_POINTSIZE\_MIN.</span></span> <span data-ttu-id="0a07c-408">Значение по умолчанию — 64,0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-408">The default value is 64.0.</span></span> <span data-ttu-id="0a07c-409">Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="0a07c-409">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_PONTSIZE_MAX, *((DWORD*)&pointSizeMax));
```



</dd> <dt>

<span data-ttu-id="0a07c-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS \_ индекседвертексбленденабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-410"><span id="D3DRS_INDEXEDVERTEXBLENDENABLE"></span><span id="d3drs_indexedvertexblendenable"></span>**D3DRS\_INDEXEDVERTEXBLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-411">Логическое значение, которое включает или отключает индексированное смешение вершин.</span><span class="sxs-lookup"><span data-stu-id="0a07c-411">bool value that enables or disables indexed vertex blending.</span></span> <span data-ttu-id="0a07c-412">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-412">The default value is **FALSE**.</span></span> <span data-ttu-id="0a07c-413">Если задано **значение true**, индексирование вершинного смешения включено.</span><span class="sxs-lookup"><span data-stu-id="0a07c-413">When set to **TRUE**, indexed vertex blending is enabled.</span></span> <span data-ttu-id="0a07c-414">Если задано **значение false**, индексирование вершинного смешения отключено.</span><span class="sxs-lookup"><span data-stu-id="0a07c-414">When set to **FALSE**, indexed vertex blending is disabled.</span></span> <span data-ttu-id="0a07c-415">Если это состояние рендеринга включено, пользователь должен передавать индексы матрицы в виде упакованной Двордвис каждой вершины.</span><span class="sxs-lookup"><span data-stu-id="0a07c-415">If this render state is enabled, the user must pass matrix indices as a packed DWORDwith every vertex.</span></span> <span data-ttu-id="0a07c-416">Если состояние прорисовки отключено и включен режим смешивания вершин через D3DRS \_ вертексбленд, то он эквивалентен индексам матриц 0, 1, 2, 3 в каждой вершине.</span><span class="sxs-lookup"><span data-stu-id="0a07c-416">When the render state is disabled and vertex blending is enabled through the D3DRS\_VERTEXBLEND state, it is equivalent to having matrix indices 0, 1, 2, 3 in every vertex.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS \_ колорвритинабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-417"><span id="D3DRS_COLORWRITEENABLE"></span><span id="d3drs_colorwriteenable"></span>**D3DRS\_COLORWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-418">Значение UINT, которое включает запись на канал для буфера цвета целевого объекта подготовки к просмотру.</span><span class="sxs-lookup"><span data-stu-id="0a07c-418">UINT value that enables a per-channel write for the render-target color buffer.</span></span> <span data-ttu-id="0a07c-419">Заданный бит приводит к изменению цветового канала во время трехмерной отрисовки.</span><span class="sxs-lookup"><span data-stu-id="0a07c-419">A set bit results in the color channel being updated during 3D rendering.</span></span> <span data-ttu-id="0a07c-420">Четкий бит приводит к неизменности канала цвета.</span><span class="sxs-lookup"><span data-stu-id="0a07c-420">A clear bit results in the color channel being unaffected.</span></span> <span data-ttu-id="0a07c-421">Эта функция доступна, если бит D3DPMISCCAPS \_ колорвритинабле может быть установлен в элементе примитивемисккапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) для устройства.</span><span class="sxs-lookup"><span data-stu-id="0a07c-421">This functionality is available if the D3DPMISCCAPS\_COLORWRITEENABLE capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="0a07c-422">Это состояние визуализации не влияет на операцию очистки.</span><span class="sxs-lookup"><span data-stu-id="0a07c-422">This render state does not affect the clear operation.</span></span> <span data-ttu-id="0a07c-423">Значение по умолчанию — 0x0000000F.</span><span class="sxs-lookup"><span data-stu-id="0a07c-423">The default value is 0x0000000F.</span></span>

<span data-ttu-id="0a07c-424">Допустимые значения для этого состояния рендеринга: D3DCOLORWRITEENABLE \_ альфа, D3DCOLORWRITEENABLE \_ Blue, D3DCOLORWRITEENABLE \_ Green или D3DCOLORWRITEENABLE \_ Red flags.</span><span class="sxs-lookup"><span data-stu-id="0a07c-424">Valid values for this render state can be any combination of the D3DCOLORWRITEENABLE\_ALPHA, D3DCOLORWRITEENABLE\_BLUE, D3DCOLORWRITEENABLE\_GREEN, or D3DCOLORWRITEENABLE\_RED flags.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS \_ твинфактор**</span><span class="sxs-lookup"><span data-stu-id="0a07c-425"><span id="D3DRS_TWEENFACTOR"></span><span id="d3drs_tweenfactor"></span>**D3DRS\_TWEENFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-426">Значение float, которое управляет коэффициентом анимации.</span><span class="sxs-lookup"><span data-stu-id="0a07c-426">A float value that controls the tween factor.</span></span> <span data-ttu-id="0a07c-427">Значение по умолчанию — 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-427">The default value is 0.0f.</span></span> <span data-ttu-id="0a07c-428">Так как метод [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) принимает значения типа DWORD, приложение должно привести переменную, содержащую значение, как показано в следующем примере кода.</span><span class="sxs-lookup"><span data-stu-id="0a07c-428">Because the [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) method accepts DWORD values, your application must cast a variable that contains the value, as shown in the following code example.</span></span>


```
m_pDevice9->SetRenderState(D3DRS_TWEENFACTOR, *((DWORD*)&TweenFactor));
```



</dd> <dt>

<span data-ttu-id="0a07c-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS \_ блендоп**</span><span class="sxs-lookup"><span data-stu-id="0a07c-429"><span id="D3DRS_BLENDOP"></span><span id="d3drs_blendop"></span>**D3DRS\_BLENDOP**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-430">Значение, используемое для выбора арифметической операции, применяемой, когда в альфа-смешенном состоянии рендеринга D3DRS \_ алфабленденабле имеет значение **true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-430">Value used to select the arithmetic operation applied when the alpha blending render state, D3DRS\_ALPHABLENDENABLE, is set to **TRUE**.</span></span> <span data-ttu-id="0a07c-431">Допустимые значения определяются перечисляемым типом [**D3DBLENDOP**](./d3dblendop.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-431">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="0a07c-432">Значение по умолчанию — D3DBLENDOP \_ Add.</span><span class="sxs-lookup"><span data-stu-id="0a07c-432">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="0a07c-433">Если \_ возможность устройства D3DPMISCCAPS блендоп не поддерживается, \_ добавляется D3DBLENDOP Add.</span><span class="sxs-lookup"><span data-stu-id="0a07c-433">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS \_ поситиондегри**</span><span class="sxs-lookup"><span data-stu-id="0a07c-434"><span id="D3DRS_POSITIONDEGREE"></span><span id="d3drs_positiondegree"></span>**D3DRS\_POSITIONDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-435">N — степень интерполяции для исправления.</span><span class="sxs-lookup"><span data-stu-id="0a07c-435">N-patch position interpolation degree.</span></span> <span data-ttu-id="0a07c-436">Значения могут быть D3DDEGREE \_ кубическим (по умолчанию) или D3DDEGREE \_ линейным.</span><span class="sxs-lookup"><span data-stu-id="0a07c-436">The values can be D3DDEGREE\_CUBIC (default) or D3DDEGREE\_LINEAR.</span></span> <span data-ttu-id="0a07c-437">Дополнительные сведения см. в разделе [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-437">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS \_ нормалдегри**</span><span class="sxs-lookup"><span data-stu-id="0a07c-438"><span id="D3DRS_NORMALDEGREE"></span><span id="d3drs_normaldegree"></span>**D3DRS\_NORMALDEGREE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-439">N — исправлять нормальную степень интерполяции.</span><span class="sxs-lookup"><span data-stu-id="0a07c-439">N-patch normal interpolation degree.</span></span> <span data-ttu-id="0a07c-440">Значения могут быть D3DDEGREE \_ линейным (по умолчанию) или D3DDEGREEным \_ квадратичным.</span><span class="sxs-lookup"><span data-stu-id="0a07c-440">The values can be D3DDEGREE\_LINEAR (default) or D3DDEGREE\_QUADRATIC.</span></span> <span data-ttu-id="0a07c-441">Дополнительные сведения см. в разделе [**D3DDEGREETYPE**](./d3ddegreetype.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-441">For more information, see [**D3DDEGREETYPE**](./d3ddegreetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS \_ сЦиссортестенабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-442"><span id="D3DRS_SCISSORTESTENABLE"></span><span id="d3drs_scissortestenable"></span>**D3DRS\_SCISSORTESTENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-443">**Значение true** , чтобы включить ножницное тестирование, и **false** , чтобы отключить его.</span><span class="sxs-lookup"><span data-stu-id="0a07c-443">**TRUE** to enable scissor testing and **FALSE** to disable it.</span></span> <span data-ttu-id="0a07c-444">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-444">The default value is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS \_ слопескаледепсбиас**</span><span class="sxs-lookup"><span data-stu-id="0a07c-445"><span id="D3DRS_SLOPESCALEDEPTHBIAS"></span><span id="d3drs_slopescaledepthbias"></span>**D3DRS\_SLOPESCALEDEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-446">Используется для определения того, какой объем смещения можно применить к трехмерным примитивам для снижения степени борьбы с z.</span><span class="sxs-lookup"><span data-stu-id="0a07c-446">Used to determine how much bias can be applied to co-planar primitives to reduce z-fighting.</span></span> <span data-ttu-id="0a07c-447">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-447">The default value is 0.</span></span>

<span data-ttu-id="0a07c-448">смещение = (Max \* D3DRS \_ слопескаледепсбиас) + D3DRS \_ депсбиас.</span><span class="sxs-lookup"><span data-stu-id="0a07c-448">bias = (max \* D3DRS\_SLOPESCALEDEPTHBIAS) + D3DRS\_DEPTHBIAS.</span></span>

<span data-ttu-id="0a07c-449">где Max — это максимальная глубина глубины отображаемого треугольника.</span><span class="sxs-lookup"><span data-stu-id="0a07c-449">where max is the maximum depth slope of the triangle being rendered.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS \_ антиалиаседлининабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-450"><span id="D3DRS_ANTIALIASEDLINEENABLE"></span><span id="d3drs_antialiasedlineenable"></span>**D3DRS\_ANTIALIASEDLINEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-451">**Значение true** , чтобы включить сглаживание линий; **значение false** , чтобы отключить сглаживание линий.</span><span class="sxs-lookup"><span data-stu-id="0a07c-451">**TRUE** to enable line antialiasing, **FALSE** to disable line antialiasing.</span></span> <span data-ttu-id="0a07c-452">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-452">The default value is **FALSE**.</span></span>

<span data-ttu-id="0a07c-453">При подготовке к просмотру в многовыборочной цели рендеринга D3DRS \_ антиалиаседлининабле игнорируется и все строки отображаются с псевдонимами.</span><span class="sxs-lookup"><span data-stu-id="0a07c-453">When rendering to a multisample render target, D3DRS\_ANTIALIASEDLINEENABLE is ignored and all lines are rendered aliased.</span></span> <span data-ttu-id="0a07c-454">Используйте [**ID3DXLine**](id3dxline.md) для отображения сглаженных линий в многовыборочной цели рендеринга.</span><span class="sxs-lookup"><span data-stu-id="0a07c-454">Use [**ID3DXLine**](id3dxline.md) for antialiased line rendering in a multisample render target.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS \_ минтесселлатионлевел**</span><span class="sxs-lookup"><span data-stu-id="0a07c-455"><span id="D3DRS_MINTESSELLATIONLEVEL"></span><span id="d3drs_mintessellationlevel"></span>**D3DRS\_MINTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-456">Минимальный уровень тесселяции.</span><span class="sxs-lookup"><span data-stu-id="0a07c-456">Minimum tessellation level.</span></span> <span data-ttu-id="0a07c-457">Значение по умолчанию — 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-457">The default value is 1.0f.</span></span> <span data-ttu-id="0a07c-458">См. раздел [тесселяция (Direct3D 9)](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-458">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS \_ макстесселлатионлевел**</span><span class="sxs-lookup"><span data-stu-id="0a07c-459"><span id="D3DRS_MAXTESSELLATIONLEVEL"></span><span id="d3drs_maxtessellationlevel"></span>**D3DRS\_MAXTESSELLATIONLEVEL**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-460">Максимальный уровень тесселяции.</span><span class="sxs-lookup"><span data-stu-id="0a07c-460">Maximum tessellation level.</span></span> <span data-ttu-id="0a07c-461">Значение по умолчанию — 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-461">The default value is 1.0f.</span></span> <span data-ttu-id="0a07c-462">См. раздел [тесселяция (Direct3D 9)](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-462">See [Tessellation (Direct3D 9)](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS \_ адаптиветесс \_ X**</span><span class="sxs-lookup"><span data-stu-id="0a07c-463"><span id="D3DRS_ADAPTIVETESS_X"></span><span id="d3drs_adaptivetess_x"></span>**D3DRS\_ADAPTIVETESS\_X**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-464">Величина адаптивной мозаики в направлении по оси x.</span><span class="sxs-lookup"><span data-stu-id="0a07c-464">Amount to adaptively tessellate, in the x direction.</span></span> <span data-ttu-id="0a07c-465">Значение по умолчанию — 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-465">Default value is 0.0f.</span></span> <span data-ttu-id="0a07c-466">См. раздел [Адаптивная тесселяция](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-466">See [Adaptive Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS \_ адаптиветесс \_ Y**</span><span class="sxs-lookup"><span data-stu-id="0a07c-467"><span id="D3DRS_ADAPTIVETESS_Y"></span><span id="d3drs_adaptivetess_y"></span>**D3DRS\_ADAPTIVETESS\_Y**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-468">Величина адаптивной мозаики в направлении оси y.</span><span class="sxs-lookup"><span data-stu-id="0a07c-468">Amount to adaptively tessellate, in the y direction.</span></span> <span data-ttu-id="0a07c-469">Значение по умолчанию — 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-469">Default value is 0.0f.</span></span> <span data-ttu-id="0a07c-470">См. раздел [Адаптивная \_ тесселяция](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-470">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS \_ адаптиветесс \_ Z**</span><span class="sxs-lookup"><span data-stu-id="0a07c-471"><span id="D3DRS_ADAPTIVETESS_Z"></span><span id="d3drs_adaptivetess_z"></span>**D3DRS\_ADAPTIVETESS\_Z**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-472">Величина адаптивной мозаики в направлении по оси z.</span><span class="sxs-lookup"><span data-stu-id="0a07c-472">Amount to adaptively tessellate, in the z direction.</span></span> <span data-ttu-id="0a07c-473">Значение по умолчанию — 1,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-473">Default value is 1.0f.</span></span> <span data-ttu-id="0a07c-474">См. раздел [Адаптивная \_ тесселяция](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-474">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS \_ адаптиветесс \_ W**</span><span class="sxs-lookup"><span data-stu-id="0a07c-475"><span id="D3DRS_ADAPTIVETESS_W"></span><span id="d3drs_adaptivetess_w"></span>**D3DRS\_ADAPTIVETESS\_W**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-476">Величина адаптивной тесселяции в направлении "w".</span><span class="sxs-lookup"><span data-stu-id="0a07c-476">Amount to adaptively tessellate, in the w direction.</span></span> <span data-ttu-id="0a07c-477">Значение по умолчанию — 0,0 f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-477">Default value is 0.0f.</span></span> <span data-ttu-id="0a07c-478">См. раздел [Адаптивная \_ тесселяция](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-478">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS \_ енаблеадаптиветесселлатион**</span><span class="sxs-lookup"><span data-stu-id="0a07c-479"><span id="D3DRS_ENABLEADAPTIVETESSELLATION"></span><span id="d3drs_enableadaptivetessellation"></span>**D3DRS\_ENABLEADAPTIVETESSELLATION**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-480">**Значение true** , чтобы включить адаптивную тесселяцию, и **false** для отключения.</span><span class="sxs-lookup"><span data-stu-id="0a07c-480">**TRUE** to enable adaptive tessellation, **FALSE** to disable it.</span></span> <span data-ttu-id="0a07c-481">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-481">The default value is **FALSE**.</span></span> <span data-ttu-id="0a07c-482">См. раздел [Адаптивная \_ тесселяция](tessellation.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-482">See [Adaptive\_Tessellation](tessellation.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS \_ твосидедстенЦилмоде**</span><span class="sxs-lookup"><span data-stu-id="0a07c-483"><span id="D3DRS_TWOSIDEDSTENCILMODE"></span><span id="d3drs_twosidedstencilmode"></span>**D3DRS\_TWOSIDEDSTENCILMODE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-484">**Значение true** включает двухстороннее набор элементов, **false** — отключает его.</span><span class="sxs-lookup"><span data-stu-id="0a07c-484">**TRUE** enables two-sided stenciling, **FALSE** disables it.</span></span> <span data-ttu-id="0a07c-485">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-485">The default value is **FALSE**.</span></span> <span data-ttu-id="0a07c-486">Приложение должно установить D3DRS \_ куллмоде в значение D3DCULL \_ None, чтобы включить режим с двумя сторонами набора элементов.</span><span class="sxs-lookup"><span data-stu-id="0a07c-486">The application should set D3DRS\_CULLMODE to D3DCULL\_NONE to enable two-sided stencil mode.</span></span> <span data-ttu-id="0a07c-487">Если порядок заполнения треугольника является по часовой стрелке, \_ будут использоваться операции с набором элементов D3DRS \* .</span><span class="sxs-lookup"><span data-stu-id="0a07c-487">If the triangle winding order is clockwise, the D3DRS\_STENCIL\* operations will be used.</span></span> <span data-ttu-id="0a07c-488">Если порядок поворота имеет значение против часовой стрелки, \_ \_ будут использоваться операции с набором элементов D3DRS CCW \* .</span><span class="sxs-lookup"><span data-stu-id="0a07c-488">If the winding order is counterclockwise, the D3DRS\_CCW\_STENCIL\* operations will be used.</span></span>

<span data-ttu-id="0a07c-489">Чтобы узнать, поддерживается ли двусторонний набор элементов, проверьте элемент СтенЦилкапс в [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) для D3DSTENCILCAPS \_ твосидед.</span><span class="sxs-lookup"><span data-stu-id="0a07c-489">To see if two-sided stencil is supported, check the StencilCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) for D3DSTENCILCAPS\_TWOSIDED.</span></span> <span data-ttu-id="0a07c-490">См. также [D3DSTENCILCAPS](d3dstencilcaps.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-490">See also [D3DSTENCILCAPS](d3dstencilcaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS \_ CCW \_ стенЦилфаил**</span><span class="sxs-lookup"><span data-stu-id="0a07c-491"><span id="D3DRS_CCW_STENCILFAIL"></span><span id="d3drs_ccw_stencilfail"></span>**D3DRS\_CCW\_STENCILFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-492">Операция с набором элементов, выполняемая при сбое теста трафарета CCW.</span><span class="sxs-lookup"><span data-stu-id="0a07c-492">Stencil operation to perform if CCW stencil test fails.</span></span> <span data-ttu-id="0a07c-493">Значения из перечисляемого типа [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-493">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="0a07c-494">Значение по умолчанию — D3DSTENCILOP \_ держитесь.</span><span class="sxs-lookup"><span data-stu-id="0a07c-494">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS \_ CCW \_ стенЦилзфаил**</span><span class="sxs-lookup"><span data-stu-id="0a07c-495"><span id="D3DRS_CCW_STENCILZFAIL"></span><span id="d3drs_ccw_stencilzfail"></span>**D3DRS\_CCW\_STENCILZFAIL**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-496">Операция с набором элементов, которую необходимо выполнить, если пройден тест шаблона CCW и не пройден z-тест.</span><span class="sxs-lookup"><span data-stu-id="0a07c-496">Stencil operation to perform if CCW stencil test passes and z-test fails.</span></span> <span data-ttu-id="0a07c-497">Значения из перечисляемого типа [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-497">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="0a07c-498">Значение по умолчанию — D3DSTENCILOP \_ держитесь.</span><span class="sxs-lookup"><span data-stu-id="0a07c-498">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS \_ CCW \_ стенЦилпасс**</span><span class="sxs-lookup"><span data-stu-id="0a07c-499"><span id="D3DRS_CCW_STENCILPASS"></span><span id="d3drs_ccw_stencilpass"></span>**D3DRS\_CCW\_STENCILPASS**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-500">Операция с набором элементов, выполняемая, если пройден и набор элементов, и z-тесты.</span><span class="sxs-lookup"><span data-stu-id="0a07c-500">Stencil operation to perform if both CCW stencil and z-tests pass.</span></span> <span data-ttu-id="0a07c-501">Значения из перечисляемого типа [**D3DSTENCILOP**](./d3dstencilop.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-501">Values are from the [**D3DSTENCILOP**](./d3dstencilop.md) enumerated type.</span></span> <span data-ttu-id="0a07c-502">Значение по умолчанию — D3DSTENCILOP \_ держитесь.</span><span class="sxs-lookup"><span data-stu-id="0a07c-502">The default value is D3DSTENCILOP\_KEEP.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS \_ CCW \_ стенЦилфунк**</span><span class="sxs-lookup"><span data-stu-id="0a07c-503"><span id="D3DRS_CCW_STENCILFUNC"></span><span id="d3drs_ccw_stencilfunc"></span>**D3DRS\_CCW\_STENCILFUNC**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-504">Функция сравнения.</span><span class="sxs-lookup"><span data-stu-id="0a07c-504">The comparison function.</span></span> <span data-ttu-id="0a07c-505">Проверка трафаретного шаблона CCW передается, если функция шаблона ((ref & Mask) (маска шаблона &)) имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-505">CCW stencil test passes if ((ref & mask) stencil function (stencil & mask)) is **TRUE**.</span></span> <span data-ttu-id="0a07c-506">Значения из перечисляемого типа [**D3DCMPFUNC**](./d3dcmpfunc.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-506">Values are from the [**D3DCMPFUNC**](./d3dcmpfunc.md) enumerated type.</span></span> <span data-ttu-id="0a07c-507">Значение по умолчанию — D3DCMP \_ Always.</span><span class="sxs-lookup"><span data-stu-id="0a07c-507">The default value is D3DCMP\_ALWAYS.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS \_ COLORWRITEENABLE1**</span><span class="sxs-lookup"><span data-stu-id="0a07c-508"><span id="D3DRS_COLORWRITEENABLE1"></span><span id="d3drs_colorwriteenable1"></span>**D3DRS\_COLORWRITEENABLE1**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-509">Дополнительные значения Колорвритинабле для устройств.</span><span class="sxs-lookup"><span data-stu-id="0a07c-509">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="0a07c-510">См. раздел D3DRS \_ колорвритинабле.</span><span class="sxs-lookup"><span data-stu-id="0a07c-510">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="0a07c-511">Эта функция доступна, если бит D3DPMISCCAPS \_ индепендентвритемаскс может быть установлен в элементе примитивемисккапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) для устройства.</span><span class="sxs-lookup"><span data-stu-id="0a07c-511">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="0a07c-512">Значение по умолчанию — 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-512">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS \_ COLORWRITEENABLE2**</span><span class="sxs-lookup"><span data-stu-id="0a07c-513"><span id="D3DRS_COLORWRITEENABLE2"></span><span id="d3drs_colorwriteenable2"></span>**D3DRS\_COLORWRITEENABLE2**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-514">Дополнительные значения Колорвритинабле для устройств.</span><span class="sxs-lookup"><span data-stu-id="0a07c-514">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="0a07c-515">См. раздел D3DRS \_ колорвритинабле.</span><span class="sxs-lookup"><span data-stu-id="0a07c-515">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="0a07c-516">Эта функция доступна, если бит D3DPMISCCAPS \_ индепендентвритемаскс может быть установлен в элементе примитивемисккапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) для устройства.</span><span class="sxs-lookup"><span data-stu-id="0a07c-516">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="0a07c-517">Значение по умолчанию — 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-517">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS \_ COLORWRITEENABLE3**</span><span class="sxs-lookup"><span data-stu-id="0a07c-518"><span id="D3DRS_COLORWRITEENABLE3"></span><span id="d3drs_colorwriteenable3"></span>**D3DRS\_COLORWRITEENABLE3**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-519">Дополнительные значения Колорвритинабле для устройств.</span><span class="sxs-lookup"><span data-stu-id="0a07c-519">Additional ColorWriteEnable values for the devices.</span></span> <span data-ttu-id="0a07c-520">См. раздел D3DRS \_ колорвритинабле.</span><span class="sxs-lookup"><span data-stu-id="0a07c-520">See D3DRS\_COLORWRITEENABLE.</span></span> <span data-ttu-id="0a07c-521">Эта функция доступна, если бит D3DPMISCCAPS \_ индепендентвритемаскс может быть установлен в элементе примитивемисккапс структуры [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) для устройства.</span><span class="sxs-lookup"><span data-stu-id="0a07c-521">This functionality is available if the D3DPMISCCAPS\_INDEPENDENTWRITEMASKS capabilities bit is set in the PrimitiveMiscCaps member of the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure for the device.</span></span> <span data-ttu-id="0a07c-522">Значение по умолчанию — 0x0000000f.</span><span class="sxs-lookup"><span data-stu-id="0a07c-522">The default value is 0x0000000f.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS \_ блендфактор**</span><span class="sxs-lookup"><span data-stu-id="0a07c-523"><span id="D3DRS_BLENDFACTOR"></span><span id="d3drs_blendfactor"></span>**D3DRS\_BLENDFACTOR**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-524">[**D3DCOLOR**](d3dcolor.md) используется для константного коэффициента смешения во время альфа-смешения.</span><span class="sxs-lookup"><span data-stu-id="0a07c-524">[**D3DCOLOR**](d3dcolor.md) used for a constant blend-factor during alpha blending.</span></span> <span data-ttu-id="0a07c-525">Эта функция доступна, если бит D3DPBLENDCAPS \_ блендфактор может быть установлен в сркблендкапс член [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) или **дестблендкапс D3DCAPS9**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-525">This functionality is available if the D3DPBLENDCAPS\_BLENDFACTOR capabilities bit is set in the SrcBlendCaps member of [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) or the DestBlendCaps member of **D3DCAPS9**.</span></span> <span data-ttu-id="0a07c-526">См. [**D3DRENDERSTATETYPE**]().</span><span class="sxs-lookup"><span data-stu-id="0a07c-526">See [**D3DRENDERSTATETYPE**]().</span></span> <span data-ttu-id="0a07c-527">Значение по умолчанию — 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="0a07c-527">The default value is 0xffffffff.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS \_ сргбвритинабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-528"><span id="D3DRS_SRGBWRITEENABLE"></span><span id="d3drs_srgbwriteenable"></span>**D3DRS\_SRGBWRITEENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-529">Включение подготовки к просмотру для исправления гаммы в sRGB.</span><span class="sxs-lookup"><span data-stu-id="0a07c-529">Enable render-target writes to be gamma corrected to sRGB.</span></span> <span data-ttu-id="0a07c-530">Формат должен предоставлять D3DUSAGE \_ сргбврите.</span><span class="sxs-lookup"><span data-stu-id="0a07c-530">The format must expose D3DUSAGE\_SRGBWRITE.</span></span> <span data-ttu-id="0a07c-531">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-531">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS \_ депсбиас**</span><span class="sxs-lookup"><span data-stu-id="0a07c-532"><span id="D3DRS_DEPTHBIAS"></span><span id="d3drs_depthbias"></span>**D3DRS\_DEPTHBIAS**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-533">Значение с плавающей запятой, используемое для сравнения значений глубины.</span><span class="sxs-lookup"><span data-stu-id="0a07c-533">A floating-point value that is used for comparison of depth values.</span></span> <span data-ttu-id="0a07c-534">См. раздел [смещение глубины (Direct3D 9)](depth-bias.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-534">See [Depth Bias (Direct3D 9)](depth-bias.md).</span></span> <span data-ttu-id="0a07c-535">Значение по умолчанию — 0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-535">The default value is 0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS \_ WRAP8**</span><span class="sxs-lookup"><span data-stu-id="0a07c-536"><span id="D3DRS_WRAP8"></span><span id="d3drs_wrap8"></span>**D3DRS\_WRAP8**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-537">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-537">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS \_ WRAP9**</span><span class="sxs-lookup"><span data-stu-id="0a07c-538"><span id="D3DRS_WRAP9"></span><span id="d3drs_wrap9"></span>**D3DRS\_WRAP9**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-539">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-539">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS \_ WRAP10**</span><span class="sxs-lookup"><span data-stu-id="0a07c-540"><span id="D3DRS_WRAP10"></span><span id="d3drs_wrap10"></span>**D3DRS\_WRAP10**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-541">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-541">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS \_ WRAP11**</span><span class="sxs-lookup"><span data-stu-id="0a07c-542"><span id="D3DRS_WRAP11"></span><span id="d3drs_wrap11"></span>**D3DRS\_WRAP11**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-543">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-543">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS \_ WRAP12**</span><span class="sxs-lookup"><span data-stu-id="0a07c-544"><span id="D3DRS_WRAP12"></span><span id="d3drs_wrap12"></span>**D3DRS\_WRAP12**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-545">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-545">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS \_ WRAP13**</span><span class="sxs-lookup"><span data-stu-id="0a07c-546"><span id="D3DRS_WRAP13"></span><span id="d3drs_wrap13"></span>**D3DRS\_WRAP13**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-547">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-547">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS \_ WRAP14**</span><span class="sxs-lookup"><span data-stu-id="0a07c-548"><span id="D3DRS_WRAP14"></span><span id="d3drs_wrap14"></span>**D3DRS\_WRAP14**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-549">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-549">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS \_ WRAP15**</span><span class="sxs-lookup"><span data-stu-id="0a07c-550"><span id="D3DRS_WRAP15"></span><span id="d3drs_wrap15"></span>**D3DRS\_WRAP15**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-551">См. раздел D3DRS \_ WRAP0.</span><span class="sxs-lookup"><span data-stu-id="0a07c-551">See D3DRS\_WRAP0.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS \_ сепаратеалфабленденабле**</span><span class="sxs-lookup"><span data-stu-id="0a07c-552"><span id="D3DRS_SEPARATEALPHABLENDENABLE"></span><span id="d3drs_separatealphablendenable"></span>**D3DRS\_SEPARATEALPHABLENDENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-553">**Значение true** включает отдельный режим смешения для альфа-канала.</span><span class="sxs-lookup"><span data-stu-id="0a07c-553">**TRUE** enables the separate blend mode for the alpha channel.</span></span> <span data-ttu-id="0a07c-554">Значение по умолчанию — **false**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-554">The default value is **FALSE**.</span></span>

<span data-ttu-id="0a07c-555">Если задано **значение false**, то коэффициенты смешения и операции, применяемые к альфа-каналу, должны быть такими же, как и для цвета.</span><span class="sxs-lookup"><span data-stu-id="0a07c-555">When set to **FALSE**, the render-target blending factors and operations applied to alpha are forced to be the same as those defined for color.</span></span> <span data-ttu-id="0a07c-556">Этот режим фактически **прикован в реализации** , не устанавливая ограничение D3DPMISCCAPS \_ сепаратеалфабленд.</span><span class="sxs-lookup"><span data-stu-id="0a07c-556">This mode is effectively hardwired to **FALSE** on implementations that don't set the cap D3DPMISCCAPS\_SEPARATEALPHABLEND.</span></span> <span data-ttu-id="0a07c-557">См. [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-557">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

<span data-ttu-id="0a07c-558">Тип отдельного альфа-смешения определяется с помощью \_ состояний отрисовки D3DRS сркблендалфа и D3DRS \_ дестблендалфа.</span><span class="sxs-lookup"><span data-stu-id="0a07c-558">The type of separate alpha blending is determined by the D3DRS\_SRCBLENDALPHA and D3DRS\_DESTBLENDALPHA render states.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS \_ сркблендалфа**</span><span class="sxs-lookup"><span data-stu-id="0a07c-559"><span id="D3DRS_SRCBLENDALPHA"></span><span id="d3drs_srcblendalpha"></span>**D3DRS\_SRCBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-560">Один член перечисляемого типа [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-560">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="0a07c-561">Это значение игнорируется, если D3DRS \_ сепаратеалфабленденабле имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-561">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="0a07c-562">Значение по умолчанию — D3DBLEND \_ 1.</span><span class="sxs-lookup"><span data-stu-id="0a07c-562">The default value is D3DBLEND\_ONE.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS \_ дестблендалфа**</span><span class="sxs-lookup"><span data-stu-id="0a07c-563"><span id="D3DRS_DESTBLENDALPHA"></span><span id="d3drs_destblendalpha"></span>**D3DRS\_DESTBLENDALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-564">Один член перечисляемого типа [**D3DBLEND**](./d3dblend.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-564">One member of the [**D3DBLEND**](./d3dblend.md) enumerated type.</span></span> <span data-ttu-id="0a07c-565">Это значение игнорируется, если D3DRS \_ сепаратеалфабленденабле имеет **значение true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-565">This value is ignored unless D3DRS\_SEPARATEALPHABLENDENABLE is **TRUE**.</span></span> <span data-ttu-id="0a07c-566">Значение по умолчанию — D3DBLEND \_ нуль.</span><span class="sxs-lookup"><span data-stu-id="0a07c-566">The default value is D3DBLEND\_ZERO.</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS \_ блендопалфа**</span><span class="sxs-lookup"><span data-stu-id="0a07c-567"><span id="D3DRS_BLENDOPALPHA"></span><span id="d3drs_blendopalpha"></span>**D3DRS\_BLENDOPALPHA**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-568">Значение, используемое для выбора арифметической операции, применяемой к отдельной альфа-смешению, когда для состояния отрисовки D3DRS \_ сепаратеалфабленденабле задано **значение true**.</span><span class="sxs-lookup"><span data-stu-id="0a07c-568">Value used to select the arithmetic operation applied to separate alpha blending when the render state, D3DRS\_SEPARATEALPHABLENDENABLE, is set to **TRUE**.</span></span>

<span data-ttu-id="0a07c-569">Допустимые значения определяются перечисляемым типом [**D3DBLENDOP**](./d3dblendop.md) .</span><span class="sxs-lookup"><span data-stu-id="0a07c-569">Valid values are defined by the [**D3DBLENDOP**](./d3dblendop.md) enumerated type.</span></span> <span data-ttu-id="0a07c-570">Значение по умолчанию — D3DBLENDOP \_ Add.</span><span class="sxs-lookup"><span data-stu-id="0a07c-570">The default value is D3DBLENDOP\_ADD.</span></span>

<span data-ttu-id="0a07c-571">Если \_ возможность устройства D3DPMISCCAPS блендоп не поддерживается, \_ добавляется D3DBLENDOP Add.</span><span class="sxs-lookup"><span data-stu-id="0a07c-571">If the D3DPMISCCAPS\_BLENDOP device capability is not supported, then D3DBLENDOP\_ADD is performed.</span></span> <span data-ttu-id="0a07c-572">См. [D3DPMISCCAPS](d3dpmisccaps.md).</span><span class="sxs-lookup"><span data-stu-id="0a07c-572">See [D3DPMISCCAPS](d3dpmisccaps.md).</span></span>

</dd> <dt>

<span data-ttu-id="0a07c-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS \_ Force \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="0a07c-573"><span id="D3DRS_FORCE_DWORD"></span><span id="d3drs_force_dword"></span>**D3DRS\_FORCE\_DWORD**</span></span>
</dt> <dd>

<span data-ttu-id="0a07c-574">Заставляет это перечисление компилироваться до 32 бит в размере.</span><span class="sxs-lookup"><span data-stu-id="0a07c-574">Forces this enumeration to compile to 32 bits in size.</span></span> <span data-ttu-id="0a07c-575">Без этого значения некоторые компиляторы позволяли бы компилировать это перечисление до размера, отличного от 32 бит.</span><span class="sxs-lookup"><span data-stu-id="0a07c-575">Without this value, some compilers would allow this enumeration to compile to a size other than 32 bits.</span></span> <span data-ttu-id="0a07c-576">Это значение не используется.</span><span class="sxs-lookup"><span data-stu-id="0a07c-576">This value is not used.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0a07c-577">Комментарии</span><span class="sxs-lookup"><span data-stu-id="0a07c-577">Remarks</span></span>



| <span data-ttu-id="0a07c-578">Состояния отрисовки</span><span class="sxs-lookup"><span data-stu-id="0a07c-578">Render States</span></span>        |                    |
|----------------------|--------------------|
| <span data-ttu-id="0a07c-579">PS \_ 1 \_ 1 – PS \_ 1 \_ 3</span><span class="sxs-lookup"><span data-stu-id="0a07c-579">ps\_1\_1 to ps\_1\_3</span></span> | <span data-ttu-id="0a07c-580">4 образцов текстуры</span><span class="sxs-lookup"><span data-stu-id="0a07c-580">4 texture samplers</span></span> |



 

<span data-ttu-id="0a07c-581">Direct3D определяет \_ константу D3DRENDERSTATE врапбиас в качестве удобства для включения или отключения переноса текстур на основе нуля целого числа набора координат текстуры (вместо явного использования одного из значений состояния D3DRS, переданных по \_ словам n).</span><span class="sxs-lookup"><span data-stu-id="0a07c-581">Direct3D defines the D3DRENDERSTATE\_WRAPBIAS constant as a convenience for applications to enable or disable texture wrapping, based on the zero-based integer of a texture coordinate set (rather than explicitly using one of the D3DRS\_WRAP n state values).</span></span> <span data-ttu-id="0a07c-582">Добавьте значение D3DRENDERSTATE \_ врапбиас в Отсчитываемый от нуля индекс набора координат текстуры, чтобы вычислить \_ значение D3DRS Wrap n, соответствующее этому индексу, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="0a07c-582">Add the D3DRENDERSTATE\_WRAPBIAS value to the zero-based index of a texture coordinate set to calculate the D3DRS\_WRAP n value that corresponds to that index, as shown in the following example.</span></span>


```
// Enable U/V wrapping for textures that use the texture 
// coordinate set at the index within the dwIndex variable
    
HRESULT hr = pd3dDevice->SetRenderState(
dwIndex + D3DRENDERSTATE_WRAPBIAS,  
D3DWRAPCOORD_0 | D3DWRAPCOORD_1);
     
// If dwIndex is 3, the value that results from 
// the addition equals D3DRS_WRAP3 (131)
```



## <a name="requirements"></a><span data-ttu-id="0a07c-583">Требования</span><span class="sxs-lookup"><span data-stu-id="0a07c-583">Requirements</span></span>



| <span data-ttu-id="0a07c-584">Требование</span><span class="sxs-lookup"><span data-stu-id="0a07c-584">Requirement</span></span> | <span data-ttu-id="0a07c-585">Значение</span><span class="sxs-lookup"><span data-stu-id="0a07c-585">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0a07c-586">Header</span><span class="sxs-lookup"><span data-stu-id="0a07c-586">Header</span></span><br/> | <dl> <span data-ttu-id="0a07c-587"><dt>D3D9Types. h</dt></span><span class="sxs-lookup"><span data-stu-id="0a07c-587"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0a07c-588">См. также раздел</span><span class="sxs-lookup"><span data-stu-id="0a07c-588">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0a07c-589">Перечисления Direct3D</span><span class="sxs-lookup"><span data-stu-id="0a07c-589">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="0a07c-590">**IDirect3DDevice9:: Жетрендерстате**</span><span class="sxs-lookup"><span data-stu-id="0a07c-590">**IDirect3DDevice9::GetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-getrenderstate)
</dt> <dt>

[<span data-ttu-id="0a07c-591">**IDirect3DDevice9::SetRenderState**</span><span class="sxs-lookup"><span data-stu-id="0a07c-591">**IDirect3DDevice9::SetRenderState**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)
</dt> </dl>

 

 
