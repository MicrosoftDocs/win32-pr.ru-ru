---
description: Блок состояния можно использовать для захвата только состояния пикселя (см. раздел состояния сохранение и восстановление состояния (Direct3D 9)).
ms.assetid: 30624c0a-e30f-4383-bc0c-b43f42403e72
title: Сохранение состояния пикселя с помощью Статеблокк (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80741d9f17939d5795163a3e84c58bcdb9003c70
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104537943"
---
# <a name="saving-pixel-state-with-a-stateblock-direct3d-9"></a>Сохранение состояния пикселя с помощью Статеблокк (Direct3D 9)

Блок состояния можно использовать для захвата только состояния пикселя (см. раздел [состояния сохранение и восстановление состояния (Direct3D 9)](state-blocks-save-and-restore-state.md)). Следующее состояние — состояние пикселей:

-   Состояние отрисовки пикселя (см. [пиксельный конвейер: состояние рендеринга](#pixel-pipeline-render-state)).
-   Состояние текстуры пикселя (см. [пиксельный конвейер: состояние текстуры](#pixel-pipeline-texture-state)).
-   Состояние образца пикселей (см. раздел [конвейер: состояние образца](#pixel-pipeline-sampler-state)).
-   Текущий шейдер пикселей и все константы шейдера пикселей.

Чтобы записать состояние пикселей с блоком состояния, укажите D3DSBT \_ пикселстате при вызове [**IDirect3DDevice9:: креатестатеблокк**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createstateblock).

## <a name="pixel-pipeline-render-state"></a>Конвейер пикселей: состояние рендеринга

Состояния визуализации устройства влияют на поведение почти каждой части конвейера. Состояния отрисовки задаются путем вызова [**IDirect3DDevice9:: сетрендерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate).

В следующей таблице перечислены все состояния рендеринга, настроенные для состояния пикселей.



| Состояния отрисовки                              | Значение по умолчанию      |
|--------------------------------------------|--------------------|
| D3DRS \_ зенабле                             | D3DZB \_ false       |
| D3DRS \_ спекуларенабле                      | **FALSE**          |
| [**D3DFILLMODE**](./d3dfillmode.md)   | D3DFILL \_     |
| [**D3DSHADEMODE**](./d3dshademode.md) | D3DSHADE метод \_ Гуро  |
| D3DRS \_ звритинабле                        | **TRUE**           |
| D3DRS \_ алфатестенабле                     | **FALSE**          |
| D3DRS \_ ластпиксел                           | **TRUE**           |
| D3DRS \_ сркбленд                            | D3DBLEND \_ один      |
| D3DRS \_ дестбленд                           | D3DBLEND \_ 0     |
| D3DRS \_ зфунк                               | D3DCMP \_ лессекуал  |
| D3DRS \_ алфареф                            | 0                  |
| D3DRS \_ алфафунк                           | D3DCMP \_ всегда     |
| D3DRS \_ дисеренабле                        | **FALSE**          |
| D3DRS \_ фогстарт                            | 0                  |
| D3DRS \_ фоженд                              | 1                  |
| D3DRS \_ фогденсити                          | 1                  |
| D3DRS \_ алфабленденабле                    | **FALSE**          |
| D3DRS \_ депсбиас                           | 0                  |
| D3DRS \_ стенЦиленабле                       | **FALSE**          |
| D3DRS \_ стенЦилфаил                         | D3DSTENCILOP \_ |
| D3DRS \_ стенЦилзфаил                        | D3DSTENCILOP \_ |
| D3DRS \_ стенЦилпасс                         | D3DSTENCILOP \_ |
| D3DRS \_ стенЦилфунк                         | D3DCMP \_ всегда     |
| D3DRS \_ стенЦилреф                          | 0                  |
| D3DRS \_ стенЦилмаск                         | 0xFFFFFFFF         |
| D3DRS \_ стенЦилвритемаск                    | 0xFFFFFFFF         |
| D3DRS \_ текстурефактор                       | 0xFFFFFFFF         |
| D3DRS \_ WRAP0                               | 0                  |
| D3DRS \_ WRAP1                               | 0                  |
| D3DRS \_ WRAP2                               | 0                  |
| D3DRS \_ WRAP3                               | 0                  |
| D3DRS \_ WRAP4                               | 0                  |
| D3DRS \_ WRAP5                               | 0                  |
| D3DRS \_ WRAP6                               | 0                  |
| D3DRS \_ WRAP7                               | 0                  |
| D3DRS \_ WRAP8                               | 0                  |
| D3DRS \_ WRAP9                               | 0                  |
| D3DRS \_ WRAP10                              | 0                  |
| D3DRS \_ WRAP11                              | 0                  |
| D3DRS \_ WRAP12                              | 0                  |
| D3DRS \_ WRAP13                              | 0                  |
| D3DRS \_ WRAP14                              | 0                  |
| D3DRS \_ WRAP15                              | 0                  |
| D3DRS \_ локалвиевер                         | **TRUE**           |
| D3DRS \_ емиссивематериалсаурце              | \_Материал D3DMCS   |
| D3DRS \_ амбиентматериалсаурце               | \_Материал D3DMCS   |
| D3DRS \_ диффусематериалсаурце               | D3DMCS \_ COLOR1     |
| D3DRS \_ спекуларматериалсаурце              | D3DMCS \_ COLOR2     |
| D3DRS \_ колорвритинабле                    | 0x0000000f         |
| [**D3DBLENDOP**](./d3dblendop.md)     | D3DBLENDOP \_ Добавить    |
| D3DRS \_ сЦиссортестенабле                   | **FALSE**          |
| D3DRS \_ слопескаледепсбиас                 | 0                  |
| D3DRS \_ антиалиаседлининабле               | **FALSE**          |
| D3DRS \_ твосидедстенЦилмоде                 | **FALSE**          |
| D3DRS \_ CCW \_ стенЦилфаил                    | D3DSTENCILOP \_ |
| D3DRS \_ CCW \_ стенЦилзфаил                   | D3DSTENCILOP \_ |
| D3DRS \_ CCW \_ стенЦилпасс                    | D3DSTENCILOP \_ |
| D3DRS \_ CCW \_ стенЦилфунк                    | D3DCMP \_ всегда     |
| D3DRS \_ COLORWRITEENABLE1                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE2                   | 0x0000000f         |
| D3DRS \_ COLORWRITEENABLE3                   | 0x0000000f         |
| D3DRS \_ блендфактор                         | 0xFFFFFFFF         |
| D3DRS \_ сргбвритинабле                     | 0                  |
| D3DRS \_ сепаратеалфабленденабле            | **FALSE**          |
| D3DRS \_ сркблендалфа                       | D3DBLEND \_ один      |
| D3DRS \_ дестблендалфа                      | D3DBLEND \_ 0     |
| D3DRS \_ блендопалфа                        | D3DBLENDOP \_ Добавить    |



 

## <a name="pixel-pipeline-sampler-state"></a>Конвейер пикселей: состояние образца

Состояния образцов контролируют связанные с выборкой разделы, такие как фильтрация, мозаичное заполнение и режимы адресации текстуры. Используйте [**IDirect3DDevice9:: сетсамплерстате**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) , чтобы настроить состояние выборки (включая ту, которая используется в блоке тесселяции в качестве образца карт смещения). Состояния образца были переименованы с \_ префиксом "D3DSAMP", чтобы включить обнаружение ошибок во время компиляции при переносе из DirectX 8.

В следующей таблице приведены все состояния образца, которые настроили состояние пикселей.



| Состояния образцов         | Значение по умолчанию     |
|------------------------|-------------------|
| D3DSAMP \_ аддрессу      | D3DTADDRESS \_ Перенос |
| D3DSAMP \_ аддрессв      | D3DTADDRESS \_ Перенос |
| D3DSAMP \_ аддрессв      | D3DTADDRESS \_ Перенос |
| D3DSAMP \_ BORDERCOLOR   | 0x00000000        |
| D3DSAMP \_ магфилтер     | \_Точка D3DTEXF    |
| D3DSAMP \_ минфилтер     | \_Точка D3DTEXF    |
| D3DSAMP \_ мипфилтер     | D3DTEXF \_ None     |
| D3DSAMP \_ мипмаплодбиас | 0                 |
| D3DSAMP \_ максмиплевел   | 0                 |
| D3DSAMP \_ максанисотропи | 1                 |
| D3DSAMP \_ сргбтекстуре   | 0                 |
| D3DSAMP \_ елементиндекс  | 0                 |



 

## <a name="pixel-pipeline-texture-state"></a>Пиксельный конвейер: состояние текстуры

Состояние текстуры управляет операциями смешения текстур для многотекстурного смешения. Используйте [**IDirect3DDevice9:: сеттекстурестажестате**](/windows/desktop/api) для настройки стадий текстуры. Используйте [**IDirect3DDevice9:: сеттекстуре**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) , чтобы связать текстуру с стадией образца.

В следующей таблице приведены все состояния текстур, которые настроили состояние пикселей.



| Состояния текстуры                | Значение по умолчанию    |
|-------------------------------|------------------|
| D3DTSS \_ колороп               | \_Отключение D3DTOP  |
| D3DTSS \_ COLORARG1             | \_Текстура D3DTA   |
| D3DTSS \_ COLORARG2             | D3DTA \_ текущий   |
| D3DTSS \_ алфаоп               | \_Отключение D3DTOP  |
| D3DTSS \_ ALPHAARG1             | \_Текстура D3DTA   |
| D3DTSS \_ ALPHAARG2             | D3DTA \_ текущий   |
| D3DTSS \_ BUMPENVMAT00          | 0                |
| D3DTSS \_ BUMPENVMAT01          | 0                |
| D3DTSS \_ BUMPENVMAT10          | 0                |
| D3DTSS \_ BUMPENVMAT11          | 0                |
| D3DTSS \_ текскурдиндекс         | 0                |
| D3DTSS \_ бумпенвлскале         | 0                |
| D3DTSS \_ бумпенвлоффсет        | 0                |
| D3DTSS \_ текстуретрансформфлагс | \_Отключение D3DTTFF |
| D3DTSS \_ COLORARG0             | D3DTA \_ текущий   |
| D3DTSS \_ ALPHAARG0             | D3DTA \_ текущий   |
| D3DTSS \_ ресултарг             | D3DTA \_ текущий   |



 

## <a name="related-topics"></a>См. также

<dl> <dt>

[Состояние блоков сохранения и восстановления](state-blocks-save-and-restore-state.md)
</dt> </dl>

 

 
