---
title: Ссылки на обложки в URL-адресах
description: Ссылки на обложки в URL-адресах
ms.assetid: 9ae30c12-2dee-46b2-90e2-c101a83856fb
keywords:
- Обложки проигрывателя Windows Media, URL-ссылки
- обложки, URL-ссылки
- URL-ссылки в обложках
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75b33ac9a5f37dce242797ae93dc4e85b973c76b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103779583"
---
# <a name="referencing-skins-in-urls"></a>Ссылки на обложки в URL-адресах

Если для загрузки файла мультимедиа, который будет воспроизводиться проигрывателем Windows Media, используется URL-адрес, можно запросить использование определенной обложки с этим файлом. Если обложка уже установлена на компьютере пользователя, она будет использоваться. в противном случае будет использоваться Предыдущая обложка.

Чтобы запросить обложку, добавьте в конец URL-адреса следующее:


```C++
?WMPSkin=skinname
```



*скиннаме* — имя обложки, которую необходимо запросить. Не используйте кавычки вокруг имени обложки.

Например, чтобы запросить использование обложки хеадспаце, введите следующий URL-адрес http:


```C++
https://www.proseware.com/mymedia.wma?WMPSkin=headspace

```



## <a name="related-topics"></a>См. также

<dl> <dt>

[**О обложках**](about-skins.md)
</dt> </dl>

 

 




