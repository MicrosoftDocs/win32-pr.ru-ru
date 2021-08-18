---
title: Преобразование в JavaScript из JScript
description: Преобразование в JavaScript из JScript
ms.assetid: 11d31c8c-868d-4220-9298-6d24a209dc47
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49c4adb5827952cc9bab0dac268997b5b73a52ecd1403e5431cdb3939b08c7e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119129586"
---
# <a name="translating-to-javascript-from-jscript"></a>Преобразование в JavaScript из JScript

JScript в значительной степени совместима с JavaScript. однако JScript содержит некоторые объекты, которые в настоящее время не поддерживаются JavaScript, такие как активексобжект, Enumerator, Error, Global и VBArray.

JScript версии 5,0 поддерживает обработку исключений с помощью **try**... операторы **catch** . В настоящее время JavaScript не предоставляет механизм обработки ошибок.

при работе с JScript или JavaScript существует ряд незначительных различий между реализациями объектной модели, поддерживаемыми различными веб-браузерами. Чтобы написать сценарий, выполняемый как в Internet Explorer, так и в Netscape Navigator, ограничьте функции, используемые скриптами, указанными в стандарте консорциум W3C (W3C) [для HTML версии 3,2](https://www.w3.org/tr/rec-html32.html).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Преобразование в JavaScript](translating-to-javascript.md)
</dt> </dl>

 

 




