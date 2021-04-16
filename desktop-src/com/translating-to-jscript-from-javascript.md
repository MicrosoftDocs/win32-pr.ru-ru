---
title: Преобразование в JScript из JavaScript
description: Преобразование в JScript из JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 45535807a5ef2baf59c2e068007a5a8df8bf4863
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 02/20/2020
ms.locfileid: "104533026"
---
# <a name="translating-to-jscript-from-javascript"></a>Преобразование в JScript из JavaScript

JScript в значительной степени совместим с JavaScript. Однако в JScript версии 5,0 есть некоторые объекты, которые в настоящее время не поддерживаются JavaScript, такие как Активексобжект, Enumerator, Error, Global и VBArray.

JScript 5,0 поддерживает обработку исключений с помощью **try**... операторы **catch** . В настоящее время JavaScript не предоставляет механизм обработки ошибок.

При работе с JScript или JavaScript существуют некоторые небольшие различия между реализациями объектной модели, поддерживаемыми различными веб-браузерами. Чтобы написать сценарий, выполняемый как в Internet Explorer, так и в Netscape Navigator, ограничьте функции, используемые скриптами, указанными в стандарте консорциум W3C (W3C) для HTML версии 3,2. Дополнительные сведения об этом стандарте см. в разделе [эталонная спецификация HTML 3,2](https://www.w3.org/TR/REC-html32.html).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Преобразование в JScript](translating-to-jscript.md)
</dt> </dl>

 

 




