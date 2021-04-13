---
description: Нарисуйте массив спрайтов.
ms.assetid: 3fcc7705-0d59-450e-b137-c9cb7ec6b1ea
title: 'ID3DX10Sprite: метод:D Равспритесиммедиате (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesImmediate
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 7fa4012f5f589c7bc0d1f789599da142194f6e08
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104356120"
---
# <a name="id3dx10spritedrawspritesimmediate-method"></a>ID3DX10Sprite: метод:D Равспритесиммедиате

Нарисуйте массив спрайтов. При этом спрайты будут немедленно отправлены на устройство для подготовки к просмотру, что отличается от [**ID3DX10Sprite::D равспритесбуфферед**](id3dx10sprite-drawspritesbuffered.md) , который добавляет массив спрайтов в пакет спрайтов для подготовки к просмотру при вызове [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) . Этот метод рисования наиболее удобен при рисовании большого количества спрайтов, которые уже были отсортированы в ЦП (или не требуют сортировки), например в системе частиц. Этот метод должен вызываться между вызовами [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) и [**ID3DX10Sprite:: end**](id3dx10sprite-end.md).

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DrawSpritesImmediate(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites,
  [in] UINT          cbSprite,
  [in] UINT          flags
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*пспритес* \[ окне\]
</dt> <dd>

Тип: **[ **D3DX10 \_ спрайт**](d3dx10-sprite.md)\***

Массив спрайтов для рисования. См. [**D3DX10 \_ Sprite**](d3dx10-sprite.md).

</dd> <dt>

*кспритес* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число спрайтов в Пспритес.

</dd> <dt>

*кбсприте* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Размер структуры спрайта, передаваемых в Пспритес. Передача 0 эквивалентна передаче в sizeof (D3DX10 \_ Sprite).

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Зарезервировано.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
