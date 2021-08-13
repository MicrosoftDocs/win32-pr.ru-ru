---
description: Добавьте массив спрайтов в пакет спрайтов для подготовки к просмотру.
ms.assetid: e6a9f806-7244-4139-b47e-c46dfab38a31
title: 'ID3DX10Sprite: метод:D Равспритесбуфферед (D3DX10. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.DrawSpritesBuffered
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: bee3fd9344e393d2b5b9ddf6162286507fac918ea15f9abde2abcc2f80a5b65d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118540041"
---
# <a name="id3dx10spritedrawspritesbuffered-method"></a>ID3DX10Sprite: метод:D Равспритесбуфферед

Добавьте массив спрайтов в пакет спрайтов для подготовки к просмотру. Этот метод должен вызываться между вызовами [**ID3DX10Sprite:: Begin**](id3dx10sprite-begin.md) и [**ID3DX10Sprite:: end**](id3dx10sprite-end.md), а [**ID3DX10Sprite:: Flush**](id3dx10sprite-flush.md) должен вызываться перед окончанием передачи всех пакетных спрайтов на устройство для подготовки к просмотру. Этот метод рисования наиболее удобен при рисовании небольшого числа спрайтов, которые нужно поместить в буфер крупного пакета, например шрифтов.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT DrawSpritesBuffered(
  [in] D3DX10_SPRITE *pSprites,
  [in] UINT          cSprites
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

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . В случае сбоя метода возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DXERR \_ INVALIDDATA.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3DX10. h</dt> </dl>   |
| Библиотека<br/> | <dl> <dt>D3DX10. lib</dt> </dl> |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DX10Sprite](id3dx10sprite.md)
</dt> <dt>

[Интерфейсы D3DX](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
