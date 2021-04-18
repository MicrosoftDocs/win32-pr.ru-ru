---
description: Удаляет набор эффектов анимации из контроллера анимации.
ms.assetid: 2ca99651-8249-44c2-9560-b3cfaa930862
title: 'Метод ID3DXAnimationController:: Унрегистераниматионсет (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.UnregisterAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 35c70552f16daac6d2cfed5cbccf268179526ae1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694330"
---
# <a name="id3dxanimationcontrollerunregisteranimationset-method"></a>Метод ID3DXAnimationController:: Унрегистераниматионсет

Удаляет набор эффектов анимации из контроллера анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT UnregisterAnimationSet(
  [in] LPD3DXANIMATIONSET pAnimSet
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*панимсет* \[ окне\]
</dt> <dd>

Тип: **[ **LPD3DXANIMATIONSET**](id3dxanimationset.md)**

Указатель на удаляемый набор анимации [**ID3DXAnimationSet**](id3dxanimationset.md) .

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих: D3DERR \_ инвалидкалл, D3DERR \_ NotFound.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




