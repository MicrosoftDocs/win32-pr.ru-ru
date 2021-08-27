---
description: Составной элемент определяет композицию, объект-контейнер для дорожек и другие вложенные композиции.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: составной элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec9ce7c889829ee227ce31df25d5d17985e877ed107870170f6939aebf14fd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084314"
---
# <a name="composite-element"></a>составной элемент

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`composite`Элемент определяет композицию, объект контейнера для дорожек и другие вложенные композиции.

## <a name="attributes"></a>Атрибуты

[**Блокировка**](lock-attribute.md), [**Отключение звука**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**имя пользователя**](username-attribute.md)

## <a name="parentchild-information"></a>Сведения о родителе и дочернем элементе



| Метка | Значение |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Parent   | `composite`, [ **Группа**](group-element.md)                                                                             |
| Дети | `composite`, [**воздействие**](effect-element.md), [**Трассировка**](track-element.md), [**Переход**](transition-element.md) |



 

## <a name="remarks"></a>Remarks

В пределах `composite` элемента приоритет вложенных слоев определяется неявно в порядке, в котором они отображаются внутри элемента. Первый уровень имеет приоритет 0, а последующие уровни увеличивают значения приоритета.

## <a name="examples"></a>Примеры


```XML
<composite> </composite>
```



## <a name="see-also"></a>См. также

<dl> <dt>

[Элементы КСТЛ](xtl-elements.md)
</dt> </dl>

 

 



