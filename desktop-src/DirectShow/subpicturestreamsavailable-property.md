---
description: Свойство Субпиктурестреамсаваилабле извлекает количество потоков субтитров, доступных в текущем заголовке.
ms.assetid: 6a6d9d15-2f56-47fc-a7bb-2cf33f384f41
title: Субпиктурестреамсаваилабле, свойство
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2349cb696c1f6d363fefb6a6e90a662fa7c3233b3b0aefcb57d381a604f41832
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119633444"
---
# <a name="subpicturestreamsavailable-property"></a>Субпиктурестреамсаваилабле, свойство

> [!Note]  
> этот компонент доступен для использования в операционных системах Microsoft Windows 2000, Windows XP и Windows Server 2003. В последующих версиях он может быть изменен или недоступен.

 

`SubpictureStreamsAvailable`Свойство получает количество потоков субтитров, доступных в текущем заголовке.

``` syntax
[ iStreams = ] MSWebDVD.SubpictureStreamsAvailable
```

## <a name="return-value"></a>Возвращаемое значение

Возвращает количество доступных потоков в виде целого числа.

## <a name="remarks"></a>Remarks

Это свойство доступно только для чтения и не имеет значения по умолчанию. Чтобы запросить каждый поток для своего атрибута языка, сначала вызовите этот метод, чтобы получить верхнюю границу.

Нумерация потоков отсчитывается от нуля.

 

 



