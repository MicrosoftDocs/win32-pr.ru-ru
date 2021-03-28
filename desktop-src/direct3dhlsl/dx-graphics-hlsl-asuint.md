---
title: асуинт
description: Интерпретирует битовый шаблон x как целое число без знака.
ms.assetid: 8401001d-f9ee-43da-9756-f311e9f2bb20
keywords:
- асуинт HLSL
topic_type:
- apiref
api_name:
- asuint
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1a2d351eb36c6910790e2dceb94e3a97951ad850
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104984060"
---
# <a name="asuint"></a>асуинт

Интерпретирует битовый шаблон *x* как целое число без знака.



| RET асуинт (*x*) |
|-----------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[во \] входном значении.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Входное значение интерпретируется как целое число без знака.

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md)                 | Размер                           |
|-------|----------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**float**](/windows/desktop/WinProg/windows-data-types), [ **int**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *обратно* | то же, что входные данные *x*                                                                                              | [**uint**](/windows/desktop/WinProg/windows-data-types)                                         | те же измерения, что и входные *x* |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                        | Поддерживается |
|---------------------------------------------------------------------|-----------|
| [Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров | да       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | Нет        |



 

## <a name="see-also"></a>См. также

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

