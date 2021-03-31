---
description: .
ms.assetid: 1cb0456d-501a-4272-b89d-35e79d29d13a
title: Internet Explorer 8 — строка агента пользователя
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7be481cf409468d9d182d37ae7636b167bc71d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910588"
---
# <a name="internet-explorer-8---user-agent-string"></a>Internet Explorer 8 — строка агента пользователя

## <a name="affected-platforms"></a>Затронутые платформы

 **Клиенты** — Windows XP Windows Vista, Windows \| \| 7  
**Серверы** — windows Server 2003 windows \| Server 2008 \| Windows Server 2008 R2  










## <a name="feature-impact"></a>Воздействие на функции

**Серьезность** — средний  
**Частота** — высокая  











## <a name="description"></a>Описание

Строка агента пользователя — это идентификатор Internet Explorer, предоставляющий данные о версии и других атрибутах для веб-серверов. Многие веб-приложения основываются на строке агента пользователя IE и проникновения в ней. Будут затронуты те, которые делают это и зависят от более раннего номера версии. Строка агента пользователя теперь содержит строку "Trident/4.0", позволяющую различать строку агента пользователя Internet Explorer 7 и строку агента пользователя Internet Explorer 8 при запуске в режиме совместимости Internet Explorer 7. Дополнительные сведения см. в разделе Основные сведения о строках агента пользователя.

## <a name="manifestation-of-impact"></a>Влияние на манифесты

Есть две затронутые области:

-   Веб-страницы, которые явно проверяют строку агента пользователя и не поддерживают строку агента пользователя Internet Explorer 8, могут работать неправильно. В большинстве случаев это означает, что страницы будут блокировать пользователей из содержимого, на которое они пытаются получить доступ, или отобразить неверное или неверное содержимое.
-   Приложения, размещающие Trident (см. раздел размещение и повторное использование), по умолчанию будут использовать Internet Explorer 7 с помощью веб-дополнительного компонента, но не будут иметь доступа к функциям Internet Explorer 8.

## <a name="solution"></a>Решение

Убедитесь, что ваши приложения должным образом обрабатывали новую версию "MSIE 8,0" в строке агента пользователя. Вы также можете выбрать представление совместимости Internet Explorer 7 для этих приложений на основе Internet Explorer 7. Это можно сделать с помощью meta tags. Дополнительные сведения см. в обсуждении о строках агента пользователя.

## <a name="compatibility-performance-reliability-and-usability-testing"></a>Совместимость, производительность, надежность и тестирование на удобство использования

-   Запустите приложения и веб-страницы в среде Internet Explorer 8 в Windows Vista или Windows XP, чтобы убедиться, что они ведут себя нужным образом.
-   Кроме того, можно запустить средство тестирования совместимости Internet Explorer (ИЕКТТ), предоставляемое вместе с набором средств для обеспечения совместимости приложений (ACT), для выявления потенциальных проблем, связанных с обновлениями функций безопасности.

## <a name="links-to-other-resources"></a>Ссылки на другие ресурсы

-   [Основные сведения о строках агента пользователя](/previous-versions/windows/internet-explorer/ie-developer/compatibility/ms537503(v=vs.85))
-   [Строка User-Agent Internet Explorer 8](/archive/blogs/ie/)
-   [Строка и вектор версии агента пользователя](https://archive.msdn.microsoft.com/ie8whitepapers)
-   [Размещение и повторное использование](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/aa752038(v=vs.85))
-   [Загрузка набора средств для обеспечения совместимости приложений](/windows-hardware/get-started/adk-install)
-   [Известные проблемы с функциями безопасности в Internet Explorer](/previous-versions/windows/it-pro/windows-7/cc722079(v=ws.10))

 

 
