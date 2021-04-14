---
title: определяющих
description: Возвращает определитель заданной квадратной матрицы с плавающей запятой.
ms.assetid: 9062b6f1-8518-4ee4-8d57-5aa9e2176d05
keywords:
- определителная HLSL
topic_type:
- apiref
api_name:
- determinant
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: eb010a0c0d0868afcb3dff488daf7926ec6c5e03
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984017"
---
# <a name="determinant"></a>определяющих

Возвращает определитель заданной квадратной матрицы с плавающей запятой.



| определитель " *RET* " (*m*) |
|------------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="m"></span><span id="M"></span>*Пн*<br/> | \[в \] указанном значении.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Скалярное значение с плавающей запятой, представляющее определитель параметра *m* .

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                                     |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------------------|
| *m*   | [**таблицу**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | Any (число строк = количество столбцов) |
| *обратно* | [**скаляр**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1                                        |



 

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

 

