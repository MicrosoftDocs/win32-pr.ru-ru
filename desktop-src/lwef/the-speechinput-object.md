---
title: Объект Спичинпут
description: Объект Спичинпут
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 022d96dd52d5847b3fbaa81bbc21d4015698655fba1fe2523aaddc065e6d2ad9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/11/2021
ms.locfileid: "118975524"
---
# <a name="the-speechinput-object"></a>Объект Спичинпут

\[Microsoft Agent является устаревшим по отношению к Windows 7 и может быть недоступен в последующих версиях Windows.\]

Объект [**спичинпут**](https://www.bing.com/search?q=**SpeechInput**) предоставляет доступ к свойствам речевого ввода, поддерживаемым сервером агента. Свойства доступны только для чтения в клиентских приложениях, но пользователь может изменить их на странице свойств Microsoft Agent. Сервер возвращает значения только в том случае, если установлен и включен совместимый обработчик речи.

Свойства [**Engine**](https://www.bing.com/search?q=**Engine**), [**Installed**](https://www.bing.com/search?q=**Installed**)и [**Language**](https://www.bing.com/search?q=**Language**) больше не поддерживаются, но (для обратной совместимости) возвращает значения NULL при запросе. Чтобы запросить или задать режим распознавания речи, используйте свойство [**срмодеид**](srmodeid-property.md) .

-   [Свойства Спичинпут](speechinput-properties.md)

 

 




