---
title: асфлоат
description: Интерпретирует битовый шаблон x в качестве числа с плавающей запятой.
ms.assetid: 48e1e0cb-8578-4e6d-8c46-2b8b201906c1
keywords:
- асфлоат HLSL
topic_type:
- apiref
api_name:
- asfloat
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9a5701d959fb59519318dd7f2e91b6790f4c0b6e
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104997134"
---
# <a name="asfloat"></a>асфлоат

Интерпретирует битовый шаблон *x* в качестве числа с плавающей запятой.



| RET асфлоат (*x*) |
|------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                        |
|--------------------------------------------------------|------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[во \] входном значении.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Входное значение интерпретируется как число с плавающей запятой.

## <a name="type-description"></a>Описание типа



| Имя  | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md)                                                         | Размер                           |
|-------|----------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|--------------------------------|
| *x*   | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**float**](/windows/desktop/WinProg/windows-data-types), [**int**](/windows/desktop/WinProg/windows-data-types), [**uint**](/windows/desktop/WinProg/windows-data-types) | any                            |
| *обратно* | то же, что входные данные *x*                                                                                              | [**float**](/windows/desktop/WinProg/windows-data-types)                                                                                | те же измерения, что и входные *x* |



 

## <a name="function-overloads"></a>Перегрузки функций

<dl> ' float <x> асфлоат ( <x> значение float); `  
` float <x> асфлоат ( <x> значение int); `  
` float <x> асфлоат ( <x> значение uint); "
</dl>

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                        | Поддерживается |
|---------------------------------------------------------------------|-----------|
| [Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров | да       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | Нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | Нет        |



 

## <a name="remarks"></a>Примечания

Старые компиляторы неправильно разрешаются `asfloat(bool)` , но обратите внимание, что входные данные типа bool не поддерживаются.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

