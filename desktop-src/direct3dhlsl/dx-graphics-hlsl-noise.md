---
title: шум
description: Создает случайное значение с помощью алгоритма Perl-Noise.
ms.assetid: 0188a7f3-9955-4e1c-9370-ef1d8aff3765
keywords:
- шум HLSL
topic_type:
- apiref
api_name:
- noise
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6a4dc01eaeb8276527d5d78b07a250d2a6fb1ab9
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/04/2020
ms.locfileid: "104414197"
---
# <a name="noise"></a>шум

Создает случайное значение с помощью алгоритма Perl-Noise.




| *RET* шум (*x*) |
|------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                                                                    |
|--------------------------------------------------------|--------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] векторе с плавающей точкой, из которого создается шум Perl.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Значение шума Perl в диапазоне от-1 до 1.

## <a name="remarks"></a>Примечания

Значения шума в Perl плавно меняются от одной точки к другой, создавая естественно выглядящие значения, создаваемые случайным образом. Можно использовать Perl для создания процедурных текстур для таких эффектов, как «формирование состояния» и «пожар».

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер |
|-------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| *x*   | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any  |
| *обратно* | [**скаляр**](dx-graphics-hlsl-intrinsic-functions.md) | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                        | 1    |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается           |
|------------------------------------------------------------------------------------|---------------------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | Нет                  |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Да (только для TX \_ 1 \_ 0) |



 

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

