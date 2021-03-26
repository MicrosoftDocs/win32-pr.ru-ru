---
title: синкос
description: Возвращает синус и косинус x.
ms.assetid: 2ef9e84e-4539-47f5-9966-d8e02ca15d36
keywords:
- синкос HLSL
topic_type:
- apiref
api_name:
- sincos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8391c2fcecc939db1d7044fe56fbd281fe3e79fc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997138"
---
# <a name="sincos"></a>синкос

Возвращает синус и косинус x.



| синкос (*x*, out *s*, out *c*) |
|-------------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                                        |
|--------------------------------------------------------|----------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] заданном значении в радианах.<br/> |
| <span id="s"></span><span id="S"></span>*#d0*<br/> | \[out \] возвращает синус x.<br/>          |
| <span id="c"></span><span id="C"></span>*ц*<br/> | \[out \] возвращает косинус x.<br/>        |



 

## <a name="return-value"></a>Возвращаемое значение

Нет.

## <a name="type-description"></a>Описание типа



| Имя | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                           |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*  | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *s*  | то же, что входные данные *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |
| c    | то же, что входные данные *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |



 

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

 

