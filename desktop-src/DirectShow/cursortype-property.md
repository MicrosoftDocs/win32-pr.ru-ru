---
description: Свойство примеры CursorType задает или получает текущий тип курсора.
ms.assetid: f362e790-a7c7-4fb6-86f3-7cd25f78fe0e
title: Примеры CursorType, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c17ae74c471bebe6da2bcef4d22d7c247f4eda1
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "103894709"
---
# <a name="cursortype-property"></a>Примеры CursorType, свойство

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`CursorType`Свойство задает или получает текущий тип курсора.

``` syntax
[ iCursorType = ] MSWebDVD.CursorType
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, представляющее тип курсора.

## <a name="remarks"></a>Комментарии

Возможные значения этого свойства:



| Значение | Описание |
|-------|-------------|
| 0     | Стрелка       |
| 1     | Увеличить     |
| 2     | Уменьшить    |
| 3     | Правый        |
| -1    | Нет        |



 

Это свойство доступно для чтения и записи и имеет нулевое значение по умолчанию. Когда изображение масштабируется, параметр `CursorType` " **рука** " (0x3) переводит приложение в режим перетаскивания, позволяя пользователю перемещать изображение в область экрана.

 

 



