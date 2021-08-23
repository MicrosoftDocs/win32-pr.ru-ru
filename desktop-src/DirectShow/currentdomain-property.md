---
description: Свойство CurrentDomain извлекает DVD-домен, в котором находится объект Мсвебдвд.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: CurrentDomain, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf022d44cc3580a4d5208c5bc96413dfa445b0f2fcbf74eeb938ee77fa0677bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118953393"
---
# <a name="currentdomain-property"></a>CurrentDomain, свойство

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`CurrentDomain`Свойство получает DVD-домен, в котором находится объект мсвебдвд.

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, представляющее текущий домен.

## <a name="remarks"></a>Remarks

Возможные значения свойства:



| Значение | Описание          |
|-------|----------------------|
| 1     | Первое воспроизведение           |
| 2     | Меню менеджера видео   |
| 3     | Меню набора заголовков видео |
| 4     | Название                |
| 5     | Stop                 |



 

Вызовите этот метод, чтобы убедиться, что Навигатор DVD находится в допустимом домене для метода, который вы собираетесь вызвать. Например, перед вызовом [**плайтитле**](playtitle-method.md)проверьте свойство, `CurrentDomain` чтобы убедиться, что Навигатор DVD не находится в домене с остановкой или первым воспроизведением.

 

 



