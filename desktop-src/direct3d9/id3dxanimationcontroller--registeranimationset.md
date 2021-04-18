---
description: Добавляет набор эффектов анимации к контроллеру анимации.
ms.assetid: 93351d61-b7f4-4bd1-a5bf-313911cf6b61
title: 'Метод ID3DXAnimationController:: Регистераниматионсет (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.RegisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ca70baf55a3dae19422c9026575d75f63eed4bde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713892"
---
# <a name="id3dxanimationcontrollerregisteranimationset-method"></a>Метод ID3DXAnimationController:: Регистераниматионсет

Добавляет набор эффектов анимации к контроллеру анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT RegisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*панимсет* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Указатель на добавляемый набор анимации [**ID3DXAnimationSet**](id3dxanimationset.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, будет возвращено следующее значение: D3DERR \_ инвалидкалл.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




