---
description: Возвращает маркер события для события приоритета Blend, выполняющегося в данный момент.
ms.assetid: a7184459-7644-4e65-a8ea-13019889e02b
title: 'Метод ID3DXAnimationController:: Жеткуррентприоритибленд (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetCurrentPriorityBlend
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: c02e65bb17e07b3d75c4949730141831e5b146011e77478d95c8976b792c1c5f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118094559"
---
# <a name="id3dxanimationcontrollergetcurrentpriorityblend-method"></a>Метод ID3DXAnimationController:: Жеткуррентприоритибленд

Возвращает маркер события для события приоритета Blend, выполняющегося в данный момент.

## <a name="syntax"></a>Синтаксис


```C++
D3DXEVENTHANDLE GetCurrentPriorityBlend();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **D3DXEVENTHANDLE**](id3dxanimationcontroller.md)**

Обработчик событий для текущего выполняемого события смешения приоритетов. Возвращается **значение NULL** , если в данный момент не выполняется событие приоритета Blend.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 




