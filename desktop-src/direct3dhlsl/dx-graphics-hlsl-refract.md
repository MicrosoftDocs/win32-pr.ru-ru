---
title: рефракт
description: Возвращает вектор дробной части с использованием входного луча, нормали области и индекса передробки.
ms.assetid: 9f9467d7-dd9b-472a-bbdc-752394d382c6
keywords:
- рефракт HLSL
topic_type:
- apiref
api_name:
- refract
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9e499d078a020ade1ff9ff2566c3fd15b2a820d2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997151"
---
# <a name="refract"></a>рефракт

Возвращает вектор дробной части с использованием входного луча, нормали области и индекса передробки.



| *RET* рефракт (*i*, *n*,?) |
|----------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                                                  |
|--------------------------------------------------------|--------------------------------------------------------------|
| <span id="i"></span><span id="I"></span>*сохранении*<br/> | \[в \] векторе направления лучей с плавающей точкой.<br/>    |
| <span id="n"></span><span id="N"></span>*\n*<br/> | \[в \] векторе нормали с плавающей запятой.<br/>   |
| *?*<br/>                                         | \[в \] скалярном индексе с плавающей запятой.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Вектор дробной части с плавающей запятой. Если угол между входом в луч i и областью нормали n слишком велик для данного индекса передробки?, то возвращаемое значение равно (0, 0, 0).

## <a name="type-description"></a>Описание типа



| Имя              | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                           |
|-------------------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *i*               | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *n*               | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные данные *i* |
| ?                 | [**скаляр**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |
| передробить вектор | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные данные *i* |



 

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

 

