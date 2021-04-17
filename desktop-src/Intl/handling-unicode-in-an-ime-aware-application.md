---
description: Обработка Юникода в приложении IME-Aware
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: Обработка Юникода в приложении IME-Aware
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78174776eb608c3e494fd5967acba41609e436a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "105684618"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a>Обработка Юникода в приложении IME-Aware

С помощью IMM вовлечены две проблемы и его обработка в Юникоде. Первая причина заключается в том, что версии Юникода функций IMM извлекают размер буфера в байтах вместо 16-разрядных символов Юникода. Вторая ошибка состоит в том, что модуль IMM обычно извлекает символы Юникода (а не символы DBCS) в сообщениях [**\_ \_ char**](wm-ime-char.md) [**WM \_ char**](../inputdev/wm-char.md) и WM IME.

Windows поддерживает интерфейс Юникод для IMM, а также изначально поддерживаемый интерфейс ANSI.

Приложения должны использовать [**регистерклассв**](/windows/win32/api/winuser/nf-winuser-registerclassa) , чтобы заставить сообщения [**WM \_ char**](../inputdev/wm-char.md) и [**WM \_ IME \_**](wm-ime-char.md) получали символы Юникода вместо символов DBCS в параметре *wParam* .

## <a name="related-topics"></a>См. также

<dl> <dt>

[Использование диспетчера методов ввода](using-input-method-manager.md)
</dt> </dl>

 

 
