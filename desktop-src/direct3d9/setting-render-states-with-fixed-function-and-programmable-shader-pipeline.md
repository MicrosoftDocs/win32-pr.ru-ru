---
title: Установка состояния устройства для конвейеров с фиксированной функцией и шейдеров
description: В этом разделе приведены основные различия между заданием состояния устройства с помощью фиксированной функции и программируемого конвейера шейдера.
ms.assetid: FF0F2A97-F75A-4AF0-8F5A-EA687523E753
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e2d5c0e0ba9e1ac890468654d348b0f8b316f64
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104262488"
---
# <a name="set-device-state-on-fixed-function-shader-pipelines"></a>Установка состояния устройства для конвейеров с фиксированной функцией и шейдеров

В этом разделе приведены основные различия между заданием состояния устройства с помощью фиксированной функции и программируемого конвейера шейдера.

Ниже приведены состояния устройств, которые можно задать только для конвейера с фиксированной функцией.

-   Преобразование и освещение с фиксированной функцией [**: IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) with D3DRS \_ шадемоде, D3DRS спекуларенабле \_ , D3DRS \_ Lighting, D3DRS \_ окружающий, D3DRS колорвертекс, D3DRS \_ \_ ЛОКАЛВИЕВЕР, D3DRS \_ нормализенормалс, D3DRS \_ DIFFUSEMATERIALSOURCE, D3DRS \_ SPECULARMATERIALSOURCE, D3DRS AMBIENTMATERIALSOURCE, D3DRS EMISSIVEMATERIALSOURCE, D3DRS VERTEXBLEND, D3DRS INDEXEDVERTEXBLENDENABLE, D3DRS TWEENFACTOR, IDirect3DDevice9:: IDirect3DDevice9, MultiplyTransform \_ \_ \_ \_ \_ [**:: IDirect3DDevice9**](/windows/desktop/api) [](/windows/desktop/api), [**SetFVF::**](/windows/desktop/api) [](/windows/desktop/api) [](/windows/desktop/api) [](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform) , IDirect3DDevice9:: SetLight, IDirect3DDevice9:: SetMaterial, IDirect3DDevice9: SetTransform
-   Шейдер пикселей с фиксированной функцией: [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) с D3DRS \_ текстурефактор, [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)
-   Туман: [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) with D3DRS \_ фоженабле, D3DRS \_ фогколор, D3DRS \_ ФОГТАБЛЕМОДЕ, D3DRS \_ фогстарт, D3DRS \_ фоженд, D3DRS \_ фогденсити, D3DRS \_ ранжефоженабле, D3DRS \_ FOGVERTEXMODE

Ниже приведены состояния отрисовки устройства, которые можно задать с помощью [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate) как для фиксированных, так и для программируемых конвейеров шейдера:

-   Состояние целевого объекта прорисовки: D3DRS \_ колорвритинабле, D3DRS \_ COLORWRITEENABLE1, D3DRS \_ COLORWRITEENABLE2, D3DRS \_ COLORWRITEENABLE3, D3DRS \_ сргбвритинабле
-   Состояние глубины: D3DRS \_ зенабле, D3DRS \_ ЗВРИТИНАБЛЕ, D3DRS \_ зфунк, D3DRS \_ слопескаледепсбиас, D3DRS \_ депсбиас
-   Состояние набора элементов: D3DRS \_ стенЦиленабле, D3DRS \_ СТЕНЦИЛФАИЛ, D3DRS \_ стенЦилзфаил, D3DRS \_ стенЦилпасс, D3DRS \_ СТЕНЦИЛФУНК, D3DRS \_ стенЦилреф, D3DRS \_ стенЦилмаск, D3DRS \_ STENCILWRITEMASK, D3DRS \_ TWOSIDEDSTENCILMODE, D3DRS \_ CCW \_ STENCILFAIL, D3DRS \_ CCW \_ STENCILZFAIL, D3DRS \_ CCW \_ STENCILPASS, D3DRS \_ CCW \_ STENCILFUNC
-   Альфа-смешение: D3DRS \_ сркбленд, D3DRS \_ ДЕСТБЛЕНД, D3DRS \_ блендоп, D3DRS \_ блендфактор, D3DRS \_ СЕПАРАТЕАЛФАБЛЕНДЕНАБЛЕ, D3DRS \_ сркблендалфа, D3DRS \_ дестблендалфа, D3DRS \_ BLENDOPALPHA
-   Альфа-тест: D3DRS \_ алфатестенабле, D3DRS \_ АЛФАРЕФ, D3DRS \_ алфафунк
-   Состояние средства программной прорисовки: D3DRS \_ филлмоде, D3DRS \_ ЛАСТПИКСЕЛ, D3DRS \_ дисеренабле (16-разрядные поверхности)
-   Отбор: D3DRS \_ куллмоде
-   Обрезка: D3DRS \_ Обрезка, D3DRS \_ клиппланинабле
-   Ножницы: D3DRS \_ сЦиссортестенабле
-   Эталонные пробы: D3DRS \_ WRAP0, D3DRS \_ WRAP1, D3DRS \_ WRAP2, D3DRS \_ WRAP3, D3DRS \_ WRAP4, D3DRS \_ WRAP5, D3DRS \_ WRAP6, D3DRS \_ WRAP7, D3DRS \_ WRAP8, D3DRS \_ WRAP9, D3DRS \_ WRAP10, D3DRS \_ WRAP11, D3DRS \_ WRAP12, D3DRS \_ WRAP13, D3DRS \_ WRAP14, \_ D3DRS WRAP15
-   Сглаживание: D3DRS \_ мултисамплеантиалиас, D3DRS \_ МУЛТИСАМПЛЕМАСК, D3DRS \_ антиалиаседлининабле
-   Спрайты для точек: D3DRS \_ POINTSIZE, D3DRS \_ POINTSIZE \_ min, D3DRS \_ поинтспритинабле, D3DRS \_ POINTSIZE \_ MAXD3DRS \_ поинтскалинабле, D3DRS \_ поинтскале \_ A, D3DRS \_ поинтскале \_ B, D3DRS \_ поинтскале \_ C
-   N-патчs: D3DRS \_ патчеджестиле, D3DRS \_ ПОСИТИОНДЕГРИ, D3DRS \_ нормалдегри, D3DRS \_ минтесселлатионлевел, D3DRS \_ макстесселлатионлевел, D3DRS \_ ADAPTIVETESS \_ X, D3DRS \_ ADAPTIVETESS \_ Y, D3DRS \_ ADAPTIVETESS \_ Z, D3DRS \_ ADAPTIVETESS \_ W, D3DRS \_ ENABLEADAPTIVETESSELLATION

## <a name="related-topics"></a>См. также

<dl> <dt>

[Дополнительные разделы](advanced-topics.md)
</dt> </dl>

 

 
