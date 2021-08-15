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
ms.openlocfilehash: 2eeec6fa26504d30588c5e148c07c6c628cc3ce752a2964d2dbefb3059040236
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118987984"
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



 

## <a name="remarks"></a>Remarks

Тип LPD3DXANIMATIONCALLBACKHANDLER определяется как указатель на этот интерфейс.


```
typedef interface ID3DXAnimationCallbackHandler ID3DXAnimationCallbackHandler;
typedef interface ID3DXAnimationCallbackHandler *LPD3DXANIMATIONCALLBACKHANDLER;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Заголовок<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 
