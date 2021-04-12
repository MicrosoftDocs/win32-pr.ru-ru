---
description: Задает скорость записи. Скорость записи аналогична множителю, который используется для ускорения или снижения скорости воспроизведения.
ms.assetid: b3946b61-0676-4690-9844-639fabd8fd7c
title: 'Метод ID3DXAnimationController:: Сеттраккспид (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackSpeed
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 6cf57df2db370921c633ab695c9f60b96d2183dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355953"
---
# <a name="id3dxanimationcontrollersettrackspeed-method"></a>Метод ID3DXAnimationController:: Сеттраккспид

Задает скорость записи. Скорость записи аналогична множителю, который используется для ускорения или снижения скорости воспроизведения.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetTrackSpeed(
  [in] UINT  Track,
  [in] FLOAT Speed
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Track* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор записи, для которой задается скорость.

</dd> <dt>

*Скорость передачи* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Новая скорость.

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

 

 
