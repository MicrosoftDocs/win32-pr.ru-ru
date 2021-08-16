---
description: Когда приложение работает с целыми словами, допустимые позиции для курсора помечаются значением элемента Фвордстоп \_ структуры Script логаттр. Это значение извлекается путем вызова Скриптбреак.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Использование точек останова Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 733d761d15299e02fbfb84d541a7ceba5d4d77a9b57e0280bfeedee24532d8cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "119146867"
---
# <a name="using-word-break-points"></a>Использование точек останова Word

Когда приложение работает с целыми словами, допустимые позиции для курсора помечаются значением элемента **фвордстоп** структуры [**script \_ логаттр**](/windows/win32/api/usp10/ns-usp10-script_logattr) . Это значение извлекается путем вызова [**скриптбреак**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

Допустимые позиции для разбиения строк между словами помечаются значением **фсофтбреак** , полученным с помощью [**скриптбреак**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

## <a name="related-topics"></a>Связанные темы

<dl> <dt>

[Использование Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



