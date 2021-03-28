---
title: tex2Dlod
description: Пример двухмерной текстуры с помощью MIP-карты. Лод mipmap указан в т.в.
ms.assetid: 689eff39-f6ac-4c25-8b92-ca68707ae8ad
keywords:
- tex2Dlod HLSL
topic_type:
- apiref
api_name:
- tex2Dlod
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f63a922fe86dc10d984369a1a872f84089b4db34
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/20/2020
ms.locfileid: "104983984"
---
# <a name="tex2dlod"></a>tex2Dlod

Пример двухмерной текстуры с помощью MIP-карты. Лод mipmap указан в т.в.



| RET tex2Dlod (s, t) |
|--------------------|



 

## <a name="parameters"></a>Параметры



| Элемент                                                   | Описание                               |
|--------------------------------------------------------|-------------------------------------------|
| <span id="s"></span><span id="S"></span>*#d0*<br/> | \[в \] состоянии выборки.<br/>      |
| <span id="t"></span><span id="T"></span>*t*<br/> | \[в \] координатах текстуры.<br/> |



 

## <a name="return-value"></a>Возвращаемое значение

Значение данных текстуры.

## <a name="type-description"></a>Описание типа



| Имя | В/Из | [**Тип шаблона**](dx-graphics-hlsl-intrinsic-functions.md)                       | [**Тип компонента**](dx-graphics-hlsl-intrinsic-functions.md) | Размер |
|------|--------|-------------------------------------------------------------------------------------|----------------------------------------------------------------|------|
| s    | in     | [**объектами**](dx-graphics-hlsl-intrinsic-functions.md) | [sampler2D](dx-graphics-hlsl-sampler.md)                      | 1    |
| t    | in     | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |
| обратно  | out    | [**уязвимо**](dx-graphics-hlsl-intrinsic-functions.md) | [**float**](/windows/desktop/WinProg/windows-data-types)                        | 4    |



 

## <a name="minimum-shader-model"></a>Минимальная модель шейдера

Эта функция поддерживается в следующих моделях шейдеров.



| Модель шейдера                                                                       | Поддерживается |
|------------------------------------------------------------------------------------|-----------|
| [Модель шейдера 3 (DirectX HLSL)](dx-graphics-hlsl-sm3.md) и более высокие модели шейдеров | да       |
| [Модель шейдера 2 (DirectX HLSL)](dx-graphics-hlsl-sm2.md)                          | Нет        |
| [Модель шейдера 1 (DirectX HLSL)](dx-graphics-hlsl-sm1.md)                          | Нет        |



 

## <a name="remarks"></a>Примечания

Начиная с Direct3D 10 можно использовать новый синтаксис HLSL для доступа к текстурам и другим ресурсам. Можно заменить встроенные функции поиска текстур, такие как **tex2Dlod**, более объектно-ориентированным стилем. В этом объектно-ориентированном стиле текстуры отделены от образцов и имеют методы для загрузки и выборки.

Для примера двухмерной текстуры вместо использования **tex2Dlod** , как в следующем коде:


```
sampler S;
...
color = tex2Dlod(S, Location);
```



Используйте метод [Самплелевел](dx-graphics-hlsl-to-samplelevel.md) [**объекта текстуры**](dx-graphics-hlsl-to-type.md) , как в следующем коде:


```
Texture2D MyTexture;
SamplerState MySampler;
...
color = MyTexture.SampleLevel(MySampler, Location, LOD);
```



Чтобы использовать функции поиска текстур в встроенном стиле, такие как **tex2Dlod**, с [моделью шейдер 4](dx-graphics-hlsl-sm4.md) и выше, используйте [**D3DCOMPILE \_ включить \_ обратную \_ Совместимость**](d3dcompile-constants.md) для компиляции. Однако если вы хотите выбрать модель шейдера 4 и более поздних версий (даже [ \* \_ 4 \_ 0 \_ уровня \_ 9 \_ \* ](/windows/desktop/direct3d11/overviews-direct3d-11-devices-downlevel-intro)) с новым объектно-ориентированным кодом стиля, переходите к более новой HLSL синтаксису.

## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**Встроенные функции (DirectX HLSL)**](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

