---
title: Указание целевых объектов компилятора
description: Здесь перечислены целевые объекты для различных профилей, которые поддерживаются D3DCompile \ функции и компилятор HLSL.
ms.assetid: 594E1C14-C1D4-4207-91A1-28892CE6D821
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84d020edaabf4c618b1fa911a91bc4cc0e8b37e
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481840"
---
# <a name="specifying-compiler-targets"></a>Указание целевых объектов компилятора

Необходимо указать целевой объект шейдера — набор функций шейдера — для компиляции при вызове функции [**D3DCompile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile), [**D3DCompile2**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompile2)или [**D3DCompileFromFile**](/windows/win32/api/d3dcompiler/nf-d3dcompiler-d3dcompilefromfile) . Здесь перечислены целевые объекты для различных профилей, которые поддерживаются функциями **D3DCompile \*** и компилятором HLSL.

-   [Уровни компонентов Direct3D 11,0 и 11,1](#direct3d-110-and-111-feature-levels)
-   [Уровень компонентов Direct3D 10,1](#direct3d-101-feature-level)
-   [Уровень компонентов Direct3D 10,0](#direct3d-100-feature-level)
-   [Уровни компонентов Direct3D 9,1, 9,2 и 9,3](#direct3d-91-92-and-93-feature-levels)
-   [Устаревшая модель шейдера Direct3D 9 3,0](#legacy-direct3d-9-shader-model-30)
-   [Устаревшая модель шейдера Direct3D 9 2,0](#legacy-direct3d-9-shader-model-20)
-   [Устаревшая модель шейдера Direct3D 9 с 1. x](#legacy-direct3d-9-shader-model-1x)
-   [Устаревшие эффекты](#legacy-effects)
-   [Примечания](#notes)
-   [Связанные темы](#related-topics)

## <a name="direct3d-110-and-111-feature-levels"></a>Уровни компонентов Direct3D 11,0 и 11,1

Ниже приведены цели шейдера, поддерживаемые [уровнями компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 11,0 и 11,1.



| целевого объекта   | Описание                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 5 \_ 0 | DirectCompute 5,0 ([COMPUTE Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader))                              |
| DS \_ 5 \_ 0 | [Шейдер доменов](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)             |
| GS \_ 5 \_ 0 | [Шейдер геометрии](/previous-versions//bb205146(v=vs.85)) |
| HS \_ 5 \_ 0 | [Шейдер поверхности](/windows/desktop/direct3d11/direct3d-11-advanced-stages-tessellation)                   |
| PS \_ 5 \_ 0 | [Построитель текстуры](/previous-versions//bb205146(v=vs.85))          |
| VS \_ 5 \_ 0 | [Вершинный построитель текстуры](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-101-feature-level"></a>Уровень компонентов Direct3D 10,1

Ниже приведены целевые шейдеры, поддерживаемые [уровнем компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 10,1.



| целевого объекта   | Описание                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 4 \_ 1 | DirectCompute 4,1 ([COMPUTE Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| GS \_ 4 \_ 1 | [Шейдер геометрии](/previous-versions//bb205146(v=vs.85)) |
| PS \_ 4 \_ 1 | [Построитель текстуры](/previous-versions//bb205146(v=vs.85))          |
| VS \_ 4 \_ 1 | [Вершинный построитель текстуры](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-100-feature-level"></a>Уровень компонентов Direct3D 10,0

Ниже приведены целевые шейдеры, поддерживаемые [уровнем компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 10,0.



| целевого объекта   | Описание                                                                                                              |
|----------|--------------------------------------------------------------------------------------------------------------------------|
| CS \_ 4 \_ 0 | DirectCompute 4,0 ([COMPUTE Shader](/windows/desktop/direct3d11/direct3d-11-advanced-stages-compute-shader)) ¹                             |
| GS \_ 4 \_ 0 | [Шейдер геометрии](/previous-versions//bb205146(v=vs.85)) |
| PS \_ 4 \_ 0 | [Построитель текстуры](/previous-versions//bb205146(v=vs.85))          |
| VS \_ 4 \_ 0 | [Вершинный построитель текстуры](/previous-versions//bb205146(v=vs.85))       |



 

## <a name="direct3d-91-92-and-93-feature-levels"></a>Уровни компонентов Direct3D 9,1, 9,2 и 9,3

Ниже приведены цели шейдера, поддерживаемые [уровнями функций](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) Direct3D 9,1, 9,2 и 9,3.

> [!Note]  
> При использовании \* \_ \_ \_ профилей шейдера с 4 уровнями \_ 9 \_ x HLSL вы неявно используете профили [шейдера 2. x](dx-graphics-hlsl-sm2.md) для поддержки аппаратного обеспечения с поддержкой Direct3D 9. Профили Shader модели 2. x поддерживают более ограниченное поведение управления потоком, чем профили [шейдера 4. x](dx-graphics-hlsl-sm4.md) и более поздних версий.

 




| целевого объекта | Описание | 
|--------|-------------|
| ps_4_0_level_9_1 | [Построитель текстуры](/previous-versions//bb205146(v=vs.85)) для 9,1 и 9,2 (аналогичные ограничения ps_2_0)<ul><li>64 арифметические и 32 текстурных инструкций</li><li>12 временных регистров</li><li>4 уровня зависимых операций чтения</li></ul> | 
| ps_4_0_level_9_3 | <a href="/previous-versions//bb205146(v=vs.85)">Построитель текстуры</a> для 9,3 (аналогичные ограничения ps_2_x ² с дополнительными функциями шейдеров)<ul><li>512 инструкции</li><li>32. временные регистры</li><li>Статическое управление потоком (максимальная глубина 4)</li><li>Динамическое управление потоком (максимальная глубина 24)</li><li>D3DPS20CAPS_ARBITRARYSWIZZLE</li><li>D3DPS20CAPS_GRADIENTINSTRUCTIONS</li><li>D3DPS20CAPS_PREDICATION</li><li>D3DPS20CAPS_NODEPENDENTREADLIMIT</li><li>D3DPS20CAPS_NOTEXINSTRUCTIONLIMIT</li></ul> | 
| vs_4_0_level_9_1 | <a href="/previous-versions//bb205146(v=vs.85)">Шейдер вершин</a> для 9,1 и 9,2 (аналогично VS_2_0)<ul><li>256 инструкции</li><li>12 временных регистров</li><li>Статическое управление потоком (максимальная глубина 1)</li></ul> | 
| vs_4_0_level_9_3 | <a href="/previous-versions//bb205146(v=vs.85)">Шейдер вершин</a> для 9,3 (аналогично vs_2_a ² с дополнительными функциями шейдера и созданием экземпляров)<ul><li>256 инструкции</li><li>32. временные регистры</li><li>Статическое управление потоком (максимальная глубина 4)</li><li>D3DVS20CAPS_PREDICATION</li></ul> | 




 

## <a name="legacy-direct3d-9-shader-model-30"></a>Устаревшая модель шейдера Direct3D 9 3,0

Ниже приведены цели шейдера для устаревшей модели шейдера Direct3D 9 3,0 ³.



| целевого объекта    | Описание                                                                                                                       |
|-----------|-----------------------------------------------------------------------------------------------------------------------------------|
| PS \_ 3 \_ 0  | [Построитель текстуры](/previous-versions//bb205146(v=vs.85)) 3,0               |
| PS \_ 3 \_ SW | [Шейдер пикселей](/previous-versions//bb205146(v=vs.85)) 3,0 (программное обеспечение)    |
| VS \_ 3 \_ 0  | [Шейдер вершин](/previous-versions//bb205146(v=vs.85)) 3,0            |
| VS \_ 3 \_ SW | [Шейдер вершин](/previous-versions//bb205146(v=vs.85)) 3,0 (программное обеспечение) |



 

## <a name="legacy-direct3d-9-shader-model-20"></a>Устаревшая модель шейдера Direct3D 9 2,0

Ниже приведены цели шейдера для устаревшей модели шейдера Direct3D 9 2,0 ³.



| целевого объекта    | Описание                                                                                                                     |
|-----------|---------------------------------------------------------------------------------------------------------------------------------|
| PS \_ 2 \_ 0  | [Построитель текстуры](/previous-versions//bb205146(v=vs.85)) 2,0             |
| PS \_ 2 \_ a  | [Шейдер пикселей](/previous-versions//bb205146(v=vs.85)) 2A              |
| PS \_ 2 \_ b  | [Шейдер пикселей](/previous-versions//bb205146(v=vs.85)) 2b              |
| PS \_ 2 \_ SW | Программное обеспечение [построителя текстуры](/previous-versions//bb205146(v=vs.85)) 2,0    |
| VS \_ 2 \_ 0  | [Шейдер вершин](/previous-versions//bb205146(v=vs.85)) 2,0          |
| VS \_ 2 \_ a  | [Шейдер вершин](/previous-versions//bb205146(v=vs.85)) 2A           |
| VS \_ 2 \_ SW | Программное обеспечение [вершинного шейдера](/previous-versions//bb205146(v=vs.85)) 2,0 |



 

## <a name="legacy-direct3d-9-shader-model-1x"></a>Устаревшая модель шейдера Direct3D 9 с 1. x

Ниже приведены цели шейдера для устаревшей версии Direct3D 9 Shader Model 1. x ⁴.



| целевого объекта   | Описание                                                                                                                                                                       |
|----------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| TX \_ 1 \_ 0 | Профиль шейдера текстуры, который использует устаревшие функции D3DX9 ⁵ [**D3DXCreateTextureShader**](/windows/desktop/direct3d9/d3dxcreatetextureshader) и [**D3DXFillTextureTX**](/windows/desktop/direct3d9/d3dxfilltexturetx) |
| VS \_ 1 \_ 1 | [Шейдер вершин](/previous-versions//bb205146(v=vs.85)) 1,1                                                            |



 

## <a name="legacy-effects"></a>Устаревшие эффекты

Ниже приведены целевые эффекты для устаревших эффектов.



| целевого объекта   | Описание                               |
|----------|-------------------------------------------|
| FX \_ 2 \_ 0 | Эффекты (FX) для Direct3D 9 в D3DX9 ⁵     |
| FX \_ 4 \_ 0 | Эффекты (FX) для Direct3D 10,0 в D3DX10 ⁵ |
| FX \_ 4 \_ 1 | Эффекты (FX) для Direct3D 10,1 в D3DX10 ⁵ |
| FX \_ 5 \_ 0 | Эффекты (FX) для Direct3D 11 ⁵             |



 

## <a name="notes"></a>Примечания

Ниже приведены некоторые замечания, на которые ссылаются предыдущие разделы.

1.  устройства [уровня](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 10,0 и 10,1 могут дополнительно поддерживать DirectCompute. Чтобы проверить поддержку, используйте [**ID3D11Device:: чеккфеатуресуппорт**](/windows/desktop/api/d3d11/nf-d3d11-id3d11device-checkfeaturesupport) с [**\_ \_ \_ \_ \_ параметрами оборудования D3D11 Feature D3D10 X**](/windows/desktop/api/d3d11/ne-d3d11-d3d11_feature).
2.  на [уровне компонентов](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro) 9,3 эффективно требуется оборудование, которое соответствует требованиям для [устаревшей модели шейдера Direct3D 9 (3,0](#legacy-direct3d-9-shader-model-30)), но этот уровень функций не использует \_ \_ целевые объекты VS 3 0 или PS \_ 3 \_ 0.
3.  Используйте только устаревшие модели шейдеров Direct3D 9 с API Direct3D 9. Вместо этого используйте профили 9. x с API Direct3D 10. x и 11. x.
4.  Текущие функции **D3DCompile \*** шейдера HLSL не поддерживают устаревшие шейдеры 1. x пикселей. Последняя версия HLSL для поддержки этих целей была D3DX9а в выпуске DirectX SDK, выпущенной в октябре 2006.
5.  Все версии D3DX и DirectX SDK являются устаревшими. Дополнительные сведения см. [в разделе где находится пакет DirectX SDK?](/windows/desktop/directx-sdk--august-2009-).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Руководство по программированию для HLSL](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 
