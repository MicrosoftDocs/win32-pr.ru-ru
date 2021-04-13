---
title: Работа с проигрывателем
description: Работа с проигрывателем
ms.assetid: 27aff735-2142-4506-b9d0-2c0fbe60fd6b
keywords:
- Обложки проигрывателя Windows Media, атрибут Player в JScript
- обложки, атрибут Player в JScript
- атрибуты, проигрыватель
- атрибут Player
- Файлы JScript для обложек, атрибут Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d47ea74b4c91f92ef33106e40e9896b98de6a34
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "104411398"
---
# <a name="working-with-the-player"></a>Работа с проигрывателем

При использовании Microsoft JScript для доступа к методам и свойствам проигрывателя Windows Media необходимо использовать имя "Player" в качестве имени элемента управления. Например, для ссылки на метод останавливаться необходимо ввести:


```C++
player.Controls.Stop()

```



Глобальный атрибут **игрока** — это ключ к доступу к элементу управления проигрывателя Windows Media через скрипты обложек. С помощью этого атрибута все объекты элемента управления проигрывателя Windows Media становятся доступными для изменения во время выполнения с помощью их свойств и методов. Кроме того, доступен элемент **Player** , позволяющий задавать обработчики событий и атрибут **URL-адреса** во время разработки.

## <a name="related-topics"></a>См. также

<dl> <dt>

[**Использование JScript**](using-jscript.md)
</dt> </dl>

 

 




