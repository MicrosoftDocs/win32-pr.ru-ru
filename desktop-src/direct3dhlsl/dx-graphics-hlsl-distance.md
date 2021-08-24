---
title: distance
description: Возвращает скалярное расстояние между двумя векторами.
ms.assetid: dda8dc39-fd72-4e92-bf9d-e700db0ede9e
keywords:
- Расстояние HLSL
topic_type:
- apiref
api_name:
- distance
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f51c5e9865b9dfc1c5a941beb43010dc8fad64e2d8ac8763998c22cb3e0dfbd5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726544"
---
# <a name="distance"></a>distance

Возвращает скалярное расстояние между двумя векторами.



| Расстояние *RET* (*x*, *y*) |
|--------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                                                    |
|--------------------------------------------------------|----------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] первом сравниваемом векторе с плавающей точкой.<br/>  |
| <span id="y"></span><span id="Y"></span>*&*<br/> | \[во \] втором сравниваемом векторе с плавающей точкой.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Скалярное значение с плавающей запятой, представляющее расстояние между параметром *x* и параметром *y* .

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                           |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *y*   | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |
| *обратно* | [**функцией**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1                              |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается |
|------------------------------------------------------------------------------------|-----------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | Да       |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | VS \_ 1 \_ 1  |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

