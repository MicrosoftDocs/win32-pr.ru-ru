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
ms.openlocfilehash: 6c11a3b356fb0f09cc3372db3ccebd824b4dc8290ff586eed9de3b9fa2ea13ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987964"
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
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
