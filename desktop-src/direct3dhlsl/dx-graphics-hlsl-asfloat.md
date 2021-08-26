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
ms.openlocfilehash: 901b64099547060305bab6db43cbe75b3fdb8d9c
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/26/2021
ms.locfileid: "122886270"
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
| *обратно* | то же, что входные данные *x*                                                                                              | [**FLOAT**](/windows/desktop/WinProg/windows-data-types)                                                                                | те же измерения, что и входные *x* |



 

## <a name="function-overloads"></a>Перегрузки функций

<dl> `float&lt;x&gt; asfloat(float&lt;x&gt; value);`  
`float&lt;x&gt; asfloat(int&lt;x&gt; value);`  
`float&lt;x&gt; asfloat(uint&lt;x&gt; value);`  
</dl>

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                        | Поддерживается |
|---------------------------------------------------------------------|-----------|
| [Модели шейдеров 4](dx-graphics-hlsl-sm4.md) и более поздних шейдеров | да       |
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md)           | нет        |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)           | нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)           | нет        |



 

## <a name="remarks"></a>Комментарии

Старые компиляторы неправильно разрешаются `asfloat(bool)` , но обратите внимание, что входные данные типа bool не поддерживаются.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

