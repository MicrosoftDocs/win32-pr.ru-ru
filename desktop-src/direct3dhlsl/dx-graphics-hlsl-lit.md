---
title: индикатор
description: Возвращает вектор коэффициента освещения.
ms.assetid: 6ae116df-41b7-42f1-96cb-da480a7c1bab
keywords:
- освещенный HLSL
topic_type:
- apiref
api_name:
- lit
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4d3f941fe3aad52f352f5a36d3642141b31e08ef00c25dd8687c8fc7a8ed2de3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118791630"
---
# <a name="lit"></a>индикатор

Возвращает вектор коэффициента освещения.



| *RET* -горит (*n \_ точек \_ l*, *n \_ точек \_ h*, *m*) |
|------------------------------------------|



 

Эта функция возвращает вектор коэффициента освещения (внешние, диффузные, блики, 1), где:

-   окружение = 1
-   Диффузная = n · l < 0? 0: n · н
-   отражающий = n · l < 0 \| \| n · h < 0? 0: (n · h) ^ m

Где Vector n является нормальным вектором, l — это направление падения, а h — половина вектора.

## <a name="parameters"></a>Параметры



| Элемент                                                                       | Описание                                                                              |
|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span id="n_dot_l"></span><span id="N_DOT_L"></span>*n \_ точек \_ l*<br/> | \[в виде \] скалярного произведения нормализованной поверхности и светлой вектор.<br/> |
| <span id="n_dot_h"></span><span id="N_DOT_H"></span>*n \_ точек \_ h*<br/> | \[в \] скалярном продукте для вектора половины углов и нормали к поверхности.<br/>       |
| <span id="m"></span><span id="M"></span>*Пн*<br/>                     | \[в \] отраженном экспоненте.<br/>                                                   |



 

## <a name="return-value"></a>Возвращаемое значение

Вектор коэффициента освещения.

## <a name="type-description"></a>Описание типа



| Имя        | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер |
|-------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *n \_ точек \_ l* | [**функцией**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *n \_ точек \_ h* | [**функцией**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *m*         | [**функцией**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *обратно*       | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается           |
|------------------------------------------------------------------------------------|---------------------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | Да                 |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Да ( \_ только VS 1 1 \_ ) |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

