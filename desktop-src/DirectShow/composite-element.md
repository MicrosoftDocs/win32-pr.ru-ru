---
description: Составной элемент определяет композицию, объект-контейнер для дорожек и другие вложенные композиции.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: составной элемент
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c81bf445769c049287bdfa7d23f4ab82bb0f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "105672983"
---
# <a name="composite-element"></a>составной элемент

> [!Note]  
> \[Не рекомендуется. Этот API может быть удален из будущих выпусков Windows.\]

 

`composite`Элемент определяет композицию, объект контейнера для дорожек и другие вложенные композиции.

## <a name="attributes"></a>Атрибуты

[**Блокировка**](lock-attribute.md), [**Отключение звука**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**UserID**](userid-attribute.md), [**имя пользователя**](username-attribute.md)

## <a name="parentchild-information"></a>Сведения о родителе и дочернем элементе



|          |                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Parent   | `composite`, [ **Группа**](group-element.md)                                                                             |
| Дети | `composite`, [**воздействие**](effect-element.md), [**Трассировка**](track-element.md), [**Переход**](transition-element.md) |



 

## <a name="remarks"></a>Комментарии

В пределах `composite` элемента приоритет вложенных слоев определяется неявно в порядке, в котором они отображаются внутри элемента. Первый уровень имеет приоритет 0, а последующие уровни увеличивают значения приоритета.

## <a name="examples"></a>Примеры


```XML
<composite> </composite>
```



## <a name="see-also"></a>См. также раздел

<dl> <dt>

[Элементы КСТЛ](xtl-elements.md)
</dt> </dl>

 

 



