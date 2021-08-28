---
description: Получает текущий приоритет смешения цветов, используемый контроллером анимации.
ms.assetid: ceaf611e-e85b-4958-b8ac-7e60b98b1aad
title: 'Метод ID3DXAnimationController:: Жетприоритибленд (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f66e4f0d6c36d2de655c8dee5f0cfbee3b5aa03d4750c5e2a8faaea43a24c657
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119373154"
---
# <a name="id3dxanimationcontrollergetpriorityblend-method"></a>Метод ID3DXAnimationController:: Жетприоритибленд

Получает текущий приоритет смешения цветов, используемый контроллером анимации.

## <a name="syntax"></a>Синтаксис


```C++
FLOAT GetPriorityBlend();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **float**](../winprog/windows-data-types.md)**

Возвращает коэффициент смешения текущего приоритета.

## <a name="remarks"></a>Remarks

Коэффициент смешения приоритетов используется для объединения дорожек высокого и низкого приоритета.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**сетприоритибленд**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
