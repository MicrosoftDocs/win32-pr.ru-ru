---
description: Приложение использует методы этого интерфейса для реализации набора анимации по ключевым кадрам.
ms.assetid: eeb7acd8-1017-4aca-9813-188fc6703837
title: Интерфейс ID3DXKeyframedAnimationSet (D3dx9anim. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 0e45ab69b3a91461c947ce9c8a63885bb5ab0a8e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 03/15/2021
ms.locfileid: "105694287"
---
# <a name="id3dxkeyframedanimationset-interface"></a>Интерфейс ID3DXKeyframedAnimationSet

Приложение использует методы этого интерфейса для реализации набора анимации по ключевым кадрам.

## <a name="members"></a>Элементы

Интерфейс **ID3DXKeyframedAnimationSet** наследует от [**ID3DXAnimationSet**](id3dxanimationset.md). **ID3DXKeyframedAnimationSet** также имеет следующие типы членов:

-   [Методы](#methods)

### <a name="methods"></a>Методы

Интерфейс **ID3DXKeyframedAnimationSet** содержит следующие методы.



| Метод                                                                                   | Описание                                                                                                                                        |
|:-----------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Сжатие**](id3dxkeyframedanimationset--compress.md)                                 | Преобразует анимации в наборе анимации в сжатый формат и возвращает указатель на буфер, в котором хранятся сжатые данные.<br/> |
| [**жеткаллбакккэй**](id3dxkeyframedanimationset--getcallbackkey.md)                     | Возвращает сведения о конкретном обратном вызове в наборе анимации.<br/>                                                                        |
| [**жеткаллбакккэйс**](id3dxkeyframedanimationset--getcallbackkeys.md)                   | Заполняет массив данными ключа обратного вызова, используемым для анимации ключевых кадров.<br/>                                                                     |
| [**жетнумкаллбакккэйс**](id3dxkeyframedanimationset--getnumcallbackkeys.md)             | Возвращает число ключей обратного вызова в наборе анимации.<br/>                                                                                  |
| [**жетнумротатионкэйс**](id3dxkeyframedanimationset--getnumrotationkeys.md)             | Возвращает число ключей вращения в указанной анимации по опорным кадрам.<br/>                                                                  |
| [**жетнумскалекэйс**](id3dxkeyframedanimationset--getnumscalekeys.md)                   | Возвращает количество ключей масштабирования в указанной анимации по опорным кадрам.<br/>                                                                     |
| [**жетнумтранслатионкэйс**](id3dxkeyframedanimationset--getnumtranslationkeys.md)       | Возвращает число ключей перевода в указанной анимации по ключевым кадрам.<br/>                                                               |
| [**жетплайбакктипе**](id3dxkeyframedanimationset--getplaybacktype.md)                   | Возвращает тип цикла воспроизведения набора анимации.<br/>                                                                                       |
| [**жетротатионкэй**](id3dxkeyframedanimationset--getrotationkey.md)                     | Получение сведений о повороте для определенного ключевого кадра в наборе анимации.<br/>                                                                 |
| [**жетротатионкэйс**](id3dxkeyframedanimationset--getrotationkeys.md)                   | Заполняет массив данными ротации ключей, используемыми для анимации ключевых кадров.<br/>                                                                   |
| [**жетскалекэй**](id3dxkeyframedanimationset--getscalekey.md)                           | Получение сведений о масштабе для определенного ключевого кадра в наборе анимации.<br/>                                                                    |
| [**жетскалекэйс**](id3dxkeyframedanimationset--getscalekeys.md)                         | Заполняет массив данными ключа шкалы, используемыми для анимации ключевых кадров.<br/>                                                                        |
| [**жетсаурцетикксперсеконд**](id3dxkeyframedanimationset--getsourcetickspersecond.md)   | Возвращает число тактов кадра анимации, произошедших в секунду.<br/>                                                                     |
| [**жеттранслатионкэй**](id3dxkeyframedanimationset--gettranslationkey.md)               | Получение сведений о переводе для определенного ключевого кадра в наборе анимации.<br/>                                                              |
| [**жеттранслатионкэйс**](id3dxkeyframedanimationset--gettranslationkeys.md)             | Заполняет массив данными ключа, используемыми для анимации ключевых кадров.<br/>                                                                |
| [**регистераниматионсрткэйс**](id3dxkeyframedanimationset--registeranimationsrtkeys.md) | Зарегистрируйте данные опорного кадра шкалы, вращения и перевода (SRT) для анимации.<br/>                                                        |
| [**сеткаллбакккэй**](id3dxkeyframedanimationset--setcallbackkey.md)                     | Задает сведения о конкретном обратном вызове в наборе анимации.<br/>                                                                        |
| [**сетротатионкэй**](id3dxkeyframedanimationset--setrotationkey.md)                     | Установка сведений о повороте для определенного ключевого кадра в наборе анимации.<br/>                                                                 |
| [**сетскалекэй**](id3dxkeyframedanimationset--setscalekey.md)                           | Установка сведений о масштабе для определенного ключевого кадра в наборе анимации.<br/>                                                                    |
| [**сеттранслатионкэй**](id3dxkeyframedanimationset--settranslationkey.md)               | Задание сведений о переводе для определенного ключевого кадра в наборе анимации.<br/>                                                              |
| [**унрегистераниматион**](id3dxkeyframedanimationset--unregisteranimation.md)           | Удалите данные анимации из набора анимации.<br/>                                                                                       |
| [**унрегистерротатионкэй**](id3dxkeyframedanimationset--unregisterrotationkey.md)       | Удаляет данные вращения в указанном опорном кадре.<br/>                                                                                   |
| [**унрегистерскалекэй**](id3dxkeyframedanimationset--unregisterscalekey.md)             | Удаляет данные шкалы в указанном опорном кадре.<br/>                                                                                      |
| [**унрегистертранслатионкэй**](id3dxkeyframedanimationset--unregistertranslationkey.md) | Удаляет данные перевода в указанном опорном кадре.<br/>                                                                                |



 

## <a name="remarks"></a>Комментарии

Создание набора анимации по ключевым кадрам с помощью [**D3DXCreateKeyframedAnimationSet**](d3dxcreatekeyframedanimationset.md).

Тип LPD3DXKEYFRAMEDANIMATIONSET определяется как указатель на этот интерфейс.


```
typedef interface ID3DXKeyframedAnimationSet ID3DXKeyframedAnimationSet;
typedef interface ID3DXKeyframedAnimationSet *LPD3DXKEYFRAMEDANIMATIONSET;
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

 

 




