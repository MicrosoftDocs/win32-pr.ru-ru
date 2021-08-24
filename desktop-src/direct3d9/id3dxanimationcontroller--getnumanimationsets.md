---
description: Возвращает число наборов анимации, зарегистрированных в данный момент в контроллере анимации.
ms.assetid: 1aacc84d-5025-4601-9a6c-84b3d9b06012
title: 'Метод ID3DXAnimationController:: Жетнуманиматионсетс (D3dx9anim. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationController.GetNumAnimationSets
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 07a6eee85c515c4b8e923aa9973eddc648ef95cbc152c27951154a7c41fbcf3f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120026824"
---
# <a name="id3dxanimationcontrollergetnumanimationsets-method"></a>Метод ID3DXAnimationController:: Жетнуманиматионсетс

Возвращает число наборов анимации, зарегистрированных в данный момент в контроллере анимации.

## <a name="syntax"></a>Синтаксис


```C++
UINT GetNumAnimationSets();
```



## <a name="parameters"></a>Параметры

Этот метод не имеет параметров.

## <a name="return-value"></a>Возвращаемое значение

Тип: **[ **uint**](../winprog/windows-data-types.md)**

Количество наборов анимации.

## <a name="remarks"></a>Remarks

Контроллер содержит любое количество наборов и дорожек анимации. Наборы анимации можно зарегистрировать с помощью [**регистераниматионаутпут**](id3dxanimationcontroller--registeranimationoutput.md). Контроллер анимации, созданный при вызове [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) , будет автоматически регистрировать загруженные наборы анимации.

## <a name="requirements"></a>Requirements (Требования)



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
