---
description: Приложение использует методы этого интерфейса для реализации набора анимации ключевых кадров, хранящегося в сжатом формате данных.
ms.assetid: 858f09b7-c3b6-4e22-8017-ce2d6188ba80
title: Интерфейс ID3DXCompressedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXCompressedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 33dd1017859be14924d8d40265696cfb552754ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105674703"
---
# <a name="id3dxcompressedanimationset-interface"></a>Интерфейс ID3DXCompressedAnimationSet

Приложение использует методы этого интерфейса для реализации набора анимации ключевых кадров, хранящегося в сжатом формате данных.

## <a name="members"></a>Элементы

Интерфейс **ID3DXCompressedAnimationSet** наследует от [**ID3DXAnimationSet**](id3dxanimationset.md). **ID3DXCompressedAnimationSet** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXCompressedAnimationSet** содержит следующие методы.



| Метод                                                                                  | Описание                                                                      |
|:----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| [**жеткаллбакккэйс**](id3dxcompressedanimationset--getcallbackkeys.md)                 | Заполняет массив данными ключа обратного вызова, используемым для анимации ключевых кадров.<br/>   |
| [**жеткомпресседдата**](id3dxcompressedanimationset--getcompresseddata.md)             | Возвращает буфер данных, в котором хранятся сжатые данные анимации с помощью ключевых кадров.<br/> |
| [**жетнумкаллбакккэйс**](id3dxcompressedanimationset--getnumcallbackkeys.md)           | Возвращает число ключей обратного вызова в наборе анимации.<br/>                |
| [**жетплайбакктипе**](id3dxcompressedanimationset--getplaybacktype.md)                 | Возвращает тип цикла воспроизведения набора анимации.<br/>                     |
| [**жетсаурцетикксперсеконд**](id3dxcompressedanimationset--getsourcetickspersecond.md) | Возвращает число тактов кадра анимации, произошедших в секунду.<br/>   |



 

## <a name="remarks"></a>Комментарии

Создайте набор анимации по ключевым кадрам из сжатого формата с помощью [**D3DXCreateCompressedAnimationSet**](d3dxcreatecompressedanimationset.md).

Тип LPD3DXCOMPRESSEDANIMATIONSET определяется как указатель на этот интерфейс.


```
typedef interface ID3DXCompressedAnimationSet ID3DXCompressedAnimationSet;
typedef interface ID3DXCompressedAnimationSet *LPD3DXCOMPRESSEDANIMATIONSET;
```



## <a name="requirements"></a>Требования



| Требование | Значение |
|--------------------|----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>D3dx9anim. h</dt> </dl> |
| Библиотека<br/> | <dl> <dt>D3dx9. lib</dt> </dl>   |



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[**ID3DXAnimationSet**](id3dxanimationset.md)
</dt> <dt>

[Интерфейсы D3DX](dx9-graphics-reference-d3dx-interfaces.md)
</dt> </dl>

 

 




