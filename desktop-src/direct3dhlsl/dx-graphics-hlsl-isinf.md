---
title: исинф (Корекрт \_ Math. h)
description: Определяет, является ли указанное значение бесконечным.
ms.assetid: 2028dc5a-e48b-4081-a0ec-35901113aab6
keywords:
- исинф HLSL
topic_type:
- apiref
api_name:
- isinf
api_location:
- corecrt_math.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30384cb4463f5751394f45bf521529a1afc79d1b9262cf007ceeaa7d790c3f0e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119789654"
---
# <a name="isinf"></a>isinf

Определяет, является ли указанное значение бесконечным.



| *RET* исинф (*x*) |
|------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                            |
|--------------------------------------------------------|----------------------------------------|
| <span id="x"></span><span id="X"></span>*x*<br/> | \[в \] указанном значении.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Возвращает значение, равное тому же размеру, что и входные данные, со значением **true** , если параметр *x* имеет значение + INF или-INF. В противном случае — **значение false**.

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



 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|-------------------|--------------------------------------------------------------------------------------------|
| Заголовок<br/> | <dl> <dt>Корекрт \_ Math. h</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

