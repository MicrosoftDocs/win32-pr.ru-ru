---
title: Интерфейс ID3DX11EffectSamplerVariable (D3dx11effect. h)
description: Интерфейс образца имеет доступ к состоянию выборки.
ms.assetid: 8d21f829-2145-45f2-a9b4-2fdc06e0a879
keywords:
- Интерфейс ID3DX11EffectSamplerVariable Direct3D 11
- Интерфейс ID3DX11EffectSamplerVariable Direct3D 11, описание
topic_type:
- apiref
api_name:
- ID3DX11EffectSamplerVariable
api_location:
- N/A
- N/A.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7b5019022cea823566611410cd6e8fd5013380b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157255"
---
# <a name="id3dx11effectsamplervariable-interface"></a>Интерфейс ID3DX11EffectSamplerVariable

Интерфейс образца имеет доступ к состоянию выборки.

## <a name="members"></a>Элементы

Интерфейс **ID3DX11EffectSamplerVariable** наследует от [**ID3DX11EffectVariable**](id3dx11effectvariable.md). **ID3DX11EffectSamplerVariable** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DX11EffectSamplerVariable** содержит следующие методы.



| Метод                                                                  | Описание                                                         |
|:------------------------------------------------------------------------|:--------------------------------------------------------------------|
| [**жетбаккингсторе**](id3dx11effectsamplervariable-getbackingstore.md) | Возвращает указатель на переменную, содержащую состояние выборки.<br/> |
| [**Выборка**](id3dx11effectsamplervariable-getsampler.md)           | Получение указателя на интерфейс образца.<br/>                    |
| [**сетсамплер**](id3dx11effectsamplervariable-setsampler.md)           | Задать состояние образца.<br/>                                       |
| [**ундосетсамплер**](id3dx11effectsamplervariable-undosetsampler.md)   | Отменить ранее установленное состояние образца.<br/>                   |



 

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

 

 





