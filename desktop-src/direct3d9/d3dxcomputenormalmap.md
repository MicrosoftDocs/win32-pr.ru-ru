---
description: Преобразует карту высоты в обычную карту. Компоненты (x, y, z) каждой нормальной версии сопоставляются с каналами (r, g, b) выходной текстуры.
ms.assetid: ed9053c0-b1df-4f74-bdee-627c0f60d942
title: Функция D3DXComputeNormalMap (D3dx9tex. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXComputeNormalMap
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6e22418f5a023dbe70fee8ea0fba8a449abbcc8d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713881"
---
# <a name="d3dxcomputenormalmap-function"></a>Функция D3DXComputeNormalMap

Преобразует карту высоты в обычную карту. Компоненты (x, y, z) каждой нормальной версии сопоставляются с каналами (r, g, b) выходной текстуры.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXComputeNormalMap(
  _Out_       LPDIRECT3DTEXTURE9 pTexture,
  _In_        LPDIRECT3DTEXTURE9 pSrcTexture,
  _In_  const PALETTEENTRY       *pSrcPalette,
  _In_        DWORD              Flags,
  _In_        DWORD              Channel,
  _In_        FLOAT              Amplitude
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*птекстуре* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий текстуру назначения.

</dd> <dt>

*псрктекстуре* \[ окне\]
</dt> <dd>

Тип: **[ **LPDIRECT3DTEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9)**

Указатель на интерфейс [**IDirect3DTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dtexture9) , представляющий текстуру исходной карты с высотой.

</dd> <dt>

*псркпалетте* \[ окне\]
</dt> <dd>

Тип: **const [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) \***

Указатель на тип [**палеттинтри**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) , который содержит исходную палитру 256 цветов или **значение NULL**.

</dd> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Один или несколько флагов [ \_ нормалмап D3DX](d3dx-normalmap.md) , управляющих созданием обычных карт.

</dd> <dt>

*Канал* \[ связи окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Один [флаг \_ канала D3DX](d3dx-channel.md) , указывающий источник сведений о высоте.

</dd> <dt>

*Амплитуда* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Коэффициент величины постоянного значения, увеличивающий (или уменьшающий) значения в нормальном сопоставлении. Более высокие значения обычно делают выпуклости более видимыми, а более низкие значения обычно делают невидимыми более выпуклости.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение D3D \_ ОК. Если функция завершается ошибкой, возвращаемое значение может иметь следующее значение: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Этот метод рассчитывает нормальную работу, используя Центральное различие с размером ядра 3X3. В качестве центрального знаменателя разницы используется 2,0. Каналы RGB в назначении содержат смещенные компоненты (x, y, z) нормали.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|---------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9tex. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>  |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции текстуры в D3DX 9](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> </dl>

 

 
