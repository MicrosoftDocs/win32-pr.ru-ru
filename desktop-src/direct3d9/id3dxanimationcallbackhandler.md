---
description: 'Приложение реализует этот интерфейс для управления обратными вызовами в наборах анимации, созданных вызовами метода ID3DXAnimationController:: AdvanceTime.'
ms.assetid: 5a24ac96-2e68-49c0-acf6-8715d87b202d
title: Интерфейс ID3DXAnimationCallbackHandler (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationCallbackHandler
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: fb3b58c58c6a0bd71924fb207170a177797b9f84
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694295"
---
# <a name="id3dxanimationcallbackhandler-interface"></a>Интерфейс ID3DXAnimationCallbackHandler

Приложение реализует этот интерфейс для управления обратными вызовами в наборах анимации, созданных вызовами метода [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).

## <a name="members"></a>Элементы

Интерфейс **ID3DXAnimationCallbackHandler** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationCallbackHandler** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXAnimationCallbackHandler** содержит следующие методы.



| Метод                                                                  | Описание                                                                                                                                                                                                                                        |
|:------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**хандлекаллбакк**](id3dxanimationcallbackhandler--handlecallback.md) | Приложение реализует этот метод. Этот метод вызывается при возникновении обратного вызова для набора анимации в одной из дорожек во время вызова [**ID3DXAnimationController:: AdvanceTime**](id3dxanimationcontroller--advancetime.md).<br/> |



 

## <a name="remarks"></a>Комментарии

Тип LPD3DXANIMATIONCALLBACKHANDLER определяется как указатель на этот интерфейс.


```
typedef interface ID3DXAnimationCallbackHandler ID3DXAnimationCallbackHandler;
typedef interface ID3DXAnimationCallbackHandler *LPD3DXANIMATIONCALLBACKHANDLER;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
