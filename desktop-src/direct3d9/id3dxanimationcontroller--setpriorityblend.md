---
description: Задает весовой коэффициент смешения, используемый контроллером анимации.
ms.assetid: b053024b-f219-48b3-906e-161d9cf47556
title: 'Метод ID3DXAnimationController:: Сетприоритибленд (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.SetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: a4c820858041c730f971ce2821698f86e6ff2c31
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713890"
---
# <a name="id3dxanimationcontrollersetpriorityblend-method"></a>Метод ID3DXAnimationController:: Сетприоритибленд

Задает весовой коэффициент смешения, используемый контроллером анимации.

## <a name="syntax"></a>Синтаксис


```C++
HRESULT SetPriorityBlend(
  [in] FLOAT BlendWeight
);
```



## <a name="parameters"></a>Параметры

<dl> <dt>

*Блендвеигхт* \[ окне\]
</dt> <dd>

Тип: **[ **float**](../winprog/windows-data-types.md)**

Приоритет смешения цветов, используемый контроллером анимации.

</dd> </dl>

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**

Если метод выполнен успешно, возвращается значение S \_ . Если метод завершается с ошибкой, возвращаемое значение может быть одним из следующих значений: D3DERR \_ инвалидкалл.

## <a name="remarks"></a>Комментарии

Вес смешения используется для одновременного смешения дорожек высокого и низкого приоритета.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**жетприоритибленд**](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
