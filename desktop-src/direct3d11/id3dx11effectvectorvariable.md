---
title: Интерфейс ID3DX11EffectVectorVariable (D3dx11effect. h)
description: Интерфейс векторной переменной обращается к вектору из четырех компонентов.
ms.assetid: 191d373b-0562-4d7b-ac3f-cd24abf259bc
keywords:
- Интерфейс ID3DX11EffectVectorVariable Direct3D 11
- Интерфейс ID3DX11EffectVectorVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectVectorVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9343659ac249153805e3dfc4c97595957dfbe52bf7be5c498d81f357c66db8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119851544"
---
# <a name="id3dx11effectvectorvariable-interface"></a>Интерфейс ID3DX11EffectVectorVariable

Интерфейс векторной переменной обращается к вектору из четырех компонентов.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11EffectVectorVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectVectorVariable** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectVectorVariable** содержит следующие методы.



| Метод                                                                         | Описание                                                                         |
|:-------------------------------------------------------------------------------|:------------------------------------------------------------------------------------|
| [**жетбулвектор**](id3dx11effectvectorvariable-getboolvector.md)             | Получение вектора из четырех компонентов, содержащего логические данные.<br/>                  |
| [**жетбулвектораррай**](id3dx11effectvectorvariable-getboolvectorarray.md)   | Получение массива векторов из четырех компонентов, содержащих логические данные.<br/>        |
| [**жетфлоатвектор**](id3dx11effectvectorvariable-getfloatvector.md)           | Получение вектора из четырех компонентов, содержащего данные с плавающей запятой.<br/>           |
| [**жетфлоатвектораррай**](id3dx11effectvectorvariable-getfloatvectorarray.md) | Получите массив векторов из четырех компонентов, содержащих данные с плавающей запятой.<br/> |
| [**жетинтвектор**](id3dx11effectvectorvariable-getintvector.md)               | Получение вектора из четырех компонентов, содержащего целочисленные данные.<br/>                  |
| [**жетинтвектораррай**](id3dx11effectvectorvariable-getintvectorarray.md)     | Получение массива векторов из четырех компонентов, содержащих целочисленные данные.<br/>        |
| [**сетбулвектор**](id3dx11effectvectorvariable-setboolvector.md)             | Установите вектор с четырьмя компонентами, содержащий логические данные.<br/>                  |
| [**сетбулвектораррай**](id3dx11effectvectorvariable-setboolvectorarray.md)   | Установите массив векторов из четырех компонентов, содержащих логические данные.<br/>        |
| [**сетфлоатвектор**](id3dx11effectvectorvariable-setfloatvector.md)           | Установите вектор с четырьмя компонентами, содержащий данные с плавающей запятой.<br/>           |
| [**сетфлоатвектораррай**](id3dx11effectvectorvariable-setfloatvectorarray.md) | Установите массив векторов из четырех компонентов, содержащих данные с плавающей запятой.<br/> |
| [**сетинтвектор**](id3dx11effectvectorvariable-setintvector.md)               | Установите вектор с четырьмя компонентами, который содержит целочисленные данные.<br/>                  |
| [**сетинтвектораррай**](id3dx11effectvectorvariable-setintvectorarray.md)     | Установите массив векторов из четырех компонентов, содержащих целочисленные данные.<br/>        |



 

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

 

 





