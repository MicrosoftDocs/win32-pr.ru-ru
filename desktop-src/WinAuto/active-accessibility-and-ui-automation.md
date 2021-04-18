---
title: Active Accessibility и автоматизация пользовательского интерфейса
description: Microsoft Active Accessibility предназначен для использования с операционными системами Windows XP и более ранних версий.
ms.assetid: 8eb36d2c-0c2f-4311-8690-52ce070c9f33
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2483f4f6679926ef2f87c380d4ac0febcc88652
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "105700693"
---
# <a name="active-accessibility-and-ui-automation"></a>Active Accessibility и автоматизация пользовательского интерфейса

Microsoft Active Accessibility предназначен для использования с операционными системами Windows XP и более ранних версий. Разработчикам пользовательских элементов управления и доступных технологических клиентских приложений для Windows XP и Windows Vista рекомендуется использовать технологию Microsoft [UI Automation](entry-uiauto-win32.md) .

Автоматизация пользовательского интерфейса Майкрософт — это полнофункциональная система, которая предоставляет более точную информацию о пользовательском интерфейсе и предоставляет пользователю больше возможностей для взаимодействия с элементами управления. В частности, он обеспечивает значительно расширенную поддержку текста.

Набор прокси-объектов обеспечивает поддержку автоматизации пользовательского интерфейса для стандартных элементов управления Microsoft Win32 и Windows Forms. Расширенная поддержка доступна для элементов управления, специально написанных с помощью модели автоматизации пользовательского интерфейса, включая элементы машинного Windows Presentation Foundation (WPF), которые не поддерживают непосредственно Microsoft Active Accessibility. Пользовательские элементы управления, поддерживающие автоматизацию пользовательского интерфейса, могут быть написаны как в управляемом, так и в неуправляемом коде.

Клиенты Microsoft Active Accessibility имеют ограниченный доступ через мостный уровень к элементам пользовательского интерфейса, поддерживающим только автоматизацию пользовательского интерфейса. Дополнительные сведения см. [в приложении ж: Active Accessibility Bridge to Automation UI](appendix-g--active-accessibility-bridge-to-ui-automation.md).

Дополнительные сведения о сходствах и различиях между Microsoft Active Accessibility и автоматизацией пользовательского интерфейса см. в [статье сравнение microsoft Active Accessibility и модели автоматизации пользовательского интерфейса](microsoft-active-accessibility-and-ui-automation-compared.md).

## <a name="related-topics"></a>См. также

<dl> <dt>

**Зрения**
</dt> <dt>

[Начало работы](getting-started.md)
</dt> <dt>

[Модель автоматизации пользовательского интерфейса](entry-uiauto-win32.md)
</dt> </dl>

 

 




