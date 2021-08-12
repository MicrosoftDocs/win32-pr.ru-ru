---
description: Создает интерфейс набора анимации ID3DXCompressedAnimationSet с кадром, который хранит данные опорных кадров в сжатом формате.
ms.assetid: c3f97d35-5654-4d85-a337-d77819ce3874
title: Функция D3DXCreateCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateCompressedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 2acca9d1b697bb9b06b47aa75948ca74ec00cc7ecb919334c01cf874293cb495
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118299289"
---
# <a name="d3dxcreatecompressedanimationset-function"></a>Функция D3DXCreateCompressedAnimationSet

Создает интерфейс набора анимации [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) с кадром, который хранит данные опорных кадров в сжатом формате.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateCompressedAnimationSet(
  _In_        LPCSTR                       pName,
  _In_        DOUBLE                       TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE            Playback,
  _In_        LPD3DXBUFFER                 pCompressedData,
  _In_        UINT                         NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK           *pCallKeys,
  _Out_       LPD3DXCOMPRESSEDANIMATIONSET *ppAnimationSet
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*pName* \[ окне\]
</dt> <dd>

Тип: **[ **LPCSTR**](../winprog/windows-data-types.md)**

Указатель на имя набора анимации.

</dd> <dt>

*Тикксперсеконд* \[ окне\]
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Число тактов опорного кадра в секунду.

</dd> <dt>

*Воспроизведение* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXPLAYBACK \_ тип**](./d3dxplayback-type.md)**

Тип цикла воспроизведения набора анимации. См. раздел [**\_ тип D3DXPLAYBACK**](./d3dxplayback-type.md).

</dd> <dt>

*пкомпресседдата* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXBUFFER**](id3dxbuffer.md)**

Указатель на буфер [**ID3DXBuffer**](id3dxbuffer.md) , в котором набор анимации хранится в виде сжатых данных.

</dd> <dt>

*Нумкаллбакккэйс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Число ключей обратного вызова.

</dd> <dt>

*пкаллкэйс* \[ окне\]
</dt> <dd>

Тип: **const [**LPD3DXKEY \_ callback**](d3dxkey-callback.md) \***

Указатель на структуру [**\_ обратного вызова D3DXKEY**](d3dxkey-callback.md) , в которой хранятся данные обратного вызова пользователя.

</dd> <dt>

*ппаниматионсет* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXCOMPRESSEDANIMATIONSET**](id3dxcompressedanimationset.md)\***

Адрес указателя на интерфейс [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) , в котором хранятся данные набора анимаций с кадрами в сжатом формате.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если функция выполнена успешно, возвращается значение S \_ ОК. Если функция завершается ошибкой, возвращаемое значение может иметь одно из следующих значений: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Функции анимации](dx9-graphics-reference-d3dx-functions-animation.md)
</dt> </dl>

 

 
