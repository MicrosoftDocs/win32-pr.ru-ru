---
title: Метод ID3DX11EffectVariable Асматрикс (D3dx11effect. h)
description: Возвращает переменную матрицы.
ms.assetid: 5d2baf65-ab0d-44df-bc6f-6ffae16cbb01
keywords:
- Метод Асматрикс Direct3D 11
- Метод Асматрикс Direct3D 11, интерфейс ID3DX11EffectVariable
- Интерфейс ID3DX11EffectVariable Direct3D 11, метод Асматрикс
topic_type:
- apiref
api_name:
- ID3DX11EffectVariable.AsMatrix
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 294f3f6a01d88f92f606e5120edbfa8d5086f2e0173375fd78f5525c17c4f1f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118531510"
---
# <a name="id3dx11effectvariableasmatrix-method"></a>Метод ID3DX11EffectVariable:: Асматрикс

Возвращает переменную матрицы.

## <a name="syntax"></a>Синтаксис


```C++
ID3DX11EffectMatrixVariable* AsMatrix();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md)\***

Указатель на переменную матрицы. См. [**ID3DX11EffectMatrixVariable**](id3dx11effectmatrixvariable.md).

## <a name="remarks"></a>Remarks

Асматрикс Возвращает версию переменной Effect, которая была специализированной для переменной матрицы. Как и в приведении, эта специализация возвращает недопустимый объект, если переменная действия не содержит данных матрицы.

Приложения могут проверить возвращаемый объект на допустимость, вызвав [**IsValid**](id3dx11effectvariable-isvalid.md).

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DX11EffectVariable](id3dx11effectvariable.md)
</dt> </dl>

 

 





