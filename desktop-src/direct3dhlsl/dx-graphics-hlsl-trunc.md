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
ms.openlocfilehash: 34493f60e60bc0dce35f5f9db50360265191c742
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998459"
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

## <a name="remarks"></a>Примечания

Эта функция усекает значение с плавающей запятой до целочисленного компонента. При значении с плавающей запятой, равном 1,6, функция TRUNC возвращает 1,0, где, как функция [**Round (DirectX HLSL)**](dx-graphics-hlsl-round.md) возвращает значение 2,0.

## <a name="type-description"></a>Описание типа



| Имя | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                                                  | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер                         |
|------|----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|------------------------------|
| *x*  | [**Скалярная**](dx-graphics-hlsl-intrinsic-functions.md), **векторная** или **Матрица** | [**float**](/windows/desktop/WinProg/windows-data-types)                        | any                          |
| обратно  | Тот же тип, что и входные данные x                                                                                           | [**float**](/windows/desktop/WinProg/windows-data-types)                        | Те же измерения, что и входные x |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается |
|------------------------------------------------------------------------------------|-----------|
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md) и более высокие модели шейдеров | да       |



 

## <a name="requirements"></a>Требования



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Корекрт \_ Math. h</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

