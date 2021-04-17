---
description: Выполняет анимацию сетки и перемещает глобальное время анимации на заданный объем.
ms.assetid: a822d92a-c301-4289-b67b-1df99808c79d
title: 'Метод ID3DXAnimationController:: AdvanceTime (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.AdvanceTime
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 848e1f8aadd302b9194168e92b2b0abe732a2c2f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694294"
---
# <a name="id3dxanimationcontrolleradvancetime-method"></a>Метод ID3DXAnimationController:: AdvanceTime

Выполняет анимацию сетки и перемещает глобальное время анимации на заданный объем.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT AdvanceTime(
  [in] DOUBLE                         TimeDelta,
  [in] LPD3DXANIMATIONCALLBACKHANDLER pCallbackHandler
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Тимеделта* \[ окне\]
</dt> <dd>

Тип: **[ **Double**](../winprog/windows-data-types.md)**

Величина (в секундах), с которой следует переместить глобальное время анимации. Значение Тимеделта не может быть отрицательным или равным нулю.

</dd> <dt>

*пкаллбаккхандлер* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXANIMATIONCALLBACKHANDLER**](id3dxanimationcallbackhandler.md)**

Указатель на пользовательский интерфейс обработчика обратного вызова анимации [**ID3DXAnimationCallbackHandler**](id3dxanimationcallbackhandler.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, E \_ OUTOFMEMORY.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
