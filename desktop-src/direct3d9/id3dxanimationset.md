---
description: Этот интерфейс инкапсулирует минимальную функциональность, необходимую для набора анимации контроллером анимации.
ms.assetid: vs|directx_sdk|~\id3dxanimationset.htm
title: Интерфейс ID3DXAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: b5aa27494931e8b6c528627fa8e96278a6d86b05
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "104273961"
---
# <a name="id3dxanimationset-interface"></a>Интерфейс ID3DXAnimationSet

Этот интерфейс инкапсулирует минимальную функциональность, необходимую для набора анимации контроллером анимации. Опытным пользователям может потребоваться реализовать этот интерфейс в соответствии со своими потребностями. Однако большинству пользователей, тем не менее, должны быть достаточно производных интерфейсов [**ID3DXCompressedAnimationSet**](id3dxcompressedanimationset.md) и [**ID3DXKeyframedAnimationSet**](id3dxkeyframedanimationset.md) .

## <a name="members"></a>Элементы

Интерфейс **ID3DXAnimationSet** наследует от интерфейса [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) . **ID3DXAnimationSet** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXAnimationSet** содержит следующие методы.



| Метод                                                                        | Описание                                                                       |
|:------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**жетаниматиониндексбинаме**](id3dxanimationset--getanimationindexbyname.md) | Возвращает индекс анимации по ее имени.<br/>                        |
| [**жетаниматионнамебиндекс**](id3dxanimationset--getanimationnamebyindex.md) | Возвращает имя анимации по заданному индексу.<br/>                        |
| [**Метод Callback**](id3dxanimationset--getcallback.md)                         | Возвращает сведения о конкретном обратном вызове в наборе анимации.<br/>       |
| [**GetName**](id3dxanimationset--getname.md)                                 | Возвращает имя набора анимации.<br/>                                           |
| [**жетнуманиматионс**](id3dxanimationset--getnumanimations.md)               | Возвращает число анимаций в наборе анимации.<br/>                    |
| [**Период**](id3dxanimationset--getperiod.md)                             | Возвращает период набора анимации.<br/>                                  |
| [**жетпериодикпоситион**](id3dxanimationset--getperiodicposition.md)         | Возвращает значение времени в локальном интервале в наборе анимации.<br/>      |
| [**жетсрт**](id3dxanimationset--getsrt.md)                                   | Возвращает значения масштаба, вращения и перевода набора анимации.<br/> |



 

## <a name="remarks"></a>Комментарии

Набор анимации состоит из анимации для многих узлов в одной и той же анимации.

Тип LPD3DXANIMATIONSET определяется как указатель на этот интерфейс.


```
typedef interface ID3DXAnimationSet ID3DXAnimationSet;
typedef interface ID3DXAnimationSet *LPD3DXANIMATIONSET;
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

 

 
