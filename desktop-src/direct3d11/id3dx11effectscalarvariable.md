---
title: Интерфейс ID3DX11EffectScalarVariable (D3dx11effect. h)
description: Интерфейс с скалярными переменными получает доступ к скалярным значениям.
ms.assetid: 52e3b856-aa1b-4ed2-b140-7ae96ec1c94b
keywords:
- Интерфейс ID3DX11EffectScalarVariable Direct3D 11
- Интерфейс ID3DX11EffectScalarVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectScalarVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3d07f0d14ce37f9c84c20564189e1b8475e69887
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273710"
---
# <a name="id3dx11effectscalarvariable-interface"></a>Интерфейс ID3DX11EffectScalarVariable

Интерфейс с скалярными переменными получает доступ к скалярным значениям.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11EffectScalarVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectScalarVariable** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectScalarVariable** содержит следующие методы.



| Метод                                                             | Описание                                          |
|:-------------------------------------------------------------------|:-----------------------------------------------------|
| [**Bool**](id3dx11effectscalarvariable-getbool.md)             | Получить логическую переменную.<br/>                   |
| [**жетбуларрай**](id3dx11effectscalarvariable-getboolarray.md)   | Получение массива логических переменных.<br/>        |
| [**GetFloat**](id3dx11effectscalarvariable-getfloat.md)           | Получение переменной с плавающей запятой.<br/>            |
| [**жетфлоатаррай**](id3dx11effectscalarvariable-getfloatarray.md) | Получение массива переменных с плавающей запятой.<br/> |
| [**GetInt**](id3dx11effectscalarvariable-getint.md)               | Получение целочисленной переменной.<br/>                  |
| [**жетинтаррай**](id3dx11effectscalarvariable-getintarray.md)     | Получение массива целочисленных переменных.<br/>        |
| [**сетбул**](id3dx11effectscalarvariable-setbool.md)             | Задайте логическую переменную.<br/>                   |
| [**сетбуларрай**](id3dx11effectscalarvariable-setboolarray.md)   | Задайте массив логических переменных.<br/>        |
| [**SetFloat**](id3dx11effectscalarvariable-setfloat.md)           | Задайте переменную с плавающей запятой.<br/>            |
| [**сетфлоатаррай**](id3dx11effectscalarvariable-setfloatarray.md) | Задайте массив переменных с плавающей запятой.<br/> |
| [**SetInt**](id3dx11effectscalarvariable-setint.md)               | Задайте целочисленную переменную.<br/>                  |
| [**сетинтаррай**](id3dx11effectscalarvariable-setintarray.md)     | Задайте массив целочисленных переменных.<br/>        |



 

## <a name="remarks"></a>Примечания

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effects 11, интерфейсы](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





