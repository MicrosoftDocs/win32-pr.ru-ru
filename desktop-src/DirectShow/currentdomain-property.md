---
description: Свойство CurrentDomain извлекает DVD-домен, в котором находится объект Мсвебдвд.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: CurrentDomain, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead6d61cd622fceac2a4d133a0297892992e763a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495150"
---
# <a name="currentdomain-property"></a>CurrentDomain, свойство

> [!Note]  
> Этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`CurrentDomain`Свойство получает DVD-домен, в котором находится объект мсвебдвд.

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает целочисленное значение, представляющее текущий домен.

## <a name="remarks"></a>Комментарии

Возможные значения свойства:



| Значение | Описание          |
|-------|----------------------|
| 1     | Первое воспроизведение           |
| 2     | Меню менеджера видео   |
| 3     | Меню набора заголовков видео |
| 4     | Заголовок                |
| 5     | Stop                 |



 

Вызовите этот метод, чтобы убедиться, что Навигатор DVD находится в допустимом домене для метода, который вы собираетесь вызвать. Например, перед вызовом [**плайтитле**](playtitle-method.md)проверьте свойство, `CurrentDomain` чтобы убедиться, что Навигатор DVD не находится в домене с остановкой или первым воспроизведением.

 

 



