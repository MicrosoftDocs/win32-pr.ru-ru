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
ms.openlocfilehash: c27e4c6d2cc706b30f2be99030e7bb4a5bccf209
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105720925"
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

## <a name="remarks"></a>Комментарии

Коэффициент смешения приоритетов используется для объединения дорожек высокого и низкого приоритета.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> <dt>

[**сетприоритибленд**](id3dxanimationcontroller--setpriorityblend.md)
</dt> </dl>

 

 
