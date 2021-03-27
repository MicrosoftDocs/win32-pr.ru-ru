---
title: Интерфейс ID3DX11EffectRenderTargetViewVariable (D3dx11effect. h)
description: Интерфейс представления визуализации-целевого объекта обращается к целевому объекту прорисовки.
ms.assetid: 35c4e1da-05a8-4f1c-8730-58e3c90ad213
keywords:
- Интерфейс ID3DX11EffectRenderTargetViewVariable Direct3D 11
- Интерфейс ID3DX11EffectRenderTargetViewVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectRenderTargetViewVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5c5b20f83639fd973016bbe263d9d21dae7b295c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104986876"
---
# <a name="id3dx11effectrendertargetviewvariable-interface"></a>Интерфейс ID3DX11EffectRenderTargetViewVariable

Интерфейс представления визуализации-целевого объекта обращается к целевому объекту прорисовки.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11EffectRenderTargetViewVariable** наследует от [**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md). **ID3DX11EffectRenderTargetViewVariable** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectRenderTargetViewVariable** содержит следующие методы.



| Метод                                                                                     | Описание                                |
|:-------------------------------------------------------------------------------------------|:-------------------------------------------|
| [**жетрендертаржет**](id3dx11effectrendertargetviewvariable-getrendertarget.md)           | Получение целевого объекта рендеринга.<br/>            |
| [**жетрендертаржетаррай**](id3dx11effectrendertargetviewvariable-getrendertargetarray.md) | Получение массива целевых объектов рендеринга.<br/> |
| [**сетрендертаржет**](id3dx11effectrendertargetviewvariable-setrendertarget.md)           | Задайте целевой объект рендеринга.<br/>            |
| [**сетрендертаржетаррай**](id3dx11effectrendertargetviewvariable-setrendertargetarray.md) | Задайте массив целевых объектов рендеринга.<br/> |



 

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

[**ID3DX11EffectRasterizerVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effects 11, интерфейсы](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





