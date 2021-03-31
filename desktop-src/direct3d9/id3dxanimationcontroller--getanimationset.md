---
description: Возвращает набор анимации.
ms.assetid: 61785f60-82c1-4ddc-b4cd-2e7f665cfe8c
title: 'Метод ID3DXAnimationController:: Animation (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c21f073b74d1ab7dac09ddd8bfb3d6be543e122a
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104157211"
---
# <a name="id3dxanimationcontrollergetanimationset-method"></a>Метод ID3DXAnimationController:: Animation

Возвращает набор анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT GetAnimationSet(
  [in]  UINT               Index,
  [out] LPD3DXANIMATIONSET *ppAnimSet
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Индекс* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Индекс набора анимации.

</dd> <dt>

*ппанимсет* \[ заполняет\]
</dt> <dd>

Тип: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)\***

Указатель на набор эффектов анимации [**ID3DXAnimationSet**](id3dxanimationset.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Контроллер анимации содержит массив наборов анимации. Этот метод возвращает один из них по указанному индексу.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
