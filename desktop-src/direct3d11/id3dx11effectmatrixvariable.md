---
title: Интерфейс ID3DX11EffectMatrixVariable (D3dx11effect. h)
description: Интерфейс переменной матрицы обращается к матрице.
ms.assetid: 44f30d1a-3ec1-49d7-92c0-475cf2fa4d2a
keywords:
- Интерфейс ID3DX11EffectMatrixVariable Direct3D 11
- Интерфейс ID3DX11EffectMatrixVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectMatrixVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9daff97a1980c7f1e5647c0e436d5e774a7a7b575b3100f1164af8b97010dea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118535090"
---
# <a name="id3dx11effectmatrixvariable-interface"></a>Интерфейс ID3DX11EffectMatrixVariable

Интерфейс переменной матрицы обращается к матрице.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11EffectMatrixVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectMatrixVariable** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectMatrixVariable** содержит следующие методы.



| Метод                                                                                 | Описание                                                       |
|:---------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| [**Матрица**](id3dx11effectmatrixvariable-getmatrix.md)                             | Получение матрицы.<br/>                                          |
| [**жетматриксаррай**](id3dx11effectmatrixvariable-getmatrixarray.md)                   | Получение массива матриц.<br/>                              |
| [**жетматрикстранспосе**](id3dx11effectmatrixvariable-getmatrixtranspose.md)           | Переставить и получить матрицу с плавающей точкой.<br/>             |
| [**жетматрикстранспосеаррай**](id3dx11effectmatrixvariable-getmatrixtransposearray.md) | Переставить и получить массив матриц с плавающей запятой.<br/> |
| [**сетматрикс**](id3dx11effectmatrixvariable-setmatrix.md)                             | Задайте матрицу с плавающей запятой.<br/>                           |
| [**сетматриксаррай**](id3dx11effectmatrixvariable-setmatrixarray.md)                   | Задайте массив матриц с плавающей запятой.<br/>               |
| [**сетматрикстранспосе**](id3dx11effectmatrixvariable-setmatrixtranspose.md)           | Переставить и установить матрицу с плавающей точкой.<br/>             |
| [**сетматрикстранспосеаррай**](id3dx11effectmatrixvariable-setmatrixtransposearray.md) | Переставить и задайте массив матриц с плавающей запятой.<br/> |



 

## <a name="remarks"></a>Remarks

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effects 11, интерфейсы](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





