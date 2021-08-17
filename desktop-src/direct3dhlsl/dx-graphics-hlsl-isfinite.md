---
title: ограничение (Корекрт \_ Math. h)
description: Определяет, является ли указанное значение с плавающей точкой конечным.
ms.assetid: 8be10499-2d06-4520-9697-dab2f461bd0d
keywords:
- HLSL
topic_type:
- apiref
api_name:
- isfinite
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bdf2370baacc9089e54c0f5ee58b7601cb54662e70a5a20352fba7f74fa04667
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118792116"
---
# <a name="isfinite"></a>isFinite

Определяет, является ли указанное значение с плавающей точкой конечным.



| *RET* -ограничение (*x*) |
|---------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] указанном значении.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение, равное тому же размеру, что и входные данные, со значением **true** , если параметр *x* является конечным; в противном случае — **false**.

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер     |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|----------|
| *x*   | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | any      |
| *обратно* | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**bool**](/windows/desktop/WinProg/windows-data-types)                         | в качестве входных данных |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается           |
|------------------------------------------------------------------------------------|---------------------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | Да                 |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Да ( \_ только VS 1 1 \_ ) |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Корекрт \_ Math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

