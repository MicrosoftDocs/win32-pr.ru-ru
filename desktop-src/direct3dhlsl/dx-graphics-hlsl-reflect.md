---
title: характеризу
description: Возвращает вектор отражения с использованием лучей инцидента и нормали к поверхности.
ms.assetid: e321b399-f382-4585-83a6-a7da1f7b2327
keywords:
- отражение HLSL
topic_type:
- apiref
api_name:
- reflect
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 46c981f636a797ecc4e0dd341ce44ed886c202cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "103793596"
---
# <a name="reflect"></a>характеризу

Возвращает вектор отражения с использованием лучей инцидента и нормали к поверхности.



| отражение *RET* (*i*, *n*) |
|-------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                                          |
|--------------------------------------------------------|------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*сохранении*<br/> | \[в \] векторе инцидента с плавающей точкой.<br/> |
| <span id="n"></span><span id="N"></span>*\n*<br/> | \[в \] векторе с плавающей запятой.<br/>   |



 

## <a name="return-value"></a>Возвращаемое значение

Вектор отражения с плавающей запятой.

## <a name="remarks"></a>Примечания

Эта функция вычисляет Вектор отражения, используя следующую формулу: v = i-2 \* n \* Dot (i n).

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*   | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *n*   | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные данные *i* |
| *обратно* | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные данные *i* |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается |
|------------------------------------------------------------------------------------|-----------|
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) и более высокие модели шейдеров | да       |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

