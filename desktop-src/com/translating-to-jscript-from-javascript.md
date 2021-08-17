---
title: преобразование в JScript из JavaScript
description: преобразование в JScript из JavaScript
ms.assetid: 86067a69-a6a1-474f-b8d8-85caf384a311
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51c25276d569c5b461693a666d1bf8cf706b6896c0995972e1d2af0071c5760b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129566"
---
# <a name="translating-to-jscript-from-javascript"></a>преобразование в JScript из JavaScript

JScript в значительной степени совместима с JavaScript. однако JScript версии 5,0 включает в себя некоторые объекты, которые в настоящее время не поддерживаются JavaScript, такие как активексобжект, Enumerator, Error, Global и VBArray.

JScript 5,0 поддерживает обработку исключений с помощью **try**... операторы **catch** . В настоящее время JavaScript не предоставляет механизм обработки ошибок.

при работе с JScript или JavaScript существует ряд незначительных различий между реализациями объектной модели, поддерживаемыми различными веб-браузерами. Чтобы написать сценарий, выполняемый как в Internet Explorer, так и в Netscape Navigator, ограничьте функции, используемые скриптами, указанными в стандарте консорциум W3C (W3C) для HTML версии 3,2. Дополнительные сведения об этом стандарте см. в разделе [эталонная спецификация HTML 3,2](https://www.w3.org/TR/REC-html32.html).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Перевод в JScript](translating-to-jscript.md)
</dt> </dl>

 

 




