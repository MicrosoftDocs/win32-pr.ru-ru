---
title: Преобразование в JavaScript из JScript
description: Преобразование в JavaScript из JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71b18972f407cf008626245798b3f7740d98058e
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104412615"
---
# <a name="translating-to-javascript-from-jscript"></a>Преобразование в JavaScript из JScript

JScript в значительной степени совместим с JavaScript. Однако в JScript есть некоторые объекты, которые в настоящее время не поддерживаются JavaScript, такие как Активексобжект, Enumerator, Error, Global и VBArray.

JScript версии 5,0 поддерживает обработку исключений с помощью **try**... операторы **catch** . В настоящее время JavaScript не предоставляет механизм обработки ошибок.

При работе с JScript или JavaScript существуют некоторые небольшие различия между реализациями объектной модели, поддерживаемыми различными веб-браузерами. Чтобы написать сценарий, выполняемый как в Internet Explorer, так и в Netscape Navigator, ограничьте функции, используемые скриптами, указанными в стандарте консорциум W3C (W3C) [для HTML версии 3,2](https://www.w3.org/tr/rec-html32.html).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Преобразование в JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




