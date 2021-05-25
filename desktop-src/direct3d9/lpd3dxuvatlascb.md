---
description: Функция обратного вызова для Уватлас.
ms.assetid: a605ae27-10c9-49b4-98fe-8c788c2c0752
title: LPD3DXUVATLASCB
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe073b5e6a798ccb74421d42502b089d59be11f
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/24/2021
ms.locfileid: "110342799"
---
# <a name="lpd3dxuvatlascb"></a>LPD3DXUVATLASCB

Функция обратного вызова для Уватлас.

## <a name="syntax"></a>Синтаксис


```
typedef HRESULT (*LPD3DXUVATLASCB ( 
    FLOAT fPercentDone,
    LPVOID lpUserContext
);
```



## <a name="parameters"></a>Параметры

\[out \] фперцентдоне — число с плавающей запятой от 0 до 1,0, представляющее процент выполненных вычислений (от 0 до 100 процентов).

\[в \] лпусерконтекст — указатель на определяемое пользователем значение, которое передается функции обратного вызова; обычно используется приложением для передачи указателя на структуру данных, которая предоставляет сведения о контексте для функции обратного вызова.

## <a name="return-value"></a>Возвращаемое значение

Эта функция должна быть реализована, чтобы вернуть значение \_ ОК для сохранения запуска симулятора. Любое другое значение остановит симулятор.

## <a name="remarks"></a>Remarks

Не забудьте указать соглашение о вызовах [**типов данных Windows**](../winprog/windows-data-types.md) при объявлении функции обратного вызова. В противном случае могут возникать переполняется стек.



| Требование                         | Значение            |
|--------------------------|-------------|
| Заголовок                   | d3dx9mesh. h |
| Библиотека импорта           | d3dx9. lib   |
| Минимальная операционная система | Windows 98  |



 

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Функции обратного вызова](dx9-graphics-reference-d3dx-callback-functions.md)
</dt> </dl>

 

 
