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
ms.openlocfilehash: e52c08d0731bc89135df4547fcfc88e94b56b826d2ccab338576a22651376d94
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120069114"
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

## <a name="remarks"></a>Remarks

Вес смешения используется для одновременного смешения дорожек высокого и низкого приоритета.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**жетприоритибленд**](id3dxanimationcontroller--getpriorityblend.md)
</dt> </dl>

 

 
