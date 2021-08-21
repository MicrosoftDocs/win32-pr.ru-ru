---
title: Интерфейс ID3DX11EffectShaderResourceVariable (D3dx11effect. h)
description: Интерфейс шейдера-ресурса получает доступ к ресурсу шейдера.
ms.assetid: 936a3439-1f7d-4fea-b124-1d6ead528250
keywords:
- Интерфейс ID3DX11EffectShaderResourceVariable Direct3D 11
- Интерфейс ID3DX11EffectShaderResourceVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderResourceVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1cdfce3ce5fe907de5b0149f2280d8b1e34a8761c56cf9e83e316ea253d7366
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118533290"
---
# <a name="id3dx11effectshaderresourcevariable-interface"></a>Интерфейс ID3DX11EffectShaderResourceVariable

Интерфейс шейдера-ресурса получает доступ к ресурсу шейдера.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11EffectShaderResourceVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectShaderResourceVariable** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectShaderResourceVariable** содержит следующие методы.



| Метод                                                                           | Описание                                  |
|:---------------------------------------------------------------------------------|:---------------------------------------------|
| [**Ресурс**](id3dx11effectshaderresourcevariable-getresource.md)           | Получение ресурса шейдера.<br/>            |
| [**жетресаурцеаррай**](id3dx11effectshaderresourcevariable-getresourcearray.md) | Получение массива ресурсов шейдера.<br/> |
| [**сетресаурце**](id3dx11effectshaderresourcevariable-setresource.md)           | Задайте ресурс шейдера.<br/>            |
| [**сетресаурцеаррай**](id3dx11effectshaderresourcevariable-setresourcearray.md) | Задайте массив ресурсов шейдера.<br/> |



 

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

 

 





