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
ms.openlocfilehash: 6dbf6f1e53218355ba1ee9ccf58dac6176007218
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103890664"
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
| *n \_ точек \_ l* | [**скаляр**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *n \_ точек \_ h* | [**скаляр**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *m*         | [**скаляр**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |
| *обратно*       | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается           |
|------------------------------------------------------------------------------------|---------------------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | да                 |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Да ( \_ только VS 1 1 \_ ) |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

