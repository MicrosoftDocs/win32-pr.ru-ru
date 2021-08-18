---
description: Задает приоритет смешивания для указанного направления анимации.
ms.assetid: 8d40b0f6-d79a-42c1-99fb-3f76bd46f30c
title: 'Метод ID3DXAnimationController:: Сеттраккприорити (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetTrackPriority
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: be294710fcd6ec2d8e72c7d7c9437623d29a2729a52144d4edfdc91e5be7eea1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119848974"
---
# <a name="id3dxanimationcontrollersettrackpriority-method"></a>Метод ID3DXAnimationController:: Сеттраккприорити

Задает приоритет смешивания для указанного направления анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetTrackPriority(
  [in] UINT              Track,
  [in] D3DXPRIORITY_TYPE Priority
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Track* \[ окне\]
</dt> <dd>

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Идентификатор трассировки.

</dd> <dt>

*Приоритет* \[ окне\]
</dt> <dd>

Тип: **[ **D3DXPRIORITY \_ тип**](./d3dxpriority-type.md)**

Контроль приоритета. Этому параметру следует присвоить одну из констант [**\_ типа D3DXPRIORITY**](./d3dxpriority-type.md).

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Remarks

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
