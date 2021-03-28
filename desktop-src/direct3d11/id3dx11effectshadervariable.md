---
title: Интерфейс ID3DX11EffectShaderVariable (D3dx11effect. h)
description: Интерфейс переменной шейдера обращается к переменной шейдера.
ms.assetid: e547a5e9-7b60-4a85-806d-272be55d12e7
keywords:
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11
- Интерфейс ID3DX11EffectShaderVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectShaderVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bcbb011591f715b4bac57dfa34f640ea90278f6b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104998438"
---
# <a name="id3dx11effectshadervariable-interface"></a>Интерфейс ID3DX11EffectShaderVariable

Интерфейс переменной шейдера обращается к переменной шейдера.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11EffectShaderVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectShaderVariable** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectShaderVariable** содержит следующие методы.



| Метод                                                                                                           | Описание                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| [**жеткомпутешадер**](id3dx11effectshadervariable-getcomputeshader.md)                                         | Получение шейдера вычислений.<br/>                       |
| [**жетдомаиншадер**](id3dx11effectshadervariable-getdomainshader.md)                                           | Получите шейдер домена.<br/>                        |
| [**жетжеометришадер**](id3dx11effectshadervariable-getgeometryshader.md)                                       | Получение шейдера Geometry.<br/>                      |
| [**жесуллшадер**](id3dx11effectshadervariable-gethullshader.md)                                               | Получите шейдер поверхности.<br/>                          |
| [**жетинпутсигнатурилементдеск**](id3dx11effectshadervariable-getinputsignatureelementdesc.md)                 | Получить описание входной подписи.<br/>         |
| [**жетаутпутсигнатурилементдеск**](id3dx11effectshadervariable-getoutputsignatureelementdesc.md)               | Получение описания выходной подписи.<br/>        |
| [**жетпатчконстантсигнатурилементдеск**](id3dx11effectshadervariable-getpatchconstantsignatureelementdesc.md) | Получить описание подписи константы исправлений.<br/> |
| [**жетпикселшадер**](id3dx11effectshadervariable-getpixelshader.md)                                             | Получение шейдера пикселей.<br/>                         |
| [**жетшадердеск**](id3dx11effectshadervariable-getshaderdesc.md)                                               | Получение описания шейдера.<br/>                   |
| [**жетвертексшадер**](id3dx11effectshadervariable-getvertexshader.md)                                           | Получение шейдера вершин.<br/>                        |



 

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

 

 





