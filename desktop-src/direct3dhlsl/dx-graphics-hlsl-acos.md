---
title: acos
description: Возвращает арккосинус указанного значения.
ms.assetid: c9bc33b8-d586-4c64-9453-5ab97396f2cf
keywords:
- ACOS HLSL
topic_type:
- apiref
api_name:
- acos
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 155915f1a9163b8569b9c92a396161659df2addfc7e27f2acde8f05bf49808d1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119673615"
---
# <a name="acos"></a>acos

Возвращает арккосинус указанного значения.



| *RET* ACOS (*x*) |
|-----------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                                                                                                         |
|--------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] указанном значении. Каждый компонент должен быть значением с плавающей запятой в диапазоне от-1 до 1.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Арккосинус параметра *x* .

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                           |
|-------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|--------------------------------|
| *x*   | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | any                            |
| *обратно* | то же, что входные данные *x*                                                                                              | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | те же измерения, что и входные *x* |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается     |
|------------------------------------------------------------------------------------|---------------|
| [Модели шейдеров 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md) и более поздние модели шейдеров | Да           |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | \_только VS 1 1 \_ |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

