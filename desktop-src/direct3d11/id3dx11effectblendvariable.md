---
title: Интерфейс ID3DX11EffectBlendVariable (D3dx11effect. h)
description: Интерфейс Blend-Variable получает доступ к состоянию смешения.
ms.assetid: 8a6e6e7e-2f1e-4e16-8d28-ffc7f3f018d6
keywords:
- Интерфейс ID3DX11EffectBlendVariable Direct3D 11
- Интерфейс ID3DX11EffectBlendVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectBlendVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 57a0a8a3ec0c2a3d92dfc9579fff8b3769dcfc5d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104000521"
---
# <a name="id3dx11effectblendvariable-interface"></a>Интерфейс ID3DX11EffectBlendVariable

Интерфейс Blend-Variable получает доступ к состоянию смешения.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11EffectBlendVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectBlendVariable** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectBlendVariable** содержит следующие методы.



| Метод                                                                    | Описание                                          |
|:--------------------------------------------------------------------------|:-----------------------------------------------------|
| [**жетбаккингсторе**](id3dx11effectblendvariable-getbackingstore.md)     | Получает указатель на переменную состояния Blend.<br/>  |
| [**жетблендстате**](id3dx11effectblendvariable-getblendstate.md)         | Получает указатель на интерфейс состояния смешения.<br/> |
| [**сетблендстате**](id3dx11effectblendvariable-setblendstate.md)         | Задает состояние смешения для действия.<br/>             |
| [**ундосетблендстате**](id3dx11effectblendvariable-undosetblendstate.md) | Восстанавливает ранее установленное состояние Blend.<br/>     |



 

## <a name="remarks"></a>Примечания

Интерфейс [**ID3DX11EffectVariable**](id3dx11effectvariable.md) создается при считывании воздействия в память.

Переменные эффектов сохраняются в памяти в резервном хранилище; При применении метода значения в резервном хранилище копируются на устройство. Для возврата состояния можно использовать любой из этих методов.

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

 

 





