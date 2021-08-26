---
title: TRUNC (Корекрт \_ Math. h)
description: Усекает значение с плавающей запятой до целочисленного компонента.
ms.assetid: a0978fa2-71f8-4257-8c90-96224c2ec953
keywords:
- TRUNC HLSL
topic_type:
- apiref
api_name:
- trunc
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0845e619e8674d729735da1b639802df256d9c210615d71578a4e1effd777e39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119845774"
---
# <a name="trunc"></a>trunc

Усекает значение с плавающей запятой до целочисленного компонента.



| RET TRUNC (*x*) |
|----------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] указанных входных данных.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Входное значение, усеченное до целочисленного компонента.

## <a name="remarks"></a>Remarks

Эта функция усекает значение с плавающей запятой до целочисленного компонента. При значении с плавающей запятой, равном 1,6, функция TRUNC возвращает 1,0, где, как функция [**Round (DirectX HLSL)**](dx-graphics-hlsl-round.md) возвращает значение 2,0.

## <a name="type-description"></a>Описание типа



| Имя | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *x*  | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | any                          |
| обратно  | Тот же тип, что и входные данные x                                                                                           | [**сделать**](/windows/desktop/WinProg/windows-data-types)                        | Те же измерения, что и входные x |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается |
|------------------------------------------------------------------------------------|-----------|
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) и более высокие модели шейдеров | Да       |



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Корекрт \_ Math. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

