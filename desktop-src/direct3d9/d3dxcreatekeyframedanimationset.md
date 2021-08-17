---
description: Создает интерфейс набора анимации с ID3DXKeyframedAnimationSet ключом в рамке.
ms.assetid: 7b4fffdc-696c-400c-a0cc-fc755fd25b75
title: Функция D3DXCreateKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXCreateKeyframedAnimationSet
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c4fbfb31b712e1521930fa468bae315a443105f3a6bc0863fe3267f9586f874a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118804570"
---
# <a name="d3dxcreatekeyframedanimationset-function"></a>Функция D3DXCreateKeyframedAnimationSet

Создает интерфейс набора анимации с [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) ключом в рамке.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT D3DXCreateKeyframedAnimationSet(
  _In_        LPCSTR                      pName,
  _In_        DOUBLE                      TicksPerSecond,
  _In_        D3DXPLAYBACK_TYPE           Playback,
  _In_        UINT                        NumAnimations,
  _In_        UINT                        NumCallbackKeys,
  _In_  const LPD3DXKEY_CALLBACK          *pCallKeys,
  _Out_       LPD3DXKEYFRAMEDANIMATIONSET *ppAnimationSet
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

*Нуманиматионс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество наборов анимации Scale, вращение и сдвига (SRT).

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

Тип: **[ **LPD3DXKEYFRAMEDANIMATIONSET**](id3dxkeyframedanimationset.md)\***

Адрес указателя на интерфейсный набор эффектов анимации [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) Key.

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

 

 
