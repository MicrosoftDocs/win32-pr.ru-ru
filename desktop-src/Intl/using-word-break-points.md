---
description: Когда приложение работает с целыми словами, допустимые позиции для курсора помечаются значением элемента Фвордстоп \_ структуры Script логаттр. Это значение извлекается путем вызова Скриптбреак.
ms.assetid: c9bbfb51-727a-45ff-8450-774bc106f9f7
title: Использование точек останова Word
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b9cf68d5c90b6e93a6e6f15706ec357c7a33b23
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "104272948"
---
# <a name="using-word-break-points"></a>Использование точек останова Word

Когда приложение работает с целыми словами, допустимые позиции для курсора помечаются значением элемента **фвордстоп** структуры [**script \_ логаттр**](/windows/win32/api/usp10/ns-usp10-script_logattr) . Это значение извлекается путем вызова [**скриптбреак**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

Допустимые позиции для разбиения строк между словами помечаются значением **фсофтбреак** , полученным с помощью [**скриптбреак**](/windows/desktop/api/Usp10/nf-usp10-scriptbreak).

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование Uniscribe](using-uniscribe.md)
</dt> </dl>

 

 



