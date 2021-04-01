---
title: Объект Спичинпут
description: Объект Спичинпут
ms.assetid: e968edb8-747f-421a-800b-29f13857410c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1671a3f3e37b0de16b42129921337ee855b58c14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 09/16/2019
ms.locfileid: "103986630"
---
# <a name="the-speechinput-object"></a>Объект Спичинпут

\[Microsoft Agent является устаревшим в Windows 7 и может быть недоступен в последующих версиях Windows.\]

Объект [**спичинпут**](https://www.bing.com/search?q=**SpeechInput**) предоставляет доступ к свойствам речевого ввода, поддерживаемым сервером агента. Свойства доступны только для чтения в клиентских приложениях, но пользователь может изменить их на странице свойств Microsoft Agent. Сервер возвращает значения только в том случае, если установлен и включен совместимый обработчик речи.

Свойства [**Engine**](https://www.bing.com/search?q=**Engine**), [**Installed**](https://www.bing.com/search?q=**Installed**)и [**Language**](https://www.bing.com/search?q=**Language**) больше не поддерживаются, но (для обратной совместимости) возвращает значения NULL при запросе. Чтобы запросить или задать режим распознавания речи, используйте свойство [**срмодеид**](srmodeid-property.md) .

-   [Свойства Спичинпут](speechinput-properties.md)

 

 




