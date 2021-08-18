---
title: Интерфейс ID3DX11EffectDepthStencilVariable (D3dx11effect. h)
description: Интерфейс переменной с глубиной и набором элементов имеет доступ к состоянию шаблона глубины.
ms.assetid: 8fb1be19-eed4-4d69-bbbe-94484531eba2
keywords:
- Интерфейс ID3DX11EffectDepthStencilVariable Direct3D 11
- Интерфейс ID3DX11EffectDepthStencilVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectDepthStencilVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9d743bfebfa9722261d220800a633bdc8b268a520b883c9fea11f9f7948f7bca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118989774"
---
# <a name="id3dx11effectdepthstencilvariable-interface"></a>Интерфейс ID3DX11EffectDepthStencilVariable

Интерфейс переменной с глубиной и набором элементов имеет доступ к состоянию шаблона глубины.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11EffectDepthStencilVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectDepthStencilVariable** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectDepthStencilVariable** содержит следующие методы.



| Метод                                                                                         | Описание                                                               |
|:-----------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [**жетбаккингсторе**](id3dx11effectdepthstencilvariable-getbackingstore.md)                   | Получает указатель на переменную, которая содержит состояние шаблона глубины.<br/> |
| [**жетдепсстенЦилстате**](id3dx11effectdepthstencilvariable-getdepthstencilstate.md)         | Получение указателя на интерфейс трафарета глубины.<br/>                    |
| [**сетдепсстенЦилстате**](id3dx11effectdepthstencilvariable-setdepthstencilstate.md)         | Задает состояние шаблона глубины.<br/>                                  |
| [**ундосетдепсстенЦилстате**](id3dx11effectdepthstencilvariable-undosetdepthstencilstate.md) | Восстанавливает ранее заданное состояние трафарета глубины.<br/>                  |



 

## <a name="remarks"></a>Remarks

Интерфейс [**ID3DX11EffectVariable**](id3dx11effectvariable.md) создается при считывании воздействия в память.

Переменные эффектов сохраняются в памяти в резервном хранилище; При применении метода значения в резервном хранилище копируются на устройство. Для возврата состояния можно использовать любой из этих методов.

> [!Note]  
> Пакет SDK для DirectX не предоставляет никаких скомпилированных двоичных файлов для эффектов. Для создания приложения типа Effects необходимо использовать исходный текст Effects 11. Дополнительные сведения об использовании источника Effects 11 см. в разделе [различия между эффектами 10 и эффекты 11](d3d11-graphics-programming-guide-effects-differences.md).

 

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx11effect. h</dt> </dl>                                                    |
| Библиотека<br/> | <dl> <dt>Н/д (библиотека Effects 11 доступна в сети в качестве общего источника.)</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID3DX11EffectVariable**](id3dx11effectvariable.md)
</dt> <dt>

[Effects 11, интерфейсы](d3d11-graphics-reference-effects11-interfaces.md)
</dt> <dt>

[Интерфейсы D3DX](d3d11-graphics-reference-d3dx11-interfaces.md)
</dt> </dl>

 

 





