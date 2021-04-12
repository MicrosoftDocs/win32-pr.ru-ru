---
description: Выполняет клонирование или копирование контроллера анимации.
ms.assetid: 9836653c-9ea5-4fbc-89ac-0b46054a12d7
title: 'Метод ID3DXAnimationController:: Клонеаниматионконтроллер (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.CloneAnimationController
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 49c4a1c000df469c72a5e5538237e7110ded126f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104355800"
---
# <a name="id3dxanimationcontrollercloneanimationcontroller-method"></a>Метод ID3DXAnimationController:: Клонеаниматионконтроллер

Выполняет клонирование или копирование контроллера анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT CloneAnimationController(
  [in] UINT                      MaxNumAnimationOutputs,
  [in] UINT                      MaxNumAnimationSets,
  [in] UINT                      MaxNumTracks,
  [in] UINT                      MaxNumEvents,
  [in] LPD3DXANIMATIONCONTROLLER *ppAnimController
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Макснуманиматионаутпутс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Максимальное число выводов анимации, которые может поддерживать контроллер.

</dd> <dt>

*Макснуманиматионсетс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Максимальное число наборов анимации, которое может поддерживать контроллер.

</dd> <dt>

*Макснумтраккс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Максимальное число дорожек, которое может поддерживать контроллер.

</dd> <dt>

*Макснумевентс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Максимальное число событий, которое может поддерживать контроллер.

</dd> <dt>

*ппанимконтроллер* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXANIMATIONCONTROLLER**](id3dxanimationcontroller.md)\***

Адрес указателя на клонированный контроллер анимации [**ID3DXAnimationController**](id3dxanimationcontroller.md) .

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

 

 
