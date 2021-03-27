---
title: фацефорвард
description: Зеркально отражает нормальную поверхность (при необходимости) на противоположную сторону. Возвращает результат в виде n.
ms.assetid: 6530a928-d221-49e4-ab68-6285c3db370f
keywords:
- фацефорвард HLSL
topic_type:
- apiref
api_name:
- faceforward
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c6a3f035ed4f0d16b500864f941bc4fe5413ff54
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104134058"
---
# <a name="faceforward"></a>фацефорвард

Зеркально отражает нормальную поверхность (при необходимости) на противоположную сторону. Возвращает результат в виде n.



| *RET* фацефорвард (*n*, *i*, *NG*) |
|-----------------------------------|



 

Эта функция использует следующую формулу:-*n*  знак (точка (*i*, *NG*)).

## <a name="parameters"></a>Параметры



| Элемент                                                      | Описание                                                                                                     |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span id="n"></span><span id="N"></span>*\n*<br/>    | \[в \] полученном векторе обычной поверхности с плавающей запятой.<br/>                                           |
| <span id="i"></span><span id="I"></span>*сохранении*<br/>    | \[в \] векторе инцидента с плавающей запятой, который указывает позицию представления на позицию заливки.<br/> |
| <span id="ng"></span><span id="NG"></span>*NG*<br/> | \[в \] векторной плоскости с плавающей запятой.<br/>                                                       |



 

## <a name="return-value"></a>Возвращаемое значение

Вектор нормали с плавающей запятой, который является направленным направлением представления.

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *n*   | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *i*   | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные данные *n* |
| *NG*  | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и у входных данных *n*   |
| *обратно* | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и у входных данных *n*   |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается             |
|------------------------------------------------------------------------------------|-----------------------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | да                   |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | VS \_ 1 \_ 1 и PS \_ 1 \_ 4 |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

