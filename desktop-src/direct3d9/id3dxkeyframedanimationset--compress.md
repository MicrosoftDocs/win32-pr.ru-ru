---
description: Преобразует анимации в наборе анимации в сжатый формат и возвращает указатель на буфер, в котором хранятся сжатые данные.
ms.assetid: b70b6dfb-545f-4309-ab72-9543c3c48fc4
title: 'Метод ID3DXKeyframedAnimationSet:: сжимать (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.Compress
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d444ffde525677715f64bd9641cc8fb3cf9513e2c8805a6be28b280aaa12e015
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118802391"
---
# <a name="id3dxkeyframedanimationsetcompress-method"></a>Метод ID3DXKeyframedAnimationSet:: сжимать

Преобразует анимации в наборе анимации в сжатый формат и возвращает указатель на буфер, в котором хранятся сжатые данные.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT Compress(
  [in]  DWORD        Flags,
  [in]  FLOAT        Lossiness,
  [in]  LPD3DXFRAME  pHierarchy,
  [out] LPD3DXBUFFER *ppCompressedData
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Флаги* \[ окне\]
</dt> <dd>

Тип: **[ **DWORD**](../winprog/windows-data-types.md)**

Одно из значений [**\_ флагов D3DXCOMPRESSION**](./d3dxcompression-flags.md) , определяющих режим сжатия, используемый для хранения данных сжатого набора анимации. D3DXCOMPRESS \_ по умолчанию — единственное поддерживаемое в настоящее время значение.

</dd> <dt>

*Потери* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Отношение степени потери сжатия в диапазоне от 0 до 1.

</dd> <dt>

*фиерарчи* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXFRAME**](d3dxframe.md)**

Указатель на иерархию фрейма преобразования [**D3DXFRAME**](d3dxframe.md) . Может иметь **значение NULL**.

</dd> <dt>

*ппкомпресседдата* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)\***

Адрес указателя на набор сжатых данных анимации [**ID3DXBuffer**](id3dxbuffer.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXKeyframedAnimationSet](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
