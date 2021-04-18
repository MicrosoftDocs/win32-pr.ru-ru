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
ms.openlocfilehash: b5baedb0ea30d51cbd659e597cb000a434ec1632
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105713481"
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

## <a name="remarks"></a>Комментарии

Контроллер содержит любое количество наборов и дорожек анимации. Наборы анимации можно зарегистрировать с помощью [**регистераниматионаутпут**](id3dxanimationcontroller--registeranimationoutput.md). Контроллер анимации, созданный при вызове [**D3DXLoadMeshHierarchyFromX**](d3dxloadmeshhierarchyfromx.md) , будет автоматически регистрировать загруженные наборы анимации.

## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[ID3DXAnimationController](id3dxanimationcontroller.md)
</dt> </dl>

 

 
